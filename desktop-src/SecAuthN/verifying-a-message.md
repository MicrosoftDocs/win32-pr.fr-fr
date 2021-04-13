---
description: L’exemple suivant montre le code permettant de recevoir et de vérifier un message signé. L’exemple reçoit la mémoire tampon de signature et sa taille dans SignatureBuffer et SignatureBufferSize, ainsi que la mémoire tampon des messages et sa taille dans MessageBuffer et MessageBufferSize.
ms.assetid: 3e71aa0f-d135-4311-96f3-305762543627
title: Vérification d’un message
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ebf62be707efcbd3ab3a5eca5345261ca1a0fde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318245"
---
# <a name="verifying-a-message"></a><span data-ttu-id="36cb2-104">Vérification d’un message</span><span class="sxs-lookup"><span data-stu-id="36cb2-104">Verifying a Message</span></span>

<span data-ttu-id="36cb2-105">L’exemple suivant montre le code permettant de recevoir et de vérifier un message signé.</span><span class="sxs-lookup"><span data-stu-id="36cb2-105">The following example shows code to receive and verify a signed message.</span></span> <span data-ttu-id="36cb2-106">L’exemple reçoit la mémoire tampon de signature et sa taille dans SignatureBuffer et SignatureBufferSize, ainsi que la mémoire tampon des messages et sa taille dans MessageBuffer et MessageBufferSize.</span><span class="sxs-lookup"><span data-stu-id="36cb2-106">The example receives the signature buffer and its size in SignatureBuffer and SignatureBufferSize and the message buffer and its size in MessageBuffer and MessageBufferSize.</span></span>

<span data-ttu-id="36cb2-107">L’exemple suppose qu’une variable **SecHandle** nommée phContext et une structure de **Socket** nommée s sont initialisées.</span><span class="sxs-lookup"><span data-stu-id="36cb2-107">The example assumes that a **SecHandle** variable named phContext and a **SOCKET** structure named s are initialized.</span></span> <span data-ttu-id="36cb2-108">Pour les déclarations et les initiations de ces variables, consultez [utilisation de SSPI avec un client Windows Sockets](using-sspi-with-a-windows-sockets-client.md) et [utilisation de SSPI avec un serveur Windows Sockets](using-sspi-with-a-windows-sockets-server.md).</span><span class="sxs-lookup"><span data-stu-id="36cb2-108">For the declarations and initiations of these variables, see [Using SSPI with a Windows Sockets Client](using-sspi-with-a-windows-sockets-client.md) and [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).</span></span> <span data-ttu-id="36cb2-109">Ce code inclut les appels aux fonctions dans secur32. lib, qui doivent être inclus dans les bibliothèques de liens.</span><span class="sxs-lookup"><span data-stu-id="36cb2-109">This code includes calls to functions in Secur32.lib, which must be included among the link libraries.</span></span>


```C++
//--------------------------------------------------------------------
//  Declare and initialize local variables.
#include <windows.h>
#include <stdio.h>
#include <sspi.h>

#define SECURITY_WIN32
#define MaxMessageLength 1024
#define BUFSIZ 512

void main()
{
    BYTE MessageBuffer[BUFSIZ];
    BYTE SignatureBuffer[BUFSIZ];
    DWORD MessageBufferSize;
    DWORD SignatureBufferSize;
    SECURITY_STATUS SecStatus;
    SecBufferDesc InputBufferDescriptor;
    SecBuffer InputSecurityToken[2];
    ULONG fQOP;

    //------------------------------------------------------------------
    //    Receive the message.

    if(!(ReceiveMsg(
         s,
         MessageBuffer,
         MaxMessageLength,
         &MessageBufferSize)))
    {
         MyHandleError("Error. Message not received.");
    }

    //------------------------------------------------------------------
    //    Receive the signature.

    if(!(ReceiveMsg(
         s,
         SignatureBuffer,
         MaxMessageLength,
         &SignatureBufferSize)))
    {
         MyHandleError("Error. Signature not received.");
    }

    //------------------------------------------------------------------
    // Build the input buffer descriptor.

    InputBufferDescriptor.cBuffers = 2;
    InputBufferDescriptor.pBuffers = InputSecurityToken;
    InputBufferDescriptor.ulVersion = SECBUFFER_VERSION;

    //-------------------------------------------------------------------
    // Build the security buffer for the message.

    InputSecurityToken[0].BufferType = SECBUFFER_DATA;
    InputSecurityToken[0].cbBuffer = MessageBufferSize;
    InputSecurityToken[0].pvBuffer = MessageBuffer;

    //-------------------------------------------------------------------
    // Build the security buffer for the signature.

    InputSecurityToken[1].BufferType = SECBUFFER_TOKEN;
    InputSecurityToken[1].cbBuffer = SignatureBufferSize;
    InputSecurityToken[1].pvBuffer = SignatureBuffer;

    //--------------------------------------------------------------------
    // Call VerifySignature. 

    SecStatus = VerifySignature(
          &phContext,
          &InputBufferDescriptor,  // input message descriptor
          0,                       // no sequence number
          &fQOP                    // quality of protection
          );
    if(SecStatus == SEC_E_OK)
    {
         printf("The signature verified the message.\n");
    }
    else
         if(SecStatus == SEC_E_MESSAGE_ALTERED)
         {
              printf("The message was altered in transit.\n");
         }
         else
              if(SecStatus == SEC_E_OUT_OF_SEQUENCE )
              {
                  printf("The message is out of sequence.\n");
              }
              else
              {
                  printf("An unknown error occurred in VerifyMessage.\n");
              }
}
```



 

 



