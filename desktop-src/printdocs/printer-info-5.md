---
description: La structure de l’imprimante \_ info \_ 5 spécifie des informations détaillées sur l’imprimante.
ms.assetid: c8599f2e-3b7c-4fde-a340-ca7d3ddaa106
title: Structure PRINTER_INFO_5 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_5
- _PRINTER_INFO_5A
- _PRINTER_INFO_5W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2ec207b60eca8cc20f6f24e2bb08bb1e3b191fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522102"
---
# <a name="printer_info_5-structure"></a><span data-ttu-id="f79da-103">\_Structure des infos sur l’imprimante \_ 5</span><span class="sxs-lookup"><span data-stu-id="f79da-103">PRINTER\_INFO\_5 structure</span></span>

<span data-ttu-id="f79da-104">La structure de l' **imprimante \_ info \_ 5** spécifie des informations détaillées sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="f79da-104">The **PRINTER\_INFO\_5** structure specifies detailed printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f79da-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f79da-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_5 {
  LPTSTR pPrinterName;
  LPTSTR pPortName;
  DWORD  Attributes;
  DWORD  DeviceNotSelectedTimeout;
  DWORD  TransmissionRetryTimeout;
} PRINTER_INFO_5, *PPRINTER_INFO_5;
```



## <a name="members"></a><span data-ttu-id="f79da-106">Membres</span><span class="sxs-lookup"><span data-stu-id="f79da-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f79da-107">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="f79da-107">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="f79da-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="f79da-108">A pointer to a null-terminated string that specifies the name of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="f79da-109">**pPortName**</span><span class="sxs-lookup"><span data-stu-id="f79da-109">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="f79da-110">Pointeur vers une chaîne se terminant par un caractère null qui identifie le ou les ports utilisés pour transmettre des données à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="f79da-110">A pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="f79da-111">Si une imprimante est connectée à plusieurs ports, les noms de chaque port doivent être séparés par des virgules (par exemple, « LPT1 :, LPT2 :, LPT3 : »).</span><span class="sxs-lookup"><span data-stu-id="f79da-111">If a printer is connected to more than one port, the names of each port must be separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span>

</dd> <dt>

<span data-ttu-id="f79da-112">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="f79da-112">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="f79da-113">Attributs de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="f79da-113">The printer attributes.</span></span> <span data-ttu-id="f79da-114">Ce membre peut être une combinaison raisonnable des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f79da-114">This member can be any reasonable combination of the following values.</span></span>

| <span data-ttu-id="f79da-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f79da-115">Value</span></span>                                   | <span data-ttu-id="f79da-116">Signification</span><span class="sxs-lookup"><span data-stu-id="f79da-116">Meaning</span></span>                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f79da-117">attribut d’imprimante \_ \_ direct</span><span class="sxs-lookup"><span data-stu-id="f79da-117">PRINTER\_ATTRIBUTE\_DIRECT</span></span>              | <span data-ttu-id="f79da-118">Le travail est envoyé directement à l’imprimante (il n’est pas mis en file d’attente).</span><span class="sxs-lookup"><span data-stu-id="f79da-118">Job is sent directly to the printer (it is not spooled).</span></span>                                                                                                                                |
| <span data-ttu-id="f79da-119">l’attribut d’imprimante se \_ \_ \_ termine en \_ premier</span><span class="sxs-lookup"><span data-stu-id="f79da-119">PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST</span></span> | <span data-ttu-id="f79da-120">Si l’imprimante est définie et que l’imprimante est définie pour l’impression pendant la mise en file d’attente, toutes les tâches dont l’attente est terminée sont planifiées pour s’imprimer avant les travaux qui n’ont pas terminé la mise en attente.</span><span class="sxs-lookup"><span data-stu-id="f79da-120">If set and printer is set for print-while-spooling, any jobs that have completed spooling are scheduled to print before jobs that have not completed spooling.</span></span>                          |
| <span data-ttu-id="f79da-121">attribut d’imprimante \_ \_ Enable \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="f79da-121">PRINTER\_ATTRIBUTE\_ENABLE\_DEVQ</span></span>        | <span data-ttu-id="f79da-122">Si cette valeur est définie, **DevQueryPrint** est appelé.</span><span class="sxs-lookup"><span data-stu-id="f79da-122">If set, **DevQueryPrint** is called.</span></span> <span data-ttu-id="f79da-123">**DevQueryPrint** peut échouer si les configurations du document et de l’imprimante ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="f79da-123">**DevQueryPrint** may fail if the document and printer setups do not match.</span></span> <span data-ttu-id="f79da-124">La définition de cet indicateur entraîne la conservation des documents incompatibles dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="f79da-124">Setting this flag causes mismatched documents to be held in the queue.</span></span> |
| <span data-ttu-id="f79da-125">\_attribut imprimante \_ masqué</span><span class="sxs-lookup"><span data-stu-id="f79da-125">PRINTER\_ATTRIBUTE\_HIDDEN</span></span>              | <span data-ttu-id="f79da-126">Réservé.</span><span class="sxs-lookup"><span data-stu-id="f79da-126">Reserved.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="f79da-127">\_attribut Printer \_ KEEPPRINTEDJOBS</span><span class="sxs-lookup"><span data-stu-id="f79da-127">PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS</span></span>     | <span data-ttu-id="f79da-128">Si cette valeur est définie, les tâches sont conservées après leur impression.</span><span class="sxs-lookup"><span data-stu-id="f79da-128">If set, jobs are kept after they are printed.</span></span> <span data-ttu-id="f79da-129">S’il est désactivé, les travaux sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="f79da-129">If unset, jobs are deleted.</span></span>                                                                                                               |
| <span data-ttu-id="f79da-130">\_attribut imprimante \_ local</span><span class="sxs-lookup"><span data-stu-id="f79da-130">PRINTER\_ATTRIBUTE\_LOCAL</span></span>               | <span data-ttu-id="f79da-131">L’imprimante est une imprimante locale.</span><span class="sxs-lookup"><span data-stu-id="f79da-131">Printer is a local printer.</span></span>                                                                                                                                                             |
| <span data-ttu-id="f79da-132">attribut d’imprimante \_ \_ réseau</span><span class="sxs-lookup"><span data-stu-id="f79da-132">PRINTER\_ATTRIBUTE\_NETWORK</span></span>             | <span data-ttu-id="f79da-133">L’imprimante est une connexion d’imprimante réseau.</span><span class="sxs-lookup"><span data-stu-id="f79da-133">Printer is a network printer connection.</span></span>                                                                                                                                                |
| <span data-ttu-id="f79da-134">\_attribut Printer \_ publié</span><span class="sxs-lookup"><span data-stu-id="f79da-134">PRINTER\_ATTRIBUTE\_PUBLISHED</span></span>           | <span data-ttu-id="f79da-135">Indique si l’imprimante est publiée dans le service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="f79da-135">Indicates whether the printer is published in the directory service.</span></span>                                                                                                                    |
| <span data-ttu-id="f79da-136">\_attribut d’imprimante en \_ file d’attente</span><span class="sxs-lookup"><span data-stu-id="f79da-136">PRINTER\_ATTRIBUTE\_QUEUED</span></span>              | <span data-ttu-id="f79da-137">Si cette valeur est définie, l’imprimante est mise en file d’attente et commence l’impression une fois que la dernière page est mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="f79da-137">If set, the printer spools and starts printing after the last page is spooled.</span></span> <span data-ttu-id="f79da-138">Si la valeur n’est pas définie et que \_ l’attribut Printer \_ direct n’est pas défini, l’imprimante met en attente et imprime pendant la mise en attente.</span><span class="sxs-lookup"><span data-stu-id="f79da-138">If not set and PRINTER\_ATTRIBUTE\_DIRECT is not set, the printer spools and prints while spooling.</span></span>      |
| <span data-ttu-id="f79da-139">attribut d’imprimante \_ \_ RAW \_ uniquement</span><span class="sxs-lookup"><span data-stu-id="f79da-139">PRINTER\_ATTRIBUTE\_RAW\_ONLY</span></span>           | <span data-ttu-id="f79da-140">Indique que seuls les travaux d’impression de type de données brutes peuvent être mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="f79da-140">Indicates that only raw data type print jobs can be spooled.</span></span>                                                                                                                            |
| <span data-ttu-id="f79da-141">attribut d’imprimante \_ \_ partagé</span><span class="sxs-lookup"><span data-stu-id="f79da-141">PRINTER\_ATTRIBUTE\_SHARED</span></span>              | <span data-ttu-id="f79da-142">L’imprimante est partagée.</span><span class="sxs-lookup"><span data-stu-id="f79da-142">Printer is shared.</span></span>                                                                                                                                                                      |



 

<span data-ttu-id="f79da-143">Dans Windows XP et les versions ultérieures de Windows, la valeur suivante peut également être utilisée.</span><span class="sxs-lookup"><span data-stu-id="f79da-143">In Windows XP and later versions of Windows, the following value can also be used.</span></span>

| <span data-ttu-id="f79da-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="f79da-144">Value</span></span>                   | <span data-ttu-id="f79da-145">Signification</span><span class="sxs-lookup"><span data-stu-id="f79da-145">Meaning</span></span>                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f79da-146">\_télécopie d’attribut d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="f79da-146">PRINTER\_ATTRIBUTE\_FAX</span></span> | <span data-ttu-id="f79da-147">S’il est défini, l’imprimante est une imprimante-télécopieur.</span><span class="sxs-lookup"><span data-stu-id="f79da-147">If set, printer is a fax printer.</span></span> <span data-ttu-id="f79da-148">Cela ne peut être défini que par [**AddPrinter**](addprinter.md), mais il peut être récupéré par [**EnumPrinters**](enumprinters.md) et [**GetPrinter**](getprinter.md).</span><span class="sxs-lookup"><span data-stu-id="f79da-148">This can only be set by [**AddPrinter**](addprinter.md), but it can be retrieved by [**EnumPrinters**](enumprinters.md) and [**GetPrinter**](getprinter.md).</span></span> |



 

<span data-ttu-id="f79da-149">Dans Windows Vista et les versions ultérieures de Windows, les valeurs suivantes peuvent également être utilisées.</span><span class="sxs-lookup"><span data-stu-id="f79da-149">In Windows Vista and later versions of Windows, the following values can also be used.</span></span>

| <span data-ttu-id="f79da-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="f79da-150">Value</span></span>                               | <span data-ttu-id="f79da-151">Signification</span><span class="sxs-lookup"><span data-stu-id="f79da-151">Meaning</span></span>                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f79da-152">\_ \_ nom convivial de l’attribut d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="f79da-152">PRINTER\_ATTRIBUTE\_FRIENDLY\_NAME</span></span>  | <span data-ttu-id="f79da-153">Un ordinateur s’est connecté à cette imprimante et lui a donné un nom convivial.</span><span class="sxs-lookup"><span data-stu-id="f79da-153">A computer has connected to this printer and given it a friendly name.</span></span>           |
| <span data-ttu-id="f79da-154">\_ordinateur d’attribut d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="f79da-154">PRINTER\_ATTRIBUTE\_MACHINE</span></span>         | <span data-ttu-id="f79da-155">L’imprimante est une connexion par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f79da-155">Printer is a per-machine connection.</span></span>                                             |
| <span data-ttu-id="f79da-156">attribut d’imprimante \_ \_ Push \_ User</span><span class="sxs-lookup"><span data-stu-id="f79da-156">PRINTER\_ATTRIBUTE\_PUSHED\_USER</span></span>    | <span data-ttu-id="f79da-157">L’imprimante a été installée à l’aide de la stratégie d’utilisateur envoyer des connexions d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="f79da-157">The printer was installed by using the Push Printer Connections user policy.</span></span>     |
| <span data-ttu-id="f79da-158">attribut d’imprimante, \_ \_ \_ ordinateur poussé</span><span class="sxs-lookup"><span data-stu-id="f79da-158">PRINTER\_ATTRIBUTE\_PUSHED\_MACHINE</span></span> | <span data-ttu-id="f79da-159">L’imprimante a été installée à l’aide de la stratégie de l’ordinateur Push Printer Connections.</span><span class="sxs-lookup"><span data-stu-id="f79da-159">The printer was installed by using the Push Printer Connections computer policy.</span></span> |



 

</dd> <dt>

<span data-ttu-id="f79da-160">**DeviceNotSelectedTimeout**</span><span class="sxs-lookup"><span data-stu-id="f79da-160">**DeviceNotSelectedTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="f79da-161">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="f79da-161">This value is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f79da-162">**TransmissionRetryTimeout**</span><span class="sxs-lookup"><span data-stu-id="f79da-162">**TransmissionRetryTimeout**</span></span>
</dt> <dd>

<span data-ttu-id="f79da-163">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="f79da-163">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f79da-164">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f79da-164">Requirements</span></span>



| <span data-ttu-id="f79da-165">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f79da-165">Requirement</span></span> | <span data-ttu-id="f79da-166">Valeur</span><span class="sxs-lookup"><span data-stu-id="f79da-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f79da-167">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f79da-167">Minimum supported client</span></span><br/> | <span data-ttu-id="f79da-168">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f79da-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f79da-169">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f79da-169">Minimum supported server</span></span><br/> | <span data-ttu-id="f79da-170">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f79da-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f79da-171">En-tête</span><span class="sxs-lookup"><span data-stu-id="f79da-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="f79da-172"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f79da-172"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f79da-173">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="f79da-173">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f79da-174">**\_ \_ Infos sur \_ l’imprimante 5W** (Unicode) et **\_ \_ informations sur l’imprimante \_ 5A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f79da-174">**\_PRINTER\_INFO\_5W** (Unicode) and **\_PRINTER\_INFO\_5A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="f79da-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f79da-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f79da-176">Impression</span><span class="sxs-lookup"><span data-stu-id="f79da-176">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f79da-177">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="f79da-177">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f79da-178">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="f79da-178">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="f79da-179">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="f79da-179">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="f79da-180">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="f79da-180">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="f79da-181">**\_Infos sur l’imprimante \_ 1**</span><span class="sxs-lookup"><span data-stu-id="f79da-181">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="f79da-182">**\_Infos sur l’imprimante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f79da-182">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="f79da-183">**\_Infos sur l’imprimante \_ 3**</span><span class="sxs-lookup"><span data-stu-id="f79da-183">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="f79da-184">**\_Infos sur l’imprimante \_ 4**</span><span class="sxs-lookup"><span data-stu-id="f79da-184">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> </dl>

 

 




