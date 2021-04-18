---
description: La valeur de la propriété COMPADDSOURCE est une liste de GUID de composant à partir de la colonne ComponentId de la table de composants, délimitée par des virgules, qui doivent être installées pour s’exécuter à partir du média source.
ms.assetid: ee1e0650-674d-4189-8ef7-3d2ece89cc28
title: Propriété COMPADDSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f59526196a75599dbd2a535db6dcda4fb733936
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540409"
---
# <a name="compaddsource-property"></a><span data-ttu-id="cf6a9-103">Propriété COMPADDSOURCE</span><span class="sxs-lookup"><span data-stu-id="cf6a9-103">COMPADDSOURCE property</span></span>

<span data-ttu-id="cf6a9-104">La valeur de la propriété **COMPADDSOURCE** est une liste de GUID de composant à partir de la colonne ComponentID de la table de [composants](component-table.md) , délimitée par des virgules, qui doivent être installées pour s’exécuter à partir du média source.</span><span class="sxs-lookup"><span data-stu-id="cf6a9-104">The value of the **COMPADDSOURCE** property is a list of component GUIDs from the ComponentId column of the [Component](component-table.md) table, delimited by commas, that are to be installed to run from the source media.</span></span> <span data-ttu-id="cf6a9-105">Le programme d’installation utilise cette valeur pour déterminer les fonctionnalités qui sont configurées pour être installées pour être exécutées à partir de la source, en fonction des composants spécifiés.</span><span class="sxs-lookup"><span data-stu-id="cf6a9-105">The installer uses this value to determine which features are set to be installed to run from source, based on the specified components.</span></span> <span data-ttu-id="cf6a9-106">Pour chaque ID de composant listé, le programme d’installation examine toutes les fonctionnalités liées (par le biais de la table [FeatureComponents](featurecomponents-table.md) ) à ce composant et installe la fonctionnalité qui nécessite le moins d’espace disque à installer.</span><span class="sxs-lookup"><span data-stu-id="cf6a9-106">For each listed component ID, the installer examines all features linked (through the [FeatureComponents](featurecomponents-table.md) table) to that component, and installs the feature that requires the least amount of disk space to install.</span></span> <span data-ttu-id="cf6a9-107">Les composants listés doivent être présents dans la colonne composant de la table des [composants](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="cf6a9-107">The components listed must be present in the Component column of the [Component](component-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf6a9-108">Notes</span><span class="sxs-lookup"><span data-stu-id="cf6a9-108">Remarks</span></span>

<span data-ttu-id="cf6a9-109">Notez que les noms des composants respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="cf6a9-109">Note that the component names are case-sensitive.</span></span> <span data-ttu-id="cf6a9-110">Notez également que si l’indicateur de bit LocalOnly est défini dans la colonne attributs de la table des [composants](component-table.md) pour un composant, le composant est installé pour s’exécuter localement.</span><span class="sxs-lookup"><span data-stu-id="cf6a9-110">Also note that if the LocalOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run locally.</span></span>

<span data-ttu-id="cf6a9-111">Le programme d’installation évalue toujours les propriétés suivantes dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="cf6a9-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="cf6a9-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="cf6a9-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="cf6a9-113">**Installez**</span><span class="sxs-lookup"><span data-stu-id="cf6a9-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="cf6a9-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="cf6a9-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="cf6a9-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="cf6a9-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="cf6a9-116">**INSTALLÉ**</span><span class="sxs-lookup"><span data-stu-id="cf6a9-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="cf6a9-117">**PUBLIÉS**</span><span class="sxs-lookup"><span data-stu-id="cf6a9-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="cf6a9-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="cf6a9-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  <span data-ttu-id="cf6a9-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="cf6a9-119">**COMPADDSOURCE**</span></span>
9.  [<span data-ttu-id="cf6a9-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="cf6a9-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="cf6a9-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="cf6a9-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="cf6a9-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="cf6a9-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="cf6a9-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="cf6a9-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="cf6a9-124">Par exemple, si la ligne de commande spécifie : ADDLOCAL = ALL, ADDSOURCE = MyFeature, toutes les fonctionnalités sont tout d’abord définies sur Run-local, puis MyFeature est défini sur Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="cf6a9-124">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="cf6a9-125">Si la ligne de commande est : ADDSOURCE = ALL, ADDLOCAL = MyFeature, First MyFeature est défini sur Run-local, puis lorsque ADDSOURCE = ALL est évalué, toutes les fonctionnalités (y compris MyFeature) sont réinitialisées à l’exécution à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="cf6a9-125">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="cf6a9-126">Le programme d’installation définit la propriété [**présélectionnée**](preselected.md) sur la valeur « 1 » pendant la reprise d’une installation interrompue ou lorsque l’une des propriétés ci-dessus est spécifiée sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="cf6a9-126">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf6a9-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf6a9-127">Requirements</span></span>



| <span data-ttu-id="cf6a9-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf6a9-128">Requirement</span></span> | <span data-ttu-id="cf6a9-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf6a9-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf6a9-130">Version</span><span class="sxs-lookup"><span data-stu-id="cf6a9-130">Version</span></span><br/> | <span data-ttu-id="cf6a9-131">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cf6a9-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cf6a9-132">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cf6a9-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cf6a9-133">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cf6a9-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="cf6a9-134">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="cf6a9-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cf6a9-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf6a9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf6a9-136">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cf6a9-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




