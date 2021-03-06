[![Build Status](https://travis-ci.org/voku/PHPMailer-BMH.svg?branch=master)](https://travis-ci.org/voku/PHPMailer-BMH)
[![codecov.io](http://codecov.io/github/voku/PHPMailer-BMH/coverage.svg?branch=master)](http://codecov.io/github/voku/PHPMailer-BMH?branch=master)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/voku/PHPMailer-BMH/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/voku/PHPMailer-BMH/?branch=master)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/64177eb1d95948789a1fb54b97e0ed21)](https://www.codacy.com/app/voku/PHPMailer-BMH)
[![SensioLabsInsight](https://insight.sensiolabs.com/projects/2161b4c1-5025-4e29-ae22-1f91c3a6657c/mini.png)](https://insight.sensiolabs.com/projects/2161b4c1-5025-4e29-ae22-1f91c3a6657c)
[![Latest Stable Version](https://poser.pugx.org/voku/bounce-mail-handler/v/stable)](https://packagist.org/packages/voku/bounce-mail-handler)
 [![Total Downloads](https://poser.pugx.org/voku/bounce-mail-handler/downloads)](https://packagist.org/packages/voku/bounce-mail-handler)
[![Latest Unstable Version](https://poser.pugx.org/voku/bounce-mail-handler/v/unstable)](https://packagist.org/packages/voku/bounce-mail-handler)
[![License](https://poser.pugx.org/voku/bounce-mail-handler/license)](https://packagist.org/packages/voku/bounce-mail-handler)

* PHP 7.0+ Support
* Composer & PSR-0 Support
* PHPUnit testing via Travis CI (TODO: more tests needed)
* PHP-Quality testing via SensioLabsInsight (TODO: more fixes needed)

# Bounce Mail Handler

WARNING: This is a Extended-Fork of:
* instaclick's [PHPMailer-BMH](https://github.com/instaclick/PHPMailer-BMH) what is on the other hand a Fork of WorxWare's [PHPMailer-BMH](http://sourceforge.net/projects/bmh/).
* voku's [PHPMailer-BMH](https://github.com/voku/PHPMailer-BMH)
* mfrascati's [PHPMailer-BMH](https://github.com/mfrascati/PHPMailer-BMH)

## Installation

The recommended installation way is through [Composer](https://getcomposer.org).

```bash
$ composer require jonnylor63/bounce-mail-handler
```

## Examples

[https://github.com/jonnylor63/PHPMailer-BMH/tree/main/examples](https://github.com/jonnylor63/PHPMailer-BMH/tree/main/examples)

If bounce_type is "hard" the process use $bmh->moveHard and $bmh->hardMailbox
If bounce_type is "soft" the process use $bmh->moveSoft and $bmh->softMailbox
If bounce_type different from "hard" and "soft" the process use $bmh->moveOther and $bmh->otherMailbox

The email process try to understand :
1. standard DSN msg
2. not standard DSN msg
3. didn't get content-type header

If process fail the email will be deleted only if disableDelete is false and purgeUnprocessed is true