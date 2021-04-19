---
description: La valeur de la propriété FILEADDSOURCE désigne une liste de clés de fichier délimitée par des virgules qui doivent être installées pour être exécutées à partir du média source.
ms.assetid: 52e328e7-7a98-4762-86a1-48e52fd55882
title: Propriété FILEADDSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b99ea1d9f4d6e212b74d6c4ee54655dce98c60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532923"
---
# <a name="fileaddsource-property"></a><span data-ttu-id="63685-103">Propriété FILEADDSOURCE</span><span class="sxs-lookup"><span data-stu-id="63685-103">FILEADDSOURCE property</span></span>

<span data-ttu-id="63685-104">La valeur de la propriété **FILEADDSOURCE** désigne une liste de clés de fichier délimitée par des virgules qui doivent être installées pour être exécutées à partir du média source.</span><span class="sxs-lookup"><span data-stu-id="63685-104">The value of the **FILEADDSOURCE** property denotes a list of file keys delimited by commas that are to be installed to run from the source media.</span></span> <span data-ttu-id="63685-105">Pour chaque clé de fichier de la liste, le programme d’installation détermine le composant qui contrôle ce fichier, puis examine toutes les fonctionnalités liées à ce composant par la table [FeatureComponents](featurecomponents-table.md) et installe la fonctionnalité qui nécessite le moins d’espace disque.</span><span class="sxs-lookup"><span data-stu-id="63685-105">For each file key in the list, the installer determines the component that controls that file, then examines all features linked to that component by the [FeatureComponents](featurecomponents-table.md) table and installs the feature that requires the least amount of disk space.</span></span> <span data-ttu-id="63685-106">Les clés de fichier de la liste doivent être présentes dans la colonne fichier de la table [file](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="63685-106">The file keys in the list must be present in the File column of the [File](file-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="63685-107">Notes</span><span class="sxs-lookup"><span data-stu-id="63685-107">Remarks</span></span>

<span data-ttu-id="63685-108">Notez que les noms de clé de fichier respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="63685-108">Note that the file key names are case-sensitive.</span></span> <span data-ttu-id="63685-109">Notez également que si l’indicateur de bit LocalOnly est défini dans la colonne attributs de la table des [composants](component-table.md) pour un composant, le composant est installé pour s’exécuter localement.</span><span class="sxs-lookup"><span data-stu-id="63685-109">Also note that if the LocalOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run locally.</span></span>

<span data-ttu-id="63685-110">Le programme d’installation évalue toujours les propriétés suivantes dans l’ordre suivant.</span><span class="sxs-lookup"><span data-stu-id="63685-110">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="63685-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="63685-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="63685-112">**Installez**</span><span class="sxs-lookup"><span data-stu-id="63685-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="63685-113">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="63685-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="63685-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="63685-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="63685-115">**INSTALLÉ**</span><span class="sxs-lookup"><span data-stu-id="63685-115">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="63685-116">**PUBLIÉS**</span><span class="sxs-lookup"><span data-stu-id="63685-116">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="63685-117">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="63685-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="63685-118">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="63685-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="63685-119">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="63685-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="63685-120">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="63685-120">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. <span data-ttu-id="63685-121">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="63685-121">**FILEADDSOURCE**</span></span>
12. [<span data-ttu-id="63685-122">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="63685-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="63685-123">Par exemple, si la ligne de commande spécifie : ADDLOCAL = ALL, ADDSOURCE = MyFeature, toutes les fonctionnalités sont tout d’abord définies sur Run-local, puis MyFeature est défini sur Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="63685-123">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="63685-124">Si la ligne de commande est : ADDSOURCE = ALL, ADDLOCAL = MyFeature, First MyFeature est défini sur Run-local, puis lorsque ADDSOURCE = ALL est évalué, toutes les fonctionnalités (y compris MyFeature) sont réinitialisées à l’exécution à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="63685-124">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="63685-125">Le programme d’installation définit la propriété [**présélectionnée**](preselected.md) sur la valeur « 1 » pendant la reprise d’une installation interrompue ou lorsque l’une des propriétés ci-dessus est spécifiée sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="63685-125">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="63685-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63685-126">Requirements</span></span>



| <span data-ttu-id="63685-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63685-127">Requirement</span></span> | <span data-ttu-id="63685-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="63685-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63685-129">Version</span><span class="sxs-lookup"><span data-stu-id="63685-129">Version</span></span><br/> | <span data-ttu-id="63685-130">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="63685-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="63685-131">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="63685-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="63685-132">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="63685-132">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="63685-133">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="63685-133">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63685-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63685-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63685-135">Propriétés</span><span class="sxs-lookup"><span data-stu-id="63685-135">Properties</span></span>](properties.md)
</dt> </dl>

 

 




