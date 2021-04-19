---
description: Le WiLstPrd.vbs de fichiers VBScript est fourni dans les composants SDK Windows pour les développeurs Windows Installer. L’exemple de script se connecte à un objet installer et énumère les produits inscrits et les informations produit.
ms.assetid: 13615dc2-ebc7-4536-9dd8-9bb1dbf3cfaf
title: Répertorier les produits, les propriétés, les fonctionnalités et les composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20d2f563efad42108f763b909e7a1118e255dcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513420"
---
# <a name="list-products-properties-features-and-components"></a><span data-ttu-id="64117-104">Répertorier les produits, les propriétés, les fonctionnalités et les composants</span><span class="sxs-lookup"><span data-stu-id="64117-104">List Products, Properties, Features, and Components</span></span>

<span data-ttu-id="64117-105">Le WiLstPrd.vbs de fichiers VBScript est fourni dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="64117-105">The VBScript file WiLstPrd.vbs is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="64117-106">L’exemple de script se connecte à un objet [**installer**](installer-object.md) et énumère les produits inscrits et les informations produit.</span><span class="sxs-lookup"><span data-stu-id="64117-106">The sample script connects to an [**Installer**](installer-object.md) object and enumerates registered products and product information.</span></span>

<span data-ttu-id="64117-107">Cet exemple illustre l’utilisation de :</span><span class="sxs-lookup"><span data-stu-id="64117-107">This sample demonstrates the use of:</span></span>

-   [<span data-ttu-id="64117-108">**Propriété ProductInfo**</span><span class="sxs-lookup"><span data-stu-id="64117-108">**ProductInfo property**</span></span>](installer-productinfo.md)
-   [<span data-ttu-id="64117-109">**Propriété ProductState (objet installer)**</span><span class="sxs-lookup"><span data-stu-id="64117-109">**ProductState property (Installer object)**</span></span>](installer-productstate-property.md)
-   [<span data-ttu-id="64117-110">**Products, propriété**</span><span class="sxs-lookup"><span data-stu-id="64117-110">**Products property**</span></span>](installer-products.md)
-   [<span data-ttu-id="64117-111">**Fonctionnalités, propriété**</span><span class="sxs-lookup"><span data-stu-id="64117-111">**Features property**</span></span>](installer-features.md)
-   [<span data-ttu-id="64117-112">**Propriété FeatureParent**</span><span class="sxs-lookup"><span data-stu-id="64117-112">**FeatureParent property**</span></span>](installer-featureparent.md)
-   [<span data-ttu-id="64117-113">**Propriété FeatureState**</span><span class="sxs-lookup"><span data-stu-id="64117-113">**FeatureState property**</span></span>](installer-featurestate.md)
-   [<span data-ttu-id="64117-114">**Components, propriété**</span><span class="sxs-lookup"><span data-stu-id="64117-114">**Components property**</span></span>](installer-components.md)
-   [<span data-ttu-id="64117-115">**Propriété ComponentClients**</span><span class="sxs-lookup"><span data-stu-id="64117-115">**ComponentClients property**</span></span>](installer-componentclients.md)
-   [<span data-ttu-id="64117-116">**Propriété ComponentPath**</span><span class="sxs-lookup"><span data-stu-id="64117-116">**ComponentPath property**</span></span>](installer-componentpath.md)
-   [<span data-ttu-id="64117-117">**Méthode LastErrorRecord**</span><span class="sxs-lookup"><span data-stu-id="64117-117">**LastErrorRecord method**</span></span>](installer-lasterrorrecord.md)
-   <span data-ttu-id="64117-118">[**Méthode RegistryValue**](installer-registryvalue.md) de l' [ **objet installer**](installer-object.md)</span><span class="sxs-lookup"><span data-stu-id="64117-118">[**RegistryValue method**](installer-registryvalue.md) of the [**Installer object**](installer-object.md)</span></span>

<span data-ttu-id="64117-119">Vous aurez besoin de la version CScript.exe ou WScript.exe de Windows Script Host pour utiliser cet exemple.</span><span class="sxs-lookup"><span data-stu-id="64117-119">You'll require the CScript.exe or WScript.exe version of Windows Script Host to use this sample.</span></span> <span data-ttu-id="64117-120">Pour utiliser CScript.exe pour exécuter cet exemple, tapez une ligne de commande à l’invite de commandes en utilisant la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="64117-120">To use CScript.exe to run this sample, type a command line at the command prompt using the following syntax.</span></span> <span data-ttu-id="64117-121">L’aide s’affiche si le premier argument est/ ?</span><span class="sxs-lookup"><span data-stu-id="64117-121">Help is displayed if the first argument is /?</span></span> <span data-ttu-id="64117-122">ou si le nombre d’arguments spécifié est insuffisant.</span><span class="sxs-lookup"><span data-stu-id="64117-122">or if too few arguments are specified.</span></span> <span data-ttu-id="64117-123">Pour rediriger la sortie vers un fichier, terminez la ligne de commande avec VBS > \[ chemin d’accès au fichier \] .</span><span class="sxs-lookup"><span data-stu-id="64117-123">To redirect the output to a file, end the command line with VBS > \[path to file\].</span></span> <span data-ttu-id="64117-124">L’exemple retourne la valeur 0 pour Success, 1 si l’aide est appelée, et 2 si le script échoue.</span><span class="sxs-lookup"><span data-stu-id="64117-124">The sample returns a value of 0 for success, 1 if help is invoked, and 2 if the script fails.</span></span>

