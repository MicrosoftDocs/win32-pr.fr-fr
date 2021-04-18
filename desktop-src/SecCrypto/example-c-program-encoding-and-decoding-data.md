---
description: Encode et décode les données simples et générales, et illustre les tâches et les fonctions CryptoAPI suivantes.
ms.assetid: 7634bd05-fca0-4538-94da-7af6e3d8e6b8
title: 'Exemple de programme C : encodage et décodage de données'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b694bcb9836dfa750940ef75d41ba703251ee190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536322"
---
# <a name="example-c-program-encoding-and-decoding-data"></a><span data-ttu-id="00998-103">Exemple de programme C : encodage et décodage de données</span><span class="sxs-lookup"><span data-stu-id="00998-103">Example C Program: Encoding and Decoding Data</span></span>

<span data-ttu-id="00998-104">L’exemple suivant encode et décode les données simples et générales, et illustre les tâches et les fonctions CryptoAPI suivantes.</span><span class="sxs-lookup"><span data-stu-id="00998-104">The following example encodes and decodes simple, general data, and illustrates the following tasks and CryptoAPI functions.</span></span>

-   <span data-ttu-id="00998-105">Détermination de la longueur nécessaire pour que la mémoire tampon contienne les données encodées à l’aide de [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength).</span><span class="sxs-lookup"><span data-stu-id="00998-105">Determining the length needed for the buffer to hold the encoded data using [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength).</span></span>
-   <span data-ttu-id="00998-106">Ouverture d’un message pour l’encodage à l’aide de [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode).</span><span class="sxs-lookup"><span data-stu-id="00998-106">Opening a message for encoding using [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode).</span></span>
-   <span data-ttu-id="00998-107">Ajout de contenu au message encodé à l’aide de [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).</span><span class="sxs-lookup"><span data-stu-id="00998-107">Adding content to the encoded message using [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate).</span></span>
-   <span data-ttu-id="00998-108">Copie du message encodé dans une mémoire tampon à l’aide de [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam).</span><span class="sxs-lookup"><span data-stu-id="00998-108">Copying the encoded message into a buffer using [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam).</span></span>
-   <span data-ttu-id="00998-109">Fermeture du message encodé à l’aide de [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).</span><span class="sxs-lookup"><span data-stu-id="00998-109">Closing the encoded message using [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose).</span></span>
-   <span data-ttu-id="00998-110">Ouverture d’un message à décoder à l’aide de [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode).</span><span class="sxs-lookup"><span data-stu-id="00998-110">Opening a message to decode using [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode).</span></span>
-   <span data-ttu-id="00998-111">Utilisation de [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) et [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) pour l’extraction des données décodées.</span><span class="sxs-lookup"><span data-stu-id="00998-111">Using [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) and [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam) to get the decoded data.</span></span>

