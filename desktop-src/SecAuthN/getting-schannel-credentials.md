---
description: L’exemple suivant montre comment un client standard peut obtenir des informations d’identification Schannel.
ms.assetid: 8f912af8-fd64-467a-b154-28c60cb14929
title: Obtention des informations d’identification Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2594b808387943cd2fc645a459dfbcd66ebc54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319342"
---
# <a name="getting-schannel-credentials"></a><span data-ttu-id="ba3d5-103">Obtention des informations d’identification Schannel</span><span class="sxs-lookup"><span data-stu-id="ba3d5-103">Getting Schannel Credentials</span></span>

<span data-ttu-id="ba3d5-104">L’exemple suivant montre comment un client standard peut obtenir des informations d’identification Schannel.</span><span class="sxs-lookup"><span data-stu-id="ba3d5-104">The following example demonstrates how a typical client would obtain Schannel credentials.</span></span> <span data-ttu-id="ba3d5-105">L’exemple suit la pratique recommandée consistant à utiliser les valeurs système par défaut pour les chiffrements et les niveaux de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="ba3d5-105">The example follows the recommended practice of using the system defaults for ciphers and cipher strengths.</span></span> <span data-ttu-id="ba3d5-106">Cela permet au package Schannel d’utiliser les algorithmes les plus puissants possibles pour sécuriser le canal.</span><span class="sxs-lookup"><span data-stu-id="ba3d5-106">This allows the Schannel package to use the strongest possible algorithms to secure the channel.</span></span>


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



<span data-ttu-id="ba3d5-107">La principale différence entre la demande côté client et côté serveur pour les informations d’identification est que le serveur doit fournir un certificat à l’aide d’une structure de [**\_ contexte de certificat**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) comme suit :</span><span class="sxs-lookup"><span data-stu-id="ba3d5-107">The primary difference between the client-side and server-side request for credentials is that the server must provide a certificate using a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structure as follows:</span></span>


```C++
  PCCERT_CONTEXT serverCert; // server-side certificate
  //-------------------------------------------------------
  // Get the server certificate. 

  if (! (serverCert = getServerCertificate())) return;

  // getServerCertificate is a placeholder function.
  credData.paCred = &serverCert;
```



<span data-ttu-id="ba3d5-108">L’exemple de fonction *getServerCertificate* est une fonction d’espace réservé pour cette activité spécifique à l’application.</span><span class="sxs-lookup"><span data-stu-id="ba3d5-108">The example function *getServerCertificate* is a placeholder function for this application-specific activity.</span></span> <span data-ttu-id="ba3d5-109">Pour obtenir un exemple d’implémentation de la fonction *getServerCertificate* , consultez [obtention d’un certificat](getting-a-certificate-for-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="ba3d5-109">For an example implementation of the *getServerCertificate* function, see [Getting a Certificate](getting-a-certificate-for-schannel.md).</span></span>

> [!Note]  
> <span data-ttu-id="ba3d5-110">Lorsque vous demandez des informations d’identification à utiliser par le serveur, modifiez le troisième paramètre (*fCredentialUse*) de la fonction [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) à partir de SECPKG \_ cred \_ sortant vers SECPKG \_ cred \_ entrant.</span><span class="sxs-lookup"><span data-stu-id="ba3d5-110">When requesting credentials to be used by the server, change the third (*fCredentialUse*) parameter of the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function from SECPKG\_CRED\_OUTBOUND to SECPKG\_CRED\_INBOUND.</span></span>

 

 

 
