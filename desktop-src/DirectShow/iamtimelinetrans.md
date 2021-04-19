---
description: L’interface IAMTimelineTrans fournit des méthodes de manipulation des transitions dans les services de modification DirectShow (DES).
ms.assetid: e29ff0cc-0e48-4a72-8a1b-051ed62c8130
title: Interface IAMTimelineTrans (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cd3c39d0a5434befdd5607b340fef936644bf48e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541748"
---
# <a name="iamtimelinetrans-interface"></a>Interface IAMTimelineTrans

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `IAMTimelineTrans` interface fournit des méthodes pour la manipulation des transitions dans les [services de modification DirectShow](directshow-editing-services.md) (des). Une transition est une progression entre une couche vidéo et le rendu composite de toutes les couches vidéo avec une priorité plus faible. Une transition peut être ajoutée à n’importe quel objet Timeline qui expose l’interface [**IAMTimelineTransable**](iamtimelinetransable.md) . Pour définir les propriétés d’une transition, utilisez l’interface [**IPropertySetter**](ipropertysetter.md) .

L’objet de transition DES est en fait un wrapper pour un objet de transformation DirectX. Tout objet de transformation DirectX à 2 entrées peut être utilisé pour implémenter l’effet visuel de la transition. Microsoft ne prend plus en charge le développement d’objets de transformation DirectX tiers. Pour spécifier l’objet de transformation DirectX pour une transition, appelez la méthode [**IAMTimelineObj :: SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) .

Pour créer un objet de transition, appelez [**IAMTimeline :: CreateEmptyNode**](iamtimeline-createemptynode.md) avec la \_ transition de type principale de la valeur Timeline \_ \_ . Vous pouvez interroger le pointeur [**IAMTimelineObj**](iamtimelineobj.md) retourné pour l' `IAMTimelineTrans` interface.

## <a name="members"></a>Membres

L’interface **IAMTimelineTrans** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineTrans** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAMTimelineTrans** possède ces méthodes.



| Méthode                                                  | Description                                                                            |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**GetCutPoint**](iamtimelinetrans-getcutpoint.md)     | Récupère le point de coupe.<br/>                                                    |
| [**GetCutPoint2**](iamtimelinetrans-getcutpoint2.md)   | Récupère le point de coupe, en tant que valeur [**REFTIME**](reftime.md) .<br/>             |
| [**GetCutsOnly**](iamtimelinetrans-getcutsonly.md)     | Détermine si la transition est rendue sous la forme d’une coupe.<br/>                     |
| [**GetSwapInputs**](iamtimelinetrans-getswapinputs.md) | Récupère une valeur qui indique si les entrées de transition sont échangées.<br/> |
| [**SetCutPoint**](iamtimelinetrans-setcutpoint.md)     | Définit le point de coupe.<br/>                                                         |
| [**SetCutPoint2**](iamtimelinetrans-setcutpoint2.md)   | Définit le point de coupe comme valeur [**REFTIME**](reftime.md) .<br/>                  |
| [**SetCutsOnly**](iamtimelinetrans-setcutsonly.md)     | Spécifie si la transition est rendue sous la forme d’une coupe.<br/>                      |
| [**SetSwapInputs**](iamtimelinetrans-setswapinputs.md) | Spécifie si les entrées de transition sont échangées.<br/>                        |



 

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

 

 
