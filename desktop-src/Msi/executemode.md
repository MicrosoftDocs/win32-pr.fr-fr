---
description: La propriété EXECUTEMODE spécifie la façon dont le programme d’installation exécute les mises à jour système.
ms.assetid: 7b90d2e6-d661-412b-b054-2c218c95c02a
title: Propriété EXECUTEMODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebf1de2fb7538ece838e674b62847f0c526842e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535032"
---
# <a name="executemode-property"></a><span data-ttu-id="be011-103">Propriété EXECUTEMODE</span><span class="sxs-lookup"><span data-stu-id="be011-103">EXECUTEMODE property</span></span>

<span data-ttu-id="be011-104">La propriété **EXECUTEMODE** spécifie la façon dont le programme d’installation exécute les mises à jour système.</span><span class="sxs-lookup"><span data-stu-id="be011-104">The **EXECUTEMODE** property specifies how the installer executes system updates.</span></span> <span data-ttu-id="be011-105">Cette propriété peut être utile lorsqu’il est nécessaire d’exécuter une installation sans modifier réellement le système.</span><span class="sxs-lookup"><span data-stu-id="be011-105">This property may be useful when it is necessary to run an installation without actually changing the system.</span></span> <span data-ttu-id="be011-106">La propriété peut avoir la valeur None pour désactiver les opérations de mise à jour telles que l’installation de fichiers et de valeurs de registre.</span><span class="sxs-lookup"><span data-stu-id="be011-106">The property can be set to None to disable updating operations such as the installation of files and registry values.</span></span>

<span data-ttu-id="be011-107">Cette propriété peut avoir l’une des deux valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="be011-107">This property can have one of the following two values.</span></span> <span data-ttu-id="be011-108">Le programme d’installation examine uniquement la première lettre de la valeur et ne respecte pas la casse.</span><span class="sxs-lookup"><span data-stu-id="be011-108">The installer only examines the first letter of the value and is case insensitive.</span></span>

<dl> <dt>

<span data-ttu-id="be011-109"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span><span class="sxs-lookup"><span data-stu-id="be011-109"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span></span>
</dt> <dd>

<span data-ttu-id="be011-110">Aucune modification n’est apportée au système.</span><span class="sxs-lookup"><span data-stu-id="be011-110">No changes are made to the system.</span></span> <span data-ttu-id="be011-111">Le programme d’installation exécute l’interface utilisateur, puis interroge la base de données.</span><span class="sxs-lookup"><span data-stu-id="be011-111">The installer runs the user interface and then queries the database.</span></span>

</dd> <dt>

<span data-ttu-id="be011-112"><span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Conseils</span><span class="sxs-lookup"><span data-stu-id="be011-112"><span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Script</span></span>
</dt> <dd>

<span data-ttu-id="be011-113">Toutes les modifications apportées au système sont effectuées par le biais de l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="be011-113">All changes to the system are made through script execution.</span></span> <span data-ttu-id="be011-114">Il s’agit du mode par défaut ;</span><span class="sxs-lookup"><span data-stu-id="be011-114">This is the default mode.</span></span>

</dd> </dl>

## <a name="default-value"></a><span data-ttu-id="be011-115">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="be011-115">Default Value</span></span>

<span data-ttu-id="be011-116">Si cette propriété n’est pas définie, le mode d’exécution prend par défaut le script.</span><span class="sxs-lookup"><span data-stu-id="be011-116">If this property is not defined, the execution mode defaults to Script.</span></span>

## <a name="requirements"></a><span data-ttu-id="be011-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="be011-117">Requirements</span></span>



| <span data-ttu-id="be011-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="be011-118">Requirement</span></span> | <span data-ttu-id="be011-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="be011-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be011-120">Version</span><span class="sxs-lookup"><span data-stu-id="be011-120">Version</span></span><br/> | <span data-ttu-id="be011-121">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="be011-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="be011-122">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="be011-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="be011-123">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="be011-123">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="be011-124">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="be011-124">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="be011-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be011-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be011-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be011-126">Properties</span></span>](properties.md)
</dt> </dl>

 

 




