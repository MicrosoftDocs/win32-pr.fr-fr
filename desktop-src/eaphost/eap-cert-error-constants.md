---
title: '\_Constantes d’erreur de certificat EAP (Eaphosterror. h)'
description: Définir des erreurs liées aux certificats communes à toutes les technologies d’API EAPHost.
ms.assetid: 12f626e1-520a-4aba-954b-769c3062a38c
topic_type:
- apiref
api_name:
- _EAP_CERT_FIRST
- _EAP_CERT_LAST
- _EAP_CERT_NOT_FOUND
- _EAP_CERT_INVALID
- _EAP_CERT_EXPIRED
- _EAP_CERT_REVOKED
- _EAP_CERT_OTHER_ERROR
- _EAP_CERT_REJECTED
- _EAP_CERT_NAME_REQUIRED
- _EAP_GENERAL_FIRST
- _EAP_GENERAL_LAST
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b373b3d28ce3c46cab92fa2a089e49e8158010681da3960e1cc4f0b58c4c2a8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984289"
---
# <a name="eap_cert-error-constants"></a>\_Constantes d’erreur de certificat EAP

Ces constantes définissent les erreurs liées aux certificats communes à toutes les technologies d’API EAPHost.

<dl> <dt>

<span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_certificat EAP en \_ \_ premier**
</dt> <dd> <dl> <dt>

0x0
</dt> <dt>



Définit la limite des rapports d’erreurs ; toutes les erreurs de certificat se produisent entre le certificat **\_ EAP en \_ \_ premier** et le **\_ \_ \_ dernier certificat EAP**.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_\_dernier certificat \_ EAP**
</dt> <dd> <dl> <dt>

0xF
</dt> <dt>



Définit la limite des rapports d’erreurs ; toutes les erreurs de certificat se produisent entre le certificat **\_ EAP en \_ \_ premier** et le **\_ \_ \_ dernier certificat EAP**.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_\_certificat EAP \_ \_ introuvable**
</dt> <dd> <dl> <dt>

0x1
</dt> <dt>



Aucun certificat utilisateur n’a été trouvé.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_\_certificat EAP \_ non valide**
</dt> <dd> <dl> <dt>

0x2
</dt> <dt>



Le certificat utilisateur n’est pas valide.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_\_certificat EAP \_ expiré**
</dt> <dd> <dl> <dt>

0x3
</dt> <dt>



Le certificat de l’utilisateur a expiré.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_\_certificat EAP \_ révoqué**
</dt> <dd> <dl> <dt>

0x4
</dt> <dt>



Le certificat utilisateur a été révoqué.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_\_ \_ autre erreur de certificat EAP \_**
</dt> <dd> <dl> <dt>

0x5
</dt> <dt>



Une erreur liée au certificat est inconnue.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_\_certificat EAP \_ rejeté**
</dt> <dd> <dl> <dt>

0x6
</dt> <dt>



Le certificat utilisateur a été rejeté.


</dt> </dl> </dd> <dt>

<span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_\_nom de certificat EAP \_ \_ requis**
</dt> <dd> <dl> <dt>

0x7
</dt> <dt>



Le certificat utilisateur requiert un nom.


</dt> </dl> </dd> <dt>

<span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_EAP- \_ général en \_ premier**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>



Définit la limite des rapports d’erreurs ; toute erreur générale EAP se produira entre **\_ EAP \_ général en \_ premier** et **\_ EAP \_ général en \_ dernier**.


</dt> </dl> </dd> <dt>

<span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_\_dernière général \_ EAP**
</dt> <dd> <dl> <dt>

0x3F
</dt> <dt>



Définit la limite des rapports d’erreurs ; toute erreur générale EAP se produira entre **\_ EAP \_ général en \_ premier** et **\_ EAP \_ général en \_ dernier**.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                      |
| En-tête<br/>                   | <dl> <dt>Eaphosterror. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes EAPHost communes](common-eap-host-error-constants.md)
</dt> </dl>

 

 





