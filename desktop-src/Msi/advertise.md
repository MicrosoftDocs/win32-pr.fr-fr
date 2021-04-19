---
description: La valeur de la propriété publier est une liste de fonctionnalités délimitée par des virgules qui doivent être publiées.
ms.assetid: ef97f70b-e4bf-4eb3-b643-046a9c348823
title: Propriété ADVERTISE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e768f22f86dacf35009ca0e0e3ef9337ef84ab70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537108"
---
# <a name="advertise-property"></a><span data-ttu-id="514c2-103">Propriété ADVERTISE</span><span class="sxs-lookup"><span data-stu-id="514c2-103">ADVERTISE property</span></span>

<span data-ttu-id="514c2-104">La valeur de la propriété **publier** est une liste de fonctionnalités délimitée par des virgules qui doivent être publiées.</span><span class="sxs-lookup"><span data-stu-id="514c2-104">The value of the **ADVERTISE** property is a list of features delimited by commas that are to be advertised.</span></span> <span data-ttu-id="514c2-105">Les fonctionnalités doivent être présentes dans la colonne Feature de la table [Feature](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="514c2-105">The features must be present in the Feature column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="514c2-106">Pour installer toutes les fonctionnalités publiées, utilisez publier = tout sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="514c2-106">To install all features as advertised, use ADVERTISE=ALL on the command line.</span></span> <span data-ttu-id="514c2-107">N’entrez pas « ADVERTISE = ALL » dans la [table des propriétés](property-table.md) , car cela génère un package publié qui ne peut pas être installé ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="514c2-107">Do not enter ADVERTISE=ALL into the [Property table](property-table.md) because this generates an advertised package that cannot be installed or removed.</span></span>

## <a name="remarks"></a><span data-ttu-id="514c2-108">Notes</span><span class="sxs-lookup"><span data-stu-id="514c2-108">Remarks</span></span>

<span data-ttu-id="514c2-109">Notez que les noms de fonctionnalités respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="514c2-109">Note that feature names are case-sensitive.</span></span>

<span data-ttu-id="514c2-110">Le programme d’installation évalue toujours les propriétés suivantes dans l’ordre suivant.</span><span class="sxs-lookup"><span data-stu-id="514c2-110">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="514c2-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="514c2-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="514c2-112">**Installez**</span><span class="sxs-lookup"><span data-stu-id="514c2-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="514c2-113">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="514c2-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="514c2-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="514c2-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="514c2-115">**INSTALLÉ**</span><span class="sxs-lookup"><span data-stu-id="514c2-115">**REINSTALL**</span></span>](reinstall.md)
6.  <span data-ttu-id="514c2-116">**PUBLIÉS**</span><span class="sxs-lookup"><span data-stu-id="514c2-116">**ADVERTISE**</span></span>
7.  [<span data-ttu-id="514c2-117">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="514c2-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="514c2-118">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="514c2-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="514c2-119">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="514c2-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="514c2-120">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="514c2-120">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="514c2-121">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="514c2-121">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="514c2-122">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="514c2-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="514c2-123">Par exemple, si la ligne de commande spécifie : ADDLOCAL = ALL, ADDSOURCE = MyFeature, toutes les fonctionnalités sont tout d’abord définies sur Run-local, puis MyFeature est défini sur Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="514c2-123">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="514c2-124">Si la ligne de commande est : ADDSOURCE = ALL, ADDLOCAL = MyFeature, First MyFeature est défini sur Run-local, puis lorsque ADDSOURCE = ALL est évalué, toutes les fonctionnalités (y compris MyFeature) sont réinitialisées à l’exécution à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="514c2-124">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="514c2-125">Le programme d’installation définit la propriété [**présélectionnée**](preselected.md) sur la valeur « 1 » pendant la reprise d’une installation interrompue ou lorsque l’une des propriétés ci-dessus est spécifiée sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="514c2-125">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="514c2-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="514c2-126">Requirements</span></span>



| <span data-ttu-id="514c2-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="514c2-127">Requirement</span></span> | <span data-ttu-id="514c2-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="514c2-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="514c2-129">Version</span><span class="sxs-lookup"><span data-stu-id="514c2-129">Version</span></span><br/> | <span data-ttu-id="514c2-130">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="514c2-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="514c2-131">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="514c2-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="514c2-132">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="514c2-132">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="514c2-133">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="514c2-133">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="514c2-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="514c2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="514c2-135">Propriétés</span><span class="sxs-lookup"><span data-stu-id="514c2-135">Properties</span></span>](properties.md)
</dt> </dl>

 

 




