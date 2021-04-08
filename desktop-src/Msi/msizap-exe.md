---
description: Msizap.exe est un utilitaire de ligne de commande qui supprime toutes les informations Windows Installer d’un produit ou de tous les produits installés sur un ordinateur. Les produits installés par le programme d’installation peuvent ne pas fonctionner après l’utilisation de Msizap.
ms.assetid: 0debb8ab-3ae7-447e-84fc-0466ec1b2f26
title: Msizap.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a89f2287443bc442ee767b01e975d6bcc118c1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034324"
---
# <a name="msizapexe"></a><span data-ttu-id="2c200-104">Msizap.exe</span><span class="sxs-lookup"><span data-stu-id="2c200-104">Msizap.exe</span></span>

<span data-ttu-id="2c200-105">Msizap.exe est un utilitaire de ligne de commande qui supprime toutes les informations Windows Installer d’un produit ou de tous les produits installés sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2c200-105">Msizap.exe is a command line utility that removes either all Windows Installer information for a product or all products installed on a computer.</span></span> <span data-ttu-id="2c200-106">Les produits installés par le programme d’installation peuvent ne pas fonctionner après l’utilisation de Msizap.</span><span class="sxs-lookup"><span data-stu-id="2c200-106">Products installed by the installer may fail to function after using Msizap.</span></span>

<span data-ttu-id="2c200-107">Sur Windows 2000 et Windows XP, des privilèges d’administrateur sont nécessaires pour utiliser Msizap.exe.</span><span class="sxs-lookup"><span data-stu-id="2c200-107">On Windows 2000 and Windows XP, administrative privileges are required to use Msizap.exe.</span></span>

<span data-ttu-id="2c200-108">Cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md) et ne doit pas être redistribué.</span><span class="sxs-lookup"><span data-stu-id="2c200-108">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) and should not be redistributed.</span></span> <span data-ttu-id="2c200-109">Utilisez la version récente de Msizap.exe (version 3.1.4000.2726 ou ultérieure) qui est disponible dans les composants SDK Windows pour les développeurs Windows Installer pour Windows Vista ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="2c200-109">Use the recent version of Msizap.exe (version 3.1.4000.2726 or greater) that is available in the Windows SDK Components for Windows Installer Developers for Windows Vista or greater.</span></span> <span data-ttu-id="2c200-110">Les versions plus petites de Msizap.exe peuvent supprimer des informations sur toutes les mises à jour qui ont été appliquées à d’autres applications sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2c200-110">Lesser versions of Msizap.exe can remove information about all updates that have been applied to other applications on the user's computer.</span></span> <span data-ttu-id="2c200-111">Si ces informations sont supprimées, ces autres applications devront peut-être être supprimées et réinstallées pour recevoir des mises à jour supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="2c200-111">If this information is removed, these other applications may need to be removed and reinstalled to receive additional updates.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c200-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c200-112">Syntax</span></span>

<span data-ttu-id="2c200-113">**Msizap T**_\[ wa ! \] {code produit}_</span><span class="sxs-lookup"><span data-stu-id="2c200-113">**msizap T**_\[WA!\]{product code}_</span></span>

<span data-ttu-id="2c200-114">**Msizap T**_\[ wa ! \] <msi package>_</span><span class="sxs-lookup"><span data-stu-id="2c200-114">**msizap T**_\[WA!\]<msi package>_</span></span>

<span data-ttu-id="2c200-115">\**\* \*\*\* Msizap \[ WA ! \]* **ALLPRODUCTS**</span><span class="sxs-lookup"><span data-stu-id="2c200-115">\**msizap \*\*\*\*\[WA!\]* **ALLPRODUCTS**</span></span>

<span data-ttu-id="2c200-116">**Msizap PWSA ?!**</span><span class="sxs-lookup"><span data-stu-id="2c200-116">**msizap PWSA?!**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="2c200-117">Options de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="2c200-117">Command Line Options</span></span>

<span data-ttu-id="2c200-118">Msizap.exe utilise les options de ligne de commande qui ne respectent pas la casse présentées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2c200-118">Msizap.exe uses case-insensitive command line options shown in the following table.</span></span>



