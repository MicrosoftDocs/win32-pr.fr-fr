---
description: 'Pour inscrire un nom d’homologue, une application doit fournir les informations suivantes : adresse IP listPeer identityPeer nameIf un nom d’homologue n’est pas sécurisé, une identité est facultative.'
ms.assetid: 4de87146-3ea1-4019-9d3f-59de296083ae
title: Inscription d’un nom d’homologue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b0944c4a41c02ff221aa1cc6a0b84ed881a9453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523319"
---
# <a name="registering-a-peer-name"></a>Inscription d’un nom d’homologue

Pour inscrire un nom d’homologue, une application doit fournir les informations suivantes :

-   Liste d’adresses IP
-   [Identité de l’homologue](creating-a-peer-identity.md)
-   [Nom de l’homologue](peer-names.md)

Si un nom d’homologue n’est pas sécurisé, une identité est facultative. Si une identité d’homologue est spécifiée comme étant **null**, le protocole PNRP (Peer Name Resolution Protocol) utilise une identité d’homologue interne par défaut.

## <a name="registering-a-peer-name"></a>Inscription d’un nom d’homologue

Une fois que la liste d’adresses IP, l’identité de l’homologue et le nom de l’homologue sont identifiés, l’application peut inscrire un nom d’homologue en appelant [**WSASetService**](pnrp-and-wsasetservice.md). Utilisez les instructions des sections suivantes de cette rubrique pour effectuer les configurations requises pour les paramètres **WSASetService** et la structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .

### <a name="configuring-wsasetservice"></a>Configuration de WSASetService

Quand une application appelle [**WSASetService**](pnrp-and-wsasetservice.md), les paramètres doivent être configurés conformément aux spécifications suivantes :

-   *essOperation* doit avoir la valeur **RNRSERVICE \_ Register**.
-   *dwFlags* doit avoir la valeur zéro (0).
-   *lpqsRegInfo* doit pointer vers une structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) , qui doit être configurée à l’aide des instructions de la section **configuration de WSAQUERYSET** suivante de cette rubrique.

### <a name="configuring-wsaqueryset"></a>Configuration de WSAQUERYSET

La structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) doit être configurée conformément aux spécifications suivantes :

-   **dwSize nul** doit spécifier la taille de la structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .
-   **lpszServiceInstanceName** doit pointer vers le nom d’homologue en cours d’inscription.
-   **lpBlob** doit pointer vers une structure [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .
-   **lpcsaBuffer** doit pointer vers la liste d’adresses.

> [!Note]  
> Les membres restants sont décrits dans [**PNRP et WSASetService**](pnrp-and-wsasetservice.md).

 

Après l’inscription d’un nom d’homologue, les informations sont disponibles pour l’infrastructure homologue. Toutefois, il existe un délai entre le moment de l’inscription et la propagation des informations d’inscription à d’autres nœuds. Pendant ce temps, les autres nœuds peuvent ne pas être en mesure de résoudre le pair nouvellement inscrit.

## <a name="example-of-registering-a-peer-name"></a>Exemple d’inscription d’un nom d’homologue

L’extrait de code suivant vous montre comment inscrire un nom d’homologue en fournissant les informations correctes lors de l’appel de [**WSASetService**](pnrp-and-wsasetservice.md) à l’aide de la structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment(lib, "ws2_32.lib")

//-------------------------------------------------------------------------
// Function: PnrpRegister
//
// Purpose:  Register the given name in the PNRP cloud
//
// Arguments:
//   pwzIdentity : identity string created using PeerIdentityCreate
//   pwzName     : name to register in PNRP
//   pwzCloud    : name of the cloud to register in, NULL = global cloud
//   pNodeInfo   : local node info returned from 

//
// Returns:  HRESULT
//
HRESULT PnrpRegister(PWSTR pwzIdentity, PWSTR pwzName, PWSTR pwzCloud, SOCKADDR_IN6* pAddress)
{
    HRESULT         hr = S_OK;
    CSADDR_INFO     csaAddr = {0};
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    INT             iRet;

    //
    // fill a CSADDR_INFO structure from the address
    //
    csaAddr.iProtocol = IPPROTO_TCP;
    csaAddr.iSocketType = SOCK_STREAM;
    csaAddr.LocalAddr.iSockaddrLength = sizeof(SOCKADDR_IN6);
    csaAddr.LocalAddr.lpSockaddr = (LPSOCKADDR)pAddress; 

    //
    // build the WSAQUERYSET required to register
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.dwLifetime = 60 * 60 * 8; //8 hours
    pnrpInfo.lpwszIdentity = pwzIdentity;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.dwNumberOfCsAddrs = 1; // one address
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpszComment = L"SomeComment";
    querySet.lpcsaBuffer = &csaAddr;
    querySet.lpBlob = &blPnrpData;

    // register the name with PNRP
    iRet = WSASetService(&querySet, RNRSERVICE_REGISTER, 0);
    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }
    
    return hr;
}
```



 

 



