---
description: Lorsque vous annulez l’inscription d’un nom d’homologue, un nom inscrit est supprimé d’un Cloud PNRP (Peer Name Resolution Protocol).
ms.assetid: a451988e-7026-4b3c-a7a3-366f9886aa02
title: Annulation de l’inscription d’un nom d’homologue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ee0bd03e881f93321c31dfccd03cc71459b323f1ed356a88f829489c578a80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675009"
---
# <a name="unregistering-a-peer-name"></a>Annulation de l’inscription d’un nom d’homologue

Lorsque vous annulez l’inscription d’un nom d’homologue, un nom inscrit est supprimé d’un Cloud PNRP (Peer Name Resolution Protocol).

## <a name="unregistering-a-peer-name"></a>Annulation de l’inscription d’un nom d’homologue

Pour annuler l’inscription d’un nom d’homologue, appelez [**WSASetService**](pnrp-and-wsasetservice.md). Le paramètre *essOperation* doit avoir la valeur **RNRSERVICE \_ Delete**. Utilisez les instructions des sections suivantes de cette rubrique pour effectuer les configurations requises pour les paramètres **WSASetService** et la structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .

## <a name="configuring-wsasetservice"></a>Configuration de WSASetService

Quand une application appelle [**WSASetService**](pnrp-and-wsasetservice.md), les paramètres doivent être configurés conformément aux spécifications suivantes :

-   *essOperation* doit avoir la valeur **RNRSERVICE \_ Delete**.
-   *dwFlags* doit avoir la valeur zéro (0).
-   *lpqsRegInfo* doit pointer vers une structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) , qui doit être configurée à l’aide des instructions de la section suivante de cette rubrique.

## <a name="configuring-wsaqueryset"></a>Configuration de WSAQUERYSET

La structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) doit être configurée conformément aux spécifications suivantes :

-   **dwSize nul** doit spécifier la taille de la structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .
-   **lpszServiceInstanceName** doit pointer sur le nom de l’homologue en cours d’annulation d’inscription.
-   **lpBlob** doit pointer vers une structure [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .
-   **lpcsaBuffer** doit pointer vers la liste d’adresses.

> [!Note]  
> Les membres restants sont décrits dans [**PNRP et WSASetService**](pnrp-and-wsasetservice.md).

 

## <a name="an-example-of-unregistering-a-peer-name"></a>Exemple d’annulation de l’inscription d’un nom d’homologue

L’extrait de code suivant vous montre comment annuler l’inscription d’un nom d’homologue en fournissant les informations correctes lors de l’appel de [**WSASetService**](pnrp-and-wsasetservice.md) à l’aide de la structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment(lib, "ws2_32.lib")

//-------------------------------------------------------------------------
// Function: PnrpUnregister
//
// Purpose:  Unregister the given name from a PNRP cloud
//
// Arguments:
//   pwzIdentity : identity string originally used to register the name
//   pwzName     : name to unregister from PNRP
//   pwzCloud    : name of the cloud to unregister from, NULL = global cloud
//
// Returns:  HRESULT
//
HRESULT PnrpUnregister(PWSTR pwzIdentity, PWSTR pwzName, PWSTR pwzCloud)
{
    HRESULT         hr = S_OK;
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    INT             iRet;

    //
    // build the WSAQUERYSET required to unregister
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.dwLifetime = 60 * 60 * 8; // 8 hours
    pnrpInfo.lpwszIdentity = pwzIdentity;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpBlob = &blPnrpData;

    // unregister the name with PNRP
    iRet = WSASetService(&querySet, RNRSERVICE_DELETE, 0);
    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }

    return hr;
}
```



 

 



