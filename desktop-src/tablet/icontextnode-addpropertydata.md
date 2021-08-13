---
description: Ajoute un élément de données spécifiques à l’application.
ms.assetid: 86ba37ac-8e65-4397-8ed1-37463152bebd
title: 'IContextNode :: AddPropertyData, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8c9988217aed21ff1142f0e2083bee568ed12c31d90530ac1f3e9f5719c46446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719693"
---
# <a name="icontextnodeaddpropertydata-method"></a>IContextNode :: AddPropertyData, méthode

Ajoute un élément de données spécifiques à l’application.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT AddPropertyData(
  [in] const GUID  *pPropertyDataId,
  [in]       ULONG ulPropertyDataSize,
  [in]       BYTE  *pbPropertiesData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pPropertyDataId* \[ dans\]
</dt> <dd>

Identificateur global unique (GUID) utilisé pour identifier le type de données.

</dd> <dt>

*ulPropertyDataSize* \[ dans\]
</dt> <dd>

Taille des données en octets.

</dd> <dt>

*pbPropertiesData* \[ dans\]
</dt> <dd>

\[dans, la taille \_ est (ulPropertyDataSize)\]

Tableau d’entiers non signés 8 bits contenant les informations de propriété à ajouter.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

Utilisez **IContextNode :: AddPropertyData** pour associer des données à un nœud de contexte. Pour récupérer les données ultérieurement, utilisez [**IContextNode :: GetPropertyData**](icontextnode-getpropertydata.md).

L’analyseur d’encre peut supprimer le nœud dans le cadre de l’analyse de l’encre, sauf si le nœud de contexte est confirmé (consultez [**IContextNode :: Confirm**](icontextnode-confirm.md)). Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

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

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> </dl>

 

 




