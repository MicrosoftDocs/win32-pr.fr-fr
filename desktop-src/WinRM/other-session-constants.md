---
title: Autres constantes de session (WSManDisp. h)
description: Spécifiez l’encodage, le chiffrement et le port du nom de principal du service.
ms.assetid: a921b7bc-1f40-427c-971f-c0bc9c9f6887
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagUTF8
- WSManFlagNoEncryption
- WSManFlagEnableSPNServerPort
- WSManFlagUTF16
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcd9d2cf44063dfb1a7ec1bfcbb0fe785d1747d34e84ef2c2d8c78598e6e6b0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743324"
---
# <a name="other-session-constants"></a>Autres constantes de session

Les constantes, répertoriées dans la liste suivante, dans l’énumération **\_ \_ WSManSessionFlags** qui spécifient l’encodage, le chiffrement et le port du nom de principal du service.

<dl> <dt>

<span id="WSManFlagUTF8"></span><span id="wsmanflagutf8"></span><span id="WSMANFLAGUTF8"></span>**WSManFlagUTF8**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Envoie la demande en UTF8 plutôt qu’en UTF16.

La méthode de script associée est [**WSMan. SessionFlagUTF8**](wsman-sessionflagutf8.md) et la méthode C++ est [**IWSManEx. SessionFlagUTF8**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagutf8).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**
</dt> <dd> <dl> <dt>

1048576 ()
</dt> <dt>



Ne chiffrez pas les messages envoyés sur le réseau. Ce paramètre est autorisé uniquement si l' [*écouteur*](windows-remote-management-glossary.md) est configuré de sorte que **AllowUnencrypted** ait la valeur **true**.

La méthode de script associée est [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md) et la méthode C++ est [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).


</dt> </dl> </dd> <dt>

<span id="WSManFlagEnableSPNServerPort"></span><span id="wsmanflagenablespnserverport"></span><span id="WSMANFLAGENABLESPNSERVERPORT"></span>**WSManFlagEnableSPNServerPort**
</dt> <dd> <dl> <dt>

4194304 (0x400000)
</dt> <dt>



Spécifiez le port du nom de principal du service (SPN) lors de la connexion directe au matériel BMC distant, également appelé connexion [*hors bande*](windows-remote-management-glossary.md) . Étant donné que l’ordinateur serveur WinRM et le matériel BMC peuvent partager la même adresse IP, cet indicateur indique que le numéro de port SPN doit être utilisé pour déterminer si la connexion concerne le service ou directement au contrôleur BMC. Pour plus d’informations, consultez [formats de noms pour les noms de principal du service uniques](/windows/desktop/AD/name-formats-for-unique-spns).

La méthode de script associée est [**WSMan. SessionFlagEnableSPNServerPort**](wsman-sessionflagenablespnserverport.md) et la méthode C++ est [**IWSManEx. SessionFlagEnableSPNServerPort**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagenablespnserverport).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUTF16"></span><span id="wsmanflagutf16"></span><span id="WSMANFLAGUTF16"></span>**WSManFlagUTF16**
</dt> <dd> <dl> <dt>

0x800000
</dt> <dt>



Envoie la requête dans UTF16.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes de session](session-constants.md)
</dt> </dl>

 