<span data-ttu-id="64117-125">**cscript WiLstPrd.vbs \[ options de nom de produit \] \[\]**</span><span class="sxs-lookup"><span data-stu-id="64117-125">**cscript WiLstPrd.vbs \[Product Name\] \[options\]**</span></span>

<span data-ttu-id="64117-126">Spécifiez le nom du produit non sensible à la casse ou le GUID de l’ID de produit du produit installé ou publié.</span><span class="sxs-lookup"><span data-stu-id="64117-126">Specify the case-insensitive product name or the product ID GUID of the installed or advertised product.</span></span> <span data-ttu-id="64117-127">Si aucun produit ou option n’est spécifié, le programme d’installation répertorie tous les produits installés ou publiés sur le système.</span><span class="sxs-lookup"><span data-stu-id="64117-127">If no product or options are specified, the installer lists all the products installed or advertised on the system.</span></span>

<span data-ttu-id="64117-128">Notez que ces options ne sont pas des commutateurs. par conséquent, vous ne devez pas les faire précéder d’une barre oblique (/) sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="64117-128">Note that these options are not switches so you should not prefix them with a slash (/) on the commandline.</span></span> <span data-ttu-id="64117-129">Les options suivantes peuvent être combinées en concaténant les lettres.</span><span class="sxs-lookup"><span data-stu-id="64117-129">The following options may be combined by concatenating the letters.</span></span> <span data-ttu-id="64117-130">Par exemple, « PC » pour répertorier les propriétés des produits et les composants installés.</span><span class="sxs-lookup"><span data-stu-id="64117-130">For example, "pc" to list both the products' properties and installed components.</span></span>



| <span data-ttu-id="64117-131">Option</span><span class="sxs-lookup"><span data-stu-id="64117-131">Option</span></span>               | <span data-ttu-id="64117-132">Description</span><span class="sxs-lookup"><span data-stu-id="64117-132">Description</span></span>                                                                                                                           |
|----------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64117-133">aucune option spécifiée</span><span class="sxs-lookup"><span data-stu-id="64117-133">no options specified</span></span> | <span data-ttu-id="64117-134">Répertorie les propriétés des produits.</span><span class="sxs-lookup"><span data-stu-id="64117-134">List the products' properties.</span></span>                                                                                                        |
| <span data-ttu-id="64117-135">p</span><span class="sxs-lookup"><span data-stu-id="64117-135">p</span></span>                    | <span data-ttu-id="64117-136">Répertorie les propriétés des produits.</span><span class="sxs-lookup"><span data-stu-id="64117-136">List the products' properties.</span></span>                                                                                                        |
| <span data-ttu-id="64117-137">f</span><span class="sxs-lookup"><span data-stu-id="64117-137">f</span></span>                    | <span data-ttu-id="64117-138">Répertorier les fonctionnalités, les parents des fonctionnalités et les États d’installation des produits</span><span class="sxs-lookup"><span data-stu-id="64117-138">List the products' features, feature parents, and installation states</span></span>                                                                 |
| <span data-ttu-id="64117-139">c</span><span class="sxs-lookup"><span data-stu-id="64117-139">c</span></span>                    | <span data-ttu-id="64117-140">Répertorie les composants installés du produit.</span><span class="sxs-lookup"><span data-stu-id="64117-140">List the products' installed components.</span></span>                                                                                              |
| <span data-ttu-id="64117-141">d</span><span class="sxs-lookup"><span data-stu-id="64117-141">d</span></span>                    | <span data-ttu-id="64117-142">Répertoriez la valeur sous **HKLM \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ SharedDlls** pour les fichiers de clé du composant Products.</span><span class="sxs-lookup"><span data-stu-id="64117-142">List the value under **HKLM\\Software\\Microsoft\\Windows\\CurrentVersion\\SharedDlls** for the key files of the products' component.</span></span> |



 

<span data-ttu-id="64117-143">Pour plus d’informations, consultez [Windows Installer des exemples de scripts](windows-installer-scripting-examples.md) pour des exemples de scripts supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="64117-143">For more information, see [Windows Installer Scripting Examples](windows-installer-scripting-examples.md) for additional scripting examples.</span></span> <span data-ttu-id="64117-144">Pour obtenir des exemples d’utilitaires qui ne nécessitent pas Windows Script Host, consultez [Windows Installer les outils de développement](windows-installer-development-tools.md).</span><span class="sxs-lookup"><span data-stu-id="64117-144">For sample utilities that do not require Windows Script Host, see [Windows Installer Development Tools](windows-installer-development-tools.md).</span></span>

 

 



