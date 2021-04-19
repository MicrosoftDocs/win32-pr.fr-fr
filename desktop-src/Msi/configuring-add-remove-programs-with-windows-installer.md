---
description: Vous pouvez fournir toutes les informations nécessaires pour configurer ajout/suppression de programmes dans le panneau de configuration en définissant les valeurs de certaines propriétés du programme d’installation dans le package Windows Installer de votre application.
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: Configuration de l’ajout/suppression de programmes avec Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6850163e18af94aa9cceaf6c4bb2e8059dcf2121
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/30/2021
ms.locfileid: "106531174"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a><span data-ttu-id="daf39-103">Configuration de l’ajout/suppression de programmes avec Windows Installer</span><span class="sxs-lookup"><span data-stu-id="daf39-103">Configuring Add/Remove Programs with Windows Installer</span></span>

<span data-ttu-id="daf39-104">Vous pouvez fournir toutes les informations nécessaires pour configurer ajout/suppression de programmes dans le panneau de configuration en définissant les valeurs de certaines propriétés du programme d’installation dans le package Windows Installer de votre application.</span><span class="sxs-lookup"><span data-stu-id="daf39-104">You can supply all of the information needed to configure Add/Remove Programs in Control Panel by setting the values of certain installer properties in your application's Windows Installer package.</span></span> <span data-ttu-id="daf39-105">La définition de ces propriétés écrit automatiquement les valeurs correspondantes dans le registre.</span><span class="sxs-lookup"><span data-stu-id="daf39-105">Setting these properties automatically writes the corresponding values into the registry.</span></span> <span data-ttu-id="daf39-106">Si le programme d’installation détecte que le produit est marqué pour une suppression complète, les opérations sont automatiquement ajoutées au script pour supprimer le dossier ajout/suppression de programmes dans les informations du panneau de configuration du produit.</span><span class="sxs-lookup"><span data-stu-id="daf39-106">If the installer detects that the product is marked for complete removal, operations are automatically added to the script to remove the Add/Remove Programs folder in Control Panel information for the product.</span></span>

<span data-ttu-id="daf39-107">Si une application n’est pas inscrite, elle n’est pas répertoriée dans Ajout/suppression de programmes dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="daf39-107">If an application is not registered, it is not listed in Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="daf39-108">Pour plus d’informations, consultez [Ajout et suppression d’une application et conservation d’aucune trace dans le registre](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).</span><span class="sxs-lookup"><span data-stu-id="daf39-108">For more information, see [Adding and Removing an Application and Leaving No Trace in the Registry](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md).</span></span>

<span data-ttu-id="daf39-109">Les applications qui ont été installées dans le [contexte d’installation](installation-context.md) par utilisateur s’affichent dans Ajout/suppression de programmes de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="daf39-109">Applications that have been installed in the per-user [installation context](installation-context.md) are displayed in the Add/Remove Programs of the current user.</span></span> <span data-ttu-id="daf39-110">Les applications qui ont été installées dans le contexte d’installation par ordinateur sont affichées dans Ajout/suppression de programmes de tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="daf39-110">Applications that have been installed in the per-machine installation context are displayed in the Add/Remove Programs of all users.</span></span> <span data-ttu-id="daf39-111">Les applications qui n’ont pas été installées par ordinateur et qui n’ont été installées qu’en tant qu’applications par utilisateur pour les utilisateurs autres que l’utilisateur actuel, n’apparaissent pas dans Ajout/suppression de programmes de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="daf39-111">Applications that have not been installed per-machine, and have only been installed as per-user applications for users other than the current user, do not appear in the Add/Remove Programs of the current user.</span></span>

<span data-ttu-id="daf39-112">Notez que les packages d’installation qui utilisent la propriété [**LIMITUI**](limitui.md) doivent également contenir [**ARPNOMODIFY**](arpnomodify.md).</span><span class="sxs-lookup"><span data-stu-id="daf39-112">Note that installation packages that use the [**LIMITUI**](limitui.md) property must also contain the [**ARPNOMODIFY**](arpnomodify.md).</span></span> <span data-ttu-id="daf39-113">Cela est nécessaire pour qu’un utilisateur obtienne le comportement correct à partir de l’utilitaire ajout/suppression de programmes dans le panneau de configuration lors de la tentative de configuration d’un produit.</span><span class="sxs-lookup"><span data-stu-id="daf39-113">This is required for a user to obtain the correct behavior from Add/Remove Programs in Control Panel utility when attempting to configure a product.</span></span>

