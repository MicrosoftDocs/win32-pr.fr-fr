---
description: Le programme d’installation définit la propriété PATCH sur une liste de correctifs appliqués en appelant MsiApplyPatch, MsiApplyMultiplePatches ou l’option de ligne de commande/p.
ms.assetid: f2993544-2124-4fb0-8bb3-59f5d8e76b83
title: Propriété PATCH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870c480c1fdff0f979701e059bfcd6eb187a4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530340"
---
# <a name="patch-property"></a><span data-ttu-id="8fcf2-103">Propriété PATCH</span><span class="sxs-lookup"><span data-stu-id="8fcf2-103">PATCH property</span></span>

<span data-ttu-id="8fcf2-104">Le programme d’installation définit la propriété **patch** sur une liste de correctifs appliqués en appelant [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha), [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) ou l’option de [ligne de commande](command-line-options.md)/p.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-104">The installer sets the **PATCH** property to a list of patches being applied by calling [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha), [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) or the /p [Command Line Option](command-line-options.md).</span></span> <span data-ttu-id="8fcf2-105">Vous pouvez également définir la propriété **patch** sur la ligne de commande lors de l’installation d’un package à l’aide de [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) ou de l’option de ligne de commande/i.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-105">You can also set the **PATCH** property on the command line while installing a package using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) or the /i Command Line Option.</span></span>

<span data-ttu-id="8fcf2-106">La valeur de la propriété **patch** est la liste des correctifs en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-106">The value of the **PATCH** property is a list of the patches that are being installed.</span></span> <span data-ttu-id="8fcf2-107">Chaque correctif de la liste est représenté par le chemin d’accès complet au package du correctif (fichier. msp). Les chemins d’accès complets de la liste sont séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-107">Each patch in the list is represented by the full path to the patch's package (.msp file.) The full paths in the list are separated by semicolons.</span></span>

<span data-ttu-id="8fcf2-108">**Windows Installer 2,0 :** Plusieurs correctifs ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-108">**Windows Installer 2.0:** Multiple patches are not supported.</span></span> <span data-ttu-id="8fcf2-109">Windows Installer 3,0 est requis pour appliquer plusieurs correctifs.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-109">Windows Installer 3.0 is required to apply multiple patches.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fcf2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="8fcf2-110">Remarks</span></span>

<span data-ttu-id="8fcf2-111">Si vous créez un package de correctifs à l’aide de [Msimsp.exe](msimsp-exe.md) et [Patchwiz.dll](patchwiz-dll.md) vous pouvez spécifier qu’une action ou une boîte de dialogue s’exécute uniquement lorsqu’un correctif particulier est appliqué.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-111">If you create a patch package using [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) you can specify that an action or a dialog box only run when a particular patch is being applied.</span></span> <span data-ttu-id="8fcf2-112">Lorsque vous créez le package de correctifs, par exemple test. msp, vous créez une image mise à niveau du produit et un fichier de propriétés de création de correctifs.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-112">When you create the patch package, for example test.msp, you author an upgraded image of the product and a patch creation properties file.</span></span> <span data-ttu-id="8fcf2-113">Lors de la création du fichier de propriétés de création de correctifs, vous pouvez entrer un nom de propriété, par exemple PATCHFORTEST, dans le champ MediaSrcPropName de la table [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) .</span><span class="sxs-lookup"><span data-stu-id="8fcf2-113">When authoring the patch creation properties file you can enter a property name, for example PATCHFORTEST, in the MediaSrcPropName field of the [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) table.</span></span> <span data-ttu-id="8fcf2-114">Lorsque vous créez les tables de séquence de l’image mise à niveau du produit, vous pouvez inclure dans la colonne condition de la table de séquence une instruction conditionnelle pour l’action ou la boîte de dialogue que vous souhaitez rendre conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-114">When you author the sequence tables of the upgraded image of the product, you can include in the Condition column of the sequence table a conditional statement for the action or dialog box you want to make conditional.</span></span>

<span data-ttu-id="8fcf2-115">Par exemple, vous pouvez utiliser l’instruction conditionnelle suivante pour exécuter une action ou une boîte de dialogue uniquement lorsque test. msp est appliqué.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-115">For example, you can use the following conditional statement to run an action or dialog box only when test.msp is being applied.</span></span>

