---
description: Définit ou obtient une valeur booléenne qui indique si une entrée du journal des événements système est effectuée lorsqu’un utilisateur dépasse son seuil de quota attribué.
ms.assetid: 93bf5a4b-a887-4403-8c61-9ca8ba430c47
title: DiskQuotaControl. LogQuotaThreshold, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fbbf83ae978e46a3867d27c23e8b8f726ba0d7dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971955"
---
# <a name="diskquotacontrollogquotathreshold-property"></a><span data-ttu-id="fa1e2-103">DiskQuotaControl. LogQuotaThreshold, propriété</span><span class="sxs-lookup"><span data-stu-id="fa1e2-103">DiskQuotaControl.LogQuotaThreshold property</span></span>

<span data-ttu-id="fa1e2-104">Définit ou obtient une valeur booléenne qui indique si une entrée du journal des événements système est effectuée lorsqu’un utilisateur dépasse son seuil de quota attribué.</span><span class="sxs-lookup"><span data-stu-id="fa1e2-104">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota threshold.</span></span>

<span data-ttu-id="fa1e2-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fa1e2-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa1e2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa1e2-106">Syntax</span></span>


```JScript
bLogQuotaThreshold = DiskQuotaControl.LogQuotaThreshold
DiskQuotaControl.LogQuotaThreshold = bLogQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="fa1e2-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fa1e2-107">Property value</span></span>

<span data-ttu-id="fa1e2-108">Cette propriété a la valeur **true** si une entrée du journal des événements système est effectuée lorsque l’utilisateur dépasse son seuil d’avertissement de quota, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="fa1e2-108">This property is set to **TRUE** if a system event log entry is made when the user exceeds his or her quota warning threshold, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa1e2-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="fa1e2-109">Requirements</span></span>



| <span data-ttu-id="fa1e2-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa1e2-110">Requirement</span></span> | <span data-ttu-id="fa1e2-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa1e2-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa1e2-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa1e2-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fa1e2-113">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa1e2-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fa1e2-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa1e2-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fa1e2-115">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa1e2-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fa1e2-116">DLL</span><span class="sxs-lookup"><span data-stu-id="fa1e2-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa1e2-117"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="fa1e2-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa1e2-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa1e2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa1e2-119">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="fa1e2-119">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="fa1e2-120">**Objet DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="fa1e2-120">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> <dt>

[<span data-ttu-id="fa1e2-121">**LogQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="fa1e2-121">**LogQuotaLimit**</span></span>](diskquotacontrol-logquotalimit.md)
</dt> </dl>

 

 




