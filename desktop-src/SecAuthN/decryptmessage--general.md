---
description: Déchiffre un message.
ms.assetid: ea271d0c-9167-41c5-8919-09611206fc71
title: DecryptMessage (général), fonction (SSPI. h)
ms.topic: reference
ms.date: 07/25/2019
ms.openlocfilehash: a05906c721d9046920c465fdfdf6b1c790b06640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201660"
---
# <a name="decryptmessage-general-function"></a>DecryptMessage (général) (fonction)

La fonction **DecryptMessage (général)** déchiffre un message. Certains packages ne chiffrent et ne déchiffrent pas les messages, mais effectuent et vérifient plutôt un [*hachage*](../secgloss/h-gly.md)d’intégrité.

Le fournisseur SSP ( [*Security Support Provider*](../secgloss/s-gly.md) ) de Digest fournit la confidentialité de chiffrement et de déchiffrement pour les messages échangés entre le client et le serveur en tant que mécanisme SASL uniquement.

Cette fonction est également utilisée avec le SSP Schannel pour signaler une demande de la part d’un expéditeur de message pour une renégociation (rétablissement) des attributs de connexion ou pour l’arrêt de la connexion.

> [!Note]  
> [**EncryptMessage (General)**](encryptmessage--general.md) et **DecryptMessage (General)** peuvent être appelés en même temps à partir de deux threads différents dans un contexte SSPI ( [*Security Support Provider Interface*](../secgloss/s-gly.md) ) unique si un thread est en cours de chiffrement et que l’autre déchiffre. Si plusieurs threads chiffrent, ou si plusieurs threads déchiffrent, chaque thread doit obtenir un contexte unique.

 

Pour plus d’informations sur l’utilisation de cette fonction avec un fournisseur de services partagés spécifique, consultez les rubriques suivantes.



| Rubrique                                                            | Description                            |
|------------------------------------------------------------------|----------------------------------------|
| [**DecryptMessage (Digest)**](decryptmessage--digest.md)       | Déchiffre un message à l’aide de Digest.    |
| [**DecryptMessage (Kerberos)**](decryptmessage--kerberos.md)   | Déchiffre un message à l’aide de Kerberos.  |
| [**DecryptMessage (Negotiate)**](decryptmessage--negotiate.md) | Déchiffre un message à l’aide de Negotiate. |
| [**DecryptMessage (NTLM)**](decryptmessage--ntlm.md)           | Déchiffre un message à l’aide de NTLM.      |
| [**DecryptMessage (SChannel)**](decryptmessage--schannel.md)   | Déchiffre un message à l’aide de Schannel.  |



 

## <a name="syntax"></a>Syntaxe


