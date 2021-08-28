---
description: Une autorité de certification d’entreprise publie des certificats émis sur le Active Directory ; une autorité de certification autonome peut également publier des certificats émis sur le Active Directory.
ms.assetid: 6449e116-1671-4120-a012-278ab9ae9925
title: Récupération d’un certificat émis à partir de Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 969d9930d24cafee9b7bfdd6532ecdf5b830970a87cb2ae43dcbcbc1b16517cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900564"
---
# <a name="retrieving-an-issued-certificate-from-active-directory"></a>Récupération d’un certificat émis à partir de Active Directory

Une [*autorité de certification*](../secgloss/c-gly.md) d’entreprise publie des [*certificats*](../secgloss/c-gly.md) émis sur le Active Directory ; une autorité de certification autonome peut également publier des certificats émis sur le Active Directory. L’exemple suivant montre comment acquérir un [*contexte de certificat*](../secgloss/c-gly.md) pour un certificat stocké dans Active Directory. Une fois le contexte de certificat acquis, vous pouvez récupérer le contenu du certificat ou effectuer des opérations de certificat à l’aide des fonctions CryptoAPI.

L’exemple suivant montre comment récupérer un certificat à partir de Active Directory.


```C++
//  Copyright (C) Microsoft.  All rights reserved.
//  Retrieve a user certificate from Active Directory.
//
//  This example uses CryptoAPI calls to retrieve 
//  a certificate previously published to Active Directory
//  by Microsoft Certificate Services.
//  Ensure Crypt32.lib and Secur32.lib are part of link libraries.
#pragma comment(lib, "crypt32.lib")

#define SECURITY_WIN32 1
#define UNICODE 1

#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#include <strsafe.h>
#include <security.h>

#define MAXBUFF 512

void __cdecl main()
{
    HCERTSTORE     hStore=NULL;

    PCCERT_CONTEXT pCertCtx = NULL;

    WCHAR          wszDN[MAXBUFF];
    ULONG          cchDN = MAXBUFF;
    
    WCHAR          wszQuery[MAXBUFF * 2];
    ULONG          cchQuery = MAXBUFF * 2;

    //  Determine the name of the user whose certificate is being
    //  retrieved. This value can be constructed by other means,
    //  but this example will use GetUserNameEx.
    if (!GetUserNameEx(NameFullyQualifiedDN,
                       wszDN,
                       &cchDN))
    {
        printf("Failed GetUserNameEx: %x\n",
               GetLastError());
        exit(1);
    }

    //  Build the LDAP query string.
    if (S_OK != StringCchPrintf(wszQuery,
                    cchQuery,
                    L"ldap:///%s?%s",
                    wszDN,
                    L"userCertificate"))
    {
        printf("Failed StringCchPrintf\n");
        exit(1);

    }

    //  Open the Active Directory certificate store.
    hStore = CertOpenStore(CERT_STORE_PROV_LDAP,
                           0,
                           0,
                           CERT_STORE_READONLY_FLAG,
                           wszQuery);
    if ( NULL == hStore)
    {
        printf("Failed CertOpenStore - %x\n", GetLastError());
        exit(1);
    }

    //  Retrieve a certificate context from this opened store.
    //  Here, retrieve any existing certificate stored for 
    //  the user in Active Directory.
    //  If more than one certificate exists, consult
    //  CertFindCertificateInStore documentation for search 
    //  types and calling instructions.
    pCertCtx = CertFindCertificateInStore(hStore,
                   X509_ASN_ENCODING | PKCS_7_ASN_ENCODING,
                   0,
                   CERT_FIND_ANY,
                   NULL,
                   NULL);
    if (NULL == pCertCtx)
    {
        DWORD dwErr;
        dwErr = GetLastError();
        if (CRYPT_E_NOT_FOUND == dwErr)
            printf("User does not have certificate"
                   "in Active Directory\n");
        else
            printf("Failed CertFindCertificateInStore - %x\n",
                   dwErr);
    }
    else
    {
        //  Use the certificate context as needed.
        //  Here, display the serial number.
        DWORD dwLen, i;
        dwLen = pCertCtx->pCertInfo->SerialNumber.cbData;
        //  The serial number bytes are stored
        //  least significant byte first.
        printf("Serial number: ");
        for (i = dwLen-1; i != MAXDWORD; i--)
            printf("%02x",
                   *(pCertCtx->pCertInfo->SerialNumber.pbData + i));
        printf("\n");
        //  Free the certificate context.
        CertFreeCertificateContext(pCertCtx);
    }

    //  Close the certificate store.
    CertCloseStore(hStore, 0);

}
```



 

 
