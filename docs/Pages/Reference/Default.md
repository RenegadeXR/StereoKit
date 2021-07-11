---
layout: default
title: Default
description: This is a collection of StereoKit default assets that are created or loaded by StereoKit during its initialization phase! Feel free to use them or Copy them, but be wary about modifying them, since it could affect many things throughout the system.
---
# static class Default

This is a collection of StereoKit default assets that are
created or loaded by StereoKit during its initialization phase! Feel
free to use them or Copy them, but be wary about modifying them,
since it could affect many things throughout the system.




## Static Fields and Properties

|  |  |
|--|--|
|[Tex]({{site.url}}/Pages/Reference/Tex.html) [Cubemap]({{site.url}}/Pages/Reference/Default/Cubemap.html)|The default cubemap that StereoKit generates, this is the cubemap that's visible as the background and initial scene lighting.|
|[Font]({{site.url}}/Pages/Reference/Font.html) [Font]({{site.url}}/Pages/Reference/Default/Font.html)|The default font used by StereoKit's text. This varies from platform to platform, but is typically a sans-serif general purpose font, such as Segoe UI.|
|[Material]({{site.url}}/Pages/Reference/Material.html) [Material]({{site.url}}/Pages/Reference/Default/Material.html)|The default material! This is used by many models and meshes rendered from within StereoKit. Its shader is tuned for high performance, and may change based on system performance characteristics, so it can be great to copy this one when creating your own materials! Or if you want to override StereoKit's default material, here's where you do it!|
|[Material]({{site.url}}/Pages/Reference/Material.html) [MaterialEquirect]({{site.url}}/Pages/Reference/Default/MaterialEquirect.html)|This material is used for projecting equirectangular textures into cubemap faces. It's probably not a great idea to change this one much!|
|[Material]({{site.url}}/Pages/Reference/Material.html) [MaterialFont]({{site.url}}/Pages/Reference/Default/MaterialFont.html)|This material is used as the default for rendering text! By default, it uses the 'default/shader_font' shader, which is a two-sided alpha-clip shader. This also turns off backface culling.|
|[Material]({{site.url}}/Pages/Reference/Material.html) [MaterialHand]({{site.url}}/Pages/Reference/Default/MaterialHand.html)|This is the default material for rendering the hand! It's a copy of the default material, but set to transparent, and using a generated texture.|
|[Material]({{site.url}}/Pages/Reference/Material.html) [MaterialPBR]({{site.url}}/Pages/Reference/Default/MaterialPBR.html)|The default Physically Based Rendering material! This is used by StereoKit anytime a mesh or model has metallic or roughness properties, or needs to look more realistic. Its shader may change based on system performance characteristics, so it can be great to copy this one when creating your own materials! Or if you want to override StereoKit's default PBR behavior, here's where you do it! Note that the shader used by default here is much more costly than Default.Material.|
|[Material]({{site.url}}/Pages/Reference/Material.html) [MaterialUI]({{site.url}}/Pages/Reference/Default/MaterialUI.html)|The material used by the UI! By default, it uses a shader that creates a 'finger shadow' that shows how close the finger is to the UI.|
|[Material]({{site.url}}/Pages/Reference/Material.html) [MaterialUIBox]({{site.url}}/Pages/Reference/Default/MaterialUIBox.html)|A material for indicating interaction volumes! It renders a border around the edges of the UV coordinates that will 'grow' on proximity to the user's finger. It will discard pixels outside of that border, but will also show the finger shadow. This is meant to be an opaque material, so it works well for depth LSR.  This material works best on cube-like meshes where each face has UV coordinates from 0-1.  Shader Parameters: ```color                - color border_size          - meters border_size_grow     - meters border_affect_radius - meters```|
|[Material]({{site.url}}/Pages/Reference/Material.html) [MaterialUnlit]({{site.url}}/Pages/Reference/Default/MaterialUnlit.html)|The default unlit material! This is used by StereoKit any time a mesh or model needs to be rendered with an unlit surface. Its shader may change based on system performance characteristics, so it can be great to copy this one when creating your own materials! Or if you want to override StereoKit's default unlit behavior, here's where you do it!|
|[Material]({{site.url}}/Pages/Reference/Material.html) [MaterialUnlitClip]({{site.url}}/Pages/Reference/Default/MaterialUnlitClip.html)|The default unlit material with alpha clipping! This is used by StereoKit for unlit content with transparency, where completely transparent pixels are discarded. This means less alpha blending, and fewer visible alpha blending issues! In particular, this is how Sprites are drawn. Its shader may change based on system performance characteristics, so it can be great to copy this one when creating your own materials! Or if you want to override StereoKit's default unlit clipped behavior, here's where you do it!|
|[Mesh]({{site.url}}/Pages/Reference/Mesh.html) [MeshCube]({{site.url}}/Pages/Reference/Default/MeshCube.html)|A cube with dimensions of (1,1,1), this is equivalent to Mesh.GenerateCube(Vec3.One).|
|[Mesh]({{site.url}}/Pages/Reference/Mesh.html) [MeshQuad]({{site.url}}/Pages/Reference/Default/MeshQuad.html)|A default quad mesh, 2 triangles, 4 verts, from (-0.5,-0.5,0) to (0.5,0.5,0) and facing forward on the Z axis (0,0,-1). White vertex colors, and UVs from (1,1) at vertex (-0.5,-0.5,0) to (0,0) at vertex (0.5,0.5,0).|
|[Mesh]({{site.url}}/Pages/Reference/Mesh.html) [MeshScreenQuad]({{site.url}}/Pages/Reference/Default/MeshScreenQuad.html)|A default quad mesh designed for full-screen rendering. 2 triangles, 4 verts, from (-1,-1,0) to (1,1,0) and facing backwards on the Z axis (0,0,1). White vertex colors, and UVs from (0,0) at vertex (-1,-1,0) to (1,1) at vertex (1,1,0).|
|[Mesh]({{site.url}}/Pages/Reference/Mesh.html) [MeshSphere]({{site.url}}/Pages/Reference/Default/MeshSphere.html)|A sphere mesh with a diameter of 1. This is equivalent to Mesh.GenerateSphere(1,4).|
|[Shader]({{site.url}}/Pages/Reference/Shader.html) [Shader]({{site.url}}/Pages/Reference/Default/Shader.html)|This is a fast, general purpose shader. It uses a texture for 'diffuse', a 'color' property for tinting the material, and a 'tex_scale' for scaling the UV coordinates. For lighting, it just uses a lookup from the current cubemap.|
|[Shader]({{site.url}}/Pages/Reference/Shader.html) [ShaderEquirect]({{site.url}}/Pages/Reference/Default/ShaderEquirect.html)|A shader for projecting equirectangular textures onto cube faces! This is for equirectangular texture loading.|
|[Shader]({{site.url}}/Pages/Reference/Shader.html) [ShaderFont]({{site.url}}/Pages/Reference/Default/ShaderFont.html)|A shader for text! Right now, this will render a font atlas texture, and perform alpha-testing for transparency, and super-sampling for better readability. It also flips normals of the back-face of the surface, so  backfaces get lit properly when backface culling is turned off, as it is by default for text.|
|[Shader]({{site.url}}/Pages/Reference/Shader.html) [ShaderPbr]({{site.url}}/Pages/Reference/Default/ShaderPbr.html)|A physically based shader.|
|[Shader]({{site.url}}/Pages/Reference/Shader.html) [ShaderUI]({{site.url}}/Pages/Reference/Default/ShaderUI.html)|A shader for UI or interactable elements, this'll be the same as the Shader, but with an additional finger 'shadow' and distance circle effect that helps indicate finger distance from the surface of the object.|
|[Shader]({{site.url}}/Pages/Reference/Shader.html) [ShaderUIBox]({{site.url}}/Pages/Reference/Default/ShaderUIBox.html)|A shader for indicating interaction volumes! It renders a border around the edges of the UV coordinates that will 'grow' on proximity to the user's finger. It will discard pixels outside of that border, but will also show the finger shadow. This is meant to be an opaque shader, so it works well for depth LSR.  This shader works best on cube-like meshes where each face has UV coordinates from 0-1.  Shader Parameters: ```color                - color border_size          - meters border_size_grow     - meters border_affect_radius - meters```|
|[Shader]({{site.url}}/Pages/Reference/Shader.html) [ShaderUnlit]({{site.url}}/Pages/Reference/Default/ShaderUnlit.html)|Sometimes lighting just gets in the way! This is an extremely simple and fast shader that uses a 'diffuse' texture and a 'color' tint property to draw a model without any lighting at all!|
|[Shader]({{site.url}}/Pages/Reference/Shader.html) [ShaderUnlitClip]({{site.url}}/Pages/Reference/Default/ShaderUnlitClip.html)|Sometimes lighting just gets in the way! This is an extremely simple and fast shader that uses a 'diffuse' texture and a 'color' tint property to draw a model without any lighting at all! This shader will also discard pixels with an alpha of zero.|
|[Sound]({{site.url}}/Pages/Reference/Sound.html) [SoundClick]({{site.url}}/Pages/Reference/Default/SoundClick.html)|A default click sound that lasts for 300ms. It's a procedurally generated sound based on a mouse press, with extra low frequencies in it.|
|[Sound]({{site.url}}/Pages/Reference/Sound.html) [SoundUnclick]({{site.url}}/Pages/Reference/Default/SoundUnclick.html)|A default click sound that lasts for 300ms. It's a procedurally generated sound based on a mouse release, with extra low frequencies in it.|
|[Tex]({{site.url}}/Pages/Reference/Tex.html) [Tex]({{site.url}}/Pages/Reference/Default/Tex.html)|Default 2x2 white opaque texture, this is the texture referred to as 'white' in the shader texture defaults.|
|[Tex]({{site.url}}/Pages/Reference/Tex.html) [TexBlack]({{site.url}}/Pages/Reference/Default/TexBlack.html)|Default 2x2 black opaque texture, this is the texture referred to as 'black' in the shader texture defaults.|
|[Tex]({{site.url}}/Pages/Reference/Tex.html) [TexFlat]({{site.url}}/Pages/Reference/Default/TexFlat.html)|Default 2x2 flat normal texture, this is a normal that faces out from the, face, and has a color value of (0.5,0.5,1). This is the texture referred to as 'flat' in the shader texture defaults.|
|[Tex]({{site.url}}/Pages/Reference/Tex.html) [TexGray]({{site.url}}/Pages/Reference/Default/TexGray.html)|Default 2x2 middle gray (0.5,0.5,0.5) opaque texture, this is the texture referred to as 'gray' in the shader texture defaults.|
|[Tex]({{site.url}}/Pages/Reference/Tex.html) [TexRough]({{site.url}}/Pages/Reference/Default/TexRough.html)|Default 2x2 roughness color (0,0,1) texture, this is the texture referred to as 'rough' in the shader texture defaults.|

