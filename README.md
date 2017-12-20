#Modified Standard Shader


Modifying the Unity standard shader is an incredibly powerful method of experimention and sandboxing in a physically based renderer. Since the entire builtin shader library is [completely available for anyone](https://beta.unity3d.com/download/d3a5469e8c44/builtin_shaders-2017.3.0f2.zip?_ga=2.40447906.1489711827.1513789478-1507371053.1498079315), users can  reach nearly every corner of the Unity shading pipeline.


The general idea of modifying the standard shader, I've found, is to start with a carbon copy of Standard .shader file (available in link), then drop in the discrete .CGINC files that you want to override (also in link). 
Due to the nature of the Unity shader compiler, if these files all live in the same directory in your project, Unity will use those ones instead for the shader, instead of the builtin ones.


This project contains a very simple, tip of the iceberg example, simply overriding the directional light shading pass at line 451 in UnityStandardCore.cginc. 