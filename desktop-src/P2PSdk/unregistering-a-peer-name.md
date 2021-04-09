---
description: Lorsque vous annulez l’inscription d’un nom d’homologue, un nom inscrit est supprimé d’un Cloud PNRP (Peer Name Resolution Protocol).
ms.assetid: a451988e-7026-4b3c-a7a3-366f9886aa02
title: Annulation de l’inscription d’un nom d’homologue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd482cc9cfd8c32d7bc95edd00e866e2d87b7a55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952026"
---
# <a name="unregistering-a-peer-name"></a><span data-ttu-id="ac80e-103">Annulation de l’inscription d’un nom d’homologue</span><span class="sxs-lookup"><span data-stu-id="ac80e-103">Unregistering a Peer Name</span></span>

<span data-ttu-id="ac80e-104">Lorsque vous annulez l’inscription d’un nom d’homologue, un nom inscrit est supprimé d’un Cloud PNRP (Peer Name Resolution Protocol).</span><span class="sxs-lookup"><span data-stu-id="ac80e-104">When you unregister a peer name, a registered name is removed from a Peer Name Resolution Protocol (PNRP) cloud.</span></span>

## <a name="unregistering-a-peer-name"></a><span data-ttu-id="ac80e-105">Annulation de l’inscription d’un nom d’homologue</span><span class="sxs-lookup"><span data-stu-id="ac80e-105">Unregistering a Peer Name</span></span>

<span data-ttu-id="ac80e-106">Pour annuler l’inscription d’un nom d’homologue, appelez [**WSASetService**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="ac80e-106">To unregister a peer name, call [**WSASetService**](pnrp-and-wsasetservice.md).</span></span> <span data-ttu-id="ac80e-107">Le paramètre *essOperation* doit avoir la valeur **RNRSERVICE \_ Delete**.</span><span class="sxs-lookup"><span data-stu-id="ac80e-107">The *essOperation* parameter must have a value of **RNRSERVICE\_DELETE**.</span></span> <span data-ttu-id="ac80e-108">Utilisez les instructions des sections suivantes de cette rubrique pour effectuer les configurations requises pour les paramètres **WSASetService** et la structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="ac80e-108">Use the guidelines in the following sections of this topic to make the required configurations to the **WSASetService** parameters and the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>

## <a name="configuring-wsasetservice"></a><span data-ttu-id="ac80e-109">Configuration de WSASetService</span><span class="sxs-lookup"><span data-stu-id="ac80e-109">Configuring WSASetService</span></span>

<span data-ttu-id="ac80e-110">Quand une application appelle [**WSASetService**](pnrp-and-wsasetservice.md), les paramètres doivent être configurés conformément aux spécifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="ac80e-110">When an application calls [**WSASetService**](pnrp-and-wsasetservice.md), the parameters must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="ac80e-111">*essOperation* doit avoir la valeur **RNRSERVICE \_ Delete**.</span><span class="sxs-lookup"><span data-stu-id="ac80e-111">*essOperation* must have a value of **RNRSERVICE\_DELETE**.</span></span>
-   <span data-ttu-id="ac80e-112">*dwFlags* doit avoir la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="ac80e-112">*dwFlags* must be zero (0).</span></span>
-   <span data-ttu-id="ac80e-113">*lpqsRegInfo* doit pointer vers une structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) , qui doit être configurée à l’aide des instructions de la section suivante de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="ac80e-113">*lpqsRegInfo* must point to a [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure, which must be configured by using the guidelines in the following section of this topic.</span></span>

## <a name="configuring-wsaqueryset"></a><span data-ttu-id="ac80e-114">Configuration de WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="ac80e-114">Configuring WSAQUERYSET</span></span>

<span data-ttu-id="ac80e-115">La structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) doit être configurée conformément aux spécifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="ac80e-115">The [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="ac80e-116">**dwSize nul** doit spécifier la taille de la structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="ac80e-116">**dwSize** must specify the size the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>
-   <span data-ttu-id="ac80e-117">**lpszServiceInstanceName** doit pointer sur le nom de l’homologue en cours d’annulation d’inscription.</span><span class="sxs-lookup"><span data-stu-id="ac80e-117">**lpszServiceInstanceName** must point to the peer name that is being unregistered.</span></span>
-   <span data-ttu-id="ac80e-118">**lpBlob** doit pointer vers une structure [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="ac80e-118">**lpBlob** must point to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span>
-   <span data-ttu-id="ac80e-119">**lpcsaBuffer** doit pointer vers la liste d’adresses.</span><span class="sxs-lookup"><span data-stu-id="ac80e-119">**lpcsaBuffer** must point to the address list.</span></span>

> [!Note]  
> <span data-ttu-id="ac80e-120">Les membres restants sont décrits dans [**PNRP et WSASetService**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="ac80e-120">The remaining members are described in [**PNRP and WSASetService**](pnrp-and-wsasetservice.md).</span></span>

 

## <a name="an-example-of-unregistering-a-peer-name"></a><span data-ttu-id="ac80e-121">Exemple d’annulation de l’inscription d’un nom d’homologue</span><span class="sxs-lookup"><span data-stu-id="ac80e-121">An Example of Unregistering a Peer Name</span></span>

<span data-ttu-id="ac80e-122">L’extrait de code suivant vous montre comment annuler l’inscription d’un nom d’homologue en fournissant les informations correctes lors de l’appel de [**WSASetService**](pnrp-and-wsasetservice.md) à l’aide de la structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="ac80e-122">The following code snippet shows you how to unregister a peer name by providing the correct information when calling [**WSASetService**](pnrp-and-wsasetservice.md) using the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>


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



 

 



