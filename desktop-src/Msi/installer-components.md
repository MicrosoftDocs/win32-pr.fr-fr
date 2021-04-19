---
description: La propriété composants en lecture seule retourne un objet StringList énumérant l’ensemble des composants installés pour tous les produits.
ms.assetid: c84e4329-428a-440a-bd65-097588a86932
title: Installer. Components, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Components
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6767be5182b15836c071bf8b00ed8441f6031dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526574"
---
# <a name="installercomponents-property"></a><span data-ttu-id="5d3f3-103">Installer. Components, propriété</span><span class="sxs-lookup"><span data-stu-id="5d3f3-103">Installer.Components property</span></span>

<span data-ttu-id="5d3f3-104">La propriété **composants** en lecture seule retourne un objet [**StringList**](stringlist-object.md) énumérant l’ensemble des composants installés pour tous les produits.</span><span class="sxs-lookup"><span data-stu-id="5d3f3-104">The read-only **Components** property returns a [**StringList**](stringlist-object.md) object enumerating the set of installed components for all products.</span></span>

<span data-ttu-id="5d3f3-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="5d3f3-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d3f3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d3f3-106">Syntax</span></span>


```JScript
propVal = Installer.Components
```



## <a name="property-value"></a><span data-ttu-id="5d3f3-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5d3f3-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="5d3f3-108">Notes</span><span class="sxs-lookup"><span data-stu-id="5d3f3-108">Remarks</span></span>

<span data-ttu-id="5d3f3-109">Pour énumérer les composants, une application peut itérer au sein de l’objet [**StringList**](stringlist-object.md) à l’aide d’une construction for each.</span><span class="sxs-lookup"><span data-stu-id="5d3f3-109">To enumerate the components, an application can iterate through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="5d3f3-110">Comme les composants ne sont pas triés, tous les nouveaux composants possèdent un index arbitraire.</span><span class="sxs-lookup"><span data-stu-id="5d3f3-110">Because components are not ordered, any new components has an arbitrary index.</span></span> <span data-ttu-id="5d3f3-111">Cela signifie que la fonction peut retourner des composants dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="5d3f3-111">This means that the function can return components in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d3f3-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d3f3-112">Requirements</span></span>



| <span data-ttu-id="5d3f3-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d3f3-113">Requirement</span></span> | <span data-ttu-id="5d3f3-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d3f3-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d3f3-115">Version</span><span class="sxs-lookup"><span data-stu-id="5d3f3-115">Version</span></span><br/> | <span data-ttu-id="5d3f3-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5d3f3-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5d3f3-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5d3f3-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5d3f3-118">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="5d3f3-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5d3f3-119">DLL</span><span class="sxs-lookup"><span data-stu-id="5d3f3-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="5d3f3-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d3f3-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5d3f3-121">IID</span><span class="sxs-lookup"><span data-stu-id="5d3f3-121">IID</span></span><br/>     | <span data-ttu-id="5d3f3-122">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5d3f3-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="5d3f3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d3f3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d3f3-124">**MsiEnumComponents**</span><span class="sxs-lookup"><span data-stu-id="5d3f3-124">**MsiEnumComponents**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)
</dt> </dl>

 

 




