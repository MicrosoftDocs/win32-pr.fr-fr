---
description: La \_ \_ structure des options de notification d’imprimante spécifie des options pour un objet de notification de modification qui surveille une imprimante ou un serveur d’impression.
ms.assetid: 712c546d-dbb3-4f78-b14e-fbb8619b57f9
title: Structure PRINTER_NOTIFY_OPTIONS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: af1aeaa1138145c5df18ea4fd5babaa1a9e60416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536687"
---
# <a name="printer_notify_options-structure"></a><span data-ttu-id="62078-103">Structure des options de \_ notification d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="62078-103">PRINTER\_NOTIFY\_OPTIONS structure</span></span>

<span data-ttu-id="62078-104">La structure des **\_ \_ options** de notification d’imprimante spécifie des options pour un objet de notification de modification qui surveille une imprimante ou un serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="62078-104">The **PRINTER\_NOTIFY\_OPTIONS** structure specifies options for a change notification object that monitors a printer or print server.</span></span>

## <a name="syntax"></a><span data-ttu-id="62078-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62078-105">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS {
  DWORD                        Version;
  DWORD                        Flags;
  DWORD                        Count;
  PPRINTER_NOTIFY_OPTIONS_TYPE pTypes;
} PRINTER_NOTIFY_OPTIONS, *PPRINTER_NOTIFY_OPTIONS;
```



## <a name="members"></a><span data-ttu-id="62078-106">Membres</span><span class="sxs-lookup"><span data-stu-id="62078-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="62078-107">**Version**</span><span class="sxs-lookup"><span data-stu-id="62078-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="62078-108">Version de cette structure.</span><span class="sxs-lookup"><span data-stu-id="62078-108">The version of this structure.</span></span> <span data-ttu-id="62078-109">Affectez la valeur 2 à ce membre.</span><span class="sxs-lookup"><span data-stu-id="62078-109">Set this member to 2.</span></span>

</dd> <dt>

<span data-ttu-id="62078-110">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="62078-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="62078-111">Indicateur de bit.</span><span class="sxs-lookup"><span data-stu-id="62078-111">A bit flag.</span></span> <span data-ttu-id="62078-112">Si vous définissez l' \_ indicateur d' \_ actualisation des options \_ de notification d’imprimante dans un appel à la fonction [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) , la fonction fournit des données actuelles pour tous les champs d’informations d’imprimante surveillés.</span><span class="sxs-lookup"><span data-stu-id="62078-112">If you set the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag in a call to the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function, the function provides current data for all monitored printer information fields.</span></span> <span data-ttu-id="62078-113">La fonction [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) ignore le membre **Flags** .</span><span class="sxs-lookup"><span data-stu-id="62078-113">The [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function ignores the **Flags** member.</span></span>

</dd> <dt>

<span data-ttu-id="62078-114">**Count**</span><span class="sxs-lookup"><span data-stu-id="62078-114">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="62078-115">Nombre d’éléments dans le tableau **pTypes** .</span><span class="sxs-lookup"><span data-stu-id="62078-115">The number of elements in the **pTypes** array.</span></span>

</dd> <dt>

<span data-ttu-id="62078-116">**pTypes**</span><span class="sxs-lookup"><span data-stu-id="62078-116">**pTypes**</span></span>
</dt> <dd>

<span data-ttu-id="62078-117">Pointeur vers un tableau de structures [**de \_ \_ \_ type d’options de notification d’imprimante**](printer-notify-options-type.md) .</span><span class="sxs-lookup"><span data-stu-id="62078-117">A pointer to an array of [**PRINTER\_NOTIFY\_OPTIONS\_TYPE**](printer-notify-options-type.md) structures.</span></span> <span data-ttu-id="62078-118">Utilisez un élément de ce tableau pour spécifier les champs d’informations d’imprimante à surveiller, et un élément pour spécifier les champs d’informations de travail à analyser.</span><span class="sxs-lookup"><span data-stu-id="62078-118">Use one element of this array to specify the printer information fields to monitor, and one element to specify the job information fields to monitor.</span></span> <span data-ttu-id="62078-119">Vous pouvez surveiller les informations de l’imprimante, les informations sur le travail ou les deux.</span><span class="sxs-lookup"><span data-stu-id="62078-119">You can monitor either printer information, job information, or both.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62078-120">Notes</span><span class="sxs-lookup"><span data-stu-id="62078-120">Remarks</span></span>

<span data-ttu-id="62078-121">Utilisez cette structure avec la fonction [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) pour spécifier le jeu de champs d’informations sur les imprimantes ou les travaux à surveiller pour la modification.</span><span class="sxs-lookup"><span data-stu-id="62078-121">Use this structure with the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function to specify the set of printer or job information fields to monitor for change.</span></span>

<span data-ttu-id="62078-122">Utilisez cette structure avec la fonction [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) pour demander les données actuelles pour tous les champs d’informations sur les imprimantes et les travaux analysés.</span><span class="sxs-lookup"><span data-stu-id="62078-122">Use this structure with the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function to request the current data for all monitored printer and job information fields.</span></span> <span data-ttu-id="62078-123">Dans ce cas, le membre **indicateurs** spécifie l' \_ indicateur d’actualisation des options de notification d’imprimante \_ \_ , et la fonction ignore les autres membres de la structure.</span><span class="sxs-lookup"><span data-stu-id="62078-123">In this case, the **Flags** member specifies the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag, and the function ignores the other structure members.</span></span>

## <a name="requirements"></a><span data-ttu-id="62078-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62078-124">Requirements</span></span>



| <span data-ttu-id="62078-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62078-125">Requirement</span></span> | <span data-ttu-id="62078-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="62078-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62078-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62078-127">Minimum supported client</span></span><br/> | <span data-ttu-id="62078-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62078-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="62078-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62078-129">Minimum supported server</span></span><br/> | <span data-ttu-id="62078-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62078-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="62078-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="62078-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="62078-132"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62078-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62078-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62078-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62078-134">Impression</span><span class="sxs-lookup"><span data-stu-id="62078-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="62078-135">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="62078-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="62078-136">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="62078-136">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="62078-137">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="62078-137">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="62078-138">**\_type d' \_ options de notification d’imprimante \_**</span><span class="sxs-lookup"><span data-stu-id="62078-138">**PRINTER\_NOTIFY\_OPTIONS\_TYPE**</span></span>](printer-notify-options-type.md)
</dt> </dl>

 

 