<span data-ttu-id="daf39-114">Le programme d’installation utilise les [propriétés publiques](public-properties.md) suivantes pour gérer ajout/suppression de programmes dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="daf39-114">The installer uses the following [public properties](public-properties.md) to manage Add/Remove Programs in Control Panel.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="daf39-115">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="daf39-115">Property name</span></span></th>
<th><span data-ttu-id="daf39-116">Brève description de la propriété</span><span class="sxs-lookup"><span data-stu-id="daf39-116">Brief description of property</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="daf39-117"><a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a></span><span class="sxs-lookup"><span data-stu-id="daf39-117"><a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a></span></span></td>
<td><span data-ttu-id="daf39-118">URL du canal de mise à jour pour l’application.</span><span class="sxs-lookup"><span data-stu-id="daf39-118">URL of the update channel for the application.</span></span> <span data-ttu-id="daf39-119">Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>.</span><span class="sxs-lookup"><span data-stu-id="daf39-119">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="daf39-120"><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></span><span class="sxs-lookup"><span data-stu-id="daf39-120"><a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a></span></span></td>
<td><span data-ttu-id="daf39-121">Fournit des commentaires pour l’ajout/suppression de programmes dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="daf39-121">Provides Comments for the Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="daf39-122">Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>.</span><span class="sxs-lookup"><span data-stu-id="daf39-122">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="daf39-123"><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></span><span class="sxs-lookup"><span data-stu-id="daf39-123"><a href="arpcontact.md"><strong>ARPCONTACT</strong></a></span></span></td>
<td><span data-ttu-id="daf39-124">Fournit le contact pour ajout/suppression de programmes dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="daf39-124">Provides the Contact for Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="daf39-125">Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>.</span><span class="sxs-lookup"><span data-stu-id="daf39-125">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="daf39-126"><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></span><span class="sxs-lookup"><span data-stu-id="daf39-126"><a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a></span></span></td>
<td><span data-ttu-id="daf39-127">Chemin d’accès complet au dossier principal de l’application.</span><span class="sxs-lookup"><span data-stu-id="daf39-127">Fully qualified path to the application's primary folder.</span></span> <span data-ttu-id="daf39-128">Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>.</span><span class="sxs-lookup"><span data-stu-id="daf39-128">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="daf39-129"><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></span><span class="sxs-lookup"><span data-stu-id="daf39-129"><a href="arphelplink.md"><strong>ARPHELPLINK</strong></a></span></span></td>
<td><span data-ttu-id="daf39-130">Adresse Internet, ou URL, pour le support technique.</span><span class="sxs-lookup"><span data-stu-id="daf39-130">Internet address, or URL, for technical support.</span></span> <span data-ttu-id="daf39-131">Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>.</span><span class="sxs-lookup"><span data-stu-id="daf39-131">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="daf39-132"><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></span><span class="sxs-lookup"><span data-stu-id="daf39-132"><a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a></span></span></td>
<td><span data-ttu-id="daf39-133">Numéros de téléphone du support technique.</span><span class="sxs-lookup"><span data-stu-id="daf39-133">Technical support phone numbers.</span></span> <span data-ttu-id="daf39-134">Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>.</span><span class="sxs-lookup"><span data-stu-id="daf39-134">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="daf39-135"><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></span><span class="sxs-lookup"><span data-stu-id="daf39-135"><a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a></span></span></td>
<td><span data-ttu-id="daf39-136">Empêche l’affichage d’un bouton modifier pour le produit dans Ajout/suppression de programmes dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="daf39-136">Prevents display of a Change button for the product in Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="daf39-137">
<b>Remarque :</b> Cela affecte uniquement l’affichage dans le protocole ARP.</span><span class="sxs-lookup"><span data-stu-id="daf39-137">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="daf39-138">La Windows Installer peut toujours réparer, installer à la demande et désinstaller des applications via une ligne de commande ou l’interface de programmation.</span><span class="sxs-lookup"><span data-stu-id="daf39-138">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="daf39-139"><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></span><span class="sxs-lookup"><span data-stu-id="daf39-139"><a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a></span></span></td>
<td><span data-ttu-id="daf39-140">Empêche l’affichage d’un bouton Supprimer pour le produit dans Ajout/suppression de programmes dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="daf39-140">Prevents display of a Remove button for the product in the Add/Remove Programs in the Control Panel.</span></span> <span data-ttu-id="daf39-141">Le produit peut toujours être supprimé en sélectionnant le bouton modifier si le package d’installation a été créé avec une interface utilisateur qui permet de supprimer le produit en tant qu’option.</span><span class="sxs-lookup"><span data-stu-id="daf39-141">The product can still be removed by selecting the Change button if the installation package has been authored with a user interface that provides product removal as an option.</span></span>
<blockquote><span data-ttu-id="daf39-142">
<b>Remarque :</b> Cela affecte uniquement l’affichage dans le protocole ARP.</span><span class="sxs-lookup"><span data-stu-id="daf39-142">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="daf39-143">La Windows Installer peut toujours réparer, installer à la demande et désinstaller des applications via une ligne de commande ou l’interface de programmation.</span><span class="sxs-lookup"><span data-stu-id="daf39-143">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="daf39-144"><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></span><span class="sxs-lookup"><span data-stu-id="daf39-144"><a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a></span></span></td>
<td><span data-ttu-id="daf39-145">Désactive le bouton réparer dans Ajout/suppression de programmes dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="daf39-145">Disables the Repair button in the Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="daf39-146">
<b>Remarque :</b> Cela affecte uniquement l’affichage dans le protocole ARP.</span><span class="sxs-lookup"><span data-stu-id="daf39-146">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="daf39-147">La Windows Installer peut toujours réparer, installer à la demande et désinstaller des applications via une ligne de commande ou l’interface de programmation.</span><span class="sxs-lookup"><span data-stu-id="daf39-147">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="daf39-148"><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></span><span class="sxs-lookup"><span data-stu-id="daf39-148"><a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a></span></span></td>
<td><span data-ttu-id="daf39-149">Identifie l’icône affichée dans Ajout/suppression de programmes.</span><span class="sxs-lookup"><span data-stu-id="daf39-149">Identifies the icon displayed in Add/Remove Programs.</span></span> <span data-ttu-id="daf39-150">Si cette propriété n’est pas définie, ajout/suppression de programmes spécifie l’icône d’affichage.</span><span class="sxs-lookup"><span data-stu-id="daf39-150">If this property is not defined, Add/Remove Programs specifies the display icon.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="daf39-151"><a href="arpreadme.md"><strong>ARPREADME</strong></a></span><span class="sxs-lookup"><span data-stu-id="daf39-151"><a href="arpreadme.md"><strong>ARPREADME</strong></a></span></span></td>
<td><span data-ttu-id="daf39-152">Contient le fichier Lisez-moi pour ajout/suppression de programmes dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="daf39-152">Provides the ReadMe for Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="daf39-153">Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>.</span><span class="sxs-lookup"><span data-stu-id="daf39-153">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="daf39-154"><a href="arpsize.md"><strong>ARPSIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="daf39-154"><a href="arpsize.md"><strong>ARPSIZE</strong></a></span></span></td>
<td><span data-ttu-id="daf39-155">Estimation de la taille de l’application en Ko.</span><span class="sxs-lookup"><span data-stu-id="daf39-155">Estimated size of the application in KB.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="daf39-156"><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="daf39-156"><a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="daf39-157">Empêche l’affichage de l’application dans la liste des programmes du panneau de configuration Ajout/suppression de programmes.</span><span class="sxs-lookup"><span data-stu-id="daf39-157">Prevents display of the application in the Programs List of the Add/Remove Programs in the Control Panel.</span></span>
<blockquote><span data-ttu-id="daf39-158">
<b>Remarque :</b> Cela affecte uniquement l’affichage dans le protocole ARP.</span><span class="sxs-lookup"><span data-stu-id="daf39-158">
<b>Note:</b> This only affects the display in the ARP.</span></span> <span data-ttu-id="daf39-159">La Windows Installer peut toujours réparer, installer à la demande et désinstaller des applications via une ligne de commande ou l’interface de programmation.</span><span class="sxs-lookup"><span data-stu-id="daf39-159">The Windows Installer is still capable of repairing, installing-on-demand, and uninstalling applications through a command line or the programming interface.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="daf39-160"><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></span><span class="sxs-lookup"><span data-stu-id="daf39-160"><a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a></span></span></td>
<td><span data-ttu-id="daf39-161">URL de la page d’hébergement de l’application.</span><span class="sxs-lookup"><span data-stu-id="daf39-161">URL for application's home page.</span></span> <span data-ttu-id="daf39-162">Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>.</span><span class="sxs-lookup"><span data-stu-id="daf39-162">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="daf39-163"><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="daf39-163"><a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a></span></span></td>
<td><span data-ttu-id="daf39-164">URL pour les informations de mise à jour d’application.</span><span class="sxs-lookup"><span data-stu-id="daf39-164">URL for application update information.</span></span> <span data-ttu-id="daf39-165">Valeur que le programme d’installation écrit sous la <a href="uninstall-registry-key.md">clé de Registre Uninstall</a>.</span><span class="sxs-lookup"><span data-stu-id="daf39-165">The value the installer writes under the <a href="uninstall-registry-key.md">Uninstall Registry Key</a>.</span></span></td>
</tr>
</tbody>
</table>

> [!Note]  
> <span data-ttu-id="daf39-166">Pour plus d’informations sur l’outil définir le programme et les valeurs par défaut, reportez-vous à la section [utilisation des paramètres par défaut de l’accès aux programmes et](/previous-versions//bb776877(v=vs.85))de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="daf39-166">For information regarding the Set Program and Defaults tool, refer to the section [Working with Set Program Access and Computer Defaults](/previous-versions//bb776877(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="daf39-167">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="daf39-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="daf39-168">Désinstaller la clé de Registre</span><span class="sxs-lookup"><span data-stu-id="daf39-168">Uninstall Registry Key</span></span>](uninstall-registry-key.md)
</dt> </dl>
