---
title: Méthode WSMan. EnumerationFlagNonXmlText (WSManDisp. h)
description: Retourne la valeur de la constante d’énumération WSManFlagNonXmlText à utiliser dans le paramètre flags de la méthode session. Enumerate.
ms.assetid: 5e062e73-f833-4090-ba5a-48ca374724e7
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode EnumerationFlagNonXmlText
- méthode EnumerationFlagNonXmlText Windows Remote Management, objet WSMan
- objet WSMan Windows Remote Management, méthode EnumerationFlagNonXmlText
topic_type:
- apiref
api_name:
- WSMan.EnumerationFlagNonXmlText
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6606a20d0ab7f59b7521367243ccdc97fd90209f1791d8f1ded3e48c70e3f59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742288"
---
# <a name="wsmanenumerationflagnonxmltext-method"></a>Méthode WSMan. EnumerationFlagNonXmlText

**WSMan. EnumerationFlagNonXmlText** retourne la valeur de la constante d’énumération **WSManFlagNonXmlText** pour une utilisation dans le paramètre *Flags* de la méthode [**session. Enumerate**](session-enumerate.md) . Cette méthode fournit une syntaxe plus efficace pour l’utilisation de la constante afin que les scripts ne soient pas requis pour définir une valeur de constante. Pour plus d’informations sur l’appel de cette méthode, consultez [sessions, constantes](session-constants.md).

**WSManFlagNonXmlText** est une constante dans l’énumération **\_ \_ WSManEnumFlags** . Pour plus d’informations, consultez [**énumération, constantes**](enumeration-constants.md).

## <a name="syntax"></a>Syntaxe


```VB
WSMan.EnumerationFlagNonXmlText( _
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

[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex)
</dt> <dt>

[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> </dl>

 

 





