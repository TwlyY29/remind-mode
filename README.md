# remind-mode

Emacs Major-Mode for Editing Remind Files.

Is very minimal, only does enough highlighting to be useful.

Has a few functions to input dates a little easier and for running
`remind` on the current file.

Put this in your configuration once `remind-mode.el` is installed:

```elisp
(require 'remind-mode)
(add-to-list 'auto-mode-alist '("\\.rem\\'" . remind-mode))
(setq auto-mode-alist
     (cons '(".reminders$" . remind-mode) auto-mode-alist))
```


Suggested keybindings and available functions:

```elisp
(define-key remind-mode-map (kbd "C-c C-t") 'rem-today)
(define-key remind-mode-map (kbd "C-c C-w") 'rem-week-away)
(define-key remind-mode-map (kbd "C-c C-W") 'rem-weeks-away)
(define-key remind-mode-map (kbd "C-c C-x") 'rem-tomorrow)
(define-key remind-mode-map (kbd "C-c C-a") 'rem-days-away)
(define-key remind-mode-map (kbd "C-c C-k") 'rem-run)
(define-key remind-mode-map (kbd "C-c C-K") 'rem-run-calendar)
```
