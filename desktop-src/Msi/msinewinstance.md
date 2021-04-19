---
description: La propriété MSINEWINSTANCE indique l’installation d’une nouvelle instance d’un produit avec des transformations d’instance.
ms.assetid: 35d41fa9-79d3-4baa-b177-5a32239b5051
title: Propriété MSINEWINSTANCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8b51ec02d7b30c42e6e400b6a6177d7ef47d88c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542651"
---
# <a name="msinewinstance-property"></a><span data-ttu-id="392ed-103">Propriété MSINEWINSTANCE</span><span class="sxs-lookup"><span data-stu-id="392ed-103">MSINEWINSTANCE property</span></span>

<span data-ttu-id="392ed-104">La propriété **MSINEWINSTANCE** indique l’installation d’une nouvelle instance d’un produit avec des transformations d’instance.</span><span class="sxs-lookup"><span data-stu-id="392ed-104">The **MSINEWINSTANCE** property indicates the installation of a new instance of a product with instance transforms.</span></span> <span data-ttu-id="392ed-105">Cette propriété prend en charge plusieurs instances par le biais du code de produit – modification des transformations.</span><span class="sxs-lookup"><span data-stu-id="392ed-105">This property supports multiple instances through product code–changing transforms.</span></span> <span data-ttu-id="392ed-106">La valeur de cette propriété est 1.</span><span class="sxs-lookup"><span data-stu-id="392ed-106">The value of this property is 1.</span></span> <span data-ttu-id="392ed-107">La présence de cette propriété sur la ligne de commande nécessite que la propriété [**TRANSformations**](transforms.md) soit également présente.</span><span class="sxs-lookup"><span data-stu-id="392ed-107">The presence of this property on the command line requires that the [**TRANSFORMS**](transforms.md) property also be present.</span></span> <span data-ttu-id="392ed-108">La première transformation figurant dans **TRANSformations** doit être une transformation d’instance.</span><span class="sxs-lookup"><span data-stu-id="392ed-108">The first transform listed in **TRANSFORMS** must be an instance transform.</span></span> <span data-ttu-id="392ed-109">Pour plus d’informations, consultez [installation de plusieurs instances de produits et correctifs](installing-multiple-instances-of-products-and-patches.md)</span><span class="sxs-lookup"><span data-stu-id="392ed-109">For more information see, [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md)</span></span>

<span data-ttu-id="392ed-110">Cette propriété est disponible avec le programme d’installation qui exécute un système dans Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="392ed-110">This property is available with the installer running a system in the Windows Server 2003 or Windows XP.</span></span>

## <a name="requirements"></a><span data-ttu-id="392ed-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="392ed-111">Requirements</span></span>



| <span data-ttu-id="392ed-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="392ed-112">Requirement</span></span> | <span data-ttu-id="392ed-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="392ed-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="392ed-114">Version</span><span class="sxs-lookup"><span data-stu-id="392ed-114">Version</span></span><br/> | <span data-ttu-id="392ed-115">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="392ed-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="392ed-116">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="392ed-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="392ed-117">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="392ed-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="392ed-118">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="392ed-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="392ed-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="392ed-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="392ed-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="392ed-120">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="392ed-121">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="392ed-121">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