<span data-ttu-id="00998-112">Cet exemple utilise la fonction [**MyHandleError**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="00998-112">This example uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="00998-113">Le code de cette fonction est inclus dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="00998-113">The code for this function is included with the sample.</span></span> <span data-ttu-id="00998-114">Le code pour cette fonction et d’autres fonctions auxiliaires est également listé sous [usage général Functions](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="00998-114">Code for this and other auxiliary functions is also listed under [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Example of encoding and decoding a message.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{
//-------------------------------------------------------------------
// Declare and initialize variables. This includes getting a pointer 
// to the message content. This sample program creates the message 
// content and gets a pointer to it. In most situations, 
// the content will exist somewhere and a pointer to it
// will get passed to the application. 

HCRYPTMSG hMsg;
BYTE* pbContent;     // a byte pointer to the message
DWORD cbContent;     // the size of message
DWORD cbEncodedBlob;
BYTE *pbEncodedBlob;


//-------------------------------------------------------------------
//  The following variables are used only in the decoding phase.

DWORD cbDecoded;
BYTE *pbDecoded;

//-------------------------------------------------------------------
//  Begin processing. Display the original message.

pbContent = (BYTE*) "Security is our only business";
cbContent = strlen((char *) pbContent)+1;

printf("The original message => %s\n",pbContent);  

//-------------------------------------------------------------------
// Get the size of the encoded message BLOB.

if(cbEncodedBlob = CryptMsgCalculateEncodedLength(
             MY_ENCODING_TYPE,       // message encoding type
             0,                      // flags
             CMSG_DATA,              // message type
             NULL,                   // pointer to structure
             NULL,                   // inner content object ID
             cbContent))             // size of content
{
    printf("The length of the data has been calculated. \n");
}
else
{
    MyHandleError("Getting cbEncodedBlob length failed");
}
//-------------------------------------------------------------------
// Allocate memory for the encoded BLOB.

if(pbEncodedBlob = (BYTE *) malloc(cbEncodedBlob))
{
   printf("Memory has been allocated for the signed message. \n");
}
else
{
   MyHandleError("Memory allocation failed");
}
//-------------------------------------------------------------------
// Open a message to encode.

if(hMsg = CryptMsgOpenToEncode(
          MY_ENCODING_TYPE,        // encoding type
          0,                       // flags
          CMSG_DATA,               // message type
          NULL,                    // pointer to structure
          NULL,                    // inner content object ID
          NULL))                   // stream information (not used)
{
    printf("The message to be encoded has been opened. \n");
}
else
{
     MyHandleError("OpenToEncode failed");
}
//-------------------------------------------------------------------
// Update the message with the data.

if(CryptMsgUpdate(
        hMsg,         // handle to the message
        pbContent,    // pointer to the content
        cbContent,    // size of the content
        TRUE))        // last call
{
     printf("Content has been added to the encoded message. \n");
}
else
{
      MyHandleError("MsgUpdate failed");
}
//-------------------------------------------------------------------
// Get the resulting message.

if(CryptMsgGetParam(
               hMsg,                      // handle to the message
               CMSG_BARE_CONTENT_PARAM,   // parameter type
               0,                         // index
               pbEncodedBlob,             // pointer to the BLOB
               &cbEncodedBlob))           // size of the BLOB
{
    printf("Message encoded successfully. \n");
}
else
{
      MyHandleError("MsgGetParam failed");
}
//-------------------------------------------------------------------
// pbEncodedBlob now points to the encoded, signed content.

//-------------------------------------------------------------------
// Close the message.

if(hMsg)
    CryptMsgClose(hMsg);

//-------------------------------------------------------------------
// The following code decodes a message. 
// This code may be included here or could be used
// in a stand-alone program if the message 
// to be decoded and its size were input. 
// The encoded message BLOB and its length could be read 
// from a disk file or could be extracted from an email message 
// or other input source.

//-------------------------------------------------------------------
// Open a message for decoding.

if(hMsg = CryptMsgOpenToDecode(
               MY_ENCODING_TYPE,      // encoding type.
               0,                     // flags.
               CMSG_DATA,             // look for a data message.
               NULL,                  // cryptographic provider.
               NULL,                  // recipient information.
               NULL))                 // stream information.
{
     printf("The message to decode is open. \n");
}
else
{
    MyHandleError("OpenToDecode failed");
}
//-------------------------------------------------------------------
// Update the message with an encoded BLOB.
// Both pbEncodedBlob, the encoded data, 
// and cbEncodedBlob, the length of the encoded data,
// must be available. 

printf("\nThe length of the encoded message is %d.\n\n",
    cbEncodedBlob);

if(CryptMsgUpdate(
    hMsg,                 // handle to the message
    pbEncodedBlob,        // pointer to the encoded BLOB
    cbEncodedBlob,        // size of the encoded BLOB
    TRUE))                // last call
{
      printf("The encoded BLOB has been added to the message. \n");
}
else
{
    MyHandleError("Decode MsgUpdate failed");
}
//-------------------------------------------------------------------
// Get the size of the content.

if(CryptMsgGetParam(
                  hMsg,                  // handle to the message
                  CMSG_CONTENT_PARAM,    // parameter type
                  0,                     // index
                  NULL,                  // address for returned 
                                         // information
                  &cbDecoded))           // size of the returned
                                         // information
{
    printf("The decoded message size is %d. \n", cbDecoded);
}
else
{
    MyHandleError("Decode CMSG_CONTENT_PARAM failed");
}
//-------------------------------------------------------------------
// Allocate memory.

if(pbDecoded = (BYTE *) malloc(cbDecoded))
{
     printf("Memory has been allocated for the decoded message.\n");
}
else
{
    MyHandleError("Decoding memory allocation failed.");
}
//-------------------------------------------------------------------
// Get a pointer to the content.

if(CryptMsgGetParam(
                  hMsg,                  // handle to the message
                  CMSG_CONTENT_PARAM,    // parameter type
                  0,                     // index
                  pbDecoded,             // address for returned 
                                         // information
                  &cbDecoded))           // size of the returned 
                                         // information
{
     printf("The message is %s.\n",(LPSTR)pbDecoded);
}
else
{
     MyHandleError("Decode CMSG_CONTENT_PARAM #2 failed");
}
//-------------------------------------------------------------------
// Clean up.

if(pbEncodedBlob)
   free(pbEncodedBlob);
if(pbDecoded)
   free(pbDecoded);
if(hMsg)
    CryptMsgClose(hMsg);

printf("This program ran to completion without error. \n");

} //  End of main

//-------------------------------------------------------------------
//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message and exit 
//  the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    printf("An error occurred in running the program.\n");
    printf("%s\n",s);
    printf("Error number %x\n.",GetLastError());
    printf("Program terminating.\n");
    exit(1);
}
```



 

 



