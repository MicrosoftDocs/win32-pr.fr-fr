---
title: Méthode WSMan. GetErrorMessage (WSManDisp. h)
description: Retourne une chaîne mise en forme qui contient le texte d’un numéro d’erreur.
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode GetErrorMessage
- Méthode GetErrorMessage Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode GetErrorMessage
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
ms.openlocfilehash: 3d085e6f19c64f609fe1389a2822df1594ee69bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317254"
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

## <a name="remarks"></a>Notes

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

 

 





