---
title: Fonctions Windows Defender
description: Fonctions appelées par les applications pour demander des analyses, des mises à jour de signature ou des informations de Windows Defender.
ms.assetid: BB3DF71E-1085-45D0-B739-F4C272E7098B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 225530c9d0c2970930d0bc38e23f7907f588e89e
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104381427"
---
# <a name="windows-defender-functions"></a><span data-ttu-id="22c43-103">Fonctions Windows Defender</span><span class="sxs-lookup"><span data-stu-id="22c43-103">Windows Defender Functions</span></span>

<span data-ttu-id="22c43-104">Fonctions appelées par les applications pour demander des analyses, des mises à jour de signature ou des informations de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="22c43-104">Functions called by apps to request scans, signature updates, or information from Windows Defender.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22c43-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="22c43-105">Function</span></span></th>
<th><span data-ttu-id="22c43-106">Description</span><span class="sxs-lookup"><span data-stu-id="22c43-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="22c43-107"><a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a></span><span class="sxs-lookup"><span data-stu-id="22c43-107"><a href="mperrormessageformat.md"><strong>MpErrorMessageFormat</strong></a></span></span></td>
<td><span data-ttu-id="22c43-108">Retourne un message d’erreur mis en forme en fonction d’un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="22c43-108">Returns a formatted error message based on an error code.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c43-109"><a href="mpfreememory.md"><strong>MpFreeMemory</strong></a></span><span class="sxs-lookup"><span data-stu-id="22c43-109"><a href="mpfreememory.md"><strong>MpFreeMemory</strong></a></span></span></td>
<td><span data-ttu-id="22c43-110">Libère de la mémoire pour le gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="22c43-110">Frees memory for the malware protection manager.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c43-111"><a href="mphandleclose.md"><strong>MpHandleClose</strong></a></span><span class="sxs-lookup"><span data-stu-id="22c43-111"><a href="mphandleclose.md"><strong>MpHandleClose</strong></a></span></span></td>
<td><span data-ttu-id="22c43-112">Ferme le handle retourné par <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>, <a href="mpscanstart.md"><strong>MpScanStart</strong></a>, <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>ou <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="22c43-112">Closes the handle returned by <a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a>, <a href="mpscanstart.md"><strong>MpScanStart</strong></a>, <a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a>, or <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c43-113"><a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a></span><span class="sxs-lookup"><span data-stu-id="22c43-113"><a href="mpmanageropen.md"><strong>MpManagerOpen</strong></a></span></span></td>
<td><span data-ttu-id="22c43-114">Établit une connexion au gestionnaire de protection contre les programmes malveillants sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="22c43-114">Establishes a connection to the malware protection manager on the local computer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c43-115"><a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="22c43-115"><a href="mpmanagerstatusquery.md"><strong>MpManagerStatusQuery</strong></a></span></span></td>
<td><span data-ttu-id="22c43-116"><strong>Non pris en charge.</strong></span><span class="sxs-lookup"><span data-stu-id="22c43-116"><strong>Not supported.</strong></span></span> <span data-ttu-id="22c43-117">Retourne des informations d’État sur les différents composants du gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="22c43-117">Returns status information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c43-118"><a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="22c43-118"><a href="mpmanagerstatusqueryex.md"><strong>MpManagerStatusQueryEx</strong></a></span></span></td>
<td><span data-ttu-id="22c43-119">Retourne des informations d’État sur les différents composants du gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="22c43-119">Returns status information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c43-120"><a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="22c43-120"><a href="mpmanagerversionquery.md"><strong>MpManagerVersionQuery</strong></a></span></span></td>
<td><span data-ttu-id="22c43-121">Retourne des informations de version sur les différents composants du gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="22c43-121">Returns version information about various components of the malware protection manager.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c43-122"><a href="mpscancontrol.md"><strong>MpScanControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="22c43-122"><a href="mpscancontrol.md"><strong>MpScanControl</strong></a></span></span></td>
<td><span data-ttu-id="22c43-123">Permet le contrôle d’une analyse qui a été initialisée de façon asynchrone par le biais de <a href="mpscanstart.md"><strong>MpScanStart</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="22c43-123">Allows the control of a scan that was asynchronously initiated via <a href="mpscanstart.md"><strong>MpScanStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c43-124"><a href="mpscanstart.md"><strong>MpScanStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="22c43-124"><a href="mpscanstart.md"><strong>MpScanStart</strong></a></span></span></td>
<td><span data-ttu-id="22c43-125">Démarre une opération d’analyse.</span><span class="sxs-lookup"><span data-stu-id="22c43-125">Starts a scanning operation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c43-126"><a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a></span><span class="sxs-lookup"><span data-stu-id="22c43-126"><a href="mpthreatenumerate.md"><strong>MpThreatEnumerate</strong></a></span></span></td>
<td><span data-ttu-id="22c43-127">Retourne des informations sur la menace suivante dans la liste d’énumération.</span><span class="sxs-lookup"><span data-stu-id="22c43-127">Returns information about the next threat in the enumeration list.</span></span> <span data-ttu-id="22c43-128">Cette fonction peut être appelée à plusieurs reprises jusqu’à ce que l’énumération de toutes les menaces soit terminée.</span><span class="sxs-lookup"><span data-stu-id="22c43-128">This function can be called repeatedly until the enumeration of all the threats is complete.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c43-129"><a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a></span><span class="sxs-lookup"><span data-stu-id="22c43-129"><a href="mpthreatopen.md"><strong>MpThreatOpen</strong></a></span></span></td>
<td><span data-ttu-id="22c43-130">Retourne un handle d’énumération à des fins de récupération des menaces.</span><span class="sxs-lookup"><span data-stu-id="22c43-130">Returns an enumeration handle for the purpose of retrieving threats.</span></span> <span data-ttu-id="22c43-131">Cette fonction peut être utilisée pour ouvrir les menaces détectées par une analyse spécifique, toutes les menaces actives dans le système, l’historique de la désinfection des menaces ou toutes les menaces présentes dans la base de données de signature.</span><span class="sxs-lookup"><span data-stu-id="22c43-131">This function can be used to open threats detected by a specific scan, all the active threats in the system, the history of threat disinfection, or all the threats present in the signature database.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c43-132"><a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a></span><span class="sxs-lookup"><span data-stu-id="22c43-132"><a href="mpthreatquery.md"><strong>MpThreatQuery</strong></a></span></span></td>
<td><span data-ttu-id="22c43-133">Utilisé pour interroger les informations statiques (par exemple, gravité et catégorie) ou localisées (telles que la description de la catégorie et les conseils) sur une menace particulière.</span><span class="sxs-lookup"><span data-stu-id="22c43-133">Used to query static (such as severity and category) or localized (such as category description and advice) information about a particular threat.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c43-134"><a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="22c43-134"><a href="mpupdatecontrol.md"><strong>MpUpdateControl</strong></a></span></span></td>
<td><span data-ttu-id="22c43-135">Autorise le contrôle d’une opération de mise à jour de signature qui a été lancée de manière asynchrone via <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="22c43-135">Allows the control of a signature update operation that was asynchronously initiated via <a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c43-136"><a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="22c43-136"><a href="mpupdatestart.md"><strong>MpUpdateStart</strong></a></span></span></td>
<td><span data-ttu-id="22c43-137">Démarre une opération de mise à jour de signature.</span><span class="sxs-lookup"><span data-stu-id="22c43-137">Starts a signature update operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="22c43-138"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a></span><span class="sxs-lookup"><span data-stu-id="22c43-138"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a></span></span></td>
<td><span data-ttu-id="22c43-139">Modifie l’état de Windows Defender à activé ou désactivé.</span><span class="sxs-lookup"><span data-stu-id="22c43-139">Changes Windows Defender status to on or off.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="22c43-140">À compter de Windows 10, version 1607 et Windows Server 2016, la fonction <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> retourne toujours <strong>E_NOTIMPL</strong>.</span><span class="sxs-lookup"><span data-stu-id="22c43-140">Beginning in Windows 10, version 1607 and Windows Server 2016, the <a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdenable"><strong>WDEnable</strong></a> function always returns <strong>E_NOTIMPL</strong>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="22c43-141"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a></span><span class="sxs-lookup"><span data-stu-id="22c43-141"><a href="/windows/desktop/api/Windowsdefender/nf-windowsdefender-wdstatus"><strong>WDStatus</strong></a></span></span></td>
<td><span data-ttu-id="22c43-142">Retourne l’état actuel de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="22c43-142">Returns the current status of Windows Defender.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 





