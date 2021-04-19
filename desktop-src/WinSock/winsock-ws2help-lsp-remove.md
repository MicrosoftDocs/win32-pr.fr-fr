---
description: Événement de modification du catalogue Winsock pour une opération de suppression du fournisseur de services en couche (LSP).
ms.assetid: 86FF17F7-8CCF-4A03-899F-42BFACDF3F54
title: Événement WINSOCK_WS2HELP_LSP_REMOVE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_REMOVE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 597cd2f8cfc3bb7727301e64af53671bafbd9469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541906"
---
# <a name="winsock_ws2help_lsp_remove-event"></a><span data-ttu-id="f50fe-103">\_Événement de \_ suppression LSP Winsock ws2help \_</span><span class="sxs-lookup"><span data-stu-id="f50fe-103">WINSOCK\_WS2HELP\_LSP\_REMOVE event</span></span>

> [!Note]  
> <span data-ttu-id="f50fe-104">Les fournisseurs de services en couche sont déconseillés.</span><span class="sxs-lookup"><span data-stu-id="f50fe-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="f50fe-105">À compter de Windows 8 et de Windows Server 2012, utilisez la [plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="f50fe-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="f50fe-106">L’événement **Winsock \_ ws2help \_ LSP \_ Remove** est un événement de modification du catalogue Winsock pour une opération de suppression du fournisseur de services en couche (LSP).</span><span class="sxs-lookup"><span data-stu-id="f50fe-106">The **WINSOCK\_WS2HELP\_LSP\_REMOVE** event is a Winsock catalog change event for a layered service provider (LSP) removal operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_REMOVE = {0x2, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="f50fe-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f50fe-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f50fe-108">*Nom LSP*</span><span class="sxs-lookup"><span data-stu-id="f50fe-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="f50fe-109">Nom du LSP obtenu à partir du membre **szProtocol** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="f50fe-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span>

</dd> <dt>

<span data-ttu-id="f50fe-110">*Catalogue*</span><span class="sxs-lookup"><span data-stu-id="f50fe-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="f50fe-111">Le catalogue Winsock (32 bits ou 64 bits) dans lequel le LSP est supprimé.</span><span class="sxs-lookup"><span data-stu-id="f50fe-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being removed.</span></span> <span data-ttu-id="f50fe-112">Il s’agit d’une valeur entière qui est 32 ou 64.</span><span class="sxs-lookup"><span data-stu-id="f50fe-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="f50fe-113">*Programme d’installation*</span><span class="sxs-lookup"><span data-stu-id="f50fe-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="f50fe-114">Nom du fichier de module de l’application qui effectue l’appel de l’LSP de suppression.</span><span class="sxs-lookup"><span data-stu-id="f50fe-114">The module filename of the application making the LSP remove call.</span></span>

</dd> <dt>

<span data-ttu-id="f50fe-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="f50fe-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="f50fe-116">Valeur GUID du fournisseur de transport Winsock duquel le LSP est supprimé.</span><span class="sxs-lookup"><span data-stu-id="f50fe-116">The GUID value of the Winsock transport provider that the LSP is being removed from.</span></span>

</dd> <dt>

<span data-ttu-id="f50fe-117">*Catégorie*</span><span class="sxs-lookup"><span data-stu-id="f50fe-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="f50fe-118">Membre **dwCatalogEntryId** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="f50fe-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f50fe-119">Notes</span><span class="sxs-lookup"><span data-stu-id="f50fe-119">Remarks</span></span>

<span data-ttu-id="f50fe-120">L’événement **Winsock \_ ws2help \_ LSP \_ Remove** est suivi pour une opération de suppression LSP lorsqu’une entrée de protocole est supprimée du catalogue Winsock.</span><span class="sxs-lookup"><span data-stu-id="f50fe-120">The **WINSOCK\_WS2HELP\_LSP\_REMOVE** event is traced for an LSP removal operation when a protocol entry is removed from the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="f50fe-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f50fe-121">Requirements</span></span>



| <span data-ttu-id="f50fe-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f50fe-122">Requirement</span></span> | <span data-ttu-id="f50fe-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f50fe-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f50fe-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f50fe-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f50fe-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f50fe-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f50fe-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f50fe-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f50fe-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f50fe-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f50fe-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f50fe-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f50fe-129">Contrôle du suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="f50fe-129">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="f50fe-130">Suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="f50fe-130">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="f50fe-131">Niveaux de suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="f50fe-131">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="f50fe-132">Détails du suivi de modification du catalogue Winsock</span><span class="sxs-lookup"><span data-stu-id="f50fe-132">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
