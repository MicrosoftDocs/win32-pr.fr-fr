---
description: Événement de modification du catalogue Winsock pour une opération de réinitialisation du catalogue Winsock.
ms.assetid: BE8DC0DB-0F96-4015-87F5-ECF25AE164AA
title: Événement WINSOCK_WS2HELP_LSP_RESET
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_RESET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 219eb85dec0cdda77ca8741ae42df1f63d1a7dbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545841"
---
# <a name="winsock_ws2help_lsp_reset-event"></a><span data-ttu-id="01929-103">\_Événement de \_ réinitialisation du LSP Winsock ws2help \_</span><span class="sxs-lookup"><span data-stu-id="01929-103">WINSOCK\_WS2HELP\_LSP\_RESET event</span></span>

> [!Note]  
> <span data-ttu-id="01929-104">Les fournisseurs de services en couche sont déconseillés.</span><span class="sxs-lookup"><span data-stu-id="01929-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="01929-105">À compter de Windows 8 et de Windows Server 2012, utilisez la [plateforme de filtrage Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="01929-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="01929-106">L’événement de **\_ \_ \_ réinitialisation de Winsock ws2help LSP** est un événement de modification de catalogue Winsock pour une opération de réinitialisation de catalogue Winsock.</span><span class="sxs-lookup"><span data-stu-id="01929-106">The **WINSOCK\_WS2HELP\_LSP\_RESET** event is a Winsock catalog change event for a Winsock catalog reset operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_RESET = {0x4, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="01929-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01929-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="01929-108">*Catalogue*</span><span class="sxs-lookup"><span data-stu-id="01929-108">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="01929-109">Le catalogue Winsock (32 bits ou 64 bits) en cours de réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="01929-109">The Winsock catalog (32-bit or 64-bit) that is being reset.</span></span> <span data-ttu-id="01929-110">Il s’agit d’une valeur entière qui est 32 ou 64.</span><span class="sxs-lookup"><span data-stu-id="01929-110">This is an integer value that is either 32 or 64.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01929-111">Notes</span><span class="sxs-lookup"><span data-stu-id="01929-111">Remarks</span></span>

<span data-ttu-id="01929-112">L’événement de **\_ \_ \_ réinitialisation Winsock ws2help LSP** est suivi pour une opération du fournisseur de services en couche (LSP) Winsock lors de la réinitialisation du catalogue Winsock.</span><span class="sxs-lookup"><span data-stu-id="01929-112">The **WINSOCK\_WS2HELP\_LSP\_RESET** event is traced for an Winsock Layered Service Provider (LSP) operation when the Winsock catalog is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="01929-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01929-113">Requirements</span></span>



| <span data-ttu-id="01929-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01929-114">Requirement</span></span> | <span data-ttu-id="01929-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="01929-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="01929-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01929-116">Minimum supported client</span></span><br/> | <span data-ttu-id="01929-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01929-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="01929-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01929-118">Minimum supported server</span></span><br/> | <span data-ttu-id="01929-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="01929-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01929-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01929-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01929-121">Contrôle du suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="01929-121">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="01929-122">Suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="01929-122">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="01929-123">Niveaux de suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="01929-123">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="01929-124">Détails du suivi de modification du catalogue Winsock</span><span class="sxs-lookup"><span data-stu-id="01929-124">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
