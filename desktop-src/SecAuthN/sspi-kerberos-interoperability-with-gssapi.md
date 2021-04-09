---
description: Une attention particulière doit être prise en compte lors de l’utilisation du fournisseur SSP (Security Support Provider) Kerberos si l’interopérabilité avec GSSAPI est requise.
ms.assetid: 3ab29ee9-42d8-498b-b507-13f8efa0b0e2
title: Interopérabilité SSPI/Kerberos avec GSSAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9efaae6b2433d76dff290d57e27e893885692a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749597"
---
# <a name="sspikerberos-interoperability-with-gssapi"></a>Interopérabilité SSPI/Kerberos avec GSSAPI

Une attention particulière doit être prise en compte lors de l’utilisation du fournisseur SSP ( [*Security Support Provider*](../secgloss/s-gly.md) ) [*Kerberos*](../secgloss/k-gly.md) si l’interopérabilité avec GSSAPI est requise. Les conventions de code suivantes permettent l’interopérabilité avec des applications basées sur GSSAPI :

-   [Noms compatibles Windows](#windows-compatible-names)
-   [Authentification](#authentication)
-   [Intégrité et confidentialité des messages](#message-integrity-and-privacy)

Vous trouverez des exemples de code dans le kit de développement logiciel (SDK) de la plateforme sous exemples de \\ sécurité \\ SSPI \\ GSS. En outre, l’exemple UNIX équivalent est distribué dans les distributions Kerberos MIT et heimdal, client et serveur GSS.

## <a name="windows-compatible-names"></a>Noms de Windows-Compatible

Les fonctions GSSAPI utilisent un format de nom connu \_ sous \_ le nom de service GSS NT \_ , tel que spécifié dans la RFC. Par exemple, sample@host.dom.com est un nom qui peut être utilisé dans une application GSSAPI. Le système d’exploitation Windows ne reconnaît pas le \_ format de nom de service GSS NT \_ \_ , et le [*nom de principal du service*](../secgloss/s-gly.md)complet, par exemple sample/host.dom.com@REALM , doit être utilisé.

## <a name="authentication"></a>Authentification

L’authentification est généralement gérée lorsqu’une connexion est configurée pour la première fois entre un client et un serveur. Dans cet exemple, le client utilise l' [*interface SSPI (Security Support Provider Interface*](../secgloss/s-gly.md) ) et le serveur utilise GSSAPI.

**Pour configurer l’authentification dans le client SSPI**

1.  Accédez aux [*informations d’identification*](../secgloss/c-gly.md) sortantes à l’aide de [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).
2.  Créez un nom de service avec **GSS \_ import \_ Name ()** et obtenez les informations d’identification entrantes à l’aide de **GSS \_ Acquire \_ cred**.
3.  Obtient un jeton d’authentification à envoyer au serveur à l’aide de [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).
4.  Envoyez le jeton au serveur.

**Pour configurer l’authentification dans le serveur GSSAPI**

1.  Analyser le message du client pour extraire le jeton de sécurité. Utilisez la fonction de **\_ \_ \_ contexte GSS Accept sec** , en passant le jeton en tant qu’argument.
2.  Analysez le message à partir du serveur pour extraire le jeton de sécurité. Transmettez ce jeton de sécurité à [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).
3.  Envoyer un jeton de réponse au client.

    La fonction de **\_ \_ \_ contexte GSS Accept sec** peut retourner un jeton que vous pouvez renvoyer au client.

4.  S’il est nécessaire de continuer, envoyez un jeton de réponse au serveur. dans le cas contraire, la configuration de l’authentification est terminée.
5.  S’il est nécessaire de continuer, attendez le jeton suivant du client. dans le cas contraire, la configuration de l’authentification est terminée.

## <a name="message-integrity-and-privacy"></a>Intégrité et confidentialité des messages

La plupart des applications basées sur GSSAPI utilisent la fonction **GSS \_ Wrap** pour signer un message avant de l’envoyer. À l’inverse, la fonction de **\_ désencapsulage GSS** vérifie la signature. **GSS \_ Wrap** est disponible dans la version 2,0 de l’API et est désormais largement utilisé et spécifié dans les normes Internet qui décrivent l’utilisation de GSSAPI pour l’ajout de la sécurité aux protocoles. Précédemment, les fonctions GSS **SignMessage** et **SealMessage** étaient utilisées pour [*l’intégrité*](../secgloss/i-gly.md) et la [*confidentialité*](../secgloss/p-gly.md)des messages. **GSS \_ Wrap** et **GSS \_ Unwrap** sont utilisés à des fins d’intégrité et de confidentialité avec l’utilisation de la confidentialité contrôlée par la valeur de l’argument « conf \_ Flag ».

Si un protocole GSSAPI est spécifié pour utiliser les fonctions **GSS \_ obtenir \_ MIC** et **GSS \_ verify \_** , les fonctions SSPI appropriées sont [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) et [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature). Sachez que **MakeSignature** et **VerifySignature** n’interagissent pas avec **GSS \_ Wrap** lorsque l' \_ indicateur conf est défini sur zéro ou avec **GSS \_ Wrap**. Il en va de même pour mélanger [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) pour la signature uniquement et le **\_ \_ MIC Verify**.

> [!Note]  
> N’utilisez pas les fonctions [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) ou [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) lorsque les fonctions **GSS \_ Wrap** et **GSS \_ Unwrap** sont appelées pour.

 

L’équivalent SSPI de **GSS \_ Wrap** est [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) pour l’intégrité et la confidentialité.

L’exemple suivant illustre l’utilisation de [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) pour signer les données qui seront vérifiées par le déchiffrement **GSS \_**.

Dans le client SSPI :


```C++
// Need three descriptors, two for the SSP and
// one to hold the application data. 
in_buf_desc.cBuffers = 3;
in_buf_desc.pBuffers = wrap_bufs;
in_buf_desc.ulVersion = SECBUFFER_VERSION;
wrap_bufs[0].cbBuffer = sizes.cbSecurityTrailer;
wrap_bufs[0].BufferType = SECBUFFER_TOKEN;
wrap_bufs[0].pvBuffer = malloc(sizes.cbSecurityTrailer);

// This buffer holds the application data.
wrap_bufs[1].BufferType = SECBUFFER_DATA;
wrap_bufs[1].cbBuffer = in_buf.cbBuffer;
wrap_bufs[1].pvBuffer = malloc(wrap_bufs[1].cbBuffer);
memcpy(wrap_bufs[1].pvBuffer, in_buf.pvBuffer, in_buf.cbBuffer);
wrap_bufs[2].BufferType = SECBUFFER_PADDING;
wrap_bufs[2].cbBuffer = sizes.cbBlockSize;
wrap_bufs[2].pvBuffer = malloc(wrap_bufs[2].cbBuffer);
maj_stat = EncryptMessage(&context,
SignOnly ? KERB_WRAP_NO_ENCRYPT : 0,
&in_buf_desc, 0);

// Send a message to the server.
```



Dans le serveur GSSAPI :


```C++
// Received message is in recv_buf. 
maj_stat = gss_unwrap(&min_stat, context, &recv_buf, &msg_buf,
    &conf_state, (gss_qop_t *) NULL);
(void) gss_release_buffer(&min_stat, &recv_buf);

// Original message is in msg_buf.
```



L’équivalent SSPI de **GSS \_ Unwrap** est [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage). Voici un exemple qui montre comment utiliser **DecryptMessage (Kerberos)** pour déchiffrer les données qui ont été chiffrées par le protocole **GSS \_ Wrap**.

Dans le serveur GSSAPI :


```C++
// Seal the message.
send_buf.value = msg;
send_buf.length = msglen;

// If encrypt_flag = 1, privacy; encrypt_flag = 0, integrity.
maj_stat = gss_wrap(&min_stat, context, encrypt_flag,
    GSS_C_QOP_DEFAULT, &send_buf, &state, &msg_buf); 

// The message to send is in msg_buf.
```



Dans le client SSPI :


```C++
wrap_buf_desc.cBuffers = 2;
wrap_buf_desc.pBuffers = wrap_bufs;
wrap_buf_desc.ulVersion = SECBUFFER_VERSION; 

// This buffer is for SSPI.
wrap_bufs[0].BufferType = SECBUFFER_STREAM;
wrap_bufs[0].pvBuffer = xmit_buf.pvBuffer;
wrap_bufs[0].cbBuffer = xmit_buf.cbBuffer;

// This buffer holds the application data.
wrap_bufs[1].BufferType = SECBUFFER_DATA;
wrap_bufs[1].cbBuffer = 0;
wrap_bufs[1].pvBuffer = NULL;
maj_stat = DecryptMessage(
&context,
&wrap_buf_desc,
0, // no sequence number
&qop
);

// This is where the data is.
msg_buf = wrap_bufs[1];

// Check QOP of received message.
// If QOP is KERB_WRAP_NO_ENCRYPT, the message is signed only; 
// otherwise, it is encrypted.
```



 

 
