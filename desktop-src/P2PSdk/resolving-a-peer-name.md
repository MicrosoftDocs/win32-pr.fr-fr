---
description: Cette rubrique décrit les méthodes permettant de résoudre un nom d’homologue à l’aide des API du fournisseur d’espace de noms PNRP.
ms.assetid: 7b21ec52-bc29-447e-9c46-34b9115574e0
title: Résolution d’un nom de pair
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e7f3aa59d3dc3be89f35ce9d6eca58bed1ce137
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867005"
---
# <a name="resolving-a-peer-name"></a><span data-ttu-id="6cae2-103">Résolution d’un nom de pair</span><span class="sxs-lookup"><span data-stu-id="6cae2-103">Resolving a Peer Name</span></span>

<span data-ttu-id="6cae2-104">Cette rubrique décrit les méthodes permettant de résoudre un nom d’homologue à l’aide des API du fournisseur d’espace de noms PNRP.</span><span class="sxs-lookup"><span data-stu-id="6cae2-104">This topic discusses methods for resolving a peer name using the PNRP Namespace Provider APIs.</span></span>

<span data-ttu-id="6cae2-105">Lorsque vous résolvez un nom d’homologue, vous devez fournir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6cae2-105">When you resolve a peer name, you must provide the following information:</span></span>

-   [<span data-ttu-id="6cae2-106">Nom de l’homologue</span><span class="sxs-lookup"><span data-stu-id="6cae2-106">Peer name</span></span>](peer-names.md)
-   [<span data-ttu-id="6cae2-107">Critères de résolution</span><span class="sxs-lookup"><span data-stu-id="6cae2-107">Resolve criteria</span></span>](/windows/desktop/api/Pnrpdef/ne-pnrpdef-pnrp_resolve_criteria)
-   <span data-ttu-id="6cae2-108">Nom du Cloud dans lequel résoudre le nom de l’homologue</span><span class="sxs-lookup"><span data-stu-id="6cae2-108">Cloud name in which to resolve the peer name</span></span>
-   <span data-ttu-id="6cae2-109">L’adresse IP, qui est facultative et est utilisée comme indicateur</span><span class="sxs-lookup"><span data-stu-id="6cae2-109">IP address, which is optional and is used as a hint</span></span>

## <a name="resolving-a-peer-name"></a><span data-ttu-id="6cae2-110">Résolution d’un nom de pair</span><span class="sxs-lookup"><span data-stu-id="6cae2-110">Resolving a Peer Name</span></span>

<span data-ttu-id="6cae2-111">Une fois que vous avez fourni un nom d’homologue, résolu les critères, le nom du Cloud et l’adresse IP facultative, les étapes suivantes doivent être effectuées pour terminer la résolution d’un nom d’homologue :</span><span class="sxs-lookup"><span data-stu-id="6cae2-111">After you provide a peer name, resolve criteria, cloud name, and the optional IP address, the following steps must be taken to complete the resolution of a peer name:</span></span>

-   <span data-ttu-id="6cae2-112">Appelez [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md) pour commencer le processus et retourner un descripteur.</span><span class="sxs-lookup"><span data-stu-id="6cae2-112">Call [**WSALookupServiceBegin**](pnrp-and-wsalookupservicebegin.md) to begin the process and return a handle.</span></span>
-   <span data-ttu-id="6cae2-113">Appelez [**WSALookupServiceNext**](pnrp-and-wsalookupservicenext.md) pour résoudre le nom de l’homologue.</span><span class="sxs-lookup"><span data-stu-id="6cae2-113">Call [**WSALookupServiceNext**](pnrp-and-wsalookupservicenext.md) to resolve the peer name.</span></span>
-   <span data-ttu-id="6cae2-114">Appelez [**WSALookupServiceEnd**](pnrp-and-wsalookupserviceend.md) pour terminer le processus.</span><span class="sxs-lookup"><span data-stu-id="6cae2-114">Call [**WSALookupServiceEnd**](pnrp-and-wsalookupserviceend.md) to complete the process.</span></span>

## <a name="an-example-of-resolving-a-peer-name"></a><span data-ttu-id="6cae2-115">Exemple de résolution d’un nom d’homologue</span><span class="sxs-lookup"><span data-stu-id="6cae2-115">An Example of Resolving a Peer Name</span></span>

