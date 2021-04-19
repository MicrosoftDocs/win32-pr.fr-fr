---
description: Le fournisseur SNMP prend en charge l’écriture dans les fichiers journaux et dans le débogueur.
ms.assetid: 66627927-2eee-4d56-a74b-f86147ad7711
ms.tgt_platform: multiple
title: Événements SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b133d2fc81c76949439b3e1f26d1fc448f0b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518171"
---
# <a name="snmp-events"></a><span data-ttu-id="04b53-103">Événements SNMP</span><span class="sxs-lookup"><span data-stu-id="04b53-103">SNMP Events</span></span>

<span data-ttu-id="04b53-104">Le fournisseur SNMP prend en charge l’écriture dans les fichiers journaux et dans le débogueur.</span><span class="sxs-lookup"><span data-stu-id="04b53-104">The SNMP provider supports writing to log files and to the debugger.</span></span>

> [!Note]  
> <span data-ttu-id="04b53-105">Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="04b53-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="04b53-106">Un certain nombre de clés de Registre et de valeurs définissent le niveau et le type de journalisation en cours de génération :</span><span class="sxs-lookup"><span data-stu-id="04b53-106">A number of registry keys and values define the level and type of logging currently being generated:</span></span>

-   <span data-ttu-id="04b53-107">Débogage</span><span class="sxs-lookup"><span data-stu-id="04b53-107">Debugging</span></span>

    <span data-ttu-id="04b53-108">La clé de Registre **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ WBEM \\ Provider \\ Logging** contient la valeur de journalisation qui indique si les informations peuvent être écrites dans le débogueur.</span><span class="sxs-lookup"><span data-stu-id="04b53-108">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\PROVIDERS\\LOGGING** registry key contains the logging value that indicates whether information can be written to the debugger.</span></span> <span data-ttu-id="04b53-109">La valeur de journalisation est définie sur 0 pour désactiver la sortie de débogage ou 1 pour l’activer.</span><span class="sxs-lookup"><span data-stu-id="04b53-109">The logging value is set either to 0 to disable debugging output or 1 to enable it.</span></span> <span data-ttu-id="04b53-110">La journalisation est une valeur de Registre \_ DWORD.</span><span class="sxs-lookup"><span data-stu-id="04b53-110">Logging is a REG\_DWORD value.</span></span>

-   <span data-ttu-id="04b53-111">Journalisation</span><span class="sxs-lookup"><span data-stu-id="04b53-111">Logging</span></span>

    <span data-ttu-id="04b53-112">La clé de Registre WBEMSNMP de la clé de Registre **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ WBEM \\ \\ \\** Provider contient toutes les informations de journalisation spécifiques au fournisseur SNMP.</span><span class="sxs-lookup"><span data-stu-id="04b53-112">The **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\MICROSOFT\\WBEM\\PROVIDERS\\LOGGING\\WBEMSNMP** registry key holds all of the logging information specific to the SNMP provider.</span></span> <span data-ttu-id="04b53-113">Le tableau suivant répertorie les valeurs associées à cette clé.</span><span class="sxs-lookup"><span data-stu-id="04b53-113">The following table lists the values associated with this key.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="04b53-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="04b53-114">Value</span></span></th>
