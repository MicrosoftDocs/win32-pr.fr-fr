---
description: Supprime un utilisateur du volume.
ms.assetid: 56a07388-b7d8-41a4-b29a-8a57fe0b9d19
title: DiskQuotaControl. DeleteUser, méthode (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DeleteUser
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c159375727ef115631a8a047d69ce235a5b8f2a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201264"
---
# <a name="diskquotacontroldeleteuser-method"></a><span data-ttu-id="63581-103">DiskQuotaControl. DeleteUser, méthode</span><span class="sxs-lookup"><span data-stu-id="63581-103">DiskQuotaControl.DeleteUser method</span></span>

<span data-ttu-id="63581-104">Supprime un utilisateur du volume.</span><span class="sxs-lookup"><span data-stu-id="63581-104">Deletes a user from the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="63581-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63581-105">Syntax</span></span>


```JScript
DiskQuotaControl.DeleteUser(
  oUser
)
```



## <a name="parameters"></a><span data-ttu-id="63581-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="63581-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63581-107">*oUser*</span><span class="sxs-lookup"><span data-stu-id="63581-107">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="63581-108">Type : **Object**</span><span class="sxs-lookup"><span data-stu-id="63581-108">Type: **Object**</span></span>

<span data-ttu-id="63581-109">Expression d’objet qui prend la valeur de l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="63581-109">An object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63581-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="63581-110">Return value</span></span>

<span data-ttu-id="63581-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="63581-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="63581-112">Notes</span><span class="sxs-lookup"><span data-stu-id="63581-112">Remarks</span></span>

<span data-ttu-id="63581-113">Cette méthode échoue si l’utilisateur possède un stockage sur le volume.</span><span class="sxs-lookup"><span data-stu-id="63581-113">This method fails if the user owns any storage on the volume.</span></span> <span data-ttu-id="63581-114">Avant de supprimer un utilisateur d’un volume, tout le stockage de cet utilisateur doit être supprimé, déplacé vers un autre volume ou une propriété est transférée à un autre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="63581-114">Before you delete a user from a volume, all storage for that user must be deleted, be moved to another volume, or have its ownership transferred to another user.</span></span>

## <a name="requirements"></a><span data-ttu-id="63581-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="63581-115">Requirements</span></span>



| <span data-ttu-id="63581-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63581-116">Requirement</span></span> | <span data-ttu-id="63581-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="63581-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63581-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63581-118">Minimum supported client</span></span><br/> | <span data-ttu-id="63581-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63581-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="63581-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63581-120">Minimum supported server</span></span><br/> | <span data-ttu-id="63581-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="63581-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="63581-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="63581-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="63581-123"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="63581-123"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="63581-124">DLL</span><span class="sxs-lookup"><span data-stu-id="63581-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63581-125"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="63581-125"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63581-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63581-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63581-127">**AddUser**</span><span class="sxs-lookup"><span data-stu-id="63581-127">**AddUser**</span></span>](diskquotacontrol-adduser.md)
</dt> <dt>

[<span data-ttu-id="63581-128">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="63581-128">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




