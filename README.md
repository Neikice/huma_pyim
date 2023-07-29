# huma_pyim
虎码输入方案在Emacs中的pyim版本
- 根据虎码官方冰凌输入法的词库生成
- 重排了单字和词的顺序，重码中单字永远在词的前面

## 使用
``` 
(use-package pyim
  :init
  (setq default-input-method "pyim")
  :config
  (pyim-scheme-add
    '(huma
      :document
      "虎码方案"
      :class xingma
      :code-prefix "huma/"
      :first-chars "abcdefghijklmnopqrstuvwxyz"
      :rest-chars "abcdefghijklmnopqrstuvwxyz"
      :code-prefix-history ("_")
      :code-split-length 4
      :code-maximum-length 4))
  ;;----'默认码表'
  (pyim-default-scheme 'huma)
)
```
