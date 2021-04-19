---
description: La propriété présélectionnée indique que des fonctionnalités ont déjà été sélectionnées et que la boîte de dialogue de sélection n’a pas besoin d’être affichée. Les expressions conditionnelles qui dépendent du fait que les fonctionnalités sont déjà installées utilisent cette valeur.
ms.assetid: 2bbab8b9-084a-4515-904c-d556d183d06e
title: Propriété présélectionnée
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369a6d5fe7db99fab0032ee933afdb54bdb87efc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542709"
---
# <a name="preselected-property"></a><span data-ttu-id="d021b-103">Propriété présélectionnée</span><span class="sxs-lookup"><span data-stu-id="d021b-103">Preselected property</span></span>

<span data-ttu-id="d021b-104">La propriété **présélectionnée** indique que des fonctionnalités ont déjà été sélectionnées et que la boîte de dialogue de sélection n’a pas besoin d’être affichée.</span><span class="sxs-lookup"><span data-stu-id="d021b-104">The **Preselected** property indicates that features have already been selected and that the selection dialog need not be shown.</span></span>

<span data-ttu-id="d021b-105">Les expressions conditionnelles qui dépendent du fait que les fonctionnalités sont déjà installées utilisent cette valeur.</span><span class="sxs-lookup"><span data-stu-id="d021b-105">Conditional expressions which depend on whether features are already installed use this value.</span></span> <span data-ttu-id="d021b-106">Par exemple, la propriété peut être utilisée pour supprimer les boîtes de dialogue qui impliquent des sélections de fonctionnalités pendant la reprise d’une installation interrompue.</span><span class="sxs-lookup"><span data-stu-id="d021b-106">For example, the property can be used to suppress any dialogs involving feature selections during the resumption of a suspended installation.</span></span>

<span data-ttu-id="d021b-107">Le programme d’installation définit la propriété **présélectionnée** sur la valeur « 1 » pendant la reprise d’une installation interrompue ou lorsque l’une des propriétés suivantes est spécifiée sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="d021b-107">The installer sets the **Preselected** property to a value of "1" during the resumption of a suspended installation or when any of the following properties are specified on the command line.</span></span> <span data-ttu-id="d021b-108">Si la propriété **présélectionnée** a la valeur 1, le programme d’installation n’utilise pas la [table de conditions](condition-table.md) pour évaluer la sélection des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="d021b-108">If the **Preselected** property has been set to 1, the installer does not use the [Condition table](condition-table.md) to evaluate the selection of features.</span></span> <span data-ttu-id="d021b-109">Les fonctionnalités sont installées en fonction des propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="d021b-109">Features are installed based upon the following properties.</span></span> <span data-ttu-id="d021b-110">Le programme d’installation évalue toujours ces propriétés dans l’ordre suivant :</span><span class="sxs-lookup"><span data-stu-id="d021b-110">The installer always evaluates these properties in the following order:</span></span>

1.  [<span data-ttu-id="d021b-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="d021b-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="d021b-112">**Installez**</span><span class="sxs-lookup"><span data-stu-id="d021b-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="d021b-113">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="d021b-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="d021b-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="d021b-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="d021b-115">**INSTALLÉ**</span><span class="sxs-lookup"><span data-stu-id="d021b-115">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="d021b-116">**PUBLIÉS**</span><span class="sxs-lookup"><span data-stu-id="d021b-116">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="d021b-117">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="d021b-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="d021b-118">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="d021b-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="d021b-119">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="d021b-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="d021b-120">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="d021b-120">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="d021b-121">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="d021b-121">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="d021b-122">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="d021b-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

## <a name="requirements"></a><span data-ttu-id="d021b-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d021b-123">Requirements</span></span>



| <span data-ttu-id="d021b-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d021b-124">Requirement</span></span> | <span data-ttu-id="d021b-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="d021b-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d021b-126">Version</span><span class="sxs-lookup"><span data-stu-id="d021b-126">Version</span></span><br/> | <span data-ttu-id="d021b-127">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d021b-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d021b-128">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d021b-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d021b-129">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d021b-129">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d021b-130">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d021b-130">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d021b-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d021b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d021b-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d021b-132">Properties</span></span>](properties.md)
</dt> </dl>

 

 




