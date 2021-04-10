---
description: Cette rubrique décrit les types de format pour les chaînes utilisées pour composer l’image de format d’une chaîne d’heure. Chaque image de format se compose d’une combinaison d’une chaîne de chacun des types de format.
ms.assetid: a5e87d88-4037-4302-99b7-179bfb03fac3
title: Images de format heure, minute et seconde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589c04fea0d6ce2f522436c30c39c873e3a7165e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042856"
---
# <a name="hour-minute-and-second-format-pictures"></a><span data-ttu-id="533e2-104">Images de format heure, minute et seconde</span><span class="sxs-lookup"><span data-stu-id="533e2-104">Hour, Minute, and Second Format Pictures</span></span>

<span data-ttu-id="533e2-105">Cette rubrique décrit les types de format pour les chaînes utilisées pour composer l’image de format d’une chaîne d’heure.</span><span class="sxs-lookup"><span data-stu-id="533e2-105">This topic describes the format types for strings used to compose the format picture for a time string.</span></span> <span data-ttu-id="533e2-106">Chaque image de format se compose d’une combinaison d’une chaîne de chacun des types de format.</span><span class="sxs-lookup"><span data-stu-id="533e2-106">Each format picture consists of a combination of one string of each of the format types.</span></span>

> [!Note]  
> <span data-ttu-id="533e2-107">Dans les types de format, les lettres « m », « s » et « t » doivent être en minuscules, et la lettre « h » doit être en minuscules pour indiquer l’heure sur 12 heures ou en majuscules (« H ») pour indiquer l’heure sur 24 heures.</span><span class="sxs-lookup"><span data-stu-id="533e2-107">In the format types, the letters "m", "s", and "t" must be lowercase, and the letter "h" must be lowercase to denote the 12-hour clock or uppercase ("H") to denote the 24-hour clock.</span></span>

<span data-ttu-id="533e2-108">Les guillemets simples peuvent être utilisés pour marquer les caractères qui doivent être affichés exactement comme spécifiés.</span><span class="sxs-lookup"><span data-stu-id="533e2-108">Single quotation marks can be used to mark characters that should be displayed exactly as specified.</span></span> <span data-ttu-id="533e2-109">Si l’application doit afficher un guillemet simple, elle doit placer deux guillemets simples dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="533e2-109">If the application must display a single quotation mark, it should place two single quotation marks in a row.</span></span> <span data-ttu-id="533e2-110">Par exemple, « ABC » « bar » est affiché sous la forme « abc’bar ».</span><span class="sxs-lookup"><span data-stu-id="533e2-110">For example, 'abc''bar', is displayed as "abc'bar".</span></span>

<span data-ttu-id="533e2-111">Le tableau suivant définit les types de format utilisés pour représenter les heures.</span><span class="sxs-lookup"><span data-stu-id="533e2-111">The following table defines the format types used to represent hours.</span></span>

| <span data-ttu-id="533e2-112">String</span><span class="sxs-lookup"><span data-stu-id="533e2-112">String</span></span> | <span data-ttu-id="533e2-113">Signification</span><span class="sxs-lookup"><span data-stu-id="533e2-113">Meaning</span></span>                                                             |
|--------|---------------------------------------------------------------------|
| <span data-ttu-id="533e2-114">h</span><span class="sxs-lookup"><span data-stu-id="533e2-114">h</span></span>      | <span data-ttu-id="533e2-115">Heures sans zéros non significatifs pour les heures à un chiffre (horloge de 12 heures).</span><span class="sxs-lookup"><span data-stu-id="533e2-115">Hours without leading zeros for single-digit hours (12-hour clock).</span></span> |
| <span data-ttu-id="533e2-116">hh</span><span class="sxs-lookup"><span data-stu-id="533e2-116">hh</span></span>     | <span data-ttu-id="533e2-117">Heures avec des zéros non significatifs pour les heures à un chiffre (horloge de 12 heures).</span><span class="sxs-lookup"><span data-stu-id="533e2-117">Hours with leading zeros for single-digit hours (12-hour clock).</span></span>    |
| <span data-ttu-id="533e2-118">H</span><span class="sxs-lookup"><span data-stu-id="533e2-118">H</span></span>      | <span data-ttu-id="533e2-119">Heures sans zéros non significatifs pour les heures à un chiffre (24 heures).</span><span class="sxs-lookup"><span data-stu-id="533e2-119">Hours without leading zeros for single-digit hours (24-hour clock).</span></span> |
| <span data-ttu-id="533e2-120">HH</span><span class="sxs-lookup"><span data-stu-id="533e2-120">HH</span></span>     | <span data-ttu-id="533e2-121">Heures avec des zéros non significatifs pour les heures à un chiffre (24 heures).</span><span class="sxs-lookup"><span data-stu-id="533e2-121">Hours with leading zeros for single-digit hours (24-hour clock).</span></span>    |

<span data-ttu-id="533e2-122">Le tableau suivant définit les types de format utilisés pour représenter les minutes.</span><span class="sxs-lookup"><span data-stu-id="533e2-122">The following table defines the format types used to represent minutes.</span></span>

