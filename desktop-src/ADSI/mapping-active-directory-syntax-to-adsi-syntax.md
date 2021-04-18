---
title: Mappage de Active Directory syntaxe à la syntaxe ADSI
description: Le tableau suivant mappe les syntaxes de Active Directory à leurs syntaxes ADSI correspondantes.
ms.assetid: ffb40eff-e137-4d6a-81e7-24d2cbbdbfbf
ms.tgt_platform: multiple
keywords:
- attributs ADSI, mappage Active Directory syntaxe à la syntaxe ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ba332a39a5d2452925f1a8f1cc8c8ca766ca10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512425"
---
# <a name="mapping-active-directory-syntax-to-adsi-syntax"></a><span data-ttu-id="bd5a9-104">Mappage de Active Directory syntaxe à la syntaxe ADSI</span><span class="sxs-lookup"><span data-stu-id="bd5a9-104">Mapping Active Directory Syntax to ADSI Syntax</span></span>

<span data-ttu-id="bd5a9-105">Le tableau suivant mappe les syntaxes de Active Directory à leurs syntaxes ADSI correspondantes.</span><span class="sxs-lookup"><span data-stu-id="bd5a9-105">The following table maps the Active Directory syntaxes to their corresponding ADSI syntaxes.</span></span>



| <span data-ttu-id="bd5a9-106">ID de la syntaxe d’attribut</span><span class="sxs-lookup"><span data-stu-id="bd5a9-106">Attribute syntax ID</span></span> | <span data-ttu-id="bd5a9-107">Type de syntaxe Active Directory</span><span class="sxs-lookup"><span data-stu-id="bd5a9-107">Active Directory syntax type</span></span>             | <span data-ttu-id="bd5a9-108">Type de syntaxe ADSI équivalent</span><span class="sxs-lookup"><span data-stu-id="bd5a9-108">Equivalent ADSI syntax type</span></span>                                         |
|---------------------|------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="bd5a9-109">2.5.5.1</span><span class="sxs-lookup"><span data-stu-id="bd5a9-109">2.5.5.1</span></span><br/>  | <span data-ttu-id="bd5a9-110">Chaîne DN</span><span class="sxs-lookup"><span data-stu-id="bd5a9-110">DN String</span></span><br/>                     | <span data-ttu-id="bd5a9-111">Chaîne DN</span><span class="sxs-lookup"><span data-stu-id="bd5a9-111">DN String</span></span><br/>                                                |
| <span data-ttu-id="bd5a9-112">2.5.5.2</span><span class="sxs-lookup"><span data-stu-id="bd5a9-112">2.5.5.2</span></span><br/>  | <span data-ttu-id="bd5a9-113">ID objet</span><span class="sxs-lookup"><span data-stu-id="bd5a9-113">Object ID</span></span><br/>                     | <span data-ttu-id="bd5a9-114">Chaîne CaseIgnore</span><span class="sxs-lookup"><span data-stu-id="bd5a9-114">CaseIgnore String</span></span><br/>                                        |
| <span data-ttu-id="bd5a9-115">2.5.5.3</span><span class="sxs-lookup"><span data-stu-id="bd5a9-115">2.5.5.3</span></span><br/>  | <span data-ttu-id="bd5a9-116">Chaîne respectant la casse</span><span class="sxs-lookup"><span data-stu-id="bd5a9-116">Case Sensitive String</span></span><br/>         | <span data-ttu-id="bd5a9-117">Chaîne CaseExact</span><span class="sxs-lookup"><span data-stu-id="bd5a9-117">CaseExact String</span></span><br/>                                         |
| <span data-ttu-id="bd5a9-118">2.5.5.4</span><span class="sxs-lookup"><span data-stu-id="bd5a9-118">2.5.5.4</span></span><br/>  | <span data-ttu-id="bd5a9-119">Chaîne case ignorée</span><span class="sxs-lookup"><span data-stu-id="bd5a9-119">Case Ignored String</span></span><br/>           | <span data-ttu-id="bd5a9-120">Chaîne CaseIgnore</span><span class="sxs-lookup"><span data-stu-id="bd5a9-120">CaseIgnore String</span></span><br/>                                        |
| <span data-ttu-id="bd5a9-121">2.5.5.5</span><span class="sxs-lookup"><span data-stu-id="bd5a9-121">2.5.5.5</span></span><br/>  | <span data-ttu-id="bd5a9-122">Imprimer la chaîne de cas</span><span class="sxs-lookup"><span data-stu-id="bd5a9-122">Print Case String</span></span><br/>             | <span data-ttu-id="bd5a9-123">Chaîne imprimable</span><span class="sxs-lookup"><span data-stu-id="bd5a9-123">Printable String</span></span><br/>                                         |
| <span data-ttu-id="bd5a9-124">2.5.5.6</span><span class="sxs-lookup"><span data-stu-id="bd5a9-124">2.5.5.6</span></span><br/>  | <span data-ttu-id="bd5a9-125">Chaîne numérique</span><span class="sxs-lookup"><span data-stu-id="bd5a9-125">Numeric String</span></span><br/>                | <span data-ttu-id="bd5a9-126">Chaîne numérique</span><span class="sxs-lookup"><span data-stu-id="bd5a9-126">Numeric String</span></span><br/>                                           |
| <span data-ttu-id="bd5a9-127">2.5.5.7</span><span class="sxs-lookup"><span data-stu-id="bd5a9-127">2.5.5.7</span></span><br/>  | <span data-ttu-id="bd5a9-128">**Ou** Nom DNWithOctetString</span><span class="sxs-lookup"><span data-stu-id="bd5a9-128">**OR** Name DNWithOctetString</span></span><br/> | <span data-ttu-id="bd5a9-129">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd5a9-129">Not Supported</span></span><br/>                                            |
| <span data-ttu-id="bd5a9-130">2.5.5.8</span><span class="sxs-lookup"><span data-stu-id="bd5a9-130">2.5.5.8</span></span><br/>  | <span data-ttu-id="bd5a9-131">Boolean</span><span class="sxs-lookup"><span data-stu-id="bd5a9-131">Boolean</span></span><br/>                       | <span data-ttu-id="bd5a9-132">Boolean</span><span class="sxs-lookup"><span data-stu-id="bd5a9-132">Boolean</span></span><br/>                                                  |
| <span data-ttu-id="bd5a9-133">2.5.5.9</span><span class="sxs-lookup"><span data-stu-id="bd5a9-133">2.5.5.9</span></span><br/>  | <span data-ttu-id="bd5a9-134">Integer</span><span class="sxs-lookup"><span data-stu-id="bd5a9-134">Integer</span></span><br/>                       | <span data-ttu-id="bd5a9-135">Integer</span><span class="sxs-lookup"><span data-stu-id="bd5a9-135">Integer</span></span><br/>                                                  |
| <span data-ttu-id="bd5a9-136">2.5.5.10</span><span class="sxs-lookup"><span data-stu-id="bd5a9-136">2.5.5.10</span></span><br/> | <span data-ttu-id="bd5a9-137">Chaîne d’octets</span><span class="sxs-lookup"><span data-stu-id="bd5a9-137">Octet String</span></span><br/>                  | <span data-ttu-id="bd5a9-138">Chaîne d’octets</span><span class="sxs-lookup"><span data-stu-id="bd5a9-138">Octet String</span></span><br/>                                             |
| <span data-ttu-id="bd5a9-139">2.5.5.11</span><span class="sxs-lookup"><span data-stu-id="bd5a9-139">2.5.5.11</span></span><br/> | <span data-ttu-id="bd5a9-140">Temps</span><span class="sxs-lookup"><span data-stu-id="bd5a9-140">Time</span></span><br/>                          | <span data-ttu-id="bd5a9-141">Heure UTC</span><span class="sxs-lookup"><span data-stu-id="bd5a9-141">UTC Time</span></span><br/>                                                 |
| <span data-ttu-id="bd5a9-142">2.5.5.12</span><span class="sxs-lookup"><span data-stu-id="bd5a9-142">2.5.5.12</span></span><br/> | <span data-ttu-id="bd5a9-143">Unicode</span><span class="sxs-lookup"><span data-stu-id="bd5a9-143">Unicode</span></span><br/>                       | <span data-ttu-id="bd5a9-144">Chaîne de cas ignore</span><span class="sxs-lookup"><span data-stu-id="bd5a9-144">Case Ignore String</span></span><br/>                                       |
| <span data-ttu-id="bd5a9-145">2.5.5.13</span><span class="sxs-lookup"><span data-stu-id="bd5a9-145">2.5.5.13</span></span><br/> | <span data-ttu-id="bd5a9-146">Adresse</span><span class="sxs-lookup"><span data-stu-id="bd5a9-146">Address</span></span><br/>                       | <span data-ttu-id="bd5a9-147">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd5a9-147">Not Supported</span></span><br/>                                            |
| <span data-ttu-id="bd5a9-148">2.5.5.14</span><span class="sxs-lookup"><span data-stu-id="bd5a9-148">2.5.5.14</span></span><br/> | <span data-ttu-id="bd5a9-149">Distname-Address</span><span class="sxs-lookup"><span data-stu-id="bd5a9-149">Distname-Address</span></span><br/>              |                                                                     |
| <span data-ttu-id="bd5a9-150">2.5.5.15</span><span class="sxs-lookup"><span data-stu-id="bd5a9-150">2.5.5.15</span></span><br/> | <span data-ttu-id="bd5a9-151">Descripteur de sécurité NT</span><span class="sxs-lookup"><span data-stu-id="bd5a9-151">NT Security Descriptor</span></span><br/>        | [<span data-ttu-id="bd5a9-152">**IADsSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="bd5a9-152">**IADsSecurityDescriptor**</span></span>](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)<br/> |
| <span data-ttu-id="bd5a9-153">2.5.5.16</span><span class="sxs-lookup"><span data-stu-id="bd5a9-153">2.5.5.16</span></span><br/> | <span data-ttu-id="bd5a9-154">Entier long</span><span class="sxs-lookup"><span data-stu-id="bd5a9-154">Large Integer</span></span><br/>                 | [<span data-ttu-id="bd5a9-155">**IADsLargeInteger**</span><span class="sxs-lookup"><span data-stu-id="bd5a9-155">**IADsLargeInteger**</span></span>](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)<br/>             |
| <span data-ttu-id="bd5a9-156">2.5.5.17</span><span class="sxs-lookup"><span data-stu-id="bd5a9-156">2.5.5.17</span></span><br/> | <span data-ttu-id="bd5a9-157">SID</span><span class="sxs-lookup"><span data-stu-id="bd5a9-157">SID</span></span><br/>                           | <span data-ttu-id="bd5a9-158">Chaîne d’octets</span><span class="sxs-lookup"><span data-stu-id="bd5a9-158">Octet String</span></span><br/>                                             |



 

 

 





