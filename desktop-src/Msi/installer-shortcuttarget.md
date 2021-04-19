---
description: La propriété ShortcutTarget de l’objet installer examine un raccourci et retourne son produit, son nom de fonctionnalité et son composant, le cas échéant.
ms.assetid: fd7a1d34-3013-4419-af92-0a0162c93494
title: Installer. ShortcutTarget, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ShortcutTarget
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1c53d43188af9ed8f58ddd54916761e346f1bad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535360"
---
# <a name="installershortcuttarget-property"></a><span data-ttu-id="97bdf-103">Installer. ShortcutTarget, propriété</span><span class="sxs-lookup"><span data-stu-id="97bdf-103">Installer.ShortcutTarget property</span></span>

<span data-ttu-id="97bdf-104">La propriété **ShortcutTarget** de l’objet [**installer**](installer-object.md) examine un raccourci et retourne son produit, son nom de fonctionnalité et son composant, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="97bdf-104">The **ShortcutTarget** property of the [**Installer**](installer-object.md) object examines a shortcut and returns its product, feature name, and component if available.</span></span>

<span data-ttu-id="97bdf-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="97bdf-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="97bdf-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97bdf-106">Syntax</span></span>


```JScript
propVal = Installer.ShortcutTarget
```



## <a name="property-value"></a><span data-ttu-id="97bdf-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="97bdf-107">Property value</span></span>

<span data-ttu-id="97bdf-108">Chemin d’accès complet et nom de fichier du fichier.</span><span class="sxs-lookup"><span data-stu-id="97bdf-108">Full path and file name for the file.</span></span>

## <a name="remarks"></a><span data-ttu-id="97bdf-109">Notes</span><span class="sxs-lookup"><span data-stu-id="97bdf-109">Remarks</span></span>

<span data-ttu-id="97bdf-110">ShortcutTarget retourne un [**objet record**](record-object.md) qui contient trois champs :</span><span class="sxs-lookup"><span data-stu-id="97bdf-110">ShortcutTarget returns a [**Record object**](record-object.md) that contains three fields:</span></span>

-   <span data-ttu-id="97bdf-111">Le champ 1 est un GUID pour le code de produit du raccourci, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="97bdf-111">Field 1 is a GUID for the product code of the shortcut, if available.</span></span> <span data-ttu-id="97bdf-112">Ce champ peut avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="97bdf-112">This field can be null.</span></span>
-   <span data-ttu-id="97bdf-113">Le champ 2 est l’ID de fonctionnalité du raccourci, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="97bdf-113">Field 2 is the Feature ID of the shortcut, if available.</span></span> <span data-ttu-id="97bdf-114">Ce champ peut avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="97bdf-114">This field can be null.</span></span>
-   <span data-ttu-id="97bdf-115">Le champ 3 est un GUID pour le code du composant, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="97bdf-115">Field 3 is a GUID for the component code, if available.</span></span> <span data-ttu-id="97bdf-116">Ce champ peut avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="97bdf-116">This field can be null.</span></span>

## <a name="requirements"></a><span data-ttu-id="97bdf-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97bdf-117">Requirements</span></span>



| <span data-ttu-id="97bdf-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97bdf-118">Requirement</span></span> | <span data-ttu-id="97bdf-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="97bdf-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97bdf-120">Version</span><span class="sxs-lookup"><span data-stu-id="97bdf-120">Version</span></span><br/> | <span data-ttu-id="97bdf-121">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="97bdf-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="97bdf-122">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="97bdf-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="97bdf-123">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="97bdf-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="97bdf-124">DLL</span><span class="sxs-lookup"><span data-stu-id="97bdf-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="97bdf-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97bdf-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="97bdf-126">IID</span><span class="sxs-lookup"><span data-stu-id="97bdf-126">IID</span></span><br/>     | <span data-ttu-id="97bdf-127">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="97bdf-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="97bdf-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97bdf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97bdf-129">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="97bdf-129">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[<span data-ttu-id="97bdf-130">**MsiGetComponentState**</span><span class="sxs-lookup"><span data-stu-id="97bdf-130">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




