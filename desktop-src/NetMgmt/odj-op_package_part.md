---
title: OP_PACKAGE_PART
description: Définition du OP_PACKAGE_PART IDL
ms.assetid: 8f13aa71-a7b2-41ee-ad1e-4953f49a391a
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74f299c58b9bf417a94119cd7520b7c0a364f73a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104199914"
---
# <a name="op_package_part-structure"></a><span data-ttu-id="4aea7-103">Structure OP_PACKAGE_PART</span><span class="sxs-lookup"><span data-stu-id="4aea7-103">OP_PACKAGE_PART structure</span></span>

<span data-ttu-id="4aea7-104">Définit une structure qui contient un jeu de données identifié par un GUID.</span><span class="sxs-lookup"><span data-stu-id="4aea7-104">Defines a structure that contains a data set identified by a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aea7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4aea7-105">Syntax</span></span>

```C++
typedef struct _OP_PACKAGE_PART
{
    GUID    PartType;
    ULONG   ulFlags;
    OP_BLOB Part;
    OP_BLOB Extension;
} OP_PACKAGE_PART, *POP_PACKAGE_PART;
```

## <a name="members"></a><span data-ttu-id="4aea7-106">Membres</span><span class="sxs-lookup"><span data-stu-id="4aea7-106">Members</span></span>

### <a name="parttype"></a><span data-ttu-id="4aea7-107">PartType</span><span class="sxs-lookup"><span data-stu-id="4aea7-107">PartType</span></span>

<span data-ttu-id="4aea7-108">Identifie la structure sérialisée contenue dans la partie en fonction du tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="4aea7-108">Identifies the serialized structure contained in Part per the following table:</span></span>

|<span data-ttu-id="4aea7-109">PartType</span><span class="sxs-lookup"><span data-stu-id="4aea7-109">PartType</span></span>|<span data-ttu-id="4aea7-110">Signification</span><span class="sxs-lookup"><span data-stu-id="4aea7-110">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="4aea7-111">GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}</span><span class="sxs-lookup"><span data-stu-id="4aea7-111">GUID_JOIN_PROVIDER {631c7621-5289-4321-bc9e-80f843f868c3}</span></span>|<span data-ttu-id="4aea7-112">Contient une structure ODJ_WIN7_BLOB sérialisée.</span><span class="sxs-lookup"><span data-stu-id="4aea7-112">Contains a serialized ODJ_WIN7_BLOB structure.</span></span>|
|<span data-ttu-id="4aea7-113">GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}</span><span class="sxs-lookup"><span data-stu-id="4aea7-113">GUID_JOIN_PROVIDER2 {57BFC56B-52F9-480C-ADCB-91B3F8A82317}</span></span>|<span data-ttu-id="4aea7-114">Contient une structure OP_JOIN_PROV2_PART sérialisée.</span><span class="sxs-lookup"><span data-stu-id="4aea7-114">Contains a serialized OP_JOIN_PROV2_PART structure.</span></span>|
|<span data-ttu-id="4aea7-115">GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}</span><span class="sxs-lookup"><span data-stu-id="4aea7-115">GUID_JOIN_PROVIDER3 {FC0CCF25-7FFA-474A-8611-69FFE269645F}</span></span>|<span data-ttu-id="4aea7-116">Contient une structure OP_JOIN_PROV3_PART sérialisée.</span><span class="sxs-lookup"><span data-stu-id="4aea7-116">Contains a serialized OP_JOIN_PROV3_PART structure.</span></span>|
|<span data-ttu-id="4aea7-117">GUID_CERT_PROVIDER {9c0971e9-832f-4873-8e87-ef1419d4781e}</span><span class="sxs-lookup"><span data-stu-id="4aea7-117">GUID_CERT_PROVIDER {9c0971e9-832f-4873-8e87-ef1419d4781e}</span></span>|<span data-ttu-id="4aea7-118">Contient une structure OP_CERT_PART sérialisée.</span><span class="sxs-lookup"><span data-stu-id="4aea7-118">Contains a serialized OP_CERT_PART structure.</span></span>|
|<span data-ttu-id="4aea7-119">GUID_POLICY_PROVIDER {68fb602a-0c09-48CE-b75f-07b7bd58f7ec}</span><span class="sxs-lookup"><span data-stu-id="4aea7-119">GUID_POLICY_PROVIDER {68fb602a-0c09-48ce-b75f-07b7bd58f7ec}</span></span>|<span data-ttu-id="4aea7-120">Contient une structure OP_POLICY_PART sérialisée.</span><span class="sxs-lookup"><span data-stu-id="4aea7-120">Contains a serialized OP_POLICY_PART structure.</span></span>|

### <a name="ulflags"></a><span data-ttu-id="4aea7-121">ulFlags</span><span class="sxs-lookup"><span data-stu-id="4aea7-121">ulFlags</span></span>

<span data-ttu-id="4aea7-122">Doit être défini sur zéro, un ou plusieurs des indicateurs suivants :</span><span class="sxs-lookup"><span data-stu-id="4aea7-122">Must be set to zero or more of the following flags:</span></span>

|<span data-ttu-id="4aea7-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="4aea7-123">Value</span></span>|<span data-ttu-id="4aea7-124">Signification</span><span class="sxs-lookup"><span data-stu-id="4aea7-124">Meaning</span></span>|
| --- | --- |
|<span data-ttu-id="4aea7-125">OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="4aea7-125">OPSPI_PACKAGE_PART_ESSENTIAL (0x00000001)</span></span>|<span data-ttu-id="4aea7-126">Cette partie de package est considérée comme essentielle.</span><span class="sxs-lookup"><span data-stu-id="4aea7-126">This package part is considered essential.</span></span> <span data-ttu-id="4aea7-127">Si le consommateur ne reconnaît pas ce composant de package ou ne parvient pas à le traiter correctement, l’opération globale doit échouer.</span><span class="sxs-lookup"><span data-stu-id="4aea7-127">If the consumer does not recognize this package part or fails to successfully process it, the overall operation must fail.</span></span>|

### <a name="part"></a><span data-ttu-id="4aea7-128">Partie</span><span class="sxs-lookup"><span data-stu-id="4aea7-128">Part</span></span>

<span data-ttu-id="4aea7-129">Contient une structure sérialisée dans une structure OP_BLOB.</span><span class="sxs-lookup"><span data-stu-id="4aea7-129">Contains a serialized structure in an OP_BLOB structure.</span></span> <span data-ttu-id="4aea7-130">La structure spécifique est déterminée par PartType.</span><span class="sxs-lookup"><span data-stu-id="4aea7-130">The specific structure is determined by PartType.</span></span>

### <a name="extension"></a><span data-ttu-id="4aea7-131">Extension</span><span class="sxs-lookup"><span data-stu-id="4aea7-131">Extension</span></span>

<span data-ttu-id="4aea7-132">Réservé pour une utilisation ultérieure et doit être défini sur tous les zéros.</span><span class="sxs-lookup"><span data-stu-id="4aea7-132">Reserved for future use and MUST be set to all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="4aea7-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4aea7-133">See also</span></span>

[<span data-ttu-id="4aea7-134">**Définitions IDL de jonction de domaine hors connexion**</span><span class="sxs-lookup"><span data-stu-id="4aea7-134">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="4aea7-135">**\_objet BLOB op**</span><span class="sxs-lookup"><span data-stu-id="4aea7-135">**OP\_BLOB**</span></span>](odj-op_blob.md)
