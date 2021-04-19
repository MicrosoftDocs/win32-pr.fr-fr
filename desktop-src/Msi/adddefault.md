---
description: La valeur de la propriété ADDDEFAULT est une liste de fonctionnalités délimitée par des virgules, qui doivent être installées dans leur configuration par défaut.
ms.assetid: 78cec3fc-c653-487a-b41c-a43c42e3a157
title: Propriété ADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43960b6d70d704337f373031ab4972bcb95dada7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537410"
---
# <a name="adddefault-property"></a><span data-ttu-id="4781a-103">Propriété ADDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="4781a-103">ADDDEFAULT property</span></span>

<span data-ttu-id="4781a-104">La valeur de la propriété **AddDefault** est une liste de fonctionnalités délimitée par des virgules, qui doivent être installées dans leur configuration par défaut.</span><span class="sxs-lookup"><span data-stu-id="4781a-104">The value of the **ADDDEFAULT** property is a list of features delimited by commas, which are to be installed in their default configuration.</span></span> <span data-ttu-id="4781a-105">Les fonctionnalités doivent être présentes dans la colonne Feature de la [table Feature.](feature-table.md)</span><span class="sxs-lookup"><span data-stu-id="4781a-105">The features must be present in the Feature column of the [Feature Table.](feature-table.md)</span></span> <span data-ttu-id="4781a-106">Pour installer toutes les fonctionnalités dans leurs configurations par défaut, utilisez ADDDEFAULT = ALL sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="4781a-106">To install all features in their default configurations, use ADDDEFAULT=ALL on the command line.</span></span>

<span data-ttu-id="4781a-107">Une fonctionnalité indiquée dans la propriété **AddDefault** est installée dans le même état d’installation que si l’utilisateur a demandé une installation à la demande de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="4781a-107">A feature listed in the **ADDDEFAULT** property is installed in the same installation state as if the user requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="4781a-108">L’État est déterminé par les bits définis pour la fonctionnalité dans la colonne attributs de la table de [fonctionnalités](feature-table.md), et les bits définis pour les composants de la fonctionnalité dans la colonne attributs de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="4781a-108">The state is determined by the bits that are set for the feature in the Attributes column of the [Feature Table](feature-table.md), and which bits are set for the feature components in the Attributes column of the [Component Table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4781a-109">Notes</span><span class="sxs-lookup"><span data-stu-id="4781a-109">Remarks</span></span>

<span data-ttu-id="4781a-110">Les noms des fonctionnalités respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="4781a-110">The feature names are case sensitive.</span></span>

<span data-ttu-id="4781a-111">Le programme d’installation évalue toujours les propriétés suivantes dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="4781a-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="4781a-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="4781a-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="4781a-113">**Installez**</span><span class="sxs-lookup"><span data-stu-id="4781a-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="4781a-114">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="4781a-114">**ADDSOURCE**</span></span>](addsource.md)
4.  <span data-ttu-id="4781a-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="4781a-115">**ADDDEFAULT**</span></span>
5.  [<span data-ttu-id="4781a-116">**INSTALLÉ**</span><span class="sxs-lookup"><span data-stu-id="4781a-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="4781a-117">**PUBLIÉS**</span><span class="sxs-lookup"><span data-stu-id="4781a-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="4781a-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="4781a-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="4781a-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="4781a-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="4781a-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="4781a-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="4781a-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="4781a-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="4781a-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="4781a-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="4781a-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="4781a-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="4781a-124">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="4781a-124">For example:</span></span>

-   <span data-ttu-id="4781a-125">Si la ligne de commande spécifie : ADDLOCAL = ALL, ADDSOURCE = MyFeature, toutes les fonctionnalités sont tout d’abord définies sur Run-local, puis **MyFeature** est défini sur Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="4781a-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="4781a-126">Si la ligne de commande est : ADDSOURCE = ALL, ADDLOCAL = MyFeature, First **MyFeature** est défini sur Run-local, puis lorsque addsource = All est évalué, toutes les fonctionnalités (y compris **MyFeature**) sont réinitialisées à l’exécution à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="4781a-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="4781a-127">Le programme d’installation définit la propriété [**présélectionnée**](preselected.md) sur la valeur « 1 » pendant la reprise d’une installation interrompue, ou lorsque l’une des propriétés ci-dessus est spécifiée sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="4781a-127">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation, or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="4781a-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4781a-128">Requirements</span></span>



| <span data-ttu-id="4781a-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4781a-129">Requirement</span></span> | <span data-ttu-id="4781a-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="4781a-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4781a-131">Version</span><span class="sxs-lookup"><span data-stu-id="4781a-131">Version</span></span><br/> | <span data-ttu-id="4781a-132">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4781a-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4781a-133">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4781a-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4781a-134">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4781a-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="4781a-135">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="4781a-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4781a-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4781a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4781a-137">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4781a-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




