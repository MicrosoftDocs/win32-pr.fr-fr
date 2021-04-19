---
description: Pour un package d’installation, la propriété Résumé du modèle indique les versions de la plateforme et de la langue qui sont compatibles avec cette base de données d’installation.
ms.assetid: a1015ddb-8d5c-40f7-97ac-4a1347644ae6
title: Propriété Résumé du modèle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b3949e7028fd0b1b5f9ff3112f1a3d03c9b87e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545405"
---
# <a name="template-summary-property"></a><span data-ttu-id="73ffc-103">Propriété Résumé du modèle</span><span class="sxs-lookup"><span data-stu-id="73ffc-103">Template Summary property</span></span>

<span data-ttu-id="73ffc-104">Pour un package d’installation, la propriété **Résumé du modèle** indique les versions de la plateforme et de la langue qui sont compatibles avec cette base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="73ffc-104">For an installation package, the **Template Summary** property indicates the platform and language versions that are compatible with this installation database.</span></span> <span data-ttu-id="73ffc-105">La syntaxe des informations de propriétés de **Résumé du modèle** pour une base de données d’installation est la suivante :</span><span class="sxs-lookup"><span data-stu-id="73ffc-105">The syntax of the **Template Summary** property information for an installation database is the following:</span></span>

<span data-ttu-id="73ffc-106">\[*propriété de la plateforme* \] ; \[ *ID* \] \[ de langue,*ID de langue* \] \[ ,... \] .</span><span class="sxs-lookup"><span data-stu-id="73ffc-106">\[*platform property*\];\[*language id*\]\[,*language id*\]\[,...\].</span></span>

<span data-ttu-id="73ffc-107">Les exemples suivants sont des valeurs valides pour la propriété **Résumé du modèle** :</span><span class="sxs-lookup"><span data-stu-id="73ffc-107">The following examples are valid values for the **Template Summary** property:</span></span>

-   <span data-ttu-id="73ffc-108">x64 ; 1033</span><span class="sxs-lookup"><span data-stu-id="73ffc-108">x64;1033</span></span>
-   <span data-ttu-id="73ffc-109">Intel ; 1033</span><span class="sxs-lookup"><span data-stu-id="73ffc-109">Intel;1033</span></span>
-   <span data-ttu-id="73ffc-110">Intel64 ; 1033</span><span class="sxs-lookup"><span data-stu-id="73ffc-110">Intel64;1033</span></span>
-   <span data-ttu-id="73ffc-111">; 1033</span><span class="sxs-lookup"><span data-stu-id="73ffc-111">;1033</span></span>
-   <span data-ttu-id="73ffc-112">Intel ; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="73ffc-112">Intel ;1033,2046</span></span>
-   <span data-ttu-id="73ffc-113">Intel64 ; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="73ffc-113">Intel64;1033,2046</span></span>
-   <span data-ttu-id="73ffc-114">Intel ; 0</span><span class="sxs-lookup"><span data-stu-id="73ffc-114">Intel;0</span></span>
-   <span data-ttu-id="73ffc-115">ARM ; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="73ffc-115">Arm;1033,2046</span></span>
-   <span data-ttu-id="73ffc-116">Arm ; 0</span><span class="sxs-lookup"><span data-stu-id="73ffc-116">Arm;0</span></span>
-   <span data-ttu-id="73ffc-117">Arm64 ; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="73ffc-117">Arm64;1033,2046</span></span>
-   <span data-ttu-id="73ffc-118">Arm64 ; 0</span><span class="sxs-lookup"><span data-stu-id="73ffc-118">Arm64;0</span></span>

<span data-ttu-id="73ffc-119">La propriété **Résumé du modèle** d’une transformation indique les versions de la plateforme et de la langue compatibles avec la transformation.</span><span class="sxs-lookup"><span data-stu-id="73ffc-119">The **Template Summary** property of a transform indicates the platform and language versions compatible with the transform.</span></span> <span data-ttu-id="73ffc-120">Dans un fichier de transformation, une seule langue peut être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="73ffc-120">In a transform file, only one language may be specified.</span></span> <span data-ttu-id="73ffc-121">La plateforme et le langage spécifiés déterminent si une transformation peut être appliquée à une base de données particulière.</span><span class="sxs-lookup"><span data-stu-id="73ffc-121">The specified platform and language determine whether a transform can be applied to a particular database.</span></span> <span data-ttu-id="73ffc-122">La propriété de la plateforme et la propriété Language peuvent être laissées vides si aucune restriction de transformation ne s’appuie sur ces dernières pour valider la transformation.</span><span class="sxs-lookup"><span data-stu-id="73ffc-122">The platform property and the language property can be left blank if no transform restriction relies on them to validate the transform.</span></span>

