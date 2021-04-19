---
description: Représente un pilote d’imprimante dont dépendent d’autres pilotes d’imprimante.
ms.assetid: b03f9ac1-7ad2-4aee-b496-e1ee15ba7d38
title: Structure CORE_PRINTER_DRIVER (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CORE_PRINTER_DRIVER
- _CORE_PRINTER_DRIVERA
- _CORE_PRINTER_DRIVERW
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 786fa3491919659fca60700cfb086023c3fdef3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521558"
---
# <a name="core_printer_driver-structure"></a><span data-ttu-id="db81c-103">Structure du pilote d' \_ imprimante principale \_</span><span class="sxs-lookup"><span data-stu-id="db81c-103">CORE\_PRINTER\_DRIVER structure</span></span>

<span data-ttu-id="db81c-104">Représente un pilote d’imprimante dont dépendent d’autres pilotes d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="db81c-104">Represents a printer driver on which other printer drivers depend.</span></span>

## <a name="syntax"></a><span data-ttu-id="db81c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db81c-105">Syntax</span></span>


```C++
typedef struct _CORE_PRINTER_DRIVER {
  GUID      CoreDriverGUID;
  FILETIME  ftDriverDate;
  DWORDLONG dwlDriverVersion;
  TCHAR     szPackageID[MAX_PATH];
} CORE_PRINTER_DRIVER, *PCORE_PRINTER_DRIVER;
```



## <a name="members"></a><span data-ttu-id="db81c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="db81c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="db81c-107">**CoreDriverGUID**</span><span class="sxs-lookup"><span data-stu-id="db81c-107">**CoreDriverGUID**</span></span>
</dt> <dd>

<span data-ttu-id="db81c-108">GUID du pilote d’imprimante principal.</span><span class="sxs-lookup"><span data-stu-id="db81c-108">The GUID of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="db81c-109">**ftDriverDate**</span><span class="sxs-lookup"><span data-stu-id="db81c-109">**ftDriverDate**</span></span>
</dt> <dd>

<span data-ttu-id="db81c-110">Date et heure de la dernière version du pilote d’imprimante principal.</span><span class="sxs-lookup"><span data-stu-id="db81c-110">The date and time of the latest version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="db81c-111">**dwlDriverVersion**</span><span class="sxs-lookup"><span data-stu-id="db81c-111">**dwlDriverVersion**</span></span>
</dt> <dd>

<span data-ttu-id="db81c-112">ID de version de la dernière version du pilote d’imprimante principal.</span><span class="sxs-lookup"><span data-stu-id="db81c-112">The version ID of the latest version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="db81c-113">**szPackageID \[ \_ chemin d’accès maximal\]**</span><span class="sxs-lookup"><span data-stu-id="db81c-113">**szPackageID\[MAX\_PATH\]**</span></span>
</dt> <dd>

<span data-ttu-id="db81c-114">Chemin d’accès au package de pilotes qui contient le pilote d’imprimante principal.</span><span class="sxs-lookup"><span data-stu-id="db81c-114">The path to the driver package that contains the core printer driver.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="db81c-115">Notes</span><span class="sxs-lookup"><span data-stu-id="db81c-115">Remarks</span></span>

<span data-ttu-id="db81c-116">Cette structure peut représenter le pilote de base d’un fabricant sur lequel les pilotes de différents modèles d’imprimante sont dépendants.</span><span class="sxs-lookup"><span data-stu-id="db81c-116">This structure can represent a manufacturer's base driver on which the drivers for various printer models are dependent.</span></span>

## <a name="requirements"></a><span data-ttu-id="db81c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db81c-117">Requirements</span></span>



| <span data-ttu-id="db81c-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db81c-118">Requirement</span></span> | <span data-ttu-id="db81c-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="db81c-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db81c-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db81c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="db81c-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db81c-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="db81c-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db81c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="db81c-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="db81c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="db81c-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="db81c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="db81c-125"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db81c-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="db81c-126">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="db81c-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="db81c-127">**\_ Core \_ Printer \_ DRIVERW** (Unicode) and **\_ Core \_ Printer \_ drivera** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="db81c-127">**\_CORE\_PRINTER\_DRIVERW** (Unicode) and **\_CORE\_PRINTER\_DRIVERA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="db81c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db81c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db81c-129">Impression</span><span class="sxs-lookup"><span data-stu-id="db81c-129">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="db81c-130">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="db81c-130">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> </dl>

 

 




