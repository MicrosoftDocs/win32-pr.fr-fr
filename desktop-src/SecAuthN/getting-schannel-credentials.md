---
description: L’exemple suivant montre comment un client standard peut obtenir des informations d’identification Schannel.
ms.assetid: 8f912af8-fd64-467a-b154-28c60cb14929
title: Obtention des informations d’identification Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4e088e0e0e0cb2edbc6a6551669cf4d8c5b8b3d2eb8cad38699e83001e5350
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623179"
---
# <a name="getting-schannel-credentials"></a>Obtention des informations d’identification Schannel

L’exemple suivant montre comment un client standard peut obtenir des informations d’identification Schannel. L’exemple suit la pratique recommandée consistant à utiliser les valeurs système par défaut pour les chiffrements et les niveaux de chiffrement. Cela permet au package Schannel d’utiliser les algorithmes les plus puissants possibles pour sécuriser le canal.


```C++
#include <windows.h>
#include <ntsecapi.h>
#include <stdio.h>
#include <sspi.h>
#include <schnlsp.h>

void getSchannelClientHandle(PCredHandle ppClientCred)
{
  SECURITY_STATUS SecStatus;
  TimeStamp Lifetime;
  CredHandle hCred;
  SCHANNEL_CRED credData;

  ZeroMemory(&credData, sizeof(credData));
  credData.dwVersion = SCHANNEL_CRED_VERSION;

  //-------------------------------------------------------
  // Specify the TLS V1.0 (client-side) security protocol.
  credData.grbitEnabledProtocols = SP_PROT_TLS1_CLIENT; 
    
  SecStatus = AcquireCredentialsHandle (
       NULL,                  // default principal
       UNISP_NAME,            // name of the SSP
       SECPKG_CRED_OUTBOUND,  // client will use the credentials
       NULL,                  // use the current LOGON id
       &credData,             // protocol-specific data
       NULL,                  // default
       NULL,                  // default
       &hCred,                // receives the credential handle
       &Lifetime              // receives the credential time limit
  );
  printf("Client credentials status: 0x%x\n", SecStatus);
  // Return the handle to the caller.
  if(ppClientCred != NULL)
      *ppClientCred = hCred;

  return;
  //-------------------------------------------------------
  // When you have finished with this handle,
  // free the handle by calling the 
  // FreeCredentialsHandle function.
}
```



La principale différence entre la demande côté client et côté serveur pour les informations d’identification est que le serveur doit fournir un certificat à l’aide d’une structure de [**\_ contexte de certificat**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) comme suit :


```C++
  PCCERT_CONTEXT serverCert; // server-side certificate
  //-------------------------------------------------------
  // Get the server certificate. 

  if (! (serverCert = getServerCertificate())) return;

  // getServerCertificate is a placeholder function.
  credData.paCred = &serverCert;
```



L’exemple de fonction *getServerCertificate* est une fonction d’espace réservé pour cette activité spécifique à l’application. Pour obtenir un exemple d’implémentation de la fonction *getServerCertificate* , consultez [obtention d’un certificat](getting-a-certificate-for-schannel.md).

> [!Note]  
> Lorsque vous demandez des informations d’identification à utiliser par le serveur, modifiez le troisième paramètre (*fCredentialUse*) de la fonction [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) à partir de SECPKG \_ cred \_ sortant vers SECPKG \_ cred \_ entrant.

 

 

 
