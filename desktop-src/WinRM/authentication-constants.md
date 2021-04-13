---
title: Constantes d’authentification (WSManDisp. h)
description: Spécifiez la méthode d’authentification et la manière de gérer les serveurs de certificats pour le transport HTTPs des demandes.
ms.assetid: adfefbc9-c386-48db-a0c2-145aa4f91bfa
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagCredUsernamePassword
- WSManFlagSkipCACheck
- WSManFlagSkipCNCheck
- WSManFlagUseNoAuthentication
- WSManFlagUseDigest
- WSManFlagUseNegotiate
- WSManFlagUseBasic
- WSManFlagUseKerberos
- WSManFlagNoEncryption
- WSManFlagUseClientCertificate
- WSManFlagUseCredSsp
- WSManFlagSkipRevocationCheck
- WSManFlagAllowNegotiateImplicitCredentials
- WSManFlagUseSsl
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce45d1474cf6c925149c05ae348231333c3356e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509238"
---
# <a name="authentication-constants"></a>Constantes d’authentification

Les constantes d’authentification sont des constantes de l’énumération **\_ \_ WSManSessionFlags** qui spécifient la méthode d’authentification et comment gérer les serveurs de certificats pour le transport HTTPS des requêtes.

Une ou plusieurs des constantes répertoriées dans la liste suivante sont requises dans le paramètre *Flags* dans les appels à [**WSMan. CreateSession**](wsman-createsession.md) ou dans les appels [**IWSMan :: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) qui se connectent à un ordinateur distant.

<dl> <dt>

<span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**WSManFlagCredUsernamePassword**
</dt> <dd> <dl> <dt>

4096 (0x1000)
</dt> <dt>



Utilisez le nom d’utilisateur et le mot de passe comme informations d’identification. Définissez cet indicateur lorsque vous créez un objet [**ConnectionOptions**](connectionoptions.md) et fournissez le [**nom d’utilisateur**](connectionoptions-username.md) et le [**mot de passe**](connectionoptions-password.md). Les informations d’identification peuvent être un compte de domaine ou un compte sur l’ordinateur local. Par défaut, le compte doit être membre du groupe Administrateurs local sur l’ordinateur local ou distant. Toutefois, le service WinRM peut être configuré pour autoriser d’autres utilisateurs. Pour plus d’informations, consultez [installation et configuration de Windows Remote Management](installation-and-configuration-for-windows-remote-management.md). Vous pouvez définir cet indicateur lorsque vous spécifiez des informations d’identification pour l’authentification par négociation (également appelée [*authentification intégrée Windows*](windows-remote-management-glossary.md)) ou pour [*l’authentification de base*](windows-remote-management-glossary.md).

La méthode de script associée est [**WSMan. SessionFlagCredUsernamePassword**](wsman-sessionflagcredusernamepassword.md), et la méthode C++ est [**IWSManEx. SessionFlagCredUsernamePassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword).


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**WSManFlagSkipCACheck**
</dt> <dd> <dl> <dt>

8192 (0x2000)
</dt> <dt>



Lors de la connexion via HTTPs, le client ne valide pas que le certificat de serveur est signé par une autorité de certification approuvée. Utilisez cette valeur uniquement lorsque l’ordinateur distant est approuvé par d’autres moyens, par exemple, si l’ordinateur distant fait partie d’un réseau qui est physiquement sécurisé et isolé ou que l’ordinateur distant est listé comme un hôte approuvé dans la configuration WinRM.

