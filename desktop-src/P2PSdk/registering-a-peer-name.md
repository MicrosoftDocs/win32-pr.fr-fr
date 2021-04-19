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
# <a name="registering-a-peer-name"></a><span data-ttu-id="5d613-103">Inscription d’un nom d’homologue</span><span class="sxs-lookup"><span data-stu-id="5d613-103">Registering a Peer Name</span></span>

<span data-ttu-id="5d613-104">Pour inscrire un nom d’homologue, une application doit fournir les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="5d613-104">To register a peer name, an application must provide the following information:</span></span>

-   <span data-ttu-id="5d613-105">Liste d’adresses IP</span><span class="sxs-lookup"><span data-stu-id="5d613-105">IP address list</span></span>
-   [<span data-ttu-id="5d613-106">Identité de l’homologue</span><span class="sxs-lookup"><span data-stu-id="5d613-106">Peer identity</span></span>](creating-a-peer-identity.md)
-   [<span data-ttu-id="5d613-107">Nom de l’homologue</span><span class="sxs-lookup"><span data-stu-id="5d613-107">Peer name</span></span>](peer-names.md)

<span data-ttu-id="5d613-108">Si un nom d’homologue n’est pas sécurisé, une identité est facultative.</span><span class="sxs-lookup"><span data-stu-id="5d613-108">If a peer name is unsecured, an identity is optional.</span></span> <span data-ttu-id="5d613-109">Si une identité d’homologue est spécifiée comme étant **null**, le protocole PNRP (Peer Name Resolution Protocol) utilise une identité d’homologue interne par défaut.</span><span class="sxs-lookup"><span data-stu-id="5d613-109">If a peer identity is specified as **NULL**, the Peer Name Resolution Protocol (PNRP) uses an internal, default peer identity.</span></span>

## <a name="registering-a-peer-name"></a><span data-ttu-id="5d613-110">Inscription d’un nom d’homologue</span><span class="sxs-lookup"><span data-stu-id="5d613-110">Registering a Peer Name</span></span>

<span data-ttu-id="5d613-111">Une fois que la liste d’adresses IP, l’identité de l’homologue et le nom de l’homologue sont identifiés, l’application peut inscrire un nom d’homologue en appelant [**WSASetService**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="5d613-111">After the IP address list, peer identity, and peer name are identified, the application can register a peer name by calling [**WSASetService**](pnrp-and-wsasetservice.md).</span></span> <span data-ttu-id="5d613-112">Utilisez les instructions des sections suivantes de cette rubrique pour effectuer les configurations requises pour les paramètres **WSASetService** et la structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="5d613-112">Use the guidelines in the following sections of this topic to make the required configurations to the **WSASetService** parameters and the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>

### <a name="configuring-wsasetservice"></a><span data-ttu-id="5d613-113">Configuration de WSASetService</span><span class="sxs-lookup"><span data-stu-id="5d613-113">Configuring WSASetService</span></span>

<span data-ttu-id="5d613-114">Quand une application appelle [**WSASetService**](pnrp-and-wsasetservice.md), les paramètres doivent être configurés conformément aux spécifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="5d613-114">When an application calls [**WSASetService**](pnrp-and-wsasetservice.md), the parameters must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="5d613-115">*essOperation* doit avoir la valeur **RNRSERVICE \_ Register**.</span><span class="sxs-lookup"><span data-stu-id="5d613-115">*essOperation* must have a value of **RNRSERVICE\_REGISTER**.</span></span>
-   <span data-ttu-id="5d613-116">*dwFlags* doit avoir la valeur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="5d613-116">*dwFlags* must be zero (0).</span></span>
-   <span data-ttu-id="5d613-117">*lpqsRegInfo* doit pointer vers une structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) , qui doit être configurée à l’aide des instructions de la section **configuration de WSAQUERYSET** suivante de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="5d613-117">*lpqsRegInfo* must point to a [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure, which must be configured by using the guidelines in the following **Configuring WSAQUERYSET** section of this topic.</span></span>

### <a name="configuring-wsaqueryset"></a><span data-ttu-id="5d613-118">Configuration de WSAQUERYSET</span><span class="sxs-lookup"><span data-stu-id="5d613-118">Configuring WSAQUERYSET</span></span>

<span data-ttu-id="5d613-119">La structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) doit être configurée conformément aux spécifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="5d613-119">The [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure must be configured according to the following specifications:</span></span>

-   <span data-ttu-id="5d613-120">**dwSize nul** doit spécifier la taille de la structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="5d613-120">**dwSize** must specify the size the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>
-   <span data-ttu-id="5d613-121">**lpszServiceInstanceName** doit pointer vers le nom d’homologue en cours d’inscription.</span><span class="sxs-lookup"><span data-stu-id="5d613-121">**lpszServiceInstanceName** must point to the peer name that is being registered.</span></span>
-   <span data-ttu-id="5d613-122">**lpBlob** doit pointer vers une structure [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) .</span><span class="sxs-lookup"><span data-stu-id="5d613-122">**lpBlob** must point to a [**PNRPINFO**](/windows/desktop/api/Pnrpns/ns-pnrpns-pnrpinfo_v1) structure.</span></span>
-   <span data-ttu-id="5d613-123">**lpcsaBuffer** doit pointer vers la liste d’adresses.</span><span class="sxs-lookup"><span data-stu-id="5d613-123">**lpcsaBuffer** must point to the address list.</span></span>

> [!Note]  
> <span data-ttu-id="5d613-124">Les membres restants sont décrits dans [**PNRP et WSASetService**](pnrp-and-wsasetservice.md).</span><span class="sxs-lookup"><span data-stu-id="5d613-124">The remaining members are described in [**PNRP and WSASetService**](pnrp-and-wsasetservice.md).</span></span>

 

<span data-ttu-id="5d613-125">Après l’inscription d’un nom d’homologue, les informations sont disponibles pour l’infrastructure homologue.</span><span class="sxs-lookup"><span data-stu-id="5d613-125">After a peer name is registered, the information is available to the Peer Infrastructure.</span></span> <span data-ttu-id="5d613-126">Toutefois, il existe un délai entre le moment de l’inscription et la propagation des informations d’inscription à d’autres nœuds.</span><span class="sxs-lookup"><span data-stu-id="5d613-126">However, there is a delay between the registration time and the propagation of the registration information to other nodes.</span></span> <span data-ttu-id="5d613-127">Pendant ce temps, les autres nœuds peuvent ne pas être en mesure de résoudre le pair nouvellement inscrit.</span><span class="sxs-lookup"><span data-stu-id="5d613-127">During that time, other nodes may not be able to resolve the newly registered peer.</span></span>

## <a name="example-of-registering-a-peer-name"></a><span data-ttu-id="5d613-128">Exemple d’inscription d’un nom d’homologue</span><span class="sxs-lookup"><span data-stu-id="5d613-128">Example of Registering a Peer Name</span></span>

<span data-ttu-id="5d613-129">L’extrait de code suivant vous montre comment inscrire un nom d’homologue en fournissant les informations correctes lors de l’appel de [**WSASetService**](pnrp-and-wsasetservice.md) à l’aide de la structure [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) .</span><span class="sxs-lookup"><span data-stu-id="5d613-129">The following code snippet shows you how to register a peer name by providing the correct information when calling [**WSASetService**](pnrp-and-wsasetservice.md) using the [**WSAQUERYSET**](pnrp-and-wsaqueryset.md) structure.</span></span>


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



 

 



