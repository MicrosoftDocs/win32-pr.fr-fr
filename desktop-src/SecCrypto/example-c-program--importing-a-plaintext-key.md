---
description: Identifiez une clé à l’aide d’un handle HCRYPTKEY.
ms.assetid: 23569104-a302-40de-a31a-a4ee22d5f7f2
title: 'Exemple de programme C : importation d’une clé en texte clair'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92341f4118770b963a9ea3dd47a153da0fe406b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321029"
---
# <a name="example-c-program-importing-a-plaintext-key"></a><span data-ttu-id="8d969-103">Exemple de programme C : importation d’une clé en texte clair</span><span class="sxs-lookup"><span data-stu-id="8d969-103">Example C Program: Importing a Plaintext Key</span></span>

<span data-ttu-id="8d969-104">La plupart des fonctions de ce kit de développement logiciel (SDK) requièrent que vous identifiiez une clé à l’aide d’un handle **HCRYPTKEY** .</span><span class="sxs-lookup"><span data-stu-id="8d969-104">Many of the functions in this SDK require that you identify a key by using an **HCRYPTKEY** handle.</span></span> <span data-ttu-id="8d969-105">Si votre clé est contenue dans un tableau d’octets, vous pouvez créer un descripteur à l’aide de la fonction [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) , comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="8d969-105">If your key is contained in a byte array, you can create a handle by using the [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) function as shown in the following example.</span></span>

<span data-ttu-id="8d969-106">Cet exemple illustre les tâches et les fonctions CryptoAPI suivantes :</span><span class="sxs-lookup"><span data-stu-id="8d969-106">This example demonstrates the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="8d969-107">Acquisition d’un handle vers un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) en appelant [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span><span class="sxs-lookup"><span data-stu-id="8d969-107">Acquiring a handle to a [*cryptographic service provider*](../secgloss/c-gly.md) by calling [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta).</span></span>
-   <span data-ttu-id="8d969-108">Importation d’une clé en texte clair dans le conteneur de clé CSP en appelant [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span><span class="sxs-lookup"><span data-stu-id="8d969-108">Importing a plaintext key into the CSP key container by calling [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey).</span></span>
-   <span data-ttu-id="8d969-109">Exportation d’une clé à partir du conteneur de clé en appelant [**CyptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span><span class="sxs-lookup"><span data-stu-id="8d969-109">Exporting a key from the key container by calling [**CyptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey).</span></span>
-   <span data-ttu-id="8d969-110">Impression de la clé exportée sur la console pour vérifier que la clé en texte clair a été importée dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="8d969-110">Printing the exported key to the console to verify that the plaintext key was indeed imported into the container.</span></span>
-   <span data-ttu-id="8d969-111">Libération de la mémoire réservée pour la clé de texte en clair.</span><span class="sxs-lookup"><span data-stu-id="8d969-111">Releasing the memory reserved for the plaintext key.</span></span>
-   <span data-ttu-id="8d969-112">Libération du CSP en appelant [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext).</span><span class="sxs-lookup"><span data-stu-id="8d969-112">Releasing the CSP by calling [**CryptReleaseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext).</span></span>


```C++
#include <stdio.h>
#include <tchar.h>
#include <windows.h>
#include <wincrypt.h>
#pragma comment(lib, "crypt32.lib")

// DesKeyBlob:      A plaintext key BLOB stored in a byte array. The 
//                  byte array  must have the following format:
//                      BLOBHEADER hdr;
//                      DWORD dwKeySize;
//                      BYTE rgbKeyData [];

BYTE DesKeyBlob[] = {
    0x08,0x02,0x00,0x00,0x01,0x66,0x00,0x00, // BLOB header 
    0x08,0x00,0x00,0x00,                     // key length, in bytes
    0xf1,0x0e,0x25,0x7c,0x6b,0xce,0x0d,0x34  // DES key with parity
    };

int _tmain()
{
//--------------------------------------------------------------------
// Declare variables.
//
// hProv:           Cryptographic service provider (CSP). This example
//                  uses the Microsoft Enhanced Cryptographic 
//                  Provider.
// hKey:            Key to be used. In this example, you import the 
//                  key as a PLAINTEXTKEYBLOB.
// dwBlobLen:       Length of the plaintext key.
// pbKeyBlob:       Pointer to the exported key.

HCRYPTPROV hProv  = NULL;
HCRYPTKEY hKey    = NULL;
DWORD dwBlobLen;
BYTE* pbKeyBlob;

//--------------------------------------------------------------------
// Acquire a handle to the CSP.

if(!CryptAcquireContext(
   &hProv,
   NULL,
   MS_ENHANCED_PROV,
   PROV_RSA_FULL,
   CRYPT_VERIFYCONTEXT))
   {
      // If the key container cannot be opened, try creating a new
      // container by specifying a container name and setting the 
      // CRYPT_NEWKEYSET flag.
      if(NTE_BAD_KEYSET == GetLastError())
      {
         if(!CryptAcquireContext(
            &hProv,
            L"mytestcontainer",
            MS_ENHANCED_PROV,
            PROV_RSA_FULL,
            CRYPT_NEWKEYSET | CRYPT_VERIFYCONTEXT))
            {
               printf("Error in AcquireContext 0x%08x \n",
                  GetLastError());
               return 1;
            }
      }
      else 
      {
         printf(" Error in AcquireContext 0x%08x \n",GetLastError());
         return 1;
      }
   }

   // Use the CryptImportKey function to import the PLAINTEXTKEYBLOB
   // BYTE array into the key container. The function returns a 
   // pointer to an HCRYPTKEY variable that contains the handle of
   // the imported key.

   if (!CryptImportKey(
       hProv,
       DesKeyBlob,
       sizeof(DesKeyBlob),
       0,
       CRYPT_EXPORTABLE,
       &hKey ) )
   {
      printf("Error 0x%08x in importing the Des key \n",
         GetLastError());
   }

   // For the purpose of this example, you can export the key and 
   // print it to verify that the plain text key created above is  
   // the key that was imported into the CSP.
   // Call CryptExportKey once to determine the length of the key.
   // Allocate memory for the BLOB, and call CryptExportKey again
   // to retrieve the key from the CSP key container.

   if(!CryptExportKey(   
      hKey,    
      NULL,    
      PLAINTEXTKEYBLOB,
      0,    
      NULL, 
      &dwBlobLen)) 
      {
         printf("Error 0x%08x computing BLOB length.\n",
            GetLastError());
         return 1;
      }

   if(pbKeyBlob = (BYTE*)malloc(dwBlobLen)) 
   {
      printf("Memory has been allocated for the BLOB. \n");
   }
   else
   {
      printf("Out of memory. \n");
      return 1;
   }

   if(!CryptExportKey(   
      hKey, 
      NULL,    
      PLAINTEXTKEYBLOB,    
      0,    
      pbKeyBlob,    
      &dwBlobLen))
      {
         printf("Error 0x%08x exporting key.\n", GetLastError());
         return 1;
      }

   DWORD count = 0;
   printf("Printing Key BLOB for verification \n");
   for(count=0; count < dwBlobLen;)
   {
      printf("%02x",pbKeyBlob[count]);
      count ++;
   }

   // Free resources.

   if(pbKeyBlob)
   {
      free(pbKeyBlob);
   }

   if(hProv)
   {
      CryptReleaseContext(hProv, 0);
   }

    return 0;
}
```



 

 
