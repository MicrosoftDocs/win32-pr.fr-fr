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
ms.openlocfilehash: ef96b296d77979e5ef72c2804ad24628f0b0d8f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750228"
---
# <a name="didiskquotauseraccountcontainername-property"></a><span data-ttu-id="44c63-103">DIDiskQuotaUser. AccountContainerName, propriété</span><span class="sxs-lookup"><span data-stu-id="44c63-103">DIDiskQuotaUser.AccountContainerName property</span></span>

<span data-ttu-id="44c63-104">Obtient le nom du conteneur de compte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="44c63-104">Gets the name of the user's account container.</span></span>

<span data-ttu-id="44c63-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="44c63-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="44c63-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="44c63-106">Syntax</span></span>


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a><span data-ttu-id="44c63-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="44c63-107">Property value</span></span>

<span data-ttu-id="44c63-108">Valeur de chaîne qui est définie sur le nom du conteneur de compte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="44c63-108">A string value that is set to the user's account container name.</span></span>

## <a name="remarks"></a><span data-ttu-id="44c63-109">Notes</span><span class="sxs-lookup"><span data-stu-id="44c63-109">Remarks</span></span>

<span data-ttu-id="44c63-110">Pour les comptes sans informations sur les services d’annuaire, cette propriété contient le nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="44c63-110">For accounts without directory services information, this property contains the domain name.</span></span> <span data-ttu-id="44c63-111">Pour les comptes avec les informations des services d’annuaire, cette propriété contient un nom canonique avec le nom de l’objet de fin supprimé.</span><span class="sxs-lookup"><span data-stu-id="44c63-111">For accounts with directory services information, this property contains a canonical name with the terminating object name removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="44c63-112">Spécifications</span><span class="sxs-lookup"><span data-stu-id="44c63-112">Requirements</span></span>



| <span data-ttu-id="44c63-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="44c63-113">Requirement</span></span> | <span data-ttu-id="44c63-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="44c63-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44c63-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44c63-115">Minimum supported client</span></span><br/> | <span data-ttu-id="44c63-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44c63-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="44c63-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="44c63-117">Minimum supported server</span></span><br/> | <span data-ttu-id="44c63-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="44c63-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="44c63-119">DLL</span><span class="sxs-lookup"><span data-stu-id="44c63-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44c63-120"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="44c63-120"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44c63-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="44c63-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44c63-122">**Objet DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="44c63-122">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