| <span data-ttu-id="2c200-119">Option</span><span class="sxs-lookup"><span data-stu-id="2c200-119">Option</span></span> | <span data-ttu-id="2c200-120">Description</span><span class="sxs-lookup"><span data-stu-id="2c200-120">Description</span></span>                                                                                                                                                                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*     | <span data-ttu-id="2c200-121">Supprime tous les dossiers et clés de Registre Windows Installer, ajuste les nombres de DLL partagées et arrête Windows Installer service.</span><span class="sxs-lookup"><span data-stu-id="2c200-121">Removes all Windows Installer folders and registry keys, adjusts shared DLL counts, and stops Windows Installer service.</span></span> <span data-ttu-id="2c200-122">Supprime également les informations de clé In-Progress et de restauration.</span><span class="sxs-lookup"><span data-stu-id="2c200-122">Also removes the In-Progress key and rollback information.</span></span>                                                                           |
| <span data-ttu-id="2c200-123">a</span><span class="sxs-lookup"><span data-stu-id="2c200-123">a</span></span>      | <span data-ttu-id="2c200-124">Modifie uniquement les ACL pour le contrôle total de l’administrateur pour une suppression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2c200-124">Only changes ACLs to Admin Full Control for any specified removal.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="2c200-125">g</span><span class="sxs-lookup"><span data-stu-id="2c200-125">g</span></span>      | <span data-ttu-id="2c200-126">Pour tous les utilisateurs, supprime tous les fichiers de données Windows Installers mis en cache qui ont été orphelins.</span><span class="sxs-lookup"><span data-stu-id="2c200-126">For all users, removes any cached Windows Installer data files that have been orphaned.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="2c200-127">p</span><span class="sxs-lookup"><span data-stu-id="2c200-127">p</span></span>      | <span data-ttu-id="2c200-128">Supprime la clé de In-Progress.</span><span class="sxs-lookup"><span data-stu-id="2c200-128">Removes the In-Progress key.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="2c200-129">s</span><span class="sxs-lookup"><span data-stu-id="2c200-129">s</span></span>      | <span data-ttu-id="2c200-130">Supprime les informations de restauration.</span><span class="sxs-lookup"><span data-stu-id="2c200-130">Removes Rollback Information.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="2c200-131">t</span><span class="sxs-lookup"><span data-stu-id="2c200-131">t</span></span>      | <span data-ttu-id="2c200-132">Supprime toutes les informations pour le code de produit spécifié.</span><span class="sxs-lookup"><span data-stu-id="2c200-132">Removes all information for the specified product code.</span></span> <span data-ttu-id="2c200-133">Lorsque vous utilisez cette option, mettez le code du produit entre accolades.</span><span class="sxs-lookup"><span data-stu-id="2c200-133">When using this option, enclose the Product Code in curly braces.</span></span> <span data-ttu-id="2c200-134">Cette option peut être utilisée avec le chemin d’accès complet au fichier. msi ou avec le code du produit.</span><span class="sxs-lookup"><span data-stu-id="2c200-134">This option may be used with either the full path to the .msi file or with the product code.</span></span>                                        |
| <span data-ttu-id="2c200-135">w</span><span class="sxs-lookup"><span data-stu-id="2c200-135">w</span></span>      | <span data-ttu-id="2c200-136">Supprime Windows Installer informations pour tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="2c200-136">Removes Windows Installer information for all users.</span></span> <span data-ttu-id="2c200-137">Lorsque cette option n’est pas définie, seules les informations de l’utilisateur actuel sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="2c200-137">When this option is not set, only the information for the current user is removed.</span></span> <span data-ttu-id="2c200-138">L’utilisation de cette option nécessite le chargement du profil de l’utilisateur afin que la ruche du Registre par utilisateur soit disponible.</span><span class="sxs-lookup"><span data-stu-id="2c200-138">Use of this option requires that the user's profile be loaded so that the user's per-user registry hive be available.</span></span> |
| <span data-ttu-id="2c200-139">?</span><span class="sxs-lookup"><span data-stu-id="2c200-139">?</span></span>      | <span data-ttu-id="2c200-140">Aide détaillée.</span><span class="sxs-lookup"><span data-stu-id="2c200-140">Verbose help.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="2c200-141">!</span><span class="sxs-lookup"><span data-stu-id="2c200-141">!</span></span>      | <span data-ttu-id="2c200-142">Force une réponse « oui » à une invite.</span><span class="sxs-lookup"><span data-stu-id="2c200-142">Forces a 'yes' response to any prompt.</span></span>                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="2c200-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c200-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c200-144">Versions, outils et redistribuables publiés</span><span class="sxs-lookup"><span data-stu-id="2c200-144">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



