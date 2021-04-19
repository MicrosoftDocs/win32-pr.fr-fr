---
description: L’exemple suivant montre le code standard RSA/SChannel côté serveur pour la création d’une clé principale.
ms.assetid: 617cda1e-0619-4162-85eb-d1f5aa35fd1c
title: Code du serveur RSA pour la création de la clé principale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c337ef8093dc2dead96e55e481781ff902ee2485
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521206"
---
# <a name="rsa-server-code-for-creating-the-master-key"></a>Code du serveur RSA pour la création de la clé principale

L’exemple suivant montre le code standard RSA/SChannel côté serveur pour la création d’une [*clé principale*](../secgloss/m-gly.md).


```C++
//--------------------------------------------------------------------
//   Define and initialize local variables.

HCRYPTPROV hProv         = <server's key container>;
PBYTE      pbKeyExchange = <pointer to RSA envelope>;
DWORD      dwKeyExchange = <size of RSA envelope>;
HCRYPTKEY  hPublicKey;
HCRYPTKEY  hMasterKey;
ALG_ID     Algid;
DWORD      dwFlags =0 ;
BYTE       rgbBlob[<max BLOB size>];
DWORD      cbBlob;

//--------------------------------------------------------------------
// Select the master key type.

switch(<protocol being used>)
{
    case <PCT 1.0>:
        Algid = CALG_PCT1_MASTER;
        break;

    case <SSL 2.0>:
        Algid = CALG_SSL2_MASTER;
        if(<we support SSL3>)
            dwFlags = CRYPT_SSL2_FALLBACK;
        break;

    case <SSL 3.0>:
        Algid = CALG_SSL3_MASTER;
        break;

    case <TLS 1.0>:
        Algid = CALG_TLS1_MASTER;
        break;
}

//--------------------------------------------------------------------
// Build a SIMPLEBLOB around the RSA envelope.
{
     BLOBHEADER *pBlobHeader = (BLOBHEADER *)rgbBlob;
     ALG_ID     *pAlgid      = (ALG_ID *)(pBlobHeader + 1);
     BYTE       *pData       = (BYTE *)(pAlgid + 1);

     pBlobHeader->bType    = SIMPLEBLOB;
     pBlobHeader->bVersion = CUR_BLOB_VERSION;
     pBlobHeader->reserved = 0;
     pBlobHeader->aiKeyAlg = Algid;

     *pAlgid = CALG_RSA_KEYX;

     ReverseMemCopy(
         pData, 
         pbKeyExchange, 
         cbKeyExchange);
}

//--------------------------------------------------------------------
// Decrypt the master key.

CryptGetUserKey(
         hProv, 
         AT_KEYEXCHANGE, 
         &hPublicKey);

CryptImportKey(
          hProv, 
          rgbBlob, 
          cbBlob, 
          hPublicKey, 
          dwFlags, 
          &hMasterKey);

CryptDestroyKey(hPublicKey);
```



 

 
