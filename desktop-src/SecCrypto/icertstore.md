---
description: Fournit l’accès au contexte d’un objet de magasin CAPICOM. Ce contexte permet d’utiliser le magasin de certificats CAPICOM dans d’autres dérivations de CryptoAPI.
ms.assetid: dc108e2d-d6ec-4972-9c8e-e6e738c25756
title: Interface ICertStore
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 119609399709340049bc43693ac51f6259021416
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542381"
---
# <a name="icertstore-interface"></a><span data-ttu-id="a0958-104">Interface ICertStore</span><span class="sxs-lookup"><span data-stu-id="a0958-104">ICertStore interface</span></span>

<span data-ttu-id="a0958-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="a0958-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="a0958-106">L’interface **ICertStore** fournit l’accès au contexte d’un objet de [**magasin**](store.md) CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="a0958-106">The **ICertStore** interface provides access to the context of a CAPICOM [**Store**](store.md) object.</span></span> <span data-ttu-id="a0958-107">Ce contexte permet d’utiliser le magasin de certificats CAPICOM dans d’autres dérivations de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="a0958-107">This context allows the CAPICOM certificate store to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="a0958-108">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="a0958-108">When to use</span></span>

<span data-ttu-id="a0958-109">Utilisez cette interface lorsque vous devez utiliser un objet de [**magasin**](store.md) CAPICOM dans une autre dérivation de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="a0958-109">Use this interface when you need to use a CAPICOM [**Store**](store.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="a0958-110">Membres</span><span class="sxs-lookup"><span data-stu-id="a0958-110">Members</span></span>

<span data-ttu-id="a0958-111">L’interface **ICertStore** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a0958-111">The **ICertStore** interface has these types of members:</span></span>

-   [<span data-ttu-id="a0958-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a0958-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="a0958-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a0958-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="a0958-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a0958-114">Methods</span></span>

<span data-ttu-id="a0958-115">L’interface **ICertStore** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a0958-115">The **ICertStore** interface has these methods.</span></span>



| <span data-ttu-id="a0958-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="a0958-116">Method</span></span>                                        | <span data-ttu-id="a0958-117">Description</span><span class="sxs-lookup"><span data-stu-id="a0958-117">Description</span></span>                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0958-118">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="a0958-118">**CloseHandle**</span></span>](icertstore-closehandle.md) | <span data-ttu-id="a0958-119">Ferme un handle HCERTSTORE acquis par le biais de la propriété [**StoreHandle**](icertstore-storehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="a0958-119">Closes an HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="a0958-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a0958-120">Properties</span></span>

<span data-ttu-id="a0958-121">L’interface **ICertStore** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="a0958-121">The **ICertStore** interface has these properties.</span></span>



| <span data-ttu-id="a0958-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="a0958-122">Property</span></span>                                                     | <span data-ttu-id="a0958-123">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="a0958-123">Access type</span></span>           | <span data-ttu-id="a0958-124">Description</span><span class="sxs-lookup"><span data-stu-id="a0958-124">Description</span></span>                                                                                                         |
|:-------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0958-125">**StoreHandle**</span><span class="sxs-lookup"><span data-stu-id="a0958-125">**StoreHandle**</span></span>](icertstore-storehandle.md)<br/>     | <span data-ttu-id="a0958-126">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a0958-126">Read/write</span></span><br/> | <span data-ttu-id="a0958-127">Définit ou récupère le handle HCERTSTORE d’un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="a0958-127">Sets or retrieves the HCERTSTORE handle of a certificate store.</span></span><br/>                                          |
| [<span data-ttu-id="a0958-128">**StoreLocation**</span><span class="sxs-lookup"><span data-stu-id="a0958-128">**StoreLocation**</span></span>](icertstore-storelocation.md)<br/> | <span data-ttu-id="a0958-129">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="a0958-129">Read/write</span></span><br/> | <span data-ttu-id="a0958-130">Définit ou récupère l' [**\_ \_ emplacement du magasin CAPICOM**](capicom-store-location.md) d’un magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="a0958-130">Sets or retrieves the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) of a certificate store.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a0958-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a0958-131">Requirements</span></span>



| <span data-ttu-id="a0958-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a0958-132">Requirement</span></span> | <span data-ttu-id="a0958-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="a0958-133">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0958-134">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a0958-134">Redistributable</span></span><br/> | <span data-ttu-id="a0958-135">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="a0958-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a0958-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a0958-136">DLL</span></span><br/>             | <dl> <span data-ttu-id="a0958-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0958-137"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




