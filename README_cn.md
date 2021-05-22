# Write-Markdown-Quickly

[English Version](./README.md)

## 必要条件
### 编辑器
- [x] Neovim
- [ ] Vim >= 8.1
### 插件
- [x] [markdown-preview.nvim](https://github.com/iamcco/markdown-preview.nvim)
- [ ] [vim-table-mode](https://github.com/dhruvasagar/vim-table-mode)

### 配置
:point_right: 添加到 `vimrc` 或者 `init.vim`
#### 占位符标记
```vim
" 按两次空格跳到下一个 `<++>` 并对其进行编辑
noremap <LEADER><LEADER> <Esc>/<++><CR>:nohlsearch<CR>c4l
```
#### Markdown snippets
```vim
autocmd Filetype markdown inoremap <buffer> ,f <Esc>/<++><CR>:nohlsearch<CR>"_c4l
autocmd Filetype markdown inoremap <buffer> ,w <Esc>/ <++><CR>:nohlsearch<CR>"_c5l<CR>
autocmd Filetype markdown inoremap <buffer> ,n ---<Enter><Enter>
autocmd Filetype markdown inoremap <buffer> ,b **** <++><Esc>F*hi
autocmd Filetype markdown inoremap <buffer> ,i ** <++><Esc>F*i
autocmd Filetype markdown inoremap <buffer> ,s ~~~~ <++><Esc>F~hi
autocmd Filetype markdown inoremap <buffer> ,d `` <++><Esc>F`i
autocmd Filetype markdown inoremap <buffer> ,c ```<Enter><++><Enter>```<Enter><Enter><++><Esc>4kA
autocmd Filetype markdown inoremap <buffer> ,m - [ ] 
autocmd Filetype markdown inoremap <buffer> ,p ![](<++>) <++><Esc>F[a
autocmd Filetype markdown inoremap <buffer> ,a [](<++>) <++><Esc>F[a
autocmd Filetype markdown inoremap <buffer> ,1 #<Space><Enter><++><Esc>kA
autocmd Filetype markdown inoremap <buffer> ,2 ##<Space><Enter><++><Esc>kA
autocmd Filetype markdown inoremap <buffer> ,3 ###<Space><Enter><++><Esc>kA
autocmd Filetype markdown inoremap <buffer> ,4 ####<Space><Enter><++><Esc>kA
autocmd Filetype markdown inoremap <buffer> ,5 #####<Space><Enter><++><Esc>kA
autocmd Filetype markdown inoremap <buffer> ,6 ######<Space><Enter><++><Esc>kA
autocmd Filetype markdown inoremap <buffer> ,l --------<Enter>
```

| 快捷键 | 作用                   |
|--------|------------------------|
| ,f     | 寻找下一个占位符       |
| ,w     | 寻找下一个占位符并换行 |
| ,n     | 插入水平线并空一行     |
| ,b     | 粗体                   |
| ,i     | 斜体                   |
| ,s     | 给文字加上删除线       |
| ,d     | 包裹代码               |
| ,c     | 包裹代码块             |
| ,m     | 任务清单               |
| ,p     | 插入图片               |
| ,a     | 插入链接               |
| ,1     | 一级标题               |
| ,2     | 二级标题               |
| ,3     | 三级标题               |
| ,4     | 四级标题               |
| ,5     | 五级标题               |
| ,6     | 六级标题               |
| ,l     | 插入水平线             |

#### vim-table-mode
```vim
noremap <LEADER>tm :TableModeToggle<CR>
```
