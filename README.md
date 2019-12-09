[![MELPA](http://melpa.org/packages/ivy-fuz-badge.svg)](http://melpa.org/#/ivy-fuz)
[![MELPA Stable](http://stable.melpa.org/packages/ivy-fuz-badge.svg)](http://stable.melpa.org/#/ivy-fuz)

# ivy-fuz.el

Emacs integration between [fuz](https://github.com/rustify-emacs/fuz.el) and [ivy](https://github.com/abo-abo/swiper).

## Installation

The recommended way to install ivy-fuz.el is through [MELPA](https://github.com/milkypostman/melpa).

You'll need a working fuz installation (https://github.com/rustify-emacs/fuz.el).

## Quickstart

### Elisp

``` elisp
(setq ivy-sort-matches-functions-alist '((t . ivy-fuz-sort-fn)))
(setq ivy-re-builders-alist '((t . ivy-fuz-regex-fuzzy)))
(with-eval-after-load 'ivy
  (require 'ivy-fuz)
  (add-to-list 'ivy-highlight-functions-alist '(ivy-fuz-regex-fuzzy . ivy-fuz-highlight-fn)))
```

### Use-Package

Here is a example [use-package](https://github.com/jwiegley/use-package) configuration:

``` elisp
(use-package ivy-fuz
  :ensure t
  :demand t
  :after ivy
  :custom
  (ivy-sort-matches-functions-alist '((t . ivy-fuz-sort-fn)))
  (ivy-re-builders-alist '((t . ivy-fuz-regex-fuzzy)))
  :config
  (add-to-list 'ivy-highlight-functions-alist '(ivy-fuz-regex-fuzzy . ivy-fuz-highlight-fn)))
```

## Contributions

They are very welcome, either as suggestions or as pull requests by opening tickets
on the [issue tracker](https://github.com/Silex/ivy-fuz.el/issues).
