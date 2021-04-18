---
description: L’interface IAMTimelineSplittable fractionne un objet Timeline dans les services de modification DirectShow (DES). Les sources, les effets, les transitions et les suivis implémentent cette interface.
ms.assetid: bb066d34-0ffd-495f-83ce-59ad054a7782
title: Interface IAMTimelineSplittable (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7b9544809068029b4ca583e83831f9b18ac84e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523020"
---
# <a name="iamtimelinesplittable-interface"></a>Interface IAMTimelineSplittable

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée dans les versions futures de Windows.\]

 

L' `IAMTimelineSplittable` interface fractionne un objet Timeline dans les [services d’édition DirectShow](directshow-editing-services.md) (des). Les sources, les effets, les transitions et les suivis implémentent cette interface.

## <a name="members"></a>Membres

L’interface **IAMTimelineSplittable** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineSplittable** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAMTimelineSplittable** possède ces méthodes.



| Méthode                                             | Description                                                                                          |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**SplitAt**](iamtimelinesplittable-splitat.md)   | Fractionne l’objet à l’heure spécifiée.<br/>                                                  |
| [**SplitAt2**](iamtimelinesplittable-splitat2.md) | Fractionne l’objet à l’heure spécifiée, spécifié en tant que valeur [**REFTIME**](reftime.md) .<br/> |



 

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



 

 
