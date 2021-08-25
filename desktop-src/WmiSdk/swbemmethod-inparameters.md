---
description: La propriété Parameters de l’objet SWbemMethod est un objet SWbemObject dont les propriétés définissent les paramètres d’entrée de cette méthode.
ms.assetid: fba1bb97-29f9-41d3-8ecc-f283989118c1
ms.tgt_platform: multiple
title: SWbemMethod. Parameters, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.InParameters
- ISWbemMethod.InParameters
- ISWbemMethod.get_InParameters
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: aa6407ab3da424852b7896f5e4a60490efea140da6e45287991b0d9e96dd9cbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955159"
---
# <a name="swbemmethodinparameters-property"></a>SWbemMethod. Parameters, propriété

La propriété **Parameters** de l’objet [**SWbemMethod**](swbemmethod.md) est un objet [**SWbemObject**](swbemobject.md) dont les propriétés définissent les paramètres d’entrée de cette méthode. Cette propriété est en lecture seule. Notez que les modifications apportées à cet objet ne sont pas reflétées dans la définition de méthode sous-jacente.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
SWbemMethod.InParameters As Object
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

Pour plus d’informations, consultez [construction d’objets inparamètres et analyse d’objets de paramètres de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethod<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemMethod<br/>                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemMethod**](swbemmethod.md)
</dt> <dt>

[**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md)
</dt> <dt>

[**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
</dt> <dt>

[**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
</dt> </dl>

 

 




