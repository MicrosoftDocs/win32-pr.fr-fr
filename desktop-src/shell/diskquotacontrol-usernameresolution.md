---
description: Définit ou obtient une valeur qui contrôle le mode de résolution de l’identificateur de sécurité (SID) de l’utilisateur en noms d’utilisateurs.
title: DiskQuotaControl. UserNameResolution, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.UserNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: dc936421-e66d-4762-912a-c586f9cdace4
ms.openlocfilehash: 169f4db6e135392e9548767520f6d2b0bd2d527c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841460"
---
# <a name="diskquotacontrolusernameresolution-property"></a><span data-ttu-id="b0b7f-103">DiskQuotaControl. UserNameResolution, propriété</span><span class="sxs-lookup"><span data-stu-id="b0b7f-103">DiskQuotaControl.UserNameResolution property</span></span>

<span data-ttu-id="b0b7f-104">Définit ou obtient une valeur qui contrôle le mode de résolution de l’identificateur de sécurité (SID) de l’utilisateur en noms d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="b0b7f-104">Sets or gets a value that controls how user security identifier (SID) are resolved to user names.</span></span>

<span data-ttu-id="b0b7f-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b0b7f-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0b7f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0b7f-106">Syntax</span></span>


```JScript
iUserNameResolution = DiskQuotaControl.UserNameResolution
DiskQuotaControl.UserNameResolution = iUserNameResolution
```



## <a name="property-value"></a><span data-ttu-id="b0b7f-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b0b7f-107">Property value</span></span>

<span data-ttu-id="b0b7f-108">Cette propriété peut être définie sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b0b7f-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="b0b7f-109">Type de résolution</span><span class="sxs-lookup"><span data-stu-id="b0b7f-109">Resolution Type</span></span> | <span data-ttu-id="b0b7f-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0b7f-110">Value</span></span> | <span data-ttu-id="b0b7f-111">Description</span><span class="sxs-lookup"><span data-stu-id="b0b7f-111">Description</span></span>                                                                                                                                              |
|-----------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b7f-112">dqResolveNone</span><span class="sxs-lookup"><span data-stu-id="b0b7f-112">dqResolveNone</span></span>   | <span data-ttu-id="b0b7f-113">0</span><span class="sxs-lookup"><span data-stu-id="b0b7f-113">0</span></span>     | <span data-ttu-id="b0b7f-114">Ne résolvez pas les informations de nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b0b7f-114">Do not resolve user name information.</span></span>                                                                                                                    |
| <span data-ttu-id="b0b7f-115">dqResolveSync</span><span class="sxs-lookup"><span data-stu-id="b0b7f-115">dqResolveSync</span></span>   | <span data-ttu-id="b0b7f-116">1</span><span class="sxs-lookup"><span data-stu-id="b0b7f-116">1</span></span>     | <span data-ttu-id="b0b7f-117">Veuillez patienter pendant la résolution des informations de nom.</span><span class="sxs-lookup"><span data-stu-id="b0b7f-117">Wait while resolving name information.</span></span>                                                                                                                   |
| <span data-ttu-id="b0b7f-118">dqResolveAsync</span><span class="sxs-lookup"><span data-stu-id="b0b7f-118">dqResolveAsync</span></span>  | <span data-ttu-id="b0b7f-119">2</span><span class="sxs-lookup"><span data-stu-id="b0b7f-119">2</span></span>     | <span data-ttu-id="b0b7f-120">N’attendez pas la résolution des informations de nom.</span><span class="sxs-lookup"><span data-stu-id="b0b7f-120">Do not wait while resolving name information.</span></span> <span data-ttu-id="b0b7f-121">L’événement [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) se déclenche lorsque le nom est résolu.</span><span class="sxs-lookup"><span data-stu-id="b0b7f-121">The [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) event fires when the name is resolved.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b0b7f-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b0b7f-122">Remarks</span></span>

<span data-ttu-id="b0b7f-123">Cette propriété affecte l’énumération des objets [**DIDiskQuotaUser**](didiskquotauser-object.md) , ainsi que les méthodes [**adduser**](diskquotacontrol-adduser.md) et [**FindUser**](diskquotacontrol-finduser.md) .</span><span class="sxs-lookup"><span data-stu-id="b0b7f-123">This property affects the enumeration of [**DIDiskQuotaUser**](didiskquotauser-object.md) objects, and the [**AddUser**](diskquotacontrol-adduser.md) and [**FindUser**](diskquotacontrol-finduser.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0b7f-124">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b0b7f-124">Requirements</span></span>



| <span data-ttu-id="b0b7f-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0b7f-125">Requirement</span></span> | <span data-ttu-id="b0b7f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0b7f-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0b7f-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0b7f-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b0b7f-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0b7f-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b0b7f-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0b7f-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b0b7f-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0b7f-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b0b7f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b0b7f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0b7f-132"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="b0b7f-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0b7f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0b7f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0b7f-134">**Objet DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="b0b7f-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




