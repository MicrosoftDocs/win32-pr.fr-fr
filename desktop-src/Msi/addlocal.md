---
description: La valeur de la propriété ADDLOCAL est une liste de fonctionnalités qui sont délimitées par des virgules et qui doivent être installées localement.
ms.assetid: d408986d-7889-4fd9-8202-1d2e59673a2f
title: Propriété ADDLOCAL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9618389d6e409829dce1eb7bb3a38c1269a2e06d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545957"
---
# <a name="addlocal-property"></a><span data-ttu-id="102e2-103">Propriété ADDLOCAL</span><span class="sxs-lookup"><span data-stu-id="102e2-103">ADDLOCAL property</span></span>

<span data-ttu-id="102e2-104">La valeur de la propriété **addlocal** est une liste de fonctionnalités qui sont délimitées par des virgules et qui doivent être installées localement.</span><span class="sxs-lookup"><span data-stu-id="102e2-104">The value of the **ADDLOCAL** property is a list of features that are delimited by commas, and are to be installed locally.</span></span> <span data-ttu-id="102e2-105">Les fonctionnalités doivent être présentes dans la colonne Feature de la [table Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="102e2-105">The features must be present in the Feature column of the [Feature Table](feature-table.md).</span></span> <span data-ttu-id="102e2-106">Pour installer toutes les fonctionnalités localement, utilisez ADDLOCAL = ALL sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="102e2-106">To install all features locally, use ADDLOCAL=ALL on the command line.</span></span> <span data-ttu-id="102e2-107">N’entrez pas ADDLOCAL = ALL dans la [table de propriétés](property-table.md), car cela génère un package installé localement qui ne peut pas être supprimé correctement.</span><span class="sxs-lookup"><span data-stu-id="102e2-107">Do not enter ADDLOCAL=ALL into the [Property Table](property-table.md), because this generates a locally installed package that cannot be correctly removed.</span></span>

## <a name="remarks"></a><span data-ttu-id="102e2-108">Notes</span><span class="sxs-lookup"><span data-stu-id="102e2-108">Remarks</span></span>

<span data-ttu-id="102e2-109">Les noms de fonctionnalités respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="102e2-109">Feature names are case sensitive.</span></span> <span data-ttu-id="102e2-110">Si l’indicateur de bit SourceOnly est défini dans la colonne attributs de la [table des composants](component-table.md) pour un composant d’une fonctionnalité de la liste, ce composant est installé en tant qu’exécution à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="102e2-110">If the SourceOnly bit flag is set in the Attributes column of the [Component Table](component-table.md) for a component of a feature in the list, that component is installed as run from source.</span></span>

<span data-ttu-id="102e2-111">Le programme d’installation évalue toujours les propriétés suivantes dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="102e2-111">The installer always evaluates the following properties in the following order:</span></span>

1.  <span data-ttu-id="102e2-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="102e2-112">**ADDLOCAL**</span></span>
2.  [<span data-ttu-id="102e2-113">**Installez**</span><span class="sxs-lookup"><span data-stu-id="102e2-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="102e2-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="102e2-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="102e2-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="102e2-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="102e2-116">**INSTALLÉ**</span><span class="sxs-lookup"><span data-stu-id="102e2-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="102e2-117">**PUBLIÉS**</span><span class="sxs-lookup"><span data-stu-id="102e2-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="102e2-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="102e2-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="102e2-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="102e2-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="102e2-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="102e2-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="102e2-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="102e2-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="102e2-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="102e2-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="102e2-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="102e2-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="102e2-124">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="102e2-124">For example:</span></span>

-   <span data-ttu-id="102e2-125">Si la ligne de commande spécifie : ADDLOCAL = ALL, ADDSOURCE = **MyFeature**, toutes les fonctionnalités sont tout d’abord définies sur Run-local, puis **MyFeature** est défini sur Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="102e2-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = **MyFeature**, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="102e2-126">Si la ligne de commande est : ADDSOURCE = ALL, ADDLOCAL =**MyFeature**, First **MyFeature** est défini sur Run-local, puis lorsque addsource = All est évalué, toutes les fonctionnalités (y compris **MyFeature**) sont réinitialisées à l’exécution à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="102e2-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=**MyFeature**, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="102e2-127">Le programme d’installation définit la propriété [**présélectionnée**](preselected.md) sur la valeur « 1 » pendant la reprise d’une installation interrompue, ou lorsque l’une des propriétés précédentes est spécifiée sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="102e2-127">The installer sets the [**Preselected**](preselected.md) Property to a value of "1" during the resumption of a suspended installation, or when any of the previous properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="102e2-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="102e2-128">Requirements</span></span>



| <span data-ttu-id="102e2-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="102e2-129">Requirement</span></span> | <span data-ttu-id="102e2-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="102e2-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="102e2-131">Version</span><span class="sxs-lookup"><span data-stu-id="102e2-131">Version</span></span><br/> | <span data-ttu-id="102e2-132">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="102e2-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="102e2-133">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="102e2-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="102e2-134">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="102e2-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="102e2-135">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="102e2-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="102e2-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="102e2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="102e2-137">Propriétés</span><span class="sxs-lookup"><span data-stu-id="102e2-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




