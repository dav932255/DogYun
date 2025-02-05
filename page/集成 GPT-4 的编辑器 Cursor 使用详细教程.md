# 集成 GPT-4 的编辑器 Cursor 使用详细教程

## 简介

随着 OpenAI 推出的 ChatGPT 系列语言模型，技术和知识的门槛逐渐降低，未来人们的生活和工作方式也可能会发生重大改变。现在，一个名为 Cursor 的编辑器已经集成了 OpenAI 的 GPT-4，并且还是免费的，它将彻底改变我们编写代码的方式。你可以根据需求直接生成代码、修复 bug、编写注释、提出问题等。

## 使用方法

### 下载安装

Cursor 编辑器提供了 Windows、MacOS 和 Linux 三个平台的安装包，你可以直接从官方下载：

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bbtdd.com/WildCard)

下载后直接安装即可。

### 启动 Cursor

下载安装完成后，系统会引导你进行初始化设置。你可以选择 VIM 或者 Emacs 的操作习惯，也可以保持默认设置。此外，它还支持绑定 Copilot。

### 使用方法

Cursor 是一款极简的编辑器，集成了编程支持的 ChatGPT-4。它的核心命令只有两个：`Generate / Edit` 和 `Chat`，分别表示生成代码和聊天，快捷键分别为 `CTRL+K` 和 `CTRL+L`。

### Edit / CTRL+K

代码编辑/生成功能的快捷键是 `CTRL+K`，你可以直接描述需求，支持中英文输入。

python
snake_x_change = 0
snake_y_change = 0


初始给出的代码有 bug，我添加了两行初始化的代码，现在可以正常运行了。

python
# Python 贪食蛇
import pygame
import random

# 初始化 Pygame
pygame.init()
# 设置窗口大小
window_width = 800
window_height = 600
window = pygame.display.set_mode((window_width, window_height))
# 设置游戏标题
pygame.display.set_caption('Python 贪食蛇')
# 定义颜色
white = (255, 255, 255)
black = (0, 0, 0)
red = (255, 0, 0)
green = (0, 255, 0)
# 定义蛇的初始位置和大小
snake_block_size = 10
snake_speed = 15
snake_list = []
snake_length = 1
snake_x = window_width / 2
snake_y = window_height / 2
snake_x_change = 0
snake_y_change = 0
# 定义食物的初始位置和大小
food_block_size = 10
food_x = round(random.randrange(0, window_width - food_block_size) / 10.0) * 10.0
food_y = round(random.randrange(0, window_height - food_block_size) / 10.0) * 10.0
# 定义字体
font_style = pygame.font.SysFont(None, 30)
# 定义分数
def score(score):
    value = font_style.render('Score: ' + str(score), True, black)
    window.blit(value, [0, 0])
# 定义蛇的形状
def draw_snake(snake_block_size, snake_list):
    for x in snake_list:
        pygame.draw.rect(window, green, [x[0], x[1], snake_block_size, snake_block_size])
# 显示消息
def message(msg, color):
    mesg = font_style.render(msg, True, color)
    window.blit(mesg, [window_width / 6, window_height / 3])
# 游戏循环
game_over = False
while not game_over:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            game_over = True

        # 定义蛇的移动
        if event.type == pygame.KEYDOWN:
            if event.key == pygame.K_LEFT:
                snake_x_change = -snake_block_size
                snake_y_change = 0
            elif event.key == pygame.K_RIGHT:
                snake_x_change = snake_block_size
                snake_y_change = 0
            elif event.key == pygame.K_UP:
                snake_y_change = -snake_block_size
                snake_x_change = 0
            elif event.key == pygame.K_DOWN:
                snake_y_change = snake_block_size
                snake_x_change = 0
    # 判断蛇是否撞到边界
    if snake_x >= window_width or snake_x < 0 or snake_y >= window_height or snake_y < 0:
        game_over = True

    # 移动蛇的位置
    snake_x += snake_x_change
    snake_y += snake_y_change

    # 绘制背景
    window.fill(white)

    # 绘制食物
    pygame.draw.rect(window, red, [food_x, food_y, food_block_size, food_block_size])

    # 绘制蛇
    snake_head = []
    snake_head.append(snake_x)
    snake_head.append(snake_y)
    snake_list.append(snake_head)
    if len(snake_list) > snake_length:
        del snake_list[0]

    for x in snake_list[:-1]:
        if x == snake_head:
            game_over = True
    draw_snake(snake_block_size, snake_list)
    score(snake_length - 1)

    pygame.display.update()

    # 判断蛇是否吃到食物
    if snake_x == food_x and snake_y == food_y:
        food_x = round(random.randrange(0, window_width - food_block_size) / 10.0) * 10.0
        food_y = round(random.randrange(0, window_height - food_block_size) / 10.0) * 10.0
        snake_length += 1

    # 刷新屏幕
    pygame.display.update()

    # 设置游戏速度
    clock = pygame.time.Clock()
    clock.tick(snake_speed)
# 退出 Pygame
pygame.quit()
# 退出程序
quit()


将代码放入 Python 中运行，即可看到效果。

### Chat / CTRL+L

你还可以使用 `CTRL+L` 快捷键与 Cursor 进行聊天，提出问题。

> 新时代已经到来了 …