<span data-ttu-id="6cae2-116">L’extrait de code suivant montre comment résoudre un nom d’homologue.</span><span class="sxs-lookup"><span data-stu-id="6cae2-116">The following code snippet shows you how to resolve a peer name.</span></span> <span data-ttu-id="6cae2-117">Une hypothèse dans l’exemple indique qu’une adresse TCP/IP sera renvoyée.</span><span class="sxs-lookup"><span data-stu-id="6cae2-117">There is an assumption in the sample that a TCP/IP address will be returned.</span></span>


```C++
#define UNICODE
#include <initguid.h>
#include <p2p.h>

#pragma comment( lib, "ws2_32.lib")

// Function: PnrpResolve
//
// Purpose:  Resolve the given name within a PNRP cloud
//
// Arguments:
//   pwzName  : name to resolve in PNRP, generally the graph id
//   pwzCloud : name of cloud to resolve in, NULL = global cloud
//   pAddr    : pointer to result buffer
//
// Returns:  HRESULT
//
HRESULT PnrpResolve(PWSTR pwzName, PWSTR pwzCloud, SOCKADDR_IN6* pAddr)
{
    HRESULT         hr = S_OK;
    PNRPINFO        pnrpInfo = {0};
    BLOB            blPnrpData = {0};
    WSAQUERYSET     querySet = {0};
    WSAQUERYSET*    pResults = NULL;
    WSAQUERYSET     tempResultSet = {0};
    HANDLE          hLookup = NULL;
    BOOL            fFound = FALSE;
    DWORD           dwError;
    INT             iRet;
    ULONG           i;
    DWORD           dwSize = 0;

    //
    // fill in the WSAQUERYSET
    //
    pnrpInfo.dwSize = sizeof(pnrpInfo);
    pnrpInfo.nMaxResolve = 1;
    pnrpInfo.dwTimeout = 30;
    pnrpInfo.enResolveCriteria = PNRP_RESOLVE_CRITERIA_NON_CURRENT_PROCESS_PEER_NAME;

    blPnrpData.cbSize = sizeof(pnrpInfo);
    blPnrpData.pBlobData = (BYTE*)&pnrpInfo;

    querySet.dwSize = sizeof(querySet);
    querySet.dwNameSpace = NS_PNRPNAME;
    querySet.lpServiceClassId = (LPGUID)&SVCID_PNRPNAME;
    querySet.lpszServiceInstanceName = pwzName;
    querySet.lpszContext = pwzCloud;
    querySet.lpBlob = &blPnrpData;
    // start resolve
    iRet = WSALookupServiceBegin(
            &querySet,
            LUP_RETURN_NAME | LUP_RETURN_ADDR | LUP_RETURN_COMMENT,
            &hLookup);


    if (iRet != 0)
    {
        hr = HRESULT_FROM_WIN32(WSAGetLastError());
    }

    if (SUCCEEDED(hr))
    {
        dwSize = sizeof(tempResultSet);

        // retrieve the required size
        iRet = WSALookupServiceNext(hLookup, 0, &dwSize, &tempResultSet);
        dwError = WSAGetLastError();

        if (dwError == WSAEFAULT)
        {
            // allocate space for the results
            pResults = (WSAQUERYSET*)malloc(dwSize);
            if (pResults == NULL)
            {
                hr = E_OUTOFMEMORY;
            }
        }
        else
        {
            hr = HRESULT_FROM_WIN32(dwError);
        }
    }

    if (SUCCEEDED(hr))
    {
        // retrieve the addresses
        iRet = WSALookupServiceNext(hLookup, 0, &dwSize, pResults);
        if (iRet != 0)
        {
            hr = HRESULT_FROM_WIN32(WSAGetLastError());
        }
    }

    if (SUCCEEDED(hr))
    {
        // return the first IPv6 address found
        for (i = 0; i < pResults->dwNumberOfCsAddrs; i++)
        {
            if (pResults->lpcsaBuffer[i].iProtocol == IPPROTO_TCP &&
                pResults->lpcsaBuffer[i].RemoteAddr.iSockaddrLength == sizeof(SOCKADDR_IN6))
            {
                CopyMemory(pAddr, pResults->lpcsaBuffer[i].RemoteAddr.lpSockaddr, sizeof(SOCKADDR_IN6));
                fFound = TRUE;
                break;
            }
        }

        if (!fFound)
        {
            // unable to find an IPv6 address
            hr = HRESULT_FROM_WIN32(WSA_E_NO_MORE);
        }
    }

    if (hLookup != NULL)
    {
        WSALookupServiceEnd(hLookup);
    }

    if (pResults != NULL)
    {
        free(pResults);
    }

    return hr;
}
```



 

 