```C++
SECURITY_STATUS SEC_Entry DecryptMessage(
  _In_    PCtxtHandle    phContext,
  _Inout_ PSecBufferDesc pMessage,
  _In_    ULONG          MessageSeqNo,
  _Out_   PULONG         pfQOP
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*phContext* \[ dans\]
</dt> <dd>

Handle du contexte de [*sécurité*](../secgloss/s-gly.md) à utiliser pour déchiffrer le message.

</dd> <dt>

*pMessage* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc) . En entrée, la structure fait référence à une ou plusieurs structures [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . L’une d’entre elles peut être de type SECBUFFER \_ Data. Cette mémoire tampon contient le message chiffré. Le message chiffré est déchiffré sur place, remplaçant le contenu d’origine de sa mémoire tampon.

Lors de l’utilisation du SSP Digest, en entrée, la structure fait référence à une ou plusieurs structures [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . L’un d’eux doit être de type SECBUFFER \_ Data ou SECBUFFER \_ Stream, et il doit contenir le message chiffré.

Lorsque vous utilisez le SSP Schannel avec des contextes qui ne sont pas orientés connexion, la structure doit contenir quatre structures [**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer) . Une seule mémoire tampon doit être de type SECBUFFER \_ Data et contenir un message chiffré, qui est déchiffré sur place. Les mémoires tampons restantes sont utilisées pour la sortie et doivent être de type SECBUFFER \_ vide. Pour les contextes orientés connexion, un \_ tampon de type de données SECBUFFER doit être fourni, comme indiqué pour les contextes non orientés connexion. En outre, un deuxième tampon de type de jeton SECBUFFER contenant \_ un jeton de sécurité doit également être fourni.

</dd> <dt>

*MessageSeqNo* \[ dans\]
</dt> <dd>

Numéro de séquence attendu par l’application de transport, le cas échéant. Si l’application de transport ne conserve pas les numéros séquentiels, ce paramètre doit avoir la valeur zéro.

Lorsque vous utilisez le SSP Digest, ce paramètre doit avoir la valeur zéro. Le SSP Digest gère la numérotation des séquences en interne.

Lorsque vous utilisez le SSP Schannel, ce paramètre doit avoir la valeur zéro. Le SSP Schannel n’utilise pas de numéros de séquence.

</dd> <dt>

*pfQOP* \[ à\]
</dt> <dd>

Pointeur vers une variable de type **ULong** qui reçoit des indicateurs spécifiques au package qui indiquent la qualité de la protection.

Lorsque vous utilisez le SSP Schannel, ce paramètre n’est pas utilisé et doit avoir la valeur **null**.

Ce paramètre peut être l’un des indicateurs suivants.



<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th>Valeur</th><th>Signification</th></tr></thead><tbody><tr class="odd"><td><span id="SECQOP_WRAP_NO_ENCRYPT"></span><span id="secqop_wrap_no_encrypt"></span><dl> <dt><strong>SECQOP_WRAP_NO_ENCRYPT</strong></dt> </dl></td><td>Le message n’a pas été chiffré, mais un en-tête ou un code de fin a été créé.<br/><blockquote>[!Note]<br />
KERB_WRAP_NO_ENCRYPT a la même valeur et la même signification.</blockquote><br/></td></tr><tr class="even"><td><span id="SIGN_ONLY_"></span><span id="sign_only_"></span><dl> <dt><strong>SIGN_ONLY</strong></dt> </dl></td><td>Lorsque vous utilisez le SSP Digest, utilisez cet indicateur lorsque le [*contexte de sécurité*](../secgloss/s-gly.md) est défini pour vérifier la [*signature*](../secgloss/s-gly.md) uniquement. Pour plus d’informations, consultez [Quality of protection](quality-of-protection.md).<br/></td></tr></tbody></table>



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction vérifie que le message a été reçu dans l’ordre correct, la fonction retourne SEC \_ E \_ OK.

Si la fonction ne parvient pas à déchiffrer le message, elle retourne l’un des codes d’erreur suivants.



| Code de retour                                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_tampon s \_ E \_ trop \_ petit**</dt> </dl>      | La mémoire tampon des messages est trop petite. Utilisé avec le SSP Digest.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**SEC \_ E \_ système de chiffrement \_ \_ non valide**</dt> </dl> | Le [*chiffrement*](../secgloss/c-gly.md) choisi pour le [*contexte de sécurité*](../secgloss/s-gly.md) n’est pas pris en charge. Utilisé avec le SSP Digest.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**s \_ E \_ message incomplet \_**</dt> </dl>     | Les données de la mémoire tampon d’entrée sont incomplètes. L’application doit lire plus de données à partir du serveur et appeler [**DecryptMessage (général)**](decryptmessage--general.md) .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**SEC \_ E \_ handle non valide \_**</dt> </dl>         | Un descripteur de contexte non valide a été spécifié dans le paramètre *phContext* . Utilisé avec les SSP condensé et Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <dt>**s \_ E \_ jeton non valide \_**</dt> </dl>          | Les mémoires tampons sont de type incorrect ou aucune mémoire tampon de type SECBUFFER \_ Data n’a été trouvée. Utilisé avec le SSP Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <dt>**s \_ \_ message électronique \_ modifié**</dt> </dl>        | Le message a été modifié. Utilisé avec les SSP condensé et Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ hors \_ \_ séquence**</dt> </dl>       | Le message n’a pas été reçu dans l’ordre correct.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**SEC \_ E \_ QoP \_ non \_ pris en charge**</dt> </dl>     | La confidentialité et l' [*intégrité*](../secgloss/i-gly.md) ne sont pas prises en charge par le [*contexte de sécurité*](../secgloss/s-gly.md). Utilisé avec le SSP Digest.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <dt>**le \_ contexte sec I \_ \_ a expiré**</dt> </dl>        | L’expéditeur du message a fini d’utiliser la connexion et a lancé un arrêt. Pour plus d’informations sur l’initialisation ou la reconnaissance d’un arrêt, consultez [arrêt d’une connexion Schannel](shutting-down-an-schannel-connection.md). Utilisé avec le SSP Schannel.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <dl> <dt>**s \_ je \_ renégocie**</dt> </dl>             | Le tiers distant requiert une nouvelle séquence de négociation ou l’application vient d’initier un arrêt. Revenez à la boucle de négociation et appelez [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) ou [**InitializeSecurityContext (General)**](initializesecuritycontext--general.md), en passant des mémoires tampons d’entrée vides. <br/> Si la fonction retourne une mémoire tampon de type **sec \_ buffer \_ extra**, elle doit être transmise à la fonction [**AcceptSecurityContext (General)**](acceptsecuritycontext--general.md) comme une mémoire tampon d’entrée.<br/> Utilisé avec le SSP Schannel.<br/> La renégociation n’est pas prise en charge pour le mode noyau Schannel. L’appelant doit soit ignorer cette valeur de retour, soit arrêter la connexion. Si la valeur est ignorée, le client ou le serveur peut arrêter la connexion en conséquence.<br/> |



 

## <a name="remarks"></a>Notes

Lorsque vous utilisez le SSP Schannel, la fonction **DecryptMessage (General)** retourne le \_ contexte sec I \_ \_ expiré lorsque l’expéditeur du message a arrêté la connexion. Pour plus d’informations sur l’initialisation ou la reconnaissance d’un arrêt, consultez [arrêt d’une connexion Schannel](shutting-down-an-schannel-connection.md).

Lorsque vous utilisez le SSP Schannel, **DecryptMessage (General)** retourne sec \_ I \_ renégociée lorsque l’expéditeur du message souhaite renégocier la connexion ([*contexte de sécurité*](../secgloss/s-gly.md)). Une application gère une renégociation demandée en appelant [**AcceptSecurityContext (général)**](acceptsecuritycontext--general.md) (côté serveur) ou [**InitializeSecurityContext (général)**](initializesecuritycontext--general.md) (côté client) et en passant dans des mémoires tampons d’entrée vides. Après que cet appel initial a retourné une valeur, procédez comme si votre application était en train de créer une nouvelle connexion. Pour plus d’informations, consultez [création d’un [*contexte de sécurité*](../secgloss/s-gly.md)Schannel](creating-an-schannel-security-context.md).

Pour plus d’informations sur l’interopérabilité avec GSSAPI, consultez [interopérabilité SSPI/Kerberos avec GSSAPI](sspi-kerberos-interoperability-with-gssapi.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>SSPI. h (include Security. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Secur32. lib</dt> </dl>                 |
| DLL<br/>                      | <dl> <dt>Secur32.dll</dt> </dl>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions SSPI](authentication-functions.md#sspi-functions)
</dt> <dt>

[**EncryptMessage (général)**](encryptmessage--general.md)
</dt> <dt>

[**SecBuffer**](/windows/win32/api/sspi/ns-sspi-secbuffer)
</dt> <dt>

[**SecBufferDesc**](/windows/win32/api/sspi/ns-sspi-secbufferdesc)
</dt> </dl>

 

 