<span data-ttu-id="73ffc-123">La propriété **Résumé du modèle** d’un package correctif est une liste délimitée par des points-virgules des codes de produit pouvant accepter le correctif.</span><span class="sxs-lookup"><span data-stu-id="73ffc-123">The **Template Summary** property of a patch package is a semicolon-delimited list of the product codes that can accept the patch.</span></span> <span data-ttu-id="73ffc-124">Si vous utilisez [Msimsp.exe](msimsp-exe.md) et [Patchwiz.dll](patchwiz-dll.md) pour générer le package de correctifs, cette liste est obtenue à partir de la [table TargetImages](targetimages-table-patchwiz-dll-.md) du fichier de création de correctif.</span><span class="sxs-lookup"><span data-stu-id="73ffc-124">If you use [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) to generate the patch package, this list is obtained from the [TargetImages table](targetimages-table-patchwiz-dll-.md) of the patch creation file.</span></span>

<span data-ttu-id="73ffc-125">Cette propriété de résumé est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="73ffc-125">This summary property is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="73ffc-126">Notes</span><span class="sxs-lookup"><span data-stu-id="73ffc-126">Remarks</span></span>

<span data-ttu-id="73ffc-127">Si la plateforme actuelle ne correspond pas à l’une des plateformes spécifiées dans la propriété **Résumé du modèle** , le programme d’installation ne traite pas le package.</span><span class="sxs-lookup"><span data-stu-id="73ffc-127">If the current platform does not match one of the platforms specified in the **Template Summary** property then the installer does not process the package.</span></span>

<span data-ttu-id="73ffc-128">Si la spécification de la plateforme est manquante dans la valeur de la propriété **Résumé du modèle** , le programme d’installation suppose l’architecture Intel.</span><span class="sxs-lookup"><span data-stu-id="73ffc-128">If the platform specification is missing in the **Template Summary** property value, the installer assumes the Intel architecture.</span></span>

<span data-ttu-id="73ffc-129">S’il s’agit d’un package de Windows Installer 64 bits exécuté sur une plate-forme Intel64 (Itanium), entrez Intel64 dans la propriété **Résumé du modèle** .</span><span class="sxs-lookup"><span data-stu-id="73ffc-129">If this is a 64-bit Windows Installer package being run on an Intel64 (Itanium) platform, enter Intel64 in the **Template Summary** property.</span></span>

<span data-ttu-id="73ffc-130">S’il s’agit d’un package de Windows Installer 64 bits exécuté sur une plateforme x64, entrez x64 dans la propriété **Résumé du modèle** .</span><span class="sxs-lookup"><span data-stu-id="73ffc-130">If this is a 64-bit Windows Installer package being run on a x64 platform, enter x64 in the **Template Summary** property.</span></span>

<span data-ttu-id="73ffc-131">S’il s’agit d’un package de Windows Installer 64 bits exécuté sur une plateforme Arm64, entrez Arm64 dans la propriété **Résumé du modèle** .</span><span class="sxs-lookup"><span data-stu-id="73ffc-131">If this is a 64-bit Windows Installer package being run on an Arm64 platform, enter Arm64 in the **Template Summary** property.</span></span>

<span data-ttu-id="73ffc-132">Un package de Windows Installer ne peut pas être marqué comme prenant en charge à la fois Intel64 et x64 ; par exemple, la valeur de la propriété de **Résumé de modèle** Intel64, x64 n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="73ffc-132">A Windows Installer package cannot be marked as supporting both Intel64 and x64; for example, the **Template Summary** property value of Intel64,x64 is invalid.</span></span>

<span data-ttu-id="73ffc-133">Un package Windows Installer ne peut pas être marqué comme prenant en charge les plateformes 32 bits et 64 bits ; par exemple, les valeurs de propriété de **Résumé de modèle** telles que Intel, x64 ou Intel, Intel64 ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="73ffc-133">A Windows Installer package cannot be marked as supporting both 32-bit and 64-bit platforms; for example, **Template Summary** property values such as Intel,x64 or Intel,Intel64 are invalid.</span></span>

