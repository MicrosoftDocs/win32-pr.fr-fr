---
description: L’interface IAMTimelineEffect fournit des méthodes pour manipuler les effets audio et vidéo dans les services de modification DirectShow (DES).
ms.assetid: 3cc8a5f8-3f57-4e2b-82dd-827e04c771f7
title: Interface IAMTimelineEffect (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8b9936616b9c4487849053d36c6a63290bd16b5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537917"
---
# <a name="iamtimelineeffect-interface"></a>Interface IAMTimelineEffect

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `IAMTimelineEffect` interface fournit des méthodes pour manipuler les effets audio et vidéo dans les [services de modification DirectShow](directshow-editing-services.md) (des). Un effet peut être ajouté à n’importe quel objet Timeline qui expose l’interface [**IAMTimelineEffectable**](iamtimelineeffectable.md) . Pour définir des propriétés sur un effet, utilisez l’interface [**IPropertySetter**](ipropertysetter.md) .

L’objet DES EFFETS DES est en fait un wrapper pour l’un des deux autres objets :

-   Pour les effets audio, n’importe quel filtre d’effet audio DirectShow.
-   Pour les effets vidéo, et 1-entrée de l’objet de transformation DirectX.

Microsoft ne prend plus en charge le développement d’objets de transformation DirectX tiers.

Pour spécifier le filtre ou l’objet de transformation DirectX pour un effet, appelez la méthode [**IAMTimelineObj :: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .

Pour créer un objet Effect, appelez [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) avec l’effet de type principal de chronologie des valeurs \_ \_ \_ . Vous pouvez interroger le pointeur [**IAMTimelineObj**](iamtimelineobj.md) retourné pour l' `IAMTimelineEffect` interface.

## <a name="members"></a>Membres

L’interface **IAMTimelineEffect** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineEffect** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAMTimelineEffect** possède ces méthodes.



| Méthode                                                           | Description                                       |
|:-----------------------------------------------------------------|:--------------------------------------------------|
| [**EffectGetPriority**](iamtimelineeffect-effectgetpriority.md) | Récupère le niveau de priorité de l’effet.<br/> |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation des effets et des transitions](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
