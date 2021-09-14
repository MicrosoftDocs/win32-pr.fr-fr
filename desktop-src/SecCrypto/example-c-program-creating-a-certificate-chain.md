---
description: L’exemple suivant crée et installe un moteur de chaîne de certificats qui n’est pas un moteur par défaut. Le moteur est utilisé pour créer des chaînes de certificats pour chacun des certificats dans un magasin de certificats.
ms.assetid: 960f2bb9-130f-494f-9af0-0ab8ae3eb6e2
title: 'Exemple de programme C : création d’une chaîne de certificats'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1857540f16cddfa754a0765d273a944e9a4a9044
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123178"
---
# <a name="example-c-program-creating-a-certificate-chain"></a>Exemple de programme C : création d’une chaîne de certificats

L’exemple suivant crée et installe un moteur de chaîne de certificats qui n’est pas un moteur par défaut. Le moteur est utilisé pour créer des chaînes de certificats pour chacun des certificats dans un [*magasin de certificats*](../secgloss/c-gly.md).

Cet exemple illustre les tâches et les fonctions [*CryptoAPI*](../secgloss/c-gly.md) suivantes :

-   Préparation de la création d’un moteur de chaîne de certificats non par défaut en déclarant et en initialisant une structure de données de [**configuration du moteur de chaîne de certificats \_ \_ \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_chain_engine_config) .
-   Création du moteur de recherche à l’aide de [**CertCreateCertificateChainEngine**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatechainengine).
-   À l’aide de [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea) pour ouvrir le magasin mon système.
-   Récupération de tous les certificats du magasin ouvert à l’aide de [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore) dans une boucle.
-   Pour chaque certificat dans le magasin ouvert, récupérez le nom du sujet à partir du certificat à l’aide de [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).
-   Création d’une chaîne de certificats pour chaque certificat à l’aide de [**CertGetCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatechain).
-   Création d’un doublon de la chaîne de certificats à l’aide de [**CertDuplicateCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatechain).
-   Utilisation de [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) pour libérer chaque chaîne avant la génération de la chaîne suivante.


