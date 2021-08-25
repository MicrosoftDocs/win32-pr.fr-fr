---
description: l’interface IAMTimelineEffect fournit des méthodes de manipulation des effets audio et vidéo dans les Services d’édition de DirectShow.
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
ms.openlocfilehash: f710693c967e1f0ac73c69534e8ac90a65d6603e749cd2aeae6a355ed8517415
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052759"
---
# <a name="iamtimelineeffect-interface"></a>Interface IAMTimelineEffect

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

l' `IAMTimelineEffect` interface fournit des méthodes de manipulation des effets audio et vidéo dans les [Services d’édition de DirectShow](directshow-editing-services.md) . Un effet peut être ajouté à n’importe quel objet Timeline qui expose l’interface [**IAMTimelineEffectable**](iamtimelineeffectable.md) . Pour définir des propriétés sur un effet, utilisez l’interface [**IPropertySetter**](ipropertysetter.md) .

L’objet DES EFFETS DES est en fait un wrapper pour l’un des deux autres objets :

-   pour les effets audio, tout DirectShow filtre d’effet audio.
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



 

## <a name="remarks"></a>Remarques

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation des effets et des transitions](working-with-effects-and-transitions.md)
</dt> </dl>

 

 
