---
description: La \_ structure informations sur le pilote \_ 1 identifie un pilote d’imprimante.
ms.assetid: 9435192b-3eba-4937-8cd3-bff4e9eb84d3
title: Structure DRIVER_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DRIVER_INFO_1
- _DRIVER_INFO_1A
- _DRIVER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 21301cdab4449d0a48254660d195d4f2507a80e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520136"
---
# <a name="driver_info_1-structure"></a><span data-ttu-id="ee7b8-103">\_Structure info du pilote \_ 1</span><span class="sxs-lookup"><span data-stu-id="ee7b8-103">DRIVER\_INFO\_1 structure</span></span>

<span data-ttu-id="ee7b8-104">La **structure \_ informations \_ sur le pilote 1** identifie un pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ee7b8-104">The **DRIVER\_INFO\_1** structure identifies a printer driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee7b8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee7b8-105">Syntax</span></span>


```C++
typedef struct _DRIVER_INFO_1 {
  LPTSTR pName;
} DRIVER_INFO_1, *PDRIVER_INFO_1;
```



## <a name="members"></a><span data-ttu-id="ee7b8-106">Membres</span><span class="sxs-lookup"><span data-stu-id="ee7b8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ee7b8-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="ee7b8-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="ee7b8-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom d’un pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ee7b8-108">Pointer to a null-terminated string that specifies the name of a printer driver.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ee7b8-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee7b8-109">Requirements</span></span>



| <span data-ttu-id="ee7b8-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee7b8-110">Requirement</span></span> | <span data-ttu-id="ee7b8-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee7b8-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee7b8-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee7b8-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ee7b8-113">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee7b8-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ee7b8-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee7b8-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ee7b8-115">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee7b8-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ee7b8-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee7b8-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee7b8-117"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee7b8-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ee7b8-118">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="ee7b8-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ee7b8-119">**\_ \_ Informations sur \_ le pilote 1s** (Unicode) et **\_ \_ informations sur le pilote \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ee7b8-119">**\_DRIVER\_INFO\_1W** (Unicode) and **\_DRIVER\_INFO\_1A** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="ee7b8-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee7b8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee7b8-121">Impression</span><span class="sxs-lookup"><span data-stu-id="ee7b8-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ee7b8-122">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="ee7b8-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="ee7b8-123">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="ee7b8-123">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> </dl>

 

 




