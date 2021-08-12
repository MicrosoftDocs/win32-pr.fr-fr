---
title: Interface ID3DX11Effect (D3dx11effect.h)
description: Une interface ID3DX11Effect gère un ensemble d’objets d’État, de ressources et de nuanceurs pour l’implémentation d’un effet de rendu.
ms.assetid: 34429d51-6b45-4a62-bce1-50c4da02edac
keywords:
- Interface ID3DX11Effect Direct3D 11
- Interface ID3DX11Effect Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11Effect
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 670e60cf68c812b6d8b296aac41c3000fa8c1405c909e8827532625a6cd93b0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535927"
---
# <a name="id3dx11effect-interface"></a>Interface ID3DX11Effect

Une interface **ID3DX11Effect** gère un ensemble d’objets d’État, de ressources et de nuanceurs pour l’implémentation d’un effet de rendu.

## <a name="members"></a>Membres

L’interface **ID3DX11Effect** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ID3DX11Effect** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11Effect** possède ces méthodes.



| Méthode                                                                     | Description                                                                               |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**CloneEffect**](id3dx11effect-cloneeffect.md)                           | Crée une copie d’une interface d’effet.<br/>                                         |
| [**GetClassLinkage**](id3dx11effect-getclasslinkage.md)                   | Obtient une interface de liaison de classe.<br/>                                                |
| [**GetConstantBufferByIndex**](id3dx11effect-getconstantbufferbyindex.md) | Obtient une mémoire tampon constante par index.<br/>                                                |
| [**GetConstantBufferByName**](id3dx11effect-getconstantbufferbyname.md)   | Obtient une mémoire tampon constante par nom.<br/>                                                 |
| [**GetDesc**](id3dx11effect-getdesc.md)                                   | Obtient une description de l’effet.<br/>                                                     |
| [**GetDevice**](id3dx11effect-getdevice.md)                               | Récupérez l’appareil qui a créé l’effet.<br/>                                        |
| [**GetGroupByIndex**](id3dx11effect-getgroupbyindex.md)                   | Obtient un groupe d’effets par index.<br/>                                                 |
| [**GetGroupByName**](id3dx11effect-getgroupbyname.md)                     | Obtient un groupe d’effets par nom.<br/>                                                  |
| [**GetTechniqueByIndex**](id3dx11effect-gettechniquebyindex.md)           | Obtient une technique par index.<br/>                                                      |
| [**GetTechniqueByName**](id3dx11effect-gettechniquebyname.md)             | Obtient une technique par nom.<br/>                                                       |
| [**GetVariableByIndex**](id3dx11effect-getvariablebyindex.md)             | Obtient une variable par index.<br/>                                                       |
| [**GetVariableByName**](id3dx11effect-getvariablebyname.md)               | Obtient une variable par nom.<br/>                                                        |
| [**GetVariableBySemantic**](id3dx11effect-getvariablebysemantic.md)       | Obtenir une variable par sémantique.<br/>                                                    |
| [**IsOptimized**](id3dx11effect-isoptimized.md)                           | Testez un effet pour voir si les métadonnées de réflexion ont été supprimées de la mémoire.<br/> |
| [**IsValid**](id3dx11effect-isvalid.md)                                   | Testez un effet pour voir s’il contient une syntaxe valide.<br/>                             |
| [**Optimiser**](id3dx11effect-optimize.md)                                 | Réduisez la quantité de mémoire requise pour un effet.<br/>                          |



 

## <a name="remarks"></a>Remarques

Un effet est créé en appelant [**D3DX11CreateEffectFromMemory**](d3dx11createeffectfrommemory.md).

Le système d’effet regroupe les informations requises pour le rendu dans un effet qui contient : les objets d’État pour l’affectation des modifications d’État dans les groupes, les ressources pour fournir des données d’entrée et le stockage des données de sortie, ainsi que les programmes qui contrôlent la façon dont le rendu est effectué appelé nuanceurs.

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

> [!Note]
>
> Si vous appelez [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur un objet **ID3DX11Effect** pour récupérer l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , **QueryInterface** retourne E \_ nointerface. Pour contourner ce problème, utilisez le code suivant :
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>    IUnknown* pIUnknown = (IUnknown*)pEffect;
>     pIUnknown->AddRef();</code></pre></td>
> </tr>
> </tbody>
> </table>>
>  

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------|-------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |

## <a name="see-also"></a>Voir aussi

[Effets 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
