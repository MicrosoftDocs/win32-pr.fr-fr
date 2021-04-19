---
title: Résolution des problèmes d’empaquetage, de déploiement et d’interrogation des applications Windows
description: Utilisez ces suggestions pour résoudre les problèmes que vous rencontrez lors de l’empaquetage, du déploiement ou de l’interrogation d’un package d’application.
ms.assetid: 38E327C6-0345-4FA6-BCDB-5FA2FCD421FB
ms.topic: article
ms.date: 02/20/2020
manager: dcscontentpm
ms.custom:
- CI 111497
- CSSTroubleshooting
- contperf-fy21q2
ms.openlocfilehash: a2ee7c28e7de2d616bd01e9b5cae0de3c325caf4
ms.sourcegitcommit: 80198645ddacc3c12c72f3814b71ade0f415e705
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2021
ms.locfileid: "106530053"
---
# <a name="troubleshooting-packaging-deployment-and-query-of-windows-apps"></a><span data-ttu-id="7b862-103">Résolution des problèmes d’empaquetage, de déploiement et d’interrogation des applications Windows</span><span class="sxs-lookup"><span data-stu-id="7b862-103">Troubleshooting packaging, deployment, and query of Windows apps</span></span>

<span data-ttu-id="7b862-104">Utilisez ces suggestions pour résoudre les problèmes que vous rencontrez lors de l’empaquetage, du déploiement ou de l’interrogation d’un package d’application Windows (. msix/. AppX) en tant que développeur.</span><span class="sxs-lookup"><span data-stu-id="7b862-104">Use these suggestions to troubleshoot problems you experience when packaging, deploying, or querying a Windows app package (.msix/.appx) as a developer.</span></span>

