---
description: Obtient le seuil de quota par défaut sous la forme d’une chaîne de texte.
ms.assetid: 48b1cbd5-12dd-4c31-a14c-7904d29f6eb9
title: DiskQuotaControl. DefaultQuotaThresholdText, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b3b209c7c8e71b49fd3b9fce90b9ea30b584bd65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112323"
---
# <a name="diskquotacontroldefaultquotathresholdtext-property"></a><span data-ttu-id="3829d-103">DiskQuotaControl. DefaultQuotaThresholdText, propriété</span><span class="sxs-lookup"><span data-stu-id="3829d-103">DiskQuotaControl.DefaultQuotaThresholdText property</span></span>

<span data-ttu-id="3829d-104">Obtient le seuil de quota par défaut sous la forme d’une chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="3829d-104">Gets the default quota threshold as a text string.</span></span>

<span data-ttu-id="3829d-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3829d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3829d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3829d-106">Syntax</span></span>


```JScript
DefaultQuotaThresholdText = DiskQuotaControl.DefaultQuotaThresholdText
```



## <a name="property-value"></a><span data-ttu-id="3829d-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3829d-107">Property value</span></span>

<span data-ttu-id="3829d-108">Valeur de chaîne qui contient le seuil de quota par défaut pour le volume.</span><span class="sxs-lookup"><span data-stu-id="3829d-108">A string value that contains the default quota threshold for the volume.</span></span>

## <a name="remarks"></a><span data-ttu-id="3829d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="3829d-109">Remarks</span></span>

<span data-ttu-id="3829d-110">Le seuil de quota par défaut est appliqué automatiquement aux nouveaux utilisateurs du volume.</span><span class="sxs-lookup"><span data-stu-id="3829d-110">The default quota threshold is applied automatically to new users of the volume.</span></span> <span data-ttu-id="3829d-111">Si l’utilisation du disque d’un utilisateur dépasse cette valeur et que la propriété [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) est définie sur **true**, le système génère une entrée de journal des événements.</span><span class="sxs-lookup"><span data-stu-id="3829d-111">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span> <span data-ttu-id="3829d-112">Par exemple, si le seuil par défaut est de 10,0 Mo, la valeur de la propriété est « 10,0 Mo ».</span><span class="sxs-lookup"><span data-stu-id="3829d-112">For example, if the default threshold is 10.0 MB, the value of the property is "10.0 MB".</span></span> <span data-ttu-id="3829d-113">Si le volume n’a pas de seuil par défaut, la propriété a la valeur « aucune limite » ou l’équivalent localisé.</span><span class="sxs-lookup"><span data-stu-id="3829d-113">If the volume has no default threshold, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="3829d-114">Spécifications</span><span class="sxs-lookup"><span data-stu-id="3829d-114">Requirements</span></span>



| <span data-ttu-id="3829d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3829d-115">Requirement</span></span> | <span data-ttu-id="3829d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3829d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3829d-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3829d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3829d-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3829d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3829d-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3829d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3829d-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3829d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3829d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="3829d-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3829d-122"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="3829d-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3829d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3829d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3829d-124">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="3829d-124">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




