---
description: NSPGetServiceClassInfo
ms.assetid: 6fbe9c0c-ac1f-4f2b-a542-eae2195b1335
title: Fonctions d’assistance dans le SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e687529bf1ede1598225708cf288e49bb7e9b5c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536330"
---
# <a name="helper-functions-in-the-spi"></a><span data-ttu-id="33baf-103">Fonctions d’assistance dans le SPI</span><span class="sxs-lookup"><span data-stu-id="33baf-103">Helper Functions in the SPI</span></span>

-   [<span data-ttu-id="33baf-104">**NSPGetServiceClassInfo**</span><span class="sxs-lookup"><span data-stu-id="33baf-104">**NSPGetServiceClassInfo**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)

<span data-ttu-id="33baf-105">La fonction [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) récupère les informations de schéma de la classe de service qui ont été conservées par un fournisseur d’espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="33baf-105">The [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) function retrieves service class schema information that has been retained by a namespace provider.</span></span> <span data-ttu-id="33baf-106">Il est également utilisé par la DLL Windows Sockets 2 dans son implémentation de [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida).</span><span class="sxs-lookup"><span data-stu-id="33baf-106">It is also used by the Windows Sockets 2 DLL in its implementation of [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida).</span></span>

<span data-ttu-id="33baf-107">Les macros suivantes définies dans le fichier d’en-tête *Svcguid. h* et peuvent faciliter le mappage entre les classes de service bien connues et ces espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="33baf-107">The following macros defined in the *Svcguid.h* header file and can aid in mapping between well known service classes and these namespaces.</span></span>

| <span data-ttu-id="33baf-108">Nom de macro</span><span class="sxs-lookup"><span data-stu-id="33baf-108">Macro name</span></span>                                                                              | <span data-ttu-id="33baf-109">Description</span><span class="sxs-lookup"><span data-stu-id="33baf-109">Description</span></span>                                                                                                                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33baf-110">**SVCID \_ TCP (port)**</span><span class="sxs-lookup"><span data-stu-id="33baf-110">**SVCID\_TCP(Port)**</span></span><br/> <span data-ttu-id="33baf-111">**\_UDP SVCID (port)**</span><span class="sxs-lookup"><span data-stu-id="33baf-111">**SVCID\_UDP(Port)**</span></span><br/>                         | <span data-ttu-id="33baf-112">À partir d’un port TCP ou UDP pour le protocole Internet, retourne le GUID.</span><span class="sxs-lookup"><span data-stu-id="33baf-112">Given a TCP or UDP port for the Internet protocol, returns the GUID.</span></span>                                                                               |
| <span data-ttu-id="33baf-113">**EST \_ SVCID \_ TCP (Guid)**</span><span class="sxs-lookup"><span data-stu-id="33baf-113">**IS\_SVCID\_TCP(GUID)**</span></span><br/> <span data-ttu-id="33baf-114">**EST \_ SVCID \_ UDP (Guid)**</span><span class="sxs-lookup"><span data-stu-id="33baf-114">**IS\_SVCID\_UDP(GUID)**</span></span><br/>                 | <span data-ttu-id="33baf-115">Retourne la **valeur true** si le GUID pour TCP ou UDP se trouve dans la plage autorisée.</span><span class="sxs-lookup"><span data-stu-id="33baf-115">Returns **TRUE** if the GUID for TCP or UDP is within the allowable range.</span></span>                                                                         |
| <span data-ttu-id="33baf-116">**PORT \_ de \_ SVCID \_ TCP (Guid)**</span><span class="sxs-lookup"><span data-stu-id="33baf-116">**PORT\_FROM\_SVCID\_TCP(GUID)**</span></span><br/> <span data-ttu-id="33baf-117">**PORT \_ du \_ SVCID \_ UDP (Guid)**</span><span class="sxs-lookup"><span data-stu-id="33baf-117">**PORT\_FROM\_SVCID\_UDP(GUID)**</span></span><br/> | <span data-ttu-id="33baf-118">Retourne le port TCP ou UDP associé au GUID.</span><span class="sxs-lookup"><span data-stu-id="33baf-118">Returns the TCP or UDP port associated with the GUID.</span></span>                                                                                              |
| <span data-ttu-id="33baf-119">**SVCID \_ NetWare (sapid)**</span><span class="sxs-lookup"><span data-stu-id="33baf-119">**SVCID\_NETWARE(SAPID)**</span></span><br/>                                                    | <span data-ttu-id="33baf-120">Compte tenu de l’identificateur SAP (Service Advertising Protocol), retourne le GUID.</span><span class="sxs-lookup"><span data-stu-id="33baf-120">Given the Service Advertising Protocol (SAP) identifier, returns the GUID.</span></span> <span data-ttu-id="33baf-121">Cette macro est utilisée avec l’espace de noms SAP au sein d’un environnement NetWare.</span><span class="sxs-lookup"><span data-stu-id="33baf-121">This macro is used with the SAP namespace within a NetWare environment.</span></span> |
| <span data-ttu-id="33baf-122">**SAPId \_ à partir de \_ SVCID \_ NetWare (Guid)**</span><span class="sxs-lookup"><span data-stu-id="33baf-122">**SAPID\_FROM\_SVCID\_NETWARE(GUID)**</span></span><br/>                                        | <span data-ttu-id="33baf-123">Retourne l’identificateur SAP SAP associé au GUID.</span><span class="sxs-lookup"><span data-stu-id="33baf-123">Returns the NetWare SAP identifier associated with the GUID.</span></span> <span data-ttu-id="33baf-124">Cette macro est utilisée avec l’espace de noms SAP au sein d’un environnement NetWare.</span><span class="sxs-lookup"><span data-stu-id="33baf-124">This macro is used with the SAP namespace within a NetWare environment.</span></span>               |
| <span data-ttu-id="33baf-125">**IS \_ SVCID \_ NetWare (Guid)**</span><span class="sxs-lookup"><span data-stu-id="33baf-125">**IS\_SVCID\_NETWARE(GUID)**</span></span><br/>                                                 | <span data-ttu-id="33baf-126">Retourne la **valeur true** si le GUID pour NetWare se trouve dans la plage autorisée.</span><span class="sxs-lookup"><span data-stu-id="33baf-126">Returns **TRUE** if the GUID for NetWare is within the allowable range.</span></span> <span data-ttu-id="33baf-127">Cette macro est utilisée avec l’espace de noms SAP au sein d’un environnement NetWare.</span><span class="sxs-lookup"><span data-stu-id="33baf-127">This macro is used with the SAP namespace within a NetWare environment.</span></span>    |



 

> [!Note]  
> <span data-ttu-id="33baf-128">Le fichier d’en-tête *Svcguid. h* n’est pas automatiquement inclus dans le fichier d’en-tête *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="33baf-128">The *Svcguid.h* header file is not automatically included by the *Winsock2.h* header file.</span></span>

 

 

 




