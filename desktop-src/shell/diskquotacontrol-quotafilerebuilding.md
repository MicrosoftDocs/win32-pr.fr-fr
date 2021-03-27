---
description: Obtient une valeur booléenne qui indique si le fichier de quota du volume est en cours de reconstruction.
ms.assetid: 66a6bafe-bda4-41b3-9207-2ea6b8e63835
title: DiskQuotaControl. QuotaFileRebuilding, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaFileRebuilding
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e06b73e53670a136e53721b4e6bc6b2f635d601b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972123"
---
# <a name="diskquotacontrolquotafilerebuilding-property"></a><span data-ttu-id="d6534-103">DiskQuotaControl. QuotaFileRebuilding, propriété</span><span class="sxs-lookup"><span data-stu-id="d6534-103">DiskQuotaControl.QuotaFileRebuilding property</span></span>

<span data-ttu-id="d6534-104">Obtient une valeur booléenne qui indique si le fichier de quota du volume est en cours de reconstruction.</span><span class="sxs-lookup"><span data-stu-id="d6534-104">Gets a Boolean value that indicates whether the quota file for the volume is currently being rebuilt.</span></span>

<span data-ttu-id="d6534-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="d6534-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6534-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6534-106">Syntax</span></span>


```JScript
bQuotaFileRebuilding = DiskQuotaControl.QuotaFileRebuilding
```



## <a name="property-value"></a><span data-ttu-id="d6534-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d6534-107">Property value</span></span>

<span data-ttu-id="d6534-108">Cette propriété a la valeur **true** si le fichier de quota est en cours de reconstruction, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d6534-108">This property is set to **TRUE** if the quota file is being rebuilt, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6534-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d6534-109">Remarks</span></span>

<span data-ttu-id="d6534-110">Le fichier de quota est automatiquement régénéré lorsque les quotas sont activés sur le système ou lorsqu’une ou plusieurs entrées utilisateur sont marquées pour suppression.</span><span class="sxs-lookup"><span data-stu-id="d6534-110">The quota file is automatically rebuilt when quotas are enabled on the system or when one or more user entries are marked for deletion.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6534-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="d6534-111">Requirements</span></span>



| <span data-ttu-id="d6534-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6534-112">Requirement</span></span> | <span data-ttu-id="d6534-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6534-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6534-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6534-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d6534-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6534-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d6534-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6534-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d6534-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6534-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d6534-118">DLL</span><span class="sxs-lookup"><span data-stu-id="d6534-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6534-119"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="d6534-119"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6534-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6534-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6534-121">**Objet DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="d6534-121">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




