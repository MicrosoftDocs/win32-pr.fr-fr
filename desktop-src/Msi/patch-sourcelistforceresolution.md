---
description: La méthode SourceListForceResolution efface la dernière propriété source utilisée.
ms.assetid: 9ecfdf6e-4fed-46fc-8956-85d20cbe5327
title: Méthode patch. SourceListForceResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListForceResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f9a44d08c05b4ece24cf3c8c8d3be42e210aec32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525396"
---
# <a name="patchsourcelistforceresolution-method"></a><span data-ttu-id="90e70-103">Méthode patch. SourceListForceResolution</span><span class="sxs-lookup"><span data-stu-id="90e70-103">Patch.SourceListForceResolution method</span></span>

<span data-ttu-id="90e70-104">La méthode **SourceListForceResolution** efface la dernière propriété source utilisée.</span><span class="sxs-lookup"><span data-stu-id="90e70-104">The **SourceListForceResolution** method clears the last used source property.</span></span> <span data-ttu-id="90e70-105">Cela oblige le programme d’installation à rechercher dans la liste source une source de correctif valide la prochaine fois que la source du correctif est requise.</span><span class="sxs-lookup"><span data-stu-id="90e70-105">This forces the installer to search the source list for a valid patch source the next time the patch source is required.</span></span> <span data-ttu-id="90e70-106">Par exemple, le programme d’installation requiert la source du correctif pour effectuer une installation ou une réinstallation lorsque la copie du cache local du correctif est manquante.</span><span class="sxs-lookup"><span data-stu-id="90e70-106">For example, the installer requires the patch source to perform an installation or reinstallation when the local cache copy of the patch is missing.</span></span> <span data-ttu-id="90e70-107">Cette méthode appelle [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span><span class="sxs-lookup"><span data-stu-id="90e70-107">This method calls [**MsiSourceListForceResolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona).</span></span>

## <a name="syntax"></a><span data-ttu-id="90e70-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90e70-108">Syntax</span></span>


```JScript
Patch.SourceListForceResolution()
```



## <a name="parameters"></a><span data-ttu-id="90e70-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90e70-109">Parameters</span></span>

<span data-ttu-id="90e70-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="90e70-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="90e70-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="90e70-111">Return value</span></span>

<span data-ttu-id="90e70-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="90e70-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="90e70-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="90e70-113">Requirements</span></span>



| <span data-ttu-id="90e70-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="90e70-114">Requirement</span></span> | <span data-ttu-id="90e70-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="90e70-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90e70-116">Version</span><span class="sxs-lookup"><span data-stu-id="90e70-116">Version</span></span><br/> | <span data-ttu-id="90e70-117">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="90e70-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="90e70-118">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="90e70-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="90e70-119">Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000</span><span class="sxs-lookup"><span data-stu-id="90e70-119">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="90e70-120">DLL</span><span class="sxs-lookup"><span data-stu-id="90e70-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="90e70-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90e70-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="90e70-122">IID</span><span class="sxs-lookup"><span data-stu-id="90e70-122">IID</span></span><br/>     | <span data-ttu-id="90e70-123">IID \_ IPatch est défini en tant que 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="90e70-123">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="90e70-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90e70-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90e70-125">**Correctif**</span><span class="sxs-lookup"><span data-stu-id="90e70-125">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="90e70-126">**MsiSourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="90e70-126">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="90e70-127">Non pris en charge dans Windows Installer 2,0 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="90e70-127">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




