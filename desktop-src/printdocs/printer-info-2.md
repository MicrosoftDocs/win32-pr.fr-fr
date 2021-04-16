---
description: La \_ structure info 2 de l’imprimante \_ spécifie des informations détaillées sur l’imprimante.
ms.assetid: 944cbfcd-9edf-4b60-a45c-9bb1839f8141
title: Structure PRINTER_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_2
- _PRINTER_INFO_2A
- _PRINTER_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b299cb1bbdd3ac2475b7a9f2b600bcd9652246d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529757"
---
# <a name="printer_info_2-structure"></a><span data-ttu-id="c5d89-103">\_Structure info 2 de l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="c5d89-103">PRINTER\_INFO\_2 structure</span></span>

<span data-ttu-id="c5d89-104">La **structure \_ info \_ 2** de l’imprimante spécifie des informations détaillées sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c5d89-104">The **PRINTER\_INFO\_2** structure specifies detailed printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5d89-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c5d89-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_2 {
  LPTSTR               pServerName;
  LPTSTR               pPrinterName;
  LPTSTR               pShareName;
  LPTSTR               pPortName;
  LPTSTR               pDriverName;
  LPTSTR               pComment;
  LPTSTR               pLocation;
  LPDEVMODE            pDevMode;
  LPTSTR               pSepFile;
  LPTSTR               pPrintProcessor;
  LPTSTR               pDatatype;
  LPTSTR               pParameters;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Attributes;
  DWORD                Priority;
  DWORD                DefaultPriority;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                Status;
  DWORD                cJobs;
  DWORD                AveragePPM;
} PRINTER_INFO_2, *PPRINTER_INFO_2;
```



## <a name="members"></a><span data-ttu-id="c5d89-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c5d89-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c5d89-107">**pServerName**</span><span class="sxs-lookup"><span data-stu-id="c5d89-107">**pServerName**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-108">Pointeur vers une chaîne se terminant par un caractère null qui identifie le serveur qui contrôle l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c5d89-108">A pointer to a null-terminated string identifying the server that controls the printer.</span></span> <span data-ttu-id="c5d89-109">Si cette chaîne est **null**, l’imprimante est contrôlée localement.</span><span class="sxs-lookup"><span data-stu-id="c5d89-109">If this string is **NULL**, the printer is controlled locally.</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-110">**pPrinterName**</span><span class="sxs-lookup"><span data-stu-id="c5d89-110">**pPrinterName**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c5d89-111">A pointer to a null-terminated string that specifies the name of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-112">**pShareName**</span><span class="sxs-lookup"><span data-stu-id="c5d89-112">**pShareName**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-113">Pointeur vers une chaîne se terminant par un caractère null qui identifie le point de partage de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c5d89-113">A pointer to a null-terminated string that identifies the share point for the printer.</span></span> <span data-ttu-id="c5d89-114">(Cette chaîne est utilisée uniquement si l’imprimante \_ Une \_ constante partagée d’attribut a été définie pour le membre **attributs** .)</span><span class="sxs-lookup"><span data-stu-id="c5d89-114">(This string is used only if the PRINTER\_ATTRIBUTE\_SHARED constant was set for the **Attributes** member.)</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-115">**pPortName**</span><span class="sxs-lookup"><span data-stu-id="c5d89-115">**pPortName**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-116">Pointeur vers une chaîne se terminant par un caractère null qui identifie le ou les ports utilisés pour transmettre des données à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c5d89-116">A pointer to a null-terminated string that identifies the port(s) used to transmit data to the printer.</span></span> <span data-ttu-id="c5d89-117">Si une imprimante est connectée à plusieurs ports, les noms de chaque port doivent être séparés par des virgules (par exemple, « LPT1 :, LPT2 :, LPT3 : »).</span><span class="sxs-lookup"><span data-stu-id="c5d89-117">If a printer is connected to more than one port, the names of each port must be separated by commas (for example, "LPT1:,LPT2:,LPT3:").</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-118">**pDriverName**</span><span class="sxs-lookup"><span data-stu-id="c5d89-118">**pDriverName**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-119">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c5d89-119">A pointer to a null-terminated string that specifies the name of the printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-120">**pComment**</span><span class="sxs-lookup"><span data-stu-id="c5d89-120">**pComment**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-121">Pointeur vers une chaîne se terminant par un caractère null qui fournit une brève description de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c5d89-121">A pointer to a null-terminated string that provides a brief description of the printer.</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-122">**pLocation**</span><span class="sxs-lookup"><span data-stu-id="c5d89-122">**pLocation**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-123">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’emplacement physique de l’imprimante (par exemple, « Bldg ».</span><span class="sxs-lookup"><span data-stu-id="c5d89-123">A pointer to a null-terminated string that specifies the physical location of the printer (for example, "Bldg.</span></span> <span data-ttu-id="c5d89-124">38, salle 1164»).</span><span class="sxs-lookup"><span data-stu-id="c5d89-124">38, Room 1164").</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-125">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="c5d89-125">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-126">Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) qui définit les données d’imprimante par défaut telles que l’orientation du papier et la résolution.</span><span class="sxs-lookup"><span data-stu-id="c5d89-126">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines default printer data such as the paper orientation and the resolution.</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-127">**pSepFile**</span><span class="sxs-lookup"><span data-stu-id="c5d89-127">**pSepFile**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-128">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du fichier utilisé pour créer la page de séparation.</span><span class="sxs-lookup"><span data-stu-id="c5d89-128">A pointer to a null-terminated string that specifies the name of the file used to create the separator page.</span></span> <span data-ttu-id="c5d89-129">Cette page est utilisée pour séparer les travaux d’impression envoyés à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c5d89-129">This page is used to separate print jobs sent to the printer.</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-130">**pPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="c5d89-130">**pPrintProcessor**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-131">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du processeur d’impression utilisé par l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c5d89-131">A pointer to a null-terminated string that specifies the name of the print processor used by the printer.</span></span> <span data-ttu-id="c5d89-132">Vous pouvez utiliser la fonction [**EnumPrintProcessors**](enumprintprocessors.md) pour obtenir la liste des processeurs d’impression installés sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="c5d89-132">You can use the [**EnumPrintProcessors**](enumprintprocessors.md) function to obtain a list of print processors installed on a server.</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-133">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="c5d89-133">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-134">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le type de données utilisé pour enregistrer le travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="c5d89-134">A pointer to a null-terminated string that specifies the data type used to record the print job.</span></span> <span data-ttu-id="c5d89-135">Vous pouvez utiliser la fonction [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) pour obtenir la liste des types de données pris en charge par un processeur d’impression spécifique.</span><span class="sxs-lookup"><span data-stu-id="c5d89-135">You can use the [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) function to obtain a list of data types supported by a specific print processor.</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-136">**pParameters**</span><span class="sxs-lookup"><span data-stu-id="c5d89-136">**pParameters**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-137">Pointeur vers une chaîne se terminant par un caractère null qui spécifie les paramètres du processeur d’impression par défaut.</span><span class="sxs-lookup"><span data-stu-id="c5d89-137">A pointer to a null-terminated string that specifies the default print-processor parameters.</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-138">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c5d89-138">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-139">Pointeur vers une structure [**de \_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) pour l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c5d89-139">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure for the printer.</span></span> <span data-ttu-id="c5d89-140">Ce membre peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c5d89-140">This member may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-141">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="c5d89-141">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-142">Attributs de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c5d89-142">The printer attributes.</span></span> <span data-ttu-id="c5d89-143">Ce membre peut être une combinaison raisonnable des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c5d89-143">This member can be any reasonable combination of the following values.</span></span>

| <span data-ttu-id="c5d89-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5d89-144">Value</span></span>                                   | <span data-ttu-id="c5d89-145">Signification</span><span class="sxs-lookup"><span data-stu-id="c5d89-145">Meaning</span></span>                                                                                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d89-146">attribut d’imprimante \_ \_ direct</span><span class="sxs-lookup"><span data-stu-id="c5d89-146">PRINTER\_ATTRIBUTE\_DIRECT</span></span>              | <span data-ttu-id="c5d89-147">Le travail est envoyé directement à l’imprimante (il n’est pas mis en file d’attente).</span><span class="sxs-lookup"><span data-stu-id="c5d89-147">Job is sent directly to the printer (it is not spooled).</span></span>                                                                                                                                |
| <span data-ttu-id="c5d89-148">l’attribut d’imprimante se \_ \_ \_ termine en \_ premier</span><span class="sxs-lookup"><span data-stu-id="c5d89-148">PRINTER\_ATTRIBUTE\_DO\_COMPLETE\_FIRST</span></span> | <span data-ttu-id="c5d89-149">Si l’imprimante est définie et que l’imprimante est définie pour l’impression pendant la mise en file d’attente, toutes les tâches dont l’attente est terminée sont planifiées pour s’imprimer avant les travaux qui n’ont pas terminé la mise en attente.</span><span class="sxs-lookup"><span data-stu-id="c5d89-149">If set and printer is set for print-while-spooling, any jobs that have completed spooling are scheduled to print before jobs that have not completed spooling.</span></span>                          |
| <span data-ttu-id="c5d89-150">attribut d’imprimante \_ \_ Enable \_ DEVQ</span><span class="sxs-lookup"><span data-stu-id="c5d89-150">PRINTER\_ATTRIBUTE\_ENABLE\_DEVQ</span></span>        | <span data-ttu-id="c5d89-151">Si cette valeur est définie, **DevQueryPrint** est appelé.</span><span class="sxs-lookup"><span data-stu-id="c5d89-151">If set, **DevQueryPrint** is called.</span></span> <span data-ttu-id="c5d89-152">**DevQueryPrint** peut échouer si les configurations du document et de l’imprimante ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="c5d89-152">**DevQueryPrint** may fail if the document and printer setups do not match.</span></span> <span data-ttu-id="c5d89-153">La définition de cet indicateur entraîne la conservation des documents incompatibles dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="c5d89-153">Setting this flag causes mismatched documents to be held in the queue.</span></span> |
| <span data-ttu-id="c5d89-154">\_attribut imprimante \_ masqué</span><span class="sxs-lookup"><span data-stu-id="c5d89-154">PRINTER\_ATTRIBUTE\_HIDDEN</span></span>              | <span data-ttu-id="c5d89-155">Réservé.</span><span class="sxs-lookup"><span data-stu-id="c5d89-155">Reserved.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="c5d89-156">\_attribut Printer \_ KEEPPRINTEDJOBS</span><span class="sxs-lookup"><span data-stu-id="c5d89-156">PRINTER\_ATTRIBUTE\_KEEPPRINTEDJOBS</span></span>     | <span data-ttu-id="c5d89-157">Si cette valeur est définie, les tâches sont conservées après leur impression.</span><span class="sxs-lookup"><span data-stu-id="c5d89-157">If set, jobs are kept after they are printed.</span></span> <span data-ttu-id="c5d89-158">S’il est désactivé, les travaux sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="c5d89-158">If unset, jobs are deleted.</span></span>                                                                                                               |
| <span data-ttu-id="c5d89-159">\_attribut imprimante \_ local</span><span class="sxs-lookup"><span data-stu-id="c5d89-159">PRINTER\_ATTRIBUTE\_LOCAL</span></span>               | <span data-ttu-id="c5d89-160">L’imprimante est une imprimante locale.</span><span class="sxs-lookup"><span data-stu-id="c5d89-160">Printer is a local printer.</span></span>                                                                                                                                                             |
| <span data-ttu-id="c5d89-161">attribut d’imprimante \_ \_ réseau</span><span class="sxs-lookup"><span data-stu-id="c5d89-161">PRINTER\_ATTRIBUTE\_NETWORK</span></span>             | <span data-ttu-id="c5d89-162">L’imprimante est une connexion d’imprimante réseau.</span><span class="sxs-lookup"><span data-stu-id="c5d89-162">Printer is a network printer connection.</span></span>                                                                                                                                                |
| <span data-ttu-id="c5d89-163">\_attribut Printer \_ publié</span><span class="sxs-lookup"><span data-stu-id="c5d89-163">PRINTER\_ATTRIBUTE\_PUBLISHED</span></span>           | <span data-ttu-id="c5d89-164">Indique si l’imprimante est publiée dans le service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="c5d89-164">Indicates whether the printer is published in the directory service.</span></span>                                                                                                                    |
| <span data-ttu-id="c5d89-165">\_attribut d’imprimante en \_ file d’attente</span><span class="sxs-lookup"><span data-stu-id="c5d89-165">PRINTER\_ATTRIBUTE\_QUEUED</span></span>              | <span data-ttu-id="c5d89-166">Si cette valeur est définie, l’imprimante est mise en file d’attente et commence l’impression une fois que la dernière page est mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="c5d89-166">If set, the printer spools and starts printing after the last page is spooled.</span></span> <span data-ttu-id="c5d89-167">Si la valeur n’est pas définie et que \_ l’attribut Printer \_ direct n’est pas défini, l’imprimante met en attente et imprime pendant la mise en attente.</span><span class="sxs-lookup"><span data-stu-id="c5d89-167">If not set and PRINTER\_ATTRIBUTE\_DIRECT is not set, the printer spools and prints while spooling.</span></span>      |
| <span data-ttu-id="c5d89-168">attribut d’imprimante \_ \_ RAW \_ uniquement</span><span class="sxs-lookup"><span data-stu-id="c5d89-168">PRINTER\_ATTRIBUTE\_RAW\_ONLY</span></span>           | <span data-ttu-id="c5d89-169">Indique que seuls les travaux d’impression de type de données brutes peuvent être mis en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="c5d89-169">Indicates that only raw data type print jobs can be spooled.</span></span>                                                                                                                            |
| <span data-ttu-id="c5d89-170">attribut d’imprimante \_ \_ partagé</span><span class="sxs-lookup"><span data-stu-id="c5d89-170">PRINTER\_ATTRIBUTE\_SHARED</span></span>              | <span data-ttu-id="c5d89-171">L’imprimante est partagée.</span><span class="sxs-lookup"><span data-stu-id="c5d89-171">Printer is shared.</span></span>                                                                                                                                                                      |



 

<span data-ttu-id="c5d89-172">Dans Windows XP et les versions ultérieures de Windows, la valeur suivante peut également être utilisée.</span><span class="sxs-lookup"><span data-stu-id="c5d89-172">In Windows XP and later versions of Windows, the following value can also be used.</span></span>

| <span data-ttu-id="c5d89-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5d89-173">Value</span></span>                   | <span data-ttu-id="c5d89-174">Signification</span><span class="sxs-lookup"><span data-stu-id="c5d89-174">Meaning</span></span>                                                                                                                                                                                           |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d89-175">\_télécopie d’attribut d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="c5d89-175">PRINTER\_ATTRIBUTE\_FAX</span></span> | <span data-ttu-id="c5d89-176">S’il est défini, l’imprimante est une imprimante-télécopieur.</span><span class="sxs-lookup"><span data-stu-id="c5d89-176">If set, printer is a fax printer.</span></span> <span data-ttu-id="c5d89-177">Cela ne peut être défini que par [**AddPrinter**](addprinter.md), mais il peut être récupéré par [**EnumPrinters**](enumprinters.md) et [**GetPrinter**](getprinter.md).</span><span class="sxs-lookup"><span data-stu-id="c5d89-177">This can only be set by [**AddPrinter**](addprinter.md), but it can be retrieved by [**EnumPrinters**](enumprinters.md) and [**GetPrinter**](getprinter.md).</span></span> |



 

<span data-ttu-id="c5d89-178">Dans Windows Vista et les versions ultérieures de Windows, les valeurs suivantes peuvent également être utilisées.</span><span class="sxs-lookup"><span data-stu-id="c5d89-178">In Windows Vista and later versions of Windows, the following values can also be used.</span></span>

| <span data-ttu-id="c5d89-179">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5d89-179">Value</span></span>                               | <span data-ttu-id="c5d89-180">Signification</span><span class="sxs-lookup"><span data-stu-id="c5d89-180">Meaning</span></span>                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c5d89-181">\_ \_ nom convivial de l’attribut d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="c5d89-181">PRINTER\_ATTRIBUTE\_FRIENDLY\_NAME</span></span>  | <span data-ttu-id="c5d89-182">Un ordinateur s’est connecté à cette imprimante et lui a donné un nom convivial.</span><span class="sxs-lookup"><span data-stu-id="c5d89-182">A computer has connected to this printer and given it a friendly name.</span></span>           |
| <span data-ttu-id="c5d89-183">\_ordinateur d’attribut d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="c5d89-183">PRINTER\_ATTRIBUTE\_MACHINE</span></span>         | <span data-ttu-id="c5d89-184">L’imprimante est une connexion par ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c5d89-184">Printer is a per-machine connection.</span></span>                                             |
| <span data-ttu-id="c5d89-185">attribut d’imprimante \_ \_ Push \_ User</span><span class="sxs-lookup"><span data-stu-id="c5d89-185">PRINTER\_ATTRIBUTE\_PUSHED\_USER</span></span>    | <span data-ttu-id="c5d89-186">L’imprimante a été installée à l’aide de la stratégie d’utilisateur envoyer des connexions d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c5d89-186">The printer was installed by using the Push Printer Connections user policy.</span></span>     |
| <span data-ttu-id="c5d89-187">attribut d’imprimante, \_ \_ \_ ordinateur poussé</span><span class="sxs-lookup"><span data-stu-id="c5d89-187">PRINTER\_ATTRIBUTE\_PUSHED\_MACHINE</span></span> | <span data-ttu-id="c5d89-188">L’imprimante a été installée à l’aide de la stratégie de l’ordinateur Push Printer Connections.</span><span class="sxs-lookup"><span data-stu-id="c5d89-188">The printer was installed by using the Push Printer Connections computer policy.</span></span> |



 

<span data-ttu-id="c5d89-189">Dans Windows Server 2003, la valeur suivante peut également être utilisée.</span><span class="sxs-lookup"><span data-stu-id="c5d89-189">In Windows Server 2003, the following value can also be used.</span></span>

| <span data-ttu-id="c5d89-190">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5d89-190">Value</span></span>                  | <span data-ttu-id="c5d89-191">Signification</span><span class="sxs-lookup"><span data-stu-id="c5d89-191">Meaning</span></span>                                                                 |
|------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="c5d89-192">attribut d’imprimante \_ \_ TS</span><span class="sxs-lookup"><span data-stu-id="c5d89-192">PRINTER\_ATTRIBUTE\_TS</span></span> | <span data-ttu-id="c5d89-193">Indique que l’imprimante est actuellement connectée via un serveur Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="c5d89-193">Indicates the printer is currently connected through a terminal server.</span></span> |



 

</dd> <dt>

<span data-ttu-id="c5d89-194">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="c5d89-194">**Priority**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-195">Valeur de priorité que le spouleur utilise pour router les travaux d’impression.</span><span class="sxs-lookup"><span data-stu-id="c5d89-195">A priority value that the spooler uses to route print jobs.</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-196">**DefaultPriority**</span><span class="sxs-lookup"><span data-stu-id="c5d89-196">**DefaultPriority**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-197">Valeur de priorité par défaut assignée à chaque travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="c5d89-197">The default priority value assigned to each print job.</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-198">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="c5d89-198">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-199">Heure à laquelle l’imprimante imprime un travail.</span><span class="sxs-lookup"><span data-stu-id="c5d89-199">The earliest time at which the printer will print a job.</span></span> <span data-ttu-id="c5d89-200">Cette valeur est exprimée sous la forme de minutes écoulées depuis 12:00 AM GMT (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="c5d89-200">This value is expressed as minutes elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-201">**UntilTime**</span><span class="sxs-lookup"><span data-stu-id="c5d89-201">**UntilTime**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-202">Dernière heure à laquelle l’imprimante imprime un travail.</span><span class="sxs-lookup"><span data-stu-id="c5d89-202">The latest time at which the printer will print a job.</span></span> <span data-ttu-id="c5d89-203">Cette valeur est exprimée sous la forme de minutes écoulées depuis 12:00 AM GMT (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="c5d89-203">This value is expressed as minutes elapsed since 12:00 AM GMT (Greenwich Mean Time).</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-204">**État**</span><span class="sxs-lookup"><span data-stu-id="c5d89-204">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-205">État de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c5d89-205">The printer status.</span></span> <span data-ttu-id="c5d89-206">Ce membre peut être une combinaison raisonnable des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c5d89-206">This member can be any reasonable combination of the following values.</span></span>



| <span data-ttu-id="c5d89-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5d89-207">Value</span></span>                               | <span data-ttu-id="c5d89-208">Signification</span><span class="sxs-lookup"><span data-stu-id="c5d89-208">Meaning</span></span>                                                          |
|-------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c5d89-209">État de l’imprimante \_ \_ occupé</span><span class="sxs-lookup"><span data-stu-id="c5d89-209">PRINTER\_STATUS\_BUSY</span></span>               | <span data-ttu-id="c5d89-210">L'imprimante est occupée.</span><span class="sxs-lookup"><span data-stu-id="c5d89-210">The printer is busy.</span></span>                                             |
| <span data-ttu-id="c5d89-211">porte de l’état de l’imprimante \_ \_ \_ ouverte</span><span class="sxs-lookup"><span data-stu-id="c5d89-211">PRINTER\_STATUS\_DOOR\_OPEN</span></span>         | <span data-ttu-id="c5d89-212">La porte de l’imprimante est ouverte.</span><span class="sxs-lookup"><span data-stu-id="c5d89-212">The printer door is open.</span></span>                                        |
| <span data-ttu-id="c5d89-213">\_erreur d’état de l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="c5d89-213">PRINTER\_STATUS\_ERROR</span></span>              | <span data-ttu-id="c5d89-214">L'imprimante est dans un état d'erreur.</span><span class="sxs-lookup"><span data-stu-id="c5d89-214">The printer is in an error state.</span></span>                                |
| <span data-ttu-id="c5d89-215">État de l’imprimante en cours \_ \_ d’initialisation</span><span class="sxs-lookup"><span data-stu-id="c5d89-215">PRINTER\_STATUS\_INITIALIZING</span></span>       | <span data-ttu-id="c5d89-216">L'imprimante s'initialise.</span><span class="sxs-lookup"><span data-stu-id="c5d89-216">The printer is initializing.</span></span>                                     |
| <span data-ttu-id="c5d89-217">\_e/s d’état d’imprimante \_ \_ active</span><span class="sxs-lookup"><span data-stu-id="c5d89-217">PRINTER\_STATUS\_IO\_ACTIVE</span></span>         | <span data-ttu-id="c5d89-218">L’imprimante est dans un état d’entrée/sortie actif</span><span class="sxs-lookup"><span data-stu-id="c5d89-218">The printer is in an active input/output state</span></span>                   |
| <span data-ttu-id="c5d89-219">\_ \_ flux manuel de l’état de l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="c5d89-219">PRINTER\_STATUS\_MANUAL\_FEED</span></span>       | <span data-ttu-id="c5d89-220">L’imprimante est dans un état de flux manuel.</span><span class="sxs-lookup"><span data-stu-id="c5d89-220">The printer is in a manual feed state.</span></span>                           |
| <span data-ttu-id="c5d89-221">État de l’imprimante \_ \_ non \_ toner</span><span class="sxs-lookup"><span data-stu-id="c5d89-221">PRINTER\_STATUS\_NO\_TONER</span></span>          | <span data-ttu-id="c5d89-222">L'imprimante est sans toner.</span><span class="sxs-lookup"><span data-stu-id="c5d89-222">The printer is out of toner.</span></span>                                     |
| <span data-ttu-id="c5d89-223">l’état de l’imprimante \_ \_ n’est pas \_ disponible</span><span class="sxs-lookup"><span data-stu-id="c5d89-223">PRINTER\_STATUS\_NOT\_AVAILABLE</span></span>     | <span data-ttu-id="c5d89-224">L’imprimante n’est pas disponible pour l’impression.</span><span class="sxs-lookup"><span data-stu-id="c5d89-224">The printer is not available for printing.</span></span>                       |
| <span data-ttu-id="c5d89-225">État de l’imprimante \_ \_ hors connexion</span><span class="sxs-lookup"><span data-stu-id="c5d89-225">PRINTER\_STATUS\_OFFLINE</span></span>            | <span data-ttu-id="c5d89-226">L'imprimante est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="c5d89-226">The printer is offline.</span></span>                                          |
| <span data-ttu-id="c5d89-227">\_ \_ mémoire insuffisante sur l’état \_ de \_ l’imprimante</span><span class="sxs-lookup"><span data-stu-id="c5d89-227">PRINTER\_STATUS\_OUT\_OF\_MEMORY</span></span>    | <span data-ttu-id="c5d89-228">La mémoire de l’imprimante est insuffisante.</span><span class="sxs-lookup"><span data-stu-id="c5d89-228">The printer has run out of memory.</span></span>                               |
| <span data-ttu-id="c5d89-229">bac de sortie de l’état de l’imprimante \_ \_ \_ \_ plein</span><span class="sxs-lookup"><span data-stu-id="c5d89-229">PRINTER\_STATUS\_OUTPUT\_BIN\_FULL</span></span>  | <span data-ttu-id="c5d89-230">Le bac de sortie de l'imprimante est plein.</span><span class="sxs-lookup"><span data-stu-id="c5d89-230">The printer's output bin is full.</span></span>                                |
| <span data-ttu-id="c5d89-231">PAGE État de l’imprimante \_ \_ \_ chargeur</span><span class="sxs-lookup"><span data-stu-id="c5d89-231">PRINTER\_STATUS\_PAGE\_PUNT</span></span>         | <span data-ttu-id="c5d89-232">L’imprimante ne peut pas imprimer la page active.</span><span class="sxs-lookup"><span data-stu-id="c5d89-232">The printer cannot print the current page.</span></span>                       |
| <span data-ttu-id="c5d89-233">\_ \_ bourrage papier sur l’état de l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="c5d89-233">PRINTER\_STATUS\_PAPER\_JAM</span></span>         | <span data-ttu-id="c5d89-234">Le papier est coincé dans l’imprimante</span><span class="sxs-lookup"><span data-stu-id="c5d89-234">Paper is jammed in the printer</span></span>                                   |
| <span data-ttu-id="c5d89-235">\_ \_ sortie papier de l’état de l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="c5d89-235">PRINTER\_STATUS\_PAPER\_OUT</span></span>         | <span data-ttu-id="c5d89-236">L’imprimante n’est plus imprimée.</span><span class="sxs-lookup"><span data-stu-id="c5d89-236">The printer is out of paper.</span></span>                                     |
| <span data-ttu-id="c5d89-237">\_ \_ problème papier sur l’état de l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="c5d89-237">PRINTER\_STATUS\_PAPER\_PROBLEM</span></span>     | <span data-ttu-id="c5d89-238">L’imprimante présente un problème de papier.</span><span class="sxs-lookup"><span data-stu-id="c5d89-238">The printer has a paper problem.</span></span>                                 |
| <span data-ttu-id="c5d89-239">État de l’imprimante \_ \_ suspendu</span><span class="sxs-lookup"><span data-stu-id="c5d89-239">PRINTER\_STATUS\_PAUSED</span></span>             | <span data-ttu-id="c5d89-240">L’imprimante est suspendue.</span><span class="sxs-lookup"><span data-stu-id="c5d89-240">The printer is paused.</span></span>                                           |
| <span data-ttu-id="c5d89-241">État de l’imprimante \_ \_ en attente de \_ suppression</span><span class="sxs-lookup"><span data-stu-id="c5d89-241">PRINTER\_STATUS\_PENDING\_DELETION</span></span>  | <span data-ttu-id="c5d89-242">L’imprimante est en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="c5d89-242">The printer is being deleted.</span></span>                                    |
| <span data-ttu-id="c5d89-243">État de l’imprimante \_ \_ économie d’énergie \_</span><span class="sxs-lookup"><span data-stu-id="c5d89-243">PRINTER\_STATUS\_POWER\_SAVE</span></span>        | <span data-ttu-id="c5d89-244">L'imprimante est en mode mise en veille.</span><span class="sxs-lookup"><span data-stu-id="c5d89-244">The printer is in power save mode.</span></span>                               |
| <span data-ttu-id="c5d89-245">\_impression de \_ l’état de l’imprimante</span><span class="sxs-lookup"><span data-stu-id="c5d89-245">PRINTER\_STATUS\_PRINTING</span></span>           | <span data-ttu-id="c5d89-246">L’imprimante est en cours d’impression.</span><span class="sxs-lookup"><span data-stu-id="c5d89-246">The printer is printing.</span></span>                                         |
| <span data-ttu-id="c5d89-247">traitement de l’état de l’imprimante \_ \_</span><span class="sxs-lookup"><span data-stu-id="c5d89-247">PRINTER\_STATUS\_PROCESSING</span></span>         | <span data-ttu-id="c5d89-248">L’imprimante est en cours de traitement d’un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="c5d89-248">The printer is processing a print job.</span></span>                           |
| <span data-ttu-id="c5d89-249">serveur d’état d’imprimante \_ \_ \_ inconnu</span><span class="sxs-lookup"><span data-stu-id="c5d89-249">PRINTER\_STATUS\_SERVER\_UNKNOWN</span></span>    | <span data-ttu-id="c5d89-250">L’état de l’imprimante est inconnu.</span><span class="sxs-lookup"><span data-stu-id="c5d89-250">The printer status is unknown.</span></span>                                   |
| <span data-ttu-id="c5d89-251">\_toner d' \_ état \_ faible de l’imprimante</span><span class="sxs-lookup"><span data-stu-id="c5d89-251">PRINTER\_STATUS\_TONER\_LOW</span></span>         | <span data-ttu-id="c5d89-252">L’imprimante manque de toner.</span><span class="sxs-lookup"><span data-stu-id="c5d89-252">The printer is low on toner.</span></span>                                     |
| <span data-ttu-id="c5d89-253">INTERVENTION de l’utilisateur sur l’état de l’imprimante \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="c5d89-253">PRINTER\_STATUS\_USER\_INTERVENTION</span></span> | <span data-ttu-id="c5d89-254">L’imprimante a une erreur qui oblige l’utilisateur à effectuer une opération.</span><span class="sxs-lookup"><span data-stu-id="c5d89-254">The printer has an error that requires the user to do something.</span></span> |
| <span data-ttu-id="c5d89-255">État de l’imprimante en \_ \_ attente</span><span class="sxs-lookup"><span data-stu-id="c5d89-255">PRINTER\_STATUS\_WAITING</span></span>            | <span data-ttu-id="c5d89-256">L’imprimante est en attente.</span><span class="sxs-lookup"><span data-stu-id="c5d89-256">The printer is waiting.</span></span>                                          |
| <span data-ttu-id="c5d89-257">État de l’imprimante \_ \_ préchauffage \_</span><span class="sxs-lookup"><span data-stu-id="c5d89-257">PRINTER\_STATUS\_WARMING\_UP</span></span>        | <span data-ttu-id="c5d89-258">L'imprimante s'allume.</span><span class="sxs-lookup"><span data-stu-id="c5d89-258">The printer is warming up.</span></span>                                       |



 

</dd> <dt>

<span data-ttu-id="c5d89-259">**cJobs**</span><span class="sxs-lookup"><span data-stu-id="c5d89-259">**cJobs**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-260">Nombre de travaux d’impression qui ont été mis en file d’attente pour l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c5d89-260">The number of print jobs that have been queued for the printer.</span></span>

</dd> <dt>

<span data-ttu-id="c5d89-261">**AveragePPM**</span><span class="sxs-lookup"><span data-stu-id="c5d89-261">**AveragePPM**</span></span>
</dt> <dd>

<span data-ttu-id="c5d89-262">Nombre moyen de pages par minute qui ont été imprimées sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c5d89-262">The average number of pages per minute that have been printed on the printer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5d89-263">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5d89-263">Requirements</span></span>



| <span data-ttu-id="c5d89-264">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5d89-264">Requirement</span></span> | <span data-ttu-id="c5d89-265">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5d89-265">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d89-266">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5d89-266">Minimum supported client</span></span><br/> | <span data-ttu-id="c5d89-267">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5d89-267">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c5d89-268">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5d89-268">Minimum supported server</span></span><br/> | <span data-ttu-id="c5d89-269">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5d89-269">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c5d89-270">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5d89-270">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5d89-271"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5d89-271"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c5d89-272">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="c5d89-272">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c5d89-273">**\_ \_ Infos sur \_ l’imprimante 2S** (Unicode) et **\_ \_ infos sur l’imprimante \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c5d89-273">**\_PRINTER\_INFO\_2W** (Unicode) and **\_PRINTER\_INFO\_2A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="c5d89-274">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5d89-274">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d89-275">Impression</span><span class="sxs-lookup"><span data-stu-id="c5d89-275">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c5d89-276">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="c5d89-276">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="c5d89-277">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="c5d89-277">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[<span data-ttu-id="c5d89-278">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="c5d89-278">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="c5d89-279">**\_Infos sur l’imprimante \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c5d89-279">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="c5d89-280">**\_Infos sur l’imprimante \_ 3**</span><span class="sxs-lookup"><span data-stu-id="c5d89-280">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="c5d89-281">**\_Infos sur l’imprimante \_ 4**</span><span class="sxs-lookup"><span data-stu-id="c5d89-281">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="c5d89-282">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="c5d89-282">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

