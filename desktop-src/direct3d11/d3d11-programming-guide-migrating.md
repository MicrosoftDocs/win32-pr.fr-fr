---
title: Migration vers Direct3D 11
description: Cette section fournit des informations sur la migration vers Direct3D 11 à partir d’une version antérieure de Direct3D.
ms.assetid: 3ec8b5c2-01e6-4fbe-ada7-43898db63bbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ade0a0d32d3f8b5c07e6653955c0c407c8fa8f
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316625"
---
# <a name="migrating-to-direct3d-11"></a>Migration vers Direct3D 11

Cette section fournit des informations sur la migration vers Direct3D 11 à partir d’une version antérieure de Direct3D.

-   [Direct3D 9 vers Direct3D 11](#direct3d-9-to-direct3d-11)
-   [Direct3D 10 vers Direct3D 11](#direct3d-10-to-direct3d-11)
    -   [Énumérations et définitions](#enumerations-and-defines)
    -   [Structures](#structures)
    -   [Interfaces](#interfaces)
    -   [Autres technologies connexes](#other-related-technologies)
-   [Direct3D 10,1 vers Direct3D 11](#direct3d-101-to-direct3d-11)
    -   [Énumérations et définitions](#enumerations-and-defines)
    -   [Structures](#structures)
    -   [Interfaces](#interfaces)
-   [Nouvelles fonctionnalités de Direct3D 11](#new-features-for-direct3d-11)
-   [Nouvelles fonctionnalités de DirectX 11,1](#new-features-for-directx-111)
-   [Nouvelles fonctionnalités de DirectX 11,2](#new-features-for-directx-112)
-   [Rubriques connexes](#related-topics)

## <a name="direct3d-9-to-direct3d-11"></a>Direct3D 9 vers Direct3D 11

L’API Direct3D 11 s’appuie sur les améliorations apportées à l’infrastructure dans Direct3D 10 et 10,1. Le portage de Direct3D 9 vers Direct3D 11 est semblable au passage de Direct3D 9 à Direct3D 10. Voici les principaux défis de cet effort.

-   Suppression de l’utilisation du pipeline de fonction fixe en faveur des nuanceurs programmables créés exclusivement en HLSL (compilé via D3DCompiler au lieu de D3DX9).
-   Gestion d’État basée sur des objets immuables plutôt que sur des basculements d’État individuels.
-   Mise à jour pour respecter les exigences de liaison stricte des mises en page d’entrée de tampon de vertex et des signatures de nuanceur.
-   Association des vues de ressources de nuanceur à toutes les ressources de texture.
-   Mappage de tout le contenu de l’image au \_ format dxgi, y compris la suppression de tous les formats de couleurs de 16 bits (5/5/5/1, 5/6/5, 4/4/4/4), la suppression de tous les formats de couleurs de 24 bits (8/8/8) et le classement des couleurs RVB strict.
-   Fractionnement de l’utilisation globale de l’état constant en plusieurs mémoires tampons constantes mises à jour, plus efficacement.

Pour plus d’informations sur le passage de Direct3D 9 à Direct3D 10, voir [considérations relatives à Direct3D 9 vers Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).

## <a name="direct3d-10-to-direct3d-11"></a>Direct3D 10 vers Direct3D 11

La conversion de programmes écrits pour utiliser l’API Direct3D 10 ou 10,1 est un processus simple, car Direct3D 11 est une extension de l’API existante. Avec une seule exception mineure (indiquée ci-dessous, le filtrage de texte monochrome), toutes les méthodes et fonctionnalités de Direct3D 10/10.1 sont disponibles dans Direct3D 11. Le plan ci-dessous décrit les différences entre les deux API pour faciliter la mise à jour du code existant. Les principales différences sont les suivantes :

-   Les opérations de rendu (dessin, État, etc.) ne font plus partie de l’interface de l’appareil, mais font partie de la nouvelle interface DeviceContext, ainsi que des méthodes de mappage des ressources/de mappage et de requête d’appareil.
-   Direct3D 11 comprend toutes les améliorations et les modifications apportées entre Direct3D 10,0 et 10,1

### <a name="enumerations-and-defines"></a>Énumérations et définitions



| Direct3D 10                            | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_format dxgi                           | [**Dxgi \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)plusieurs nouveaux formats dxgi ont été définis.<br/>                                                                                                                                                                                                                                                                                                                                |
| D3D10 \_ créer \_ un \_ commutateur \_ d’appareil pour \_ référence | [**D3d11 \_ CRÉER \_ un \_ commutateur \_ d’appareil pour \_ ref**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)la fonctionnalité Switch-to-Ref n’est pas prise en charge par Direct3D 11.<br/>                                                                                                                                                                                                                                                                        |
| \_Type de pilote D3D10 \_                    | [**D3D \_ \_Type de pilote**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)Notez que les identificateurs d’énumération dans le [**\_ \_ type de pilote D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) ont été redéfinis à partir des identificateurs dans le [**\_ \_ type de pilote D3D10**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type). Par conséquent, vous devez être sûr d’utiliser les identificateurs d’énumération à la place des nombres littéraux.<br/> [**D3D \_ Le \_ type de pilote**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) est défini dans D3Dcommon. h.<br/> |
| \_ \_ Indicateur div de la ressource D3D10 \_            | [**D3d11 \_ \_ \_ Indicateur divers des ressources**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)Notez que la plupart de ces indicateurs ont été redéfinis. Veillez donc à utiliser des identificateurs d’énumération plutôt que des nombres littéraux.<br/>                                                                                                                                                                                                                                |
| \_Filtre D3D10                          | [**D3d11 \_ FILTRE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter)Notez que le filtrage de texte D3D10 \_ \_ de filtre de texte \_ 1BIT a été supprimé de Direct3D 11. Consultez DirectWrite.<br/>                                                                                                                                                                                                                                                                            |
| \_Compteur d3d11                         | [**D3d11 \_ Notez que les compteurs indépendants**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_counter)du fournisseur ont été supprimés pour Direct3D 11, car ils étaient rarement pris en charge.<br/>                                                                                                                                                                                                                                                                          |
| D3D10 \_ x                               | D3D11 \_ x de nombreuses énumérations et définitions sont identiques, ont des limites plus grandes ou ont des valeurs supplémentaires.<br/>                                                                                                                                                                                                                                                                                                               |



 

### <a name="structures"></a>Structures



| Direct3D 10                              | Direct3D 11                                                                                                                                                 |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ , \_ entrée de Déclaration \_            | [**D3d11 \_ Ainsi, l' \_ \_ entrée de déclaration**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry)Ajoute Stream.<br/>                                                                  |
| D3D10 \_ Blend \_ desc                       | [**D3d11 \_ BLEND \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)Remarque Cette structure a été considérablement modifiée de 10 à 10,1 pour fournir un état de fusion par cible de rendu<br/> |
| Description de la \_ mémoire tampon D3D10 \_                      | [**D3d11 \_ La \_ Description de la mémoire tampon**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)ajoute un StructureByteStride à utiliser avec les ressources de nuanceur de calcul<br/>                                 |
| Vue de la \_ ressource du nuanceur D3D10 \_ \_ \_ desc      | [**D3d11 \_ Vue de la ressource de NUANCEur \_ \_ \_ desc**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)Remarque Cette structure a ajouté des membres d’Union supplémentaires pour 10,1<br/>    |
| \_Vue du stencil de profondeur D3D10 \_ \_ \_ desc        | [**D3d11 \_ La \_ vue du stencil de profondeur \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)a un nouveau membre Flags.<br/>                                                |
| \_Statistiques du \_ \_ pipeline de données de requête D3D10 \_ | [**D3d11 \_ L’interrogation des \_ \_ \_ statistiques de pipeline de données**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics)ajoute plusieurs nouveaux compteurs d’étape de nuanceur.<br/>                  |
| D3D10 \_ x                                 | D3D11 \_ x de nombreuses structures sont identiques entre les deux API.<br/>                                                                                     |



 

### <a name="interfaces"></a>Interfaces



| Direct3D 10        | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID3D10Device       | [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) et [ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)<br/> L’interface de l’appareil a été divisée en deux parties. Pour le portage rapide, vous pouvez utiliser [**ID3D11Device :: GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).<br/> Les méthodes « ID3D10Device :: GetTextFilterSize » et « SetTextFilerSize » n’existent plus. Consultez DirectWrite.<br/> Create \* Shader prend un paramètre facultatif supplémentaire pour [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage).<br/> \*SetShader et \* GetShader prennent des paramètres facultatifs supplémentaires pour [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)(s).<br/> [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) prend un tableau et un nombre pour plusieurs Strides de flux de sortie.<br/> La limite du paramètre NumEntries de [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) a été augmentée à d3d11 \_ , le nombre de \_ flux \_ \* d3d11 donc le \_ \_ \_ nombre de composants de sortie \_ dans Direct3D 11.<br/> |
| ID3D10Buffer       | [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ID3D10SwitchToRef  | [**ID3D11SwitchToRef**](/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref) La fonctionnalité de basculement vers la référence n’est pas prise en charge dans Direct3D 11.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ID3D10Texture1D    | [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ID3D10Texture2D    | [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ID3D10Texture3D    | [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d) Les méthodes Map et unout ont été déplacées vers [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext), et toutes les méthodes cartographiques utilisent la sous- [**\_ \_ ressource mappée d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) au lieu de void \* \* .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ID3D10Asynchronous | [**ID3D11Asynchronous**](/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous) Begin, end et GetData ont été déplacés vers [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ID3D10x            | ID3D11x de nombreuses interfaces sont identiques entre les deux API.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="other-related-technologies"></a>Autres technologies connexes



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Solution 10/10.1</th>
<th>11 solution</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>API de réflexion HLSL (D3D10Compile *, D3DX10Compile*) et nuanceur de nuanceur</td>
<td>D3DCompiler (voir D3DCompiler. h)
<blockquote>
[!Note]<br />
Pour les applications du Windows Store, les <a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference">API D3DCompiler</a> sont prises en charge uniquement pour le développement, et non pour le déploiement.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Effets 10</td>
<td>Les <a href="https://github.com/Microsoft/FX11">effets 11</a> sont disponibles en ligne dans la source partagée.
<blockquote>
[!Note]<br />
Cette solution n’est pas adaptée aux applications du Windows Store, car elle nécessite les <a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference">API D3DCompiler</a> au moment de l’exécution (déploiement).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Mathématiques D3DX9/D3DX10</td>
<td><a href="/windows/desktop/dxmath/directxmath-portal">DirectXMath</a></td>
</tr>
<tr class="even">
<td>D3DX10</td>
<td>D3DX11 dans le SDK DirectX hérité <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a>, <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a>et <a href="https://github.com/Microsoft/DirectXMesh">DirectXMesh</a> offrent des alternatives à de nombreuses technologies dans les bibliothèques d3dx10 et D3DX11 héritées.<br/> <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> et <a href="/windows/desktop/DirectWrite/direct-write-portal">DirectWrite</a> offrent une prise en charge de haute qualité pour le rendu des polices et des lignes de style.<br/></td>
</tr>
</tbody>
</table>



 

Pour plus d’informations sur le SDK DirectX hérité, consultez [où est le kit de développement logiciel (SDK) DirectX ?](/windows/desktop/directx-sdk--august-2009-).

## <a name="direct3d-101-to-direct3d-11"></a>Direct3D 10,1 vers Direct3D 11

Direct3D 10,1 est une extension de l’interface Direct3D 10, et toutes les fonctionnalités de Direct3D 10,1 sont disponibles dans Direct3D 11. La plupart des portages de 10,1 à 11 sont déjà traités ci-dessus en passant de 10 à 11.

### <a name="enumerations-and-defines"></a>Énumérations et définitions



| Direct3D 10,1          | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ fonctionnalité de \_ niveau1 | [**D3D \_ \_Niveau de fonctionnalité**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)identique mais défini dans D3DCommon. h plus l’ajout du \_ niveau de fonctionnalité D3D \_ \_ 11 \_ 0 pour le matériel 11 Class avec le \_ niveau de fonctionnalité D3D \_ \_ 9 \_ 1, le \_ \_ niveau de fonctionnalité D3D \_ 9 \_ 2 et le \_ \_ niveau de fonctionnalité D3D \_ 9 \_ 3 pour 10level9<br/> (D3D10 \_ Le \_ niveau \_ de fonctionnalité 9 \_ 1, le \_ \_ niveau de fonctionnalité D3D10 \_ 9 \_ 2 et le \_ \_ niveau de fonctionnalité D3D10 \_ 9 \_ 3 ont également été ajoutés pour 10,1 à D3D10 \_ 1. h)<br/> |



 

### <a name="structures"></a>Structures



| Direct3D 10,1                        | Direct3D 11                                                                                                                   |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ Blend \_ DESC1                  | [**D3d11 \_ BLEND \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)la version 11 est identique à 10,1.<br/>                                 |
| \_Affichage des ressources du nuanceur D3D10 \_ \_ \_ DESC1 | [**D3d11 \_ Vue de la ressource de NUANCEur \_ \_ \_ desc**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)la version 11 est identique à 10,1.<br/> |



 

### <a name="interfaces"></a>Interfaces



| Direct3D 10,1             | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID3D10Device1             | [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) et [ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)<br/> L’interface de l’appareil a été divisée en deux parties. Pour le portage rapide, vous pouvez utiliser [**ID3D11Device :: GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).<br/> Les méthodes « ID3D10Device :: GetTextFilterSize » et « SetTextFilerSize » n’existent plus. Consultez DirectWrite.<br/> Create \* Shader prend un paramètre facultatif supplémentaire pour [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage).<br/> \*SetShader et \* GetShader prennent des paramètres facultatifs supplémentaires pour [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)(s).<br/> [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) prend un tableau et un nombre pour plusieurs Strides de flux de sortie.<br/> La limite du paramètre NumEntries de [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) a été augmentée à d3d11 \_ , le nombre de \_ flux \_ \* d3d11 donc le \_ \_ \_ nombre de composants de sortie \_ dans Direct3D 11.<br/> |
| ID3D10BlendState1         | [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ID3D10ShaderResourceView1 | [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="new-features-for-direct3d-11"></a>Nouvelles fonctionnalités de Direct3D 11

Une fois votre code mis à jour pour utiliser l’API Direct3D 11, de nombreuses [nouvelles fonctionnalités](direct3d-11-features.md) sont à prendre en compte.

-   Rendu multithread à l’aide de listes de commandes et de plusieurs contextes
-   Implémentation d’algorithmes avancés à l’aide du nuanceur de calcul (à l’aide des profils de nuanceur 4,0, 4,1 ou 5,0)
-   Nouvelles fonctionnalités matérielles de 11 classes :
    -   Modèle de nuanceur HLSL 5,0
    -   Liaison de nuanceur dynamique
    -   Pavage via les nuanceurs de la coque et du domaine
    -   Nouveaux formats de compression de bloc : BC6H pour les images HDR, BC7 pour les images standard haute fidélité
-   Utilisation de la [technologie 10level9](overviews-direct3d-11-devices-downlevel.md) pour le rendu sur de nombreux appareils de nuanceur 2,0 et modèle de nuanceur 3,0 via l’API DIrect3D 11 pour la prise en charge de matériel vidéo de bas de gamme sur Windows Vista et Windows 7.
-   Tirer parti du périphérique de rendu logiciel WARP.

## <a name="new-features-for-directx-111"></a>Nouvelles fonctionnalités de DirectX 11,1

Windows 8 comprend d’autres améliorations graphiques DirectX à prendre en compte lors de l’implémentation de votre code graphique DirectX, notamment [Direct3D 11,1](direct3d-11-features.md), [DXGI 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements), [Windows Display Driver Model (WDDM) 1,2](/windows-hardware/drivers/display/wddm-in-windows-8), le matériel de [niveau de fonctionnalité](overviews-direct3d-11-devices-downlevel-intro.md) 11,1, les contextes de périphérique Direct2D et d’autres améliorations.

La prise en charge partielle de [Direct3D 11,1](direct3d-11-features.md) est également disponible sur Windows 7, par le biais de la [mise à jour de plateforme pour Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7), disponible via la [mise à jour de plateforme pour Windows 7](https://support.microsoft.com/kb/2670838).

## <a name="new-features-for-directx-112"></a>Nouvelles fonctionnalités de DirectX 11,2

Le Windows 8.1 comprend [Direct3D 11,2](direct3d-11-2-features.md), [DXGI 1,3](/windows/desktop/direct3ddxgi/dxgi-1-3-improvements), ainsi que d’autres améliorations.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour Direct3D 11](dx-graphics-overviews.md)
</dt> <dt>

[Effets (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

