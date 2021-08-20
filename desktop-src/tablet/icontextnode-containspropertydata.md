---
description: Détermine si l’objet IContextNode contient des données stockées sous l’identificateur spécifié.
ms.assetid: ac3a85a2-abf8-4ac4-8779-d9fda89497d4
title: 'IContextNode :: ContainsPropertyData, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.ContainsPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 7bf840b921461f7b767d622a3daecd7b9d3dc3ad8d93b90b7b1f8cfa4d101af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118044850"
---
# <a name="icontextnodecontainspropertydata-method"></a>IContextNode :: ContainsPropertyData, méthode

Détermine si l’objet [**IContextNode**](icontextnode.md) contient des données stockées sous l’identificateur spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ContainsPropertyData(
  [in]  const GUID         *pPropertyDataId,
  [out]       VARIANT_BOOL *pbContains
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPropertyDataId* \[ dans\]
</dt> <dd>

Identificateur des données.

</dd> <dt>

*pbContains* \[ à\]
</dt> <dd>

**Variante \_ TRUE** si l’objet [**IContextNode**](icontextnode.md) contient des données stockées sous l’identificateur spécifié ; Sinon, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Outre les données spécifiques à l’application, vous pouvez également utiliser cette méthode pour déterminer si ce [**IContextNode**](icontextnode.md) contient d’autres données internes (voir Propriétés de l' [indicateur d’analyse](analysis-hint-properties.md) et propriétés du nœud de [contexte](context-node-properties.md)).

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                 |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                     |
| En-tête<br/>                   | <dl> <dt>IACom. h (nécessite également IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




