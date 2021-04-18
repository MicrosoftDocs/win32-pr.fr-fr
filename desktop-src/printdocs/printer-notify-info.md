---
description: La structure des informations de \_ notification \_ d’imprimante contient les informations d’imprimante retournées par la fonction FindNextPrinterChangeNotification. La fonction retourne ces informations après qu’une opération d’attente sur un objet de notification de modification d’imprimante a été satisfaite.
ms.assetid: c104fabe-edf5-426e-859b-694811975623
title: Structure PRINTER_NOTIFY_INFO (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_NOTIFY_INFO
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 631169cfcdabd6a87459ebb777adb6842d09089b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533940"
---
# <a name="printer_notify_info-structure"></a><span data-ttu-id="c3430-104">Structure des informations de \_ notification de l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="c3430-104">PRINTER\_NOTIFY\_INFO structure</span></span>

<span data-ttu-id="c3430-105">La structure des informations de **\_ notification \_ d’imprimante** contient les informations d’imprimante retournées par la fonction [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="c3430-105">The **PRINTER\_NOTIFY\_INFO** structure contains printer information returned by the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span> <span data-ttu-id="c3430-106">La fonction retourne ces informations après qu’une opération d’attente sur un objet de notification de modification d’imprimante a été satisfaite.</span><span class="sxs-lookup"><span data-stu-id="c3430-106">The function returns this information after a wait operation on a printer change notification object has been satisfied.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3430-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3430-107">Syntax</span></span>


```C++
typedef struct _PRINTER_NOTIFY_INFO {
  DWORD                    Version;
  DWORD                    Flags;
  DWORD                    Count;
  PRINTER_NOTIFY_INFO_DATA aData[1];
} PRINTER_NOTIFY_INFO, *PPRINTER_NOTIFY_INFO;
```



## <a name="members"></a><span data-ttu-id="c3430-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c3430-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c3430-109">**Version**</span><span class="sxs-lookup"><span data-stu-id="c3430-109">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="c3430-110">Version de cette structure.</span><span class="sxs-lookup"><span data-stu-id="c3430-110">The version of this structure.</span></span> <span data-ttu-id="c3430-111">Affectez la valeur 2 à ce membre.</span><span class="sxs-lookup"><span data-stu-id="c3430-111">Set this member to 2.</span></span>

</dd> <dt>

<span data-ttu-id="c3430-112">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="c3430-112">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="c3430-113">Indicateur binaire qui indique l’état de la structure de notification.</span><span class="sxs-lookup"><span data-stu-id="c3430-113">A bit flag that indicates the state of the notification structure.</span></span> <span data-ttu-id="c3430-114">Si le \_ bit d’informations sur la notification d’imprimante \_ \_ ignoré est défini, cela indique que certaines notifications devaient être ignorées.</span><span class="sxs-lookup"><span data-stu-id="c3430-114">If the PRINTER\_NOTIFY\_INFO\_DISCARDED bit is set, it indicates that some notifications had to be discarded.</span></span>

</dd> <dt>

<span data-ttu-id="c3430-115">**Count**</span><span class="sxs-lookup"><span data-stu-id="c3430-115">**Count**</span></span>
</dt> <dd>

<span data-ttu-id="c3430-116">Nombre d’éléments [**de \_ \_ \_ données d’informations de notification d’imprimante**](printer-notify-info-data.md) dans le tableau **adatuma** .</span><span class="sxs-lookup"><span data-stu-id="c3430-116">The number of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) elements in the **aData** array.</span></span>

</dd> <dt>

<span data-ttu-id="c3430-117">**Adatum**</span><span class="sxs-lookup"><span data-stu-id="c3430-117">**aData**</span></span>
</dt> <dd>

<span data-ttu-id="c3430-118">Tableau de structures [**de \_ \_ \_ données d’informations de notification d’imprimante**](printer-notify-info-data.md) .</span><span class="sxs-lookup"><span data-stu-id="c3430-118">An array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures.</span></span> <span data-ttu-id="c3430-119">Chaque élément du tableau identifie un champ de travail unique ou un champ d’informations d’imprimante, et fournit les données actuelles pour ce champ.</span><span class="sxs-lookup"><span data-stu-id="c3430-119">Each element of the array identifies a single job or printer information field, and provides the current data for that field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3430-120">Notes</span><span class="sxs-lookup"><span data-stu-id="c3430-120">Remarks</span></span>

<span data-ttu-id="c3430-121">Si le membre **Flags** comporte l' \_ \_ ensemble de bits d’informations de notification d’imprimante \_ , cela indique qu’un dépassement de capacité ou une erreur s’est produite et que des notifications ont peut-être été perdues.</span><span class="sxs-lookup"><span data-stu-id="c3430-121">If the **Flags** member has the PRINTER\_NOTIFY\_INFO\_DISCARDED bit set, this indicates that an overflow or error occurred, and notifications may have been lost.</span></span> <span data-ttu-id="c3430-122">Dans ce cas, vous devez appeler [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) et spécifier l' \_ \_ \_ indicateur d’actualisation des options de notification d’imprimante pour récupérer toutes les informations actuelles.</span><span class="sxs-lookup"><span data-stu-id="c3430-122">In this case, you must call [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) and specify the PRINTER\_NOTIFY\_OPTIONS\_REFRESH flag to retrieve all current information.</span></span> <span data-ttu-id="c3430-123">Tant que vous n’avez pas demandé cette opération d’actualisation, le système n’envoie pas de notifications supplémentaires pour cet objet de notification de modification.</span><span class="sxs-lookup"><span data-stu-id="c3430-123">Until you request this refresh operation, the system will not send additional notifications for this change notification object.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3430-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c3430-124">Requirements</span></span>



| <span data-ttu-id="c3430-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c3430-125">Requirement</span></span> | <span data-ttu-id="c3430-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="c3430-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3430-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3430-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c3430-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3430-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c3430-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c3430-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c3430-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c3430-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c3430-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="c3430-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c3430-132"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3430-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3430-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c3430-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3430-134">Impression</span><span class="sxs-lookup"><span data-stu-id="c3430-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c3430-135">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="c3430-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="c3430-136">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="c3430-136">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="c3430-137">**\_données d' \_ informations de notification d’imprimante \_**</span><span class="sxs-lookup"><span data-stu-id="c3430-137">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> </dl>

 

 




