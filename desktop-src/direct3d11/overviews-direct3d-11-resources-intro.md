---
title: Présentation d’une ressource dans Direct3D 11
description: Cette rubrique présente les ressources Direct3D, telles que les mémoires tampons et les textures.
ms.assetid: 9e991ab0-9648-484a-9a2c-5391ee5abf20
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cc6f9ba62bdfedc59ff2a152588ccad3d81423d55f8c230ff3836c52e5251d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098244"
---
# <a name="introduction-to-a-resource-in-direct3d-11"></a>Présentation d’une ressource dans Direct3D 11

Les ressources sont les blocs de construction de votre scène. Ils contiennent la plupart des données utilisées par Direct3D pour interpréter et rendre votre scène. Les ressources sont des zones en mémoire accessibles par le pipeline Direct3D. Les ressources contiennent les types de données suivants : Geometry, textures, données de nuanceur. Cette rubrique présente les ressources Direct3D, telles que les mémoires tampons et les textures.

Vous pouvez créer des ressources fortement typées ou non typées. vous pouvez contrôler si les ressources ont un accès en lecture et en écriture. vous pouvez rendre les ressources accessibles uniquement au processeur, au GPU ou aux deux. Jusqu’à 128 ressources peuvent être actives à chaque phase du pipeline.

Direct3D garantit de retourner zéro pour toute ressource qui est accessible à partir de limites.

Le cycle de vie d’une ressource Direct3D est le suivant :

