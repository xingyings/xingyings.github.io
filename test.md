<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>音乐播放器测试页面</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            margin: 0;
            padding: 0;
        }
        table {
            width: 100%;
            border-collapse: collapse;
        }
        th, td {
            border: 1px solid #ddd;
            padding: 8px;
        }
        th {
            background-color: #f2f2f2;
        }
    </style>
</head>
<body>

<div id="content" style="display: none;">
    <h1>音乐播放器测试页面</h1>

    <h2>音乐列表</h2>

    <details>
    <summary>点击展开播放器</summary>

    <table>
      <thead>
        <tr>
          <th>音乐名称</th>
          <th>播放器</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Aoharu</td>
          <td><audio controls id="aoharu"></audio></td>
        </tr>
        <tr>
          <td>Artifact</td>
          <td><audio controls id="artifact"></audio></td>
        </tr>
        <tr>
          <td>Constant Moderato</td>
          <td><audio controls id="constantmoderato"></audio></td>
        </tr>
        <tr>
          <td>Constant Moderato 8bit</td>
          <td><audio controls id="constantmoderato8bit"></audio></td>
        </tr>
        <tr>
          <td>Hello to Halo</td>
          <td><audio controls id="hellotohalo"></audio></td>
        </tr>
        <tr>
          <td>JUMP! BEAT! PLAY! (伴奏)</td>
          <td><audio controls id="jumpbeatplay"></audio></td>
        </tr>
        <tr>
          <td>Raise the Huddle 晄轮大祭运动会·</td>
          <td><audio controls id="raisethehuddle"></audio></td>
        </tr>
        <tr>
          <td>Signal of Abydos</td>
          <td><audio controls id="signalofabydos"></audio></td>
        </tr>
        <tr>
          <td>准备出发! (伴奏)</td>
          <td><audio controls id="zunbeichufa"></audio></td>
        </tr>
      </tbody>
    </table>

    <p>如果无法加载音乐，请尝试更换浏览器或联系管理员：<a href="mailto:admin@xingying.us.kg">admin@xingying.us.kg</a>。</p>
    </details>
</div>

<script>
document.addEventListener("DOMContentLoaded", function() {
    // 获取URL参数
    const urlParams = new URLSearchParams(window.location.search);
    const password = urlParams.get('password');

    if (password === 'admin') {
        // 显示内容
        document.getElementById('content').style.display = 'block';

        // 动态加载音频源
        document.getElementById('aoharu').src = '/music/Aoharu.mp3';
        document.getElementById('artifact').src = '/music/Artifact.mp3';
        document.getElementById('constantmoderato').src = '/music/ConstantModerato.mp3';
        document.getElementById('constantmoderato8bit').src = '/music/ConstantModerato8bit.mp3';
        document.getElementById('hellotohalo').src = '/music/Hello%20to%20Halo.mp3';
        document.getElementById('jumpbeatplay').src = '/music/JUMP!BEAT!PLAY!(伴奏).mp3';
        document.getElementById('raisethehuddle').src = '/music/Raise%20the%20Huddle%20滉轮大祭运动会·.mp3';
        document.getElementById('signalofabydos').src = '/music/Signal%20of%20Abydos.mp3';
        document.getElementById('zunbeichufa').src = '/music/准备出发!(伴奏).mp3';
    } else {
        // 跳转到403页面
        window.location.href = '403.html';
    }
});
</script>

</body>
</html>
