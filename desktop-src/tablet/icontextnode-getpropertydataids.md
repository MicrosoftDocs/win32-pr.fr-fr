---
description: Récupère les identificateurs pour lesquels il existe des données de propriété.
ms.assetid: c9c491b7-95e2-421a-8632-f65844cd5ef9
title: 'IContextNode :: GetPropertyDataIds, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPropertyDataIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 94aab2b91a5da9588de65f5a48bf496bdceae71bf4aa90f82f3969cbe6a9e76e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935369"
---
# <a name="icontextnodegetpropertydataids-method"></a>IContextNode :: GetPropertyDataIds, méthode

Récupère les identificateurs pour lesquels il existe des données de propriété.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPropertyDataIds(
  [out] ULONG *pulGuidCount,
  [out] GUID  **ppGuids
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pulGuidCount* \[ à\]
</dt> <dd>

Nombre de propriétés.

</dd> <dt>

*ppGuids* \[ à\]
</dt> <dd>

Identificateurs pour lesquels il existe des données de propriété.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *ppGuids* lorsque vous n’avez plus besoin des informations.

 

Cette méthode retourne les identificateurs spécifiques à l’application pour les données de propriété qui ont été ajoutées. Elle retourne également les identificateurs pour les données de propriété internes, qui sont décrites par les constantes des [Propriétés du nœud de contexte](context-node-properties.md) .

## <a name="requirements"></a>Configuration requise



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

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

