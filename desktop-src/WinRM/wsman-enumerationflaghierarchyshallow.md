---
title: Méthode WSMan. EnumerationFlagHierarchyShallow (WSManDisp. h)
description: Retourne la valeur de l’indicateur d’énumération EnumerationFlagHierarchyShallow à utiliser dans le paramètre flags de session. Enumerate.
ms.assetid: 18b564e6-dda1-44b9-b445-26c6183b6af9
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode EnumerationFlagHierarchyShallow
- Méthode EnumerationFlagHierarchyShallow Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode EnumerationFlagHierarchyShallow
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagHierarchyShallow
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46b74552fd88ac370ad4a3f8b885a7f61e65a053
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508817"
---
# <a name="wsmanenumerationflaghierarchyshallow-method"></a>Méthode WSMan. EnumerationFlagHierarchyShallow

La méthode **EnumerationFlagHierarchyShallow** retourne la valeur de l’indicateur d’énumération **EnumerationFlagHierarchyShallow** pour une utilisation dans le paramètre *Flags* de [**session. Enumerate**](session-enumerate.md). Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante. Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).

**EnumerationFlagHierarchyShallow** est une constante dans l’énumération **\_ WSManEnumFlags** et est décrite dans [**constantes d’énumération**](enumeration-constants.md).

## <a name="syntax"></a>Syntaxe


```VB
WSMan.EnumerationFlagHierarchyShallow( _
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

 

 





