---
description: Cet exemple montre comment initialiser un tableau de mémoires tampons de sécurité.
ms.assetid: f8196a9c-786a-49a3-85a4-1bd5f414a653
title: Exemple de code SecBuffer et SecBufferDesc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7d28e885d6eec65c209caeda299b2f7e5f2ad3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233483"
---
# <a name="secbuffer-and-secbufferdesc-example-code"></a>Exemple de code SecBuffer et SecBufferDesc

Cet exemple montre comment initialiser un tableau de mémoires tampons de sécurité. Il montre les tampons de sécurité d’entrée initialisés par le côté serveur d’une connexion pour préparer un appel à [**AcceptSecurityContext (général)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext). Notez que la dernière mémoire tampon contient le jeton de sécurité opaque reçu par le client et que l' \_ indicateur ReadOnly SECBUFFER est défini sur [**SECBUFFER**](/windows/desktop/api/Sspi/ns-sspi-secbuffer).


```C++
SecBuffer  Buffers[3];
SecBufferDesc BufferDesc;
BYTE *pHeader;
BYTE *pMessage;
BYTE *pTrailer;

//--------------------------------------------------------------------
// pHeader, pMessage, and pTrailer are BYTE strings.
// In a working program, they would be assigned string values.

BufferDesc.ulVersion = SECBUFFER_VERSION;
BufferDesc.cBuffers = 3;
BufferDesc.pBuffers = Buffers;

Buffers[0].cbBuffer = sizeof(pHeader);
Buffers[0].BufferType = SECBUFFER_READONLY | SECBUFFER_DATA;
Buffers[0].pvBuffer = pHeader;

Buffers[1].cbBuffer = sizeof(pMessage);
Buffers[1].BufferType = SECBUFFER_DATA;
Buffers[1].pvBuffer = pMessage;

Buffers[2].cbBuffer = sizeof(pTrailer);
Buffers[2].BufferType = SECBUFFER_READONLY | SECBUFFER_TOKEN;
Buffers[2].pvBuffer = pTrailer;
```



 

 