<span data-ttu-id="73ffc-134">Si vous entrez 0 (zéro) dans le champ ID de langue de la propriété **Résumé du modèle** , ou si vous laissez ce champ vide, cela indique que le package est indépendant de la langue.</span><span class="sxs-lookup"><span data-stu-id="73ffc-134">Entering 0 (zero) in the language ID field of the **Template Summary** property, or leaving this field empty, indicates that the package is language neutral.</span></span>

<span data-ttu-id="73ffc-135">S’il s’agit d’un package Windows Installer exécuté sur Windows RT, entrez la valeur ARM dans la propriété **Résumé du modèle** .</span><span class="sxs-lookup"><span data-stu-id="73ffc-135">If this is a Windows Installer package being run on Windows RT, enter the value Arm in the **Template Summary** property.</span></span>

<span data-ttu-id="73ffc-136">Les modules de fusion sont les seuls packages qui peuvent avoir plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="73ffc-136">Merge Modules are the only packages that may have multiple languages.</span></span> <span data-ttu-id="73ffc-137">Une seule langue peut être spécifiée dans une base de données du programme d’installation source.</span><span class="sxs-lookup"><span data-stu-id="73ffc-137">Only one language can be specified in a source installer database.</span></span> <span data-ttu-id="73ffc-138">Pour plus d’informations, consultez [modules de fusion multilingues](multiple-language-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="73ffc-138">For more information, see [Multiple Language Merge Modules](multiple-language-merge-modules.md).</span></span>

<span data-ttu-id="73ffc-139">La plateforme alpha n’est pas prise en charge par Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="73ffc-139">The Alpha platform is not supported by Windows Installer.</span></span>

<span data-ttu-id="73ffc-140">**Windows Installer :** La syntaxe suivante n’est pas prise en charge :</span><span class="sxs-lookup"><span data-stu-id="73ffc-140">**Windows Installer:** The following syntax is not supported:</span></span>

<span data-ttu-id="73ffc-141">\[*propriété Platform* \] \[ ,*propriété Platform* \] \[ \] ,... \[ *ID* \] \[ de langue,*ID de langue* \] \[ ,... \] .</span><span class="sxs-lookup"><span data-stu-id="73ffc-141">\[*platform property*\]\[,*platform property*\]\[,...\]\[*language id*\]\[,*language id*\]\[,...\].</span></span>

<span data-ttu-id="73ffc-142">Les exemples suivants ne sont pas des valeurs valides pour la propriété **Résumé du modèle** :</span><span class="sxs-lookup"><span data-stu-id="73ffc-142">The following examples are not valid values for the **Template Summary** property:</span></span>

-   <span data-ttu-id="73ffc-143">Alpha, Intel ; 1033</span><span class="sxs-lookup"><span data-stu-id="73ffc-143">Alpha,Intel;1033</span></span>
-   <span data-ttu-id="73ffc-144">Intel, alpha ; 1033</span><span class="sxs-lookup"><span data-stu-id="73ffc-144">Intel,Alpha;1033</span></span>
-   <span data-ttu-id="73ffc-145">Alpha ; 1033</span><span class="sxs-lookup"><span data-stu-id="73ffc-145">Alpha;1033</span></span>
-   <span data-ttu-id="73ffc-146">Alpha ; 1033, 2046</span><span class="sxs-lookup"><span data-stu-id="73ffc-146">Alpha;1033,2046</span></span>

## <a name="requirements"></a><span data-ttu-id="73ffc-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73ffc-147">Requirements</span></span>



| <span data-ttu-id="73ffc-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73ffc-148">Requirement</span></span> | <span data-ttu-id="73ffc-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="73ffc-149">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73ffc-150">Version</span><span class="sxs-lookup"><span data-stu-id="73ffc-150">Version</span></span><br/> | <span data-ttu-id="73ffc-151">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="73ffc-151">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="73ffc-152">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="73ffc-152">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="73ffc-153">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="73ffc-153">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="73ffc-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73ffc-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ffc-155">Descriptions des propriétés de synthèse</span><span class="sxs-lookup"><span data-stu-id="73ffc-155">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




