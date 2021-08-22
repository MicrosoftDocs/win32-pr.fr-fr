---
description: Récupère un tableau d’octets qui contient les données de propriété internes et spécifiques à l’application pour ce IContextNode.
ms.assetid: f26d71a7-fe71-48a8-9c8f-9c4d99261df1
title: 'IContextNode :: SavePropertiesData, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SavePropertiesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5b02f5df7526b429a65b2a0baf49bda4571dd718a9bff875c79b7e325de244ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719683"
---
# <a name="icontextnodesavepropertiesdata-method"></a>IContextNode :: SavePropertiesData, méthode

Récupère un tableau d’octets qui contient les données de propriété internes et spécifiques à l’application pour ce [**IContextNode**](icontextnode.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SavePropertiesData(
  [in, out] ULONG *pulPropertiesDataSize,
  [out]     BYTE  **ppbPropertiesData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pulPropertiesDataSize* \[ in, out\]
</dt> <dd>

Taille du tableau de données contenant les informations de propriété. La valeur passée n’est pas utilisée.

</dd> <dt>

*ppbPropertiesData* \[ à\]
</dt> <dd>

Pointeur vers un tableau d’entiers non signés 8 bits qui contient les données de propriété internes et spécifiques à l’application.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.

## <a name="remarks"></a>Remarques

> [!Caution]  
> Pour éviter une fuite de mémoire, utilisez [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire à partir de \* *ppbPropertiesData* lorsque vous n’avez plus besoin des informations.

 

Utilisez cette méthode lorsque votre application gère sa propre structure de données, qui est synchronisée avec celle du [**IInkAnalyzer**](iinkanalyzer.md). Cette méthode enregistre les données de propriétés définies par **IInkAnalyzer** sur [**IContextNode**](icontextnode.md).

Pour plus d’informations sur la synchronisation des données de votre application avec [**IInkAnalyzer**](iinkanalyzer.md), consultez [Data proxy with Ink Analysis](data-proxy-with-ink-analysis.md).

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

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[Référence de l’analyse de l’encre](ink-analysis-reference.md)
</dt> </dl>

 

