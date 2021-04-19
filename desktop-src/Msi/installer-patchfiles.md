---
description: La propriété PatchFiles retourne un objet StringList qui contient une liste de fichiers qui peuvent être mis à jour par la liste de correctifs fournie.
ms.assetid: 14549847-8558-4a9a-9ad5-3575c3f4391e
title: Installer. PatchFiles, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.PatchFiles
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 43491bb384e6f95b31b4e7ae12e5fd32f4fbe8b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531116"
---
# <a name="installerpatchfiles-property"></a><span data-ttu-id="ba6fd-103">Installer. PatchFiles, propriété</span><span class="sxs-lookup"><span data-stu-id="ba6fd-103">Installer.PatchFiles property</span></span>

<span data-ttu-id="ba6fd-104">La propriété **PatchFiles** retourne un objet [**StringList**](stringlist-object.md) qui contient une liste de fichiers qui peuvent être mis à jour par la liste de correctifs fournie.</span><span class="sxs-lookup"><span data-stu-id="ba6fd-104">The **PatchFiles** property returns a [**StringList**](stringlist-object.md) object that contains a list of files that can be updated by the provided list of patches.</span></span> <span data-ttu-id="ba6fd-105">Cette propriété appelle [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista).</span><span class="sxs-lookup"><span data-stu-id="ba6fd-105">This property calls [**MsiGetPatchFileList**](/windows/desktop/api/Msi/nf-msi-msigetpatchfilelista).</span></span> <span data-ttu-id="ba6fd-106">Pour plus d’informations sur l’utilisation de la propriété **PatchFiles** [, consultez Liste des fichiers qui peuvent être mis à jour](listing-the-files-that-can-be-updated.md).</span><span class="sxs-lookup"><span data-stu-id="ba6fd-106">For more information about using the **PatchFiles** property see [Listing the Files that can be Updated](listing-the-files-that-can-be-updated.md).</span></span>

<span data-ttu-id="ba6fd-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ba6fd-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba6fd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba6fd-108">Syntax</span></span>


```JScript
propVal = Installer.PatchFiles
```



## <a name="property-value"></a><span data-ttu-id="ba6fd-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ba6fd-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="ba6fd-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba6fd-110">Requirements</span></span>



| <span data-ttu-id="ba6fd-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba6fd-111">Requirement</span></span> | <span data-ttu-id="ba6fd-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba6fd-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba6fd-113">Version</span><span class="sxs-lookup"><span data-stu-id="ba6fd-113">Version</span></span><br/> | <span data-ttu-id="ba6fd-114">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ba6fd-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ba6fd-115">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ba6fd-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ba6fd-116">Windows Installer 4,5 sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="ba6fd-116">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="ba6fd-117">DLL</span><span class="sxs-lookup"><span data-stu-id="ba6fd-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="ba6fd-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba6fd-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="ba6fd-119">IID</span><span class="sxs-lookup"><span data-stu-id="ba6fd-119">IID</span></span><br/>     | <span data-ttu-id="ba6fd-120">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="ba6fd-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="ba6fd-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba6fd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba6fd-122">**Objet installer**</span><span class="sxs-lookup"><span data-stu-id="ba6fd-122">**Installer Object**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="ba6fd-123">Non pris en charge dans Windows Installer 3,1 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="ba6fd-123">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




