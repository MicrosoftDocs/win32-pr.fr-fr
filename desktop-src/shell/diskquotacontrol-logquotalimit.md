---
description: Définit ou obtient une valeur booléenne qui indique si une entrée du journal des événements système est effectuée lorsqu’un utilisateur dépasse sa limite de quota affectée.
ms.assetid: f7f6b0a0-0fd1-47bd-9950-d6d579819377
title: DiskQuotaControl. LogQuotaLimit, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3db64d7fb06ed8bfb7ba8c2483eb413f3f01a224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971958"
---
# <a name="diskquotacontrollogquotalimit-property"></a><span data-ttu-id="44747-103">DiskQuotaControl. LogQuotaLimit, propriété</span><span class="sxs-lookup"><span data-stu-id="44747-103">DiskQuotaControl.LogQuotaLimit property</span></span>

<span data-ttu-id="44747-104">Définit ou obtient une valeur booléenne qui indique si une entrée du journal des événements système est effectuée lorsqu’un utilisateur dépasse sa limite de quota affectée.</span><span class="sxs-lookup"><span data-stu-id="44747-104">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota limit.</span></span>

<span data-ttu-id="44747-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="44747-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="44747-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44747-106">Syntax</span></span>


```JScript
bLogQuotaLimit = DiskQuotaControl.LogQuotaLimit
DiskQuotaControl.LogQuotaLimit = bLogQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="44747-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="44747-107">Property value</span></span>

<span data-ttu-id="44747-108">Cette propriété a la valeur **true** si une entrée du journal des événements système est effectuée lorsque l’utilisateur dépasse sa limite de quota, ou **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="44747-108">This property is set to **TRUE** if a system event log entry is made when the user exceeds his or her quota limit, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="44747-109">Spécifications</span><span class="sxs-lookup"><span data-stu-id="44747-109">Requirements</span></span>



| <span data-ttu-id="44747-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44747-110">Requirement</span></span> | <span data-ttu-id="44747-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="44747-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44747-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44747-112">Minimum supported client</span></span><br/> | <span data-ttu-id="44747-113">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44747-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="44747-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44747-114">Minimum supported server</span></span><br/> | <span data-ttu-id="44747-115">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44747-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="44747-116">DLL</span><span class="sxs-lookup"><span data-stu-id="44747-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44747-117"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="44747-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44747-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44747-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44747-119">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="44747-119">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="44747-120">**Objet DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="44747-120">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> <dt>

[<span data-ttu-id="44747-121">**LogQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="44747-121">**LogQuotaThreshold**</span></span>](diskquotacontrol-logquotathreshold.md)
</dt> </dl>

 

 




