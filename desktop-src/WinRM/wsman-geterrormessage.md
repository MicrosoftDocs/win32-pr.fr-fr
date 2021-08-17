---
title: Méthode WSMan. GetErrorMessage (WSManDisp. h)
description: Retourne une chaîne mise en forme qui contient le texte d’un numéro d’erreur.
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode GetErrorMessage
- méthode GetErrorMessage Windows Remote Management, objet WSMan
- objet WSMan Windows Remote Management, méthode GetErrorMessage
topic_type:
- apiref
api_name:
- WSMan.GetErrorMessage
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94e7f23a5d2678d3df024c78397aaeb6a388d8b75368f329867f6457b9ad4d84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742089"
---
# <a name="wsmangeterrormessage-method"></a>Méthode WSMan. GetErrorMessage

Retourne une chaîne mise en forme qui contient le texte d’un numéro d’erreur. Cette méthode effectue la même opération que le numéro d’erreur **de ligne de commande WinRM** **WinRM** *ou hexadécimal*.

## <a name="syntax"></a>Syntaxe


```VB
WSMan.GetErrorMessage( _
  ByVal errorNumber, _
  ByRef errorMessage _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*errornumber* \[ dans\]
</dt> <dd>

Numéro de message d’erreur au format décimal ou hexadécimal de WinRM, WinHTTP ou d’autres composants du système d’exploitation.

</dd> <dt>

*ErrorMessage* \[ à\]
</dt> <dd>

Chaîne de message d’erreur mise en forme comme les messages retournés par la commande **WinRM** .

</dd> </dl>

## <a name="remarks"></a>Remarques

La méthode C++ correspondante est [**IWSManEx :: GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).

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
</dt> </dl>

 

 





