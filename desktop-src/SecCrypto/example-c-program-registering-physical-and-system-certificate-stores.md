---
description: Affiche l’enregistrement (création) et l’ouverture d’un magasin système, l’inscription d’un magasin physique en tant que membre d’un magasin système et la désinscription (suppression) d’un magasin système.
ms.assetid: 857ab592-68c7-4660-b37d-b165aeee14f4
title: 'Exemple de programme C : inscription de magasins de certificats physiques et système'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 708a840767b4e49bd1ba5c70dd5ae63f0f9ab7bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319594"
---
# <a name="example-c-program-registering-physical-and-system-certificate-stores"></a><span data-ttu-id="70400-103">Exemple de programme C : inscription de magasins de certificats physiques et système</span><span class="sxs-lookup"><span data-stu-id="70400-103">Example C Program: Registering Physical and System Certificate Stores</span></span>

<span data-ttu-id="70400-104">Les magasins physiques peuvent être rendus plus ou moins permanents dans un magasin système.</span><span class="sxs-lookup"><span data-stu-id="70400-104">Physical stores may be made more or less permanent members of a system store.</span></span> <span data-ttu-id="70400-105">Lorsqu’un magasin physique est membre d’un magasin système, les opérations sur le magasin système, telles que la recherche d’un certificat, s’affichent dans tous les magasins physiques inscrits en tant que membres du magasin système.</span><span class="sxs-lookup"><span data-stu-id="70400-105">When a physical store is a member of a system store, operations on the system store such as finding a certificate will look in all of the physical stores that are registered as members of the system store.</span></span> <span data-ttu-id="70400-106">Un magasin physique peut être supprimé de l’appartenance à un magasin système à l’aide d’une fonction d’annulation d’inscription.</span><span class="sxs-lookup"><span data-stu-id="70400-106">A physical store can be removed from membership in a system store by using an unregister function.</span></span>

<span data-ttu-id="70400-107">Cet exemple montre les tâches et les fonctions CryptoAPI suivantes :</span><span class="sxs-lookup"><span data-stu-id="70400-107">This example shows the following tasks and CryptoAPI functions:</span></span>

-   <span data-ttu-id="70400-108">Enregistrement (création) d’un nouveau magasin système à l’aide de [**CertRegisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore).</span><span class="sxs-lookup"><span data-stu-id="70400-108">Registering (creating) a new system store using [**CertRegisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore).</span></span>
-   <span data-ttu-id="70400-109">Ouverture d’un magasin système nouvellement créé à l’aide de [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span><span class="sxs-lookup"><span data-stu-id="70400-109">Opening a newly created system store using [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore).</span></span>
-   <span data-ttu-id="70400-110">Inscription d’un magasin physique en tant que membre d’un magasin système à l’aide de [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).</span><span class="sxs-lookup"><span data-stu-id="70400-110">Registering a physical store as a member of a system store using [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).</span></span>
-   <span data-ttu-id="70400-111">Annulation de l’inscription (suppression) d’un magasin système à l’aide de [**CertUnregisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore).</span><span class="sxs-lookup"><span data-stu-id="70400-111">Unregistering (deleting) a system store using [**CertUnregisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore).</span></span>

<span data-ttu-id="70400-112">Cet exemple illustre également la création et la suppression de magasins système.</span><span class="sxs-lookup"><span data-stu-id="70400-112">This example also demonstrates the creation and deletion of system stores.</span></span>


```C++
// This example uses CertRegisterSystemStore.
#pragma comment(lib, "crypt32.lib")

// Copyright (C) Microsoft.  All rights reserved.
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)
void MyHandleError(char *s);

void main()
{


// Declare and initialize variables.

HCERTSTORE hSystemStore;
DWORD dwFlags= CERT_SYSTEM_STORE_CURRENT_USER;
LPCWSTR pvSystemName= L"NEWSTORE";  // For this setting of 
                                    // dwFlags, the store name may 
                                    // be prefixed with a user name.
CERT_PHYSICAL_STORE_INFO PhysicalStoreInfo;
BYTE fResponse  = 'n';

if(CertRegisterSystemStore(
    pvSystemName,
    dwFlags,
    NULL,
    NULL))
  printf("System store %S is registered. \n",pvSystemName);
else
  printf("The system store did not register. \n");


// Open the NEWSTORE as a system store.

if(hSystemStore = CertOpenStore(
   CERT_STORE_PROV_SYSTEM,   // the store provider type
   0,                        // the encoding type is not needed
   NULL,                     // use the default HCRYPTPROV
   CERT_SYSTEM_STORE_CURRENT_USER,
                             // set the store location in a registry
                             // location
   pvSystemName ))           // the store name as a Unicode string
{
     printf("The new store has been opened as a system store.\n");
}
else
{
     printf("The new store was not opened as a system store.\n");
}
if(hSystemStore)
{
    if(CertCloseStore(hSystemStore,0))
    {
        printf("The system store has been closed.\n");
    }
    else
    {
        printf("The system store could not be closed.\n");
    }
}
else
{
   printf("The system store did not need to be closed.\n");
}


// Initialize PhysicalStoreInfo.

PhysicalStoreInfo.cbSize=sizeof(CERT_PHYSICAL_STORE_INFO);
PhysicalStoreInfo.pszOpenStoreProvider=(LPSTR)
    CERT_STORE_PROV_FILENAME;
PhysicalStoreInfo.dwFlags=CERT_PHYSICAL_STORE_ADD_ENABLE_FLAG;


// Replace the path below with one that is appropriate for you.

PhysicalStoreInfo.OpenParameters.pbData = 
    (BYTE *) L"C:\\temp\\mystore";
PhysicalStoreInfo.OpenParameters.cbData = 
    (wcslen((LPWSTR) PhysicalStoreInfo.OpenParameters.pbData) + 1) * 
    sizeof(WCHAR);

PhysicalStoreInfo.dwPriority=1;
PhysicalStoreInfo.dwOpenEncodingType=MY_ENCODING_TYPE;


// Register the physical store.

if(CertRegisterPhysicalStore(
      L"NEWSTORE",
      dwFlags,
      L"TESTOR.STO",
      &PhysicalStoreInfo,
      NULL
      ))
{
       printf("Physical store is registered. \n");
}
else
{
       printf("The physical store was not registered.\n");
}  


//  Next, unregister the store.

printf("Would you like to unregister the %S store? (y/n) "
       ,pvSystemName);
scanf_s("%c",&fResponse);

if(fResponse=='y')
{
   if(CertUnregisterSystemStore(
     pvSystemName,
     dwFlags))
   {
      printf("System store %S has been unregistered.\n"
          ,pvSystemName);
   }
   else
   {
      printf("The system store was not unregistered.\n");
   }
}
}  // end main


//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to  
//  the standard error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // end of MyHandleError
```



 

 



