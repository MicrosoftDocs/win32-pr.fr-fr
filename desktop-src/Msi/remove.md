---
description: La valeur de la propriété supprimer est une liste de fonctionnalités délimitée par des virgules qui doivent être supprimées.
ms.assetid: 39f4609a-7bf8-42b3-b23e-0d6a40b69fd3
title: REMOVE (propriété)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f46bcd5547abdefd67f98dff312bfdf1dff41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534879"
---
# <a name="remove-property"></a><span data-ttu-id="b2e3c-103">REMOVE (propriété)</span><span class="sxs-lookup"><span data-stu-id="b2e3c-103">REMOVE property</span></span>

<span data-ttu-id="b2e3c-104">La valeur de la propriété **supprimer** est une liste de fonctionnalités délimitée par des virgules qui doivent être supprimées.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-104">The value of the **REMOVE** property is a list of features delimited by commas that are to be removed.</span></span> <span data-ttu-id="b2e3c-105">Les fonctionnalités doivent être présentes dans la colonne Feature de la [table Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="b2e3c-105">The features must be present in the Feature column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="b2e3c-106">Notez que si vous utilisez REMOVE = ALL sur la ligne de commande, le programme d’installation supprime toutes les fonctionnalités dont le niveau d’installation est supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-106">Note that if you use REMOVE=ALL on the command line, the installer removes all features having an install level greater than 0.</span></span> <span data-ttu-id="b2e3c-107">Dans ce cas, le programme d’installation ne supprime pas les fonctionnalités dont le niveau d’installation est égal à 0.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-107">In this case, the installer does not remove features having an install level of 0.</span></span> <span data-ttu-id="b2e3c-108">Pour plus d’informations sur le niveau d’installation des fonctionnalités, consultez [table](feature-table.md)des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-108">For more information about the install level of features see [Feature table](feature-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b2e3c-109">Notes</span><span class="sxs-lookup"><span data-stu-id="b2e3c-109">Remarks</span></span>

<span data-ttu-id="b2e3c-110">Pour déterminer si un produit a été configuré pour être complètement désinstallé, l’auteur d’un package peut utiliser une expression conditionnelle pour vérifier si REMOVE = ALL.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-110">To determine whether a product has been set to be completely uninstalled, a package author may use a conditional expression to check whether REMOVE=ALL.</span></span> <span data-ttu-id="b2e3c-111">Notez que si le produit est supprimé en affectant à sa fonctionnalité supérieure la valeur absent, la propriété **supprimer** ne peut pas être égale à tout jusqu’à la fin de l' [action InstallValidate](installvalidate-action.md).</span><span class="sxs-lookup"><span data-stu-id="b2e3c-111">Note that if the product is removed by setting its top feature to absent, the **REMOVE** property may not equal ALL until after the [InstallValidate action](installvalidate-action.md).</span></span> <span data-ttu-id="b2e3c-112">Cela signifie que toute action personnalisée qui dépend de REMOVE = ALL doit être séquencée après InstallValidate.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-112">This means that any custom action that depends upon REMOVE=ALL must be sequenced after the InstallValidate.</span></span> <span data-ttu-id="b2e3c-113">Pour plus d’informations, consultez également les [actions de conditionnement à exécuter pendant la suppression](conditioning-actions-to-run-during-removal.md).</span><span class="sxs-lookup"><span data-stu-id="b2e3c-113">For more information see also [Conditioning Actions to Run During Removal](conditioning-actions-to-run-during-removal.md).</span></span> <span data-ttu-id="b2e3c-114">Notez que les noms de fonctionnalités respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-114">Note that the feature names are case-sensitive.</span></span>

<span data-ttu-id="b2e3c-115">Le programme d’installation évalue toujours les propriétés suivantes dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="b2e3c-115">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="b2e3c-116">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="b2e3c-116">**ADDLOCAL**</span></span>](addlocal.md)
2.  <span data-ttu-id="b2e3c-117">**Installez**</span><span class="sxs-lookup"><span data-stu-id="b2e3c-117">**REMOVE**</span></span>
3.  [<span data-ttu-id="b2e3c-118">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="b2e3c-118">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="b2e3c-119">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b2e3c-119">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="b2e3c-120">**INSTALLÉ**</span><span class="sxs-lookup"><span data-stu-id="b2e3c-120">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="b2e3c-121">**PUBLIÉS**</span><span class="sxs-lookup"><span data-stu-id="b2e3c-121">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="b2e3c-122">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="b2e3c-122">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="b2e3c-123">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="b2e3c-123">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="b2e3c-124">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b2e3c-124">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="b2e3c-125">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="b2e3c-125">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="b2e3c-126">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="b2e3c-126">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="b2e3c-127">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b2e3c-127">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="b2e3c-128">Par exemple, si la ligne de commande spécifie ADDLOCAL = ALL, ADDSOURCE = MyFeature, toutes les fonctionnalités sont d’abord définies sur Run-local, puis MyFeature est défini sur Run-from-source.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-128">For example, if the command line specifies ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="b2e3c-129">Si la ligne de commande est ADDSOURCE = ALL, ADDLOCAL = MyFeature, First MyFeature est défini sur Run-local, alors que ADDSOURCE = ALL est évalué, toutes les fonctionnalités (y compris MyFeature) sont réinitialisées à l’exécution à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-129">If the command line is ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="b2e3c-130">Le programme d’installation définit la propriété [**présélectionnée**](preselected.md) sur la valeur « 1 » pendant la reprise d’une installation interrompue ou lorsque l’une des propriétés ci-dessus est spécifiée sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-130">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2e3c-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2e3c-131">Requirements</span></span>



| <span data-ttu-id="b2e3c-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2e3c-132">Requirement</span></span> | <span data-ttu-id="b2e3c-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2e3c-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e3c-134">Version</span><span class="sxs-lookup"><span data-stu-id="b2e3c-134">Version</span></span><br/> | <span data-ttu-id="b2e3c-135">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b2e3c-136">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b2e3c-137">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b2e3c-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b2e3c-138">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="b2e3c-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b2e3c-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2e3c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2e3c-140">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b2e3c-140">Properties</span></span>](properties.md)
</dt> </dl>

 

 




