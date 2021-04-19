---
description: Événement de modification du catalogue Winsock pour une opération de désactivation du fournisseur de services en couche (LSP).
ms.assetid: 6BCEECB1-92AD-47D8-952B-D0FD2A78EB45
title: Événement WINSOCK_WS2HELP_LSP_DISABLE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_DISABLE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6d785bfbd96d35717be7bbf76dab8f28f41c9fc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518812"
---
# <a name="winsock_ws2help_lsp_disable-event"></a><span data-ttu-id="a6ad1-103">\_Événement de \_ \_ désactivation de l’LSP Winsock ws2help</span><span class="sxs-lookup"><span data-stu-id="a6ad1-103">WINSOCK\_WS2HELP\_LSP\_DISABLE event</span></span>

> [!Note]  
> <span data-ttu-id="a6ad1-104">Les fournisseurs de services en couche sont déconseillés.</span><span class="sxs-lookup"><span data-stu-id="a6ad1-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="a6ad1-105">À compter de Windows 8 et de Windows Server 2012, utilisez la [plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="a6ad1-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="a6ad1-106">L’événement **Winsock \_ ws2help \_ LSP \_ Disable** est un événement de modification du catalogue Winsock pour une opération de désactivation du fournisseur de services en couche (LSP).</span><span class="sxs-lookup"><span data-stu-id="a6ad1-106">The **WINSOCK\_WS2HELP\_LSP\_DISABLE** event is a Winsock catalog change event for a layered service provider (LSP) disable operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_DISABLE = {0x3, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="a6ad1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6ad1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6ad1-108">*Nom LSP*</span><span class="sxs-lookup"><span data-stu-id="a6ad1-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ad1-109">Nom du LSP obtenu à partir du membre **szProtocol** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours de désactivation.</span><span class="sxs-lookup"><span data-stu-id="a6ad1-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span>

</dd> <dt>

<span data-ttu-id="a6ad1-110">*Catalogue*</span><span class="sxs-lookup"><span data-stu-id="a6ad1-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ad1-111">Le catalogue Winsock (32 bits ou 64 bits) sur lequel est désactivé le LSP.</span><span class="sxs-lookup"><span data-stu-id="a6ad1-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being disabled.</span></span> <span data-ttu-id="a6ad1-112">Il s’agit d’une valeur entière qui est 32 ou 64.</span><span class="sxs-lookup"><span data-stu-id="a6ad1-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="a6ad1-113">*Programme d’installation*</span><span class="sxs-lookup"><span data-stu-id="a6ad1-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ad1-114">Nom du fichier de module de l’application qui effectue l’appel de désactivation du LSP.</span><span class="sxs-lookup"><span data-stu-id="a6ad1-114">The module filename of the application making the LSP disable call.</span></span>

</dd> <dt>

<span data-ttu-id="a6ad1-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="a6ad1-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ad1-116">Valeur GUID du fournisseur de transport Winsock que le LSP est en cours de désactivation.</span><span class="sxs-lookup"><span data-stu-id="a6ad1-116">The GUID value of the Winsock transport provider that the LSP is being disabled.</span></span>

</dd> <dt>

<span data-ttu-id="a6ad1-117">*Catégorie*</span><span class="sxs-lookup"><span data-stu-id="a6ad1-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="a6ad1-118">Le membre **dwCatalogEntryId** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours de désactivation.</span><span class="sxs-lookup"><span data-stu-id="a6ad1-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span>

</dd> </dl>

<span data-ttu-id="a6ad1-119">Cet événement n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="a6ad1-119">This event has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6ad1-120">Notes</span><span class="sxs-lookup"><span data-stu-id="a6ad1-120">Remarks</span></span>

<span data-ttu-id="a6ad1-121">L’événement de **\_ \_ \_ désactivation de l’LSP Winsock ws2help** est suivi pour une opération de désactivation LSP lorsqu’une entrée de protocole est désactivée dans le catalogue Winsock.</span><span class="sxs-lookup"><span data-stu-id="a6ad1-121">The **WINSOCK\_WS2HELP\_LSP\_DISABLE** event is traced for an LSP disable operation when a protocol entry is disabled in the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6ad1-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a6ad1-122">Requirements</span></span>



| <span data-ttu-id="a6ad1-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6ad1-123">Requirement</span></span> | <span data-ttu-id="a6ad1-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6ad1-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a6ad1-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6ad1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ad1-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6ad1-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a6ad1-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6ad1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ad1-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6ad1-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a6ad1-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6ad1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ad1-130">Contrôle du suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="a6ad1-130">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="a6ad1-131">Suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="a6ad1-131">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="a6ad1-132">Niveaux de suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="a6ad1-132">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="a6ad1-133">Détails du suivi de modification du catalogue Winsock</span><span class="sxs-lookup"><span data-stu-id="a6ad1-133">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
