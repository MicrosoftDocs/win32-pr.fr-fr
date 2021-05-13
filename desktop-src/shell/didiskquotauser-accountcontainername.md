---
description: Obtient le nom du conteneur de compte de l’utilisateur.
title: DIDiskQuotaUser. AccountContainerName, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountContainerName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b9b0355-ea69-4c34-b0be-fc8e5855ec73
ms.openlocfilehash: 1cb709ccc4fa0afcb56314bd097b1b0120b8b59a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843350"
---
# <a name="didiskquotauseraccountcontainername-property"></a><span data-ttu-id="5fad6-103">DIDiskQuotaUser. AccountContainerName, propriété</span><span class="sxs-lookup"><span data-stu-id="5fad6-103">DIDiskQuotaUser.AccountContainerName property</span></span>

<span data-ttu-id="5fad6-104">Obtient le nom du conteneur de compte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5fad6-104">Gets the name of the user's account container.</span></span>

<span data-ttu-id="5fad6-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="5fad6-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fad6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5fad6-106">Syntax</span></span>


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a><span data-ttu-id="5fad6-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="5fad6-107">Property value</span></span>

<span data-ttu-id="5fad6-108">Valeur de chaîne qui est définie sur le nom du conteneur de compte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5fad6-108">A string value that is set to the user's account container name.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fad6-109">Notes</span><span class="sxs-lookup"><span data-stu-id="5fad6-109">Remarks</span></span>

<span data-ttu-id="5fad6-110">Pour les comptes sans informations sur les services d’annuaire, cette propriété contient le nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="5fad6-110">For accounts without directory services information, this property contains the domain name.</span></span> <span data-ttu-id="5fad6-111">Pour les comptes avec les informations des services d’annuaire, cette propriété contient un nom canonique avec le nom de l’objet de fin supprimé.</span><span class="sxs-lookup"><span data-stu-id="5fad6-111">For accounts with directory services information, this property contains a canonical name with the terminating object name removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fad6-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="5fad6-112">Requirements</span></span>



| <span data-ttu-id="5fad6-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5fad6-113">Requirement</span></span> | <span data-ttu-id="5fad6-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="5fad6-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fad6-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fad6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5fad6-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fad6-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5fad6-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5fad6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5fad6-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5fad6-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5fad6-119">DLL</span><span class="sxs-lookup"><span data-stu-id="5fad6-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fad6-120"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="5fad6-120"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fad6-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5fad6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fad6-122">**Objet DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="5fad6-122">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