| <span data-ttu-id="533e2-123">String</span><span class="sxs-lookup"><span data-stu-id="533e2-123">String</span></span> | <span data-ttu-id="533e2-124">Signification</span><span class="sxs-lookup"><span data-stu-id="533e2-124">Meaning</span></span>                                                 |
|--------|---------------------------------------------------------|
| <span data-ttu-id="533e2-125">m</span><span class="sxs-lookup"><span data-stu-id="533e2-125">m</span></span>      | <span data-ttu-id="533e2-126">Minutes sans zéros non significatifs pour les minutes à un chiffre.</span><span class="sxs-lookup"><span data-stu-id="533e2-126">Minutes without leading zeros for single-digit minutes.</span></span> |
| <span data-ttu-id="533e2-127">MM</span><span class="sxs-lookup"><span data-stu-id="533e2-127">mm</span></span>     | <span data-ttu-id="533e2-128">Minutes avec des zéros non significatifs pour les minutes à un chiffre.</span><span class="sxs-lookup"><span data-stu-id="533e2-128">Minutes with leading zeros for single-digit minutes.</span></span>    |

<span data-ttu-id="533e2-129">Le tableau suivant définit les types de format utilisés pour représenter les secondes.</span><span class="sxs-lookup"><span data-stu-id="533e2-129">The following table defines the format types used to represent seconds.</span></span>

| <span data-ttu-id="533e2-130">String</span><span class="sxs-lookup"><span data-stu-id="533e2-130">String</span></span> | <span data-ttu-id="533e2-131">Signification</span><span class="sxs-lookup"><span data-stu-id="533e2-131">Meaning</span></span>                                                 |
|--------|---------------------------------------------------------|
| <span data-ttu-id="533e2-132">s</span><span class="sxs-lookup"><span data-stu-id="533e2-132">s</span></span>      | <span data-ttu-id="533e2-133">Secondes sans zéros non significatifs pour les secondes à un chiffre.</span><span class="sxs-lookup"><span data-stu-id="533e2-133">Seconds without leading zeros for single-digit seconds.</span></span> |
| <span data-ttu-id="533e2-134">ss</span><span class="sxs-lookup"><span data-stu-id="533e2-134">ss</span></span>     | <span data-ttu-id="533e2-135">Secondes avec des zéros non significatifs pour les secondes à un chiffre.</span><span class="sxs-lookup"><span data-stu-id="533e2-135">Seconds with leading zeros for single-digit seconds.</span></span>    |

<span data-ttu-id="533e2-136">Le tableau suivant définit les types de format utilisés pour représenter un marqueur d’heure.</span><span class="sxs-lookup"><span data-stu-id="533e2-136">The following table defines the format types used to represent a time marker.</span></span>

| <span data-ttu-id="533e2-137">String</span><span class="sxs-lookup"><span data-stu-id="533e2-137">String</span></span> | <span data-ttu-id="533e2-138">Signification</span><span class="sxs-lookup"><span data-stu-id="533e2-138">Meaning</span></span>|
| ---    | ---    |
| <span data-ttu-id="533e2-139">t</span><span class="sxs-lookup"><span data-stu-id="533e2-139">t</span></span>      | <span data-ttu-id="533e2-140">Chaîne de marqueur d’heure à un seul caractère.</span><span class="sxs-lookup"><span data-stu-id="533e2-140">One-character time marker string.</span></span><br /><span data-ttu-id="533e2-141">**Remarque :** Ce format n’est pas recommandé pour une utilisation avec certaines langues, telles que le japonais (Japon).</span><span class="sxs-lookup"><span data-stu-id="533e2-141">**Note:** This format is not recommended for use with certain languages, such as Japanese (Japan).</span></span> <span data-ttu-id="533e2-142">Avec ce format, une application prend toujours le premier caractère de la chaîne du marqueur d’heure, définie par [LOCALE_S1159](locale-s1159.md) (AM) et [LOCALE_S2359](locale-s2359.md) (PM).</span><span class="sxs-lookup"><span data-stu-id="533e2-142">With this format, an application always takes the first character from the time marker string, defined by [LOCALE_S1159](locale-s1159.md) (AM) and [LOCALE_S2359](locale-s2359.md) (PM).</span></span> <span data-ttu-id="533e2-143">Pour cette raison, l’application peut créer une mise en forme incorrecte avec la même chaîne utilisée pour AM et PM.</span><span class="sxs-lookup"><span data-stu-id="533e2-143">Because of this, the application can create incorrect formatting with the same string used for both AM and PM.</span></span>|
| <span data-ttu-id="533e2-144">tt</span><span class="sxs-lookup"><span data-stu-id="533e2-144">tt</span></span>     | <span data-ttu-id="533e2-145">Chaîne de marqueur d’heure à plusieurs caractères.</span><span class="sxs-lookup"><span data-stu-id="533e2-145">Multi-character time marker string.</span></span> |
