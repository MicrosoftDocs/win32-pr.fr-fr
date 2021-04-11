---
description: Spécifie la mise en cache d’un handle pour une imprimante ouverte avec OpenPrinter2.
ms.assetid: e5a62322-723c-490d-8de1-f74dcac9e22d
title: Énumération PRINTER_OPTION_FLAGS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTION_FLAGS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 683ad70b5db12c11a2bccd11905e7ef87fce1bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209786"
---
# <a name="printer_option_flags-enumeration"></a><span data-ttu-id="8741f-103">\_Énumération d’indicateurs d’option d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="8741f-103">PRINTER\_OPTION\_FLAGS enumeration</span></span>

<span data-ttu-id="8741f-104">Spécifie la mise en cache d’un handle pour une imprimante ouverte avec [**OpenPrinter2**](openprinter2.md).</span><span class="sxs-lookup"><span data-stu-id="8741f-104">Specifies the caching of a handle for a printer opened with [**OpenPrinter2**](openprinter2.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8741f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8741f-105">Syntax</span></span>


```C++
typedef enum tagPRINTER_OPTION_FLAGS { 
  PRINTER_OPTION_NO_CACHE,
  PRINTER_OPTION_CACHE,
  PRINTER_OPTION_CLIENT_CHANGE
} PRINTER_OPTION_FLAGS;
```



## <a name="constants"></a><span data-ttu-id="8741f-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="8741f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8741f-107"><span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**OPTION d’imprimante \_ \_ sans \_ cache**</span><span class="sxs-lookup"><span data-stu-id="8741f-107"><span id="PRINTER_OPTION_NO_CACHE"></span><span id="printer_option_no_cache"></span>**PRINTER\_OPTION\_NO\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="8741f-108">Le descripteur n’est pas mis en cache.</span><span class="sxs-lookup"><span data-stu-id="8741f-108">The handle is not cached.</span></span> <span data-ttu-id="8741f-109">Toutes les fonctions appliquées à un handle retourné par [**OpenPrinter2**](openprinter2.md) seront dirigées vers l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="8741f-109">All functions applied to a handle returned by [**OpenPrinter2**](openprinter2.md) will go to the remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="8741f-110"><span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**\_cache des options d’imprimante \_**</span><span class="sxs-lookup"><span data-stu-id="8741f-110"><span id="PRINTER_OPTION_CACHE"></span><span id="printer_option_cache"></span>**PRINTER\_OPTION\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="8741f-111">Le descripteur est mis en cache.</span><span class="sxs-lookup"><span data-stu-id="8741f-111">The handle is cached.</span></span> <span data-ttu-id="8741f-112">Toutes les fonctions appliquées à un handle retourné par [**OpenPrinter2**](openprinter2.md) seront placées dans le cache local.</span><span class="sxs-lookup"><span data-stu-id="8741f-112">All functions applied to a handle returned by [**OpenPrinter2**](openprinter2.md) will go to the local cache.</span></span>

</dd> <dt>

<span data-ttu-id="8741f-113"><span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**OPTION d’imprimante \_ \_ modification du client \_**</span><span class="sxs-lookup"><span data-stu-id="8741f-113"><span id="PRINTER_OPTION_CLIENT_CHANGE"></span><span id="printer_option_client_change"></span>**PRINTER\_OPTION\_CLIENT\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="8741f-114">Le descripteur retourné par [**OpenPrinter2**](openprinter2.md) peut être utilisé par [**SetPrinter**](setprinter.md) pour renommer la connexion d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="8741f-114">The handle returned by [**OpenPrinter2**](openprinter2.md) can be used by [**SetPrinter**](setprinter.md) to rename the printer connection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8741f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8741f-115">Requirements</span></span>



| <span data-ttu-id="8741f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8741f-116">Requirement</span></span> | <span data-ttu-id="8741f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="8741f-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8741f-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8741f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8741f-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8741f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="8741f-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8741f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8741f-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8741f-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8741f-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="8741f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8741f-123"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8741f-123"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8741f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8741f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8741f-125">Impression</span><span class="sxs-lookup"><span data-stu-id="8741f-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8741f-126">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="8741f-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="8741f-127">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="8741f-127">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="8741f-128">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="8741f-128">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

 




