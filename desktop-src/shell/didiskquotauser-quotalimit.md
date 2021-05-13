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
ms.openlocfilehash: b1971871bdeb18e3c7dd4c7978152bbec276fa8b
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841630"
---
# <a name="didiskquotauserquotalimit-property"></a><span data-ttu-id="1f597-103">DIDiskQuotaUser. QuotaLimit, propriété</span><span class="sxs-lookup"><span data-stu-id="1f597-103">DIDiskQuotaUser.QuotaLimit property</span></span>

<span data-ttu-id="1f597-104">Définit ou obtient la [**limite de quota**](diskquotacontrol-object.md)actuelle de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="1f597-104">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span>

<span data-ttu-id="1f597-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1f597-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f597-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f597-106">Syntax</span></span>


```JScript
iQuotaLimit = DIDiskQuotaUser.QuotaLimit
DIDiskQuotaUser.QuotaLimit = iQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="1f597-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="1f597-107">Property value</span></span>

<span data-ttu-id="1f597-108">Valeur **entière** qui spécifie ou reçoit la limite de quota actuelle de l’utilisateur, en octets.</span><span class="sxs-lookup"><span data-stu-id="1f597-108">An **Integer** value that specifies or receives the user's current quota limit, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f597-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="1f597-109">Requirements</span></span>



| <span data-ttu-id="1f597-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f597-110">Requirement</span></span> | <span data-ttu-id="1f597-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f597-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f597-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f597-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1f597-113">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f597-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1f597-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f597-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1f597-115">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f597-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1f597-116">DLL</span><span class="sxs-lookup"><span data-stu-id="1f597-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f597-117"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="1f597-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f597-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f597-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f597-119">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="1f597-119">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="1f597-120">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="1f597-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="1f597-121">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="1f597-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> </dl>

 

 




