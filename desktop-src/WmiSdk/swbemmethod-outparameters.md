---
description: La propriété des paramètres de l’objet SWbemMethod est un objet SWbemObject dont les propriétés définissent les paramètres de sortie et le type de retour de cette méthode. Cette propriété est en lecture seule.
ms.assetid: ae7774f7-8a53-44e4-a110-2aef9ae4037f
ms.tgt_platform: multiple
title: Propriété SWbemMethod. commeters (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethod.OutParameters
- ISWbemMethod.OutParameters
- ISWbemMethod.get_OutParameters
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5dec1b2fe18dae65443b45ee6c1d2efcd1d924a72eb2817869c35406ebbc7808
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314411"
---
# <a name="swbemmethodoutparameters-property"></a>SWbemMethod. les paramètres de propriété

La propriété des **paramètres** de l’objet [**SWbemMethod**](swbemmethod.md) est un objet [**SWbemObject**](swbemobject.md) dont les propriétés définissent les paramètres de sortie et le type de retour de cette méthode. Cette propriété est en lecture seule.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
SWbemMethod.OutParameters As Object
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

Pour plus d’informations sur l’utilisation de cette propriété pour obtenir des paramètres de sortie à partir de méthodes de fournisseur, consultez [construction d’objets inparamètres et analyse d’objets de paramètres](constructing-inparameters-objects-and-parsing-outparameters-objects.md)de sortie. Notez que les modifications apportées à cet objet ne sont pas reflétées dans la définition de méthode sous-jacente.

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

 

 




