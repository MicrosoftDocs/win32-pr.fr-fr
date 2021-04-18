---
description: La propriété INSTALLLEVEL est le niveau initial auquel les fonctionnalités sont sélectionnées &\# 0034 ; sur&\# 0034 ; pour une installation par défaut.
ms.assetid: 5051cc46-837a-4446-a54c-4bd4081a424c
title: Propriété INSTALLLEVEL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebc0616fdf49e2c713c65017a202320fa6ea9622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540292"
---
# <a name="installlevel-property"></a><span data-ttu-id="5ea21-103">Propriété INSTALLLEVEL</span><span class="sxs-lookup"><span data-stu-id="5ea21-103">INSTALLLEVEL property</span></span>

<span data-ttu-id="5ea21-104">La propriété **INSTALLLEVEL** est le niveau initial auquel les fonctionnalités sont sélectionnées par défaut pour l’installation.</span><span class="sxs-lookup"><span data-stu-id="5ea21-104">The **INSTALLLEVEL** property is the initial level at which features are selected "ON" for installation by default.</span></span> <span data-ttu-id="5ea21-105">Une fonctionnalité est installée uniquement si la valeur du champ niveau de la [table de fonctionnalités](feature-table.md) est inférieure ou égale à la valeur actuelle de INSTALLLEVEL.</span><span class="sxs-lookup"><span data-stu-id="5ea21-105">A feature is installed only if the value in the Level field of the [Feature table](feature-table.md) is less than or equal to the current INSTALLLEVEL value.</span></span> <span data-ttu-id="5ea21-106">Le niveau d’installation de n’importe quelle installation est spécifié par la propriété **INSTALLLEVEL** et peut être un entier compris entre 1 et 32 767.</span><span class="sxs-lookup"><span data-stu-id="5ea21-106">The installation level for any installation is specified by the **INSTALLLEVEL** property, and can be an integral from 1 to 32,767.</span></span> <span data-ttu-id="5ea21-107">Pour plus d’informations sur les niveaux d’installation, consultez [table des fonctionnalités](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="5ea21-107">For further discussion of installation levels, see [Feature Table](feature-table.md).</span></span>

## <a name="default-value"></a><span data-ttu-id="5ea21-108">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="5ea21-108">Default Value</span></span>

<span data-ttu-id="5ea21-109">Si aucune valeur n’est spécifiée, le niveau d’installation par défaut est 1.</span><span class="sxs-lookup"><span data-stu-id="5ea21-109">If no value is specified, the install level defaults to 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ea21-110">Notes</span><span class="sxs-lookup"><span data-stu-id="5ea21-110">Remarks</span></span>

<span data-ttu-id="5ea21-111">Le niveau d’installation spécifié par la propriété **INSTALLLEVEL** peut être remplacé par les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="5ea21-111">The installation level specified by the **INSTALLLEVEL** property can be overridden by the following properties:</span></span>

-   [<span data-ttu-id="5ea21-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="5ea21-112">**ADDLOCAL**</span></span>](addlocal.md)
-   [<span data-ttu-id="5ea21-113">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="5ea21-113">**ADDSOURCE**</span></span>](addsource.md)
-   [<span data-ttu-id="5ea21-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="5ea21-114">**ADDDEFAULT**</span></span>](adddefault.md)
-   [<span data-ttu-id="5ea21-115">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="5ea21-115">**COMPADDLOCAL**</span></span>](compaddlocal.md)
-   [<span data-ttu-id="5ea21-116">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="5ea21-116">**COMPADDSOURCE**</span></span>](compaddsource.md)
-   [<span data-ttu-id="5ea21-117">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="5ea21-117">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
-   [<span data-ttu-id="5ea21-118">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="5ea21-118">**FILEADDSOURCE**</span></span>](fileaddsource.md)
-   [<span data-ttu-id="5ea21-119">**Installez**</span><span class="sxs-lookup"><span data-stu-id="5ea21-119">**REMOVE**</span></span>](remove.md)
-   [<span data-ttu-id="5ea21-120">**INSTALLÉ**</span><span class="sxs-lookup"><span data-stu-id="5ea21-120">**REINSTALL**</span></span>](reinstall.md)
-   [<span data-ttu-id="5ea21-121">**PUBLIÉS**</span><span class="sxs-lookup"><span data-stu-id="5ea21-121">**ADVERTISE**</span></span>](advertise.md)

<span data-ttu-id="5ea21-122">Par exemple, la définition de ADDLOCAL = ALL installe toutes les fonctionnalités localement, quelle que soit la valeur de la propriété **INSTALLLEVEL** .</span><span class="sxs-lookup"><span data-stu-id="5ea21-122">For example, setting ADDLOCAL=ALL installs all features locally regardless of the value of the **INSTALLLEVEL** property.</span></span> <span data-ttu-id="5ea21-123">Si la valeur de la colonne Level dans la [table Feature](feature-table.md) est 0, cette fonctionnalité n’est pas installée et n’est pas affichée dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5ea21-123">If the value of the Level column in the [Feature table](feature-table.md) is 0, that feature is not installed and not displayed in the UI.</span></span>

<span data-ttu-id="5ea21-124">Un administrateur peut désactiver définitivement une fonctionnalité en appliquant une transformation de personnalisation qui définit 0 dans la colonne de niveau pour cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="5ea21-124">An administrator can permanently disable a feature by applying a customization transform that sets a 0 in the Level column for that feature.</span></span> <span data-ttu-id="5ea21-125">L’application de la transformation de personnalisation empêche l’installation et l’affichage de la fonctionnalité même si l’utilisateur sélectionne une installation complète à l’aide de l’interface utilisateur ou en affectant à ADDLOCAL la valeur ALL sur la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="5ea21-125">The application of the customization transform prevents the installation and display of the feature even if the user selects a complete installation using the UI or by setting ADDLOCAL to ALL on the command line.</span></span> <span data-ttu-id="5ea21-126">Consultez [un exemple de transformation de personnalisation](a-customization-transform-example.md).</span><span class="sxs-lookup"><span data-stu-id="5ea21-126">See [A Customization Transform Example](a-customization-transform-example.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ea21-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ea21-127">Requirements</span></span>



| <span data-ttu-id="5ea21-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ea21-128">Requirement</span></span> | <span data-ttu-id="5ea21-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ea21-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea21-130">Version</span><span class="sxs-lookup"><span data-stu-id="5ea21-130">Version</span></span><br/> | <span data-ttu-id="5ea21-131">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5ea21-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5ea21-132">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5ea21-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5ea21-133">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5ea21-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="5ea21-134">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="5ea21-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5ea21-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ea21-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea21-136">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5ea21-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




