---
description: Obtient la limite de quota par défaut sous la forme d’une chaîne de texte.
title: DiskQuotaControl. DefaultQuotaLimitText, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaLimitText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ea1b02e0-c480-4ef1-b6e0-1ec202d5f3c5
ms.openlocfilehash: 442e9094c62f22c3d990cf1112d145a1b2838e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112326"
---
# <a name="diskquotacontroldefaultquotalimittext-property"></a><span data-ttu-id="bf7ee-103">DiskQuotaControl. DefaultQuotaLimitText, propriété</span><span class="sxs-lookup"><span data-stu-id="bf7ee-103">DiskQuotaControl.DefaultQuotaLimitText property</span></span>

<span data-ttu-id="bf7ee-104">Obtient la limite de quota par défaut sous la forme d’une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="bf7ee-104">Gets the default quota limit as a text string.</span></span>

<span data-ttu-id="bf7ee-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="bf7ee-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf7ee-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf7ee-106">Syntax</span></span>


```JScript
DefaultQuotaLimitText = DiskQuotaControl.DefaultQuotaLimitText
```



## <a name="property-value"></a><span data-ttu-id="bf7ee-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bf7ee-107">Property value</span></span>

<span data-ttu-id="bf7ee-108">Valeur de chaîne qui contient la limite de quota par défaut pour les nouveaux utilisateurs du volume.</span><span class="sxs-lookup"><span data-stu-id="bf7ee-108">A string value that contains the default quota limit for new users of the volume.</span></span> <span data-ttu-id="bf7ee-109">Par exemple, si le quota par défaut est de 10,5 Mo, la valeur de la propriété est « 10,5 Mo ».</span><span class="sxs-lookup"><span data-stu-id="bf7ee-109">For example, if the default quota is 10.5 MB, the value of the property is "10.5 MB".</span></span> <span data-ttu-id="bf7ee-110">Si le volume n’a pas de quota par défaut, la propriété a la valeur « aucune limite » ou l’équivalent localisé.</span><span class="sxs-lookup"><span data-stu-id="bf7ee-110">If the volume has no default quota, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf7ee-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="bf7ee-111">Requirements</span></span>



| <span data-ttu-id="bf7ee-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf7ee-112">Requirement</span></span> | <span data-ttu-id="bf7ee-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf7ee-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf7ee-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf7ee-114">Minimum supported client</span></span><br/> | <span data-ttu-id="bf7ee-115">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf7ee-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bf7ee-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf7ee-116">Minimum supported server</span></span><br/> | <span data-ttu-id="bf7ee-117">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf7ee-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="bf7ee-118">DLL</span><span class="sxs-lookup"><span data-stu-id="bf7ee-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf7ee-119"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="bf7ee-119"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf7ee-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf7ee-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf7ee-121">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="bf7ee-121">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="bf7ee-122">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="bf7ee-122">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




