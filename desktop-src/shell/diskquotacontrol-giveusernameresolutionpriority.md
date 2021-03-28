---
description: Place l’objet utilisateur spécifié en regard de la résolution de nom.
ms.assetid: 4c75f966-2e7d-4415-b1db-c98f8bdd4ce3
title: Méthode DiskQuotaControl. GiveUserNameResolutionPriority (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.GiveUserNameResolutionPriority
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1acf50e0cec59a7ee14fbd9d7760fb68b27c4de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525330"
---
# <a name="diskquotacontrolgiveusernameresolutionpriority-method"></a><span data-ttu-id="fb2f1-103">Méthode DiskQuotaControl. GiveUserNameResolutionPriority</span><span class="sxs-lookup"><span data-stu-id="fb2f1-103">DiskQuotaControl.GiveUserNameResolutionPriority method</span></span>

<span data-ttu-id="fb2f1-104">Place l’objet utilisateur spécifié en regard de la résolution de nom.</span><span class="sxs-lookup"><span data-stu-id="fb2f1-104">Places the specified user object next in line for name resolution.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb2f1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb2f1-105">Syntax</span></span>


```JScript
DiskQuotaControl.GiveUserNameResolutionPriority(
  oUser
)
```



## <a name="parameters"></a><span data-ttu-id="fb2f1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb2f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb2f1-107">*oUser*</span><span class="sxs-lookup"><span data-stu-id="fb2f1-107">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="fb2f1-108">Type : **Object**</span><span class="sxs-lookup"><span data-stu-id="fb2f1-108">Type: **Object**</span></span>

<span data-ttu-id="fb2f1-109">Expression d’objet qui prend la valeur de l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fb2f1-109">An object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb2f1-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb2f1-110">Return value</span></span>

<span data-ttu-id="fb2f1-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fb2f1-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb2f1-112">Notes</span><span class="sxs-lookup"><span data-stu-id="fb2f1-112">Remarks</span></span>

<span data-ttu-id="fb2f1-113">Si la résolution de noms asynchrone est activée, les objets utilisateur sont placés dans une file d’attente.</span><span class="sxs-lookup"><span data-stu-id="fb2f1-113">If asynchronous name resolution is enabled, user objects are placed in a queue.</span></span> <span data-ttu-id="fb2f1-114">Par défaut, elles sont desservies dans l’ordre dans lequel elles sont placées dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="fb2f1-114">By default, they are serviced in the order they are placed in the queue.</span></span> <span data-ttu-id="fb2f1-115">La méthode **GiveUserNameResolutionPriority** déplace un objet au début de la file d’attente afin qu’il soit en ligne à traiter.</span><span class="sxs-lookup"><span data-stu-id="fb2f1-115">The **GiveUserNameResolutionPriority** method moves an object to the front of the queue so that it is next in line to be serviced.</span></span>

<span data-ttu-id="fb2f1-116">Utilisez la propriété [**UserNameResolution**](diskquotacontrol-usernameresolution.md) pour activer la résolution de noms asynchrone.</span><span class="sxs-lookup"><span data-stu-id="fb2f1-116">Use the [**UserNameResolution**](diskquotacontrol-usernameresolution.md) property to enable asynchronous name resolution.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb2f1-117">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fb2f1-117">Requirements</span></span>



| <span data-ttu-id="fb2f1-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb2f1-118">Requirement</span></span> | <span data-ttu-id="fb2f1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb2f1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb2f1-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb2f1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fb2f1-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb2f1-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fb2f1-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb2f1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fb2f1-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb2f1-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fb2f1-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb2f1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb2f1-125"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb2f1-125"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="fb2f1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="fb2f1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb2f1-127"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="fb2f1-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb2f1-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb2f1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb2f1-129">**Objet DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="fb2f1-129">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




