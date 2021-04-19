---
description: La \_ \_ \_ structure de type options de notification d’imprimante spécifie le jeu de champs d’informations d’imprimante ou de travail à surveiller par un objet de notification de modification d’imprimante. Un appel à la fonction FindFirstPrinterChangeNotification spécifie une \_ \_ structure d’options Notify d’imprimante, qui contient un tableau de structures de types d’options de notification d’imprimante \_ \_ \_ .
ms.assetid: 1009f892-d3a8-4887-99b4-a35d1268eeb4
title: Structure PRINTER_NOTIFY_OPTIONS_TYPE (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_OPTIONS_TYPE
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 4a82d0bc0481533a65fc90d32a992c51116b4595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528167"
---
# <a name="printer_notify_options_type-structure"></a><span data-ttu-id="bf626-103">\_Structure de \_ type des options de notification d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="bf626-103">PRINTER\_NOTIFY\_OPTIONS\_TYPE structure</span></span>

<span data-ttu-id="bf626-104">La structure de **\_ \_ \_ type options de notification d’imprimante** spécifie le jeu de champs d’informations d’imprimante ou de travail à surveiller par un objet de notification de modification d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="bf626-104">The **PRINTER\_NOTIFY\_OPTIONS\_TYPE** structure specifies the set of printer or job information fields to be monitored by a printer change notification object.</span></span>

<span data-ttu-id="bf626-105">Un appel à la fonction [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) spécifie une structure d' [**\_ \_ options Notify d’imprimante**](printer-notify-options.md) , qui contient un tableau de structures de **\_ \_ \_ types d’options de notification d’imprimante** .</span><span class="sxs-lookup"><span data-stu-id="bf626-105">A call to the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function specifies a [**PRINTER\_NOTIFY\_OPTIONS**](printer-notify-options.md) structure, which contains an array of **PRINTER\_NOTIFY\_OPTIONS\_TYPE** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf626-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf626-106">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_OPTIONS_TYPE {
  WORD  Type;
  WORD  Reserved0;
  DWORD Reserved1;
  DWORD Reserved2;
  DWORD Count;
  PWORD pFields;
} PRINTER_NOTIFY_OPTIONS_TYPE, *PPRINTER_NOTIFY_OPTIONS_TYPE;
```



## <a name="members"></a><span data-ttu-id="bf626-107">Membres</span><span class="sxs-lookup"><span data-stu-id="bf626-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bf626-108">**Type**</span><span class="sxs-lookup"><span data-stu-id="bf626-108">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="bf626-109">Type à suivre.</span><span class="sxs-lookup"><span data-stu-id="bf626-109">The type to be watched.</span></span> <span data-ttu-id="bf626-110">Ce membre peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="bf626-110">This member can be one of the following values.</span></span>



| <span data-ttu-id="bf626-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf626-111">Value</span></span>                                                                                                                                                                                                                                      | <span data-ttu-id="bf626-112">Signification</span><span class="sxs-lookup"><span data-stu-id="bf626-112">Meaning</span></span>                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span id="JOB_NOTIFY_TYPE"></span><span id="job_notify_type"></span><dl> <span data-ttu-id="bf626-113"><dt>**Travail \_ \_Type de notification**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="bf626-113"><dt>**JOB\_NOTIFY\_TYPE**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="bf626-114">Indique que les champs spécifiés dans le tableau **pFields** sont \_ des \_ constantes de champ de notification de travail \_ \* .</span><span class="sxs-lookup"><span data-stu-id="bf626-114">Indicates that the fields specified in the **pFields** array are JOB\_NOTIFY\_FIELD\_\* constants.</span></span><br/>     |
| <span id="PRINTER_NOTIFY_TYPE"></span><span id="printer_notify_type"></span><dl> <span data-ttu-id="bf626-115"><dt>**Imprimante \_ \_Type de notification**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="bf626-115"><dt>**PRINTER\_NOTIFY\_TYPE**</dt> <dt>0x00</dt></span></span> </dl> | <span data-ttu-id="bf626-116">Indique que les champs spécifiés dans le tableau **pFields** sont \_ des \_ constantes de champ de notification d’imprimante \_ \* .</span><span class="sxs-lookup"><span data-stu-id="bf626-116">Indicates that the fields specified in the **pFields** array are PRINTER\_NOTIFY\_FIELD\_\* constants.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bf626-117">**Reserved0**</span><span class="sxs-lookup"><span data-stu-id="bf626-117">**Reserved0**</span></span>
</dt> <dd>

<span data-ttu-id="bf626-118">Réservé.</span><span class="sxs-lookup"><span data-stu-id="bf626-118">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bf626-119">**Reserved1**</span><span class="sxs-lookup"><span data-stu-id="bf626-119">**Reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="bf626-120">Réservé.</span><span class="sxs-lookup"><span data-stu-id="bf626-120">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bf626-121">**Reserved2**</span><span class="sxs-lookup"><span data-stu-id="bf626-121">**Reserved2**</span></span>
</dt> <dd>

<span data-ttu-id="bf626-122">Réservé.</span><span class="sxs-lookup"><span data-stu-id="bf626-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bf626-123">**Count**</span><span class="sxs-lookup"><span data-stu-id="bf626-123">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="bf626-124">Nombre d’éléments dans le tableau **pFields** .</span><span class="sxs-lookup"><span data-stu-id="bf626-124">The number of elements in the **pFields** array.</span></span>

</dd> <dt>

<span data-ttu-id="bf626-125">**pFields**</span><span class="sxs-lookup"><span data-stu-id="bf626-125">**pFields**</span></span>
</dt> <dd>

<span data-ttu-id="bf626-126">Pointeur vers un tableau de valeurs.</span><span class="sxs-lookup"><span data-stu-id="bf626-126">A pointer to an array of values.</span></span> <span data-ttu-id="bf626-127">Chaque élément du tableau spécifie un champ d’information de travail ou d’imprimante qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="bf626-127">Each element of the array specifies a job or printer information field of interest.</span></span> <span data-ttu-id="bf626-128">Pour obtenir la liste des champs d’informations sur les imprimantes et les travaux pris en charge, consultez la structure des [**\_ \_ \_ données de notification d’imprimante**](printer-notify-info-data.md) .</span><span class="sxs-lookup"><span data-stu-id="bf626-128">For a list of supported printer and job information fields, see the [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bf626-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf626-129">Requirements</span></span>



| <span data-ttu-id="bf626-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf626-130">Requirement</span></span> | <span data-ttu-id="bf626-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf626-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf626-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf626-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bf626-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf626-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bf626-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf626-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bf626-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf626-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bf626-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf626-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf626-137"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf626-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf626-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf626-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf626-139">Impression</span><span class="sxs-lookup"><span data-stu-id="bf626-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bf626-140">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="bf626-140">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="bf626-141">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="bf626-141">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="bf626-142">**\_données d' \_ informations de notification d’imprimante \_**</span><span class="sxs-lookup"><span data-stu-id="bf626-142">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> <dt>

[<span data-ttu-id="bf626-143">**\_options de notification d’imprimante \_**</span><span class="sxs-lookup"><span data-stu-id="bf626-143">**PRINTER\_NOTIFY\_OPTIONS**</span></span>](printer-notify-options.md)
</dt> </dl>

 

 




