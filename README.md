# F029 vue游戏推荐大数据可视化系统vue+flask+mysql|steam游戏平台可视化

> 完整项目收费，可联系QQ: 81040295 微信: mmdsj186011 注明从github来的，谢谢！
也可以关注我的B站： 麦麦大数据 https://space.bilibili.com/1583208775
> 

关注B站，有好处！
编号:  **F029**
## 视频

[video(video-f7uyWJ1k-1760594132972)(type-bilibili)(url-https://player.bilibili.com/player.html?aid=944050264)(image-https://i-blog.csdnimg.cn/img_convert/76afff6edc5c56699dcc964fc2c729ca.jpeg)(title-超帅vue+python游戏推荐大数据系统源码|协同过滤|可视化|KNN算法|推荐算法|Flask框架|MySQL|沙箱支付|短信接口|OCR识别|爬虫)]

## 1 系统简介
系统简介：本系统是一个基于Vue+Flask构建的游戏推荐与数据分析平台。其核心功能围绕用户管理、游戏推荐和数据可视化展开。主要包括：个性化的登录与注册界面，支持背景视频播放；智能的游戏推荐系统，采用UserCF和ItemCF两种推荐算法；丰富的游戏库和搜索功能，方便用户查找感兴趣的游戏；多维度的数据分析模块，包括游戏评价、类型分布和词云分析等可视化呈现；以及完善的个人设置功能，支持用户信息和头像管理。系统还整合了数据爬虫模块，定期从Steam平台抓取最新游戏数据，确保内容的时效性和准确性。
## 2 功能设计
该系统采用典型的B/S（浏览器/服务器）架构模式。用户通过浏览器访问Vue前端界面，前端由HTML、CSS、JavaScript以及Vue.js生态系统中的Vuex（用于状态管理）、Vue Router（用于路由导航）和ECharts（用于数据可视化）等组件构建。前端通过API请求与Flask后端进行数据交互，Flask后端则负责业务逻辑处理，并利用SQLAlchemy等ORM工具与MySQL数据库进行数据存储。系统还部署了数据爬虫模块，用于从Steam平台抓取游戏数据并导入数据库，为平台提供数据支持。通过AI推荐算法，系统能够根据用户行为和游戏特征进行个性化推荐，为用户带来智能化的游戏推荐体验。
### 2.1系统架构图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/b4dcb3955a4049949e232f1c9b682187.png)
### 2.2 功能模块图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/758e62c686cb477599b45737321c1f55.png)
## 3 功能展示
### 3.1 登录 & 注册
登录注册做的是一个可以切换的登录注册界面，点击去登录后者去注册可以切换，背景是一个视频，循环播放。
登录需要验证用户名和密码是否正确，如果**不正确会有错误提示**。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4311ebcb8d214134b4bafc5051b38603.png)
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/200099b3c5674742a0e7f50c67818050.png)
注册需要**验证用户名是否存在**，如果错误会有提示。
### 3.2 主页
主页的布局采用了左侧是菜单，右侧是操作面板的布局方法，右侧的上方还有用户的头像和退出按钮，如果是新注册用户，没有头像，这边则不显示，需要在个人设置中上传了头像之后就会显示。
### 3.3 推荐算法
采用两种推荐算法，UserCF和ItemCF进行游戏推荐，以卡片形式展示游戏内容。
UserCF推荐：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/82f028cbf5ae4552854efa721a3bc323.png)
ItemCF推荐：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/0a91886606a94ffda020b4826527ac65.png)
展示游戏视频：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/fb15bc61ecc3452fbccdc321ced673a4.png)
### 3.4 游戏库
可以在游戏库中搜索游戏，寻找自己感兴趣的游戏信息：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/d9230926a48d484f8e28ad5bc6ef2e32.png)
搜索游戏：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/6e6d406dbdff4a5a84d10d2137ba3f85.png)
### 3.5 数据分析
这边数据分析也是实现了多种不同的图形，比如
游戏评价：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/21079751e13a4e039d8982277943ba5a.png)
好评、差评
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/ef8a254075224e9a8423f8e0e3d50911.png)
游戏类型散点图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f6b49cdf9d794932926bc32edfe749a8.png)
游戏介绍的词云分析
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/c044a220b0bd4f6d8514abdd9fdf7847.png)
### 3.6 个人设置
个人设置方面包含了用户信息修改、密码修改功能。
用户信息修改中可以上传头像，完成用户的头像个性化设置，也可以修改用户其他信息。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/f59e22973f1b4d39b57ec757aad72f27.png)
修改密码需要输入用户旧密码和新密码，验证旧密码成功后，就可以完成密码修改。
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/4bf27ead4c0d417dac9cef27da18ce06.png)
### 3.7 数据爬虫
可以爬取steam网站更新数据：
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/2e0c12bde8334adabc22db2b7d9f95fc.png)
## 4程序代码
### 4.1 代码说明
代码介绍：数据加载：从CSV文件中读取用户游戏评分数据，并构建用户-游戏评分字典。
余弦相似度计算：衡量用户间的兴趣相似程度。
推荐生成：基于相似用户的评分，为目标用户推荐未评分的游戏。
评估：通过精确率、召回率和F1值评估推荐效果。
### 4.2 流程图
![在这里插入图片描述](https://i-blog.csdnimg.cn/direct/47f0e01fb3c84594863cdb9779babe18.png)
### 4.3 代码实例
```python
import numpy as np
import pandas as pd
from collections import defaultdict

# 数据加载
def load_data(file_path):
    data = pd.read_csv(file_path)
    user_game_dict = defaultdict(dict)
    for _, row in data.iterrows():
        user = row['user_id']
        game = row['game_id']
        rating = row['rating']
        user_game_dict[user][game] = rating
    return user_game_dict

# 计算余弦相似度
def cosine_similarity(user1, user2, user_game_dict):
    games1 = set(user_game_dict[user1].keys())
    games2 = set(user_game_dict[user2].keys())
    common_games = games1.intersection(games2)
    if not common_games:
        return 0
    vector1 = [user_game_dict[user1][g] for g in common_games]
    vector2 = [user_game_dict[user2][g] for g in common_games]
    dot_product = np.dot(vector1, vector2)
    norm1 = np.linalg.norm(vector1)
    norm2 = np.linalg.norm(vector2)
    return dot_product / (norm1 * norm2) if norm1 != 0 and norm2 != 0 else 0

# 生成推荐
def generate_recommendations(target_user, user_game_dict, num_recs=5):
    similarities = {}
    for user in user_game_dict:
        if user != target_user:
            sim = cosine_similarity(target_user, user, user_game_dict)
            if sim > 0:
                similarities[user] = sim
    # 按照相似度排序
    sorted_users = sorted(similarities.items(), key=lambda x: x[1], reverse=True)
    # 收集推荐游戏
    recommended_games = set()
    for user, _ in sorted_users:
        for game, rating in user_game_dict[user].items():
            if game not in user_game_dict[target_user]:
                recommended_games.add(game)
                if len(recommended_games) >= num_recs:
                    break
        if len(recommended_games) >= num_recs:
            break
    return list(recommended_games)[:num_recs]

# 评估推荐效果
def evaluate_recommendations(recommended, actual):
    precision = len(set(recommended) & set(actual)) / len(recommended) if recommended else 0
    recall = len(set(recommended) & set(actual)) / len(actual) if actual else 0
    f1 = 2 * (precision * recall) / (precision + recall) if (precision + recall) != 0 else 0
    return precision, recall, f1

# 主函数
def main():
    # 加载数据
    user_game_dict = load_data('user_game_ratings.csv')
    # 生成推荐
    target_user = 1
    recommended_games = generate_recommendations(target_user, user_game_dict)
    print(f"推荐给用户{target_user}的游戏：{recommended_games}")
    # 评估
    actual_games = list(user_game_dict[target_user].keys())
    precision, recall, f1 = evaluate_recommendations(recommended_games, actual_games)
    print(f"Precision: {precision:.4f}, Recall: {recall:.4f}, F1: {f1:.4f}")

if __name__ == "__main__":
    main()
```
