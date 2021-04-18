---
description: La propriété CostingComplete indique si le programme d’installation a terminé l’évaluation de l’espace disque.
ms.assetid: 23688f1e-3ae8-4cd9-824c-36077cc7838f
title: Propriété CostingComplete
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b4d38b71e377bbf9b51588efef33e4fd6e93e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522790"
---
# <a name="costingcomplete-property"></a><span data-ttu-id="b9e11-103">Propriété CostingComplete</span><span class="sxs-lookup"><span data-stu-id="b9e11-103">CostingComplete property</span></span>

<span data-ttu-id="b9e11-104">La propriété **CostingComplete** indique si le programme d’installation a terminé l’évaluation de l’espace disque.</span><span class="sxs-lookup"><span data-stu-id="b9e11-104">The **CostingComplete** property indicates whether the installer has completed disk space costing.</span></span> <span data-ttu-id="b9e11-105">Cette propriété peut être utilisée pour créer une boîte de dialogue déclenchée si le coût n’est pas terminé.</span><span class="sxs-lookup"><span data-stu-id="b9e11-105">This property can be used to author a dialog box triggered if costing has not been completed.</span></span> <span data-ttu-id="b9e11-106">La propriété est définie de façon dynamique lors de l’évaluation de l’espace disque et est définie sur 1 dès que le coût est terminé.</span><span class="sxs-lookup"><span data-stu-id="b9e11-106">The property is set dynamically during disk space costing and is set to 1 as soon as the costing is complete.</span></span> <span data-ttu-id="b9e11-107">Cette propriété est initialisée à 0 par l' [action CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="b9e11-107">This property is initialized to 0 by the [CostFinalize action](costfinalize-action.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b9e11-108">Notes</span><span class="sxs-lookup"><span data-stu-id="b9e11-108">Remarks</span></span>

<span data-ttu-id="b9e11-109">Pour obtenir un exemple illustrant comment créer un «Veuillez patienter.</span><span class="sxs-lookup"><span data-stu-id="b9e11-109">For an example of how to author a "Please wait .</span></span> <span data-ttu-id="b9e11-110">.</span><span class="sxs-lookup"><span data-stu-id="b9e11-110">.</span></span> <span data-ttu-id="b9e11-111">.</span><span class="sxs-lookup"><span data-stu-id="b9e11-111">.</span></span> <span data-ttu-id="b9e11-112">"boîte de dialogue qui s’affiche lors de l’évaluation de l’espace disque, consultez la section [création d’un conditionnel" Veuillez patienter... " MessageBox.](authoring-a-conditional-please-wait-------message-box.md)</span><span class="sxs-lookup"><span data-stu-id="b9e11-112">" dialog box that pops up during disk space costing, see the section [Authoring a Conditional "Please wait . . ." Message Box](authoring-a-conditional-please-wait-------message-box.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b9e11-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9e11-113">Requirements</span></span>



| <span data-ttu-id="b9e11-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9e11-114">Requirement</span></span> | <span data-ttu-id="b9e11-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9e11-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9e11-116">Version</span><span class="sxs-lookup"><span data-stu-id="b9e11-116">Version</span></span><br/> | <span data-ttu-id="b9e11-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b9e11-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b9e11-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b9e11-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b9e11-119">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b9e11-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b9e11-120">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="b9e11-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b9e11-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9e11-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9e11-122">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b9e11-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




