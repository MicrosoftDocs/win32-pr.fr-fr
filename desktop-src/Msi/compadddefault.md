---
description: La valeur de la propriété COMPADDDEFAULT est une liste de GUID de composant à partir de la colonne ComponentId de la table de composants, délimitée par des virgules, qui sont installées dans leur configuration par défaut.
ms.assetid: 1bf05680-fcba-4fbb-8f8c-4203a90346ce
title: Propriété COMPADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e96d2259f0610a3030e79f8685c498a0fb2d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537455"
---
# <a name="compadddefault-property"></a><span data-ttu-id="8d75e-103">Propriété COMPADDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="8d75e-103">COMPADDDEFAULT property</span></span>

<span data-ttu-id="8d75e-104">La valeur de la propriété **COMPADDDEFAULT** est une liste de GUID de composant à partir de la colonne ComponentID de la [table de composants](component-table.md), délimitée par des virgules, qui sont installées dans leur configuration par défaut.</span><span class="sxs-lookup"><span data-stu-id="8d75e-104">The value of the **COMPADDDEFAULT** property is a list of component GUIDs from the ComponentId column of the [Component table](component-table.md), delimited by commas, that are installed in their default configuration.</span></span> <span data-ttu-id="8d75e-105">Pour chaque ID de composant dans la liste, le programme d’installation installe la fonctionnalité qui nécessite le moins d’espace disque.</span><span class="sxs-lookup"><span data-stu-id="8d75e-105">For each component ID in the list, the installer installs the feature that requires the least disk space.</span></span> <span data-ttu-id="8d75e-106">Les ID de composant dans la liste doivent être présents dans la colonne ComponentId de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="8d75e-106">The component IDs in the list must be present in the ComponentId column of the [Component table](component-table.md).</span></span> <span data-ttu-id="8d75e-107">Une fonctionnalité est installée dans le même état d’installation que si l’utilisateur avait demandé une installation à la demande de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8d75e-107">A feature is installed in the same installation state as if the user had requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="8d75e-108">L’État est déterminé par les bits définis pour la fonctionnalité dans la colonne attributs de la [table de fonctionnalités](feature-table.md), et par les bits définis pour les composants de la fonctionnalité dans la colonne attributs de la table des composants.</span><span class="sxs-lookup"><span data-stu-id="8d75e-108">The state is determined by which bits are set for the feature in the Attributes column of the [Feature table](feature-table.md), and which bits are set for the feature's components in the Attributes column of the Component table.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d75e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="8d75e-109">Remarks</span></span>

<span data-ttu-id="8d75e-110">Notez que si l’indicateur de bit SourceOnly est défini dans la colonne attributs de la table des [composants](component-table.md) pour un composant, le composant est installé pour s’exécuter à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="8d75e-110">Note that if the SourceOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run from source.</span></span>

<span data-ttu-id="8d75e-111">Le programme d’installation évalue toujours les propriétés suivantes dans l’ordre suivant.</span><span class="sxs-lookup"><span data-stu-id="8d75e-111">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="8d75e-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="8d75e-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="8d75e-113">**Installez**</span><span class="sxs-lookup"><span data-stu-id="8d75e-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="8d75e-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="8d75e-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="8d75e-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="8d75e-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="8d75e-116">**INSTALLÉ**</span><span class="sxs-lookup"><span data-stu-id="8d75e-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="8d75e-117">**PUBLIÉS**</span><span class="sxs-lookup"><span data-stu-id="8d75e-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="8d75e-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="8d75e-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="8d75e-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="8d75e-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  <span data-ttu-id="8d75e-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="8d75e-120">**COMPADDDEFAULT**</span></span>
10. [<span data-ttu-id="8d75e-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="8d75e-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="8d75e-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="8d75e-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="8d75e-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="8d75e-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="8d75e-124">Par exemple, si la ligne de commande spécifie : ADDLOCAL = ALL, ADDSOURCE = MyFeature, toutes les fonctionnalités sont tout d’abord définies sur Run-local, puis MyFeature est défini sur Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="8d75e-124">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="8d75e-125">Si la ligne de commande est : ADDSOURCE = ALL, ADDLOCAL = MyFeature, First MyFeature est défini sur Run-local, puis lorsque ADDSOURCE = ALL est évalué, toutes les fonctionnalités (y compris MyFeature) sont réinitialisées à l’exécution à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="8d75e-125">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="8d75e-126">Le programme d’installation définit la propriété [**présélectionnée**](preselected.md) sur la valeur « 1 » pendant la reprise d’une installation interrompue ou lorsque l’une des propriétés ci-dessus est spécifiée sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="8d75e-126">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d75e-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d75e-127">Requirements</span></span>



| <span data-ttu-id="8d75e-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d75e-128">Requirement</span></span> | <span data-ttu-id="8d75e-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d75e-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d75e-130">Version</span><span class="sxs-lookup"><span data-stu-id="8d75e-130">Version</span></span><br/> | <span data-ttu-id="8d75e-131">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8d75e-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8d75e-132">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8d75e-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8d75e-133">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8d75e-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="8d75e-134">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="8d75e-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8d75e-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d75e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d75e-136">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8d75e-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