<th><span data-ttu-id="04b53-115">Description</span><span class="sxs-lookup"><span data-stu-id="04b53-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="04b53-116">Type</span><span class="sxs-lookup"><span data-stu-id="04b53-116">Type</span></span></td>
<td><span data-ttu-id="04b53-117"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="04b53-117"><strong>REG_SZ</strong></span></span><br/> <span data-ttu-id="04b53-118">Prend l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="04b53-118">Takes one of the following values:</span></span><br/> <span data-ttu-id="04b53-119">&quot;Fichier &quot; = (valeur par défaut) envoie la sortie de débogage à un fichier.</span><span class="sxs-lookup"><span data-stu-id="04b53-119">&quot;File&quot; = (Default) Sends debugging output to a file.</span></span><br/> <span data-ttu-id="04b53-120">&quot;Debugger &quot; = envoie la sortie de débogage au débogueur.</span><span class="sxs-lookup"><span data-stu-id="04b53-120">&quot;Debugger&quot; = Sends debugging output to the debugger.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04b53-121">MaxFileSize</span><span class="sxs-lookup"><span data-stu-id="04b53-121">MaxFileSize</span></span></td>
<td><span data-ttu-id="04b53-122"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="04b53-122"><strong>REG_DWORD</strong></span></span><br/> <span data-ttu-id="04b53-123">Prend des valeurs entières comprises entre 1024 et 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="04b53-123">Takes integer values from 1024 to 2^32-1.</span></span> <span data-ttu-id="04b53-124">La valeur correspond à la taille maximale autorisée, en octets, pour le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="04b53-124">The value is the maximum allowed size in bytes for the log file.</span></span> <span data-ttu-id="04b53-125">Si la valeur est inférieure à 1024, le mécanisme de journalisation utilise la valeur 1024.</span><span class="sxs-lookup"><span data-stu-id="04b53-125">If less than 1024, the logging mechanism uses a value of 1024.</span></span> <span data-ttu-id="04b53-126">Une taille minimale de 8 Ko est recommandée pour cette valeur.</span><span class="sxs-lookup"><span data-stu-id="04b53-126">A minimum size of 8 KB is recommended for this value.</span></span> <span data-ttu-id="04b53-127">Lorsque le fichier atteint la taille spécifiée par MaxFileSize, le nom de fichier est précédé d’un caractère « ~ » et un nouveau fichier est créé.</span><span class="sxs-lookup"><span data-stu-id="04b53-127">When the file reaches the size specified by MaxFileSize, the file name is prepended with a '~' character and a new file is created.</span></span> <span data-ttu-id="04b53-128">Par conséquent, l’espace disque maximal requis pour la journalisation est le double de cette valeur.</span><span class="sxs-lookup"><span data-stu-id="04b53-128">Therefore, the maximum disk space required for logging is twice this value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="04b53-129">Fichier</span><span class="sxs-lookup"><span data-stu-id="04b53-129">File</span></span></td>
<td><span data-ttu-id="04b53-130"><strong>REG_SZ</strong></span><span class="sxs-lookup"><span data-stu-id="04b53-130"><strong>REG_SZ</strong></span></span><br/> <span data-ttu-id="04b53-131">Définit le nom du fichier dans lequel la sortie de débogage est envoyée lorsque le type de journalisation est défini sur « file ».</span><span class="sxs-lookup"><span data-stu-id="04b53-131">Defines the name of the file to which the debugging output is sent when the logging type is set to 'File'.</span></span> <span data-ttu-id="04b53-132">La valeur par défaut est' <WBEMLOGS> \wbemsnmp.log. '</span><span class="sxs-lookup"><span data-stu-id="04b53-132">The default value is '<WBEMLOGS>\wbemsnmp.log.'</span></span> <span data-ttu-id="04b53-133">Si le <WBEMLOGS> Répertoire ne peut pas être déterminé à partir de la section du Registre WMI, la valeur par défaut est « c:\wbemsnmp.log ».</span><span class="sxs-lookup"><span data-stu-id="04b53-133">If the <WBEMLOGS> directory cannot be determined from the WMI registry section, the value defaults to 'c:\wbemsnmp.log'.</span></span> <span data-ttu-id="04b53-134">Si un partage est utilisé, tel que \\ machine\share\wbemsnmp.log ou M:\wbemsnmp.log où M : est \\ machine\share, le compte système local sur lequel WMI s’exécute doit disposer de droits d’accès en lecture/écriture au \\ machine\share.</span><span class="sxs-lookup"><span data-stu-id="04b53-134">If a share is used, such as \\machine\share\wbemsnmp.log or M:\wbemsnmp.log where M: is \\machine\share, the local SYSTEM account on which WMI runs must have read/write access rights to the \\machine\share.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="04b53-135">Level</span><span class="sxs-lookup"><span data-stu-id="04b53-135">Level</span></span></td>
<td><span data-ttu-id="04b53-136"><strong>REG_DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="04b53-136"><strong>REG_DWORD</strong></span></span><br/> <span data-ttu-id="04b53-137">Prend des valeurs entières comprises entre 0 et 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="04b53-137">Takes integer values from 0 through 2^32-1.</span></span> <span data-ttu-id="04b53-138">La valeur est un masque logique constitué de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="04b53-138">The value is a logical mask consisting of 32 bits.</span></span> <span data-ttu-id="04b53-139">Les masques de bits suivants sont combinés pour définir le type de sortie de débogage générée :</span><span class="sxs-lookup"><span data-stu-id="04b53-139">The following bit masks are combined to define the type of debugging output generated:</span></span><br/>
<ul>
<li><span data-ttu-id="04b53-140">0 : fournisseur de classes SNMP appels de méthode <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a></span><span class="sxs-lookup"><span data-stu-id="04b53-140">0: SNMP class provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> method invocations</span></span></li>
<li><span data-ttu-id="04b53-141">1 : implémentation du fournisseur de classes SNMP</span><span class="sxs-lookup"><span data-stu-id="04b53-141">1: SNMP class provider implementation</span></span></li>
<li><span data-ttu-id="04b53-142">2 : fournisseur d’instance SNMP appels de méthode <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a></span><span class="sxs-lookup"><span data-stu-id="04b53-142">2: SNMP instance provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> method invocations</span></span></li>
<li><span data-ttu-id="04b53-143">3 : implémentation du fournisseur d’instance SNMP</span><span class="sxs-lookup"><span data-stu-id="04b53-143">3: SNMP instance provider implementation</span></span></li>
<li><span data-ttu-id="04b53-144">4 : bibliothèque de classes SNMP</span><span class="sxs-lookup"><span data-stu-id="04b53-144">4: SNMP class library</span></span></li>
<li><span data-ttu-id="04b53-145">5 : STOCKAGE SMIR SNMP</span><span class="sxs-lookup"><span data-stu-id="04b53-145">5: SNMP SMIR</span></span></li>
<li><span data-ttu-id="04b53-146">6 : corrélation SNMP</span><span class="sxs-lookup"><span data-stu-id="04b53-146">6: SNMP correlator</span></span></li>
<li><span data-ttu-id="04b53-147">7 : code de mappage de type SNMP</span><span class="sxs-lookup"><span data-stu-id="04b53-147">7: SNMP type mapping code</span></span></li>
<li><span data-ttu-id="04b53-148">8 : code de thread SNMP</span><span class="sxs-lookup"><span data-stu-id="04b53-148">8: SNMP threading code</span></span></li>
<li><span data-ttu-id="04b53-149">9 : interfaces et implémentations du fournisseur d’événements SNMP</span><span class="sxs-lookup"><span data-stu-id="04b53-149">9: SNMP event provider interfaces and implementation</span></span></li>
</ul>
<span data-ttu-id="04b53-150">Définissez niveau sur (2 ^ 0 + 2 ^ 8 =) 257 pour les opérations impliquant des appels aux méthodes <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> du fournisseur de classes SNMP, et des opérations utilisant le code de thread SNMP.</span><span class="sxs-lookup"><span data-stu-id="04b53-150">Set Level to (2^0 + 2^8=) 257 for operations involving calls to the SNMP class provider <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> methods, and operations using SNMP threading code.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




