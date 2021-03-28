---
description: Se produit lorsque les informations de nom d’un objet DIDiskQuotaUser ont été résolues.
ms.assetid: df32cb17-ad90-4535-a36b-60c5b4e9999f
title: OnUserNameChanged, fonction (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnUserNameChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 98906f281c6c93a64754c1aa5cecfc6624599c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319550"
---
# <a name="onusernamechanged-function"></a><span data-ttu-id="992c4-103">OnUserNameChanged fonction)</span><span class="sxs-lookup"><span data-stu-id="992c4-103">OnUserNameChanged function</span></span>

<span data-ttu-id="992c4-104">Se produit lorsque les informations de nom d’un objet [**DIDiskQuotaUser**](didiskquotauser-object.md) ont été résolues.</span><span class="sxs-lookup"><span data-stu-id="992c4-104">Occurs when the name information for a [**DIDiskQuotaUser**](didiskquotauser-object.md) object has been resolved.</span></span>

## <a name="parameters"></a><span data-ttu-id="992c4-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="992c4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="992c4-106">*oUser*</span><span class="sxs-lookup"><span data-stu-id="992c4-106">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="992c4-107">**Objet** qui prend la valeur de l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) associé à l’utilisateur dont le nom a été résolu.</span><span class="sxs-lookup"><span data-stu-id="992c4-107">The **Object** that evaluates to the [**DIDiskQuotaUser**](didiskquotauser-object.md) object associated with the user whose name has been resolved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="992c4-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="992c4-108">Return value</span></span>

<span data-ttu-id="992c4-109">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="992c4-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="992c4-110">Notes</span><span class="sxs-lookup"><span data-stu-id="992c4-110">Remarks</span></span>

<span data-ttu-id="992c4-111">Lorsqu’un client [**énumère des utilisateurs**](didiskquotauser-object.md)ou appelle la méthode [**adduser**](diskquotacontrol-adduser.md) ou [**FindUser**](diskquotacontrol-finduser.md) , le nom d’utilisateur doit être résolu à l’ID de sécurité (SID) associé.</span><span class="sxs-lookup"><span data-stu-id="992c4-111">When a client [**enumerates users**](didiskquotauser-object.md), or calls the [**AddUser**](diskquotacontrol-adduser.md) or [**FindUser**](diskquotacontrol-finduser.md) method, the user name must be resolved to the associated security ID (SID).</span></span> <span data-ttu-id="992c4-112">Étant donné que cette procédure peut prendre du temps, la résolution de noms peut être effectuée de façon asynchrone sur un thread d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="992c4-112">Because this procedure can be time-consuming, a client can have name resolution done asynchronously on a background thread.</span></span> <span data-ttu-id="992c4-113">Lorsque le nom d’un utilisateur est résolu, l’objet [**DiskQuotaControl**](diskquotacontrol-object.md) avertit son client en déclenchant l’événement **OnUserNameChanged** .</span><span class="sxs-lookup"><span data-stu-id="992c4-113">When a user's name is resolved, the [**DiskQuotaControl**](diskquotacontrol-object.md) object notifies its client by firing the **OnUserNameChanged** event.</span></span> <span data-ttu-id="992c4-114">Un objet **DIDiskQuotaUser** associé à l’utilisateur est passé en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="992c4-114">A **DIDiskQuotaUser** object associated with the user is passed as a parameter.</span></span> <span data-ttu-id="992c4-115">Cet objet permet au client de modifier les paramètres de quota de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="992c4-115">This object allows the client to modify the user's quota settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="992c4-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="992c4-116">Requirements</span></span>



| <span data-ttu-id="992c4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="992c4-117">Requirement</span></span> | <span data-ttu-id="992c4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="992c4-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="992c4-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="992c4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="992c4-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="992c4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="992c4-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="992c4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="992c4-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="992c4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="992c4-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="992c4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="992c4-124"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="992c4-124"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="992c4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="992c4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="992c4-126"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="992c4-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="992c4-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="992c4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="992c4-128">**Objet DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="992c4-128">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




