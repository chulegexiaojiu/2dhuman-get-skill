# 实际提示词组装模板

将下列占位符替换为具体描述。块A/C/D为固定风格约束；块B负责人物差异。不能遗留占位符。中文设计依据留在提示词文件前部，英文完整正文作为工具prompt。此模板用于有图参考的续作，不宣称逐字复现首次无参考生成。

## A｜参考图职责与构图（固定）

Create ONE full-body 2D side-scrolling pixel-art character illustration. The FIRST reference image is the approved STYLE ANCHOR: closely match its visible pixel-cluster rendering, edge treatment, detail density, grounded stylized anatomy, muted palette relationships, upper-left lighting, simple gray background, framing and presentation. Match the actual reference image rather than a generic interpretation of pixel art.

[REFERENCE_ROLE]

One character only, facing RIGHT in a clear side-view gameplay silhouette, torso allowed a slight turn toward the viewer. Orthographic side elevation, camera at torso height, NOT isometric and NOT top-down. Landscape composition. The figure occupies approximately 80–85 percent of image height, with clear margins around all hair, footwear, clothing and weapons. Both feet rest on one horizontal ground baseline. Preserve the full weapon silhouette without cropping.

## B｜人物设定（按角色替换）

Character: [ROLE_AND_WORLD].
Visible personal identity: [AGE_GENDER_BUILD_FACE_HAIR_SKIN].
Story expressed through visual design: [TWO_OR_THREE_HISTORY_TO_DESIGN_CONNECTIONS].
Clothing and equipment stage: [LAYERS_MATERIALS_CUT_PALETTE_WEAR].
Weapons and signature objects: [WEAPONS_CARRY_PLACEMENT_AND_GRIP].
Pose and expression: [GROUNDED_IDLE_POSE_AND_EXPRESSION].
Character-specific exclusions: [FORBIDDEN_ITEMS_OR_WRONG_FACTION_MARKERS].

## C｜画法（固定）

Grounded dark Western-fantasy character concept rendered as detailed 2D pixel art in the same visual family as the reference. Realistic-stylized human proportions, approximately six to seven heads tall, not chibi. Visible deliberate pixel clusters, crisp stepped contours, restrained selective dark outlines, carefully grouped material shadows and small highlights. Match the reference's level of detail, without adding tiny noisy texture or converting the image into smooth digital painting. Muted earth-toned palette; choose role-appropriate clothing colors rather than copying the hunter's green costume. Natural skin tones, coherent upper-left light. A simple nearly uniform light warm-gray to neutral-gray background and a small pixel-styled contact shadow under the boots. No scenery. Readable silhouette, distinct limbs, coherent hands and practical equipment construction.

## D｜排除（固定）

No photorealism, no 3D render, no smooth painterly brushwork, no generic mosaic filter, no blurry edges, no glossy plastic materials, no chibi proportions, no isometric view, no top-down camera, no front-facing portrait composition, no dramatic perspective foreshortening, no cinematic landscape, no text, no labels, no watermark, no logo, no UI, no border, no multiple characters, no sprite sheet, no extra limbs, no cropped feet or weapons. Do not invent costume changes inconsistent with the character brief.

## REFERENCE_ROLE 的两种替换

### 新角色，只传风格图
The reference hunter is NOT the requested identity. Transfer the art style and presentation ONLY. Do not copy his face, hairstyle, green tunic, bow, quiver or accessories unless the new character brief explicitly requests them. Design a clearly distinct individual with the correct class-specific silhouette.

### 同一角色续作，有第二张人物图
The SECOND reference image defines the character identity, facial features, hair, clothing construction and signature equipment. Preserve those features while using the FIRST image for style and presentation. Make only the changes explicitly listed in the character brief. Do not blend the hunter's identity or equipment into this character.

若用户续作的就是锚点猎手：只传锚点一次，将参考职责改为“The reference defines BOTH the approved style and this hunter's identity. Preserve his identity and equipment except for the explicitly requested changes.”

## 防止模型语法误用
默认是自然语言提示词。不使用未证实有效的 --ar、--seed、LoRA标签或SD权重语法；不假定 generate_image 支持负面提示词独立字段。尺寸等工具参数以实际schema为准。
