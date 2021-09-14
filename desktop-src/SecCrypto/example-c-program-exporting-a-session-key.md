---
description: L’exemple suivant crée une clé de session aléatoire et crée un objet BLOB de clé exportable. L’exemple illustre l’utilisation de CryptGetUserKey, CryptExportKey et des fonctions associées.
ms.assetid: a7f2fdd1-9514-4cda-bae2-2f379dd9a27d
title: 'Exemple de programme C : exportation d’une clé de session'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5252e5eced86dd4e671f5080cf6dab5e1ec96b9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121050"
---
# <a name="example-c-program-exporting-a-session-key"></a>Exemple de programme C : exportation d’une clé de session

L’exemple suivant crée une clé de session aléatoire et crée un [*objet blob de clé*](../secgloss/k-gly.md)exportable. L’exemple illustre l’utilisation de [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey), [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)et des fonctions associées.

Cet exemple illustre les tâches et les fonctions CryptoAPI suivantes :

-   Acquisition d’un contexte CSP à l’aide de [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).
-   Accès à deux paires différentes de clés publiques/privées à l’aide de [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey).
-   Génération d’une clé de session exportable à l’aide de [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey).
-   Création d’un [*objet blob de clé simple*](../secgloss/s-gly.md) contenant une clé de session à l’aide de [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).
-   La destruction d’une clé de session et l’accès aux deux paires de clés publiques/privées à l’aide de [**CryptDestroyKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey).
-   Libération du contexte du fournisseur de services Cloud à l’aide de [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext).

Cet exemple utilise la fonction [**MyHandleError**](myhandleerror.md). Le code de cette fonction est inclus dans l’exemple. Le code pour cette fonction et d’autres fonctions auxiliaires est également listé sous [usage général Functions](general-purpose-functions.md).


```C++
//--------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// This example program creates a session key and a simple key 
// BLOB holding that session key. The key BLOB can be written to disk 
// and later read from a disk file.
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main(void)
{
//--------------------------------------------------------------------
// Declare and initialize variables.

HCRYPTPROV hProv;       // CSP handle
HCRYPTKEY hSignKey;     // Signature key pair handle
HCRYPTKEY hXchgKey;     // Exchange key pair handle
HCRYPTKEY hKey;         // Session key handle
BYTE *pbKeyBlob;        // Pointer to a simple key BLOB
DWORD dwBlobLen;        // The length of the key BLOB

//--------------------------------------------------------------------
// Acquire a cryptographic provider context handle.

if(CryptAcquireContext(
   &hProv, 
   NULL, 
   NULL, 
   PROV_RSA_FULL, 
   0)) 
{
    printf("The CSP has been acquired. \n");
}
else
{
    MyHandleError("Error during CryptAcquireContext.");
}
//--------------------------------------------------------------------
// Get a handle to the signature key.
// The signature key must exist before it can be retrieved. For more
// information, see the CryptGetUserKey documentation.

if(CryptGetUserKey(
   hProv, 
   AT_SIGNATURE, 
   &hSignKey)) 
{
    printf("The signature key has been acquired. \n");
}
else
{
    MyHandleError("Error during CryptGetUserKey for signkey.");
}
//--------------------------------------------------------------------
// Get a handle to the key exchange key.
// The key must exist before it can be retrieved. For more
// information, see the CryptGetUserKey documentation.

if(CryptGetUserKey(
   hProv, 
   AT_KEYEXCHANGE, 
   &hXchgKey)) 
{
    printf("The key exchange key has been acquired. \n");
}
else
{
    printf("Error during CryptGetUserKey exchange key.");
}
// hSignKey may be used to verify a signature. hXchgKey will be used
// to export a session key.

//--------------------------------------------------------------------
// Generate a session key.

if (CryptGenKey(     
    hProv,      
    CALG_RC4,      
    CRYPT_EXPORTABLE, 
    &hKey))
{   
    printf("Original session key is created. \n");
}
else
{
   MyHandleError("ERROR -- CryptGenKey.");
}
// Determine the size of the key BLOB and allocate memory.

if(CryptExportKey(
   hKey, 
   hXchgKey, 
   SIMPLEBLOB, 
   0, 
   NULL, 
   &dwBlobLen)) 
{
     printf("Size of the BLOB for the session key determined. \n");
}
else
{
     MyHandleError("Error computing BLOB length.");
}

if(pbKeyBlob = (BYTE*)malloc(dwBlobLen)) 
{
    printf("Memory has been allocated for the BLOB. \n");
}
else
{
    MyHandleError("Out of memory. \n");
}
//--------------------------------------------------------------------
// Export the key into a simple key BLOB.

if(CryptExportKey(
   hKey, 
   hXchgKey, 
   SIMPLEBLOB, 
   0, 
   pbKeyBlob, 
   &dwBlobLen))
{
     printf("Contents have been written to the BLOB. \n");
}
else
{
    MyHandleError("Error during CryptExportKey.");
}
//--------------------------------------------------------------------
//   At this point, other processing such as writing the key BLOB to
//   a file could be done.

//--------------------------------------------------------------------
// After all processing, clean up.

//--------------------------------------------------------------------
//  Free the memory used by the key BLOB.

free(pbKeyBlob);

// Destroy the session key.
if(hKey)
    CryptDestroyKey(hKey);

// Destroy the signature key handle.
if(hSignKey)
    CryptDestroyKey(hSignKey);

// Destroy the key exchange key handle.
if(hXchgKey)
     CryptDestroyKey(hXchgKey);

// Release the provider handle.
if(hProv) 
   CryptReleaseContext(hProv, 0);
printf("The program ran to completion without error. \n");

}// End of main                                                    

//--------------------------------------------------------------------
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



 

 
