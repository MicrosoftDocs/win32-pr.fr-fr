---
description: La propriété ComponentQualifiers est une propriété en lecture seule qui retourne un objet StringList énumérant l’ensemble des qualificateurs inscrits pour le composant spécifié.
ms.assetid: 49b16c9a-ce84-42ff-af1d-f4ecf7dbe23a
title: Installer. ComponentQualifiers, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentQualifiers
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e6f58850974eaa2021578f0d56015ea0ef6d9e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523651"
---
# <a name="installercomponentqualifiers-property"></a><span data-ttu-id="e83f9-103">Installer. ComponentQualifiers, propriété</span><span class="sxs-lookup"><span data-stu-id="e83f9-103">Installer.ComponentQualifiers property</span></span>

<span data-ttu-id="e83f9-104">La propriété **ComponentQualifiers** est une propriété en lecture seule qui retourne un objet [**StringList**](stringlist-object.md) énumérant l’ensemble des qualificateurs inscrits pour le composant spécifié.</span><span class="sxs-lookup"><span data-stu-id="e83f9-104">The **ComponentQualifiers** property is a read-only property that returns a [**StringList**](stringlist-object.md) object enumerating the set of registered qualifiers for the specified component.</span></span>

<span data-ttu-id="e83f9-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="e83f9-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e83f9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e83f9-106">Syntax</span></span>


```JScript
propVal = Installer.ComponentQualifiers
```



## <a name="property-value"></a><span data-ttu-id="e83f9-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="e83f9-107">Property value</span></span>

<span data-ttu-id="e83f9-108">GUID de chaîne qui représente la catégorie du [composant](publishcomponent-table.md).</span><span class="sxs-lookup"><span data-stu-id="e83f9-108">A string GUID that represents the category of [component](publishcomponent-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e83f9-109">Notes</span><span class="sxs-lookup"><span data-stu-id="e83f9-109">Remarks</span></span>

<span data-ttu-id="e83f9-110">Pour énumérer les qualificateurs, l’application itère au sein de l’objet [**StringList**](stringlist-object.md) à l’aide d’une construction for each.</span><span class="sxs-lookup"><span data-stu-id="e83f9-110">To enumerate qualifiers the application iterates through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="e83f9-111">Étant donné que les qualificateurs ne sont pas triés, tout nouveau qualificateur a un index arbitraire, ce qui signifie que la fonction peut retourner des qualificateurs dans n’importe quel ordre.</span><span class="sxs-lookup"><span data-stu-id="e83f9-111">Because qualifiers are not ordered, any new qualifier has an arbitrary index, meaning the function can return qualifiers in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="e83f9-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e83f9-112">Requirements</span></span>



| <span data-ttu-id="e83f9-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e83f9-113">Requirement</span></span> | <span data-ttu-id="e83f9-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="e83f9-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e83f9-115">Version</span><span class="sxs-lookup"><span data-stu-id="e83f9-115">Version</span></span><br/> | <span data-ttu-id="e83f9-116">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e83f9-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e83f9-117">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e83f9-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e83f9-118">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="e83f9-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e83f9-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e83f9-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="e83f9-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e83f9-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e83f9-121">IID</span><span class="sxs-lookup"><span data-stu-id="e83f9-121">IID</span></span><br/>     | <span data-ttu-id="e83f9-122">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e83f9-122">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="e83f9-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e83f9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e83f9-124">**MsiEnumComponentQualifiers**</span><span class="sxs-lookup"><span data-stu-id="e83f9-124">**MsiEnumComponentQualifiers**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> </dl>

 

 




