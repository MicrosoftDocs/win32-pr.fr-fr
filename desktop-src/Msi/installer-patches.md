---
description: La propriété patchs en lecture seule de l’objet installer retourne un objet StringList qui contient tous les correctifs appliqués au produit.
ms.assetid: a8d46073-399b-480e-b4b0-a7a2f832e160
title: Installer. patches, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Patches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: fd94c5853b3e455cf4d814dfb3c4078705ac727b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534860"
---
# <a name="installerpatches-property"></a><span data-ttu-id="83154-103">Installer. patches, propriété</span><span class="sxs-lookup"><span data-stu-id="83154-103">Installer.Patches property</span></span>

<span data-ttu-id="83154-104">La propriété **patchs** en lecture seule de l’objet [**installer**](installer-object.md) retourne un objet [**StringList**](stringlist-object.md) qui contient tous les correctifs appliqués au produit.</span><span class="sxs-lookup"><span data-stu-id="83154-104">The read-only **Patches** property of the [**Installer**](installer-object.md) object returns a [**StringList**](stringlist-object.md) object that contains all the patches applied to the product.</span></span>

<span data-ttu-id="83154-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="83154-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="83154-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83154-106">Syntax</span></span>


```JScript
propVal = Installer.Patches
```



## <a name="property-value"></a><span data-ttu-id="83154-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="83154-107">Property value</span></span>

<span data-ttu-id="83154-108">Spécifie le code du produit.</span><span class="sxs-lookup"><span data-stu-id="83154-108">Specifies the product code.</span></span>

## <a name="remarks"></a><span data-ttu-id="83154-109">Notes</span><span class="sxs-lookup"><span data-stu-id="83154-109">Remarks</span></span>

<span data-ttu-id="83154-110">Pour énumérer les correctifs, une application itère au sein de l’objet [**StringList**](stringlist-object.md) à l’aide d’une construction for each.</span><span class="sxs-lookup"><span data-stu-id="83154-110">To enumerate the patches, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="83154-111">Étant donné que les correctifs ne sont pas triés, les nouveaux correctifs ont un index arbitraire.</span><span class="sxs-lookup"><span data-stu-id="83154-111">Because patches are not ordered, any new patch has an arbitrary index.</span></span> <span data-ttu-id="83154-112">Cela signifie que la fonction peut retourner des correctifs dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="83154-112">This means that the function can return patches in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="83154-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83154-113">Requirements</span></span>



| <span data-ttu-id="83154-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83154-114">Requirement</span></span> | <span data-ttu-id="83154-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="83154-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83154-116">Version</span><span class="sxs-lookup"><span data-stu-id="83154-116">Version</span></span><br/> | <span data-ttu-id="83154-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="83154-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="83154-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="83154-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="83154-119">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="83154-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="83154-120">DLL</span><span class="sxs-lookup"><span data-stu-id="83154-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="83154-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83154-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="83154-122">IID</span><span class="sxs-lookup"><span data-stu-id="83154-122">IID</span></span><br/>     | <span data-ttu-id="83154-123">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="83154-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="83154-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83154-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83154-125">**MsiEnumPatches**</span><span class="sxs-lookup"><span data-stu-id="83154-125">**MsiEnumPatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> </dl>

 

 




