---
description: Le fichier d’en-tête suivant doit être inclus avec les exemples SSPI du client et du serveur en tant que SspiExample. h. Elle déclare les fonctions qui gèrent la communication avec le package de sécurité.
ms.assetid: 358c2cd6-674b-4d70-9657-800b0d1b2fe7
title: Fichier d’en-tête pour le client et le serveur SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f2702186f7a0a9def4405890f39f588dbbfa84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393591"
---
# <a name="header-file-for-sspi-client-and-server"></a><span data-ttu-id="322cf-104">Fichier d’en-tête pour le client et le serveur SSPI</span><span class="sxs-lookup"><span data-stu-id="322cf-104">Header File for SSPI Client and Server</span></span>

<span data-ttu-id="322cf-105">Le fichier d’en-tête suivant doit être inclus avec les exemples SSPI du client et du serveur en tant que SspiExample. h.</span><span class="sxs-lookup"><span data-stu-id="322cf-105">The following header file should be included with both the client and the server SSPI samples as SspiExample.h.</span></span> <span data-ttu-id="322cf-106">Elle déclare les fonctions qui gèrent la communication avec le package de sécurité.</span><span class="sxs-lookup"><span data-stu-id="322cf-106">It declares functions that handle communication with the security package.</span></span>


```C++
//  SspiExample.h
#include <sspi.h>
#include <windows.h>

BOOL SendMsg (SOCKET s, PBYTE pBuf, DWORD cbBuf);
BOOL ReceiveMsg (SOCKET s, PBYTE pBuf, DWORD cbBuf, DWORD *pcbRead);
BOOL SendBytes (SOCKET s, PBYTE pBuf, DWORD cbBuf);
BOOL ReceiveBytes (SOCKET s, PBYTE pBuf, DWORD cbBuf, DWORD *pcbRead);
void cleanup();

BOOL GenClientContext (
    BYTE *pIn,
    DWORD cbIn,
    BYTE *pOut,
    DWORD *pcbOut,
    BOOL *pfDone,
    CHAR *pszTarget,
    CredHandle *hCred,
    struct _SecHandle *hcText
);

BOOL GenServerContext (
   BYTE *pIn,
   DWORD cbIn,
   BYTE *pOut,
   DWORD *pcbOut,
   BOOL *pfDone,
   BOOL  fNewCredential
);

BOOL EncryptThis (
         PBYTE pMessage, 
         ULONG cbMessage,
         BYTE ** ppOutput,
         LPDWORD pcbOutput,
         ULONG securityTrailer
    );

PBYTE DecryptThis(
         PBYTE achData, 
         LPDWORD pcbMessage,
         struct _SecHandle *hCtxt,
         ULONG   cbSecurityTrailer
);

BOOL 
SignThis (
         PBYTE pMessage, 
         ULONG cbMessage,
         BYTE ** ppOutput,
         LPDWORD pcbOutput
);

PBYTE VerifyThis(
          PBYTE pBuffer, 
          LPDWORD pcbMessage,
          struct _SecHandle *hCtxt,
          ULONG   cbMaxSignature
);

void PrintHexDump(DWORD length, PBYTE buffer);

BOOL ConnectAuthSocket (
   SOCKET *s, 
   CredHandle *hCred, 
   struct _SecHandle *hcText
);

BOOL CloseAuthSocket (SOCKET s);

BOOL DoAuthentication (SOCKET s);

void MyHandleError(char *s);

```



 

 



