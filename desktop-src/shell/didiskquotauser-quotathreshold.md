---
description: Définit ou obtient le seuil d’avertissement de l’utilisateur, en octets.
ms.assetid: 5289d472-d591-4604-91f9-252dd4a1b62b
title: DIDiskQuotaUser. QuotaThreshold, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7ce336c84d086c4e4be369278a77e40e59474bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862114"
---
# <a name="didiskquotauserquotathreshold-property"></a><span data-ttu-id="a6ab7-103">DIDiskQuotaUser. QuotaThreshold, propriété</span><span class="sxs-lookup"><span data-stu-id="a6ab7-103">DIDiskQuotaUser.QuotaThreshold property</span></span>

<span data-ttu-id="a6ab7-104">Définit ou obtient le seuil d’avertissement de l’utilisateur, en octets.</span><span class="sxs-lookup"><span data-stu-id="a6ab7-104">Sets or gets the user's warning threshold, in bytes.</span></span>

<span data-ttu-id="a6ab7-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a6ab7-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6ab7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6ab7-106">Syntax</span></span>


```JScript
iQuotaThreshold = DIDiskQuotaUser.QuotaThreshold
DIDiskQuotaUser.QuotaThreshold = iQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="a6ab7-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a6ab7-107">Property value</span></span>

<span data-ttu-id="a6ab7-108">Valeur **entière** qui spécifie ou reçoit le seuil d’avertissement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a6ab7-108">An **Integer** value that specifies or receives the user's warning threshold.</span></span> <span data-ttu-id="a6ab7-109">Si l’utilisation du disque d’un utilisateur dépasse cette valeur et que la propriété [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) est définie sur **true**, le système génère une entrée de journal des événements.</span><span class="sxs-lookup"><span data-stu-id="a6ab7-109">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6ab7-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a6ab7-110">Requirements</span></span>



| <span data-ttu-id="a6ab7-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a6ab7-111">Requirement</span></span> | <span data-ttu-id="a6ab7-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="a6ab7-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ab7-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6ab7-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a6ab7-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6ab7-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a6ab7-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a6ab7-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a6ab7-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a6ab7-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a6ab7-117">DLL</span><span class="sxs-lookup"><span data-stu-id="a6ab7-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6ab7-118"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="a6ab7-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6ab7-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6ab7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ab7-120">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="a6ab7-120">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="a6ab7-121">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="a6ab7-121">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="a6ab7-122">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="a6ab7-122">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="a6ab7-123">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="a6ab7-123">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)
</dt> </dl>

 

 