> [!NOTE]
> <span data-ttu-id="7b862-105">Cet article s’adresse aux développeurs.</span><span class="sxs-lookup"><span data-stu-id="7b862-105">This article is intended for developers.</span></span> <span data-ttu-id="7b862-106">Si vous n’êtes pas un développeur et que vous recherchez de l’aide concernant une erreur d’installation d’une application Windows, consultez [prise en charge de Windows](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).</span><span class="sxs-lookup"><span data-stu-id="7b862-106">If you are not a developer and you are looking for help with a Windows app installation error, see [Windows support](https://support.microsoft.com/hub/4338813/windows-help?os=windows-10).</span></span>

## <a name="get-diagnostic-information"></a><span data-ttu-id="7b862-107">Recevoir des informations de diagnostic</span><span class="sxs-lookup"><span data-stu-id="7b862-107">Get diagnostic information</span></span>

<span data-ttu-id="7b862-108">Lorsqu’une API échoue, elle retourne un code d’erreur qui décrit le problème.</span><span class="sxs-lookup"><span data-stu-id="7b862-108">When an API fails, it returns an error code that describes the problem.</span></span> <span data-ttu-id="7b862-109">Si le code d’erreur ne fournit pas suffisamment d’informations, vous trouverez plus d’informations de diagnostic dans les journaux des événements détaillés.</span><span class="sxs-lookup"><span data-stu-id="7b862-109">If the error code doesn't provide enough information, you find more diagnostic information in the detailed event logs.</span></span>

<span data-ttu-id="7b862-110">Pour accéder aux journaux des événements de Packaging et de déploiement à l’aide de **Observateur d’événements**, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7b862-110">To access the packaging and deployment event logs by using **Event Viewer**, follow these steps:</span></span>

1. <span data-ttu-id="7b862-111">Effectuez l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="7b862-111">Perform one of the following steps:</span></span>

    * <span data-ttu-id="7b862-112">Dans le menu fenêtres, cliquez sur **Démarrer** , tapez **Observateur d’événements**, puis **Appuyez sur entrée**.</span><span class="sxs-lookup"><span data-stu-id="7b862-112">Click **Start** on the Windows menu, type **Event Viewer**, and **press Enter**.</span></span>
    * <span data-ttu-id="7b862-113">Exécutez **eventvwr. msc**.</span><span class="sxs-lookup"><span data-stu-id="7b862-113">Run **eventvwr.msc**.</span></span>

2. <span data-ttu-id="7b862-114">Dans la page de gauche, développez **Observateur d’événements (local)**  >  **applications et services journaux**  >  **Microsoft**  >  **Windows**.</span><span class="sxs-lookup"><span data-stu-id="7b862-114">In the left page, expand **Event Viewer (Local)** > **Applications and Services Logs** > **Microsoft** > **Windows**.</span></span>
3. <span data-ttu-id="7b862-115">Recherchez les journaux disponibles dans les catégories suivantes :</span><span class="sxs-lookup"><span data-stu-id="7b862-115">Check for available logs under these categories:</span></span>

    * <span data-ttu-id="7b862-116">**AppxPackagingOM**  >  **Microsoft-Windows-AppxPackaging/Operational**</span><span class="sxs-lookup"><span data-stu-id="7b862-116">**AppxPackagingOM** > **Microsoft-Windows-AppxPackaging/Operational**</span></span>
    * <span data-ttu-id="7b862-117">**AppXDeployment-serveur**  >  **Microsoft-Windows-AppXDeploymentServer/Operational**</span><span class="sxs-lookup"><span data-stu-id="7b862-117">**AppXDeployment-Server** > **Microsoft-Windows-AppXDeploymentServer/Operational**</span></span>

<span data-ttu-id="7b862-118">Commencez par examiner les journaux sous **AppXDeployment-Server**.</span><span class="sxs-lookup"><span data-stu-id="7b862-118">Start by looking at the logs under **AppXDeployment-Server**.</span></span> <span data-ttu-id="7b862-119">Si l’erreur a été provoquée par **0x80073CF0** ou **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, des détails supplémentaires peuvent être présents dans les journaux **AppxpackagingOM** .</span><span class="sxs-lookup"><span data-stu-id="7b862-119">If the error was caused by **0x80073CF0** or **ERROR_INSTALL_OPEN_PACKAGE_FAILED**, additional details may be present in the **AppxpackagingOM** logs.</span></span>

<span data-ttu-id="7b862-120">Vous pouvez également utiliser la commande [AppxLog](/powershell/module/appx/get-appxlog) dans PowerShell pour récupérer les premiers événements journalisés.</span><span class="sxs-lookup"><span data-stu-id="7b862-120">You can also use the [Get-AppxLog](/powershell/module/appx/get-appxlog) command in PowerShell to get the first few logged events.</span></span> <span data-ttu-id="7b862-121">L’exemple suivant affiche les journaux associés à l’opération de déploiement la plus récente.</span><span class="sxs-lookup"><span data-stu-id="7b862-121">The following example displays the logs associated with the most recent deployment operation.</span></span>

```PowerShell
Get-Appxlog
```

<span data-ttu-id="7b862-122">L’exemple suivant affiche les journaux associés à l’opération de déploiement la plus récente dans une table interactive dans une fenêtre distincte.</span><span class="sxs-lookup"><span data-stu-id="7b862-122">The following example displays the logs associated with the most recent deployment operation in an interactive table in a separate window.</span></span>

```PowerShell
Get-Appxlog | Out-GridView
```

## <a name="common-error-codes"></a><span data-ttu-id="7b862-123">Common error codes (Codes d’erreur courants)</span><span class="sxs-lookup"><span data-stu-id="7b862-123">Common error codes</span></span>

<span data-ttu-id="7b862-124">Ce tableau répertorie certains des codes d’erreur les plus courants.</span><span class="sxs-lookup"><span data-stu-id="7b862-124">This table lists some of the most common error codes.</span></span> <span data-ttu-id="7b862-125">Si vous avez besoin d’aide pour l’une de ces erreurs ou si vous rencontrez un code d’erreur qui ne figure pas dans cette liste, consultez [options d’aide supplémentaires](#get-additional-help).</span><span class="sxs-lookup"><span data-stu-id="7b862-125">If you need further help with one of these errors, or if you're encountering an error code not in this list, see [additional help options](#get-additional-help).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7b862-126">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="7b862-126">Error code</span></span></th>
<th><span data-ttu-id="7b862-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b862-127">Value</span></span></th>
<th><span data-ttu-id="7b862-128">Description et causes possibles</span><span class="sxs-lookup"><span data-stu-id="7b862-128">Description and possible causes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="even">
<td><span data-ttu-id="7b862-129"><strong>E_FILENOTFOUND</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-129"><strong>E_FILENOTFOUND</strong></span></span></td>
<td><span data-ttu-id="7b862-130">0x80070002</span><span class="sxs-lookup"><span data-stu-id="7b862-130">0x80070002</span></span></td>
<td><span data-ttu-id="7b862-131">Fichier ou chemin d'accès introuvable.</span><span class="sxs-lookup"><span data-stu-id="7b862-131">File or path is not found.</span></span> <span data-ttu-id="7b862-132">Cela peut se produire pendant une validation de TypeLib COM exige que le chemin d’accès au répertoire existe réellement dans votre package MSIX.</span><span class="sxs-lookup"><span data-stu-id="7b862-132">This can occur during a COM  typelib validation requires that the path for the directory actually exist within your MSIX package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-133"><strong>ERROR_BAD_FORMAT</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-133"><strong>ERROR_BAD_FORMAT</strong></span></span></td>
<td><span data-ttu-id="7b862-134">0x8007000B</span><span class="sxs-lookup"><span data-stu-id="7b862-134">0x8007000B</span></span></td>
<td><span data-ttu-id="7b862-135">Le package n’est pas formaté correctement et doit être recréé ou resigné.</span><span class="sxs-lookup"><span data-stu-id="7b862-135">The package isn't correctly formatted and needs to be re-built or re-signed.</span></span><br/> <span data-ttu-id="7b862-136">Vous pouvez obtenir cette erreur en cas de discordance entre le nom d’objet du certificat de signature et le nom de l’éditeur de AppxManifest.xml.</span><span class="sxs-lookup"><span data-stu-id="7b862-136">You may get this error if there is a mismatch between the signing certificate subject name and the AppxManifest.xml publisher name.</span></span><br/> <span data-ttu-id="7b862-137">Consultez <a href="how-to-sign-a-package-using-signtool.md">Comment signer un package d’application à l’aide de SignTool</a>.</span><span class="sxs-lookup"><span data-stu-id="7b862-137">See <a href="how-to-sign-a-package-using-signtool.md">How to sign an app package using SignTool</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-138"><strong>E_INVALIDARG</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-138"><strong>E_INVALIDARG</strong></span></span></td>
<td><span data-ttu-id="7b862-139">0x80070057</span><span class="sxs-lookup"><span data-stu-id="7b862-139">0x80070057</span></span></td>
<td><span data-ttu-id="7b862-140">Un ou plusieurs arguments ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="7b862-140">One or more arguments are not valid.</span></span> <span data-ttu-id="7b862-141">Si vous consultez le journal des événements AppXDeployment-Server et que vous voyez l’événement suivant : « lors de l’installation du package, le système n’a pas pu inscrire l’extension Windows. repositoryExtension en raison de l’erreur suivante : le paramètre est incorrect. »</span><span class="sxs-lookup"><span data-stu-id="7b862-141">If you check the AppXDeployment-Server event log and see the following event: "While installing the package, the system failed to register the windows.repositoryExtension extension due to the following error: The parameter is incorrect."</span></span> <br/> <span data-ttu-id="7b862-142">Vous pouvez recevoir cette erreur si les éléments de manifeste DisplayName ou description contiennent des caractères non autorisés par le pare-feu Windows ; à savoir |  et tout, car Windows ne parvient pas à créer le profil AppContainer pour le package.</span><span class="sxs-lookup"><span data-stu-id="7b862-142">You may get this error if the manifest elements DisplayName or Description contain characters disallowed by Windows firewall; namely  |  and  all , due to which Windows fails to create the AppContainer profile for the package.</span></span> <span data-ttu-id="7b862-143">Supprimez ces caractères du manifeste et essayez d’installer le package.</span><span class="sxs-lookup"><span data-stu-id="7b862-143">Please remove these characters from the manifest and try installing the package.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-144"><strong>ERROR_INSTALL_OPEN_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-144"><strong>ERROR_INSTALL_OPEN_</strong></span></span><br/> <span data-ttu-id="7b862-145"><strong>PACKAGE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-145"><strong>PACKAGE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-146">0x80073CF0</span><span class="sxs-lookup"><span data-stu-id="7b862-146">0x80073CF0</span></span></td>
<td><span data-ttu-id="7b862-147">Impossible d’ouvrir le package.</span><span class="sxs-lookup"><span data-stu-id="7b862-147">The package couldn't be opened.</span></span><br/> <span data-ttu-id="7b862-148">Causes possibles :</span><span class="sxs-lookup"><span data-stu-id="7b862-148">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="7b862-149">Le package n'est pas signé.</span><span class="sxs-lookup"><span data-stu-id="7b862-149">The package is unsigned.</span></span></li>
<li><span data-ttu-id="7b862-150">Le nom de l’éditeur ne correspond pas à l’objet du certificat de signature.</span><span class="sxs-lookup"><span data-stu-id="7b862-150">The publisher name doesn't match the signing certificate subject.</span></span></li>
<li><span data-ttu-id="7b862-151">Le préfixe file://est manquant ou le package est introuvable à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="7b862-151">The file:// prefix is missing or the package couldn't be found at the specified location.</span></span></li>
</ul>
<span data-ttu-id="7b862-152">Pour plus d’informations, consultez le journal des événements <strong>AppxPackagingOM</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b862-152">For more information, check the <strong>AppxPackagingOM</strong> event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-153"><strong>ERROR_INSTALL_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-153"><strong>ERROR_INSTALL_PACKAGE_</strong></span></span><br/> <span data-ttu-id="7b862-154"><strong>NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-154"><strong>NOT_FOUND</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-155">0x80073CF1</span><span class="sxs-lookup"><span data-stu-id="7b862-155">0x80073CF1</span></span></td>
<td><span data-ttu-id="7b862-156">Le package est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7b862-156">The package couldn't be found.</span></span><br/> <span data-ttu-id="7b862-157">Vous pouvez obtenir cette erreur lors de la suppression d’un package qui n’est pas installé pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="7b862-157">You may get this error while removing a package that isn't installed for the current user.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-158"><strong>ERROR_INSTALL_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-158"><strong>ERROR_INSTALL_INVALID_</strong></span></span><br/> <span data-ttu-id="7b862-159"><strong>Packages</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-159"><strong>PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-160">0x80073CF2</span><span class="sxs-lookup"><span data-stu-id="7b862-160">0x80073CF2</span></span></td>
<td><span data-ttu-id="7b862-161">Les données du package ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="7b862-161">The package data isn't valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-162"><strong>ERROR_INSTALL_RESOLVE_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-162"><strong>ERROR_INSTALL_RESOLVE_</strong></span></span><br/> <span data-ttu-id="7b862-163"><strong>DEPENDENCY_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-163"><strong>DEPENDENCY_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-164">0x80073CF3</span><span class="sxs-lookup"><span data-stu-id="7b862-164">0x80073CF3</span></span></td>
<td><span data-ttu-id="7b862-165">Échec de la mise à jour du package, d'une dépendance ou validation de conflit.</span><span class="sxs-lookup"><span data-stu-id="7b862-165">The package failed update, dependency, or conflict validation.</span></span><br/> <span data-ttu-id="7b862-166">Causes possibles :</span><span class="sxs-lookup"><span data-stu-id="7b862-166">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="7b862-167">Le package entrant est en conflit avec un package installé.</span><span class="sxs-lookup"><span data-stu-id="7b862-167">The incoming package conflicts with an installed package.</span></span></li>
<li><span data-ttu-id="7b862-168">Une dépendance de package spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7b862-168">A specified package dependency can't be found.</span></span></li>
<li><span data-ttu-id="7b862-169">Le package ne prend pas en charge l’architecture de processeur correcte.</span><span class="sxs-lookup"><span data-stu-id="7b862-169">The package doesn't support the correct processor architecture.</span></span></li>
</ul>
<span data-ttu-id="7b862-170">Pour plus d’informtion, consultez le journal des événements <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b862-170">For more informtion, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-171"><strong>ERROR_INSTALL_OUT_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-171"><strong>ERROR_INSTALL_OUT_</strong></span></span><br/> <span data-ttu-id="7b862-172"><strong>OF_DISK_SPACE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-172"><strong>OF_DISK_SPACE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-173">0x80073CF4</span><span class="sxs-lookup"><span data-stu-id="7b862-173">0x80073CF4</span></span></td>
<td><span data-ttu-id="7b862-174">L’espace disque est insuffisant sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7b862-174">There isn't enough disk space on your computer.</span></span> <span data-ttu-id="7b862-175">Libérez de l’espace et réessayez.</span><span class="sxs-lookup"><span data-stu-id="7b862-175">Free some space and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-176"><strong>ERROR_INSTALL_NETWORK_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-176"><strong>ERROR_INSTALL_NETWORK_</strong></span></span><br/> <span data-ttu-id="7b862-177"><strong>TOUTE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-177"><strong>FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-178">0x80073CF5</span><span class="sxs-lookup"><span data-stu-id="7b862-178">0x80073CF5</span></span></td>
<td><span data-ttu-id="7b862-179">Le package ne peut pas être téléchargé.</span><span class="sxs-lookup"><span data-stu-id="7b862-179">The package can't be downloaded.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-180"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-180"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="7b862-181"><strong>REGISTRATION_FAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-181"><strong>REGISTRATION_FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-182">0x80073CF6</span><span class="sxs-lookup"><span data-stu-id="7b862-182">0x80073CF6</span></span></td>
<td><span data-ttu-id="7b862-183">Le package ne peut pas être inscrit.</span><span class="sxs-lookup"><span data-stu-id="7b862-183">The package can't be registered.</span></span><br/> <span data-ttu-id="7b862-184">Pour plus d’informations, consultez le journal des événements <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b862-184">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-185"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-185"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="7b862-186"><strong>DEREGISTRATION_EFAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-186"><strong>DEREGISTRATION_EFAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-187">0x80073CF7</span><span class="sxs-lookup"><span data-stu-id="7b862-187">0x80073CF7</span></span></td>
<td><span data-ttu-id="7b862-188">Impossible d’annuler l’inscription du package.</span><span class="sxs-lookup"><span data-stu-id="7b862-188">The package can't be unregistered.</span></span><br/> <span data-ttu-id="7b862-189">Vous pouvez obtenir cette erreur lors de la suppression d’un package.</span><span class="sxs-lookup"><span data-stu-id="7b862-189">You may get this error while removing a package.</span></span><br/> <span data-ttu-id="7b862-190">Pour plus d’informations, consultez le journal des événements <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b862-190">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-191"><strong>ERROR_INSTALL_CANCEL</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-191"><strong>ERROR_INSTALL_CANCEL</strong></span></span></td>
<td><span data-ttu-id="7b862-192">0x80073CF8</span><span class="sxs-lookup"><span data-stu-id="7b862-192">0x80073CF8</span></span></td>
<td><span data-ttu-id="7b862-193">L’utilisateur a annulé la demande d’installation.</span><span class="sxs-lookup"><span data-stu-id="7b862-193">The user canceled the install request.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-194"><strong>ERROR_INSTALL_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-194"><strong>ERROR_INSTALL_FAILED</strong></span></span></td>
<td><span data-ttu-id="7b862-195">0x80073CF9</span><span class="sxs-lookup"><span data-stu-id="7b862-195">0x80073CF9</span></span></td>
<td><span data-ttu-id="7b862-196">Échec de l’installation du package.</span><span class="sxs-lookup"><span data-stu-id="7b862-196">Package install failed.</span></span> <span data-ttu-id="7b862-197">Contactez le fournisseur du logiciel.</span><span class="sxs-lookup"><span data-stu-id="7b862-197">Contact the software vendor.</span></span><br/> <span data-ttu-id="7b862-198">Pour plus d’informations, consultez le journal des événements <strong>AppXDeployment-Server</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b862-198">For more information, check the <strong>AppXDeployment-Server</strong> event log.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-199"><strong>ERROR_REMOVE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-199"><strong>ERROR_REMOVE_FAILED</strong></span></span></td>
<td><span data-ttu-id="7b862-200">0x80073CFA</span><span class="sxs-lookup"><span data-stu-id="7b862-200">0x80073CFA</span></span></td>
<td><span data-ttu-id="7b862-201">Échec de la suppression du package.</span><span class="sxs-lookup"><span data-stu-id="7b862-201">Package removal failed.</span></span><br/> <span data-ttu-id="7b862-202">Vous pouvez obtenir cette erreur pour les échecs qui se produisent pendant la désinstallation du package.</span><span class="sxs-lookup"><span data-stu-id="7b862-202">You may get this error for failures that occur during package uninstall.</span></span><br/> <span data-ttu-id="7b862-203">Pour plus d’informations, consultez <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7b862-203">For more information, see <a href="/uwp/api/windows.management.deployment.packagemanager.removepackageasync"><strong>RemovePackageAsync</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-204"><strong>ERROR_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-204"><strong>ERROR_PACKAGE_</strong></span></span><br/> <span data-ttu-id="7b862-205"><strong>ALREADY_EXISTS</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-205"><strong>ALREADY_EXISTS</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-206">0x80073CFB</span><span class="sxs-lookup"><span data-stu-id="7b862-206">0x80073CFB</span></span></td>
<td><span data-ttu-id="7b862-207">Le package fourni est déjà installé, et la réinstallation du package est bloquée.</span><span class="sxs-lookup"><span data-stu-id="7b862-207">The provided package is already installed, and reinstallation of the package is blocked.</span></span> <br/> <span data-ttu-id="7b862-208">Vous pouvez obtenir cette erreur si vous installez un package qui n’est pas identique au niveau du bit au package déjà installé.</span><span class="sxs-lookup"><span data-stu-id="7b862-208">You may get this error if installing a package that is not bitwise identical to the package that is already installed.</span></span> <span data-ttu-id="7b862-209">Notez que la signature numérique fait également partie du package.</span><span class="sxs-lookup"><span data-stu-id="7b862-209">Note that the digital signature is also part of the package.</span></span> <span data-ttu-id="7b862-210">Par conséquent, si un package est reconstruit ou resigné, il n’est plus identique au niveau du bit au package précédemment installé.</span><span class="sxs-lookup"><span data-stu-id="7b862-210">Hence if a package is rebuilt or resigned, it is no longer bitwise identical to the previously installed package.</span></span> <span data-ttu-id="7b862-211">Deux options possibles pour corriger cette erreur sont les suivantes : (1) incrémenter le numéro de version de l’application, puis reconstruire et abandonner le package (2) Supprimez l’ancien package pour chaque utilisateur sur le système avant d’installer le nouveau package.</span><span class="sxs-lookup"><span data-stu-id="7b862-211">Two possible options to fix this error are: (1) Increment the version number of the app, then rebuild and resign the package (2) Remove the old package for every user on the system before installing the new package.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-212"><strong>ERROR_NEEDS_REMEDIATION</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-212"><strong>ERROR_NEEDS_REMEDIATION</strong></span></span></td>
<td><span data-ttu-id="7b862-213">0x80073CFC</span><span class="sxs-lookup"><span data-stu-id="7b862-213">0x80073CFC</span></span></td>
<td><span data-ttu-id="7b862-214">L’application ne peut pas être démarrée.</span><span class="sxs-lookup"><span data-stu-id="7b862-214">The app can't be started.</span></span> <span data-ttu-id="7b862-215">Essayez de réinstaller l’application.</span><span class="sxs-lookup"><span data-stu-id="7b862-215">Try reinstalling the app.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-216"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-216"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="7b862-217"><strong>PREREQUISITE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-217"><strong>PREREQUISITE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-218">0x80073CFD</span><span class="sxs-lookup"><span data-stu-id="7b862-218">0x80073CFD</span></span></td>
<td><span data-ttu-id="7b862-219">Impossible de satisfaire un prérequis d’installation spécifié.</span><span class="sxs-lookup"><span data-stu-id="7b862-219">A specified install prerequisite couldn't be satisfied.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-220"><strong>ERROR_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-220"><strong>ERROR_PACKAGE_</strong></span></span><br/> <span data-ttu-id="7b862-221"><strong>REPOSITORY_CORRUPTED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-221"><strong>REPOSITORY_CORRUPTED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-222">0x80073CFE</span><span class="sxs-lookup"><span data-stu-id="7b862-222">0x80073CFE</span></span></td>
<td><span data-ttu-id="7b862-223">Le référentiel du package est endommagé.</span><span class="sxs-lookup"><span data-stu-id="7b862-223">The package repository is corrupted.</span></span><br/> <span data-ttu-id="7b862-224">Vous pouvez recevoir cette erreur si le dossier référencé par cette clé de Registre n’existe pas ou est endommagé :</span><span class="sxs-lookup"><span data-stu-id="7b862-224">You may get this error if the folder referenced by this registry key doesn't exist or is corrupted:</span></span> <br/> <span data-ttu-id="7b862-225"><strong>HKLM\Software\Microsoft\Windows</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-225"><strong>HKLM\Software\Microsoft\Windows\</strong></span></span><br/> <span data-ttu-id="7b862-226"><strong>CurrentVersion\Appx\PackageRepositoryRoot</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-226"><strong>CurrentVersion\Appx\PackageRepositoryRoot</strong></span></span><br/> <span data-ttu-id="7b862-227">Pour récupérer à partir de cet État, actualisez votre PC.</span><span class="sxs-lookup"><span data-stu-id="7b862-227">To recover from this state, refresh your PC.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-228"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-228"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="7b862-229"><strong>POLICY_FAILURE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-229"><strong>POLICY_FAILURE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-230">0x80073CFF</span><span class="sxs-lookup"><span data-stu-id="7b862-230">0x80073CFF</span></span></td>
<td><span data-ttu-id="7b862-231">Pour installer cette application, vous avez besoin d’une licence de développeur ou d’un système compatible chargement.</span><span class="sxs-lookup"><span data-stu-id="7b862-231">To install this app, you need a developer license or a sideloading-enabled system.</span></span> <br/> <span data-ttu-id="7b862-232">Vous pouvez recevoir cette erreur si le package ne remplit pas l’une des conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="7b862-232">You may get this error if the package doesn't meet one of the following requirements:</span></span><br/>
<ul>
<li><span data-ttu-id="7b862-233">L’application est déployée à l’aide de la touche F5 dans Visual Studio sur un ordinateur doté d’une licence de développeur Windows.</span><span class="sxs-lookup"><span data-stu-id="7b862-233">The app is deployed using F5 in Visual Studio on a computer with a Windows developer license.</span></span></li>
<li><span data-ttu-id="7b862-234">Le package est signé avec une signature Microsoft et déployé dans le cadre de Windows ou de l’Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="7b862-234">The package is signed with a Microsoft signature and deployed as part of Windows or from the Microsoft Store.</span></span></li>
<li><span data-ttu-id="7b862-235">Le package est signé avec une signature approuvée et installé sur un ordinateur disposant d’une licence de développeur, d’un ordinateur joint à un domaine avec la stratégie AllowAllTrustedApps activée, ou d’un ordinateur avec une licence Windows chargement avec la stratégie AllowAllTrustedApps activée.</span><span class="sxs-lookup"><span data-stu-id="7b862-235">The package is signed with a trusted signature and installed on a computer with a developer license, a domain-joined computer with the AllowAllTrustedApps policy enabled, or a computer with a Windows Sideloading license with the AllowAllTrustedApps policy enabled.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-236"><strong>ERROR_PACKAGE_UPDATING</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-236"><strong>ERROR_PACKAGE_UPDATING</strong></span></span></td>
<td><span data-ttu-id="7b862-237">0x80073D00</span><span class="sxs-lookup"><span data-stu-id="7b862-237">0x80073D00</span></span></td>
<td><span data-ttu-id="7b862-238">L’application ne peut pas être démarrée car elle est en cours de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="7b862-238">The app can't be started because it's currently updating.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-239"><strong>ERROR_DEPLOYMENT_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-239"><strong>ERROR_DEPLOYMENT_</strong></span></span><br/> <span data-ttu-id="7b862-240"><strong>BLOCKED_BY_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-240"><strong>BLOCKED_BY_POLICY</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-241">0x80073D01</span><span class="sxs-lookup"><span data-stu-id="7b862-241">0x80073D01</span></span></td>
<td><span data-ttu-id="7b862-242">L’opération de déploiement de package est bloquée par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="7b862-242">The package deployment operation is blocked by policy.</span></span> <span data-ttu-id="7b862-243">Contactez votre administrateur système.</span><span class="sxs-lookup"><span data-stu-id="7b862-243">Contact your system administrator.</span></span><br/> <span data-ttu-id="7b862-244">Causes possibles :</span><span class="sxs-lookup"><span data-stu-id="7b862-244">Possible causes:</span></span><br/>
<ul>
<li><span data-ttu-id="7b862-245">Le déploiement de package est bloqué par les stratégies de contrôle d’application.</span><span class="sxs-lookup"><span data-stu-id="7b862-245">Package deployment is blocked by Application Control Policies.</span></span></li>
<li><span data-ttu-id="7b862-246">Le déploiement de package est bloqué par la &quot; stratégie autoriser les opérations de déploiement dans les profils spéciaux &quot; .</span><span class="sxs-lookup"><span data-stu-id="7b862-246">Package deployment is blocked by the &quot;Allow deployment operations in special profiles&quot; policy.</span></span></li>
</ul>
<span data-ttu-id="7b862-247">L’une des raisons possibles est la nécessité d’un profil itinérant.</span><span class="sxs-lookup"><span data-stu-id="7b862-247">One of the possible reasons is a need for a roaming profile.</span></span> <span data-ttu-id="7b862-248">Pour plus d’informations sur la configuration des profils utilisateur itinérants sur des comptes d’utilisateur, consultez <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">déployer des profils utilisateur itinérants</a>.</span><span class="sxs-lookup"><span data-stu-id="7b862-248">For information about setting up Roaming User Profiles on user accounts, see <a href="/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/jj649079(v=ws.11)">Deploy Roaming User Profiles</a>.</span></span> <span data-ttu-id="7b862-249">Si aucune stratégie n’est configurée sur votre système et que vous voyez toujours cette erreur, vous êtes peut-être connecté avec un profil temporaire.</span><span class="sxs-lookup"><span data-stu-id="7b862-249">If there are no policies configured on your system and you still see this error, perhaps you are logged in with a temporary profile.</span></span> <span data-ttu-id="7b862-250">Déconnectez-vous et reconnectez-vous, puis recommencez l’opération.</span><span class="sxs-lookup"><span data-stu-id="7b862-250">Log out and log in again, then try the operation again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-251"><strong>ERROR_PACKAGES_IN_USE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-251"><strong>ERROR_PACKAGES_IN_USE</strong></span></span></td>
<td><span data-ttu-id="7b862-252">0x80073D02</span><span class="sxs-lookup"><span data-stu-id="7b862-252">0x80073D02</span></span></td>
<td><span data-ttu-id="7b862-253">Le package n’a pas pu être installé car les ressources qu’il modifie sont actuellement utilisées.</span><span class="sxs-lookup"><span data-stu-id="7b862-253">The package couldn't be installed because resources it modifies are currently in use.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-254"><strong>ERROR_RECOVERY_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-254"><strong>ERROR_RECOVERY_</strong></span></span><br/> <span data-ttu-id="7b862-255"><strong>FILE_CORRUPT</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-255"><strong>FILE_CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-256">0x80073D03</span><span class="sxs-lookup"><span data-stu-id="7b862-256">0x80073D03</span></span></td>
<td><span data-ttu-id="7b862-257">Le package n’a pas pu être récupéré car les données nécessaires à la récupération sont endommagées.</span><span class="sxs-lookup"><span data-stu-id="7b862-257">The package couldn't be recovered because data that's necessary for recovery is corrupted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-258"><strong>ERROR_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-258"><strong>ERROR_INVALID_</strong></span></span><br/> <span data-ttu-id="7b862-259"><strong>STAGED_SIGNATURE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-259"><strong>STAGED_SIGNATURE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-260">0x80073D04</span><span class="sxs-lookup"><span data-stu-id="7b862-260">0x80073D04</span></span></td>
<td><span data-ttu-id="7b862-261">La signature n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7b862-261">The signature isn't valid.</span></span> <span data-ttu-id="7b862-262">Pour s’inscrire en mode développeur, AppxSignature. p7x et AppxBlockMap.xml doivent être valides ou ne doivent pas être présents.</span><span class="sxs-lookup"><span data-stu-id="7b862-262">To register in developer mode, AppxSignature.p7x and AppxBlockMap.xml must be valid or shouldn't be present.</span></span><br/> <span data-ttu-id="7b862-263">Si vous êtes développeur à l’aide de la touche F5 avec Visual Studio, assurez-vous que votre répertoire de projet créé ne contient pas de signature ou de fichier de mappage de bloc à partir des versions précédentes du package.</span><span class="sxs-lookup"><span data-stu-id="7b862-263">If you are a developer using F5 with Visual Studio, ensure that your built project directory doesn't contain signature or block map files from previous versions of the package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-264"><strong>ERROR_DELETING_EXISTING_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-264"><strong>ERROR_DELETING_EXISTING_</strong></span></span><br/> <span data-ttu-id="7b862-265"><strong>APPLICATIONDATA_STORE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-265"><strong>APPLICATIONDATA_STORE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-266">0x80073D05</span><span class="sxs-lookup"><span data-stu-id="7b862-266">0x80073D05</span></span></td>
<td><span data-ttu-id="7b862-267">Une erreur s’est produite lors de la suppression des données d’application précédemment existantes du package.</span><span class="sxs-lookup"><span data-stu-id="7b862-267">An error occurred while deleting the package's previously existing application data.</span></span><br/> <span data-ttu-id="7b862-268">Vous pouvez recevoir cette erreur si le <a href="/previous-versions/hh441475(v=vs.110)">simulateur</a> est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7b862-268">You can get this error if the <a href="/previous-versions/hh441475(v=vs.110)">simulator</a> is running.</span></span> <span data-ttu-id="7b862-269">Fermez le simulateur.</span><span class="sxs-lookup"><span data-stu-id="7b862-269">Close the simulator.</span></span> <span data-ttu-id="7b862-270">Vous pouvez également obtenir cette erreur si des fichiers sont ouverts dans les données de l’application (par exemple, si un fichier journal est ouvert dans un éditeur de texte).</span><span class="sxs-lookup"><span data-stu-id="7b862-270">You can also get this error if there are files open in the app data (for example, if you have a log file open in a text editor).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-271"><strong>ERROR_INSTALL_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-271"><strong>ERROR_INSTALL_</strong></span></span><br/> <span data-ttu-id="7b862-272"><strong>PACKAGE_DOWNGRADE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-272"><strong>PACKAGE_DOWNGRADE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-273">0x80073D06</span><span class="sxs-lookup"><span data-stu-id="7b862-273">0x80073D06</span></span></td>
<td><span data-ttu-id="7b862-274">Le package n’a pas pu être installé car une version plus récente de ce package est déjà installée.</span><span class="sxs-lookup"><span data-stu-id="7b862-274">The package couldn't be installed because a higher version of this package is already installed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-275"><strong>ERROR_SYSTEM_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-275"><strong>ERROR_SYSTEM_</strong></span></span><br/> <span data-ttu-id="7b862-276"><strong>NEEDS_REMEDIATION</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-276"><strong>NEEDS_REMEDIATION</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-277">0x80073D07</span><span class="sxs-lookup"><span data-stu-id="7b862-277">0x80073D07</span></span></td>
<td><span data-ttu-id="7b862-278">Une erreur a été détectée dans un fichier binaire système.</span><span class="sxs-lookup"><span data-stu-id="7b862-278">An error in a system binary was detected.</span></span> <span data-ttu-id="7b862-279">Pour résoudre le problème, essayez d’actualiser le PC.</span><span class="sxs-lookup"><span data-stu-id="7b862-279">To fix the problem, try refreshing the PC.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-280"><strong>ERROR_APPX_INTEGRITY_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-280"><strong>ERROR_APPX_INTEGRITY_</strong></span></span><br/> <span data-ttu-id="7b862-281"><strong>FAILURE_EXTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-281"><strong>FAILURE_EXTERNAL</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-282">0x80073D08</span><span class="sxs-lookup"><span data-stu-id="7b862-282">0x80073D08</span></span></td>
<td><span data-ttu-id="7b862-283">Un fichier binaire non-Windows endommagé a été détecté sur le système.</span><span class="sxs-lookup"><span data-stu-id="7b862-283">A corrupted non-Windows binary was detected on the system.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-284"><strong>ERROR_RESILIENCY_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-284"><strong>ERROR_RESILIENCY_</strong></span></span><br/> <span data-ttu-id="7b862-285"><strong>FILE_CORRUPT</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-285"><strong>FILE_CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-286">0x80073D09</span><span class="sxs-lookup"><span data-stu-id="7b862-286">0x80073D09</span></span></td>
<td><span data-ttu-id="7b862-287">Impossible de reprendre l’opération, car les données nécessaires à la récupération sont endommagées.</span><span class="sxs-lookup"><span data-stu-id="7b862-287">The operation couldn't be resumed because data that's necessary for recovery is corrupted.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-288"><strong>ERROR_INSTALL_FIREWALL_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-288"><strong>ERROR_INSTALL_FIREWALL_</strong></span></span><br/> <span data-ttu-id="7b862-289"><strong>SERVICE_NOT_RUNNING</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-289"><strong>SERVICE_NOT_RUNNING</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-290">0x80073D0A</span><span class="sxs-lookup"><span data-stu-id="7b862-290">0x80073D0A</span></span></td>
<td><span data-ttu-id="7b862-291">Le package n’a pas pu être installé car le service pare-feu Windows n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7b862-291">The package couldn't be installed because the Windows Firewall service isn't running.</span></span> <span data-ttu-id="7b862-292">Activez le service pare-feu Windows, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="7b862-292">Enable the Windows Firewall service and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-293"><strong>ERROR_PACKAGE_MOVE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-293"><strong>ERROR_PACKAGE_MOVE_FAILED</strong></span></span></td>
<td><span data-ttu-id="7b862-294">0x80073D0B</span><span class="sxs-lookup"><span data-stu-id="7b862-294">0x80073D0B</span></span></td>
<td><span data-ttu-id="7b862-295">Échec de l’opération de déplacement du package.</span><span class="sxs-lookup"><span data-stu-id="7b862-295">The package move operation failed.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-296"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-296"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="7b862-297"><strong>NOT_EMPTY</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-297"><strong>NOT_EMPTY</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-298">0x80073D0C</span><span class="sxs-lookup"><span data-stu-id="7b862-298">0x80073D0C</span></span></td>
<td><span data-ttu-id="7b862-299">L’opération de déploiement a échoué, car le volume n’est pas vide.</span><span class="sxs-lookup"><span data-stu-id="7b862-299">The deployment operation failed because the volume is not empty.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-300"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-300"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="7b862-301"><strong>HORS connexion</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-301"><strong>OFFLINE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-302">0x80073D0D</span><span class="sxs-lookup"><span data-stu-id="7b862-302">0x80073D0D</span></span></td>
<td><span data-ttu-id="7b862-303">L’opération de déploiement a échoué car le volume est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="7b862-303">The deployment operation failed because the volume is offline.</span></span> <span data-ttu-id="7b862-304">Pour une mise à jour de package, le volume fait référence au volume installé de toutes les versions de package.</span><span class="sxs-lookup"><span data-stu-id="7b862-304">For a package update, the volume refers to the installed volume of all package versions.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-305"><strong>ERROR_INSTALL_VOLUME_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-305"><strong>ERROR_INSTALL_VOLUME_</strong></span></span><br/> <span data-ttu-id="7b862-306"><strong>ENDOMMAGÉ</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-306"><strong>CORRUPT</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-307">0x80073D0E</span><span class="sxs-lookup"><span data-stu-id="7b862-307">0x80073D0E</span></span></td>
<td><span data-ttu-id="7b862-308">L’opération de déploiement a échoué, car le volume spécifié est endommagé.</span><span class="sxs-lookup"><span data-stu-id="7b862-308">The deployment operation failed because the specified volume is corrupt.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-309"><strong>ERROR_NEEDS_REGISTRATION</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-309"><strong>ERROR_NEEDS_REGISTRATION</strong></span></span><br/> <strong></strong><br/></td>
<td><span data-ttu-id="7b862-310">0x80073D0F</span><span class="sxs-lookup"><span data-stu-id="7b862-310">0x80073D0F</span></span></td>
<td><span data-ttu-id="7b862-311">L’opération de déploiement a échoué car l’application spécifiée doit être inscrite en premier.</span><span class="sxs-lookup"><span data-stu-id="7b862-311">The deployment operation failed because the specified application needs to be registered first.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-312"><strong>ERROR_INSTALL_WRONG_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-312"><strong>ERROR_INSTALL_WRONG_</strong></span></span><br/> <span data-ttu-id="7b862-313"><strong>PROCESSOR_ARCHITECTURE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-313"><strong>PROCESSOR_ARCHITECTURE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-314">0x80073D10</span><span class="sxs-lookup"><span data-stu-id="7b862-314">0x80073D10</span></span></td>
<td><span data-ttu-id="7b862-315">L’opération de déploiement a échoué, car le package cible une architecture de processeur incorrecte.</span><span class="sxs-lookup"><span data-stu-id="7b862-315">The deployment operation failed because the package targets the wrong processor architecture.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-316"><strong>ERROR_DEV_SIDELOAD_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-316"><strong>ERROR_DEV_SIDELOAD_</strong></span></span><br/> <span data-ttu-id="7b862-317"><strong>LIMIT_EXCEEDED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-317"><strong>LIMIT_EXCEEDED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-318">0x80073D11</span><span class="sxs-lookup"><span data-stu-id="7b862-318">0x80073D11</span></span></td>
<td><span data-ttu-id="7b862-319">Vous avez atteint le nombre maximal de packages faisant développeur autorisés sur cet appareil.</span><span class="sxs-lookup"><span data-stu-id="7b862-319">You have reached the maximum number of developer sideloaded packages allowed on this device.</span></span> <span data-ttu-id="7b862-320">Désinstallez un package faisant, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="7b862-320">Please uninstall a sideloaded package and try again.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-321"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-321"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="7b862-322"><strong>PACKAGE_REQUIRES_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-322"><strong>PACKAGE_REQUIRES_</strong></span></span><br/> <span data-ttu-id="7b862-323"><strong>MAIN_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-323"><strong>MAIN_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-324">0x80073D12</span><span class="sxs-lookup"><span data-stu-id="7b862-324">0x80073D12</span></span></td>
<td><span data-ttu-id="7b862-325">Un package d’application principal est requis pour installer ce package facultatif.</span><span class="sxs-lookup"><span data-stu-id="7b862-325">A main app package is required to install this optional package.</span></span> <span data-ttu-id="7b862-326">Installez d’abord le package principal, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="7b862-326">Install the main package first and try again.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-327"><strong>ERROR_PACKAGE_NOT_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-327"><strong>ERROR_PACKAGE_NOT_</strong></span></span><br/> <span data-ttu-id="7b862-328"><strong>SUPPORTED_ON_FILESYSTEM</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-328"><strong>SUPPORTED_ON_FILESYSTEM</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-329">0x80073D13</span><span class="sxs-lookup"><span data-stu-id="7b862-329">0x80073D13</span></span></td>
<td><span data-ttu-id="7b862-330">Ce type de package d’application n’est pas pris en charge sur ce système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="7b862-330">This app package type is not supported on this filesystem.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-331"><strong>ERROR_PACKAGE_MOVE_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-331"><strong>ERROR_PACKAGE_MOVE_</strong></span></span><br/> <span data-ttu-id="7b862-332"><strong>BLOCKED_BY_STREAMING</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-332"><strong>BLOCKED_BY_STREAMING</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-333">0x80073D14</span><span class="sxs-lookup"><span data-stu-id="7b862-333">0x80073D14</span></span></td>
<td><span data-ttu-id="7b862-334">L’opération de déplacement du package est bloquée jusqu’à la fin de la diffusion de l’application.</span><span class="sxs-lookup"><span data-stu-id="7b862-334">Package move operation is blocked until the application has finished streaming.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-335"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-335"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="7b862-336"><strong>PACKAGE_APPLICATIONID_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-336"><strong>PACKAGE_APPLICATIONID_</strong></span></span><br/> <span data-ttu-id="7b862-337"><strong>NOT_UNIQUE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-337"><strong>NOT_UNIQUE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-338">0x80073D15</span><span class="sxs-lookup"><span data-stu-id="7b862-338">0x80073D15</span></span></td>
<td><span data-ttu-id="7b862-339">Un package d’application principal ou un autre package d’application facultatif possède le même ID d’application que ce package facultatif.</span><span class="sxs-lookup"><span data-stu-id="7b862-339">A main or another optional app package has the same application ID as this optional package.</span></span> <span data-ttu-id="7b862-340">Modifiez l’ID de l’application pour le package facultatif afin d’éviter les conflits.</span><span class="sxs-lookup"><span data-stu-id="7b862-340">Change the application ID for the optional package to avoid conflicts.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-341"><strong>ERROR_PACKAGE_STAGING_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-341"><strong>ERROR_PACKAGE_STAGING_</strong></span></span><br/> <span data-ttu-id="7b862-342"><strong>ONHOLD</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-342"><strong>ONHOLD</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-343">0x80073D16</span><span class="sxs-lookup"><span data-stu-id="7b862-343">0x80073D16</span></span></td>
<td><span data-ttu-id="7b862-344">Cette session intermédiaire a été conservée pour permettre la hiérarchisation d’une autre opération intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="7b862-344">This staging session has been held to allow another staging operation to be prioritized.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-345"><strong>ERROR_INSTALL_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-345"><strong>ERROR_INSTALL_INVALID_</strong></span></span><br/> <span data-ttu-id="7b862-346"><strong>RELATED_SET_UPDATE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-346"><strong>RELATED_SET_UPDATE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-347">0x80073D17</span><span class="sxs-lookup"><span data-stu-id="7b862-347">0x80073D17</span></span></td>
<td><span data-ttu-id="7b862-348">Impossible de mettre à jour un jeu associé, car le jeu mis à jour n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7b862-348">A related set cannot be updated because the updated set is invalid.</span></span> <span data-ttu-id="7b862-349">Tous les packages de l’ensemble associé doivent être mis à jour en même temps.</span><span class="sxs-lookup"><span data-stu-id="7b862-349">All packages in the related set must be updated at the same time.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-350"><strong>ERROR_INSTALL_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-350"><strong>ERROR_INSTALL_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="7b862-351"><strong>PACKAGE_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-351"><strong>PACKAGE_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="7b862-352"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-352"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-353">0x80073D18</span><span class="sxs-lookup"><span data-stu-id="7b862-353">0x80073D18</span></span></td>
<td><span data-ttu-id="7b862-354">Pour un package facultatif avec un point d’entrée FullTrust, le package principal doit disposer de la fonctionnalité <strong>runFullTrust</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b862-354">An optional package with a FullTrust entry point requires the main package to have the <strong>runFullTrust</strong> capability.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-355"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-355"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="7b862-356"><strong>BY_USER_LOG_OFF</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-356"><strong>BY_USER_LOG_OFF</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-357">0x80073D19</span><span class="sxs-lookup"><span data-stu-id="7b862-357">0x80073D19</span></span></td>
<td><span data-ttu-id="7b862-358">Une erreur s’est produite en raison de la fermeture de la session d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7b862-358">An error occurred because a user was logged off.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-359"><strong>ERROR_PROVISION_OPTIONAL_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-359"><strong>ERROR_PROVISION_OPTIONAL_</strong></span></span><br/> <span data-ttu-id="7b862-360"><strong>PACKAGE_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-360"><strong>PACKAGE_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="7b862-361"><strong>PACKAGE_PROVISIONED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-361"><strong>PACKAGE_PROVISIONED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-362">0x80073D1A</span><span class="sxs-lookup"><span data-stu-id="7b862-362">0x80073D1A</span></span></td>
<td><span data-ttu-id="7b862-363">Une provision facultative de packages nécessite que le package principal de dépendance soit également approvisionné.</span><span class="sxs-lookup"><span data-stu-id="7b862-363">An optional package provision requires the dependency main package to also be provisioned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-364"><strong>ERROR_PACKAGES_REPUTATION_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-364"><strong>ERROR_PACKAGES_REPUTATION_</strong></span></span><br/> <span data-ttu-id="7b862-365"><strong>CHECK_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-365"><strong>CHECK_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-366">0x80073D1B</span><span class="sxs-lookup"><span data-stu-id="7b862-366">0x80073D1B</span></span></td>
<td><span data-ttu-id="7b862-367">Les packages n’ont pas pu <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">Vérifier la réputation SmartScreen</a>.</span><span class="sxs-lookup"><span data-stu-id="7b862-367">The packages failed the <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen reputation check</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-368"><strong>ERROR_PACKAGES_REPUTATION_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-368"><strong>ERROR_PACKAGES_REPUTATION_</strong></span></span><br/> <span data-ttu-id="7b862-369"><strong>CHECK_TIMEDOUT</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-369"><strong>CHECK_TIMEDOUT</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-370">0x80073D1C</span><span class="sxs-lookup"><span data-stu-id="7b862-370">0x80073D1C</span></span></td>
<td><span data-ttu-id="7b862-371">L’opération de vérification de la <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">réputation SmartScreen</a> a expiré.</span><span class="sxs-lookup"><span data-stu-id="7b862-371">The <a href="/windows/security/threat-protection/windows-defender-smartscreen/windows-defender-smartscreen-overview">SmartScreen reputation check</a> operation timed out.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-372"><strong>ERROR_DEPLOYMENT_OPTION_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-372"><strong>ERROR_DEPLOYMENT_OPTION_</strong></span></span><br/> <span data-ttu-id="7b862-373"><strong>NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-373"><strong>NOT_SUPPORTED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-374">0x80073D1D</span><span class="sxs-lookup"><span data-stu-id="7b862-374">0x80073D1D</span></span></td>
<td><span data-ttu-id="7b862-375">L’option de déploiement actuelle n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7b862-375">The current deployment option is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-376"><strong>ERROR_APPINSTALLER_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-376"><strong>ERROR_APPINSTALLER_</strong></span></span><br/> <span data-ttu-id="7b862-377"><strong>ACTIVATION_BLOCKED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-377"><strong>ACTIVATION_BLOCKED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-378">0x80073D1E</span><span class="sxs-lookup"><span data-stu-id="7b862-378">0x80073D1E</span></span></td>
<td><span data-ttu-id="7b862-379">L’activation est bloquée en raison des paramètres de mise à jour. appinstaller pour cette application.</span><span class="sxs-lookup"><span data-stu-id="7b862-379">Activation is blocked due to the .appinstaller update settings for this app.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-380"><strong>ERROR_REGISTRATION_FROM_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-380"><strong>ERROR_REGISTRATION_FROM_</strong></span></span><br/> <span data-ttu-id="7b862-381"><strong>REMOTE_DRIVE_NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-381"><strong>REMOTE_DRIVE_NOT_SUPPORTED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-382">0x80073D1F</span><span class="sxs-lookup"><span data-stu-id="7b862-382">0x80073D1F</span></span></td>
<td><span data-ttu-id="7b862-383">Les lecteurs distants ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7b862-383">Remote drives are not supported.</span></span> <span data-ttu-id="7b862-384">Utilisez <strong> \\ server\share</strong> pour inscrire un package distant.</span><span class="sxs-lookup"><span data-stu-id="7b862-384">Use <strong>\\server\share</strong> to register a remote package.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-385"><strong>ERROR_APPX_RAW_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-385"><strong>ERROR_APPX_RAW_</strong></span></span><br/> <span data-ttu-id="7b862-386"><strong>DATA_WRITE_FAILED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-386"><strong>DATA_WRITE_FAILED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-387">0x80073D20</span><span class="sxs-lookup"><span data-stu-id="7b862-387">0x80073D20</span></span></td>
<td><span data-ttu-id="7b862-388">Échec du traitement et de l’écriture des données du package téléchargé sur le disque.</span><span class="sxs-lookup"><span data-stu-id="7b862-388">Failed to process and write downloaded package data to disk.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-389"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-389"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="7b862-390"><strong>BY_VOLUME_POLICY_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-390"><strong>BY_VOLUME_POLICY_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-391">0x80073D21</span><span class="sxs-lookup"><span data-stu-id="7b862-391">0x80073D21</span></span></td>
<td><span data-ttu-id="7b862-392">L’opération de déploiement a été bloquée en raison d’une stratégie par famille de packages qui limite les déploiements sur un volume non-système.</span><span class="sxs-lookup"><span data-stu-id="7b862-392">The deployment operation was blocked due to a per-package-family policy restricting deployments on a non-system volume.</span></span> <span data-ttu-id="7b862-393">Par stratégie, cette application doit être installée sur le lecteur système, mais elle n’est pas définie par défaut.</span><span class="sxs-lookup"><span data-stu-id="7b862-393">Per policy, this app must be installed to the system drive, but that's not set as the default.</span></span> <span data-ttu-id="7b862-394">Dans paramètres de stockage, définissez le lecteur système comme emplacement par défaut pour enregistrer le nouveau contenu, puis réessayez l’installation.</span><span class="sxs-lookup"><span data-stu-id="7b862-394">In Storage settings, make the system drive the default location to save new content, then retry the install.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-395"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-395"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="7b862-396"><strong>BY_VOLUME_POLICY_MACHINE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-396"><strong>BY_VOLUME_POLICY_MACHINE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-397">0x80073D22</span><span class="sxs-lookup"><span data-stu-id="7b862-397">0x80073D22</span></span></td>
<td><span data-ttu-id="7b862-398">L’opération de déploiement a été bloquée en raison d’une stratégie au niveau de l’ordinateur qui limite les déploiements sur un volume non-système.</span><span class="sxs-lookup"><span data-stu-id="7b862-398">The deployment operation was blocked due to a machine-wide policy restricting deployments on a non-system volume.</span></span> <span data-ttu-id="7b862-399">Par stratégie, cette application doit être installée sur le lecteur système, mais elle n’est pas définie par défaut.</span><span class="sxs-lookup"><span data-stu-id="7b862-399">Per policy, this app must be installed to the system drive, but that's not set as the default.</span></span> <span data-ttu-id="7b862-400">Dans paramètres de stockage, définissez le lecteur système comme emplacement par défaut pour enregistrer le nouveau contenu, puis réessayez l’installation.</span><span class="sxs-lookup"><span data-stu-id="7b862-400">In Storage settings, make the system drive the default location to save new content, then retry the install.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-401"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-401"><strong>ERROR_DEPLOYMENT_BLOCKED_</strong></span></span><br/> <span data-ttu-id="7b862-402"><strong>BY_PROFILE_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-402"><strong>BY_PROFILE_POLICY</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-403">0x80073D23</span><span class="sxs-lookup"><span data-stu-id="7b862-403">0x80073D23</span></span></td>
<td><span data-ttu-id="7b862-404">L’opération de déploiement a été bloquée, car un déploiement de profil spécial n’est pas autorisé (les profils spéciaux sont des profils utilisateur où les modifications sont ignorées une fois que l’utilisateur se déconnecte).</span><span class="sxs-lookup"><span data-stu-id="7b862-404">The deployment operation was blocked because special profile deployment is not allowed (special profiles are user profiles where changes are discarded after the user signs out).</span></span> <span data-ttu-id="7b862-405">Essayez de vous connecter à un compte qui n’est pas un profil spécial.</span><span class="sxs-lookup"><span data-stu-id="7b862-405">Try logging into an account that is not a special profile.</span></span> <span data-ttu-id="7b862-406">Vous pouvez essayer de vous déconnecter et de vous reconnecter au compte actif, ou essayer de vous connecter à un autre compte.</span><span class="sxs-lookup"><span data-stu-id="7b862-406">You can try logging out and logging back into the current account, or try logging into a different account.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-407"><strong>ERROR_DEPLOYMENT_FAILED_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-407"><strong>ERROR_DEPLOYMENT_FAILED_</strong></span></span><br/> <span data-ttu-id="7b862-408"><strong>CONFLICTING_MUTABLE_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-408"><strong>CONFLICTING_MUTABLE_PACKAGE_</strong></span></span><br/> <span data-ttu-id="7b862-409"><strong>DIRECTORY</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-409"><strong>DIRECTORY</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-410">0x80073D24</span><span class="sxs-lookup"><span data-stu-id="7b862-410">0x80073D24</span></span></td>
<td><span data-ttu-id="7b862-411">L’opération de déploiement a échoué en raison d’un <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">Répertoire de packages mutable</a>en conflit.</span><span class="sxs-lookup"><span data-stu-id="7b862-411">The deployment operation failed due to a conflicting package's <a href="/uwp/schemas/appxpackage/uapmanifestschema/element-desktop6-mutablepackagedirectory">mutable package directory</a>.</span></span> <span data-ttu-id="7b862-412">Pour installer ce package, supprimez le package existant avec le répertoire de packages mutable en conflit.</span><span class="sxs-lookup"><span data-stu-id="7b862-412">To install this package, remove the existing package with the conflicting mutable package directory.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-413"><strong>ERROR_SINGLETON_RESOURCE_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-413"><strong>ERROR_SINGLETON_RESOURCE_</strong></span></span><br/> <span data-ttu-id="7b862-414"><strong>INSTALLED_IN_ACTIVE_USER</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-414"><strong>INSTALLED_IN_ACTIVE_USER</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-415">0x80073D25</span><span class="sxs-lookup"><span data-stu-id="7b862-415">0x80073D25</span></span></td>
<td><span data-ttu-id="7b862-416">L’installation du package a échoué, car une ressource Singleton a été spécifiée et un autre utilisateur sur lequel ce package est installé est connecté.</span><span class="sxs-lookup"><span data-stu-id="7b862-416">The package installation failed because a singleton resource was specified and another user with that package installed is logged in.</span></span> <span data-ttu-id="7b862-417">Assurez-vous que tous les utilisateurs actifs sur lesquels le package est installé sont déconnectés et réessayez l’installation.</span><span class="sxs-lookup"><span data-stu-id="7b862-417">Make sure that all active users with the package installed are logged out and retry installation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-418">ERROR_DIFFERENT_VERSION_<strong></strong></span><span class="sxs-lookup"><span data-stu-id="7b862-418">ERROR_DIFFERENT_VERSION_<strong></strong></span></span><br/> <span data-ttu-id="7b862-419"><strong>OF_PACKAGED_SERVICE_INSTALLED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-419"><strong>OF_PACKAGED_SERVICE_INSTALLED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-420">0x80073D26</span><span class="sxs-lookup"><span data-stu-id="7b862-420">0x80073D26</span></span></td>
<td><span data-ttu-id="7b862-421">L’installation du package a échoué car une autre version du service est installée.</span><span class="sxs-lookup"><span data-stu-id="7b862-421">The package installation failed because a different version of the service is installed.</span></span> <span data-ttu-id="7b862-422">Essayez d’installer une version plus récente du package.</span><span class="sxs-lookup"><span data-stu-id="7b862-422">Try installing a newer version of the package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-423"><strong>ERROR_SERVICE_EXISTS_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-423"><strong>ERROR_SERVICE_EXISTS_</strong></span></span><br/> <span data-ttu-id="7b862-424"><strong>AS_NON_PACKAGED_SERVICE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-424"><strong>AS_NON_PACKAGED_SERVICE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-425">0x80073D27</span><span class="sxs-lookup"><span data-stu-id="7b862-425">0x80073D27</span></span></td>
<td><span data-ttu-id="7b862-426">L’installation du package a échoué, car une version du service existe en dehors d’un package. msix/. Appx.</span><span class="sxs-lookup"><span data-stu-id="7b862-426">The package installation failed because a version of the service exists outside of an .msix/.appx package.</span></span> <span data-ttu-id="7b862-427">Contactez votre fournisseur de logiciels.</span><span class="sxs-lookup"><span data-stu-id="7b862-427">Contact your software vendor.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-428"><strong>ERROR_PACKAGED_SERVICE_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-428"><strong>ERROR_PACKAGED_SERVICE_</strong></span></span><br/> <span data-ttu-id="7b862-429"><strong>REQUIRES_ADMIN_PRIVILEGES</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-429"><strong>REQUIRES_ADMIN_PRIVILEGES</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-430">0x80073D28</span><span class="sxs-lookup"><span data-stu-id="7b862-430">0x80073D28</span></span></td>
<td><span data-ttu-id="7b862-431">L’installation du package a échoué car des privilèges d’administrateur sont requis.</span><span class="sxs-lookup"><span data-stu-id="7b862-431">The package installation failed because administrator privileges are required.</span></span> <span data-ttu-id="7b862-432">Contactez un administrateur pour installer ce package.</span><span class="sxs-lookup"><span data-stu-id="7b862-432">Contact an administrator to install this package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-433"><strong>ERROR_REDIRECTION_TO_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-433"><strong>ERROR_REDIRECTION_TO_</strong></span></span><br/> <span data-ttu-id="7b862-434"><strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-434"><strong>DEFAULT_ACCOUNT_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-435">0x80073D29</span><span class="sxs-lookup"><span data-stu-id="7b862-435">0x80073D29</span></span></td>
<td><span data-ttu-id="7b862-436">Le déploiement du package a échoué, car l’opération aurait été redirigée vers le compte par défaut, lorsque l’appelant ne l’a pas fait.</span><span class="sxs-lookup"><span data-stu-id="7b862-436">The package deployment failed because the operation would have redirected to default account, when the caller said not to do so.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-437"><strong>ERROR_PACKAGE_LACKS_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-437"><strong>ERROR_PACKAGE_LACKS_</strong></span></span><br/> <span data-ttu-id="7b862-438"><strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-438"><strong>CAPABILITY_TO_DEPLOY_ON_HOST</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-439">0x80073D2A</span><span class="sxs-lookup"><span data-stu-id="7b862-439">0x80073D2A</span></span></td>
<td><span data-ttu-id="7b862-440">Le déploiement du package a échoué, car le package nécessite une capacité à cibler en mode natif cet hôte.</span><span class="sxs-lookup"><span data-stu-id="7b862-440">The package deployment failed because the package requires a capability to natively target this host.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-441"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-441"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="7b862-442"><strong>INVALID_CONTENT</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-442"><strong>INVALID_CONTENT</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-443">0x80073D2B</span><span class="sxs-lookup"><span data-stu-id="7b862-443">0x80073D2B</span></span></td>
<td><span data-ttu-id="7b862-444">Le déploiement du package a échoué, car son contenu n’est pas valide pour un package non signé.</span><span class="sxs-lookup"><span data-stu-id="7b862-444">The package deployment failed because its content is not valid for an unsigned package.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-445"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-445"><strong>ERROR_UNSIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="7b862-446"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-446"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-447">0x80073D2C</span><span class="sxs-lookup"><span data-stu-id="7b862-447">0x80073D2C</span></span></td>
<td><span data-ttu-id="7b862-448">Le déploiement du package a échoué, car son serveur de publication n’est pas dans l’espace de noms non signé.</span><span class="sxs-lookup"><span data-stu-id="7b862-448">The package deployment failed because its publisher is not in the unsigned namespace.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-449"><strong>ERROR_SIGNED_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-449"><strong>ERROR_SIGNED_PACKAGE_</strong></span></span><br/> <span data-ttu-id="7b862-450"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-450"><strong>INVALID_PUBLISHER_NAMESPACE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-451">0x80073D2D</span><span class="sxs-lookup"><span data-stu-id="7b862-451">0x80073D2D</span></span></td>
<td><span data-ttu-id="7b862-452">Le déploiement du package a échoué, car son serveur de publication n’est pas dans l’espace de noms signé.</span><span class="sxs-lookup"><span data-stu-id="7b862-452">The package deployment failed because its publisher is not in the signed namespace.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-453"><strong>ERROR_PACKAGE_EXTERNAL_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-453"><strong>ERROR_PACKAGE_EXTERNAL_</strong></span></span><br/> <span data-ttu-id="7b862-454"><strong>LOCATION_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-454"><strong>LOCATION_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-455">0x80073D2E</span><span class="sxs-lookup"><span data-stu-id="7b862-455">0x80073D2E</span></span></td>
<td><span data-ttu-id="7b862-456">Le déploiement du package a échoué, car son serveur de publication n’est pas dans l’espace de noms signé.</span><span class="sxs-lookup"><span data-stu-id="7b862-456">The package deployment failed because its publisher is not in the signed namespace.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-457"><strong>ERROR_INSTALL_FULLTRUST_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-457"><strong>ERROR_INSTALL_FULLTRUST_</strong></span></span><br/> <span data-ttu-id="7b862-458"><strong>HOSTRUNTIME_REQUIRES_MAIN_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-458"><strong>HOSTRUNTIME_REQUIRES_MAIN_</strong></span></span><br/> <span data-ttu-id="7b862-459"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-459"><strong>PACKAGE_FULLTRUST_CAPABILITY</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-460">0x80073D2F</span><span class="sxs-lookup"><span data-stu-id="7b862-460">0x80073D2F</span></span></td>
<td><span data-ttu-id="7b862-461">Une dépendance de l’exécution de l’hôte qui est résolue en un package avec un contenu de confiance totale requiert que le package principal dispose de la fonctionnalité <strong>runFullTrust</strong> .</span><span class="sxs-lookup"><span data-stu-id="7b862-461">A host runtime dependency resolving to a package with full trust content requires the main package to have the <strong>runFullTrust</strong> capability.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-462"><strong>APPX_E_PACKAGING_INTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-462"><strong>APPX_E_PACKAGING_INTERNAL</strong></span></span></td>
<td><span data-ttu-id="7b862-463">0x80080200</span><span class="sxs-lookup"><span data-stu-id="7b862-463">0x80080200</span></span></td>
<td><span data-ttu-id="7b862-464">L’API de Packaging a rencontré une erreur interne.</span><span class="sxs-lookup"><span data-stu-id="7b862-464">The packaging API has encountered an internal error.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-465"><strong>APPX_E_INTERLEAVING_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-465"><strong>APPX_E_INTERLEAVING_</strong></span></span><br/> <span data-ttu-id="7b862-466"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-466"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-467">0x80080201</span><span class="sxs-lookup"><span data-stu-id="7b862-467">0x80080201</span></span></td>
<td><span data-ttu-id="7b862-468">Le package n’est pas valide car son contenu est entrelacé.</span><span class="sxs-lookup"><span data-stu-id="7b862-468">The package isn't valid because its contents are interleaved.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-469"><strong>APPX_E_RELATIONSHIPS_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-469"><strong>APPX_E_RELATIONSHIPS_</strong></span></span><br/> <span data-ttu-id="7b862-470"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-470"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-471">0x80080202</span><span class="sxs-lookup"><span data-stu-id="7b862-471">0x80080202</span></span></td>
<td><span data-ttu-id="7b862-472">Le package n’est pas valide, car il contient des relations OPC.</span><span class="sxs-lookup"><span data-stu-id="7b862-472">The package isn't valid because it contains OPC relationships.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-473"><strong>APPX_E_MISSING_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-473"><strong>APPX_E_MISSING_</strong></span></span><br/> <span data-ttu-id="7b862-474"><strong>REQUIRED_FILE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-474"><strong>REQUIRED_FILE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-475">0x80080203</span><span class="sxs-lookup"><span data-stu-id="7b862-475">0x80080203</span></span></td>
<td><span data-ttu-id="7b862-476">Le package n’est pas valide, car un manifeste ou un mappage de bloc est manquant, ou un fichier d’intégrité du code est présent, mais un fichier de signature est manquant.</span><span class="sxs-lookup"><span data-stu-id="7b862-476">The package isn't valid because it's missing a manifest or block map, or a code integrity file is present but a signature file is missing.</span></span><br/> <span data-ttu-id="7b862-477">Assurez-vous que le package ne contient pas un ou plusieurs des fichiers requis suivants :</span><span class="sxs-lookup"><span data-stu-id="7b862-477">Ensure that the package isn't missing one or more of these required files:</span></span><br/>
<ul>
<li><span data-ttu-id="7b862-478">\AppxManifest.xml</span><span class="sxs-lookup"><span data-stu-id="7b862-478">\AppxManifest.xml</span></span></li>
<li><span data-ttu-id="7b862-479">\AppxBlockMap.xml</span><span class="sxs-lookup"><span data-stu-id="7b862-479">\AppxBlockMap.xml</span></span></li>
</ul>
<span data-ttu-id="7b862-480">Si le package contient \AppxMetadata\CodeIntegrity.cat, il doit également contenir \AppxSignature.p7x.</span><span class="sxs-lookup"><span data-stu-id="7b862-480">If the package contains \AppxMetadata\CodeIntegrity.cat, it must also contain \AppxSignature.p7x.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-481"><strong>APPX_E_INVALID_MANIFEST</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-481"><strong>APPX_E_INVALID_MANIFEST</strong></span></span></td>
<td><span data-ttu-id="7b862-482">0x80080204</span><span class="sxs-lookup"><span data-stu-id="7b862-482">0x80080204</span></span></td>
<td><span data-ttu-id="7b862-483">Le fichier AppxManifest.xml du package n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7b862-483">The package's AppxManifest.xml file isn't valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-484"><strong>APPX_E_INVALID_BLOCKMAP</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-484"><strong>APPX_E_INVALID_BLOCKMAP</strong></span></span></td>
<td><span data-ttu-id="7b862-485">0x80080205</span><span class="sxs-lookup"><span data-stu-id="7b862-485">0x80080205</span></span></td>
<td><span data-ttu-id="7b862-486">Le fichier AppxBlockMap.xml du package n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7b862-486">The package's AppxBlockMap.xml file isn't valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-487"><strong>APPX_E_CORRUPT_CONTENT</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-487"><strong>APPX_E_CORRUPT_CONTENT</strong></span></span></td>
<td><span data-ttu-id="7b862-488">0x80080206</span><span class="sxs-lookup"><span data-stu-id="7b862-488">0x80080206</span></span></td>
<td><span data-ttu-id="7b862-489">Le contenu du package ne peut pas être lu, car il est endommagé.</span><span class="sxs-lookup"><span data-stu-id="7b862-489">The package contents can't be read because it's corrupted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-490"><strong>APPX_E_BLOCK_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-490"><strong>APPX_E_BLOCK_</strong></span></span><br/> <span data-ttu-id="7b862-491"><strong>HASH_INVALID</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-491"><strong>HASH_INVALID</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-492">0x80080207</span><span class="sxs-lookup"><span data-stu-id="7b862-492">0x80080207</span></span></td>
<td><span data-ttu-id="7b862-493">La valeur de hachage calculée du bloc ne correspond pas à la valeur de est stockée dans le mappage de bloc.</span><span class="sxs-lookup"><span data-stu-id="7b862-493">The computed hash value of the block doesn't match the has value stored in the block map.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-494"><strong>APPX_E_REQUESTED_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-494"><strong>APPX_E_REQUESTED_</strong></span></span><br/> <span data-ttu-id="7b862-495"><strong>RANGE_TOO_LARGE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-495"><strong>RANGE_TOO_LARGE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-496">0x80080208</span><span class="sxs-lookup"><span data-stu-id="7b862-496">0x80080208</span></span></td>
<td><span data-ttu-id="7b862-497">La plage d’octets demandée est supérieure à 4 Go lorsqu’elle est traduite en plage d’octets de blocs.</span><span class="sxs-lookup"><span data-stu-id="7b862-497">The requested byte range is over 4 GB when translated to a byte range of blocks.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-498"><strong>TRUST_E_NOSIGNATURE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-498"><strong>TRUST_E_NOSIGNATURE</strong></span></span></td>
<td><span data-ttu-id="7b862-499">0x800B0100</span><span class="sxs-lookup"><span data-stu-id="7b862-499">0x800B0100</span></span></td>
<td><span data-ttu-id="7b862-500">Aucune signature n’est présente dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="7b862-500">No signature is present in the subject.</span></span><br/> <span data-ttu-id="7b862-501">Vous pouvez recevoir cette erreur si le package n’est pas signé ou si la signature n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7b862-501">You may get this error if the package is unsigned or the signature isn't valid.</span></span> <span data-ttu-id="7b862-502">Le package doit être signé pour être déployé.</span><span class="sxs-lookup"><span data-stu-id="7b862-502">The package must be signed to be deployed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-503"><strong>CERT_E_UNTRUSTEDROOT</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-503"><strong>CERT_E_UNTRUSTEDROOT</strong></span></span></td>
<td><span data-ttu-id="7b862-504">0x800B0109</span><span class="sxs-lookup"><span data-stu-id="7b862-504">0x800B0109</span></span></td>
<td><span data-ttu-id="7b862-505">Une chaîne de certificats A été traitée, mais se termine par un certificat racine qui n’est pas approuvé par le fournisseur d’approbation.</span><span class="sxs-lookup"><span data-stu-id="7b862-505">A certificate chain processed, but terminated in a root certificate which isn't trusted by the trust provider.</span></span><br/> <span data-ttu-id="7b862-506">Consultez <a href="/previous-versions/br230260(v=vs.110)">signature d’un package</a>.</span><span class="sxs-lookup"><span data-stu-id="7b862-506">See <a href="/previous-versions/br230260(v=vs.110)">Signing a package</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-507"><strong>CERT_E_CHAINING</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-507"><strong>CERT_E_CHAINING</strong></span></span></td>
<td><span data-ttu-id="7b862-508">0x800B010A</span><span class="sxs-lookup"><span data-stu-id="7b862-508">0x800B010A</span></span></td>
<td><span data-ttu-id="7b862-509">Impossible de créer une chaîne de certificats pour une autorité de certification racine de confiance.</span><span class="sxs-lookup"><span data-stu-id="7b862-509">A certificate chain couldn't be built to a trusted root certification authority.</span></span><br/> <span data-ttu-id="7b862-510">Consultez <a href="/previous-versions/br230260(v=vs.110)">signature d’un package</a>.</span><span class="sxs-lookup"><span data-stu-id="7b862-510">See <a href="/previous-versions/br230260(v=vs.110)">Signing a package</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-511"><strong>APPX_E_INVALID_</strong> </span><span class="sxs-lookup"><span data-stu-id="7b862-511"><strong>APPX_E_INVALID_</strong> </span></span><br/> <span data-ttu-id="7b862-512"><strong>SIP_CLIENT_DATA</strong> </span><span class="sxs-lookup"><span data-stu-id="7b862-512"><strong>SIP_CLIENT_DATA</strong> </span></span><br/></td>
<td><span data-ttu-id="7b862-513">0x80080209</span><span class="sxs-lookup"><span data-stu-id="7b862-513">0x80080209</span></span></td>
<td><span data-ttu-id="7b862-514">La structure <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>utilisée pour signer le package ne contenait pas les données requises</span><span class="sxs-lookup"><span data-stu-id="7b862-514">The <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>SIP_SUBJECTINFO</strong></a>structure used to sign the package didn't contain the required data</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-515"><strong>APPX_E_INVALID_</strong> </span><span class="sxs-lookup"><span data-stu-id="7b862-515"><strong>APPX_E_INVALID_</strong> </span></span><br/> <span data-ttu-id="7b862-516"><strong>KEY_INFO</strong> </span><span class="sxs-lookup"><span data-stu-id="7b862-516"><strong>KEY_INFO</strong> </span></span><br/></td>
<td><span data-ttu-id="7b862-517">0x8008020A</span><span class="sxs-lookup"><span data-stu-id="7b862-517">0x8008020A</span></span></td>
<td><span data-ttu-id="7b862-518">La structure <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> utilisée pour chiffrer ou déchiffrer le package contient des données non valides.</span><span class="sxs-lookup"><span data-stu-id="7b862-518">The <a href="/windows/win32/api/appxpackaging/ns-appxpackaging-appx_key_info"><strong>APPX_KEY_INFO</strong></a> structure used to encrypt or decrypt the package contains invalid data.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-519"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-519"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="7b862-520"><strong>CONTENTGROUPMAP</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-520"><strong>CONTENTGROUPMAP</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-521">0x8008020B</span><span class="sxs-lookup"><span data-stu-id="7b862-521">0x8008020B</span></span></td>
<td><span data-ttu-id="7b862-522">Le mappage de groupe de contenu du package. msix/. AppX n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7b862-522">The .msix/.appx package's content group map is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-523"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-523"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="7b862-524"><strong>APPINSTALLER</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-524"><strong>APPINSTALLER</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-525">0x8008020C</span><span class="sxs-lookup"><span data-stu-id="7b862-525">0x8008020C</span></span></td>
<td><span data-ttu-id="7b862-526">Le <a href="/windows/msix/app-installer/app-installer-root">fichier. appinstaller</a> du package n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7b862-526">The <a href="/windows/msix/app-installer/app-installer-root">.appinstaller file</a> for the package is invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-527"><strong>APPX_E_DELTA_BASELINE_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-527"><strong>APPX_E_DELTA_BASELINE_</strong></span></span><br/> <span data-ttu-id="7b862-528"><strong>VERSION_MISMATCH</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-528"><strong>VERSION_MISMATCH</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-529">0x8008020D</span><span class="sxs-lookup"><span data-stu-id="7b862-529">0x8008020D</span></span></td>
<td><span data-ttu-id="7b862-530">La version du package de base de référence dans le package delta ne correspond pas à la version du package de base à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="7b862-530">The baseline package version in delta package does not match the version in the baseline package to be updated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-531"><strong>APPX_E_DELTA_PACKAGE_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-531"><strong>APPX_E_DELTA_PACKAGE_</strong></span></span><br/> <span data-ttu-id="7b862-532"><strong>MISSING_FILE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-532"><strong>MISSING_FILE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-533">0x8008020E</span><span class="sxs-lookup"><span data-stu-id="7b862-533">0x8008020E</span></span></td>
<td><span data-ttu-id="7b862-534">Le package delta ne contient pas de fichier du package mis à jour.</span><span class="sxs-lookup"><span data-stu-id="7b862-534">The delta package is missing a file from the updated package.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-535"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-535"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="7b862-536"><strong>DELTA_PACKAGE</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-536"><strong>DELTA_PACKAGE</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-537">0x8008020F</span><span class="sxs-lookup"><span data-stu-id="7b862-537">0x8008020F</span></span></td>
<td><span data-ttu-id="7b862-538">Le package Delta n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7b862-538">The delta package is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-539"><strong>APPX_E_DELTA_APPENDED_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-539"><strong>APPX_E_DELTA_APPENDED_</strong></span></span><br/> <span data-ttu-id="7b862-540"><strong>PACKAGE_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-540"><strong>PACKAGE_NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-541">0x80080210</span><span class="sxs-lookup"><span data-stu-id="7b862-541">0x80080210</span></span></td>
<td><span data-ttu-id="7b862-542">Le package ajouté Delta n’est pas autorisé pour l’opération en cours.</span><span class="sxs-lookup"><span data-stu-id="7b862-542">The delta appended package is not allowed for the current operation.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-543"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-543"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="7b862-544"><strong>PACKAGING_LAYOUT</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-544"><strong>PACKAGING_LAYOUT</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-545">0x80080211</span><span class="sxs-lookup"><span data-stu-id="7b862-545">0x80080211</span></span></td>
<td><span data-ttu-id="7b862-546">Le fichier de disposition d’empaquetage n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7b862-546">The packaging layout file is invalid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-547"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-547"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="7b862-548"><strong>PACKAGESIGNCONFIG</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-548"><strong>PACKAGESIGNCONFIG</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-549">0x80080212</span><span class="sxs-lookup"><span data-stu-id="7b862-549">0x80080212</span></span></td>
<td><span data-ttu-id="7b862-550">Le fichier packageSignConfig n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7b862-550">The packageSignConfig file is invalid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-551"><strong>APPX_E_RESOURCESPRI_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-551"><strong>APPX_E_RESOURCESPRI_</strong></span></span><br/> <span data-ttu-id="7b862-552"><strong>NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-552"><strong>NOT_ALLOWED</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-553">0x80080213</span><span class="sxs-lookup"><span data-stu-id="7b862-553">0x80080213</span></span></td>
<td><span data-ttu-id="7b862-554">Le fichier Resources. pri n’est pas autorisé lorsqu’il n’existe aucun élément de ressource dans le manifeste du package.</span><span class="sxs-lookup"><span data-stu-id="7b862-554">The resources.pri file is not allowed when there are no resource elements in the package manifest.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-555"><strong>APPX_E_FILE_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-555"><strong>APPX_E_FILE_</strong></span></span><br/> <span data-ttu-id="7b862-556"><strong>COMPRESSION_MISMATCH</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-556"><strong>COMPRESSION_MISMATCH</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-557">0x80080214</span><span class="sxs-lookup"><span data-stu-id="7b862-557">0x80080214</span></span></td>
<td><span data-ttu-id="7b862-558">L’état de compression du fichier dans la ligne de base et le package mis à jour ne correspond pas.</span><span class="sxs-lookup"><span data-stu-id="7b862-558">The compression state of file in baseline and updated package does not match.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7b862-559"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-559"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="7b862-560"><strong>PAYLOAD_PACKAGE_EXTENSION</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-560"><strong>PAYLOAD_PACKAGE_EXTENSION</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-561">0x80080215</span><span class="sxs-lookup"><span data-stu-id="7b862-561">0x80080215</span></span></td>
<td><span data-ttu-id="7b862-562">Les extensions non. AppX ne sont pas autorisées pour les packages de charge utile ciblant des plateformes plus anciennes.</span><span class="sxs-lookup"><span data-stu-id="7b862-562">Non .appx extensions are not allowed for payload packages targeting older platforms.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7b862-563"><strong>APPX_E_INVALID_</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-563"><strong>APPX_E_INVALID_</strong></span></span><br/> <span data-ttu-id="7b862-564"><strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong></span><span class="sxs-lookup"><span data-stu-id="7b862-564"><strong>ENCRYPTION_EXCLUSION_FILE_LIST</strong></span></span><br/></td>
<td><span data-ttu-id="7b862-565">0x80080216</span><span class="sxs-lookup"><span data-stu-id="7b862-565">0x80080216</span></span></td>
<td><span data-ttu-id="7b862-566">Le fichier encryptionExclusionFileList n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7b862-566">The encryptionExclusionFileList file is invalid.</span></span><br/></td>
</tr>
</tbody>
</table>

## <a name="applications-dont-start-and-their-names-are-dimmed"></a><span data-ttu-id="7b862-567">Les applications ne démarrent pas et leurs noms sont estompés</span><span class="sxs-lookup"><span data-stu-id="7b862-567">Applications don't start and their names are dimmed</span></span>

<span data-ttu-id="7b862-568">Sur un ordinateur Windows 10, vous ne pouvez pas démarrer certaines applications et les noms d’application apparaissent grisés.</span><span class="sxs-lookup"><span data-stu-id="7b862-568">On a Windows 10-based computer, you cannot start some applications, and the application names appear dimmed.</span></span>

![Certains noms d’application apparaissent estompés dans le menu Démarrer](./images/app-names-dimmed.png)

<span data-ttu-id="7b862-570">Lorsque vous essayez d’ouvrir une application en sélectionnant le nom grisé, vous pouvez recevoir l’un des messages d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="7b862-570">When you try to open an application by selecting the dimmed name, you may receive one of the following error messages:</span></span>

> <span data-ttu-id="7b862-571">Il y a un problème avec \<*application name*> .</span><span class="sxs-lookup"><span data-stu-id="7b862-571">There's a problem with \<*application name*>.</span></span> <span data-ttu-id="7b862-572">Contactez votre administrateur système pour le réparer ou le réinstaller</span><span class="sxs-lookup"><span data-stu-id="7b862-572">Contact your system administrator about repairing or reinstalling it</span></span>  
> <span data-ttu-id="7b862-573">Erreur : cette application ne peut pas s’ouvrir</span><span class="sxs-lookup"><span data-stu-id="7b862-573">Error: This app can't open</span></span>

<span data-ttu-id="7b862-574">En outre, les entrées d’événements suivantes sont consignées dans le journal « Microsoft-Windows-TWinUI/Operational » sous **applications et Services\Microsoft\Windows\Apps**:</span><span class="sxs-lookup"><span data-stu-id="7b862-574">Additionally, the following event entries are logged in the "Microsoft-Windows-TWinUI/Operational" log under **Applications and Services\Microsoft\Windows\Apps**:</span></span>

> <span data-ttu-id="7b862-575">Nom du journal : Microsoft-Windows-TWinUI/Operational</span><span class="sxs-lookup"><span data-stu-id="7b862-575">Log Name: Microsoft-Windows-TWinUI/Operational</span></span>  
> <span data-ttu-id="7b862-576">Source : Microsoft-Windows-immersif-Shell</span><span class="sxs-lookup"><span data-stu-id="7b862-576">Source: Microsoft-Windows-Immersive-Shell</span></span>  
> <span data-ttu-id="7b862-577">Date : *Date* de <></span><span class="sxs-lookup"><span data-stu-id="7b862-577">Date: <*date*></span></span>  
> <span data-ttu-id="7b862-578">ID d’événement : 5960</span><span class="sxs-lookup"><span data-stu-id="7b862-578">Event ID: 5960</span></span>  
> <span data-ttu-id="7b862-579">Catégorie de tâche : (5960)</span><span class="sxs-lookup"><span data-stu-id="7b862-579">Task Category: (5960)</span></span>  
> <span data-ttu-id="7b862-580">Niveau : erreur</span><span class="sxs-lookup"><span data-stu-id="7b862-580">Level: Error</span></span>  
> <span data-ttu-id="7b862-581">Mots clés :</span><span class="sxs-lookup"><span data-stu-id="7b862-581">Keywords:</span></span>  
> <span data-ttu-id="7b862-582">Description :</span><span class="sxs-lookup"><span data-stu-id="7b862-582">Description:</span></span>  
> <span data-ttu-id="7b862-583">Activation de l’application Microsoft.BingNews_8wekyb3d8bbwe ! AppexNews pour Windows.</span><span class="sxs-lookup"><span data-stu-id="7b862-583">Activation of the app Microsoft.BingNews_8wekyb3d8bbwe!AppexNews for the Windows.</span></span> <span data-ttu-id="7b862-584">Le lancement du contrat a été bloqué avec l’erreur 0x80073CFC, car son package est dans l’État : modifié.</span><span class="sxs-lookup"><span data-stu-id="7b862-584">Launch contract was blocked with error 0x80073CFC because its package is in state: Modified.</span></span>  

### <a name="cause"></a><span data-ttu-id="7b862-585">Cause</span><span class="sxs-lookup"><span data-stu-id="7b862-585">Cause</span></span>

<span data-ttu-id="7b862-586">Ce problème se produit parce que l’entrée de Registre correspondant à la valeur d’État du package correspondant à l’application a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="7b862-586">This issue occurs because the registry entry for the status value of application's corresponding package was modified.</span></span>

### <a name="resolution"></a><span data-ttu-id="7b862-587">Résolution</span><span class="sxs-lookup"><span data-stu-id="7b862-587">Resolution</span></span>

> [!WARNING]
> <span data-ttu-id="7b862-588">Des problèmes graves peuvent survenir si vous modifiez le Registre de façon incorrecte à l’aide de l’Éditeur du Registre ou d’une autre méthode.</span><span class="sxs-lookup"><span data-stu-id="7b862-588">Serious problems might occur if you modify the registry incorrectly by using Registry Editor or by using another method.</span></span> <span data-ttu-id="7b862-589">Ces problèmes peuvent nécessiter la réinstallation du système d'exploitation.</span><span class="sxs-lookup"><span data-stu-id="7b862-589">These problems might require that you reinstall the operating system.</span></span> <span data-ttu-id="7b862-590">Microsoft ne peut pas garantir que ces problèmes puissent être résolus.</span><span class="sxs-lookup"><span data-stu-id="7b862-590">Microsoft cannot guarantee that these problems can be solved.</span></span> <span data-ttu-id="7b862-591">Toute modification du registre relève de votre propre responsabilité.</span><span class="sxs-lookup"><span data-stu-id="7b862-591">Modify the registry at your own risk.</span></span>

<span data-ttu-id="7b862-592">Pour résoudre ce problème :</span><span class="sxs-lookup"><span data-stu-id="7b862-592">To fix this issue:</span></span>

1. <span data-ttu-id="7b862-593">Démarrez l’éditeur du Registre, puis recherchez la sous-clé **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** .</span><span class="sxs-lookup"><span data-stu-id="7b862-593">Start Registry Editor, and then locate the **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList** subkey.</span></span>
2. <span data-ttu-id="7b862-594">Pour sauvegarder les données de sous-clé, cliquez avec le bouton droit sur **PackageList**, sélectionnez **Exporter**, puis enregistrez les données en tant que fichier de registre.</span><span class="sxs-lookup"><span data-stu-id="7b862-594">To back up the subkey data, right-click **PackageList**, select **Export**, and then save the data as a registry file.</span></span>
3. <span data-ttu-id="7b862-595">Pour chacune des applications répertoriées dans les entrées de journal de l’ID d’événement 5960, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7b862-595">For each of the applications that are listed in the Event ID 5960 log entries, follow these steps:</span></span>  
   1. <span data-ttu-id="7b862-596">Recherchez l’entrée **PackageStatus** .</span><span class="sxs-lookup"><span data-stu-id="7b862-596">Locate the **PackageStatus** entry.</span></span>
   2. <span data-ttu-id="7b862-597">Affectez à **PackageStatus** la valeur zéro (**0**).</span><span class="sxs-lookup"><span data-stu-id="7b862-597">Set the value of **PackageStatus** to zero (**0**).</span></span>
   > [!NOTE]  
   > <span data-ttu-id="7b862-598">S’il n’existe aucune entrée pour l’application sous **PackageList**, le problème est dû à une autre cause.</span><span class="sxs-lookup"><span data-stu-id="7b862-598">If there are no entries for the application under **PackageList**, then the issue has some other cause.</span></span> <span data-ttu-id="7b862-599">Dans le cas de l’exemple d’événement de cet article, la sous-clé complète est **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**</span><span class="sxs-lookup"><span data-stu-id="7b862-599">In the case of the example event in this article, the full subkey is **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\AppModel\StateChange\PackageList\Microsoft.BingNews_8wekyb3d8bbwe!AppexNews\PackageStatus**</span></span>
4. <span data-ttu-id="7b862-600">Redémarrez l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7b862-600">Restart the computer.</span></span>

## <a name="get-additional-help"></a><span data-ttu-id="7b862-601">Obtenir une aide supplémentaire</span><span class="sxs-lookup"><span data-stu-id="7b862-601">Get additional help</span></span>

<span data-ttu-id="7b862-602">Si vous avez besoin d’aide pour résoudre un problème que vous rencontrez lors de l’empaquetage, du déploiement ou de l’interrogation d’un package d’application Windows (. msix/. AppX) en tant que développeur, reportez-vous à ces ressources de support pour développeurs supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="7b862-602">If you need further help with resolving a problem you are experience when packaging, deploying, or querying a Windows app package (.msix/.appx) as a developer, refer to these additional developer support resources.</span></span>

- <span data-ttu-id="7b862-603">[Microsoft Q&A](/answers/topics/uwp.html?filter=all&sort=active) offre des réponses pertinentes et opportunes à vos problèmes techniques à partir d’une communauté d’experts et d’ingénieurs Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7b862-603">[Microsoft Q&A](/answers/topics/uwp.html?filter=all&sort=active) offers relevant and timely answers to your technical problems from a community of experts and Microsoft engineers.</span></span>
- <span data-ttu-id="7b862-604">Pour obtenir de l’aide auprès de la communauté sur les questions de développement, nous avons nos [Forums](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required)et [StackOverflow](https://stackoverflow.com/questions).</span><span class="sxs-lookup"><span data-stu-id="7b862-604">For community assistance with development questions, there are our [forums](https://social.msdn.microsoft.com/Forums/newthread?category=windowsapps&forum=wpdevelop&prof=required), and [StackOverflow](https://stackoverflow.com/questions).</span></span>
- <span data-ttu-id="7b862-605">Le site du [support technique](https://developer.microsoft.com/windows/support) pour les développeurs de Windows explique d’autres options de support.</span><span class="sxs-lookup"><span data-stu-id="7b862-605">The [Windows developer support](https://developer.microsoft.com/windows/support) site explains other support options.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b862-606">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7b862-606">Related topics</span></span>

- [<span data-ttu-id="7b862-607">Comment signer un package d’application à l’aide de SignTool</span><span class="sxs-lookup"><span data-stu-id="7b862-607">How to sign an app package using SignTool</span></span>](how-to-sign-a-package-using-signtool.md)
- [<span data-ttu-id="7b862-608">Comment résoudre les erreurs de signature de package d’application</span><span class="sxs-lookup"><span data-stu-id="7b862-608">How to troubleshoot app package signature errors</span></span>](how-to-troubleshoot-app-package-signature-errors.md)
