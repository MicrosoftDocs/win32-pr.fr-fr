---
title: Mappage de types de données de description de service à des types de données IDL
description: Le tableau suivant montre le mappage des types de données XML spécifiés dans une description de service aux types de données correspondants utilisés dans IDL.
ms.assetid: eeb86177-8c3b-47f1-bbe1-f9aabd2dde76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b5fac697c41f54279ecde7436900434895ff23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029673"
---
# <a name="mapping-service-description-data-types-to-idl-data-types"></a><span data-ttu-id="effa8-103">Mappage de types de données de description de service à des types de données IDL</span><span class="sxs-lookup"><span data-stu-id="effa8-103">Mapping Service Description Data Types to IDL Data Types</span></span>

<span data-ttu-id="effa8-104">Le tableau suivant montre le mappage des types de données XML spécifiés dans une description de service aux types de données correspondants utilisés dans IDL.</span><span class="sxs-lookup"><span data-stu-id="effa8-104">The following table shows the mapping of XML data types specified in a service description to the corresponding data types used in IDL.</span></span>



| <span data-ttu-id="effa8-105">Type de données XML</span><span class="sxs-lookup"><span data-stu-id="effa8-105">XML Data Type</span></span> | <span data-ttu-id="effa8-106">Type de données IDL</span><span class="sxs-lookup"><span data-stu-id="effa8-106">IDL Data Type</span></span>  |
|---------------|----------------|
| <span data-ttu-id="effa8-107">bin.base64</span><span class="sxs-lookup"><span data-stu-id="effa8-107">bin.base64</span></span>    | <span data-ttu-id="effa8-108">SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="effa8-108">SAFEARRAY</span></span>      |
| <span data-ttu-id="effa8-109">bin.hex</span><span class="sxs-lookup"><span data-stu-id="effa8-109">bin.hex</span></span>       | <span data-ttu-id="effa8-110">SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="effa8-110">SAFEARRAY</span></span>      |
| <span data-ttu-id="effa8-111">boolean</span><span class="sxs-lookup"><span data-stu-id="effa8-111">boolean</span></span>       | <span data-ttu-id="effa8-112">VARIANT \_ booléen</span><span class="sxs-lookup"><span data-stu-id="effa8-112">VARIANT\_BOOL</span></span>  |
| <span data-ttu-id="effa8-113">char</span><span class="sxs-lookup"><span data-stu-id="effa8-113">char</span></span>          | <span data-ttu-id="effa8-114">WCHAR \_ t</span><span class="sxs-lookup"><span data-stu-id="effa8-114">wchar\_t</span></span>       |
| <span data-ttu-id="effa8-115">Date</span><span class="sxs-lookup"><span data-stu-id="effa8-115">date</span></span>          | <span data-ttu-id="effa8-116">DATE</span><span class="sxs-lookup"><span data-stu-id="effa8-116">DATE</span></span>           |
| <span data-ttu-id="effa8-117">dateTime</span><span class="sxs-lookup"><span data-stu-id="effa8-117">dateTime</span></span>      | <span data-ttu-id="effa8-118">DATE</span><span class="sxs-lookup"><span data-stu-id="effa8-118">DATE</span></span>           |
| <span data-ttu-id="effa8-119">dateTime.tz</span><span class="sxs-lookup"><span data-stu-id="effa8-119">dateTime.tz</span></span>   | <span data-ttu-id="effa8-120">DATE</span><span class="sxs-lookup"><span data-stu-id="effa8-120">DATE</span></span>           |
| <span data-ttu-id="effa8-121">fixed.14.4</span><span class="sxs-lookup"><span data-stu-id="effa8-121">fixed.14.4</span></span>    | <span data-ttu-id="effa8-122">CY</span><span class="sxs-lookup"><span data-stu-id="effa8-122">CY</span></span>             |
| <span data-ttu-id="effa8-123">float</span><span class="sxs-lookup"><span data-stu-id="effa8-123">float</span></span>         | <span data-ttu-id="effa8-124">float</span><span class="sxs-lookup"><span data-stu-id="effa8-124">float</span></span>          |
| <span data-ttu-id="effa8-125">i1</span><span class="sxs-lookup"><span data-stu-id="effa8-125">i1</span></span>            | <span data-ttu-id="effa8-126">char</span><span class="sxs-lookup"><span data-stu-id="effa8-126">char</span></span>           |
| <span data-ttu-id="effa8-127">i2</span><span class="sxs-lookup"><span data-stu-id="effa8-127">i2</span></span>            | <span data-ttu-id="effa8-128">short</span><span class="sxs-lookup"><span data-stu-id="effa8-128">short</span></span>          |
| <span data-ttu-id="effa8-129">i4</span><span class="sxs-lookup"><span data-stu-id="effa8-129">i4</span></span>            | <span data-ttu-id="effa8-130">long</span><span class="sxs-lookup"><span data-stu-id="effa8-130">long</span></span>           |
| <span data-ttu-id="effa8-131">int</span><span class="sxs-lookup"><span data-stu-id="effa8-131">int</span></span>           | <span data-ttu-id="effa8-132">long</span><span class="sxs-lookup"><span data-stu-id="effa8-132">long</span></span>           |
| <span data-ttu-id="effa8-133">nombre</span><span class="sxs-lookup"><span data-stu-id="effa8-133">number</span></span>        | <span data-ttu-id="effa8-134">BSTR</span><span class="sxs-lookup"><span data-stu-id="effa8-134">BSTR</span></span>           |
| <span data-ttu-id="effa8-135">r4</span><span class="sxs-lookup"><span data-stu-id="effa8-135">r4</span></span>            | <span data-ttu-id="effa8-136">float</span><span class="sxs-lookup"><span data-stu-id="effa8-136">float</span></span>          |
| <span data-ttu-id="effa8-137">r8</span><span class="sxs-lookup"><span data-stu-id="effa8-137">r8</span></span>            | <span data-ttu-id="effa8-138">double</span><span class="sxs-lookup"><span data-stu-id="effa8-138">double</span></span>         |
| <span data-ttu-id="effa8-139">string</span><span class="sxs-lookup"><span data-stu-id="effa8-139">string</span></span>        | <span data-ttu-id="effa8-140">BSTR</span><span class="sxs-lookup"><span data-stu-id="effa8-140">BSTR</span></span>           |
| <span data-ttu-id="effa8-141">time</span><span class="sxs-lookup"><span data-stu-id="effa8-141">time</span></span>          | <span data-ttu-id="effa8-142">DATE</span><span class="sxs-lookup"><span data-stu-id="effa8-142">DATE</span></span>           |
| <span data-ttu-id="effa8-143">time.tz</span><span class="sxs-lookup"><span data-stu-id="effa8-143">time.tz</span></span>       | <span data-ttu-id="effa8-144">DATE</span><span class="sxs-lookup"><span data-stu-id="effa8-144">DATE</span></span>           |
| <span data-ttu-id="effa8-145">ui1</span><span class="sxs-lookup"><span data-stu-id="effa8-145">ui1</span></span>           | <span data-ttu-id="effa8-146">unsigned char</span><span class="sxs-lookup"><span data-stu-id="effa8-146">unsigned char</span></span>  |
| <span data-ttu-id="effa8-147">ui2</span><span class="sxs-lookup"><span data-stu-id="effa8-147">ui2</span></span>           | <span data-ttu-id="effa8-148">unsigned short</span><span class="sxs-lookup"><span data-stu-id="effa8-148">unsigned short</span></span> |
| <span data-ttu-id="effa8-149">ui4</span><span class="sxs-lookup"><span data-stu-id="effa8-149">ui4</span></span>           | <span data-ttu-id="effa8-150">unsigned long</span><span class="sxs-lookup"><span data-stu-id="effa8-150">unsigned long</span></span>  |
| <span data-ttu-id="effa8-151">URI</span><span class="sxs-lookup"><span data-stu-id="effa8-151">uri</span></span>           | <span data-ttu-id="effa8-152">BSTR</span><span class="sxs-lookup"><span data-stu-id="effa8-152">BSTR</span></span>           |
| <span data-ttu-id="effa8-153">uuid</span><span class="sxs-lookup"><span data-stu-id="effa8-153">uuid</span></span>          | <span data-ttu-id="effa8-154">BSTR</span><span class="sxs-lookup"><span data-stu-id="effa8-154">BSTR</span></span>           |



 

 

 




