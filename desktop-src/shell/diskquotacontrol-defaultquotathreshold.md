---
description: Définit ou obtient le seuil de quota par défaut.
ms.assetid: d3f23e52-586f-4cb8-b91c-44a71f8f94b2
title: DiskQuotaControl. DefaultQuotaThreshold, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a4ce4205ee8bcc73c78bd1aabe7d8659ac3f5489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971970"
---
# <a name="diskquotacontroldefaultquotathreshold-property"></a><span data-ttu-id="781c9-103">DiskQuotaControl. DefaultQuotaThreshold, propriété</span><span class="sxs-lookup"><span data-stu-id="781c9-103">DiskQuotaControl.DefaultQuotaThreshold property</span></span>

<span data-ttu-id="781c9-104">Définit ou obtient le seuil de quota par défaut.</span><span class="sxs-lookup"><span data-stu-id="781c9-104">Sets or gets the default quota threshold.</span></span>

<span data-ttu-id="781c9-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="781c9-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="781c9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="781c9-106">Syntax</span></span>


```JScript
iDefaultQuotaThreshold = DiskQuotaControl.DefaultQuotaThreshold
DiskQuotaControl.DefaultQuotaThreshold = iDefaultQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="781c9-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="781c9-107">Property value</span></span>

<span data-ttu-id="781c9-108">Valeur **entière** qui est définie sur le seuil d’avertissement par défaut pour les nouveaux utilisateurs, en octets.</span><span class="sxs-lookup"><span data-stu-id="781c9-108">An **Integer** value that is set to the default warning threshold for new users, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="781c9-109">Notes</span><span class="sxs-lookup"><span data-stu-id="781c9-109">Remarks</span></span>

<span data-ttu-id="781c9-110">Le seuil de quota par défaut est appliqué automatiquement aux nouveaux utilisateurs du volume.</span><span class="sxs-lookup"><span data-stu-id="781c9-110">The default quota threshold is applied automatically to new users of the volume.</span></span> <span data-ttu-id="781c9-111">Si l’utilisation du disque d’un utilisateur dépasse cette valeur et que la propriété [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) est définie sur **true**, le système génère une entrée de journal des événements.</span><span class="sxs-lookup"><span data-stu-id="781c9-111">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span> <span data-ttu-id="781c9-112">Par exemple, si le seuil par défaut est de 10,0 Mo, la valeur de la propriété est « 10,0 Mo ».</span><span class="sxs-lookup"><span data-stu-id="781c9-112">For example, if the default threshold is 10.0 MB, the value of the property is "10.0 MB".</span></span> <span data-ttu-id="781c9-113">Si le volume n’a pas de seuil par défaut, la propriété a la valeur « aucune limite » ou l’équivalent localisé.</span><span class="sxs-lookup"><span data-stu-id="781c9-113">If the volume has no default threshold, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="781c9-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="781c9-114">Requirements</span></span>



| <span data-ttu-id="781c9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="781c9-115">Requirement</span></span> | <span data-ttu-id="781c9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="781c9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="781c9-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="781c9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="781c9-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="781c9-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="781c9-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="781c9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="781c9-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="781c9-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="781c9-121">DLL</span><span class="sxs-lookup"><span data-stu-id="781c9-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="781c9-122"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="781c9-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="781c9-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="781c9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="781c9-124">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="781c9-124">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




