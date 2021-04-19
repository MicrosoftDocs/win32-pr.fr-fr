---
description: La propriété features est une propriété en lecture seule qui retourne un objet StringList énumérant l’ensemble des fonctionnalités publiées pour le produit spécifié.
ms.assetid: feb8f09a-fa97-4fee-9082-8f04288af22f
title: Installer. Features, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Features
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4f63ce80249fb8bd24d70f92e72c44420a13d798
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528616"
---
# <a name="installerfeatures-property"></a><span data-ttu-id="9ca84-103">Installer. Features, propriété</span><span class="sxs-lookup"><span data-stu-id="9ca84-103">Installer.Features property</span></span>

<span data-ttu-id="9ca84-104">La propriété **features** est une propriété en lecture seule qui retourne un objet [**StringList**](stringlist-object.md) énumérant l’ensemble des fonctionnalités publiées pour le produit spécifié.</span><span class="sxs-lookup"><span data-stu-id="9ca84-104">The **Features** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of published features for the specified product.</span></span>

<span data-ttu-id="9ca84-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9ca84-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ca84-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ca84-106">Syntax</span></span>


```JScript
propVal = Installer.Features
```



## <a name="property-value"></a><span data-ttu-id="9ca84-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="9ca84-107">Property value</span></span>

<span data-ttu-id="9ca84-108">Spécifie le code de produit du produit.</span><span class="sxs-lookup"><span data-stu-id="9ca84-108">Specifies the product code of the product.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ca84-109">Notes</span><span class="sxs-lookup"><span data-stu-id="9ca84-109">Remarks</span></span>

<span data-ttu-id="9ca84-110">Pour énumérer les fonctionnalités, une application itère au sein de l’objet [**StringList**](stringlist-object.md) à l’aide d’une construction for each.</span><span class="sxs-lookup"><span data-stu-id="9ca84-110">To enumerate the features, an application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="9ca84-111">Étant donné que les fonctionnalités ne sont pas ordonnées, toutes les nouvelles fonctionnalités ont un index arbitraire, ce qui signifie que la fonction peut retourner des fonctionnalités dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="9ca84-111">Because features are not ordered, any new feature has an arbitrary index, meaning the function can return features in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ca84-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ca84-112">Requirements</span></span>



| <span data-ttu-id="9ca84-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ca84-113">Requirement</span></span> | <span data-ttu-id="9ca84-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ca84-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ca84-115">Version</span><span class="sxs-lookup"><span data-stu-id="9ca84-115">Version</span></span><br/> | <span data-ttu-id="9ca84-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9ca84-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9ca84-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9ca84-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9ca84-118">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="9ca84-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="9ca84-119">DLL</span><span class="sxs-lookup"><span data-stu-id="9ca84-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="9ca84-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ca84-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="9ca84-121">IID</span><span class="sxs-lookup"><span data-stu-id="9ca84-121">IID</span></span><br/>     | <span data-ttu-id="9ca84-122">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9ca84-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="9ca84-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ca84-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ca84-124">**MsiEnumFeatures**</span><span class="sxs-lookup"><span data-stu-id="9ca84-124">**MsiEnumFeatures**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)
</dt> <dt>

[<span data-ttu-id="9ca84-125">Fonctions d’État du système</span><span class="sxs-lookup"><span data-stu-id="9ca84-125">System Status Functions</span></span>](installer-function-reference.md)
</dt> </dl>

 

 




