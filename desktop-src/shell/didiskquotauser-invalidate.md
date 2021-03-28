---
description: Efface les informations utilisateur mises en cache de l’objet.
title: DIDiskQuotaUser. Invalidate, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.Invalidate
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e0ffd5b7-db1d-40a4-810a-ff43549b0c9b
ms.openlocfilehash: 2b07ae6fd210b8722378a771cda97c2c04572c66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525342"
---
# <a name="didiskquotauserinvalidate-method"></a><span data-ttu-id="54195-103">DIDiskQuotaUser. Invalidate, méthode</span><span class="sxs-lookup"><span data-stu-id="54195-103">DIDiskQuotaUser.Invalidate method</span></span>

<span data-ttu-id="54195-104">Efface les informations utilisateur mises en cache de l’objet.</span><span class="sxs-lookup"><span data-stu-id="54195-104">Clears the object's cached user information.</span></span>

## <a name="syntax"></a><span data-ttu-id="54195-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54195-105">Syntax</span></span>


```JScript
DIDiskQuotaUser.Invalidate()
```



## <a name="parameters"></a><span data-ttu-id="54195-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54195-106">Parameters</span></span>

<span data-ttu-id="54195-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="54195-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="54195-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54195-108">Return value</span></span>

<span data-ttu-id="54195-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="54195-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="54195-110">Notes</span><span class="sxs-lookup"><span data-stu-id="54195-110">Remarks</span></span>

<span data-ttu-id="54195-111">Cette méthode efface les informations utilisateur stockées dans le cache de l’objet.</span><span class="sxs-lookup"><span data-stu-id="54195-111">This method clears the user information stored in the object's cache.</span></span> <span data-ttu-id="54195-112">La prochaine fois qu’une demande est effectuée pour obtenir des informations sur les quotas, l’objet récupère les informations à partir du volume NTFS et actualise le cache.</span><span class="sxs-lookup"><span data-stu-id="54195-112">The next time a request is made for quota-related information, the object retrieves the information from the NTFS volume and refreshes the cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="54195-113">Spécifications</span><span class="sxs-lookup"><span data-stu-id="54195-113">Requirements</span></span>



| <span data-ttu-id="54195-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54195-114">Requirement</span></span> | <span data-ttu-id="54195-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="54195-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54195-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54195-116">Minimum supported client</span></span><br/> | <span data-ttu-id="54195-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54195-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="54195-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54195-118">Minimum supported server</span></span><br/> | <span data-ttu-id="54195-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54195-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="54195-120">DLL</span><span class="sxs-lookup"><span data-stu-id="54195-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54195-121"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="54195-121"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54195-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54195-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54195-123">**Objet DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="54195-123">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




