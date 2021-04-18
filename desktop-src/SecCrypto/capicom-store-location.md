---
description: Indique l’emplacement d’un magasin de certificats.
ms.assetid: b0c64e54-7139-4945-9802-6e6c479481e2
title: Énumération CAPICOM_STORE_LOCATION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_STORE_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 24b2e786e2821c39c6ff67f5919dca2ac0c6bfe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528935"
---
# <a name="capicom_store_location-enumeration"></a><span data-ttu-id="93722-103">\_Énumération de l’emplacement du magasin CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="93722-103">CAPICOM\_STORE\_LOCATION enumeration</span></span>

<span data-ttu-id="93722-104">Le type d’énumération de l' **\_ \_ emplacement du magasin CAPICOM** indique l’emplacement d’un [*magasin de certificats*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="93722-104">The **CAPICOM\_STORE\_LOCATION** enumeration type indicates the location of a [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="members"></a><span data-ttu-id="93722-105">Membres</span><span class="sxs-lookup"><span data-stu-id="93722-105">Members</span></span>



| <span data-ttu-id="93722-106">Membre</span><span class="sxs-lookup"><span data-stu-id="93722-106">Member</span></span>                                      | <span data-ttu-id="93722-107">Description</span><span class="sxs-lookup"><span data-stu-id="93722-107">Description</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="93722-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="93722-108">Value</span></span> |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="93722-109">**\_magasin mémoire CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="93722-109">**CAPICOM\_MEMORY\_STORE**</span></span>                  | <span data-ttu-id="93722-110">Le magasin est un magasin de mémoire.</span><span class="sxs-lookup"><span data-stu-id="93722-110">The store is a memory store.</span></span> <span data-ttu-id="93722-111">Les modifications apportées au contenu du magasin ne sont pas conservées.</span><span class="sxs-lookup"><span data-stu-id="93722-111">Any changes in the contents of the store are not persisted.</span></span><br/>                                                                                                                                                                              | <span data-ttu-id="93722-112">0</span><span class="sxs-lookup"><span data-stu-id="93722-112">0</span></span>     |
| <span data-ttu-id="93722-113">**base de l' \_ ordinateur local CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93722-113">**CAPICOM\_LOCAL\_MACHINE\_STORE**</span></span>          | <span data-ttu-id="93722-114">Le magasin est un magasin de l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="93722-114">The store is a local machine store.</span></span> <span data-ttu-id="93722-115">Les magasins d’ordinateurs locaux peuvent être des magasins de lecture/écriture uniquement si l’utilisateur dispose d’autorisations de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="93722-115">Local machine stores can be read/write stores only if the user has read/write permissions.</span></span> <span data-ttu-id="93722-116">Si l’utilisateur dispose d’autorisations de lecture/écriture et si le magasin est ouvert en lecture/écriture, les modifications apportées au contenu du magasin sont conservées.</span><span class="sxs-lookup"><span data-stu-id="93722-116">If the user has read/write permissions and if the store is opened read/write, then changes in the contents of the store are persisted.</span></span><br/> | <span data-ttu-id="93722-117">1</span><span class="sxs-lookup"><span data-stu-id="93722-117">1</span></span>     |
| <span data-ttu-id="93722-118">**magasin de l' \_ utilisateur actuel CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93722-118">**CAPICOM\_CURRENT\_USER\_STORE**</span></span>           | <span data-ttu-id="93722-119">Le magasin est un magasin de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="93722-119">The store is a current user store.</span></span> <span data-ttu-id="93722-120">Un magasin de l’utilisateur actuel peut être un magasin en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="93722-120">A current user store may be a read/write store.</span></span> <span data-ttu-id="93722-121">Si c’est le cas, les modifications apportées au contenu du magasin sont conservées.</span><span class="sxs-lookup"><span data-stu-id="93722-121">If it is, changes in the contents of the store are persisted.</span></span><br/>                                                                                                                      | <span data-ttu-id="93722-122">2</span><span class="sxs-lookup"><span data-stu-id="93722-122">2</span></span>     |
| <span data-ttu-id="93722-123">**magasin d’utilisateurs de CAPICOM \_ active \_ Directory \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93722-123">**CAPICOM\_ACTIVE\_DIRECTORY\_USER\_STORE**</span></span> | <span data-ttu-id="93722-124">Le magasin est un magasin de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="93722-124">The store is an Active Directory store.</span></span> <span data-ttu-id="93722-125">Les magasins de Active Directory ne peuvent être ouverts qu’en mode lecture seule.</span><span class="sxs-lookup"><span data-stu-id="93722-125">Active Directory stores can be opened only in read-only mode.</span></span> <span data-ttu-id="93722-126">Impossible d’ajouter ou de supprimer des certificats dans des magasins de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="93722-126">Certificates cannot be added to or removed from Active Directory stores.</span></span><br/>                                                                                        | <span data-ttu-id="93722-127">3</span><span class="sxs-lookup"><span data-stu-id="93722-127">3</span></span>     |
| <span data-ttu-id="93722-128">**\_magasin d’utilisateurs de \_ carte à puce \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="93722-128">**CAPICOM\_SMART\_CARD\_USER\_STORE**</span></span>       | <span data-ttu-id="93722-129">Les magasins prennent en charge les magasins de certificats basés sur une carte à puce.</span><span class="sxs-lookup"><span data-stu-id="93722-129">Stores support smart card–based certificate stores.</span></span> <span data-ttu-id="93722-130">Le magasin est le groupe de cartes à puce actuelles.</span><span class="sxs-lookup"><span data-stu-id="93722-130">The store is the group of present smart cards.</span></span> <span data-ttu-id="93722-131">Introduit dans CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="93722-131">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                                                                         | <span data-ttu-id="93722-132">4</span><span class="sxs-lookup"><span data-stu-id="93722-132">4</span></span>     |



## <a name="remarks"></a><span data-ttu-id="93722-133">Notes</span><span class="sxs-lookup"><span data-stu-id="93722-133">Remarks</span></span>

<span data-ttu-id="93722-134">Le type d’énumération de l' **\_ \_ emplacement du magasin CAPICOM** est utilisé par les méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="93722-134">The **CAPICOM\_STORE\_LOCATION** enumeration type is used by the following methods:</span></span>

-   [<span data-ttu-id="93722-135">**PrivateKey. Open**</span><span class="sxs-lookup"><span data-stu-id="93722-135">**PrivateKey.Open**</span></span>](privatekey-open.md)
-   [<span data-ttu-id="93722-136">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="93722-136">**Store.Open**</span></span>](store-open.md)

## <a name="requirements"></a><span data-ttu-id="93722-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="93722-137">Requirements</span></span>



| <span data-ttu-id="93722-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="93722-138">Requirement</span></span> | <span data-ttu-id="93722-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="93722-139">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="93722-140">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="93722-140">Redistributable</span></span><br/> | <span data-ttu-id="93722-141">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="93722-141">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="93722-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="93722-142">Header</span></span><br/>          | <dl> <span data-ttu-id="93722-143"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="93722-143"><dt>Capicom.h</dt></span></span> </dl> |



 

 
