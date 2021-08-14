---
description: 'Recrée les données de propriété internes et spécifiques à l’application pour un tableau d’octets précédemment créé avec IContextNode :: SavePropertiesData.'
ms.assetid: 2d24d0da-16f1-4ddc-8e2e-93c312ecfa42
title: 'IContextNode :: LoadPropertiesData, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.LoadPropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8d58c37dc91fac9704221fae13505f5e32c6e48d097133e3aad9154f5f2ec3e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719673"
---
# <a name="icontextnodeloadpropertiesdata-method"></a>IContextNode :: LoadPropertiesData, méthode

Recrée les données de propriété internes et spécifiques à l’application pour un tableau d’octets précédemment créé avec [**IContextNode :: SavePropertiesData**](icontextnode-savepropertiesdata.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT LoadPropertiesData(
  [in]  ULONG        cbPropertiesDataSize,
  [in]  BYTE         *pbPropertiesData,
  [out] VARIANT_BOOL *pfSuccessful
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cbPropertiesDataSize* \[ dans\]
</dt> <dd>

Taille du tableau de données des propriétés.

</dd> <dt>

*pbPropertiesData* \[ dans\]
</dt> <dd>

Tableau d’entiers non signés 8 bits contenant les informations de propriété à charger.

</dd> <dt>

*pfSuccessful* \[ à\]
</dt> <dd>

**Variante \_ TRUE** si les données de propriété ont été correctement chargées ; Sinon, **Variant \_ false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

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

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

 




