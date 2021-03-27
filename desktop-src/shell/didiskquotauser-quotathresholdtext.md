---
description: Obtient le seuil d’avertissement de l’utilisateur sous la forme d’une chaîne de texte.
ms.assetid: 55b53ad0-e7cd-4417-9087-297ac96e245f
title: DIDiskQuotaUser. QuotaThresholdText, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 511829233b93dbe164ce2feccd1247ccebf3ec3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971982"
---
# <a name="didiskquotauserquotathresholdtext-property"></a><span data-ttu-id="3820f-103">DIDiskQuotaUser. QuotaThresholdText, propriété</span><span class="sxs-lookup"><span data-stu-id="3820f-103">DIDiskQuotaUser.QuotaThresholdText property</span></span>

<span data-ttu-id="3820f-104">Obtient le seuil d’avertissement de l’utilisateur sous la forme d’une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="3820f-104">Gets the user's warning threshold as a text string.</span></span>

<span data-ttu-id="3820f-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3820f-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3820f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3820f-106">Syntax</span></span>


```JScript
QuotaThresholdText = DIDiskQuotaUser.QuotaThresholdText
```



## <a name="property-value"></a><span data-ttu-id="3820f-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3820f-107">Property value</span></span>

<span data-ttu-id="3820f-108">Valeur de chaîne qui contient le seuil d’avertissement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3820f-108">The string value that contains the user's warning threshold.</span></span> <span data-ttu-id="3820f-109">Si l’utilisation du disque d’un utilisateur dépasse cette valeur et que la propriété [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) est définie sur **true**, le système génère une entrée de journal des événements.</span><span class="sxs-lookup"><span data-stu-id="3820f-109">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="3820f-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3820f-110">Requirements</span></span>



| <span data-ttu-id="3820f-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3820f-111">Requirement</span></span> | <span data-ttu-id="3820f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="3820f-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3820f-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3820f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3820f-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3820f-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3820f-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3820f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3820f-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3820f-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3820f-117">DLL</span><span class="sxs-lookup"><span data-stu-id="3820f-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3820f-118"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="3820f-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3820f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3820f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3820f-120">**Objet IDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="3820f-120">**IDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="3820f-121">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="3820f-121">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="3820f-122">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="3820f-122">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> <dt>

[<span data-ttu-id="3820f-123">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="3820f-123">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)
</dt> </dl>

 

 




