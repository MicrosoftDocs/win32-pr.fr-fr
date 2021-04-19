---
description: Met à jour la zone de ce IContextNode.
ms.assetid: e7001411-17e4-4f33-af04-dd3220275895
title: 'IContextNode :: SetLocation, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetLocation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 20daefeab7a9e36d5e968d5d14bfa5110d733487
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517511"
---
# <a name="icontextnodesetlocation-method"></a>IContextNode :: SetLocation, méthode

Met à jour la zone de ce [**IContextNode**](icontextnode.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetLocation(
  [in] IAnalysisRegion *pIAnalysisRegion
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pIAnalysisRegion* \[ dans\]
</dt> <dd>

[**IAnalysisRegion**](ianalysisregion.md) décrivant la zone dans laquelle définir l’emplacement de l’objet [**IContextNode**](icontextnode.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Notes

Utilisez cette méthode pour mettre à jour l’emplacement du nœud de contexte (consultez [**IContextNode :: GetLocation**](icontextnode-getlocation.md)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IContextNode::GetLocation**](icontextnode-getlocation.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




