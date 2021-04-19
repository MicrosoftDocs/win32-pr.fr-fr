---
description: Fournit l’accès au contexte d’un objet de chaîne CAPICOM. Ce contexte autorise l’utilisation de la chaîne d’approbation de certificat CAPICOM dans d’autres dérivations de CryptoAPI.
ms.assetid: ee258586-028e-486e-8129-07f43b6cc468
title: Interface IChainContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34ba471c50ceb9475121139c3ecb997cf1d26f2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542213"
---
# <a name="ichaincontext-interface"></a><span data-ttu-id="2e3ad-104">Interface IChainContext</span><span class="sxs-lookup"><span data-stu-id="2e3ad-104">IChainContext interface</span></span>

<span data-ttu-id="2e3ad-105">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="2e3ad-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="2e3ad-106">L’interface **IChainContext** fournit l’accès au contexte d’un objet de [**chaîne**](chain.md) CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-106">The **IChainContext** interface provides access to the context of a CAPICOM [**Chain**](chain.md) object.</span></span> <span data-ttu-id="2e3ad-107">Ce contexte autorise l’utilisation de la chaîne d’approbation de certificat CAPICOM dans d’autres dérivations de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-107">This context allows the CAPICOM certificate trust chain to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="2e3ad-108">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="2e3ad-108">When to use</span></span>

<span data-ttu-id="2e3ad-109">Utilisez cette interface lorsque vous devez utiliser un objet de [**chaîne**](chain.md) CAPICOM dans une autre dérivation de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-109">Use this interface when you need to use a CAPICOM [**Chain**](chain.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="2e3ad-110">Membres</span><span class="sxs-lookup"><span data-stu-id="2e3ad-110">Members</span></span>

<span data-ttu-id="2e3ad-111">L’interface **IChainContext** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2e3ad-111">The **IChainContext** interface has these types of members:</span></span>

-   [<span data-ttu-id="2e3ad-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2e3ad-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="2e3ad-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2e3ad-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2e3ad-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2e3ad-114">Methods</span></span>

<span data-ttu-id="2e3ad-115">L’interface **IChainContext** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-115">The **IChainContext** interface has these methods.</span></span>



| <span data-ttu-id="2e3ad-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="2e3ad-116">Method</span></span>                                           | <span data-ttu-id="2e3ad-117">Description</span><span class="sxs-lookup"><span data-stu-id="2e3ad-117">Description</span></span>                                                                                                                    |
|:-------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e3ad-118">**FreeContext**</span><span class="sxs-lookup"><span data-stu-id="2e3ad-118">**FreeContext**</span></span>](ichaincontext-freecontext.md) | <span data-ttu-id="2e3ad-119">Libère un \_ contexte de chaîne PCCERT \_ acquis par le biais de la propriété [**chainContext**](ichaincontext-chaincontext.md) .</span><span class="sxs-lookup"><span data-stu-id="2e3ad-119">Releases a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2e3ad-120">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2e3ad-120">Properties</span></span>

<span data-ttu-id="2e3ad-121">L’interface **IChainContext** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-121">The **IChainContext** interface has these properties.</span></span>



| <span data-ttu-id="2e3ad-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="2e3ad-122">Property</span></span>                                                      | <span data-ttu-id="2e3ad-123">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="2e3ad-123">Access type</span></span>           | <span data-ttu-id="2e3ad-124">Description</span><span class="sxs-lookup"><span data-stu-id="2e3ad-124">Description</span></span>                                                               |
|:--------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="2e3ad-125">**ChainContext**</span><span class="sxs-lookup"><span data-stu-id="2e3ad-125">**ChainContext**</span></span>](ichaincontext-chaincontext.md)<br/> | <span data-ttu-id="2e3ad-126">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="2e3ad-126">Read/write</span></span><br/> | <span data-ttu-id="2e3ad-127">Définit ou récupère le \_ \_ contexte de chaîne PCCERT d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="2e3ad-127">Sets or retrieves the PCCERT\_CHAIN\_CONTEXT of a certificate.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2e3ad-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e3ad-128">Requirements</span></span>



| <span data-ttu-id="2e3ad-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e3ad-129">Requirement</span></span> | <span data-ttu-id="2e3ad-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e3ad-130">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e3ad-131">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="2e3ad-131">Redistributable</span></span><br/> | <span data-ttu-id="2e3ad-132">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="2e3ad-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2e3ad-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2e3ad-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="2e3ad-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e3ad-134"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




