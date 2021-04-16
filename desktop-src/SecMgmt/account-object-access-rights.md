---
description: Le type de droits d’accès à l’objet de compte a les types d’accès suivants.
ms.assetid: 42fb22bb-8135-4a8f-bce6-e767d6c5aaea
title: Droits d’accès à l’objet de compte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d69ba0939286564517c7293da136e88aa0367a60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529649"
---
# <a name="account-object-access-rights"></a><span data-ttu-id="8d4df-103">Droits d’accès à l’objet de compte</span><span class="sxs-lookup"><span data-stu-id="8d4df-103">Account Object Access Rights</span></span>

<span data-ttu-id="8d4df-104">Le type de droits d’accès à l’objet de compte a les types d’accès suivants.</span><span class="sxs-lookup"><span data-stu-id="8d4df-104">The Account Object Access Rights type has the following access types.</span></span>



| <span data-ttu-id="8d4df-105">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="8d4df-105">Access type</span></span>                     | <span data-ttu-id="8d4df-106">Description</span><span class="sxs-lookup"><span data-stu-id="8d4df-106">Description</span></span>                                                                                                                                                                                                                                           |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d4df-107">vue de compte \_</span><span class="sxs-lookup"><span data-stu-id="8d4df-107">ACCOUNT\_VIEW</span></span>                   | <span data-ttu-id="8d4df-108">Ce type d’accès est nécessaire pour lire les informations de compte.</span><span class="sxs-lookup"><span data-stu-id="8d4df-108">This access type is required to read the account information.</span></span> <span data-ttu-id="8d4df-109">Cela comprend les [*privilèges*](/windows/desktop/SecGloss/p-gly) attribués au compte, les quotas de mémoire affectés et tout type d’accès spécial accordé.</span><span class="sxs-lookup"><span data-stu-id="8d4df-109">This includes the [*privileges*](/windows/desktop/SecGloss/p-gly) assigned to the account, memory quotas assigned, and any special access types granted.</span></span> |
| <span data-ttu-id="8d4df-110">\_privilèges d’ajustement de compte \_</span><span class="sxs-lookup"><span data-stu-id="8d4df-110">ACCOUNT\_ADJUST\_PRIVILEGES</span></span>     | <span data-ttu-id="8d4df-111">Ce type d’accès est nécessaire pour attribuer des privilèges à un compte ou en supprimer.</span><span class="sxs-lookup"><span data-stu-id="8d4df-111">This access type is required to assign privileges to or remove privileges from an account.</span></span>                                                                                                                                                            |
| <span data-ttu-id="8d4df-112">COMPTE- \_ ajuster les \_ quotas</span><span class="sxs-lookup"><span data-stu-id="8d4df-112">ACCOUNT\_ADJUST\_QUOTAS</span></span>         | <span data-ttu-id="8d4df-113">Ce type d’accès est requis pour modifier les quotas système attribués à un compte.</span><span class="sxs-lookup"><span data-stu-id="8d4df-113">This access type is required to change the system quotas assigned to an account.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="8d4df-114">COMPTE \_ ajuster \_ \_ l’accès système</span><span class="sxs-lookup"><span data-stu-id="8d4df-114">ACCOUNT\_ADJUST\_SYSTEM\_ACCESS</span></span> | <span data-ttu-id="8d4df-115">Ce type d’accès est nécessaire pour mettre à jour les indicateurs d’accès système pour le compte.</span><span class="sxs-lookup"><span data-stu-id="8d4df-115">This access type is required to update the system access flags for the account.</span></span>                                                                                                                                                                       |



 

## <a name="generic-access-masks"></a><span data-ttu-id="8d4df-116">Masques d’accès génériques</span><span class="sxs-lookup"><span data-stu-id="8d4df-116">Generic Access Masks</span></span>

<span data-ttu-id="8d4df-117">L’objet [**Account**](account-object.md) publie les mappages suivants à partir de types d’accès génériques à des types d’accès spécifiques.</span><span class="sxs-lookup"><span data-stu-id="8d4df-117">The [**Account**](account-object.md) object publishes the following mappings from generic access types to specific access types.</span></span>

``` syntax
    GENERIC_READ        STANDARD_RIGHTS_READ |
                        ACCOUNT_VIEW 
            
    GENERIC_WRITE       STANDARD_RIGHTS_WRITE |
                        ACCOUNT_ADJUST_PRIVILEGES |
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS

    GENERIC_EXECUTE        STANDARD_RIGHTS_EXECUTE
```

## <a name="standard-access-types"></a><span data-ttu-id="8d4df-118">Types d’accès standard</span><span class="sxs-lookup"><span data-stu-id="8d4df-118">Standard Access Types</span></span>

<span data-ttu-id="8d4df-119">Cet objet ne prend pas en charge le type d’accès standard SYNCHRONIZE (facultatif).</span><span class="sxs-lookup"><span data-stu-id="8d4df-119">This object does not support the (optional) SYNCHRONIZE standard access type.</span></span> <span data-ttu-id="8d4df-120">Tous les types d’accès requis sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8d4df-120">All required access types are supported.</span></span> <span data-ttu-id="8d4df-121">Le masque de tous les types d’accès pris en charge pour ce type d’objet est le suivant.</span><span class="sxs-lookup"><span data-stu-id="8d4df-121">The mask of all supported access types for this object type is as follows.</span></span>

``` syntax
    ACCOUNT_ALL_ACCESS  STANDARD_RIGHTS_REQUIRED |
                        ACCOUNT_VIEW |
                        ACCOUNT_ADJUST_PRIVILEGES |    
                        ACCOUNT_ADJUST_QUOTAS |
                        ACCOUNT_ADJUST_SYSTEM_ACCESS
```

 

 
