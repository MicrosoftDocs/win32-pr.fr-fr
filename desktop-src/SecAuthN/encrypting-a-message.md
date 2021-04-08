---
description: L’exemple suivant montre un message chiffré avant d’être envoyé à un ordinateur distant via la connexion sécurisée.
ms.assetid: 1788b496-ad19-427e-be07-4aa68543fced
title: Chiffrement d’un message
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7fcc987e17c37f9b2eb80289f257101b51f5f3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861982"
---
# <a name="encrypting-a-message"></a>Chiffrement d’un message

L’exemple suivant montre un message chiffré avant d’être envoyé à un ordinateur distant via la connexion sécurisée.

L’exemple suppose qu’une variable **SecHandle** nommée `phContext` et un **Socket** nommé `s` sont initialisés. Pour les déclarations et les initiations de ces variables, consultez [utilisation de SSPI avec un client Windows Sockets](using-sspi-with-a-windows-sockets-client.md) et [utilisation de SSPI avec un serveur Windows Sockets](using-sspi-with-a-windows-sockets-server.md). Cet exemple inclut des appels aux fonctions dans secur32. lib, qui doivent être inclus dans les bibliothèques de liens.


```C++
//--------------------------------------------------------------------
//   Declare and initialize local variables.

SecPkgContext_StreamSizes  Sizes;
SECURITY_STATUS            scRet;
SecBufferDesc              Message;
SecBuffer                  Buffers[4];
SecBuffer                  *pDataBuffer;

PBYTE                       pbIoBuffer;
DWORD                       cbIoBuffer;
DWORD                       cbIoBufferLength;
PBYTE                       pbMessage;
DWORD                       cbMessage;

//--------------------------------------------------------------------
// Get the stream encryption sizes. This needs to 
// be done once per connection. 
// phContext must have been initialized during the handshake process.

scRet = QueryContextAttributes(
            phContext,
            SECPKG_ATTR_STREAM_SIZES,
            &Sizes);

if(FAILED(scRet))
{
    MyHandleError("Error reading SECPKG_ATTR_STREAM_SIZES");
}

//--------------------------------------------------------------------
// Allocate a working buffer. The plaintext sent to EncryptMessage
// can never be more than 'Sizes.cbMaximumMessage', so a buffer 
// size of Sizes.cbMaximumMessage plus the header and trailer sizes 
// is sufficient for the longest message.

cbIoBufferLength = Sizes.cbHeader + 
                   Sizes.cbMaximumMessage +
                   Sizes.cbTrailer;

if(!(pbIoBuffer = malloc((BYTE *), cbIoBufferLength)))
{
    MyHandleError("Out of memory");
}

//--------------------------------------------------------------------
// Create a plaintext message to be encrypted offset into the data 
// buffer by "header size" bytes. This allows encryption in place.

pbMessage = pbIoBuffer + Sizes.cbHeader;

StringCbPrintfA(pbMessage,
                cbIoBufferLength - Sizes.cbHeader,
                "This is the plaintext message.");
cbMessage = strlen(pbMessage);

//--------------------------------------------------------------------
// Encrypt the plaintext message.

Buffers[0].pvBuffer     = pbIoBuffer;
Buffers[0].cbBuffer     = Sizes.cbHeader;
Buffers[0].BufferType   = SECBUFFER_STREAM_HEADER;

Buffers[1].pvBuffer     = pbMessage;
Buffers[1].cbBuffer     = cbMessage;
Buffers[1].BufferType   = SECBUFFER_DATA;

Buffers[2].pvBuffer     = pbMessage + cbMessage;
Buffers[2].cbBuffer     = Sizes.cbTrailer;
Buffers[2].BufferType   = SECBUFFER_STREAM_TRAILER;

Buffers[3].BufferType   = SECBUFFER_EMPTY;

Message.ulVersion       = SECBUFFER_VERSION;
Message.cBuffers        = 4;
Message.pBuffers        = Buffers;

scRet = EncryptMessage(phContext, 0, &Message, 0);

if(FAILED(scRet))
{
    MyHandleError("Error returned by EncryptMessage.");
}

//--------------------------------------------------------------------
// Send the encrypted data.

if(!(SendMsg(
     s,
     pbIoBuffer,
     Buffers[0].cbBuffer + Buffers[1].cbBuffer + 
           Buffers[2].cbBuffer)))
{
     MyHandleError("SendMsg failed.");
}
```



 

 



