---
description: La propriété RelatedProducts en lecture seule retourne un objet StringList énumérant l’ensemble de tous les produits installés ou publiés pour l’utilisateur et l’ordinateur actuels avec une propriété UpgradeCode spécifiée dans leur table de propriétés.
ms.assetid: 0316e536-ccd4-4d7a-9c49-66e6c4a07f1c
title: Installer. RelatedProducts, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RelatedProducts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fb30be6ea5250a90ef8aa18065e9be679946e503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540043"
---
# <a name="installerrelatedproducts-property"></a><span data-ttu-id="3a244-103">Installer. RelatedProducts, propriété</span><span class="sxs-lookup"><span data-stu-id="3a244-103">Installer.RelatedProducts property</span></span>

<span data-ttu-id="3a244-104">La propriété **RelatedProducts** en lecture seule retourne un objet [**StringList**](stringlist-object.md) énumérant l’ensemble de tous les produits installés ou publiés pour l’utilisateur et l’ordinateur actuels avec une propriété [**UpgradeCode**](upgradecode.md) spécifiée dans leur table de [Propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="3a244-104">The read-only **RelatedProducts** property returns a [**StringList**](stringlist-object.md) object enumerating the set of all products installed or advertised for the current user and machine with a specified [**UpgradeCode**](upgradecode.md) property in their [Property table](property-table.md).</span></span>

<span data-ttu-id="3a244-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3a244-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a244-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a244-106">Syntax</span></span>


```JScript
propVal = Installer.RelatedProducts
```



## <a name="property-value"></a><span data-ttu-id="3a244-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3a244-107">Property value</span></span>

<span data-ttu-id="3a244-108">Code de mise à niveau des produits connexes que le programme d’installation énumère.</span><span class="sxs-lookup"><span data-stu-id="3a244-108">The upgrade code of related products that the installer enumerates.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a244-109">Notes</span><span class="sxs-lookup"><span data-stu-id="3a244-109">Remarks</span></span>

<span data-ttu-id="3a244-110">Pour énumérer les produits connexes, une application itère au sein du [**StringList**](stringlist-object.md) à l’aide d’une construction for each.</span><span class="sxs-lookup"><span data-stu-id="3a244-110">To enumerate the related products, an application iterates through the [**StringList**](stringlist-object.md) using a For Each construct.</span></span> <span data-ttu-id="3a244-111">Étant donné que les produits associés ne sont pas triés, tous les nouveaux produits associés possèdent un index arbitraire.</span><span class="sxs-lookup"><span data-stu-id="3a244-111">Because related products are not ordered, any new related product has an arbitrary index.</span></span> <span data-ttu-id="3a244-112">Cela signifie que la fonction peut retourner des produits connexes dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="3a244-112">This means that the function can return related products in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a244-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3a244-113">Requirements</span></span>



| <span data-ttu-id="3a244-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3a244-114">Requirement</span></span> | <span data-ttu-id="3a244-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3a244-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a244-116">Version</span><span class="sxs-lookup"><span data-stu-id="3a244-116">Version</span></span><br/> | <span data-ttu-id="3a244-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3a244-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3a244-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3a244-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3a244-119">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="3a244-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3a244-120">DLL</span><span class="sxs-lookup"><span data-stu-id="3a244-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="3a244-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a244-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3a244-122">IID</span><span class="sxs-lookup"><span data-stu-id="3a244-122">IID</span></span><br/>     | <span data-ttu-id="3a244-123">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3a244-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="3a244-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3a244-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a244-125">**MsiEnumRelatedProducts**</span><span class="sxs-lookup"><span data-stu-id="3a244-125">**MsiEnumRelatedProducts**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumrelatedproductsa)
</dt> </dl>

 

 




