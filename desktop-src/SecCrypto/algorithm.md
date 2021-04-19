---
description: Spécifie l’algorithme utilisé pour la signature, l’enveloppe et le chiffrement des opérations.
ms.assetid: 9a3071a3-e62d-43d3-acd7-0685592c78b4
title: Algorithme, objet (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f564efe9df3122951969a45443d58ace60e9db30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532201"
---
# <a name="algorithm-object"></a><span data-ttu-id="d37eb-103">Algorithme (objet)</span><span class="sxs-lookup"><span data-stu-id="d37eb-103">Algorithm object</span></span>

<span data-ttu-id="d37eb-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d37eb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="d37eb-105">Utilisez plutôt la [**classe AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="d37eb-105">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="d37eb-106">L’objet **algorithme** spécifie l’algorithme utilisé pour la signature, l’enveloppe et le chiffrement des opérations.</span><span class="sxs-lookup"><span data-stu-id="d37eb-106">The **Algorithm** object specifies the algorithm used for signing, enveloping, and encrypting operations.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="d37eb-107">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="d37eb-107">When to use</span></span>

<span data-ttu-id="d37eb-108">L’objet **algorithme** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="d37eb-108">The **Algorithm** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="d37eb-109">Définissez ou récupérez l’algorithme à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d37eb-109">Set or retrieve the algorithm to be used.</span></span>
-   <span data-ttu-id="d37eb-110">Définissez ou récupérez la longueur de la clé.</span><span class="sxs-lookup"><span data-stu-id="d37eb-110">Set or retrieve the key length.</span></span>

> [!Note]  
> <span data-ttu-id="d37eb-111">CAPICOM tente d’utiliser le fournisseur de services de chiffrement (CSP) par défaut du système.</span><span class="sxs-lookup"><span data-stu-id="d37eb-111">CAPICOM attempts to use the system default cryptographic service provider (CSP).</span></span> <span data-ttu-id="d37eb-112">Si le fournisseur de services de chiffrement ne peut pas fournir l’algorithme ou la longueur de clé demandés, CAPICOM recherche un CSP disponible fourni par Microsoft qui peut gérer l’algorithme et la longueur de clé demandés, dans cet ordre de disponibilité : fournisseur de chiffrement amélioré Microsoft, fournisseur de chiffrement fort Microsoft, fournisseur de chiffrement de base Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d37eb-112">If that CSP cannot provide the requested algorithm or key length, CAPICOM searches for an available Microsoft-provided CSP that can handle the requested algorithm and key length, in this order of availability: Microsoft Enhanced Cryptographic Provider, Microsoft Strong Cryptographic Provider, Microsoft Base Cryptographic Provider.</span></span>

 

## <a name="members"></a><span data-ttu-id="d37eb-113">Membres</span><span class="sxs-lookup"><span data-stu-id="d37eb-113">Members</span></span>

<span data-ttu-id="d37eb-114">L’objet **algorithme** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d37eb-114">The **Algorithm** object has these types of members:</span></span>

-   [<span data-ttu-id="d37eb-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d37eb-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d37eb-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d37eb-116">Properties</span></span>

<span data-ttu-id="d37eb-117">L’objet **algorithme** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d37eb-117">The **Algorithm** object has these properties.</span></span>



| <span data-ttu-id="d37eb-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="d37eb-118">Property</span></span>                                            | <span data-ttu-id="d37eb-119">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="d37eb-119">Access type</span></span>           | <span data-ttu-id="d37eb-120">Description</span><span class="sxs-lookup"><span data-stu-id="d37eb-120">Description</span></span>                                                                                                                       |
|:----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d37eb-121">**KeyLength**</span><span class="sxs-lookup"><span data-stu-id="d37eb-121">**KeyLength**</span></span>](algorithm-keylength.md)<br/> | <span data-ttu-id="d37eb-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d37eb-122">Read/write</span></span><br/> | <span data-ttu-id="d37eb-123">Définit ou récupère la longueur de la clé.</span><span class="sxs-lookup"><span data-stu-id="d37eb-123">Sets or retrieves the length of the key.</span></span><br/>                                                                               |
| [<span data-ttu-id="d37eb-124">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d37eb-124">**Name**</span></span>](algorithm-name.md)<br/>           | <span data-ttu-id="d37eb-125">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d37eb-125">Read/write</span></span><br/> | <span data-ttu-id="d37eb-126">Définit ou récupère l’algorithme utilisé pour la signature, l’enveloppe et le chiffrement des opérations.</span><span class="sxs-lookup"><span data-stu-id="d37eb-126">Sets or retrieves the algorithm used for signing, enveloping, and encrypting operations.</span></span> <span data-ttu-id="d37eb-127">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="d37eb-127">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d37eb-128">Notes</span><span class="sxs-lookup"><span data-stu-id="d37eb-128">Remarks</span></span>

<span data-ttu-id="d37eb-129">Impossible de créer l’objet **algorithme** .</span><span class="sxs-lookup"><span data-stu-id="d37eb-129">The **Algorithm** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="d37eb-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d37eb-130">Requirements</span></span>



| <span data-ttu-id="d37eb-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d37eb-131">Requirement</span></span> | <span data-ttu-id="d37eb-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="d37eb-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d37eb-133">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="d37eb-133">End of client support</span></span><br/> | <span data-ttu-id="d37eb-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d37eb-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d37eb-135">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="d37eb-135">End of server support</span></span><br/> | <span data-ttu-id="d37eb-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d37eb-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d37eb-137">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d37eb-137">Redistributable</span></span><br/>       | <span data-ttu-id="d37eb-138">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="d37eb-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d37eb-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="d37eb-139">Header</span></span><br/>                | <dl> <span data-ttu-id="d37eb-140"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="d37eb-140"><dt>Capicom.h</dt></span></span> </dl>   |
| <span data-ttu-id="d37eb-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d37eb-141">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d37eb-142"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d37eb-142"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d37eb-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d37eb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d37eb-144">**Objets de chiffrement**</span><span class="sxs-lookup"><span data-stu-id="d37eb-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
