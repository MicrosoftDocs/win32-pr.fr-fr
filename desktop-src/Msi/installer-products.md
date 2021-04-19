---
description: La propriété Products est une propriété en lecture seule qui retourne un objet StringList énumérant l’ensemble de tous les produits installés ou publiés pour l’utilisateur et l’ordinateur actuels.
ms.assetid: 5c210827-a7cc-4358-bfe6-4d8e9767bd8c
title: Installer. Products, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Products
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8d5b20a770154382e7e7a68cc3fe4d81c350fb1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520935"
---
# <a name="installerproducts-property"></a><span data-ttu-id="21d91-103">Installer. Products, propriété</span><span class="sxs-lookup"><span data-stu-id="21d91-103">Installer.Products property</span></span>

<span data-ttu-id="21d91-104">La propriété **Products** est une propriété en lecture seule qui retourne un objet [**StringList**](stringlist-object.md) énumérant l’ensemble de tous les produits installés ou publiés pour l’utilisateur et l’ordinateur actuels.</span><span class="sxs-lookup"><span data-stu-id="21d91-104">The **Products** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of all products installed or advertised for the current user and machine.</span></span>

<span data-ttu-id="21d91-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="21d91-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="21d91-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21d91-106">Syntax</span></span>


```JScript
propVal = Installer.Products
```



## <a name="property-value"></a><span data-ttu-id="21d91-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="21d91-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="21d91-108">Notes</span><span class="sxs-lookup"><span data-stu-id="21d91-108">Remarks</span></span>

<span data-ttu-id="21d91-109">Pour énumérer les produits, une application itère au sein de l’objet [**StringList**](stringlist-object.md) à l’aide d’une construction for each.</span><span class="sxs-lookup"><span data-stu-id="21d91-109">To enumerate the products, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="21d91-110">Étant donné que les produits ne sont pas triés, tous les nouveaux produits possèdent un index arbitraire.</span><span class="sxs-lookup"><span data-stu-id="21d91-110">Because products are not ordered, any new product has an arbitrary index.</span></span> <span data-ttu-id="21d91-111">Cela signifie que la fonction peut retourner des produits dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="21d91-111">This means that the function can return products in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="21d91-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21d91-112">Requirements</span></span>



| <span data-ttu-id="21d91-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21d91-113">Requirement</span></span> | <span data-ttu-id="21d91-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="21d91-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21d91-115">Version</span><span class="sxs-lookup"><span data-stu-id="21d91-115">Version</span></span><br/> | <span data-ttu-id="21d91-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="21d91-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="21d91-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="21d91-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="21d91-118">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="21d91-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="21d91-119">DLL</span><span class="sxs-lookup"><span data-stu-id="21d91-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="21d91-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21d91-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="21d91-121">IID</span><span class="sxs-lookup"><span data-stu-id="21d91-121">IID</span></span><br/>     | <span data-ttu-id="21d91-122">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="21d91-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="21d91-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21d91-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21d91-124">**MsiEnumProducts**</span><span class="sxs-lookup"><span data-stu-id="21d91-124">**MsiEnumProducts**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumproductsa)
</dt> </dl>

 

 




