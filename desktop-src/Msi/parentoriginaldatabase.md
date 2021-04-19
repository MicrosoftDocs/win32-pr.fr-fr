---
description: Pendant une installation simultanée, le programme d’installation définit la propriété ParentOriginalDatabase dans la session de l’installation simultanée sur la même valeur que la propriété OriginalDatabase dans la session de l’installation parente.
ms.assetid: 8af1c7e5-313c-47b7-be0f-0e31ef21f6a6
title: Propriété ParentOriginalDatabase
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ab69dff7058336a5b68fd3373100f4789059ed7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545549"
---
# <a name="parentoriginaldatabase-property"></a><span data-ttu-id="9d714-103">Propriété ParentOriginalDatabase</span><span class="sxs-lookup"><span data-stu-id="9d714-103">ParentOriginalDatabase property</span></span>

<span data-ttu-id="9d714-104">Pendant une installation simultanée, le programme d’installation définit la propriété **ParentOriginalDatabase** dans la session de l’installation simultanée sur la même valeur que la propriété [**OriginalDatabase**](originaldatabase.md) dans la session de l’installation parente.</span><span class="sxs-lookup"><span data-stu-id="9d714-104">During a concurrent installation, the installer sets the **ParentOriginalDatabase** property in the concurrent installation's session to the same value as the [**OriginalDatabase**](originaldatabase.md) property in the parent installation's session.</span></span> <span data-ttu-id="9d714-105">Les installations parentes utilisent les actions d’installation simultanées pour effectuer une installation simultanée.</span><span class="sxs-lookup"><span data-stu-id="9d714-105">Parent installations use the concurrent installation actions to perform a concurrent installation.</span></span> <span data-ttu-id="9d714-106">Un package d’installation peut déterminer s’il est installé par une action d’installation simultanée en vérifiant la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="9d714-106">An installation package can determine whether it is being installed by a concurrent installation action by checking the value of this property.</span></span>

> [!Note]  
> <span data-ttu-id="9d714-107">Les installations simultanées ne sont pas recommandées pour l’installation d’applications destinées à être communiquées au public.</span><span class="sxs-lookup"><span data-stu-id="9d714-107">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="9d714-108">Pour plus d’informations sur les installations simultanées, consultez [installations simultanées](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="9d714-108">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="9d714-109">Cette propriété n’est pas définie si l’installation simultanée est exécutée par l’action [RemoveExistingProducts](removeexistingproducts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="9d714-109">This property is not set if the concurrent installation is being run by the [RemoveExistingProducts](removeexistingproducts-action.md) action.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="9d714-110">Notes</span><span class="sxs-lookup"><span data-stu-id="9d714-110">Remarks</span></span>

<span data-ttu-id="9d714-111">Pour empêcher l’installation d’un package en tant qu’installation simultanée, ajoutez l’une des instructions conditionnelles suivantes à la table [LaunchCondition](launchcondition-table.md) .</span><span class="sxs-lookup"><span data-stu-id="9d714-111">To prevent a package from ever being installed as a concurrent installation, add either of the following conditional statements to the [LaunchCondition](launchcondition-table.md) table.</span></span> <span data-ttu-id="9d714-112">Cela évite que le package ne soit installé par une action d’installation simultanée exécutée par une autre installation.</span><span class="sxs-lookup"><span data-stu-id="9d714-112">This prevents the package from ever being installed by a concurrent installation action run by another installation.</span></span> <span data-ttu-id="9d714-113">Cela n’empêche pas l’installation du package par l’action [RemoveExistingProducts](removeexistingproducts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="9d714-113">This does not prevent the package from being installed by the [RemoveExistingProducts](removeexistingproducts-action.md) action.</span></span>

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

## <a name="requirements"></a><span data-ttu-id="9d714-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d714-114">Requirements</span></span>



| <span data-ttu-id="9d714-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d714-115">Requirement</span></span> | <span data-ttu-id="9d714-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d714-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d714-117">Version</span><span class="sxs-lookup"><span data-stu-id="9d714-117">Version</span></span><br/> | <span data-ttu-id="9d714-118">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9d714-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9d714-119">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9d714-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9d714-120">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9d714-120">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9d714-121">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="9d714-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9d714-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d714-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d714-123">Propriétés</span><span class="sxs-lookup"><span data-stu-id="9d714-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="9d714-124">**ParentProductCode**</span><span class="sxs-lookup"><span data-stu-id="9d714-124">**ParentProductCode**</span></span>](parentproductcode.md)
</dt> </dl>

 

 




