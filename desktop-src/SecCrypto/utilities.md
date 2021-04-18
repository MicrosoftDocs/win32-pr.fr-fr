---
description: Fournit des fonctionnalités pour la génération de nombres aléatoires, les conversions et l’encodage et le décodage à partir de base64.
ms.assetid: c0073361-5d0d-4915-8110-02f6e1e0714e
title: Objet Utilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2f6000179b1752630f02d03aa5c87dea11364d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540614"
---
# <a name="utilities-object"></a><span data-ttu-id="2f21b-103">Objet Utilities</span><span class="sxs-lookup"><span data-stu-id="2f21b-103">Utilities object</span></span>

<span data-ttu-id="2f21b-104">\[L’objet **Utilities** peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.\]</span><span class="sxs-lookup"><span data-stu-id="2f21b-104">\[The **Utilities** object is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="2f21b-105">L’objet **Utilities** fournit des fonctionnalités pour la génération de nombres aléatoires, les conversions et l’encodage et le décodage à partir de base64.</span><span class="sxs-lookup"><span data-stu-id="2f21b-105">The **Utilities** object provides functionality for random number generation, conversions, and encoding and decoding from base64.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="2f21b-106">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="2f21b-106">When to use</span></span>

<span data-ttu-id="2f21b-107">L’objet **Utilities** est utilisé pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="2f21b-107">The **Utilities** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="2f21b-108">Encoder une chaîne en base64 ou décoder une chaîne de base64.</span><span class="sxs-lookup"><span data-stu-id="2f21b-108">Encode a string as base64 or decode a string from base64.</span></span>
-   <span data-ttu-id="2f21b-109">Convertit une chaîne binaire compressée en un tableau d’octets, et vice versa.</span><span class="sxs-lookup"><span data-stu-id="2f21b-109">Convert a binary-packed string to a byte array and vice versa.</span></span>
-   <span data-ttu-id="2f21b-110">Convertit une chaîne binaire compressée en chaîne hexadécimale, et vice versa.</span><span class="sxs-lookup"><span data-stu-id="2f21b-110">Convert a binary-packed string to a hexadecimal string and vice versa.</span></span>
-   <span data-ttu-id="2f21b-111">Générez un nombre aléatoire sécurisé.</span><span class="sxs-lookup"><span data-stu-id="2f21b-111">Generate a secure random number.</span></span>
-   <span data-ttu-id="2f21b-112">Convertit l’heure locale en temps universel coordonné (heure de Greenwich) et vice versa.</span><span class="sxs-lookup"><span data-stu-id="2f21b-112">Convert local time to Coordinated Universal Time (Greenwich Mean Time) and vice versa.</span></span>

## <a name="members"></a><span data-ttu-id="2f21b-113">Membres</span><span class="sxs-lookup"><span data-stu-id="2f21b-113">Members</span></span>

<span data-ttu-id="2f21b-114">L’objet **Utilities** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2f21b-114">The **Utilities** object has these types of members:</span></span>

-   [<span data-ttu-id="2f21b-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2f21b-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2f21b-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="2f21b-116">Methods</span></span>

<span data-ttu-id="2f21b-117">L’objet **Utilities** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="2f21b-117">The **Utilities** object has these methods.</span></span>



| <span data-ttu-id="2f21b-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="2f21b-118">Method</span></span>                                                               | <span data-ttu-id="2f21b-119">Description</span><span class="sxs-lookup"><span data-stu-id="2f21b-119">Description</span></span>                                                                  |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="2f21b-120">**Base64Decode**</span><span class="sxs-lookup"><span data-stu-id="2f21b-120">**Base64Decode**</span></span>](utilities-base64decode.md)                       | <span data-ttu-id="2f21b-121">Décode une chaîne de base64.</span><span class="sxs-lookup"><span data-stu-id="2f21b-121">Decodes a string from base64.</span></span><br/>                                     |
| [<span data-ttu-id="2f21b-122">**Base64Encode**</span><span class="sxs-lookup"><span data-stu-id="2f21b-122">**Base64Encode**</span></span>](utilities-base64encode.md)                       | <span data-ttu-id="2f21b-123">Encode une chaîne au format Base64.</span><span class="sxs-lookup"><span data-stu-id="2f21b-123">Encodes a string as base64.</span></span><br/>                                       |
| [<span data-ttu-id="2f21b-124">**BinaryStringToByteArray**</span><span class="sxs-lookup"><span data-stu-id="2f21b-124">**BinaryStringToByteArray**</span></span>](utilities-binarystringtobytearray.md) | <span data-ttu-id="2f21b-125">Convertit une chaîne binaire compressée en un tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="2f21b-125">Converts a binary-packed string to an array of bytes.</span></span><br/>             |
| [<span data-ttu-id="2f21b-126">**BinaryToHex**</span><span class="sxs-lookup"><span data-stu-id="2f21b-126">**BinaryToHex**</span></span>](utilities-binarytohex.md)                         | <span data-ttu-id="2f21b-127">Convertit une chaîne binaire compressée en chaîne hexadécimale.</span><span class="sxs-lookup"><span data-stu-id="2f21b-127">Converts a binary-packed string to a hexadecimal string.</span></span><br/>          |
| [<span data-ttu-id="2f21b-128">**ByteArrayToBinaryString**</span><span class="sxs-lookup"><span data-stu-id="2f21b-128">**ByteArrayToBinaryString**</span></span>](utilities-bytearraytobinarystring.md) | <span data-ttu-id="2f21b-129">Convertit un tableau d’octets en une chaîne condensé binaire.</span><span class="sxs-lookup"><span data-stu-id="2f21b-129">Converts an array of bytes to a binary-packed string.</span></span><br/>             |
| [<span data-ttu-id="2f21b-130">**GetRandom**</span><span class="sxs-lookup"><span data-stu-id="2f21b-130">**GetRandom**</span></span>](utilities-getrandom.md)                             | <span data-ttu-id="2f21b-131">Génère un nombre aléatoire sécurisé.</span><span class="sxs-lookup"><span data-stu-id="2f21b-131">Generates a secure random number.</span></span><br/>                                 |
| [<span data-ttu-id="2f21b-132">**HexToBinary**</span><span class="sxs-lookup"><span data-stu-id="2f21b-132">**HexToBinary**</span></span>](utilities-hextobinary.md)                         | <span data-ttu-id="2f21b-133">Convertit une chaîne hexadécimale en chaîne binaire.</span><span class="sxs-lookup"><span data-stu-id="2f21b-133">Converts a hexadecimal string to a binary-packed string.</span></span><br/>          |
| [<span data-ttu-id="2f21b-134">**LocalTimeToUTCTime**</span><span class="sxs-lookup"><span data-stu-id="2f21b-134">**LocalTimeToUTCTime**</span></span>](utilities-localtimetoutctime.md)           | <span data-ttu-id="2f21b-135">Convertit l’heure locale de l’ordinateur en temps universel coordonné.</span><span class="sxs-lookup"><span data-stu-id="2f21b-135">Converts the computer's local time to Coordinated Universal Time.</span></span><br/> |
| [<span data-ttu-id="2f21b-136">**UTCTimeToLocalTime**</span><span class="sxs-lookup"><span data-stu-id="2f21b-136">**UTCTimeToLocalTime**</span></span>](utilities-utctimetolocaltime.md)           | <span data-ttu-id="2f21b-137">Convertit le temps universel coordonné en heure locale de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2f21b-137">Converts Coordinated Universal Time to the computer's local time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2f21b-138">Notes</span><span class="sxs-lookup"><span data-stu-id="2f21b-138">Remarks</span></span>

<span data-ttu-id="2f21b-139">L’objet **Utilities** peut être créé et il est sécurisé pour les scripts.</span><span class="sxs-lookup"><span data-stu-id="2f21b-139">The **Utilities** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="2f21b-140">Le ProgID de l’objet **Utilities** est CAPICOM. Utilities. 1.</span><span class="sxs-lookup"><span data-stu-id="2f21b-140">The ProgID for the **Utilities** object is CAPICOM.Utilities.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f21b-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f21b-141">Requirements</span></span>



| <span data-ttu-id="2f21b-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f21b-142">Requirement</span></span> | <span data-ttu-id="2f21b-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f21b-143">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f21b-144">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="2f21b-144">Redistributable</span></span><br/> | <span data-ttu-id="2f21b-145">CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP</span><span class="sxs-lookup"><span data-stu-id="2f21b-145">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2f21b-146">DLL</span><span class="sxs-lookup"><span data-stu-id="2f21b-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="2f21b-147"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f21b-147"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




