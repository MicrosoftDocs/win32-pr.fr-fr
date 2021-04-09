---
description: Événement de modification du catalogue Winsock pour une opération d’installation d’un fournisseur de services en couche (LSP).
ms.assetid: 76A3D175-8CDC-486C-8341-D6314BCEC113
title: Événement WINSOCK_WS2HELP_LSP_INSTALL
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_INSTALL
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2d95a77f68bafd29fde3bbf34336d9b31d2a412e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952552"
---
# <a name="winsock_ws2help_lsp_install-event"></a><span data-ttu-id="7d114-103">Événement d’installation de l' \_ ws2help \_ LSP Winsock \_</span><span class="sxs-lookup"><span data-stu-id="7d114-103">WINSOCK\_WS2HELP\_LSP\_INSTALL event</span></span>

> [!Note]  
> <span data-ttu-id="7d114-104">Les fournisseurs de services en couche sont déconseillés.</span><span class="sxs-lookup"><span data-stu-id="7d114-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="7d114-105">À compter de Windows 8 et de Windows Server 2012, utilisez la [plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="7d114-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="7d114-106">L’événement d' **installation de Winsock \_ ws2help \_ LSP \_** est un événement de modification du catalogue Winsock pour une opération d’installation d’un fournisseur de services en couche (LSP).</span><span class="sxs-lookup"><span data-stu-id="7d114-106">The **WINSOCK\_WS2HELP\_LSP\_INSTALL** event is a Winsock catalog change event for a layered service provider (LSP) installation operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_INSTALL = {0x1, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="7d114-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d114-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d114-108">*Nom LSP*</span><span class="sxs-lookup"><span data-stu-id="7d114-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="7d114-109">Nom du LSP obtenu à partir du membre **szProtocol** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="7d114-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span>

</dd> <dt>

<span data-ttu-id="7d114-110">*Catalogue*</span><span class="sxs-lookup"><span data-stu-id="7d114-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="7d114-111">Le catalogue Winsock (32 bits ou 64 bits) sur lequel est installé le LSP.</span><span class="sxs-lookup"><span data-stu-id="7d114-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being installed.</span></span> <span data-ttu-id="7d114-112">Il s’agit d’une valeur entière qui est 32 ou 64.</span><span class="sxs-lookup"><span data-stu-id="7d114-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="7d114-113">*Programme d’installation*</span><span class="sxs-lookup"><span data-stu-id="7d114-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="7d114-114">Nom de fichier du module de l’application effectuant l’appel d’installation LSP.</span><span class="sxs-lookup"><span data-stu-id="7d114-114">The module filename of the application making the LSP install call.</span></span>

</dd> <dt>

<span data-ttu-id="7d114-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="7d114-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="7d114-116">Valeur GUID du fournisseur de transport Winsock sous lequel le LSP est installé.</span><span class="sxs-lookup"><span data-stu-id="7d114-116">The GUID value of the Winsock transport provider that the LSP is being installed under.</span></span>

</dd> <dt>

<span data-ttu-id="7d114-117">*Catégorie*</span><span class="sxs-lookup"><span data-stu-id="7d114-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="7d114-118">Le membre **dwCatalogEntryId** de la structure [**WSAPROTOCOL \_ info**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour le LSP en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="7d114-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d114-119">Notes</span><span class="sxs-lookup"><span data-stu-id="7d114-119">Remarks</span></span>

<span data-ttu-id="7d114-120">L’événement d' **installation de Winsock \_ ws2help \_ LSP \_** est suivi pour une opération d’installation LSP lorsqu’une entrée de protocole est installée dans le catalogue Winsock.</span><span class="sxs-lookup"><span data-stu-id="7d114-120">The **WINSOCK\_WS2HELP\_LSP\_INSTALL** event is traced for an LSP install operation when a protocol entry is installed into the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d114-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d114-121">Requirements</span></span>



| <span data-ttu-id="7d114-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d114-122">Requirement</span></span> | <span data-ttu-id="7d114-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d114-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7d114-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d114-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7d114-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d114-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7d114-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7d114-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7d114-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7d114-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7d114-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d114-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d114-129">Contrôle du suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="7d114-129">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="7d114-130">Suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="7d114-130">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="7d114-131">Niveaux de suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="7d114-131">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="7d114-132">Détails du suivi de modification du catalogue Winsock</span><span class="sxs-lookup"><span data-stu-id="7d114-132">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
