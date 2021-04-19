---
description: Les \_ informations sur l’imprimante \_ 6 spécifient la valeur d’état d’une imprimante.
ms.assetid: f26fe75b-7c97-47ad-892f-d9e40331fa5d
title: Structure PRINTER_INFO_6 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_6
- _PRINTER_INFO_6A
- _PRINTER_INFO_6W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0ee4e86590483ec1751fa088fd56770c5891df0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545101"
---
# <a name="printer_info_6-structure"></a><span data-ttu-id="2a9fb-103">\_Structure infos imprimante \_ 6</span><span class="sxs-lookup"><span data-stu-id="2a9fb-103">PRINTER\_INFO\_6 structure</span></span>

<span data-ttu-id="2a9fb-104">Les **\_ informations sur \_ l’imprimante 6** spécifient la valeur d’état d’une imprimante.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-104">The **PRINTER\_INFO\_6** specifies the status value of a printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a9fb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a9fb-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_6 {
  DWORD dwStatus;
} PRINTER_INFO_6, *PPRINTER_INFO_6;
```



## <a name="members"></a><span data-ttu-id="2a9fb-106">Membres</span><span class="sxs-lookup"><span data-stu-id="2a9fb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2a9fb-107">**dwStatus**</span><span class="sxs-lookup"><span data-stu-id="2a9fb-107">**dwStatus**</span></span>
</dt> <dd>

<span data-ttu-id="2a9fb-108">État de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-108">The printer status.</span></span> <span data-ttu-id="2a9fb-109">Ce membre peut être une combinaison raisonnable des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-109">This member can be any reasonable combination of the following values.</span></span>



| <span data-ttu-id="2a9fb-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a9fb-110">Value</span></span>                               | <span data-ttu-id="2a9fb-111">Signification</span><span class="sxs-lookup"><span data-stu-id="2a9fb-111">Meaning</span></span>                                                                                                       |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a9fb-112">État de l’imprimante \_ \_ occupé</span><span class="sxs-lookup"><span data-stu-id="2a9fb-112">PRINTER\_STATUS\_BUSY</span></span>               | <span data-ttu-id="2a9fb-113">L'imprimante est occupée.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-113">The printer is busy.</span></span>                                                                                          |
| <span data-ttu-id="2a9fb-114">porte de l’état de l’imprimante \_ \_ \_ ouverte</span><span class="sxs-lookup"><span data-stu-id="2a9fb-114">PRINTER\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="2a9fb-115">La porte de l’imprimante est ouverte.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-115">The printer door is open.</span></span>                                                                                     |
| <span data-ttu-id="2a9fb-116">\_erreur d’état de l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="2a9fb-116">PRINTER\_STATUS\_ERROR</span></span>              | <span data-ttu-id="2a9fb-117">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-117">Not used.</span></span>                                                                                                     |
| <span data-ttu-id="2a9fb-118">État de l’imprimante en cours \_ \_ d’initialisation</span><span class="sxs-lookup"><span data-stu-id="2a9fb-118">PRINTER\_STATUS\_INITIALIZING</span></span>       | <span data-ttu-id="2a9fb-119">L'imprimante s'initialise.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-119">The printer is initializing.</span></span>                                                                                  |
| <span data-ttu-id="2a9fb-120">\_e/s d’état d’imprimante \_ \_ active</span><span class="sxs-lookup"><span data-stu-id="2a9fb-120">PRINTER\_STATUS\_IO\_ACTIVE</span></span>         | <span data-ttu-id="2a9fb-121">L’imprimante est dans un état d’entrée/sortie actif</span><span class="sxs-lookup"><span data-stu-id="2a9fb-121">The printer is in an active input/output state</span></span>                                                                |
| <span data-ttu-id="2a9fb-122">\_ \_ flux manuel de l’état de l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="2a9fb-122">PRINTER\_STATUS\_MANUAL\_FEED</span></span>       | <span data-ttu-id="2a9fb-123">L’imprimante est dans un état de flux manuel.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-123">The printer is in a manual feed state.</span></span>                                                                        |
| <span data-ttu-id="2a9fb-124">État de l’imprimante \_ \_ non \_ toner</span><span class="sxs-lookup"><span data-stu-id="2a9fb-124">PRINTER\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="2a9fb-125">L'imprimante est sans toner.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-125">The printer is out of toner.</span></span>                                                                                  |
| <span data-ttu-id="2a9fb-126">l’état de l’imprimante \_ \_ n’est pas \_ disponible</span><span class="sxs-lookup"><span data-stu-id="2a9fb-126">PRINTER\_STATUS\_NOT\_AVAILABLE</span></span>     | <span data-ttu-id="2a9fb-127">L’imprimante n’est pas disponible pour l’impression.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-127">The printer is not available for printing.</span></span>                                                                    |
| <span data-ttu-id="2a9fb-128">État de l’imprimante \_ \_ hors connexion</span><span class="sxs-lookup"><span data-stu-id="2a9fb-128">PRINTER\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="2a9fb-129">L'imprimante est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-129">The printer is offline.</span></span>                                                                                       |
| <span data-ttu-id="2a9fb-130">\_ \_ mémoire insuffisante sur l’état \_ de \_ l’imprimante</span><span class="sxs-lookup"><span data-stu-id="2a9fb-130">PRINTER\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="2a9fb-131">La mémoire de l’imprimante est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-131">The printer has run out of memory.</span></span>                                                                            |
| <span data-ttu-id="2a9fb-132">bac de sortie de l’état de l’imprimante \_ \_ \_ \_ plein</span><span class="sxs-lookup"><span data-stu-id="2a9fb-132">PRINTER\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="2a9fb-133">Le bac de sortie de l'imprimante est plein.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-133">The printer's output bin is full.</span></span>                                                                             |
| <span data-ttu-id="2a9fb-134">PAGE État de l’imprimante \_ \_ \_ chargeur</span><span class="sxs-lookup"><span data-stu-id="2a9fb-134">PRINTER\_STATUS\_PAGE\_PUNT</span></span>         | <span data-ttu-id="2a9fb-135">L’imprimante ne peut pas imprimer la page active.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-135">The printer cannot print the current page.</span></span>                                                                    |
| <span data-ttu-id="2a9fb-136">\_ \_ bourrage papier sur l’état de l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="2a9fb-136">PRINTER\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="2a9fb-137">Le papier est coincé dans l’imprimante</span><span class="sxs-lookup"><span data-stu-id="2a9fb-137">Paper is jammed in the printer</span></span>                                                                                |
| <span data-ttu-id="2a9fb-138">\_ \_ sortie papier de l’état de l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="2a9fb-138">PRINTER\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="2a9fb-139">L’imprimante n’est plus imprimée.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-139">The printer is out of paper.</span></span>                                                                                  |
| <span data-ttu-id="2a9fb-140">\_ \_ problème papier sur l’état de l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="2a9fb-140">PRINTER\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="2a9fb-141">L’imprimante présente un problème de papier.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-141">The printer has a paper problem.</span></span>                                                                              |
| <span data-ttu-id="2a9fb-142">État de l’imprimante \_ \_ suspendu</span><span class="sxs-lookup"><span data-stu-id="2a9fb-142">PRINTER\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="2a9fb-143">L’imprimante est suspendue.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-143">The printer is paused.</span></span>                                                                                        |
| <span data-ttu-id="2a9fb-144">État de l’imprimante \_ \_ en attente de \_ suppression</span><span class="sxs-lookup"><span data-stu-id="2a9fb-144">PRINTER\_STATUS\_PENDING\_DELETION</span></span>  | <span data-ttu-id="2a9fb-145">L’imprimante est en attente de suppression suite à un appel à la fonction [**DeletePrinter**](deleteprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="2a9fb-145">The printer is pending deletion as a result of a call to the [**DeletePrinter**](deleteprinter.md) function.</span></span> |
| <span data-ttu-id="2a9fb-146">État de l’imprimante \_ \_ économie d’énergie \_</span><span class="sxs-lookup"><span data-stu-id="2a9fb-146">PRINTER\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="2a9fb-147">L'imprimante est en mode mise en veille.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-147">The printer is in power save mode.</span></span>                                                                            |
| <span data-ttu-id="2a9fb-148">\_impression de \_ l’état de l’imprimante</span><span class="sxs-lookup"><span data-stu-id="2a9fb-148">PRINTER\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="2a9fb-149">L’imprimante est en cours d’impression.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-149">The printer is printing.</span></span>                                                                                      |
| <span data-ttu-id="2a9fb-150">traitement de l’état de l’imprimante \_ \_</span><span class="sxs-lookup"><span data-stu-id="2a9fb-150">PRINTER\_STATUS\_PROCESSING</span></span>         | <span data-ttu-id="2a9fb-151">L’imprimante traite une commande à partir de la fonction [**SetPrinter**](setprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="2a9fb-151">The printer is processing a command from the [**SetPrinter**](setprinter.md) function.</span></span>                       |
| <span data-ttu-id="2a9fb-152">serveur d’état d’imprimante \_ \_ \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="2a9fb-152">PRINTER\_STATUS\_SERVER\_UNKNOWN</span></span>    | <span data-ttu-id="2a9fb-153">L’état de l’imprimante est inconnu.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-153">The printer status is unknown.</span></span>                                                                                |
| <span data-ttu-id="2a9fb-154">\_toner d' \_ état \_ faible de l’imprimante</span><span class="sxs-lookup"><span data-stu-id="2a9fb-154">PRINTER\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="2a9fb-155">L’imprimante manque de toner.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-155">The printer is low on toner.</span></span>                                                                                  |
| <span data-ttu-id="2a9fb-156">INTERVENTION de l’utilisateur sur l’état de l’imprimante \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="2a9fb-156">PRINTER\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="2a9fb-157">L’imprimante a une erreur qui oblige l’utilisateur à effectuer une opération.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-157">The printer has an error that requires the user to do something.</span></span>                                              |
| <span data-ttu-id="2a9fb-158">État de l’imprimante en \_ \_ attente</span><span class="sxs-lookup"><span data-stu-id="2a9fb-158">PRINTER\_STATUS\_WAITING</span></span>            | <span data-ttu-id="2a9fb-159">L’imprimante est en attente.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-159">The printer is waiting.</span></span>                                                                                       |
| <span data-ttu-id="2a9fb-160">État de l’imprimante \_ \_ préchauffage \_</span><span class="sxs-lookup"><span data-stu-id="2a9fb-160">PRINTER\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="2a9fb-161">L'imprimante s'allume.</span><span class="sxs-lookup"><span data-stu-id="2a9fb-161">The printer is warming up.</span></span>                                                                                    |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2a9fb-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a9fb-162">Requirements</span></span>



| <span data-ttu-id="2a9fb-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a9fb-163">Requirement</span></span> | <span data-ttu-id="2a9fb-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a9fb-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a9fb-165">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a9fb-165">Minimum supported client</span></span><br/> | <span data-ttu-id="2a9fb-166">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2a9fb-166">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2a9fb-167">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2a9fb-167">Minimum supported server</span></span><br/> | <span data-ttu-id="2a9fb-168">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2a9fb-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2a9fb-169">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a9fb-169">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a9fb-170"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a9fb-170"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2a9fb-171">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="2a9fb-171">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2a9fb-172">**\_ \_ Infos sur \_ l’imprimante 6W** (Unicode) et **\_ \_ informations sur l’imprimante \_ 6A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2a9fb-172">**\_PRINTER\_INFO\_6W** (Unicode) and **\_PRINTER\_INFO\_6A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="2a9fb-173">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a9fb-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a9fb-174">Impression</span><span class="sxs-lookup"><span data-stu-id="2a9fb-174">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2a9fb-175">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="2a9fb-175">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="2a9fb-176">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="2a9fb-176">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="2a9fb-177">**\_Infos sur l’imprimante \_ 1**</span><span class="sxs-lookup"><span data-stu-id="2a9fb-177">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="2a9fb-178">**\_Infos sur l’imprimante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="2a9fb-178">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="2a9fb-179">**\_Infos sur l’imprimante \_ 3**</span><span class="sxs-lookup"><span data-stu-id="2a9fb-179">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="2a9fb-180">**\_Infos sur l’imprimante \_ 4**</span><span class="sxs-lookup"><span data-stu-id="2a9fb-180">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="2a9fb-181">**\_Infos sur l’imprimante \_ 5**</span><span class="sxs-lookup"><span data-stu-id="2a9fb-181">**PRINTER\_INFO\_5**</span></span>](printer-info-5.md)
</dt> </dl>

 

 




