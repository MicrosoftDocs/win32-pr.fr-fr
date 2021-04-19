---
description: Le type de données date/heure correspond à l’heure et à la date stockées individuellement, en utilisant des entiers non signés comme champs de bits, compressés comme suit.
ms.assetid: 02c6076e-7f81-489c-9997-1435dec81852
title: Heure/date
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b973143c2043419e4a54348917aa5d38fa97ff67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106517901"
---
# <a name="timedate"></a><span data-ttu-id="1c498-103">Heure/date</span><span class="sxs-lookup"><span data-stu-id="1c498-103">Time/Date</span></span>

<span data-ttu-id="1c498-104">Le type de données date/heure correspond à l’heure et à la date stockées individuellement, en utilisant des entiers non signés comme champs de bits, compressés comme suit.</span><span class="sxs-lookup"><span data-stu-id="1c498-104">The Time/Date data type has the time and the date stored individually, using unsigned integers as bit fields, packed as follows.</span></span>

## <a name="time"></a><span data-ttu-id="1c498-105">Temps</span><span class="sxs-lookup"><span data-stu-id="1c498-105">Time</span></span>

<span data-ttu-id="1c498-106">L’heure est encodée dans un entier non signé de 2 octets avec les champs de bits suivants.</span><span class="sxs-lookup"><span data-stu-id="1c498-106">Time is encoded in an unsigned 2-byte integer with the following bit fields.</span></span>



| <span data-ttu-id="1c498-107">Contenu</span><span class="sxs-lookup"><span data-stu-id="1c498-107">Contents</span></span>           | <span data-ttu-id="1c498-108">Bits</span><span class="sxs-lookup"><span data-stu-id="1c498-108">Bits</span></span>        | <span data-ttu-id="1c498-109">Plage de valeurs</span><span class="sxs-lookup"><span data-stu-id="1c498-109">Value range</span></span> |
|--------------------|-------------|-------------|
| <span data-ttu-id="1c498-110">heures</span><span class="sxs-lookup"><span data-stu-id="1c498-110">hours</span></span>              | <span data-ttu-id="1c498-111">0 1 2 3 4</span><span class="sxs-lookup"><span data-stu-id="1c498-111">0 1 2 3 4</span></span>   | <span data-ttu-id="1c498-112">0–23</span><span class="sxs-lookup"><span data-stu-id="1c498-112">0–23</span></span>        |
| <span data-ttu-id="1c498-113">minutes</span><span class="sxs-lookup"><span data-stu-id="1c498-113">minutes</span></span>            | <span data-ttu-id="1c498-114">5 6 7 8 9 A</span><span class="sxs-lookup"><span data-stu-id="1c498-114">5 6 7 8 9 A</span></span> | <span data-ttu-id="1c498-115">0–59</span><span class="sxs-lookup"><span data-stu-id="1c498-115">0–59</span></span>        |
| <span data-ttu-id="1c498-116">intervalles de 2 secondes</span><span class="sxs-lookup"><span data-stu-id="1c498-116">2-second intervals</span></span> | <span data-ttu-id="1c498-117">B C D E F</span><span class="sxs-lookup"><span data-stu-id="1c498-117">B C D E F</span></span>   | <span data-ttu-id="1c498-118">0 – 29</span><span class="sxs-lookup"><span data-stu-id="1c498-118">0–29</span></span>        |



 

## <a name="date"></a><span data-ttu-id="1c498-119">Date</span><span class="sxs-lookup"><span data-stu-id="1c498-119">Date</span></span>

<span data-ttu-id="1c498-120">La date est encodée dans un entier non signé de 2 octets avec les champs de bits suivants.</span><span class="sxs-lookup"><span data-stu-id="1c498-120">Date is encoded in an unsigned 2-byte integer with the following bit fields.</span></span>



| <span data-ttu-id="1c498-121">Contenu</span><span class="sxs-lookup"><span data-stu-id="1c498-121">Contents</span></span> | <span data-ttu-id="1c498-122">Bits</span><span class="sxs-lookup"><span data-stu-id="1c498-122">Bits</span></span>          | <span data-ttu-id="1c498-123">Plage de valeurs</span><span class="sxs-lookup"><span data-stu-id="1c498-123">Value range</span></span>              |
|----------|---------------|--------------------------|
| <span data-ttu-id="1c498-124">year</span><span class="sxs-lookup"><span data-stu-id="1c498-124">year</span></span>     | <span data-ttu-id="1c498-125">0 1 2 3 4 5 6</span><span class="sxs-lookup"><span data-stu-id="1c498-125">0 1 2 3 4 5 6</span></span> | <span data-ttu-id="1c498-126">0 – 119 (par rapport à 1980)</span><span class="sxs-lookup"><span data-stu-id="1c498-126">0–119 (relative to 1980)</span></span> |
| <span data-ttu-id="1c498-127">month</span><span class="sxs-lookup"><span data-stu-id="1c498-127">month</span></span>    | <span data-ttu-id="1c498-128">7 8 9 A</span><span class="sxs-lookup"><span data-stu-id="1c498-128">7 8 9 A</span></span>       | <span data-ttu-id="1c498-129">1–12</span><span class="sxs-lookup"><span data-stu-id="1c498-129">1–12</span></span>                     |
| <span data-ttu-id="1c498-130">day</span><span class="sxs-lookup"><span data-stu-id="1c498-130">day</span></span>      | <span data-ttu-id="1c498-131">B C D E F</span><span class="sxs-lookup"><span data-stu-id="1c498-131">B C D E F</span></span>     | <span data-ttu-id="1c498-132">1–31</span><span class="sxs-lookup"><span data-stu-id="1c498-132">1–31</span></span>                     |



 

 

 



