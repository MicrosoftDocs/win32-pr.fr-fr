---
description: Les fonctions de cette section installent et configurent des pilotes d’imprimante sur un ordinateur.
ms.assetid: e6aa8963-aa1a-4313-bc24-2aeb4f4b93c4
title: Référence d’installation du pilote d’imprimante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1613725ec5c7e2dbb06710bff706ec5aa7e32dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521252"
---
# <a name="printer-driver-installation-reference"></a><span data-ttu-id="9776c-103">Référence d’installation du pilote d’imprimante</span><span class="sxs-lookup"><span data-stu-id="9776c-103">Printer Driver Installation Reference</span></span>

<span data-ttu-id="9776c-104">Les fonctions de cette section installent et configurent des pilotes d’imprimante sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="9776c-104">The functions in this section install and configure printer drivers on a computer.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9776c-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="9776c-105">In this section</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9776c-106">Fonction</span><span class="sxs-lookup"><span data-stu-id="9776c-106">Function</span></span></th>
<th><span data-ttu-id="9776c-107">Description</span><span class="sxs-lookup"><span data-stu-id="9776c-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9776c-108"><a href="addmonitor.md"><strong>AddMonitor</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-108"><a href="addmonitor.md"><strong>AddMonitor</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-109">La fonction <a href="/windows/desktop/printdocs/addmonitor"><strong>AddMonitor</strong></a> installe un moniteur de port local et lie les fichiers de configuration, de données et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="9776c-109">The <a href="/windows/desktop/printdocs/addmonitor"><strong>AddMonitor</strong></a> function installs a local port monitor and links the configuration, data, and monitor files.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9776c-110"><a href="addport.md"><strong>AddPort</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-110"><a href="addport.md"><strong>AddPort</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-111">La fonction <a href="/windows/desktop/printdocs/addport"><strong>addport</strong></a> ajoute le nom d’un port à la liste des ports pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9776c-111">The <a href="/windows/desktop/printdocs/addport"><strong>AddPort</strong></a> function adds the name of a port to the list of supported ports.</span></span> <span data-ttu-id="9776c-112">La fonction <strong>addport</strong> est exportée par le moniteur de port.</span><span class="sxs-lookup"><span data-stu-id="9776c-112">The <strong>AddPort</strong> function is exported by the port monitor.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9776c-113"><a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-113"><a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-114">La fonction <a href="/windows/desktop/printdocs/addprinterdriver"><strong>AddPrinterDriver</strong></a> installe un pilote d’imprimante local ou distant et associe les fichiers de configuration, de données et de pilote.</span><span class="sxs-lookup"><span data-stu-id="9776c-114">The <a href="/windows/desktop/printdocs/addprinterdriver"><strong>AddPrinterDriver</strong></a> function installs a local or remote printer driver and associates the configuration, data, and driver files.</span></span><br/> <span data-ttu-id="9776c-115">Pour une plus grande flexibilité lors de l’installation ou de la mise à niveau des pilotes d’imprimante, utilisez la fonction <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a> car elle permet une mise à niveau stricte, une rétrogradation stricte, la copie de fichiers plus récents uniquement et la copie de tous les fichiers (quels que soient les horodatages de fichier).</span><span class="sxs-lookup"><span data-stu-id="9776c-115">For more flexibility in installing or upgrading printer drivers, use the <a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a> function because it allows strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of the file time stamps).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9776c-116">L’installation d’un pilote d’imprimante sans package de pilotes n’est plus recommandée.</span><span class="sxs-lookup"><span data-stu-id="9776c-116">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="9776c-117">Utilisez <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> à la place.</span><span class="sxs-lookup"><span data-stu-id="9776c-117">Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9776c-118"><a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-118"><a href="addprinterdriverex.md"><strong>AddPrinterDriverEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-119">La fonction <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>AddPrinterDriverEx</strong></a> installe un pilote d’imprimante local ou distant et lie les fichiers de configuration, de données et de pilote.</span><span class="sxs-lookup"><span data-stu-id="9776c-119">The <a href="/windows/desktop/printdocs/addprinterdriverex"><strong>AddPrinterDriverEx</strong></a> function installs a local or remote printer driver and links the configuration, data, and driver files.</span></span> <span data-ttu-id="9776c-120">Outre les fonctionnalités de <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a>, il offre également des options qui permettent une mise à niveau stricte, une rétrogradation stricte, la copie de fichiers récents uniquement et la copie de tous les fichiers (quels que soient les horodatages des fichiers).</span><span class="sxs-lookup"><span data-stu-id="9776c-120">Besides having the capabilities of <a href="addprinterdriver.md"><strong>AddPrinterDriver</strong></a>, it also has options that permit strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of file time stamps).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9776c-121">L’installation d’un pilote d’imprimante sans package de pilotes n’est plus recommandée.</span><span class="sxs-lookup"><span data-stu-id="9776c-121">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="9776c-122">Utilisez <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> à la place.</span><span class="sxs-lookup"><span data-stu-id="9776c-122">Use <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a> instead.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9776c-123"><a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-123"><a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-124">La fonction <a href="/windows/desktop/printdocs/addprintprocessor"><strong>AddPrintProcessor</strong></a> installe un processeur d’impression sur le serveur spécifié et ajoute le nom du processeur d’impression à la liste des processeurs d’impression pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9776c-124">The <a href="/windows/desktop/printdocs/addprintprocessor"><strong>AddPrintProcessor</strong></a> function installs a print processor on the specified server and adds the print-processor name to the list of supported print processors.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9776c-125"><a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-125"><a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-126">La fonction <a href="/windows/desktop/printdocs/addprintprovidor"><strong>AddPrintProvidor</strong></a> installe un fournisseur d’impression local et lie les fichiers de configuration, de données et de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="9776c-126">The <a href="/windows/desktop/printdocs/addprintprovidor"><strong>AddPrintProvidor</strong></a> function installs a local print provider and links the configuration, data, and provider files.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9776c-127"><a href="coreprinterdriverinstalled.md"><strong>CorePrinterDriverInstalled</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-127"><a href="coreprinterdriverinstalled.md"><strong>CorePrinterDriverInstalled</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-128">La fonction <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>CorePrinterDriverInstalled</strong></a> indique si un pilote d’imprimante principal avec un GUID, une date et une version spécifiés est installé.</span><span class="sxs-lookup"><span data-stu-id="9776c-128">The <a href="/windows/desktop/printdocs/coreprinterdriverinstalled"><strong>CorePrinterDriverInstalled</strong></a> function reports whether a core printer driver with a specified GUID, date, and version is installed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9776c-129"><a href="deletemonitor.md"><strong>DeleteMonitor</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-129"><a href="deletemonitor.md"><strong>DeleteMonitor</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-130">La fonction <a href="/windows/desktop/printdocs/deletemonitor"><strong>DeleteMonitor</strong></a> supprime un moniteur de port ajouté par la fonction <a href="addmonitor.md"><strong>AddMonitor</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9776c-130">The <a href="/windows/desktop/printdocs/deletemonitor"><strong>DeleteMonitor</strong></a> function removes a port monitor added by the <a href="addmonitor.md"><strong>AddMonitor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9776c-131"><a href="deleteport.md"><strong>DeletePort</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-131"><a href="deleteport.md"><strong>DeletePort</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-132">La fonction <a href="/windows/desktop/printdocs/deleteport"><strong>DeletePort</strong></a> affiche une boîte de dialogue qui permet à l’utilisateur de supprimer un nom de port.</span><span class="sxs-lookup"><span data-stu-id="9776c-132">The <a href="/windows/desktop/printdocs/deleteport"><strong>DeletePort</strong></a> function displays a dialog box that allows the user to delete a port name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9776c-133"><a href="deleteprinterdriver.md"><strong>DeletePrinterDriver</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-133"><a href="deleteprinterdriver.md"><strong>DeletePrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-134">La fonction <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> supprime le nom du pilote d’imprimante spécifié de la liste des noms des pilotes pris en charge sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="9776c-134">The <a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> function removes the specified printer-driver name from the list of names of supported drivers on a server.</span></span><br/> <span data-ttu-id="9776c-135">Pour supprimer les fichiers associés au pilote en plus de supprimer le nom du pilote d’imprimante spécifié de la liste des noms des pilotes pris en charge pour un serveur, utilisez la fonction <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9776c-135">To delete the files associated with the driver in addition to removing the specified printer-driver name from the list of names of supported drivers for a server, use the <a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> function.</span></span><br/> <span data-ttu-id="9776c-136"><a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> supprime un pilote uniquement si aucune version du pilote n’est utilisée pour l’environnement spécifié.</span><span class="sxs-lookup"><span data-stu-id="9776c-136"><a href="/windows/desktop/printdocs/deleteprinterdriver"><strong>DeletePrinterDriver</strong></a> deletes a driver only if no version of the driver is in use for the specified environment.</span></span> <span data-ttu-id="9776c-137"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> peut supprimer des versions spécifiques du pilote.</span><span class="sxs-lookup"><span data-stu-id="9776c-137"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a> can delete specific versions of the driver.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9776c-138"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-138"><a href="deleteprinterdriverex.md"><strong>DeletePrinterDriverEx</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-139">La fonction <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>DeletePrinterDriverEx</strong></a> supprime le nom du pilote d’imprimante spécifié de la liste des noms des pilotes pris en charge sur un serveur et supprime les fichiers associés au pilote.</span><span class="sxs-lookup"><span data-stu-id="9776c-139">The <a href="/windows/desktop/printdocs/deleteprinterdriverex"><strong>DeletePrinterDriverEx</strong></a> function removes the specified printer-driver name from the list of names of supported drivers on a server and deletes the files associated with the driver.</span></span> <span data-ttu-id="9776c-140">Cette fonction peut également supprimer des versions spécifiques du pilote.</span><span class="sxs-lookup"><span data-stu-id="9776c-140">This function can also delete specific versions of the driver.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9776c-141"><a href="deleteprinterdriverpackage.md"><strong>DeletePrinterDriverPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-141"><a href="deleteprinterdriverpackage.md"><strong>DeletePrinterDriverPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-142">Supprime un package de pilotes d’imprimante du magasin de pilotes.</span><span class="sxs-lookup"><span data-stu-id="9776c-142">Deletes a printer driver package from the driver store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9776c-143"><a href="deleteprintprocessor.md"><strong>DeletePrintProcessor</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-143"><a href="deleteprintprocessor.md"><strong>DeletePrintProcessor</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-144">La fonction <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>DeletePrintProcessor</strong></a> supprime un processeur d’impression ajouté par la fonction <a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9776c-144">The <a href="/windows/desktop/printdocs/deleteprintprocessor"><strong>DeletePrintProcessor</strong></a> function removes a print processor added by the <a href="addprintprocessor.md"><strong>AddPrintProcessor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9776c-145"><a href="deleteprintprovidor.md"><strong>DeletePrintProvidor</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-145"><a href="deleteprintprovidor.md"><strong>DeletePrintProvidor</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-146">La fonction <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>DeletePrintProvidor</strong></a> supprime un fournisseur d’impression ajouté par la fonction <a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="9776c-146">The <a href="/windows/desktop/printdocs/deleteprintprovidor"><strong>DeletePrintProvidor</strong></a> function removes a print provider added by the <a href="addprintprovidor.md"><strong>AddPrintProvidor</strong></a> function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9776c-147"><a href="enummonitors.md"><strong>EnumMonitors</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-147"><a href="enummonitors.md"><strong>EnumMonitors</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-148">La fonction <a href="/windows/desktop/printdocs/enummonitors"><strong>EnumMonitors</strong></a> récupère des informations sur les moniteurs de port installés sur le serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="9776c-148">The <a href="/windows/desktop/printdocs/enummonitors"><strong>EnumMonitors</strong></a> function retrieves information about the port monitors installed on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9776c-149"><a href="enumports.md"><strong>EnumPorts</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-149"><a href="enumports.md"><strong>EnumPorts</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-150">La fonction <a href="/windows/desktop/printdocs/enumports"><strong>EnumPorts</strong></a> énumère les ports qui sont disponibles pour l’impression sur un serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="9776c-150">The <a href="/windows/desktop/printdocs/enumports"><strong>EnumPorts</strong></a> function enumerates the ports that are available for printing on a specified server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9776c-151"><a href="enumprinterdrivers.md"><strong>EnumPrinterDrivers</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-151"><a href="enumprinterdrivers.md"><strong>EnumPrinterDrivers</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-152">La fonction <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>EnumPrinterDrivers</strong></a> énumère les pilotes d’imprimante installés sur un serveur d’impression spécifié.</span><span class="sxs-lookup"><span data-stu-id="9776c-152">The <a href="/windows/desktop/printdocs/enumprinterdrivers"><strong>EnumPrinterDrivers</strong></a> function enumerates the printer drivers installed on a specified printer server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9776c-153"><a href="enumprintprocessordatatypes.md"><strong>EnumPrintProcessorDatatypes</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-153"><a href="enumprintprocessordatatypes.md"><strong>EnumPrintProcessorDatatypes</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-154">La fonction <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>EnumPrintProcessorDatatypes</strong></a> énumère les types de données pris en charge par un processeur d’impression spécifié.</span><span class="sxs-lookup"><span data-stu-id="9776c-154">The <a href="/windows/desktop/printdocs/enumprintprocessordatatypes"><strong>EnumPrintProcessorDatatypes</strong></a> function enumerates the data types that a specified print processor supports.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9776c-155"><a href="enumprintprocessors.md"><strong>EnumPrintProcessors</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-155"><a href="enumprintprocessors.md"><strong>EnumPrintProcessors</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-156">La fonction <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>EnumPrintProcessors</strong></a> énumère les processeurs d’impression installés sur le serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="9776c-156">The <a href="/windows/desktop/printdocs/enumprintprocessors"><strong>EnumPrintProcessors</strong></a> function enumerates the print processors installed on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9776c-157"><a href="getcoreprinterdrivers.md"><strong>GetCorePrinterDrivers</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-157"><a href="getcoreprinterdrivers.md"><strong>GetCorePrinterDrivers</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-158">Récupère le GUID, la version et la date des pilotes d’imprimante principaux spécifiés et le chemin d’accès à leurs packages.</span><span class="sxs-lookup"><span data-stu-id="9776c-158">Retrieves GUID, version, and date of the specified core printer drivers and the path to their packages.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9776c-159"><a href="getprinterdriver.md"><strong>GetPrinterDriver</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-159"><a href="getprinterdriver.md"><strong>GetPrinterDriver</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-160">La fonction <a href="/windows/desktop/printdocs/getprinterdriver"><strong>GetPrinterDriver</strong></a> récupère les données du pilote pour l’imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9776c-160">The <a href="/windows/desktop/printdocs/getprinterdriver"><strong>GetPrinterDriver</strong></a> function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="9776c-161">Si le pilote n’est pas installé sur l’ordinateur local, <strong>GetPrinterDriver</strong> l’installe.</span><span class="sxs-lookup"><span data-stu-id="9776c-161">If the driver is not installed on the local computer, <strong>GetPrinterDriver</strong> installs it.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9776c-162"><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-162"><a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-163">La fonction <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> récupère les données du pilote pour l’imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9776c-163">The <a href="getprinterdriver2.md"><strong>GetPrinterDriver2</strong></a> function retrieves driver data for the specified printer.</span></span> <span data-ttu-id="9776c-164">Si le pilote n’est pas installé sur l’ordinateur local, <strong>GetPrinterDriver2</strong> l’installe et affiche l’interface utilisateur dans la fenêtre spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9776c-164">If the driver is not installed on the local computer, <strong>GetPrinterDriver2</strong> installs it and displays any user interface to the specified window.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9776c-165"><a href="getprinterdriverdirectory.md"><strong>GetPrinterDriverDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-165"><a href="getprinterdriverdirectory.md"><strong>GetPrinterDriverDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-166">La fonction <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>GetPrinterDriverDirectory</strong></a> récupère le chemin d’accès du répertoire du pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="9776c-166">The <a href="/windows/desktop/printdocs/getprinterdriverdirectory"><strong>GetPrinterDriverDirectory</strong></a> function retrieves the path of the printer-driver directory.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9776c-167"><a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-167"><a href="getprinterdriverpackagepath.md"><strong>GetPrinterDriverPackagePath</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-168">Récupère le chemin d’accès au package de pilotes d’imprimante spécifié sur un serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="9776c-168">Retrieves the path to the specified printer driver package on a print server.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9776c-169"><a href="getprintprocessordirectory.md"><strong>GetPrintProcessorDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-169"><a href="getprintprocessordirectory.md"><strong>GetPrintProcessorDirectory</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-170">La fonction <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>GetPrintProcessorDirectory</strong></a> récupère le chemin d’accès au répertoire du processeur d’impression sur le serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="9776c-170">The <a href="/windows/desktop/printdocs/getprintprocessordirectory"><strong>GetPrintProcessorDirectory</strong></a> function retrieves the path to the print processor directory on the specified server.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9776c-171"><a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-171"><a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-172">Installe un pilote d’imprimante à partir d’un package de pilotes qui se trouve dans le magasin de pilotes du serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="9776c-172">Installs a printer driver from a driver package that is in the print server's driver store.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9776c-173"><a href="uploadprinterdriverpackage.md"><strong>UploadPrinterDriverPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="9776c-173"><a href="uploadprinterdriverpackage.md"><strong>UploadPrinterDriverPackage</strong></a></span></span><br/></td>
<td><span data-ttu-id="9776c-174">Charge un pilote d’imprimante sur le magasin de pilotes du serveur d’impression afin qu’il puisse être installé en appelant <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9776c-174">Uploads a printer driver to the print server's driver store so that it can be installed by calling <a href="installprinterdriverfrompackage.md"><strong>InstallPrinterDriverFromPackage</strong></a>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

