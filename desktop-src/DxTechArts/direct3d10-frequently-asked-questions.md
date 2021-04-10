---
title: 'Direct3D 10 : Forum Aux Questions'
description: Cet article contient certaines des questions fréquemment posées concernant Direct3D 10, du point de vue d’un développeur qui Portage une application existante de Direct3D 9 (D3D9) vers Direct3D 10 (D3D10).
ms.assetid: da3022ca-b120-d0d7-6747-65b946dbc73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae228923715400e5ba7e4f795e3ea6bfacfd98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101897"
---
# <a name="direct3d-10-frequently-asked-questions"></a>Direct3D 10 : Forum Aux Questions

Cet article contient certaines des questions fréquemment posées concernant Direct3D 10, du point de vue d’un développeur qui Portage une application existante de Direct3D 9 (D3D9) vers Direct3D 10 (D3D10).

-   [Mémoires tampons constantes](#constant-buffers)
-   [State](#state)
-   [Formats](#formats)
-   [Liaison de nuanceur](#shader-linkage)
-   [Appels de dessin](#draw-calls)
-   [Ressources](#resources)
-   [Profondeur comme texture](#depth-as-texture)
-   [MSAA](#msaa)
-   [Crashes](#crashes)
-   [Rendu prédicat](#predicated-rendering)
-   [Nuanceur de géométrie](#geometry-shader)
-   [HLSL](#hlsl)

## <a name="constant-buffers"></a>Mémoires tampons constantes

<dl> <dt>

<span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>Quelle est la meilleure façon de mettre à jour les mémoires tampons constantes ?
</dt> <dd>

UpdateSubresource et Map with Discard doivent être à la même vitesse. Choisissez entre elles en fonction de laquelle une copie la plus petite quantité de mémoire. Si vos données sont déjà stockées en mémoire dans un bloc contigu, utilisez UpdateSubresource. Si vous devez accumuler des données à partir d’autres emplacements, utilisez la fonction Map with Discard.

</dd> <dt>

<span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>Quelle est la pire façon d’organiser les mémoires tampons constantes ?
</dt> <dd>

Les pires performances sont obtenues en plaçant toutes les constantes d’un nuanceur particulier dans une mémoire tampon constante. Bien qu’il s’agisse souvent du moyen le plus simple de portage de D3D9 vers D3D10, cela peut paralyser les performances. Par exemple, imaginez un scénario qui utilise la mémoire tampon constante suivante :

``` syntax
cbuffer VSGlobalsCB
{
    matrix  ViewProj;
    matrix  Bones[100];
    matrix  World;
    float   SpecPower;
    float4  BDRFCoefficients;
    float   AppTime;
    uint2   RenderTargetSize;
};
```

La mémoire tampon est de 6560 octets. Supposons qu’il existe une application avec 1000 objets à restituer, 100 qui sont des maillages dépouillés et 900 de maillages statiques. Par ailleurs, supposons que cette application utilise le mappage Shadow avec une source de lumière. Cela signifie qu’il y a deux passes, une pour la carte de profondeur rendue à partir de la lumière et une pour la passe de rendu avant. Cela provoque des appels 2000 Draw. Bien que chaque appel de dessin n’ait pas besoin de mettre à jour toutes les parties de la mémoire tampon constante, la totalité de la mémoire tampon constante est toujours mise à jour et envoyée à la carte. Cela entraîne la mise à jour de 13 Mo de données toutes les trames (2000 de dessin appelle l’heure 6560 Ko).

</dd> <dt>

<span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>Quelle est la meilleure façon d’organiser mes mémoires tampons constantes ?
</dt> <dd>

Le meilleur moyen consiste à organiser des mémoires tampons constantes par fréquence de mise à jour. Les constantes mises à jour à des fréquences similaires doivent se trouver dans la même mémoire tampon. Par exemple, considérez le scénario présenté sous, « quel est le pire moyen d’organiser les mémoires tampons constantes ? », mais avec une meilleure disposition constante :

``` syntax
cbuffer VSGlobalPerFrameCB
  { 
    float   AppTime; 
  };
cbuffer VSPerSkinnedCB
  { 
    matrix  Bones[100]; 
  };
cbuffer VSPerStaticCB
  {
    matrix  World;
  };
cbuffer VSPerPassCB
  {
    matrix  ViewProj;
    uint2   RenderTargetSize;
  };
cbuffer VSPerMaterialCB
  {
    float   SpecPower;
    float4  BDRFCoefficients;
  };    
```

Les mémoires tampons constantes sont divisées en fonction de leur fréquence de mise à jour, mais ce n’est que la moitié de la solution. L’application doit mettre à jour les mémoires tampons constantes correctement afin de tirer pleinement parti du fractionnement. Nous allons supposer la même scène que ci-dessus : 900 maillages statiques, 100 maillages dépouillés, un passe de lumière et une passe directe. Nous supposons également que certaines mémoires tampons constantes par objet seront stockées. Cela signifie que chaque objet contiendra soit un VSPerSkinnedCB, soit un VSPerStaticCB, selon qu’il est dépouillé ou statique. Nous faisons cela pour éviter le double de la quantité de matrices envoyées via le pipeline.

Nous séparons le cadre en trois phases. La première phase est le début du frame et ne nécessite pas de rendu, juste des mises à jour constantes.

<dl> <dt>

<span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Frame de début**
</dt> <dd>

-   Mettre à jour VSGlobalPerFrameCB pour l’heure de l’application (4 octets)
-   Mise à jour 100 VSPerSkinnedCB pour les objets dépouillés 100 (640000 octets)
-   Mettre à jour VSPerStaticCB pour 900 objets statiques (57600 octets)

L’étape suivante est le passage de la table fictive. Notez que la seule mémoire tampon constante qui est réellement mise à jour est VSPerPassCB. Toutes les autres mémoires tampons constantes ont été mises à jour pendant le passage de frame de début. Bien que nous ayons toujours besoin de lier ces mémoires tampons constantes, la quantité d’informations transmises à la carte vidéo est minime, car les tampons ont déjà été mis à jour.

</dd> <dt>

<span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Passe-miroir**
</dt> <dd>

-   Mettre à jour VSPerPassCB (72 octets)
-   Dessiner 100 maillages dépouillés (100 liaisons, aucune mise à jour)
-   Dessiner 900 mailles statiques (100 liaisons, aucune mise à jour)

De même, le test de rendu de transfert doit uniquement mettre à jour les données par matériau, car il n’a pas été stocké par maillage. Si nous partons du principe qu’il existe 500 matériaux en cours d’utilisation dans la scène :

</dd> <dt>

<span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Transfert direct**
</dt> <dd>

-   Mettre à jour VSPerPassCB (72 octets)
-   Mise à jour 500 VSPerMaterialCBs (10000 octets)

Il en résulte un total de 707 Ko seulement. Bien qu’il s’agisse d’un scénario très fictif, il illustre simplement la quantité de surcharge de mise à jour constante pouvant être réduite en triant les constantes par fréquence de mise à jour.

</dd> </dl> </dd> <dt>

<span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>Que se passe-t-il si je n’ai pas suffisamment d’espace pour stocker des mémoires tampons constantes pour mes maillages, notre matériel, etc. ? 
</dt> <dd>

Vous pouvez toujours utiliser un système à plusieurs niveaux de mémoires tampons constantes. Créez des mémoires tampons constantes de taille variable (16 octets, 32 octets, 64 octets, etc.) jusqu’à la plus grande taille de mémoire tampon constante nécessaire. Lorsqu’il est temps de lier une mémoire tampon constante à un nuanceur, sélectionnez la plus petite mémoire tampon constante qui peut contenir les données requises par le nuanceur. Bien que cette approche soit légèrement moins efficace, il s’agit d’une bonne étape intermédiaire.

</dd> <dt>

<span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>Je partage des mémoires tampons constantes entre différents nuanceurs. Un nuanceur peut utiliser toutes les constantes, mais un autre peut utiliser certaines des constantes. Quelle est la meilleure façon de les mettre à jour ? 
</dt> <dd>

Une approche consiste à fractionner le tampon constant encore plus loin. Toutefois, il y a un point où trop de mémoires tampons constantes sont liées. Dans ce cas, déplacez les constantes qui sont susceptibles d’être inutilisées par plusieurs nuanceurs jusqu’à la fin de la mémoire tampon constante. Lors de l’obtention des données de la variable à partir du nuanceur, utilisez l' \_ indicateur D3D10 SVF \_ used de la \_ variable de nuanceur D3D10 \_ \_ desc pour déterminer si la variable est utilisée. En plaçant les variables inutilisées à la fin de la mémoire tampon constante, vous pouvez lier une mémoire tampon plus petite au nuanceur qui n’utilise pas ces variables, ce qui permet d’économiser les coûts de mise à jour.

</dd> <dt>

<span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>Combien puis-je améliorer la fréquence d’images si je charge uniquement les segments de mon caractère une fois par image au lieu d’une fois par passe/dessin ? 
</dt> <dd>

Vous pouvez améliorer la fréquence d’images comprise entre 8% et 50% en fonction de la quantité de données redondantes. Dans le pire des cas, les performances ne seront pas réduites.

</dd> <dt>

<span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>Combien de mémoires tampons constantes dois-je lier en même temps ? 
</dt> <dd>

Liez le nombre minimal de mémoires tampons constantes nécessaires à l’extraction de toutes vos données dans le nuanceur. Dans un scénario réaliste, cinq est le nombre recommandé de mémoires tampons constantes à utiliser. Le partage de mémoires tampons constantes entre les nuanceurs (en liant le même CB aux VS et PS) peut également améliorer les performances.

</dd> <dt>

<span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>Y a-t-il un coût pour la liaison de mémoires tampons constantes sans les utiliser ? 
</dt> <dd>

Oui, si vous ne prévoyez pas d’utiliser la mémoire tampon, n’appelez pas VSSetConsantBuffer ou PSSetConstantBuffer. Cette surcharge d’API supplémentaire peut être ajoutée au cours de plusieurs appels de dessin.

</dd> </dl>

## <a name="state"></a>State

<dl> <dt>

<span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>Quelle est la meilleure façon de gérer l’État dans D3D10 ? 
</dt> <dd>

La meilleure solution consiste à connaître l’ensemble de votre état en amont et à créer les objets d’État en amont. Cela signifie qu’au moment du rendu, la liaison d’État est la seule opération qui doit se produire. D3D10 filtre également les doublons.

</dd> <dt>

<span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>Mon jeu a été chargé dynamiquement ou possède du contenu généré par l’utilisateur. Je ne peux pas charger tous mes objets d’État en amont. Que dois-je faire ? 
</dt> <dd>

Il existe deux solutions ici. La première consiste à créer des objets d’État à la volée et à laisser D3D10 filtrer les doublons. Toutefois, cela n’est pas recommandé pour les scénarios avec de nombreuses modifications d’objets d’État par frame. Une meilleure solution consiste à hacher les objets d’État vous-même et à créer un objet d’état uniquement s’il est introuvable dans la table de hachage. Le raisonnement derrière l’utilisation d’une table de hachage personnalisée est qu’une application peut sélectionner un hachage rapide basé sur le scénario d’utilisation spécifique à cette application. Par exemple, si une application modifie uniquement le rendertargetwritemask dans le BlendState et conserve toutes les autres valeurs de la même façon, l’application peut générer un hachage à partir du rendertargetwritemask au lieu de la structure entière.

</dd> <dt>

<span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>L’état de AlphaTest a disparu. Où se trouve-t-il ? 
</dt> <dd>

AlphaTest doit maintenant avoir des performances dans le nuanceur. Consultez l’exemple FixedFuncEMU.

</dd> <dt>

<span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>Qu’est-il arrivé aux plans de clip utilisateur ? 
</dt> <dd>

Les plans de clip utilisateur ont été déplacés dans le nuanceur. Il existe deux façons de gérer cela. La première consiste à générer une sortie \_ de SV ClipDistance à partir du nuanceur de sommets ou du nuanceur de géométrie. L’autre option consiste à utiliser ignorer dans le nuanceur de pixels en fonction d’une valeur passée par le nuanceur de sommets ou le nuanceur de géométrie. Expérimentez les deux pour voir qui est plus rapide pour votre scénario particulier. L’utilisation de SV \_ ClipDistance peut entraîner l’utilisation par le matériel d’une routine de découpage basée sur la géométrie qui peut entraîner des appels de dessin liés à la géométrie pour s’exécuter plus lentement. De même, l’utilisation de l’opération ignorer déplace le travail vers le nuanceur de pixels, ce qui peut ralentir l’exécution des appels de dessin liés aux pixels.

</dd> <dt>

<span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>Efface ne respecte pas les paramètres d’État, tels que les paramètres des rectangles ciseaux dans mon état de rastériseur. 
</dt> <dd>

Les effacs ont été séparés de l’état du pipeline. Pour obtenir un comportement de style D3D9, émule les effaces en dessinant un quadruple écran plein écran.

</dd> <dt>

<span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>Je définis mes États sur par défaut pour essayer et diagnostiquer une erreur de rendu. À présent, mon écran affiche le noir, bien que je sache que je dessine des objets sur l’écran. 
</dt> <dd>

Lors de la définition de l’État sur les valeurs par défaut (NULL), assurez-vous que le SampleMask dans l’appel à OMSetBlendState n’est jamais égal à zéro. Si SampleMask a la valeur zéro, tous les échantillons sont logiquement et avec zéro. Dans ce scénario, aucun échantillon ne passera le test Blend.

</dd> <dt>

<span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>Où l’état de D3DSAMP SRGBTEXTURE est- \_ il atteint ? 
</dt> <dd>

SRVB a été supprimé dans le cadre de l’état de l’échantillonneur et est maintenant lié au format de texture. La liaison d’une texture sRVB aura pour résultat le même échantillonnage que celui obtenu si vous avez spécifié D3DSAMP \_ SRGBTEXTURE dans Direct3D 9.

</dd> </dl>

## <a name="formats"></a>Formats

<dl> <dt>

<span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>Quel format D3D9 correspond au format D3D10 ? 
</dt> <dd>

Pour plus d’informations, consultez [considérations relatives à Direct3D 9 vers Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).

</dd> <dt>

<span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>Qu’est-il arrivé aux formats de texture A8R8G8B8 ? 
</dt> <dd>

Ils ont été dépréciés dans D3D10. Vous pouvez resourcer vos Textures en tant que R8G8B8A8, ou vous pouvez Swizzle au chargement, ou vous pouvez Swizzle dans le nuanceur.

</dd> <dt>

<span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>Comment faire utiliser des textures en palette ? 
</dt> <dd>

Placez votre palette de couleurs dans une texture ou dans une mémoire tampon constante et liez-la au pipeline. Dans le nuanceur de pixels, effectuez une recherche indirecte à l’aide de l’index dans votre texture en palette.

</dd> <dt>

<span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>Quels sont ces nouveaux formats sRVB ? 
</dt> <dd>

SRVB a été supprimé dans le cadre de l’état de l’échantillonneur et est maintenant lié au format de texture. La liaison d’une texture sRVB aura pour résultat le même échantillonnage que celui obtenu si vous avez spécifié D3DSAMP \_ SRGBTEXTURE dans Direct3D 9.

</dd> <dt>

<span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>Où les fans de triangle ont-ils atteint ? 
</dt> <dd>

Les ventilateurs triangulaires ont été dépréciés dans D3D10. Les ventilateurs à triangle doivent être convertis dans le pipeline de contenu ou lors du chargement.

</dd> </dl>

## <a name="shader-linkage"></a>Liaison de nuanceur

<dl> <dt>

<span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>Mes nuanceurs Direct3D 9 se compilent correctement avec le modèle de nuanceur 4,0, mais lorsque je les lie au pipeline, j’obtiens des erreurs de liaison qui s’affichent dans la sortie de débogage avec le runtime de débogage. 
</dt> <dd>

La liaison de nuanceur est plus stricte dans D3D10. Les éléments d’une étape suivante doivent être lus dans l’ordre dans lequel ils sont générés à partir de l’étape précédente. Par exemple :

Un nuanceur de sommets génère :

``` syntax
    float4 Pos  : SV_POSITION;
    float3 Norm : NORMAL;
    float2 Tex  : TEXCOORD0;
```

Un nuanceur de pixels lit les éléments suivants :

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

Même si la position n’est pas nécessaire dans le nuanceur de pixels, cela provoque une erreur de liaison, car la position est la sortie du nuanceur de sommets, mais elle n’est pas lue par le nuanceur de pixels. La version la plus correcte ressemble à ceci :

Un nuanceur de sommets génère :

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
        float4 Pos  : SV_POSITION;
```

Un nuanceur de pixels lit les éléments suivants :

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

Dans ce cas, le nuanceur de sommets génère les mêmes informations, mais maintenant le nuanceur de pixels lit les éléments dans la sortie de commande. Étant donné que le nuanceur de pixels ne lit rien après Tex, nous n’avons pas à vous soucier de la génération d’informations supplémentaires par rapport à la lecture de PS.

</dd> <dt>

<span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>J’ai besoin d’une signature de nuanceur pour créer une disposition d’entrée, mais je charge mes maillages et je crée des dispositions avant de créer des nuanceurs. Que faire ? 
</dt> <dd>

Une solution consiste à changer l’ordre et à charger les nuanceurs avant de charger les maillages. Toutefois, c’est beaucoup plus facile à dire qu’à faire. Vous pouvez toujours créer les dispositions d’entrée à la demande lorsque l’application l’exige. Vous devez conserver une version de la signature du nuanceur. Vous devez créer un hachage basé sur la disposition du nuanceur et de la mémoire tampon, et créer uniquement la disposition d’entrée si celle qui correspond n’existe pas déjà.

</dd> </dl>

## <a name="draw-calls"></a>Appels de dessin

<dl> <dt>

<span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>Quelle est la limite des appels de dessin pour D3D10 pour atteindre 60 Hz ? 30 Hz ? 
</dt> <dd>

Direct3D 9 avait une limitation du nombre d’appels de dessin en raison du coût de l’UC par appel de dessin. Sur Direct3D 10, le coût de chaque appel de dessin a été réduit. Toutefois, il n’existe plus de corrélation définie entre les appels de dessin et les fréquences d’images. Étant donné que les appels de dessin requièrent souvent de nombreux appels de support (mises à jour de tampon constantes, liaisons de texture, paramètres d’État, etc.), l’impact sur la fréquence de trame de l’API est désormais plus dépendant de l’utilisation globale de l’API, contrairement au simple dessin des nombres d’appels.

</dd> </dl>

## <a name="resources"></a>Ressources

<dl> <dt>

<span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>Quel type d’utilisation de ressource dois-je utiliser pour quelles opérations ? 
</dt> <dd>

Utilisez la feuille de triche suivante :

-   L’UC met à jour la ressource plusieurs fois par image : D3D10 \_ utilisation \_ dynamique
-   L’UC met à jour la ressource moins d’une fois par Frame : D3D10 \_ usage \_ default
-   L’UC ne met pas à jour la ressource : utilisation de D3D10 \_ \_ immuable
-   L’UC doit lire la ressource : D3D10 \_ usage \_ Staging

Étant donné que les mémoires tampons constantes sont toujours censées être mises à jour fréquemment, elles ne sont pas conformes à la « feuille de triche ». Pour connaître les types de ressources à utiliser pour les mémoires tampons constantes, consultez la section [mémoires tampons constantes](#constant-buffers) .

</dd> <dt>

<span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>Qu’est-il arrivé à DrawPrimitiveUP et DrawIndexedPrimitiveUP ? 
</dt> <dd>

Ils sont abD3D10s. Pour une géométrie dynamique, utilisez une \_ mémoire tampon dynamique de grande utilisation D3D10 \_ . Au début du frame, mappez-le avec D3D10 \_ carte d' \_ écriture \_ ignorée. Pour chaque appel de dessin suivant avance le pointeur d’écriture au-delà de la position des vertex précédemment dessinés et mappez la mémoire tampon avec la carte de D3D10 \_ \_ \_ n’écrire aucun remplacement \_ . Si vous approchez de la fin de la mémoire tampon avant la fin du frame, encapsulez le pointeur d’écriture au début et mappez avec D3D10 \_ carte d' \_ écriture \_ ignorée.

</dd> <dt>

<span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>Puis-je écrire des index 16 bits et des index 32 bits dans la même mémoire tampon de géométrie dynamique ? 
</dt> <dd>

Oui, vous pouvez, mais cela peut entraîner une baisse des performances sur un certain matériel. Il est plus sûr de créer des mémoires tampons distinctes pour les données d’index 16 bits dynamiques et les données d’index 32 bits.

</dd> <dt>

<span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>Comment faire lire les données du GPU vers le processeur ? 
</dt> <dd>

Vous devez utiliser une ressource intermédiaire. Copiez les données de la ressource GPU vers la ressource intermédiaire à l’aide de CopyResource. Mappez la ressource intermédiaire pour lire les données.

</dd> <dt>

<span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>Mon application dépend de la fonctionnalité StretchRect. 
</dt> <dd>

Comme il s’agissait essentiellement d’un wrapper pour la fonctionnalité Direct3D de base, il a été supprimé de l’API. Certaines fonctionnalités de StretchRect ont été déplacées dans D3DX10LoadTextureFromTexture. Pour les conversions de format et la copie des textures, D3DX10LoadTextureFromTexture peut effectuer le travail. Toutefois, les opérations telles que la conversion d’une taille à une autre peuvent nécessiter un rendu pour une opération de texture dans l’application.

</dd> <dt>

<span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>Il n’existe aucun décalage ni aucune taille sur les appels de carte pour les ressources. Ils se trouvaient sur des appels de verrou sur Direct3D 9 ; Pourquoi a-t-il changé ? 
</dt> <dd>

Les décalages et les tailles sur les appels de verrou sur Direct3D 9 étaient l’encombrement de l’API et sont souvent ignorés par le pilote. Les décalages doivent être calculés à la place de l’application à partir du pointeur retourné dans l’appel de carte.

</dd> </dl>

## <a name="depth-as-texture"></a>Profondeur comme texture

<dl> <dt>

<span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>Qui est plus rapide ? Vous utilisez la profondeur comme une texture ou une profondeur d’écriture dans alpha et que vous lisez ? 
</dt> <dd>

Il s’agit d’une application et d’un matériel spécifiques. Utilisez celui qui économise le plus de bande passante. Si vous utilisez déjà plusieurs cibles de rendu et que vous avez un canal supplémentaire, l’écriture de profondeur à partir du nuanceur peut être une meilleure solution. En outre, l’écriture de profondeur dans alpha ou une autre cible de rendu vous permet d’écrire des valeurs de profondeur linéaire qui peuvent accélérer les calculs qui doivent accéder à la mémoire tampon de profondeur.

</dd> <dt>

<span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>PUIS-je avoir une texture liée en tant qu’entrée et être liée comme une texture de stencil de profondeur tant que je désactive les écritures de profondeur ? 
</dt> <dd>

Pas dans D3D10.

</dd> </dl>

## <a name="msaa"></a>MSAA

<dl> <dt>

<span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>Puis-je résoudre une texture de stencil de profondeur MSAA ? 
</dt> <dd>

Pas dans D3D10. Toutefois, vous pouvez échantillonner des échantillons individuels à partir de la texture MSAA. Pour plus d’informations, consultez la section [HLSL](#hlsl) .

</dd> <dt>

<span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>Pourquoi mon application se bloque-t-elle dès que j’active MSAA ? 
</dt> <dd>

Veillez à activer un nombre d’échantillons MSAA et un numéro de qualité qui sont réellement énumérés par le pilote.

</dd> </dl>

## <a name="crashes"></a>Crashes

<dl> <dt>

<span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>Mon application se bloque dans D3D10 ou dans le pilote et je ne sais pas pourquoi. 
</dt> <dd>

La première étape consiste à activer le runtime de débogage (D3D10 créer l’indicateur de [**\_ \_ \_ débogage**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) de l’appareil passé dans [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)). Cela exposera les erreurs les plus courantes comme sortie de débogage.

</dd> <dt>

<span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>PIX se bloque lorsque j’essaie d’utiliser mon application avec celle-ci. 
</dt> <dd>

La première étape consiste à activer le runtime de débogage (D3D10 créer l’indicateur de [**\_ \_ \_ débogage**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) de l’appareil passé dans [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)). PIX a une probabilité plus élevée de blocage si la sortie de débogage n’est pas propre.

</dd> <dt>

<span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>Mon jeu ne dispose plus de suffisamment d’espace d’adressage virtuel sur Vista 32 bits sous D3D10. Il n’y a aucun problème sur D3D9. 
</dt> <dd>

Certains problèmes se sont produits avec D3D10 et l’espace d’adressage virtuel. Ce problème a été résolu dans [KB940105](https://support.microsoft.com/kb/940105). Si cela ne résout pas votre problème, assurez-vous de ne pas créer plus de ressources qui peuvent être mappées (verrouillées) dans D3D10 que dans D3D9. Pensez également au portage vers 64 bits, car cela deviendra plus répandu à l’avenir.

</dd> </dl>

## <a name="predicated-rendering"></a>Rendu prédicat

<dl> <dt>

<span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>J’ai utilisé le rendu prédicat (en fonction des résultats d’une requête d’occlusion). Pourquoi mon application a-t-elle toujours la même vitesse ? 
</dt> <dd>

Tout d’abord, assurez-vous que le rendu que vous souhaitez ignorer est en fait le goulot d’étranglement de l’application. S’il ne s’agit pas du goulot d’étranglement, le fait d’ignorer le rendu ne permet pas d’obtenir une fréquence d’images.

Ensuite, assurez-vous que suffisamment de temps s’est écoulé entre le problème de la requête et du rendu que vous souhaitez définir comme prédicat. Si la requête n’est pas terminée au moment où l’appel de rendu atteint le GPU, le rendu se produit tout de même.

Troisièmement, le prédicat ignore uniquement certains appels. Les appels ignorés sont dessiner, effacer, copier, mettre à jour, ResolveSubresource et GenerateMips. Le paramètre d’État, le programme d’installation d’IA, le mappage et les appels de création ne respectent pas la prédicat. Si un grand nombre d’appels de paramètres d’État autour de l’appel de dessin doivent être prédicats, ces États sont toujours définis.

</dd> </dl>

## <a name="geometry-shader"></a>Nuanceur de géométrie

<dl> <dt>

<span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>Dois-je utiliser le nuanceur Geometry pour paver mon (insérer quoi que ce soit ici) ? 
</dt> <dd>

Non. Le nuanceur Geometry ne doit pas être utilisé pour le pavage.

</dd> <dt>

<span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>Puis-je utiliser le nuanceur Geometry pour créer une géométrie ? 
</dt> <dd>

Oui, dans des scénarios très limités. Le nuanceur Geometry des parties D3D10 actuelles (2008) n’est pas conçu pour gérer une grande expansion. Cela peut changer à l’avenir. Les fournisseurs de cartes vidéo peuvent avoir un chemin d’accès spécial pour quatre expansions en raison d’un matériel de point-Sprite existant. Toute autre expansion devrait être très limitée. Les exemples ParticlesGS et PipesGS permettent d’obtenir des fréquences d’images élevées en n’ayant qu’une expansion limitée. Seuls quelques points sont développés par frame.

</dd> <dt>

<span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>À quoi dois-je utiliser le nuanceur Geometry ? 
</dt> <dd>

Tout ce qui nécessite des opérations sur une primitive entière, comme la détection silhouette, les coordonnées Barycentric, etc. Vous pouvez également l’utiliser pour sélectionner le secteur d’un tableau cible de rendu auquel envoyer les primitives.

</dd> <dt>

<span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>Puis-je générer des quantités variables de géométrie à partir du nuanceur Geometry ? 
</dt> <dd>

Oui, mais cela peut entraîner des problèmes de performances. Prenons l’exemple de la génération d’un point 1 pour un appel et de 4 points pour un autre. En cas de montage dans les règles de développement, cela peut entraîner l’exécution en série des threads du nuanceur Geometry.

</dd> <dt>

<span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>Comment D3D10 sait-il comment générer des index d’adjacence pour ma maille ? Ou bien, pourquoi D3D10 ne s’affiche pas correctement lorsque je spécifie que le nuanceur Geometry a besoin d’informations d’adjacence. 
</dt> <dd>

Les informations d’adjacence ne sont pas créées par D3D10, mais par l’application. Les index d’adjacence sont générés par l’application et doivent contenir six index par primitive ; Parmi les six, les index impairs sont les vertex adjacents du bord. ID3DX10Mesh :: GenerateAdjacencyAndPointsReps peut être utilisé pour générer ces données.

</dd> </dl>

## <a name="hlsl"></a>HLSL

<dl> <dt>

<span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>Les instructions d’entiers et de bits sont-elles lentes ? 
</dt> <dd>

Ils peuvent être. Diverses cartes D3D10 peuvent uniquement être en mesure d’émettre des opérations d’entiers sur un sous-ensemble des unités ALU disponibles. Cela dépend fortement du matériel. Pour obtenir des recommandations sur la façon d’effectuer des opérations sur les entiers sur ce matériel particulier, consultez le fournisseur de votre matériel. En outre, veillez à effectuer des casts entre les types.

</dd> <dt>

<span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>Qu’est-il arrivé à VPOS ? 
</dt> <dd>

Si vous déclarez une entrée à votre nuanceur de pixels comme position de SV \_ , vous obtiendrez le même comportement que le déclarer comme VPOS.

</dd> <dt>

<span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>Comment faire un exemple de texture MSAA ? 
</dt> <dd>

Dans votre nuanceur, déclarez votre texture comme Texture2DMS. Vous pouvez ensuite extraire des exemples individuels à l’aide des exemples de méthodes de l’objet Texture2DMS.

</dd> <dt>

<span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>Comment faire indiquer si une variable de nuanceur dans une mémoire tampon constante est réellement utilisée ? 
</dt> <dd>

Examinez le \_ \_ struct Description variable de nuanceur D3D10 réfléchi \_ pour cette variable. uFlags doit avoir l' \_ indicateur D3D10 SVF \_ utilisé défini.

</dd> <dt>

<span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>Comment faire indiquer si une variable de nuanceur dans une mémoire tampon constante utilise réellement FX10 ? 
</dt> <dd>

Cela n’est pas possible actuellement avec FX10.

</dd> <dt>

<span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>Je n’ai aucun contrôle sur les mémoires tampons constantes créées par FX10. Comment sont-ils créés et mis à jour ? 
</dt> <dd>

Toutes les mémoires tampons constantes gérées par FX10 sont créées en tant que \_ \_ ressources par défaut d’utilisation D3D10 et sont mises à jour à l’aide de UpdateSubresource. Étant donné que FX10 conserve un magasin de stockage de toutes les données constantes, UpdateSubresource est la meilleure approche pour les mettre à jour.

</dd> <dt>

<span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>Comment faire émuler le pipeline de fonction fixe à l’aide de nuanceurs ? 
</dt> <dd>

Consultez l’exemple FixedFuncEMU.

</dd> <dt>

<span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>Dois-je utiliser les nouveaux \[ \] indicateurs de compilation, de boucle, de \[ \] \[ branche \] , etc. ? 
</dt> <dd>

En général, non. Le compilateur essaiera souvent les deux façons et choisissez le plus rapide. Dans certains cas, il peut être nécessaire d’utiliser la \[ désroll \] , par exemple, lorsqu’une extraction de texture à l’intérieur d’une boucle a besoin d’accéder à un dégradé.

</dd> <dt>

<span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>La précision partielle fait-elle une différence sur les D3D10 ? Je peux spécifier une précision partielle dans mon D3D9 HLSL, mais pas dans mon D3D10 HLSL. 
</dt> <dd>

Toutes les opérations D3D10 sont spécifiées pour s’exécuter à la précision à virgule flottante 32 bits. Par conséquent, la précision partielle ne doit pas faire de différence dans D3D10.

</dd> <dt>

<span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>Dans D3D9, il serait possible de procéder à un filtrage instantané PCF en liant une mémoire tampon de profondeur comme texture et en utilisant les instructions standard tex2d HLSL. Comment faire le faire sur D3D10 ? 
</dt> <dd>

Vous devez utiliser un état d’échantillonnage de comparaison et utiliser des instructions SampleCmp.

</dd> <dt>

<span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>Comment ce mot clé Register fonctionne-t-il dans D3D10 ? 
</dt> <dd>

Le mot clé Register dans D3D10 s’applique désormais à l’emplacement auquel une ressource particulière est liée. Dans ce cas, la ressource peut être une mémoire tampon (constante ou autre), une texture ou un échantillonneur.

-   Pour les mémoires tampons constantes, utilisez la syntaxe suivante : Register (-), où N est l’emplacement d’entrée (0-15)
-   Pour les textures, utilisez la syntaxe : Register (tN), où N est l’emplacement d’entrée (0-127)
-   Pour les échantillonneurs, utilisez la syntaxe suivante : Register (sN), où N est l’emplacement d’entrée (0-127)

</dd> <dt>

<span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>Comment faire placer une variable à l’intérieur d’une mémoire tampon constante si le Registre est simplement utilisé pour spécifier l’emplacement de la liaison de la mémoire tampon entière ? 
</dt> <dd>

Utilisez le mot clé packoffset. L’argument de packoffset se présente sous la forme c \[ 0-4095 \] . \[ x, y, z, w \] . Par exemple :

``` syntax
        cbuffer cbLotsOfEmptySpace
        {
        float   IWaste2Floats   : packoffset(c0.z);
        float4  IWasteMore  : packoffset(c13);
        };
```

Dans ce tampon de constante, IWaste2Floats est placé au troisième float (douzième octet) dans la mémoire tampon constante. IWasteMore est placé au 13e float4 ou 52nd float dans la mémoire tampon constante.

</dd> </dl>

 

 