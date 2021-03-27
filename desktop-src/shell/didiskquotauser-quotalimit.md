---
description: Définit ou obtient la limite de quota actuelle de l’utilisateur.
title: DIDiskQuotaUser. QuotaLimit, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 7eee1be7-8ad5-4796-910c-987fe3fd6338
ms.openlocfilehash: 6c13c0d38c3c5f4387b7ee90165057edb111124a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971983"
---
# <a name="didiskquotauserquotalimit-property"></a><span data-ttu-id="67f39-103">DIDiskQuotaUser. QuotaLimit, propriété</span><span class="sxs-lookup"><span data-stu-id="67f39-103">DIDiskQuotaUser.QuotaLimit property</span></span>

<span data-ttu-id="67f39-104">Définit ou obtient la [**limite de quota**](diskquotacontrol-object.md)actuelle de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="67f39-104">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span>

<span data-ttu-id="67f39-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="67f39-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="67f39-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67f39-106">Syntax</span></span>


```JScript
iQuotaLimit = DIDiskQuotaUser.QuotaLimit
DIDiskQuotaUser.QuotaLimit = iQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="67f39-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="67f39-107">Property value</span></span>

<span data-ttu-id="67f39-108">Valeur **entière** qui spécifie ou reçoit la limite de quota actuelle de l’utilisateur, en octets.</span><span class="sxs-lookup"><span data-stu-id="67f39-108">An **Integer** value that specifies or receives the user's current quota limit, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="67f39-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="67f39-109">Requirements</span></span>



| <span data-ttu-id="67f39-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67f39-110">Requirement</span></span> | <span data-ttu-id="67f39-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="67f39-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f39-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67f39-112">Minimum supported client</span></span><br/> | <span data-ttu-id="67f39-113">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67f39-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="67f39-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67f39-114">Minimum supported server</span></span><br/> | <span data-ttu-id="67f39-115">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67f39-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="67f39-116">DLL</span><span class="sxs-lookup"><span data-stu-id="67f39-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67f39-117"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="67f39-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67f39-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67f39-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67f39-119">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="67f39-119">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="67f39-120">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="67f39-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="67f39-121">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="67f39-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> </dl>

 

 




