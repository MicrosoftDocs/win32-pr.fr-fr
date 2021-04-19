---
title: WMDMDATETIME, structure
description: La structure WMDMDATETIME contient une date et une heure.
ms.assetid: 47f3994d-66c6-47e4-803d-0c98c70eccc8
keywords:
- Structure WMDMDATETIME Windows Media Gestionnaire de périphériques
- Pointeur de structure PWMDMDATETIME Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- WMDMDATETIME
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07acf706aa63a21edd27fb2ac206db3039249055
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528375"
---
# <a name="wmdmdatetime-structure"></a><span data-ttu-id="79c20-105">WMDMDATETIME, structure</span><span class="sxs-lookup"><span data-stu-id="79c20-105">WMDMDATETIME structure</span></span>

<span data-ttu-id="79c20-106">La structure **WMDMDATETIME** contient une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="79c20-106">The **WMDMDATETIME** structure contains a date and time of day.</span></span>

## <a name="syntax"></a><span data-ttu-id="79c20-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79c20-107">Syntax</span></span>


```C++
typedef struct _WMDMDATETIME {
  WORD wYear;
  WORD wMonth;
  WORD wDay;
  WORD wHour;
  WORD wMinute;
  WORD wSecond;
} WMDMDATETIME, *PWMDMDATETIME;
```



## <a name="members"></a><span data-ttu-id="79c20-108">Membres</span><span class="sxs-lookup"><span data-stu-id="79c20-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="79c20-109">**wYear**</span><span class="sxs-lookup"><span data-stu-id="79c20-109">**wYear**</span></span>
</dt> <dd>

<span data-ttu-id="79c20-110">Mot contenant l’année à quatre chiffres.</span><span class="sxs-lookup"><span data-stu-id="79c20-110">Word containing the four-digit year.</span></span>

</dd> <dt>

<span data-ttu-id="79c20-111">**wMonth**</span><span class="sxs-lookup"><span data-stu-id="79c20-111">**wMonth**</span></span>
</dt> <dd>

<span data-ttu-id="79c20-112">Mot contenant le mois (1-12).</span><span class="sxs-lookup"><span data-stu-id="79c20-112">Word containing the month (1-12).</span></span>

</dd> <dt>

<span data-ttu-id="79c20-113">**wDay**</span><span class="sxs-lookup"><span data-stu-id="79c20-113">**wDay**</span></span>
</dt> <dd>

<span data-ttu-id="79c20-114">Mot contenant le jour du mois (1-31).</span><span class="sxs-lookup"><span data-stu-id="79c20-114">Word containing the day of the month (1-31).</span></span>

</dd> <dt>

<span data-ttu-id="79c20-115">**wHour**</span><span class="sxs-lookup"><span data-stu-id="79c20-115">**wHour**</span></span>
</dt> <dd>

<span data-ttu-id="79c20-116">Mot contenant l’heure (0-23).</span><span class="sxs-lookup"><span data-stu-id="79c20-116">Word containing the hour (0-23).</span></span>

</dd> <dt>

<span data-ttu-id="79c20-117">**wMinute**</span><span class="sxs-lookup"><span data-stu-id="79c20-117">**wMinute**</span></span>
</dt> <dd>

<span data-ttu-id="79c20-118">Mot contenant la minute (0-59).</span><span class="sxs-lookup"><span data-stu-id="79c20-118">Word containing the minute (0-59).</span></span>

</dd> <dt>

<span data-ttu-id="79c20-119">**wSecond**</span><span class="sxs-lookup"><span data-stu-id="79c20-119">**wSecond**</span></span>
</dt> <dd>

<span data-ttu-id="79c20-120">Mot contenant le deuxième (0-59).</span><span class="sxs-lookup"><span data-stu-id="79c20-120">Word containing the second (0-59).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79c20-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79c20-121">Requirements</span></span>



| <span data-ttu-id="79c20-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79c20-122">Requirement</span></span> | <span data-ttu-id="79c20-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="79c20-123">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="79c20-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="79c20-124">Header</span></span><br/> | <dl> <span data-ttu-id="79c20-125"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="79c20-125"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79c20-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79c20-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79c20-127">**IMDSPStorage :: GetDate**</span><span class="sxs-lookup"><span data-stu-id="79c20-127">**IMDSPStorage::GetDate**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getdate)
</dt> <dt>

[<span data-ttu-id="79c20-128">**IWMDMStorage :: GetDate**</span><span class="sxs-lookup"><span data-stu-id="79c20-128">**IWMDMStorage::GetDate**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getdate)
</dt> <dt>

[<span data-ttu-id="79c20-129">**WMDMRIGHTS**</span><span class="sxs-lookup"><span data-stu-id="79c20-129">**WMDMRIGHTS**</span></span>](wmdmrights.md)
</dt> <dt>

[<span data-ttu-id="79c20-130">**Structures**</span><span class="sxs-lookup"><span data-stu-id="79c20-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





