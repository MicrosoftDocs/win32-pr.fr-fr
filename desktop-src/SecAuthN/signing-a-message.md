---
description: Quand un client et un serveur terminent la configuration du contexte de sécurité, les fonctions de prise en charge des messages peuvent être utilisées.
ms.assetid: a65054bd-31cb-4842-af59-82cfe799fb70
title: Signature d’un message
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36f8151a66120575bfcaeda62955a7f6aa47e8e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521113"
---
# <a name="signing-a-message"></a>Signature d’un message

Quand un client et un serveur terminent la configuration du [*contexte de sécurité*](../secgloss/s-gly.md), les fonctions de prise en charge des messages peuvent être utilisées. Le client et le serveur utilisent le jeton de contexte de sécurité créé lors de l’établissement de la session pour appeler les fonctions [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) et [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) . Le jeton de contexte peut être utilisé avec [**EncryptMessage (général)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) et [**DecryptMessage (général)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) pour la [*confidentialité*](../secgloss/p-gly.md)des communications.

L’exemple suivant montre le côté client qui génère un message signé à envoyer au serveur. Avant d’appeler [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), le client appelle [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) avec une structure de [**\_ tailles SecPkgContext**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes) pour déterminer la longueur de la mémoire tampon nécessaire pour contenir la signature du message. Si le membre **cbMaxSignature** est égal à zéro, le [*package de sécurité*](../secgloss/s-gly.md) ne prend pas en charge la signature des messages. Dans le cas contraire, ce membre indique la taille de la mémoire tampon à allouer pour recevoir la signature.

L’exemple suppose qu’une variable **SecHandle** nommée *phContext* et une structure de **Socket** nommée *s* sont initialisées. Pour les déclarations et les initiations de ces variables, consultez [utilisation de SSPI avec un client Windows Sockets](using-sspi-with-a-windows-sockets-client.md) et [utilisation de SSPI avec un serveur Windows Sockets](using-sspi-with-a-windows-sockets-server.md). Cet exemple inclut des appels aux fonctions dans secur32. lib, qui doivent être inclus dans les bibliothèques de liens.


```C++
//--------------------------------------------------------------------
//   Declare and initialize local variables.

SecPkgContext_Sizes ContextSizes;
char *MessageBuffer = "This is a sample buffer to be signed.";
DWORD MessageBufferSize = strlen(MessageBuffer);
SecBufferDesc InputBufferDescriptor;
SecBuffer InputSecurityToken[2];

ss = QueryContextAttributes(
    &phContext,
    SECPKG_ATTR_SIZES,
    &ContextSizes
    );
if(ContextSizes.cbMaxSignature == 0)
{
     MyHandleError("This session does not support message signing.");
}
//--------------------------------------------------------------------
// The message as a byte string is in the variable 
// MessageBuffer, and its length is in MessageBufferSize. 

//--------------------------------------------------------------------
// Build the buffer descriptor and the buffers 
// to pass to the MakeSignature call.

InputBufferDescriptor.cBuffers = 2;
InputBufferDescriptor.pBuffers = InputSecurityToken;
InputBufferDescriptor.ulVersion = SECBUFFER_VERSION;

//--------------------------------------------------------------------
// Build a security buffer for the message itself. If 
// the SECBUFFER_READONLY attribute is set, the buffer will not be
// signed.

InputSecurityToken[0].BufferType = SECBUFFER_DATA;
InputSecurityToken[0].cbBuffer = MessageBufferSize;
InputSecurityToken[0].pvBuffer = MessageBuffer;

//--------------------------------------------------------------------
// Allocate and build a security buffer for the message
// signature.

InputSecurityToken[1].BufferType = SECBUFFER_TOKEN;
InputSecurityToken[1].cbBuffer = ContextSizes.cbMaxSignature;
InputSecurityToken[1].pvBuffer = 
        (void *)malloc(ContextSizes.cbMaxSignature);

//--------------------------------------------------------------------
// Call MakeSignature 
// For the NTLM package, the sequence number need not be specified 
// because the package provides sequencing.
// The quality of service parameter is ignored.

Ss = MakeSignature(
    &phContext,
    0,                       // no quality of service
    &InputBufferDescriptor,  // input message descriptor
    0                        // no sequence number
    );
if (SEC_SUCCESS(ss))
{
     printf("Have made a signature.\n");
}
else
{ 
    MyHandleError("MakeSignature Failed."); 
}

//--------------------------------------------------------------------
//  Send the message.

if(!SendMsg(
    s,
    (BYTE *)InputSecurityToken[0].pvBuffer,
    InputSecurityToken[0].cbBuffer))
{
     MyHandleError("The message was not sent.");
}

//--------------------------------------------------------------------
//   Send the signature.

if(!SendMsg(
     s,
    (BYTE *)InputSecurityToken[1].pvBuffer,
    InputSecurityToken[1].cbBuffer ))
{
     MyHandleError("The signature was not sent.");
}
```



[**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) retourne la **valeur true** si le contexte est configuré pour autoriser les messages de signature et si le descripteur de mémoire tampon d’entrée est correctement mis en forme. Une fois le message signé, le message et la signature avec leurs longueurs sont envoyés à l’ordinateur distant.

> [!Note]  
> Le contenu des données des structures [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) est envoyé, et non pas les structures **SecBuffer** elles-mêmes, ni la structure [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) . Les nouvelles structures **SecBuffer** et une nouvelle structure **SecBufferDesc** sont créées par l’application réceptrice pour vérifier la signature.

 

 

 
