---
description: La valeur de la propriété réinstaller est une liste de fonctionnalités délimitée par des virgules qui doivent être réinstallées. Les fonctionnalités indiquées doivent être présentes dans la colonne fonctionnalité du tableau des fonctionnalités. Pour réinstaller toutes les fonctionnalités, utilisez réinstaller = ALL sur la ligne de commande.
ms.assetid: 14346fef-7923-4f30-bca8-96a29c0f820d
title: RÉINSTALLER la propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5147b4120968991aa3cb6caf438b7565281fc6f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544018"
---
# <a name="reinstall-property"></a><span data-ttu-id="4bfa7-105">RÉINSTALLER la propriété</span><span class="sxs-lookup"><span data-stu-id="4bfa7-105">REINSTALL property</span></span>

<span data-ttu-id="4bfa7-106">La valeur de la propriété **réinstaller** est une liste de fonctionnalités délimitée par des virgules qui doivent être réinstallées.</span><span class="sxs-lookup"><span data-stu-id="4bfa7-106">The value of the **REINSTALL** property is a list of features delimited by commas that are to be reinstalled.</span></span> <span data-ttu-id="4bfa7-107">Les fonctionnalités indiquées doivent être présentes dans la colonne fonctionnalité [du tableau des fonctionnalités.](feature-table.md)</span><span class="sxs-lookup"><span data-stu-id="4bfa7-107">The features listed must be present in the Feature column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="4bfa7-108">Pour réinstaller toutes les fonctionnalités, utilisez réinstaller = ALL sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="4bfa7-108">To reinstall all features use REINSTALL=ALL on the command line.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bfa7-109">Notes</span><span class="sxs-lookup"><span data-stu-id="4bfa7-109">Remarks</span></span>

<span data-ttu-id="4bfa7-110">Notez que les noms de fonctionnalités respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="4bfa7-110">Note that the feature names are case-sensitive.</span></span>

<span data-ttu-id="4bfa7-111">Si la propriété **réinstaller** est définie, la propriété [**REINSTALLMODE**](reinstallmode.md) doit également être définie pour indiquer le type de réinstallation à effectuer.</span><span class="sxs-lookup"><span data-stu-id="4bfa7-111">If the **REINSTALL** property is set, the [**REINSTALLMODE**](reinstallmode.md) property should also be set, to indicate the type of reinstall to be performed.</span></span> <span data-ttu-id="4bfa7-112">Si la propriété **REINSTALLMODE** n’est pas définie, par défaut, tous les fichiers qui sont actuellement installés sont réinstallés, si le fichier actuellement installé est une version antérieure (ou n’est pas présent).</span><span class="sxs-lookup"><span data-stu-id="4bfa7-112">If the **REINSTALLMODE** property is not set, then by default all files that are currently installed are reinstalled, IF the currently installed file is a lesser version (or is not present).</span></span> <span data-ttu-id="4bfa7-113">Par défaut, aucune entrée de Registre n’est réécrite.</span><span class="sxs-lookup"><span data-stu-id="4bfa7-113">By default, no registry entries are rewritten.</span></span>

<span data-ttu-id="4bfa7-114">Notez que même si la **réinstallation** est définie sur tous, seules les fonctionnalités qui ont déjà été installées précédemment sont réinstallées.</span><span class="sxs-lookup"><span data-stu-id="4bfa7-114">Note that even if **REINSTALL** is set to ALL, only those features that were already installed previously are reinstalled.</span></span> <span data-ttu-id="4bfa7-115">Ainsi, si la **réinstallation** est définie pour un produit qui n’est pas encore installé, aucune action d’installation n’aura lieu.</span><span class="sxs-lookup"><span data-stu-id="4bfa7-115">Thus, if **REINSTALL** is set for a product that is yet to be installed, no installation action will take place at all.</span></span>

<span data-ttu-id="4bfa7-116">Le programme d’installation évalue toujours les propriétés suivantes dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="4bfa7-116">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="4bfa7-117">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="4bfa7-117">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="4bfa7-118">**Installez**</span><span class="sxs-lookup"><span data-stu-id="4bfa7-118">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="4bfa7-119">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="4bfa7-119">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="4bfa7-120">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="4bfa7-120">**ADDDEFAULT**</span></span>](adddefault.md)
5.  <span data-ttu-id="4bfa7-121">**INSTALLÉ**</span><span class="sxs-lookup"><span data-stu-id="4bfa7-121">**REINSTALL**</span></span>
6.  [<span data-ttu-id="4bfa7-122">**PUBLIÉS**</span><span class="sxs-lookup"><span data-stu-id="4bfa7-122">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="4bfa7-123">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="4bfa7-123">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="4bfa7-124">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="4bfa7-124">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="4bfa7-125">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="4bfa7-125">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
10. [<span data-ttu-id="4bfa7-126">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="4bfa7-126">**FILEADDSOURCE**</span></span>](fileaddsource.md)
11. [<span data-ttu-id="4bfa7-127">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="4bfa7-127">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="4bfa7-128">Par exemple, si la ligne de commande spécifie : ADDLOCAL = ALL, ADDSOURCE = MyFeature, toutes les fonctionnalités sont tout d’abord définies sur Run-local, puis MyFeature est défini sur Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="4bfa7-128">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="4bfa7-129">Si la ligne de commande est : ADDSOURCE = ALL, ADDLOCAL = MyFeature, First MyFeature est défini sur Run-local, puis lorsque ADDSOURCE = ALL est évalué, toutes les fonctionnalités (y compris MyFeature) sont réinitialisées à l’exécution à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="4bfa7-129">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="4bfa7-130">Le programme d’installation définit la propriété [**présélectionnée**](preselected.md) sur la valeur « 1 » pendant la reprise d’une installation interrompue ou lorsque l’une des propriétés ci-dessus est spécifiée sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="4bfa7-130">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bfa7-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4bfa7-131">Requirements</span></span>



| <span data-ttu-id="4bfa7-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4bfa7-132">Requirement</span></span> | <span data-ttu-id="4bfa7-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bfa7-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bfa7-134">Version</span><span class="sxs-lookup"><span data-stu-id="4bfa7-134">Version</span></span><br/> | <span data-ttu-id="4bfa7-135">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4bfa7-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4bfa7-136">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4bfa7-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4bfa7-137">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4bfa7-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="4bfa7-138">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="4bfa7-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4bfa7-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bfa7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bfa7-140">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4bfa7-140">Properties</span></span>](properties.md)
</dt> </dl>

 

 




