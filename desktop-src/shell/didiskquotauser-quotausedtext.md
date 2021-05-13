---
description: Obtient l’utilisation du disque actuel de l’utilisateur sous la forme d’une chaîne de texte.
title: DIDiskQuotaUser. QuotaUsedText, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsedText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: be27a17c-77ec-4016-8c2e-16fbc88c7c7a
ms.openlocfilehash: bf818bdcd22b734c6f4638a837af97bfecef1695
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843210"
---
# <a name="didiskquotauserquotausedtext-property"></a><span data-ttu-id="87db4-103">DIDiskQuotaUser. QuotaUsedText, propriété</span><span class="sxs-lookup"><span data-stu-id="87db4-103">DIDiskQuotaUser.QuotaUsedText property</span></span>

<span data-ttu-id="87db4-104">Obtient l’utilisation du disque actuel de l’utilisateur sous la forme d’une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="87db4-104">Gets the user's current disk usage as a text string.</span></span>

<span data-ttu-id="87db4-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="87db4-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="87db4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87db4-106">Syntax</span></span>


```JScript
QuotaUsedText = DIDiskQuotaUser.QuotaUsedText
```



## <a name="property-value"></a><span data-ttu-id="87db4-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="87db4-107">Property value</span></span>

<span data-ttu-id="87db4-108">Valeur de chaîne qui est définie sur la quantité d’espace disque actuellement utilisée.</span><span class="sxs-lookup"><span data-stu-id="87db4-108">A string value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="87db4-109">Si la compression de fichiers NTFS est activée, cette propriété reflète la quantité d’espace disque requise par les données dans un État non compressé.</span><span class="sxs-lookup"><span data-stu-id="87db4-109">If NTFS file compression is enabled, this property reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="87db4-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="87db4-110">Requirements</span></span>



| <span data-ttu-id="87db4-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87db4-111">Requirement</span></span> | <span data-ttu-id="87db4-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="87db4-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87db4-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87db4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="87db4-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87db4-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="87db4-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87db4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="87db4-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87db4-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="87db4-117">DLL</span><span class="sxs-lookup"><span data-stu-id="87db4-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87db4-118"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="87db4-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87db4-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87db4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87db4-120">**Objet DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="87db4-120">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="87db4-121">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="87db4-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> <dt>

[<span data-ttu-id="87db4-122">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="87db4-122">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)
</dt> <dt>

[<span data-ttu-id="87db4-123">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="87db4-123">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)
</dt> </dl>

 

 




