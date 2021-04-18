---
description: La valeur de la propriété ProductVersion est la version du produit au format de chaîne.
ms.assetid: 551fca7e-a827-482d-bc56-ff2fe5a17025
title: Propriété ProductVersion
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01f82fcbd28c4a4132e4c3f76adfd68e33c43b36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543250"
---
# <a name="productversion-property"></a><span data-ttu-id="d6d4f-103">Propriété ProductVersion</span><span class="sxs-lookup"><span data-stu-id="d6d4f-103">ProductVersion property</span></span>

<span data-ttu-id="d6d4f-104">La valeur de la propriété **ProductVersion** est la version du produit au format de chaîne.</span><span class="sxs-lookup"><span data-stu-id="d6d4f-104">The value of the **ProductVersion** property is the version of the product in string format.</span></span> <span data-ttu-id="d6d4f-105">Cette propriété est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d6d4f-105">This property is REQUIRED.</span></span>

<span data-ttu-id="d6d4f-106">Le format de la chaîne est le suivant :</span><span class="sxs-lookup"><span data-stu-id="d6d4f-106">The format of the string is as follows:</span></span>

<dl> <span data-ttu-id="d6d4f-107">major.minor.build</span><span class="sxs-lookup"><span data-stu-id="d6d4f-107">major.minor.build</span></span>  
</dl>

<span data-ttu-id="d6d4f-108">Le premier champ est la version principale et a une valeur maximale de 255.</span><span class="sxs-lookup"><span data-stu-id="d6d4f-108">The first field is the major version and has a maximum value of 255.</span></span> <span data-ttu-id="d6d4f-109">Le deuxième champ est la version mineure et a une valeur maximale de 255.</span><span class="sxs-lookup"><span data-stu-id="d6d4f-109">The second field is the minor version and has a maximum value of 255.</span></span> <span data-ttu-id="d6d4f-110">Le troisième champ est appelé version de build ou version de mise à jour et a une valeur maximale de 65 535.</span><span class="sxs-lookup"><span data-stu-id="d6d4f-110">The third field is called the build version or the update version and has a maximum value of 65,535.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6d4f-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d6d4f-111">Remarks</span></span>

<span data-ttu-id="d6d4f-112">Au moins l’un des trois champs de **ProductVersion** doit changer pour une mise à niveau à l’aide de la [table de mise à niveau](upgrade-table.md).</span><span class="sxs-lookup"><span data-stu-id="d6d4f-112">At least one of the three fields of **ProductVersion** must change for an upgrade using the [Upgrade table](upgrade-table.md).</span></span> <span data-ttu-id="d6d4f-113">Toute mise à jour qui modifie uniquement le code du package, mais qui laisse **ProductVersion** et [**ProductCode**](productcode.md) inchangée, est appelée [petite mise à jour](small-updates.md).</span><span class="sxs-lookup"><span data-stu-id="d6d4f-113">Any update that changes only the package code, but leaves **ProductVersion** and [**ProductCode**](productcode.md) unchanged is called a [small update](small-updates.md).</span></span> <span data-ttu-id="d6d4f-114">Les champs de trois versions sont fournis principalement pour des raisons pratiques.</span><span class="sxs-lookup"><span data-stu-id="d6d4f-114">The three versions fields are provided primarily for convenience.</span></span> <span data-ttu-id="d6d4f-115">Par exemple, si vous souhaitez modifier **ProductVersion**, mais que vous ne voulez pas modifier les versions majeures ou mineures, vous pouvez modifier la version de la Build.</span><span class="sxs-lookup"><span data-stu-id="d6d4f-115">For example, if you want to change **ProductVersion**, but do not want to change either the major or minor versions, you can change the build version.</span></span>

<span data-ttu-id="d6d4f-116">Notez que Windows Installer utilise uniquement les trois premiers champs de la version du produit.</span><span class="sxs-lookup"><span data-stu-id="d6d4f-116">Note that Windows Installer uses only the first three fields of the product version.</span></span> <span data-ttu-id="d6d4f-117">Si vous incluez un quatrième champ dans la version de votre produit, le programme d’installation ignore le quatrième champ.</span><span class="sxs-lookup"><span data-stu-id="d6d4f-117">If you include a fourth field in your product version, the installer ignores the fourth field.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6d4f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6d4f-118">Requirements</span></span>



| <span data-ttu-id="d6d4f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6d4f-119">Requirement</span></span> | <span data-ttu-id="d6d4f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6d4f-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6d4f-121">Version</span><span class="sxs-lookup"><span data-stu-id="d6d4f-121">Version</span></span><br/> | <span data-ttu-id="d6d4f-122">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d6d4f-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d6d4f-123">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d6d4f-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d6d4f-124">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d6d4f-124">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d6d4f-125">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d6d4f-125">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d6d4f-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6d4f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6d4f-127">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d6d4f-127">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="d6d4f-128">Correctifs et mises à niveau</span><span class="sxs-lookup"><span data-stu-id="d6d4f-128">Patching and Upgrades</span></span>](patching-and-upgrades.md)
</dt> <dt>

[<span data-ttu-id="d6d4f-129">petite mise à jour</span><span class="sxs-lookup"><span data-stu-id="d6d4f-129">small update</span></span>](small-updates.md)
</dt> </dl>

 

 




