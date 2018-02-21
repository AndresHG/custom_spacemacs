# custom_spacemacs
Self customized .spacemacs file, with special keybindings for OSX

keybings use lambda functions to insert special characters:
<pre>
  (global-set-key (kbd "s-ç") 'comment-line)
  (global-set-key (kbd "s-3") (lambda () (interactive) (insert "#")))
  (global-set-key (kbd "s-1") (lambda () (interactive) (insert "|")))
  (global-set-key (kbd "s-º") (lambda () (interactive) (insert "\\")))

  (defun duplicate-line()
    (interactive)
    (move-beginning-of-line 1)
    (kill-line)
    (yank)
    (open-line 1)
    (next-line 1)
    (yank)
    )
  (defun delete-line()
    (interactive)
    (move-beginning-of-line 1)
    (kill-line)
    )
  (global-set-key (kbd "s-d") 'duplicate-line)
  (global-set-key (kbd "s-k") 'delete-line)
  )

</pre>

# Installation:

Install Spacemacs from <a href="http://spacemacs.org/">here</a>.

Download spacemacs_customized file and rename it to .spacemacs:

<pre><code> mv spacemacs_customized .spacemacs
</code></pre>

Backup your old .spacemacs:
<pre><code> cp ~/.spacemacs ~/spacemacs.bak
</code></pre>

Overroide old file with de new one:
<pre><code> mv .spacemacs ~/.spacemacs
</code></pre>
