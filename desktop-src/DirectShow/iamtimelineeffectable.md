---
description: L’interface IAMTimelineEffectable fournit des méthodes pour ajouter des effets à un objet Timeline dans les services de modification DirectShow (DES) et pour manipuler les effets sur un objet.
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539273"
---
# <a name="iamtimelineeffectable-interface"></a>Interface IAMTimelineEffectable

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `IAMTimelineEffectable` interface fournit des méthodes pour ajouter des effets à un objet Timeline dans les [services de modification DirectShow](directshow-editing-services.md) (des) et pour manipuler les effets sur un objet. Tous les objets qui peuvent avoir des effets appliqués implémentent cette interface ; Cela comprend les sources, les pistes et les compositions.

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
> Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