La méthode de script associée est [**WSMan. SessionFlagSkipCACheck**](wsman-sessionflagskipcacheck.md), et la méthode C++ est [**IWSManEx. SessionFlagSkipCACheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**WSManFlagSkipCNCheck**
</dt> <dd> <dl> <dt>

16384 (0x4000)
</dt> <dt>



Lors de la connexion via HTTPs, le client ne valide pas que le nom commun (CN) dans le certificat de serveur correspond au nom de l’ordinateur dans la chaîne de connexion. À utiliser uniquement lorsque l’ordinateur distant est approuvé par d’autres moyens, par exemple, si l’ordinateur distant fait partie d’un réseau qui est physiquement sécurisé et isolé ou que l’ordinateur distant est listé comme un hôte approuvé dans la configuration WinRM.

La méthode de script associée est [**WSMan. SessionFlagSkipCNCheck**](wsman-sessionflagskipcncheck.md), et la méthode C++ est [**IWSManEx. SessionFlagSkipCNCheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**WSManFlagUseNoAuthentication**
</dt> <dd> <dl> <dt>

32768 (0x8000)
</dt> <dt>



N’utilisez aucune authentification. Spécifiez cette constante lors du test d’une connexion à un ordinateur distant pour déterminer si un service qui implémente le protocole WS-Management est configuré pour écouter les demandes de données. **WSManFlagUseNoAuthentication** ne peut pas être associé à une autre constante de [**session**](session.md) . La méthode de script associée est [**WSMan. SessionFlagUseNoAuthentication**](wsman-sessionflagusenoauthentication.md), et la méthode C++ est [**WSManEx. SessionFlagUseNoAuthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**WSManFlagUseDigest**
</dt> <dd> <dl> <dt>

65536 (0x10000)
</dt> <dt>



Utilisez l’authentification Digest. Seul l'ordinateur client peut initier une demande d'authentification Digest. Le client envoie une demande au serveur pour s’authentifier et reçoit une chaîne de jeton du serveur. Le client envoie ensuite la demande de ressource, y compris le nom d’utilisateur et un hachage de chiffrement du mot de passe associé à la chaîne de jeton. L’authentification Digest est prise en charge pour HTTP et HTTPs. Les applications et scripts clients WinRM peuvent spécifier l’authentification Digest, mais pas le service.

La méthode de script associée est [**WSMan. SessionFlagUseDigest**](wsman-sessionflagusedigest.md), et la méthode C++ est [**IWSManEx. SessionFlagUseDigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**WSManFlagUseNegotiate**
</dt> <dd> <dl> <dt>

131072 (0x20000)
</dt> <dt>



Utilisez l’authentification par négociation. Le client envoie une demande au serveur pour s’authentifier. Le serveur détermine s’il faut utiliser Kerberos ou NTLM. Kerberos est sélectionné pour authentifier un compte de domaine et NTLM est sélectionné pour les comptes d’ordinateur local. Le nom d’utilisateur doit être spécifié sous la forme domaine \\ nom d’utilisateur pour un utilisateur de domaine ou un \\ nom d’utilisateur ServerName pour un utilisateur local sur un ordinateur serveur.

Le [contrôle de compte d’utilisateur (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) affecte l’accès au service WinRM. Lorsque l’authentification par négociation est utilisée dans un groupe de travail ou un domaine, seul le compte administrateur intégré peut accéder au service. Pour autoriser tous les comptes du groupe administrateurs à accéder au service, définissez la clé de Registre suivante sur 1 : **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Policies \\ System \\ LocalAccountTokenFilterPolicy**.

La méthode de script associée est [**WSMan. SessionFlagUseNegotiate**](wsman-sessionflagusenegotiate.md), et la méthode C++ est [**IWSManEx. SessionFlagUseNegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**WSManFlagUseBasic**
</dt> <dd> <dl> <dt>

262144 (0x40000)
</dt> <dt>



Utilisez l’authentification de base. Le client présente les informations d’identification sous la forme d’un nom d’utilisateur et d’un mot de passe, transmises directement dans le message de demande. Vous pouvez spécifier uniquement les informations d’identification qui identifient un compte d’administrateur local sur l’ordinateur distant.

La méthode de script associée est [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md), et la méthode C++ est [**IWSManEx. SessionFlagUseBasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**WSManFlagUseKerberos**
</dt> <dd> <dl> <dt>

524288 (0x80000)
</dt> <dt>



Utilisez l'authentification Kerberos. Le client et le serveur s’authentifient mutuellement à l’aide des tickets Kerberos.

La méthode de script associée est [**WSMan. SessionFlagUseKerberos**](wsman-sessionflagusekerberos.md), et la méthode C++ est [**IWSManEx. WSMan. SessionFlagUseKerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**
</dt> <dd> <dl> <dt>

1048576 ()
</dt> <dt>



N’utilisez pas de chiffrement. Le trafic non chiffré n’est pas autorisé par défaut et doit être activé à la fois sur le client et sur le serveur.

La méthode de script associée est [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md), et la méthode C++ est [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**WSManFlagUseClientCertificate**
</dt> <dd> <dl> <dt>

2097152 (0x200000)
</dt> <dt>



Utilisez l’authentification par certificat client.

La méthode de script associée est [**WSMan. SessionFlagUseClientCertificate**](wsman-sessionflaguseclientcert.md), et la méthode C++ est [**IWSManEx2. SessionFlagUseClientCertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**WSManFlagUseCredSsp**
</dt> <dd> <dl> <dt>

16777216 (0x1000000)
</dt> <dt>



Utilisez l’authentification CredSSP (Credential Security Support Provider).

La méthode de script associée est [**WSMan. SessionFlagUseCredSsp**](wsman-sessionflagusecredssp.md), et la méthode C++ est [**IWSManEx3. SessionFlagUseCredSsp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**WSManFlagSkipRevocationCheck**
</dt> <dd> <dl> <dt>

0x2000000
</dt> <dt>



Ne pas vérifier la révocation des certificats lors de l’authentification.


</dt> </dl> </dd> <dt>

<span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**WSManFlagAllowNegotiateImplicitCredentials**
</dt> <dd> <dl> <dt>

0x4000000
</dt> <dt>



Autorisez les informations d’identification implicites.


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**WSManFlagUseSsl**
</dt> <dd> <dl> <dt>

0x8000000
</dt> <dt>



Utilisez SSL (Secure Socket Layer) pour activer le protocole HTTPs.


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

 

 





