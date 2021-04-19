---
description: La propriété UpgradeCode est un GUID qui représente un ensemble connexe de produits. La fonction UpgradeCode est utilisée dans la table de mise à niveau pour rechercher les versions associées du produit qui sont déjà installées. Cette propriété est utilisée par l’action RegisterProduct.
ms.assetid: 6cdee5d8-8aa0-4fad-9338-152ee33b8077
title: UpgradeCode, propriété
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1e5493ad651e609f6ef9d7ae14e07c0c15b5b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528130"
---
# <a name="upgradecode-property"></a><span data-ttu-id="a8694-104">UpgradeCode, propriété</span><span class="sxs-lookup"><span data-stu-id="a8694-104">UpgradeCode property</span></span>

<span data-ttu-id="a8694-105">La propriété **UpgradeCode** est un GUID qui représente un ensemble connexe de produits.</span><span class="sxs-lookup"><span data-stu-id="a8694-105">The **UpgradeCode** property is a GUID representing a related set of products.</span></span> <span data-ttu-id="a8694-106">La fonction **UpgradeCode** est utilisée dans la [table de mise à niveau](upgrade-table.md) pour rechercher les versions associées du produit qui sont déjà installées.</span><span class="sxs-lookup"><span data-stu-id="a8694-106">The **UpgradeCode** is used in the [Upgrade Table](upgrade-table.md) to search for related versions of the product that are already installed.</span></span>

<span data-ttu-id="a8694-107">Cette propriété est utilisée par l' [action RegisterProduct](registerproduct-action.md).</span><span class="sxs-lookup"><span data-stu-id="a8694-107">This property is used by the [RegisterProduct action](registerproduct-action.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a8694-108">Notes</span><span class="sxs-lookup"><span data-stu-id="a8694-108">Remarks</span></span>

<span data-ttu-id="a8694-109">Il est fortement recommandé que les auteurs des packages d’installation spécifient une **UpgradeCode** pour leur application.</span><span class="sxs-lookup"><span data-stu-id="a8694-109">It is strongly recommended that authors of installation packages specify an **UpgradeCode** for their application.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8694-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8694-110">Requirements</span></span>



| <span data-ttu-id="a8694-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8694-111">Requirement</span></span> | <span data-ttu-id="a8694-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8694-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8694-113">Version</span><span class="sxs-lookup"><span data-stu-id="a8694-113">Version</span></span><br/> | <span data-ttu-id="a8694-114">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a8694-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a8694-115">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a8694-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a8694-116">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a8694-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a8694-117">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="a8694-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8694-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8694-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8694-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a8694-119">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="a8694-120">Correctifs et mises à niveau</span><span class="sxs-lookup"><span data-stu-id="a8694-120">Patching and Upgrades</span></span>](patching-and-upgrades.md)
</dt> <dt>

[<span data-ttu-id="a8694-121">Préparation d’une application pour les futures mises à niveau majeures</span><span class="sxs-lookup"><span data-stu-id="a8694-121">Preparing an Application for Future Major Upgrades</span></span>](preparing-an-application-for-future-major-upgrades.md)
</dt> </dl>

 

 