<dl> <span data-ttu-id="8fcf2-116">PATCH ET PATCHFORTEST ET PATCH >< PATCHFORTEST</span><span class="sxs-lookup"><span data-stu-id="8fcf2-116">PATCH AND PATCHFORTEST AND PATCH >< PATCHFORTEST</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="8fcf2-117">Étant donné que la propriété **patch** peut contenir plusieurs correctifs, utilisez l’opérateur de sous-chaîne « >< » pour tester la présence d’un correctif spécifique plutôt que l’opérateur égal « = ».</span><span class="sxs-lookup"><span data-stu-id="8fcf2-117">Because the **PATCH** property can contain multiple patches, use the substring operator "><" to test for the presence of a particular patch rather than the equals operator "=".</span></span> <span data-ttu-id="8fcf2-118">Pour plus d’informations sur les instructions conditionnelles, consultez la section [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="8fcf2-118">For more information about conditional statements see the [Conditional Statement Syntax](conditional-statement-syntax.md) section.</span></span>

 

<span data-ttu-id="8fcf2-119">Le programme d’installation définit les deux propriétés si vous appliquez une liste de correctifs incluant test. msp.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-119">The installer sets both properties if you apply a list of patches that includes test.msp.</span></span> <span data-ttu-id="8fcf2-120">Par exemple, vous pouvez utiliser l' [option de ligne de commande](command-line-options.md) /p pour appliquer une liste de deux correctifs.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-120">For example, you can use the /p [Command Line Option](command-line-options.md) to apply a list of two patches.</span></span>

<span data-ttu-id="8fcf2-121">**msiexec/qb/p \\ \\ éraflure \\ Scratch \\ \\ \\ test. msp ; \\ \\ éraflures \\ \\ xyz \\ bar. msp**</span><span class="sxs-lookup"><span data-stu-id="8fcf2-121">**msiexec /qb /p \\\\scratch\\scratch\\XYZ\\Patches\\test.msp;\\\\scratch\\scratch\\XYZ\\bar.msp**</span></span>

<span data-ttu-id="8fcf2-122">Le programme d’installation définit les propriétés **patch** et PATCHFORTEST comme suit.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-122">The installer sets the **PATCH** and PATCHFORTEST properties as follows.</span></span>

<dl> <span data-ttu-id="8fcf2-123">PATCH = éraflure \\ \\ \\ Scratch \\ \\ \\ test. msp \\ \\ éraflures \\ \\ xyz \\ bar. msp</span><span class="sxs-lookup"><span data-stu-id="8fcf2-123">PATCH=\\\\scratch\\scratch\\XYZ\\Patches\\test.msp;\\\\scratch\\scratch\\XYZ\\bar.msp</span></span>  
<span data-ttu-id="8fcf2-124">PATCHFORTEST = éraflure \\ \\ \\ Scratch \\ \\ \\ test. msp</span><span class="sxs-lookup"><span data-stu-id="8fcf2-124">PATCHFORTEST=\\\\scratch\\scratch\\XYZ\\Patches\\test.msp</span></span>  
</dl>

<span data-ttu-id="8fcf2-125">Dans ce cas, la condition est TRUE et la boîte de dialogue ou l’action conditionnelle ci-dessus peut s’exécuter pour chaque correctif installé, test. msp et bar. msp.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-125">In this case, the condition is TRUE and the above conditional action or dialog box can run for each patch being installed, test.msp and bar.msp.</span></span>

<span data-ttu-id="8fcf2-126">Si test. msp n’est pas appliqué, le programme d’installation ne l’inclut pas dans la propriété **patch** et ne définit pas PATCHFORTEST.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-126">If test.msp is not being applied, the installer does not include it in the **PATCH** property and does not set PATCHFORTEST.</span></span> <span data-ttu-id="8fcf2-127">Dans ce cas, la condition ci-dessus a la valeur FALSe et la boîte de dialogue ou l’action conditionnelle ne s’exécute pas.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-127">In this case, the condition above is FALSE and the conditional action or dialog box does not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fcf2-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fcf2-128">Requirements</span></span>



| <span data-ttu-id="8fcf2-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fcf2-129">Requirement</span></span> | <span data-ttu-id="8fcf2-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fcf2-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fcf2-131">Version</span><span class="sxs-lookup"><span data-stu-id="8fcf2-131">Version</span></span><br/> | <span data-ttu-id="8fcf2-132">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8fcf2-133">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8fcf2-134">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8fcf2-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="8fcf2-135">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="8fcf2-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8fcf2-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fcf2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fcf2-137">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8fcf2-137">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="8fcf2-138">Syntaxe d’instruction conditionnelle</span><span class="sxs-lookup"><span data-stu-id="8fcf2-138">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> <dt>

[<span data-ttu-id="8fcf2-139">Exemples de syntaxe d’instruction conditionnelle</span><span class="sxs-lookup"><span data-stu-id="8fcf2-139">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)
</dt> </dl>

 

 




