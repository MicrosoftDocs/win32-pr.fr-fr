---
title: Méthode WSMan. EnumerationFlagReturnObjectAndEPR (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’énumération EnumerationFlagReturnObjectAndEPR à utiliser dans le paramètre flags de session. Enumerate.
ms.assetid: 052b93df-8a83-4b5e-8325-1ad500b43a88
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode EnumerationFlagReturnObjectAndEPR
- Méthode EnumerationFlagReturnObjectAndEPR Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode EnumerationFlagReturnObjectAndEPR
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagReturnObjectAndEPR
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187f8c029d0392ad9ac1a909e1e45de165815e2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466602"
---
# <a name="wsmanenumerationflagreturnobjectandepr-method"></a>Méthode WSMan. EnumerationFlagReturnObjectAndEPR

La méthode **EnumerationFlagReturnObjectAndEPR** retourne la valeur de l’indicateur d’énumération **EnumerationFlagReturnObjectAndEPR** pour une utilisation dans le paramètre *Flags* de [**session. Enumerate**](session-enumerate.md). Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante. Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).

**EnumerationFlagReturnObjectAndEPR** est une constante dans l’énumération **\_ WSManEnumFlags** et est décrite dans [**constantes d’énumération**](enumeration-constants.md).

## <a name="syntax"></a>Syntaxe


```VB
WSMan.EnumerationFlagReturnObjectAndEPR( _
  ByRef flags _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*indicateurs* \[ à\]
</dt> <dd>

Valeur de la constante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WSMan**](wsman.md)
</dt> <dt>

[**session**](session.md)
</dt> </dl>

 

 





