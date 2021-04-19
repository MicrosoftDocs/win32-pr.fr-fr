---
description: La propriété ProductInfo est une propriété en lecture seule qui retourne la valeur de l’attribut spécifié pour un produit installé ou publié.
ms.assetid: 144cbba7-ec2b-44cd-acc8-868c210ccebd
title: Installer. ProductInfo, propriété (Oemupgex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 03ad741dd1c92fe68caccc4582738e54032750e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545665"
---
# <a name="installerproductinfo-property"></a><span data-ttu-id="09b85-103">Installer. ProductInfo, propriété</span><span class="sxs-lookup"><span data-stu-id="09b85-103">Installer.ProductInfo property</span></span>

<span data-ttu-id="09b85-104">La propriété **ProductInfo** est une propriété en lecture seule qui retourne la valeur de l’attribut spécifié pour un produit installé ou publié.</span><span class="sxs-lookup"><span data-stu-id="09b85-104">The **ProductInfo** property is a read-only property that returns the value of the specified attribute for an installed or published product.</span></span>

<span data-ttu-id="09b85-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="09b85-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="09b85-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09b85-106">Syntax</span></span>


```JScript
propVal = Installer.ProductInfo
```



## <a name="property-value"></a><span data-ttu-id="09b85-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="09b85-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="09b85-108">Notes</span><span class="sxs-lookup"><span data-stu-id="09b85-108">Remarks</span></span>

<span data-ttu-id="09b85-109">La propriété **ProductInfo** (« LocalPackage ») ne retourne pas nécessairement un chemin d’accès au package mis en cache.</span><span class="sxs-lookup"><span data-stu-id="09b85-109">The **ProductInfo** property ("LocalPackage") does not necessarily return a path to the cached package.</span></span> <span data-ttu-id="09b85-110">Les installations en mode maintenance ne doivent pas être appelées à partir du LocalPackage.</span><span class="sxs-lookup"><span data-stu-id="09b85-110">Maintenance mode installations should be not be invoked from the LocalPackage.</span></span> <span data-ttu-id="09b85-111">Le package mis en cache est réservé aux utilisations internes.</span><span class="sxs-lookup"><span data-stu-id="09b85-111">The cached package is for internal uses only.</span></span>

## <a name="requirements"></a><span data-ttu-id="09b85-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09b85-112">Requirements</span></span>



| <span data-ttu-id="09b85-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09b85-113">Requirement</span></span> | <span data-ttu-id="09b85-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="09b85-114">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09b85-115">Version</span><span class="sxs-lookup"><span data-stu-id="09b85-115">Version</span></span><br/> | <span data-ttu-id="09b85-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="09b85-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="09b85-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="09b85-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="09b85-118">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="09b85-118">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="09b85-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="09b85-119">Header</span></span><br/>  | <dl> <span data-ttu-id="09b85-120"><dt>Oemupgex. h</dt></span><span class="sxs-lookup"><span data-stu-id="09b85-120"><dt>Oemupgex.h</dt></span></span> </dl>                                                                                                                                                                                 |
| <span data-ttu-id="09b85-121">DLL</span><span class="sxs-lookup"><span data-stu-id="09b85-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="09b85-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09b85-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="09b85-123">IID</span><span class="sxs-lookup"><span data-stu-id="09b85-123">IID</span></span><br/>     | <span data-ttu-id="09b85-124">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="09b85-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="09b85-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09b85-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09b85-126">**MsiGetProductInfo**</span><span class="sxs-lookup"><span data-stu-id="09b85-126">**MsiGetProductInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[<span data-ttu-id="09b85-127">**MsiGetUserInfo**</span><span class="sxs-lookup"><span data-stu-id="09b85-127">**MsiGetUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)
</dt> <dt>

[<span data-ttu-id="09b85-128">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="09b85-128">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