-   Créez une ressource à l’aide de l’une des méthodes Create de l’interface [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .
-   Liez une ressource au pipeline à l’aide d’un contexte et de l’une des méthodes Set de l’interface [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .
-   Désallouez une ressource en appelant la méthode [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) de l’interface de ressource.

Cette section contient les rubriques suivantes :

-   [Typage fort et de typage faible](#strong-vs-weak-typing)
-   [Affichages des ressources](#resource-views)
-   [Affichages bruts de mémoires tampons](#raw-views-of-buffers)
-   [Rubriques connexes](#related-topics)

## <a name="strong-vs-weak-typing"></a>Typage fort et de typage faible

Il existe deux façons de spécifier entièrement la disposition (ou l’encombrement mémoire) d’une ressource :

-   Typé : spécifiez entièrement le type lorsque la ressource est créée.
-   Type : spécifiez entièrement le type lorsque la ressource est liée au pipeline.

La création d’une ressource entièrement typée restreint la ressource au format avec lequel elle a été créée. Cela permet au runtime d’optimiser l’accès, surtout si la ressource est créée avec des indicateurs indiquant qu’elle ne peut pas être mappée par l’application. Les ressources créées avec un type spécifique ne peuvent pas être réinterprétées à l’aide du mécanisme de vue, à moins que la ressource ait été créée avec l' \_ indicateur D3D10 DDI \_ Bind \_ présent. Si \_ \_ la liaison DDI D3D10 \_ présente est définie, les vues de la cible ou de la ressource de nuanceur peuvent être créées sur ces ressources à l’aide de l’un des membres entièrement typés de la famille appropriée, même si la ressource d’origine a été créée comme étant entièrement typée.

Dans un type inférieur à une ressource, le type de données est inconnu lorsque la ressource est créée pour la première fois. L’application doit choisir parmi les formats de type disponibles moins ( [**voir \_ format dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)). Vous devez spécifier la taille de la mémoire à allouer et déterminer si le runtime doit générer les sous-textures dans un mipmap. Toutefois, le format de données exact (si la mémoire est interprétée comme des entiers, des valeurs à virgule flottante, des entiers non signés, etc.) n’est pas déterminé tant que la ressource n’est pas liée au pipeline avec un [affichage des ressources](#resource-views). Étant donné que le format de texture reste flexible jusqu’à ce que la texture soit liée au pipeline, la ressource est appelée stockage faiblement typé. Le stockage faiblement typé présente l’avantage de pouvoir être réutilisé ou réinterprété dans un autre format, à condition que le nombre de composants et le nombre de bits de chaque composant soient identiques dans les deux formats.

Une seule ressource peut être liée à plusieurs étapes de pipeline, à condition que chacune ait une vue unique, qui qualifie entièrement les formats à chaque emplacement. Par exemple, une ressource créée au format DXGI format \_ \_ R32G32B32A32 \_ peut être utilisée en tant que \_ format dxgi \_ R32G32B32A32 \_ float et un \_ format dxgi \_ R32G32B32A32 \_ uint à différents emplacements dans le pipeline simultanément.

## <a name="resource-views"></a>Affichages des ressources

Les ressources peuvent être stockées dans des formats mémoire à usage général afin de pouvoir être partagées par plusieurs étapes de pipeline. Une étape de pipeline interprète les données de ressources à l’aide d’une vue. Un affichage des ressources est conceptuellement similaire au cast des données de ressources afin qu’elles puissent être utilisées dans un contexte particulier.

Une vue peut être utilisée avec une ressource sans type. Autrement dit, vous pouvez créer une ressource au moment de la compilation et déclarer le type de données lorsque la ressource est liée au pipeline. Une vue créée pour une ressource non typée a toujours le même nombre de bits par composant ; la façon dont les données sont interprétées dépend du format spécifié. Le format spécifié doit provenir de la même famille que le format non typé utilisé lors de la création de la ressource. Par exemple, une ressource créée avec le format R8G8B8A8 sans \_ type ne peut pas être affichée en tant que \_ ressource float R32, même si les deux formats peuvent avoir la même taille en mémoire.

Une vue expose également d’autres fonctionnalités telles que la capacité à lire des surfaces de gabarit/de profondeur dans un nuanceur, à générer un carte cubique dynamique en une seule passe et à effectuer le rendu simultanément sur plusieurs secteurs d’un volume.



| Interface de ressource                                             | Description                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**ID3D11DepthStencilView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11depthstencilview)       | Accédez à une ressource de texture pendant le test des stencils de profondeur.                                       |
| [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)       | Accédez à une ressource de texture utilisée en tant que cible de rendu.                                    |
| [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)   | Accédez à une ressource de nuanceur, telle qu’une mémoire tampon constante, une mémoire tampon de texture, une texture ou un échantillonneur. |
| [**ID3D11UnorderedAccessView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11unorderedaccessview) | Accédez à une ressource non ordonnée à l’aide d’un nuanceur de pixels ou d’un nuanceur de calcul.                        |



 

## <a name="raw-views-of-buffers"></a>Affichages bruts de mémoires tampons

Vous pouvez considérer une mémoire tampon brute, qui peut également être appelée [mémoire tampon d’adresse en octets](direct3d-11-advanced-stages-cs-resources.md), comme un conteneur de bits vers lequel vous voulez un accès brut, autrement dit, une mémoire tampon qui vous permet d’accéder facilement via des segments d’une aux valeurs d’adresse sans type 4 32 bits. Vous indiquez que vous souhaitez un accès brut à une mémoire tampon (ou à une vue brute d’une mémoire tampon) quand vous appelez l’une des méthodes suivantes pour créer une vue dans la mémoire tampon :

-   Pour créer un affichage des ressources de nuanceur (SRV) dans la mémoire tampon, appelez [**ID3D11Device :: CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview) avec l’indicateur [**d3d11 \_ BUFFEREX \_ SRV \_ \_ RAW**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bufferex_srv_flag). Vous spécifiez cet indicateur dans le membre **Flags** de la structure [**d3d11 \_ BUFFEREX \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_bufferex_srv) . Vous définissez **d3d11 \_ BUFFEREX \_ SRV** dans le membre **BUFFEREX** de la structure DESC de la vue des [**ressources du \_ nuanceur \_ \_ \_ d3d11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) sur lequel le paramètre *pDesc* de **ID3D11Device :: CreateShaderResourceView** pointe. Vous définissez également la valeur BUFFEREX de la [**\_ \_ \_ dimension SRV d3d11**](/previous-versions/windows/desktop/legacy/ff476217(v=vs.85)) dans le membre **ViewDimension** de la vue de la **ressource du \_ nuanceur d3d11 \_ \_ \_ desc** pour indiquer que le SRV est un affichage brut.
-   Pour créer une vue d’accès non triée (UAV) dans la mémoire tampon, appelez [**ID3D11Device :: CreateUnorderedAccessView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createunorderedaccessview) avec l’indicateur [**d3d11 \_ buffer \_ UAV \_ Flag \_ RAW**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_buffer_uav_flag). Vous spécifiez cet indicateur dans le membre **Flags** de la structure UAV de la [**\_ mémoire tampon \_ d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_uav) . Vous définissez **d3d11 \_ buffer \_ UAV** dans le membre de la **mémoire tampon** de la structure [**desc (vue d' \_ accès non triée \_ \_ \_ ) d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_unordered_access_view_desc) à laquelle le paramètre *pDesc* de **ID3D11Device :: CreateUnorderedAccessView** pointe. Vous définissez également la valeur de la [**\_ \_ \_ mémoire tampon de la dimension d3d11 UAV**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_uav_dimension) dans le membre **ViewDimension** de la **vue d’accès non \_ trié d3d11 \_ \_ \_ desc** pour indiquer que le UAV est un affichage brut.

Vous pouvez utiliser les types d’objets HLSL [**ByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer) et [**RWByteAddressBuffer**](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer) lorsque vous utilisez des mémoires tampons brutes.

Pour créer un affichage brut dans une mémoire tampon, vous devez d’abord appeler [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) avec l’indicateur de [**\_ mémoire tampon misc de la ressource d3d11 \_ autoriser les \_ \_ \_ \_ affichages bruts**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) pour créer la ressource de mémoire tampon sous-jacente. Vous spécifiez cet indicateur dans le membre **MiscFlags** de la structure [**\_ \_ desc de mémoire tampon d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) à laquelle le paramètre *pDesc* de **ID3D11Device :: CreateBuffer** pointe. Vous ne pouvez pas combiner les indicateurs de **\_ mémoire tampon diverse de la ressource d3d11 \_ autoriser les \_ \_ \_ \_ affichages bruts** avec la [**mise en \_ \_ \_ mémoire tampon \_ diverse de la ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag). En outre, si vous spécifiez d3d11 de la mémoire [**\_ \_ \_ tampon constante**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) dans **BindFlags** de la description de la **\_ mémoire tampon \_ d3d11**, vous ne pouvez pas également spécifier **d3d11 la \_ \_ mémoire tampon diverse des ressources autorise les \_ \_ \_ \_ affichages bruts** dans **MiscFlags**. Il ne s’agit pas d’une limitation des affichages bruts, car les mémoires tampons constantes ont déjà une contrainte qu’elles ne peuvent pas être combinées avec une autre vue.

À part les cas non valides précédents, lorsque vous créez une mémoire tampon avec la [**\_ mémoire tampon diverse de la ressource d3d11 \_ \_ \_ autorisez des \_ \_ affichages bruts**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag), vous n’êtes pas limité en matière de fonctionnalités plutôt que de définir des **\_ \_ \_ \_ \_ \_ vues brutes dans la mémoire tampon d3d11 des ressources**. Autrement dit, vous pouvez utiliser ce type de mémoire tampon pour un accès non brut dans un certain nombre de méthodes possibles avec Direct3D. Si vous spécifiez l’indicateur de **\_ \_ \_ \_ \_ \_ vues brutes pour la ressource d3d11** , vous augmentez uniquement les fonctionnalités disponibles.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources](overviews-direct3d-11-resources.md)
</dt> <dt>

[Nouveaux types de ressources](direct3d-11-advanced-stages-cs-resources.md)
</dt> </dl>

 

 