```C++
#pragma comment(lib, "crypt32.lib")

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>

void MyHandleError(char *s);

void main(void)
{
//---------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
// Declare and initialize variables.

HCERTCHAINENGINE         hChainEngine;
CERT_CHAIN_ENGINE_CONFIG ChainConfig;
PCCERT_CHAIN_CONTEXT     pChainContext;
PCCERT_CHAIN_CONTEXT     pDupContext;
HCERTSTORE               hCertStore;
PCCERT_CONTEXT           pCertContext = NULL;
CERT_ENHKEY_USAGE        EnhkeyUsage;
CERT_USAGE_MATCH         CertUsage;  
CERT_CHAIN_PARA          ChainPara;
DWORD                    dwFlags=0;
LPWSTR                   pszNameString;



//---------------------------------------------------------
// Initialize data structures.

if(!(pszNameString=(LPWSTR)malloc(256)))
    MyHandleError("Memory allocation failed.");
EnhkeyUsage.cUsageIdentifier = 0;
EnhkeyUsage.rgpszUsageIdentifier=NULL;
CertUsage.dwType = USAGE_MATCH_TYPE_AND;
CertUsage.Usage  = EnhkeyUsage;
ChainPara.cbSize = sizeof(CERT_CHAIN_PARA);
ChainPara.RequestedUsage=CertUsage;

ChainConfig.cbSize = sizeof(CERT_CHAIN_ENGINE_CONFIG);
ChainConfig.hRestrictedRoot= NULL ;
ChainConfig.hRestrictedTrust= NULL ;
ChainConfig.hRestrictedOther= NULL ;
ChainConfig.cAdditionalStore=0 ;
ChainConfig.rghAdditionalStore = NULL ;
ChainConfig.dwFlags = CERT_CHAIN_CACHE_END_CERT;
ChainConfig.dwUrlRetrievalTimeout= 0 ;
ChainConfig.MaximumCachedCertificates=0 ;
ChainConfig.CycleDetectionModulus = 0;

//---------------------------------------------------------
// Create the nondefault certificate chain engine.

if(CertCreateCertificateChainEngine(
         &ChainConfig,
         &hChainEngine))
{
    printf("A chain engine has been created.\n");
}
else
{
    MyHandleError("The engine creation function failed.");
}
// Open the My system store.

if(hCertStore=CertOpenSystemStore(NULL,L"MY"))
{
       printf("The MY Store is open.\n");
}
else
{
       MyHandleError("The MY system store did not open.");
}

//-------------------------------------------------------
// Loop through the certificates in the store, 
// and create a chain for each.

while(pCertContext = CertEnumCertificatesInStore(
             hCertStore,
             pCertContext))
{
//-------------------------------------------------------------------
// Get and display the name of subject of the certificate.

if(CertGetNameString(   
   pCertContext,   
   CERT_NAME_SIMPLE_DISPLAY_TYPE,   
   0,
   NULL,   
   pszNameString,   
   128))
{
   printf("\nCertificate for %s found.\n",pszNameString);
}
else
{
   MyHandleError("CertGetName failed.");
}

//-------------------------------------------------------------------
// Build a chain using CertGetCertificateChain
// and the certificate retrieved.

if(CertGetCertificateChain(
    NULL,                  // use the default chain engine
    pCertContext,          // pointer to the end certificate
    NULL,                  // use the default time
    NULL,                  // search no additional stores
    &ChainPara,            // use AND logic and enhanced key usage 
                           //  as indicated in the ChainPara 
                           //  data structure
    dwFlags,
    NULL,                  // currently reserved
    &pChainContext))       // return a pointer to the chain created
{
    printf("The chain has been created. \n");
}
else
{
    MyHandleError("The chain could not be created.");
}

//---------------------------------------------------------------
// Display some of the contents of the chain.

printf("The size of the chain context "
       "is %d. \n",pChainContext->cbSize);
printf("%d simple chains found.\n",pChainContext->cChain);
printf("\nError status for the chain:\n");

switch(pChainContext->TrustStatus.dwErrorStatus)
{
case CERT_TRUST_NO_ERROR :
     printf("No error found for this certificate or chain.\n");
     break;
case CERT_TRUST_IS_NOT_TIME_VALID: 
     printf("This certificate or one of the certificates in the "
         "certificate chain is not time-valid.\n");
     break;
case CERT_TRUST_IS_REVOKED:
     printf("Trust for this certificate or one of the certificates "
         "in the certificate chain has been revoked.\n");
     break;
case CERT_TRUST_IS_NOT_SIGNATURE_VALID:
     printf("The certificate or one of the certificates in the "
         "certificate chain does not have a valid signature.\n");
     break;
case CERT_TRUST_IS_NOT_VALID_FOR_USAGE:
     printf("The certificate or certificate chain is not valid "
         "in its proposed usage.\n");
     break;
case CERT_TRUST_IS_UNTRUSTED_ROOT:
     printf("The certificate or certificate chain is based "
         "on an untrusted root.\n");
     break;
case CERT_TRUST_REVOCATION_STATUS_UNKNOWN:
     printf("The revocation status of the certificate or one of the"
         "certificates in the certificate chain is unknown.\n");
     break;
case CERT_TRUST_IS_CYCLIC :
     printf("One of the certificates in the chain was issued by a "
         "certification authority that the original certificate "
         "had certified.\n");
     break;
case CERT_TRUST_IS_PARTIAL_CHAIN: 
     printf("The certificate chain is not complete.\n");
     break;
case CERT_TRUST_CTL_IS_NOT_TIME_VALID: 
     printf("A CTL used to create this chain was not time-valid.\n");
     break;
case CERT_TRUST_CTL_IS_NOT_SIGNATURE_VALID: 
     printf("A CTL used to create this chain did not have a valid "
         "signature.\n");
     break;
case CERT_TRUST_CTL_IS_NOT_VALID_FOR_USAGE: 
     printf("A CTL used to create this chain is not valid for this "
         "usage.\n");
} // End switch

printf("\nInfo status for the chain:\n");
switch(pChainContext->TrustStatus.dwInfoStatus)
{
case 0:
     printf("No information status reported.\n");
     break;
case CERT_TRUST_HAS_EXACT_MATCH_ISSUER :
     printf("An exact match issuer certificate has been found for "
         "this certificate.\n");
     break;
case CERT_TRUST_HAS_KEY_MATCH_ISSUER: 
    printf("A key match issuer certificate has been found for this "
        "certificate.\n");
     break;
case CERT_TRUST_HAS_NAME_MATCH_ISSUER: 
    printf("A name match issuer certificate has been found for this "
        "certificate.\n");
     break;
case CERT_TRUST_IS_SELF_SIGNED:
     printf("This certificate is self-signed.\n");
     break;
case CERT_TRUST_IS_COMPLEX_CHAIN:
     printf("The certificate chain created is a complex chain.\n");
     break;
} // end switch

//-------------------------------------------------------------------
// Duplicate the original chain.
if(pDupContext = CertDuplicateCertificateChain(
       pChainContext ))
{
  printf("Duplicated the chain.\n");
}
else
{
  printf("Duplication failed.\n"); 
}
//-------------------------------------------------------------------
// Free both chains.

CertFreeCertificateChain(pDupContext);
printf("The duplicate chains is free.\n");
CertFreeCertificateChain(pChainContext);
printf("The Original chain is free.\n");
printf("\nPress Enter to continue.");
getchar();
} // end while loop 

printf("\nThere are no more certificates in the store. \n");

//---------------------------------------------------------
// Free the chain engine.

CertFreeCertificateChainEngine(hChainEngine);
printf("The chain engine has been released.\n");

// Free memory for pszNameString.
if(pszNameString)
     free(pszNameString);

printf("The demo program ran to completion without error.\n");


} // end main

//-------------------------------------------------------------------
// This example uses the function MyHandleError, a simple error
// handling function to print an error message and exit 
// the program. 
// For most applications, replace this function with one 
// that does more extensive error reporting.

void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program. \n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr, "Error number %x.\n", GetLastError());
    fprintf(stderr, "Program terminating. \n");
    exit(1);
} // end MyHandleError
```



 

 
