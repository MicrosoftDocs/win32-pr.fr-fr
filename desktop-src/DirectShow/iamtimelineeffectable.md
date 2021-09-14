---
description: l’interface IAMTimelineEffectable fournit des méthodes pour ajouter des effets à un objet timeline dans DirectShow Services d’édition (DES) et pour manipuler les effets sur un objet.
ms.assetid: 70f2da64-e16a-4d4d-9522-042b5fa2855c
title: Interface IAMTimelineEffectable (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bc67483f44515c2ce18825de5b6657d51e2c3826
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126853965"
---
# <a name="iamtimelineeffectable-interface"></a>Interface IAMTimelineEffectable

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

l' `IAMTimelineEffectable` interface fournit des méthodes pour ajouter des effets à un objet timeline dans [DirectShow Services de modification](directshow-editing-services.md) (DES) et pour manipuler les effets sur un objet. Tous les objets qui peuvent avoir des effets appliqués implémentent cette interface ; Cela comprend les sources, les pistes et les compositions.

Un objet qui implémente cette interface peut avoir n’importe quel nombre d’effets. Pour chaque objet, le moteur de rendu applique ses effets par ordre de priorité, en commençant par le niveau de priorité 0.

## <a name="members"></a>Membres

L’interface **IAMTimelineEffectable** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineEffectable** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAMTimelineEffectable** possède ces méthodes.



| Méthode                                                                     | Description                                                                   |
|:---------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**EffectGetCount**](iamtimelineeffectable-effectgetcount.md)             | Récupère le nombre d’effets sur cet objet.<br/>                    |
| [**EffectInsBefore**](iamtimelineeffectable-effectinsbefore.md)           | Insère un effet dans l’objet au niveau de priorité spécifié.<br/> |
| [**EffectSwapPriorities**](iamtimelineeffectable-effectswappriorities.md) | Change les niveaux de priorité de deux effets.<br/>                       |
| [**GetEffect**](iamtimelineeffectable-geteffect.md)                       | Récupère l’effet au niveau de priorité spécifié.<br/>              |



 

## <a name="remarks"></a>Notes

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
