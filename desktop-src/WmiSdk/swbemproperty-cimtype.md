---
description: La propriété CIMType de l’objet SWbemProperty est un entier qui peut être utilisé pour déterminer le type CIM de cette propriété. Cette propriété est en lecture seule.
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.tgt_platform: multiple
title: SWbemProperty. CIMType, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.CIMType
- ISWbemProperty.CIMType
- ISWbemProperty.get_CIMType
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 416101df1c3ae8542d3d2cd170b873407f007c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952152"
---
# <a name="swbempropertycimtype-property"></a>SWbemProperty. CIMType, propriété

La propriété **CimType** de l’objet [**SWbemProperty**](swbemproperty.md) est un entier qui peut être utilisé pour déterminer le type CIM de cette propriété. Cette propriété est en lecture seule.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
SWbemProperty.CIMType As Integer
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Notes

Pour plus d’informations sur les types valides pour cette propriété, consultez [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).

Les instances d’objets incorporés sont stockées dans des objets composites en tant que propriétés de type **\_ objet CIM**. Pour déterminer la classe d’un objet incorporé dans une instance d’une classe composite, vous devez examiner le qualificateur **CimType** de la propriété type d' **\_ objet CIM** .

Les références d’objet dans une classe d’association sont stockées dans des propriétés de type **\_ référence CIM**. Pour déterminer les chemins d’accès aux objets réels, vous devez examiner le qualificateur **CimType** de la propriété type de **\_ référence CIM** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemProperty<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemProperty<br/>                                                          |



 

 




