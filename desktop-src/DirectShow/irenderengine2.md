---
description: l’interface IRenderEngine2 permet à l’application de remplacer le filtre de redimensionnement vidéo par défaut utilisé par les Services d’édition de DirectShow (DES). Le moteur de rendu de base et le moteur de rendu intelligent prennent tous deux en charge cette interface.
ms.assetid: 37603c73-e199-431a-9a1e-a40c77755c70
title: Interface IRenderEngine2 (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ed7802cf3d47d745b4e4733bb1fb60c61130b44a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857535"
---
# <a name="irenderengine2-interface"></a>Interface IRenderEngine2

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

l' `IRenderEngine2` interface permet à l’application de remplacer le filtre de redimensionnement vidéo par défaut utilisé par les Services d’édition de DirectShow (DES). Le [moteur de rendu de base](basic-render-engine.md) et le [moteur de rendu intelligent](smart-render-engine.md) prennent tous deux en charge cette interface.

## <a name="members"></a>Membres

L’interface **IRenderEngine2** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IRenderEngine2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IRenderEngine2** possède ces méthodes.



| Méthode                                                  | Description                                                                             |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**SetResizerGUID**](irenderengine2-setresizerguid.md) | Spécifie le CLSID d’un filtre de redimensionnement personnalisé fourni par l’application.<br/> |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | DirectX 9,0 ou version ultérieure<br/>                                                         |
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fournir un redimensionnement vidéo personnalisé](providing-a-custom-video-resizer.md)
</dt> </dl>

 

 
