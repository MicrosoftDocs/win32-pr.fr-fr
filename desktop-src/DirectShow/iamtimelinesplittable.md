---
description: l’interface IAMTimelineSplittable fractionne un objet timeline en DirectShow Services d’édition (DES). Les sources, les effets, les transitions et les suivis implémentent cette interface.
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
ms.openlocfilehash: fd9f3ca6b1bdea5f80c117b869163d9a2375d5b434765b5962c6216795dd9e64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078969"
---
# <a name="iamtimelinesplittable-interface"></a>Interface IAMTimelineSplittable

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

l' `IAMTimelineSplittable` interface fractionne un objet timeline en [DirectShow Services d’édition](directshow-editing-services.md) (DES). Les sources, les effets, les transitions et les suivis implémentent cette interface.

## <a name="members"></a>Membres

L’interface **IAMTimelineSplittable** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineSplittable** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IAMTimelineSplittable** possède ces méthodes.



| Méthode                                             | Description                                                                                          |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**SplitAt**](iamtimelinesplittable-splitat.md)   | Fractionne l’objet à l’heure spécifiée.<br/>                                                  |
| [**SplitAt2**](iamtimelinesplittable-splitat2.md) | Fractionne l’objet à l’heure spécifiée, spécifié en tant que valeur [**REFTIME**](reftime.md) .<br/> |



 

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



 

 
