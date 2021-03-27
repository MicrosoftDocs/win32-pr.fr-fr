---
title: Fonctionnalités Direct3D 11,1
description: Les fonctionnalités suivantes ont été ajoutées dans Direct3D 11,1, qui est inclus avec Windows 8, Windows RT et Windows Server 2012.
ms.assetid: 2203D2D2-ECF6-4753-90FA-12A52678DFBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dece9ed6e0a40ade28857277c344be0e9f2e7ce1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727493"
---
# <a name="direct3d-111-features"></a>Fonctionnalités Direct3D 11,1

Les fonctionnalités suivantes ont été ajoutées dans Direct3D 11,1, qui est inclus avec Windows 8, Windows RT et Windows Server 2012. La prise en charge partielle de [Direct3D 11,1](direct3d-11-features.md) est disponible sur Windows 7 et windows Server 2008 R2 via la [mise à jour de plateforme pour Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7), disponible via la [mise à jour de plateforme pour Windows 7](https://support.microsoft.com/kb/2670838).

-   [Suivi des nuanceurs et améliorations du compilateur](#shader-tracing-and-compiler-enhancements)
-   [Partage d’appareils Direct3D](#direct3d-device-sharing)
-   [Vérifier la prise en charge des nouvelles fonctionnalités et des formats Direct3D 11,1](#check-support-of-new-direct3d-111-features-and-formats)
-   [Utiliser la précision minimale HLSL](#use-hlsl-minimum-precision)
-   [Spécifier des plans de clip utilisateur en HLSL sur le niveau de fonctionnalité 9 et versions ultérieures](#specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Créer des mémoires tampons constantes plus grandes qu’un nuanceur peut accéder](#create-larger-constant-buffers-than-a-shader-can-access)
-   [Utiliser des opérations logiques dans une cible de rendu](#use-logical-operations-in-a-render-target)
-   [Forcer le nombre d’échantillons à créer un état de rastériseur](#force-the-sample-count-to-create-a-rasterizer-state)
-   [Traiter des ressources vidéo avec des nuanceurs](#process-video-resources-with-shaders)
-   [Prise en charge étendue des ressources Texture2D partagées](#extended-support-for-shared-texture2d-resources)
-   [Modifier les sous-ressources avec les nouvelles options de copie](#change-subresources-with-new-copy-options)
-   [Ignorer les ressources et les affichages des ressources](#discard-resources-and-resource-views)
-   [Prendre en charge un plus grand nombre de UAVs](#support-a-larger-number-of-uavs)
-   [Lier une sous-plage d’une mémoire tampon constante à un nuanceur](#bind-a-subrange-of-a-constant-buffer-to-a-shader)
-   [Récupérer la sous-plage d’une mémoire tampon constante liée à un nuanceur](#retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader)
-   [Effacer tout ou partie d’un affichage des ressources](#clear-all-or-part-of-a-resource-view)
-   [Mapper les SRVs de mémoires tampons dynamiques sans \_ remplacement](/windows)
-   [Utiliser UAVs à chaque étape du pipeline](#use-uavs-at-every-pipeline-stage)
-   [Prise en charge étendue des appareils WARPs](#extended-support-for-warp-devices)
-   [Utiliser Direct3D dans les processus de la session 0](#use-direct3d-in-session-0-processes)
-   [Prise en charge de la mémoire tampon Shadow au niveau de la fonctionnalité 9](#support-for-shadow-buffer-on-feature-level-9)
-   [Rubriques connexes](#related-topics)

## <a name="shader-tracing-and-compiler-enhancements"></a>Suivi des nuanceurs et améliorations du compilateur

Direct3D 11,1 vous permet d’utiliser le suivi du nuanceur pour vous assurer que votre code fonctionne comme prévu, et si ce n’est pas le cas, vous pouvez détecter et résoudre le problème. Le kit de développement logiciel (SDK) Windows pour Windows 8 contient des améliorations du compilateur HLSL. Le suivi du nuanceur et le compilateur HLSL sont implémentés dans D3dcompiler \_nn.dll.

L’API de suivi de nuanceur et les améliorations apportées au compilateur HLSL consistent en les méthodes et les fonctions suivantes.

-   [**ID3D11RefDefaultTrackingOptions::SetTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11refdefaulttrackingoptions-settrackingoptions)
-   [**ID3D11RefTrackingOptions::SetTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11reftrackingoptions-settrackingoptions)
-   [**ID3D11TracingDevice::SetShaderTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype)
-   [**ID3D11TracingDevice::SetShaderTrackingOptionsByType**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype)
-   [**ID3D11ShaderTraceFactory::CreateShaderTrace**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertracefactory-createshadertrace)
-   [**ID3D11ShaderTrace::TraceReady**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-traceready)
-   [**ID3D11ShaderTrace::ResetTrace**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-resettrace)
-   [**ID3D11ShaderTrace::GetTraceStats**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-gettracestats)
-   [**ID3D11ShaderTrace ::P SSelectStamp**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-psselectstamp)
-   [**ID3D11ShaderTrace::GetInitialRegisterContents**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getinitialregistercontents)
-   [**ID3D11ShaderTrace::GetStep**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getstep)
-   [**ID3D11ShaderTrace::GetWrittenRegister**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getwrittenregister)
-   [**ID3D11ShaderTrace::GetReadRegister**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getreadregister)
-   [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2)
-   [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)
-   [**D3DDisassemble11Trace**](/windows/desktop/direct3dhlsl/d3ddisassemble11trace)
-   [**D3DDisassembleRegion**](/windows/desktop/direct3dhlsl/d3ddisassembleregion)
-   [**D3DGetTraceInstructionOffsets**](/windows/desktop/direct3dhlsl/d3dgettraceinstructionoffsets)
-   [**D3DReadFileToBlob**](/windows/desktop/direct3dhlsl/d3dreadfiletoblob)
-   [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart)
-   [**D3DWriteBlobToFile**](/windows/desktop/direct3dhlsl/d3dwriteblobtofile)

La bibliothèque D3dcompiler. lib requiert D3dcompiler \_nn.dll. Cette DLL ne fait pas partie de Windows 8 ; Il se trouve dans le \\ dossier bin de la SDK Windows pour Windows 8, ainsi que la version de ligne de commande Fxc.exe du compilateur HLSL.

> [!Note]  
> Bien que vous puissiez utiliser cette combinaison de bibliothèques et de DLL pour le développement, vous ne pouvez pas déployer des applications du Windows Store qui utilisent cette combinaison. Par conséquent, vous devez à la place compiler les nuanceurs HLSL avant d’expédier votre application du Windows Store. Vous pouvez écrire des binaires de compilation HLSL sur le disque ou le compilateur peut générer des en-têtes avec des tableaux d’octets statiques contenant les données d’objet blob de nuanceur. Vous utilisez l’interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) pour accéder aux données d’objet BLOB. Pour développer votre application du Windows Store, appelez [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2) ou [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) pour compiler la source HLSL brute, puis placez les données BLOB obtenues dans Direct3D.

 

## <a name="direct3d-device-sharing"></a>Partage d’appareils Direct3D

Direct3D 11,1 permet aux API Direct3D 10 et aux API Direct3D 11 d’utiliser un périphérique de rendu sous-jacent.

Cette fonctionnalité Direct3D 11,1 se compose des méthodes et de l’interface suivantes.

-   [**ID3D11Device1::CreateDeviceContextState**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate)
-   [**ID3D11DeviceContext1::SwapDeviceContextState**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-swapdevicecontextstate)
-   [**ID3DDeviceContextState**](/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate)

## <a name="check-support-of-new-direct3d-111-features-and-formats"></a>Vérifier la prise en charge des nouvelles fonctionnalités et des formats Direct3D 11,1

Direct3D 11,1 vous permet de vérifier les nouvelles fonctionnalités que le pilote Graphics peut prendre en charge et les nouvelles méthodes de prise en charge d’un format sur un appareil. Microsoft DirectX Graphics infrastructure (DXGI) 1,2 spécifie également les nouvelles valeurs de [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) .

Cette fonctionnalité Direct3D 11,1 est constituée de l’API suivante.

-   [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) avec [**les \_ \_ options de \_ d3d11 \_ de données de la fonctionnalité d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), les [**\_ \_ \_ \_ informations sur l’architecture de données**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info)de la fonctionnalité d3d11, les [**\_ \_ \_ \_ options**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options)d3d11 des données de fonctionnalités d3d9, la [**\_ \_ \_ \_ \_ \_ prise en charge de la précision minimale des nuanceurs de données**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)de fonctionnalités d3d11 et les structures de [**\_ \_ \_ \_ \_ prise en charge Shadow**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support)
-   [**ID3D11Device :: CheckFormatSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) avec [**le \_ format d3d11 \_ prend en charge la \_ \_ sortie du décodeur**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), le [**\_ format d3d11 prend en charge la \_ \_ \_ \_ sortie du processeur vidéo**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), le [**format d3d11 l' \_ \_ \_ \_ \_ entrée du processeur vidéo**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), le [**\_ format d3d11 \_ prend en charge l' \_ \_ encodeur vidéo**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support)et le [**format d3d11 format de sortie de la \_ \_ \_ \_ fusion \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2)

## <a name="use-hlsl-minimum-precision"></a>Utiliser la précision minimale HLSL

À compter de Windows 8, les pilotes graphiques peuvent implémenter des [types de données scalaires HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) de précision minimale à l’aide d’une précision supérieure ou égale à la précision de bit spécifiée. Lorsque votre code de nuanceur de précision minimale HLSL est utilisé sur le matériel qui implémente la précision minimale HLSL, vous utilisez moins de bande passante de mémoire et vous utilisez donc moins de puissance système.

Vous pouvez interroger la prise en charge de précision minimale que le pilote Graphics fournit en appelant [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) avec la valeur de [**\_ \_ \_ \_ \_ prise en charge de l’outil nuanceur min précision de la fonctionnalité d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) . Dans cet appel **ID3D11Device :: CheckFeatureSupport** , transmettez un pointeur vers une structure de [**\_ \_ \_ \_ \_ \_ prise en charge de nuanceur min précision de la fonctionnalité d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support) que **ID3D11Device :: CheckFeatureSupport** remplit avec les niveaux de précision minimale que le pilote prend en charge pour l’étape nuanceur de pixels et pour d’autres étapes de nuanceur. Les informations renvoyées indiquent simplement que le matériel graphique peut effectuer des opérations HLSL à une précision inférieure à la précision de la virgule flottante 32 bits standard, mais ne garantit pas que le matériel graphique s’exécutera en fait à une précision inférieure.

Vous n’avez pas besoin de créer plusieurs nuanceurs qui n’utilisent pas la précision minimale. Au lieu de cela, créez des nuanceurs avec une précision minimale, et les variables de précision minimale se comportent à une précision de 32 bits complète si le pilote graphique signale qu’il ne prend pas en charge de précision minimale. Pour plus d’informations sur la précision minimale du HLSL, consultez Utilisation de la [précision minimale HLSL](/windows/desktop/direct3dhlsl/using-hlsl-minimum-precision).

Les nuanceurs de précision minimale HLSL ne fonctionnent pas sur les systèmes d’exploitation antérieurs à Windows 8.

## <a name="specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Spécifier des plans de clip utilisateur en HLSL sur le niveau de fonctionnalité 9 et versions ultérieures

À compter de Windows 8, vous pouvez utiliser l’attribut de fonction **clipplanes** dans une [déclaration de fonction](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-syntax) HLSL plutôt que [SV \_ ClipDistance](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) pour que votre nuanceur fonctionne sur le [niveau de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) 9 x, ainsi que sur le niveau de \_ fonctionnalité 10 et ultérieur. Pour plus d’informations, consultez l' [image des plans d’utilisateur sur le matériel de niveau de fonctionnalité 9](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).

## <a name="create-larger-constant-buffers-than-a-shader-can-access"></a>Créer des mémoires tampons constantes plus grandes qu’un nuanceur peut accéder

Direct3D 11,1 vous permet de créer des mémoires tampons constantes dont la taille est supérieure à la taille maximale de la mémoire tampon constante à laquelle un nuanceur peut accéder ( \* constantes à 4 composants, 4096 32 bits). Plus tard, lorsque vous lierez les mémoires tampons au pipeline, par exemple, via [**PSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers) ou [**PSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1), vous pouvez spécifier une plage de mémoires tampons auxquelles le nuanceur peut accéder et qui correspond à la limite de 4096.

Direct3D 11,1 met à jour la méthode [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) pour cette fonctionnalité.

## <a name="use-logical-operations-in-a-render-target"></a>Utiliser des opérations logiques dans une cible de rendu

Direct3D 11,1 vous permet d’utiliser des opérations logiques au lieu de les fusionner dans une cible de rendu. Toutefois, vous ne pouvez pas mélanger des opérations logiques avec la fusion sur plusieurs cibles de rendu.

Cette fonctionnalité Direct3D 11,1 est constituée de l’API suivante.

-   [**ID3D11Device1 :: CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1) avec [ **d3d11 \_ Logic \_ op**](/windows/desktop/api/D3D11_1/ne-d3d11_1-d3d11_logic_op)

## <a name="force-the-sample-count-to-create-a-rasterizer-state"></a>Forcer le nombre d’échantillons à créer un état de rastériseur

Direct3D 11,1 vous permet de spécifier un nombre d’échantillons forcés lorsque vous créez un état de rastériseur.

Cette fonctionnalité Direct3D 11,1 est constituée de l’API suivante.

-   [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1)

> [!Note]  
>
> Si vous souhaitez effectuer un rendu avec un nombre d’échantillons forcé à 1 ou supérieur, vous devez suivre les instructions suivantes :
>
> -   Ne pas lier les vues de stencil de profondeur.
> -   Désactivez le test de profondeur.
> -   Assurez-vous que le nuanceur ne génère pas de profondeur.
> -   Si vous avez lié des vues de cible de rendu ([**d3d11 \_ liaison de \_ rendu \_ cible**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)) et que vous avez forcé le nombre d’échantillons à supérieur à 1, assurez-vous que chaque cible de rendu n’a qu’un seul échantillon.
> -   Ne pas utiliser le nuanceur à la fréquence d’échantillonnage. Par conséquent, [**ID3D11ShaderReflection :: IsSampleFrequencyShader**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11shaderreflection-issamplefrequencyshader) retourne **false**.
>
> Dans le cas contraire, le comportement de rendu n’est pas défini. Pour plus d’informations sur la configuration du gabarit de profondeur, consultez [Configuration des fonctionnalités de Depth-Stencil](d3d10-graphics-programming-guide-depth-stencil.md).

 

## <a name="process-video-resources-with-shaders"></a>Traiter des ressources vidéo avec des nuanceurs

Direct3D 11,1 vous permet de créer des affichages (SRV/RTV/UAV) dans des ressources vidéo afin que les nuanceurs Direct3D puissent traiter ces ressources vidéo. Le format d’une ressource vidéo sous-jacente restreint les formats que la vue peut utiliser. L’énumération de [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) contient de nouvelles valeurs de format de ressource vidéo. Ces valeurs de **\_ format dxgi** spécifient les formats de vue valides que vous pouvez créer et la façon dont le runtime Direct3D 11,1 mappe la vue. Vous pouvez créer plusieurs vues de différentes parties de la même surface et, selon le format, les tailles des vues peuvent différer les unes des autres.

Direct3D 11,1 met à jour les méthodes suivantes pour cette fonctionnalité.

-   [**ID3D11Device :: CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview)
-   [**ID3D11Device :: CreateRenderTargetView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createrendertargetview)
-   [**ID3D11Device :: CreateUnorderedAccessView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createunorderedaccessview)

## <a name="extended-support-for-shared-texture2d-resources"></a>Prise en charge étendue des ressources Texture2D partagées

Direct3D 11,1 garantit que vous pouvez partager des ressources Texture2D que vous avez créées avec des types de ressources et des formats particuliers. Pour partager des ressources Texture2D, utilisez la ressource d3d11 Shared [**\_ \_ misc \_ Shared**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag), [**d3d11 \_ Resource misc \_ \_ Shared \_ KEYEDMUTEX**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag), ou une combinaison des indicateurs d3d11 Resource misc **\_ \_ \_ Shared \_ KEYEDMUTEX** et [**d3d11 \_ Resource misc Shared \_ \_ \_ NTHANDLE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) (New for Windows 8) lorsque vous créez ces ressources.

Direct3D 11,1 garantit que vous pouvez partager des ressources Texture2D que vous avez créées avec ces valeurs de [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) :

-   DXGI \_ format \_ R8G8B8A8 \_ UNORM
-   DXGI \_ format \_ R8G8B8A8 \_ UNORM \_ sRVB
-   DXGI \_ format \_ B8G8R8A8 \_ UNORM
-   DXGI \_ format \_ B8G8R8A8 \_ UNORM \_ sRVB
-   DXGI \_ format \_ B8G8R8X8 \_ UNORM
-   DXGI \_ format \_ B8G8R8X8 \_ UNORM \_ sRVB
-   DXGI \_ format \_ R10G10B10A2 \_ UNORM
-   DXGI \_ format \_ R16G16B16A16 \_ float

En outre, Direct3D 11,1 garantit que vous pouvez partager des ressources Texture2D que vous avez créées avec un niveau mipmap de 1, une taille de tableau de 1, des indicateurs de liaison de la [**\_ \_ \_ ressource de nuanceur de liaison d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) et la cible de rendu de la liaison de d3d11 combinés, l’utilisation par défaut ([**d3d11 d' \_ utilisation \_ par défaut**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)) et uniquement ces valeurs d' [**\_ \_ \_ indicateur diverses des ressources d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) : [**\_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)

-   [**\_Ressources \_ \_ PARTAGÉes divers d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ ressources \_ \_ partagées divers \_ KEYEDMUTEX**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ ressources \_ \_ partagées divers \_ NTHANDLE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**\_ \_ \_ Compatibilité GDI divers des ressources d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

Direct3D 11,1 vous permet de partager une plus grande variété de types de ressources et de formats de Texture2D. Vous pouvez demander si le pilote graphique et le matériel prennent en charge le partage de ressources Texture2D étendu en appelant [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) avec la [**fonctionnalité d3d11 valeur des \_ \_ \_ options d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) . Dans cet appel **ID3D11Device :: CheckFeatureSupport** , passer un pointeur vers une structure d’options de d3d11 de [**données de \_ fonctionnalités \_ \_ \_ d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) . **ID3D11Device :: CheckFeatureSupport** définit le membre **ExtendedResourceSharing** des **\_ \_ \_ \_ options d3d11 des données de la fonctionnalité d3d11** sur **true** si le matériel et le pilote prennent en charge le partage de ressources Texture2D étendus.

Si [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) retourne la **valeur true** dans **ExtendedResourceSharing**, vous pouvez partager les ressources que vous avez créées avec ces valeurs de [**\_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) :

-   DXGI \_ format \_ R32G32B32A32 non \_ typé
-   DXGI \_ format \_ R32G32B32A32 \_ float
-   DXGI \_ format \_ R32G32B32A32 \_ uint
-   \_Format dxgi \_ R32G32B32A32 \_ Saint-
-   DXGI \_ format \_ R16G16B16A16 non \_ typé
-   DXGI \_ format \_ R16G16B16A16 \_ float
-   DXGI \_ format \_ R16G16B16A16 \_ UNORM
-   DXGI \_ format \_ R16G16B16A16 \_ uint
-   \_Format dxgi \_ R16G16B16A16 \_ ronfler
-   \_Format dxgi \_ R16G16B16A16 \_ Saint-
-   DXGI \_ format \_ R10G10B10A2 \_ UNORM
-   DXGI \_ format \_ R10G10B10A2 \_ uint
-   DXGI \_ format \_ R8G8B8A8 non \_ typé
-   DXGI \_ format \_ R8G8B8A8 \_ UNORM
-   DXGI \_ format \_ R8G8B8A8 \_ UNORM \_ sRVB
-   DXGI \_ format \_ R8G8B8A8 \_ uint
-   \_Format dxgi \_ R8G8B8A8 \_ ronfler
-   \_Format dxgi \_ R8G8B8A8 \_ Saint-
-   DXGI \_ format \_ B8G8R8A8 non \_ typé
-   DXGI \_ format \_ B8G8R8A8 \_ UNORM
-   DXGI \_ format \_ B8G8R8X8 \_ UNORM
-   DXGI \_ format \_ B8G8R8A8 \_ UNORM \_ sRVB
-   DXGI \_ format \_ B8G8R8X8 non \_ typé
-   DXGI \_ format \_ B8G8R8X8 \_ UNORM \_ sRVB
-   DXGI \_ format \_ R32 non \_ typé
-   DXGI \_ format \_ R32 \_ float
-   DXGI \_ format \_ R32 \_ uint
-   \_Format dxgi \_ R32 \_ Saint-
-   DXGI \_ format \_ R16 non \_ typé
-   DXGI \_ format \_ R16 \_ float
-   DXGI \_ format \_ R16 \_ UNORM
-   DXGI \_ format \_ R16 \_ uint
-   \_Format dxgi \_ R16 \_ ronfler
-   \_Format dxgi \_ R16 \_ Saint-
-   \_Format dxgi \_ R8 non \_ typé
-   \_Format dxgi \_ R8 \_ UNORM
-   \_Format dxgi \_ R8 \_ uint
-   \_Format dxgi \_ R8 \_ ronfler
-   \_Format dxgi \_ R8 \_ Saint-
-   \_Format dxgi \_ a8 \_ UNORM
-   DXGI \_ format \_ AYUV
-   DXGI \_ format \_ YUY2
-   DXGI \_ format \_ NV12
-   DXGI \_ format \_ NV11
-   DXGI \_ format \_ P016
-   DXGI \_ format \_ P010
-   DXGI \_ format \_ Y216
-   DXGI \_ format \_ Y210
-   DXGI \_ format \_ Y416
-   DXGI \_ format \_ Y410

Si [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) retourne la **valeur true** dans **ExtendedResourceSharing**, vous pouvez partager les ressources que vous avez créées avec ces fonctionnalités et indicateurs :

-   [**Utilisation de D3D11 \_ \_ par défaut**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)
-   [**\_Ressource de \_ nuanceur de liaison d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**\_Cible de \_ rendu de liaison d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**D3D11 \_ ressources \_ \_ mips générer \_ divers**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ lier \_ \_ l’accès non ordonné**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   Niveaux de mipmap (un ou plusieurs niveaux) dans les ressources de texture 2D (spécifiées dans le membre **miplevels a** de [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc))
-   Tableaux de ressources de texture 2D (une ou plusieurs textures) (spécifiées dans le membre **arraySize** de [**d3d11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc))
-   [**\_DÉcodeur de liaison d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**\_Contenu à \_ \_ restriction diverse des ressources \_ d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**\_ \_ \_ Ressource partagée de restriction \_ diverse \_ de la ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**\_Pilote de \_ \_ \_ ressource partagée de restriction diverse \_ de \_ ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

> [!Note]  
> Quand **ExtendedResourceSharing** a la **valeur true**, vous avez plus de flexibilité lorsque vous spécifiez des indicateurs de liaison pour partager des ressources Texture2D. Non seulement le pilote graphique et le matériel prennent en charge plus d’indicateurs de liaison, mais également d’autres combinaisons d’indicateurs de liaison. Par exemple, vous pouvez spécifier uniquement [**la \_ \_ \_ cible de rendu d3d11 bind**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) ou aucun indicateur de liaison, et ainsi de suite.

 

Même si [**ID3D11Device :: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) retourne la **valeur true** dans **ExtendedResourceSharing**, vous ne pouvez toujours pas partager les ressources que vous avez créées avec ces fonctionnalités et indicateurs :

-   [**\_Stencil de \_ profondeur de liaison d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   ressources de texture 2D en mode MSAA (MultiSample anticrénelage) (spécifié avec l' [**\_ exemple dxgi \_ desc**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc))
-   [**D3D11 \_ de \_ ressources diverses de ressources \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3d11 \_ UTILISATION \_ immuable**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), d3d11 d’utilisation [**\_ \_ dynamique**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)ou [**intermédiaire de \_ l' \_ utilisation de d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) (autrement dit, mappable)
-   [**D3D11 \_ \_ divers \_ TEXTURECUBE des ressources**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="change-subresources-with-new-copy-options"></a>Modifier les sous-ressources avec les nouvelles options de copie

Direct3D 11,1 vous permet d’utiliser de nouveaux indicateurs de copie pour copier et mettre à jour des sous-ressources. Lorsque vous copiez une sous-ressource, les ressources source et de destination peuvent être identiques et les régions source et de destination peuvent se chevaucher.

Cette fonctionnalité Direct3D 11,1 est constituée de l’API suivante.

-   [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1)
-   [**ID3D11DeviceContext1::UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)

## <a name="discard-resources-and-resource-views"></a>Ignorer les ressources et les affichages des ressources

Direct3D 11,1 vous permet d’ignorer les ressources et les vues des ressources à partir du contexte de périphérique. Cette nouvelle fonctionnalité informe le GPU que le contenu existant dans les ressources ou les affichages de ressources n’est plus nécessaire.

Cette fonctionnalité Direct3D 11,1 est constituée de l’API suivante.

-   [**ID3D11DeviceContext1 ::D iscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource)
-   [**ID3D11DeviceContext1 ::D iscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview)
-   [**ID3D11DeviceContext1 ::D iscardView1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview1)

## <a name="support-a-larger-number-of-uavs"></a>Prendre en charge un plus grand nombre de UAVs

Direct3D 11,1 vous permet d’utiliser un plus grand nombre de UAVs quand vous liez des ressources à l' [étape de fusion de sortie](d3d10-graphics-programming-guide-output-merger-stage.md) et lorsque vous définissez un tableau de vues pour une ressource non triée.

Direct3D 11,1 met à jour les méthodes suivantes pour cette fonctionnalité.

-   [**ID3D11DeviceContext :: OMSetRenderTargetsAndUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargetsandunorderedaccessviews)
-   [**ID3D11DeviceContext :: CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews)

## <a name="bind-a-subrange-of-a-constant-buffer-to-a-shader"></a>Lier une sous-plage d’une mémoire tampon constante à un nuanceur

Direct3D 11,1 vous permet de lier une sous-plage d’une mémoire tampon constante à un nuanceur pour y accéder. Vous pouvez fournir une mémoire tampon constante plus grande et spécifier la sous-plage que le nuanceur peut utiliser.

Cette fonctionnalité Direct3D 11,1 est constituée de l’API suivante.

-   [**ID3D11DeviceContext1::CSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-cssetconstantbuffers1)
-   [**ID3D11DeviceContext1 ::D SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dssetconstantbuffers1)
-   [**ID3D11DeviceContext1::GSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gssetconstantbuffers1)
-   [**ID3D11DeviceContext1::HSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hssetconstantbuffers1)
-   [**ID3D11DeviceContext1 ::P SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1)
-   [**ID3D11DeviceContext1::VSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vssetconstantbuffers1)

## <a name="retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader"></a>Récupérer la sous-plage d’une mémoire tampon constante liée à un nuanceur

Direct3D 11,1 vous permet de récupérer la sous-plage d’une mémoire tampon constante qui est liée à un nuanceur.

Cette fonctionnalité Direct3D 11,1 est constituée de l’API suivante.

-   [**ID3D11DeviceContext1::CSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-csgetconstantbuffers1)
-   [**ID3D11DeviceContext1 ::D SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::GSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::HSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hsgetconstantbuffers1)
-   [**ID3D11DeviceContext1 ::P SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-psgetconstantbuffers1)
-   [**ID3D11DeviceContext1::VSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vsgetconstantbuffers1)

## <a name="clear-all-or-part-of-a-resource-view"></a>Effacer tout ou partie d’un affichage des ressources

Direct3D 11,1 vous permet de supprimer un affichage des ressources (RTV, UAV ou n’importe quelle vue vidéo d’une surface Texture2D). Vous appliquez la même valeur de couleur à toutes les parties de la vue.

Cette fonctionnalité Direct3D 11,1 est constituée de l’API suivante.

-   [**ID3D11DeviceContext1::ClearView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview)

## <a name="map-srvs-of-dynamic-buffers-with-no_overwrite"></a>Mapper les SRVs de mémoires tampons dynamiques sans \_ remplacement

Direct3D 11,1 vous permet de mapper des vues de ressource de nuanceur (SRV) de mémoires tampons dynamiques avec la carte de D3D11 \_ \_ \_ sans remplacement \_ . Les runtimes Direct3D 11 et versions antérieures limitent le mappage aux mémoires tampons de vertex ou d’index.

Direct3D 11,1 met à jour la méthode [**ID3D11DeviceContext :: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) pour cette fonctionnalité.

## <a name="use-uavs-at-every-pipeline-stage"></a>Utiliser UAVs à chaque étape du pipeline

Direct3D 11,1 vous permet d’utiliser les modèles de nuanceur 5,0 suivants dans toutes les étapes du nuanceur qui étaient précédemment utilisés dans les nuanceurs de pixels et les nuanceurs de calcul.

-   [\_UAV de \_ type DCL](/windows/desktop/direct3dhlsl/dcl-uav-typed--sm5---asm-)
-   [\_UAV \_ brute du DCL](/windows/desktop/direct3dhlsl/dcl-uav-raw--sm5---asm-)
-   [\_UAV \_ structurée DCL](/windows/desktop/direct3dhlsl/dcl-uav-structured--sm5---asm-)
-   [LD \_ bruts](/windows/desktop/direct3dhlsl/ld-raw--sm5---asm-)
-   [LD \_ structurées](/windows/desktop/direct3dhlsl/ld-structured--sm5---asm-)
-   [LD \_ UAV \_ typé](/windows/desktop/direct3dhlsl/ld-uav-typed--sm5---asm-)
-   [stockage \_ brut](/windows/desktop/direct3dhlsl/store-raw--sm5---asm-)
-   [stockage \_ structuré](/windows/desktop/direct3dhlsl/store-structured--sm5---asm-)
-   [stockage \_ UAV \_ typé](/windows/desktop/direct3dhlsl/store-uav-typed--sm5---asm-)
-   [synchroniser \_ Uglobal](/windows/desktop/direct3dhlsl/sync--sm5---asm-)
-   Tous les Atomic atomiques et les atomices immédiats (par exemple, [Atomic \_ atomique](/windows/desktop/direct3dhlsl/atomic-and--sm5---asm-) et et [IMM \_ Atomic \_ et](/windows/desktop/direct3dhlsl/imm-atomic-and--sm5---asm-))

Direct3D 11,1 met à jour les méthodes suivantes pour cette fonctionnalité.

-   [**ID3D11DeviceContext :: CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**ID3D11DeviceContext :: CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**ID3D11DeviceContext :: CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**ID3D11DeviceContext :: CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**ID3D11DeviceContext :: CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Ces instructions existaient dans Direct3D 11,0 dans PS \_ 5 \_ 0 et CS \_ 5 \_ 0. Étant donné que Direct3D 11,1 rend les UAVs disponibles à toutes les étapes du nuanceur, ces instructions sont disponibles à toutes les étapes du nuanceur.

Si vous transmettez des nuanceurs compilés (VS/HS/DS/HS) qui utilisent l’une de ces instructions à une fonction de création de nuanceur, comme [**CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader), sur les appareils qui ne prennent pas en charge UAVs à chaque étape (y compris les pilotes existants qui ne sont pas implémentés avec cette fonctionnalité), la fonction de création de nuanceur échoue. La fonction Create-Shader échoue également si le nuanceur tente d’utiliser un emplacement UAV au-delà du jeu d’emplacements UAV pris en charge par le matériel.

Les UAVs référencés par ces instructions sont partagés entre toutes les étapes de pipeline. Par exemple, un UAV qui est lié à l’emplacement 0 à l' [étape de fusion de sortie](d3d10-graphics-programming-guide-output-merger-stage.md) est disponible à l’emplacement 0 vers vs/HS/DS/GS/PS.

Les accès UAV que vous émettez à partir de ou à travers les étapes du nuanceur qui s’exécutent dans un dessin donné \* () ou que vous émettez à partir du nuanceur de calcul au sein d’une distribution \* () ne sont pas forcément terminés dans l’ordre dans lequel vous les avez émis. Toutefois, tous les accès UAV se terminent à la fin du dessin \* () ou de la distribution \* ().

## <a name="extended-support-for-warp-devices"></a>Prise en charge étendue des appareils WARPs

Direct3D 11,1 étend la prise en charge des appareils [Warps](overviews-direct3d-11-devices-create-warp.md) , que vous créez en passant la [**\_ \_ \_ distorsion de type de pilote D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) dans le paramètre *DriverType* de [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice).

À compter de la prise en charge des appareils Direct3D 11,1 WARP :

-   Tous les [niveaux de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) Direct3D de 9,1 à 11,1
-   [Nuanceurs](direct3d-11-advanced-stages-compute-shader.md) et [facettisation](direct3d-11-advanced-stages-tessellation.md) de calcul
-   Surfaces partagées. Autrement dit, vous pouvez entièrement partager des surfaces entre des appareils de distorsion, ainsi qu’entre des appareils WARPs dans différents processus.

Les appareils WARP ne prennent pas en charge les fonctionnalités facultatives suivantes :

-   [doubles](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)
-   [encodage ou décodage vidéo](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)
-   [prise en charge du nuanceur de précision minimal](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)

Lorsque vous exécutez une machine virtuelle, Hyper-V, avec votre unité de traitement graphique (GPU) désactivée ou sans pilote d’affichage, vous recevez un appareil de distorsion dont le nom convivial est « carte vidéo Microsoft de base ». Ce périphérique WARP peut exécuter l’expérience Windows complète, qui comprend les applications DWM, Internet Explorer et Windows Store. Ce périphérique WARP prend également en charge l’exécution d’applications héritées qui utilisent [DirectDraw](/windows/desktop/directdraw/directdraw) ou les applications en cours d’exécution qui utilisent Direct3D 3 via Direct3D 11,1.

## <a name="use-direct3d-in-session-0-processes"></a>Utiliser Direct3D dans les processus de la session 0

À compter de Windows 8 et de Windows Server 2012, vous pouvez utiliser la plupart des API Direct3D dans les processus de la session 0.

> [!Note]  
> Ces API de sortie, de fenêtre, de permutation et de présentation ne sont pas disponibles dans les processus de la session 0, car elles ne s’appliquent pas à l’environnement de la session 0 :
>
> -   [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain)
> -   [**IDXGIFactory::GetWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-getwindowassociation)
> -   [**IDXGIFactory::MakeWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation)
> -   [**IDXGIAdapter::EnumOutputs**](/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-enumoutputs)
> -   [**ID3D11Debug::SetFeatureMask**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)
> -   [**ID3D11Debug::SetPresentPerRenderOpDelay**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setpresentperrenderopdelay)
> -   [**ID3D11Debug::SetSwapChain**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setswapchain)
> -   [**ID3D10Debug::SetFeatureMask**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setfeaturemask)
> -   [**ID3D10Debug::SetPresentPerRenderOpDelay**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setpresentperrenderopdelay)
> -   [**ID3D10Debug::SetSwapChain**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setswapchain)
> -   [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdeviceandswapchain)
> -   [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdeviceandswapchain1)
> -   [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)
>
> Si vous appelez l’une des API précédentes dans un processus de session 0, l' [**\_ erreur dxgi \_ n’est pas \_ \_ disponible actuellement**](/windows/desktop/direct3ddxgi/dxgi-error).

 

## <a name="support-for-shadow-buffer-on-feature-level-9"></a>Prise en charge de la mémoire tampon Shadow au niveau de la fonctionnalité 9

Utilisez un sous-ensemble de \_ fonctionnalités de mémoire tampon fantôme Direct3D 10 0 + pour implémenter des effets d’ombre sur le [niveau de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x. Pour plus d’informations sur ce que vous devez faire pour implémenter des effets d’ombre sur le niveau de fonctionnalité 9 \_ x, consultez [implémentation de mémoires tampons secondaires pour le niveau de fonctionnalité Direct3D 9](/previous-versions/windows/apps/jj262110(v=win.10)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nouveautés de Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 