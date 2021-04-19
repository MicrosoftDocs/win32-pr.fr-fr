---
description: Fournit des fonctionnalités pour hacher une chaîne.
ms.assetid: 893639c2-57b9-48f6-bf60-a21c3368ffeb
title: Objet HashedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b6e54d7d2ca52ceafe500615af4063dfc7310b0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528656"
---
# <a name="hasheddata-object"></a><span data-ttu-id="b914b-103">Objet HashedData</span><span class="sxs-lookup"><span data-stu-id="b914b-103">HashedData object</span></span>

<span data-ttu-id="b914b-104">\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b914b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b914b-105">Utilisez plutôt la [**classe HashAlgorithm**](/previous-versions/windows/) dans l’espace de noms [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="b914b-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="b914b-106">L’objet **HashedData** fournit les fonctionnalités de hachage d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="b914b-106">The **HashedData** object provides functionality for hashing a string.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="b914b-107">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="b914b-107">When to use</span></span>

<span data-ttu-id="b914b-108">L’objet **HashedData** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="b914b-108">The **HashedData** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="b914b-109">Spécifiez la chaîne de contenu qui contient les données à hacher.</span><span class="sxs-lookup"><span data-stu-id="b914b-109">Specify the content string that contains the data to be hashed.</span></span>
-   <span data-ttu-id="b914b-110">Applique un algorithme de hachage spécifié à la chaîne de contenu.</span><span class="sxs-lookup"><span data-stu-id="b914b-110">Apply a specified hash algorithm to the content string.</span></span>

## <a name="members"></a><span data-ttu-id="b914b-111">Membres</span><span class="sxs-lookup"><span data-stu-id="b914b-111">Members</span></span>

<span data-ttu-id="b914b-112">L’objet **HashedData** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b914b-112">The **HashedData** object has these types of members:</span></span>

-   [<span data-ttu-id="b914b-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b914b-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="b914b-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b914b-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="b914b-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b914b-115">Methods</span></span>

<span data-ttu-id="b914b-116">L’objet **HashedData** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b914b-116">The **HashedData** object has these methods.</span></span>



| <span data-ttu-id="b914b-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="b914b-117">Method</span></span>                          | <span data-ttu-id="b914b-118">Description</span><span class="sxs-lookup"><span data-stu-id="b914b-118">Description</span></span>                                        |
|:--------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="b914b-119">**Format**</span><span class="sxs-lookup"><span data-stu-id="b914b-119">**Hash**</span></span>](hasheddata-hash.md) | <span data-ttu-id="b914b-120">Crée un hachage de la chaîne spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b914b-120">Creates a hash of the specified string.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="b914b-121">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b914b-121">Properties</span></span>

<span data-ttu-id="b914b-122">L’objet **HashedData** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b914b-122">The **HashedData** object has these properties.</span></span>



| <span data-ttu-id="b914b-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="b914b-123">Property</span></span>                                             | <span data-ttu-id="b914b-124">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="b914b-124">Access type</span></span>           | <span data-ttu-id="b914b-125">Description</span><span class="sxs-lookup"><span data-stu-id="b914b-125">Description</span></span>                                                                                                                                                                          |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b914b-126">**Algorithme**</span><span class="sxs-lookup"><span data-stu-id="b914b-126">**Algorithm**</span></span>](hasheddata-algorithm.md)<br/> | <span data-ttu-id="b914b-127">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b914b-127">Read/write</span></span><br/> | <span data-ttu-id="b914b-128">Définit ou récupère le type d’algorithme de hachage utilisé.</span><span class="sxs-lookup"><span data-stu-id="b914b-128">Sets or retrieves the type of hashing algorithm used.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="b914b-129">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="b914b-129">**Value**</span></span>](hasheddata-value.md)<br/>         | <span data-ttu-id="b914b-130">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b914b-130">Read-only</span></span><br/>  | <span data-ttu-id="b914b-131">Récupère les données hachées après des appels réussis à la méthode de [**hachage**](hasheddata-hash.md) .</span><span class="sxs-lookup"><span data-stu-id="b914b-131">Retrieves the hashed data after successful calls to the [**Hash**](hasheddata-hash.md) method.</span></span> <span data-ttu-id="b914b-132">Le hachage est retourné au format hexadécimal.</span><span class="sxs-lookup"><span data-stu-id="b914b-132">The hash is returned in hexadecimal format.</span></span> <span data-ttu-id="b914b-133">Il s’agit de la propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="b914b-133">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b914b-134">Notes</span><span class="sxs-lookup"><span data-stu-id="b914b-134">Remarks</span></span>

<span data-ttu-id="b914b-135">Pour créer le hachage d’une grande quantité de données, appelez la méthode de [**hachage**](hasheddata-hash.md) pour chaque élément de données.</span><span class="sxs-lookup"><span data-stu-id="b914b-135">To create the hash of a large amount of data, call the [**Hash**](hasheddata-hash.md) method for each piece of data.</span></span> <span data-ttu-id="b914b-136">Le hachage de chaque élément de données est concaténé à la propriété [**value**](hasheddata-value.md) jusqu’à ce que la propriété soit lue.</span><span class="sxs-lookup"><span data-stu-id="b914b-136">The hash of each piece of data is concatenated to the [**Value**](hasheddata-value.md) property until the property is read.</span></span> <span data-ttu-id="b914b-137">Le contenu de la propriété **value** est réinitialisé lorsque la propriété est lue.</span><span class="sxs-lookup"><span data-stu-id="b914b-137">The contents of the **Value** property are reset when the property is read.</span></span>

<span data-ttu-id="b914b-138">L’objet **HashedData** peut être créé et il est sécurisé pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="b914b-138">The **HashedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="b914b-139">Le ProgID de l’objet **HashedData** est «CAPICOM. HashedData. 1».</span><span class="sxs-lookup"><span data-stu-id="b914b-139">The ProgID for the **HashedData** object is "CAPICOM.HashedData.1".</span></span>

## <a name="requirements"></a><span data-ttu-id="b914b-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b914b-140">Requirements</span></span>



| <span data-ttu-id="b914b-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b914b-141">Requirement</span></span> | <span data-ttu-id="b914b-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="b914b-142">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b914b-143">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b914b-143">End of client support</span></span><br/> | <span data-ttu-id="b914b-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b914b-144">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b914b-145">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="b914b-145">End of server support</span></span><br/> | <span data-ttu-id="b914b-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b914b-146">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b914b-147">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="b914b-147">Redistributable</span></span><br/>       | <span data-ttu-id="b914b-148">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="b914b-148">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b914b-149">DLL</span><span class="sxs-lookup"><span data-stu-id="b914b-149">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b914b-150"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b914b-150"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
