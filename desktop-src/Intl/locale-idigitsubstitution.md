---
description: paramètres régionaux \_ IDIGITSUBSTITUTION
ms.assetid: f3f7d7ac-8f1e-4bfa-84f0-dfe8cff568c3
title: LOCALE_IDIGITSUBSTITUTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c063ed5b937c3e4c4ae06e40631b9795f6a73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112002"
---
# <a name="locale_idigitsubstitution"></a><span data-ttu-id="6274e-103">paramètres régionaux \_ IDIGITSUBSTITUTION</span><span class="sxs-lookup"><span data-stu-id="6274e-103">LOCALE\_IDIGITSUBSTITUTION</span></span>

<span data-ttu-id="6274e-104">**Windows 2000 :** Forme des chiffres.</span><span class="sxs-lookup"><span data-stu-id="6274e-104">**Windows 2000:** The shape of digits.</span></span> <span data-ttu-id="6274e-105">Par exemple, les chiffres arabe, thaï et Indo-aryen ont des formes classiques différentes des chiffres européens.</span><span class="sxs-lookup"><span data-stu-id="6274e-105">For example, Arabic, Thai, and Indic digits have classical shapes different from European digits.</span></span> <span data-ttu-id="6274e-106">Pour les paramètres régionaux avec les [paramètres régionaux \_ SNATIVEDIGITS](locale-snative-constants.md) spécifiés en tant que valeurs autres que ASCII 0-9, cette valeur spécifie si la préférence doit être donnée à ces autres chiffres à des fins d’affichage.</span><span class="sxs-lookup"><span data-stu-id="6274e-106">For locales with [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) specified as values other than ASCII 0-9, this value specifies whether preference should be given to those other digits for display purposes.</span></span> <span data-ttu-id="6274e-107">Par exemple, si vous choisissez la valeur 2, les chiffres spécifiés par les paramètres régionaux \_ SNATIVEDIGITS sont toujours utilisés.</span><span class="sxs-lookup"><span data-stu-id="6274e-107">For example, if a value of 2 is chosen, the digits specified by LOCALE\_SNATIVEDIGITS are always used.</span></span> <span data-ttu-id="6274e-108">Si 1 est choisi, les chiffres ASCII 0-9 sont toujours utilisés.</span><span class="sxs-lookup"><span data-stu-id="6274e-108">If a 1 is chosen, the ASCII 0-9 digits are always used.</span></span> <span data-ttu-id="6274e-109">Si un 0 est choisi, ASCII est utilisé dans certaines circonstances et les chiffres spécifiés par les paramètres régionaux \_ SNATIVEDIGITS sont utilisés dans d’autres, selon le contexte.</span><span class="sxs-lookup"><span data-stu-id="6274e-109">If a 0 is chosen, ASCII is used in some circumstances and the digits specified by LOCALE\_SNATIVEDIGITS are used in others, depending on the context.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6274e-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="6274e-110">Value</span></span></th>
<th><span data-ttu-id="6274e-111">Signification</span><span class="sxs-lookup"><span data-stu-id="6274e-111">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6274e-112">0</span><span class="sxs-lookup"><span data-stu-id="6274e-112">0</span></span></td>
<td><span data-ttu-id="6274e-113">Substitution basée sur le contexte.</span><span class="sxs-lookup"><span data-stu-id="6274e-113">Context-based substitution.</span></span> <span data-ttu-id="6274e-114">Les chiffres s’affichent en fonction du texte précédent dans la même sortie.</span><span class="sxs-lookup"><span data-stu-id="6274e-114">Digits are displayed based on the previous text in the same output.</span></span> <span data-ttu-id="6274e-115">Les chiffres européens suivent les scripts latins, Arabic-Indic chiffres suivent le texte arabe et d’autres chiffres nationaux suivent le texte écrit dans d’autres scripts.</span><span class="sxs-lookup"><span data-stu-id="6274e-115">European digits follow Latin scripts, Arabic-Indic digits follow Arabic text, and other national digits follow text written in various other scripts.</span></span> <span data-ttu-id="6274e-116">En l’absence de texte précédent, les paramètres régionaux et l’ordre de lecture affiché déterminent la substitution des chiffres, comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6274e-116">When there is no preceding text, the locale and the displayed reading order determine digit substitution, as shown in the following table.</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6274e-117">Paramètres régionaux</span><span class="sxs-lookup"><span data-stu-id="6274e-117">Locale</span></span></th>
<th><span data-ttu-id="6274e-118">Ordre de lecture</span><span class="sxs-lookup"><span data-stu-id="6274e-118">Reading order</span></span></th>
<th><span data-ttu-id="6274e-119">Chiffres utilisés</span><span class="sxs-lookup"><span data-stu-id="6274e-119">Digits used</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6274e-120">Arabe</span><span class="sxs-lookup"><span data-stu-id="6274e-120">Arabic</span></span></td>
<td><span data-ttu-id="6274e-121">De droite à gauche</span><span class="sxs-lookup"><span data-stu-id="6274e-121">Right-to-left</span></span></td>
<td><span data-ttu-id="6274e-122">Arabic-Indic</span><span class="sxs-lookup"><span data-stu-id="6274e-122">Arabic-Indic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6274e-123">Thaï</span><span class="sxs-lookup"><span data-stu-id="6274e-123">Thai</span></span></td>
<td><span data-ttu-id="6274e-124">De gauche à droite</span><span class="sxs-lookup"><span data-stu-id="6274e-124">Left-to-right</span></span></td>
<td><span data-ttu-id="6274e-125">Chiffres thaï</span><span class="sxs-lookup"><span data-stu-id="6274e-125">Thai digits</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6274e-126">Tous les autres</span><span class="sxs-lookup"><span data-stu-id="6274e-126">All others</span></span></td>
<td><span data-ttu-id="6274e-127">Quelconque</span><span class="sxs-lookup"><span data-stu-id="6274e-127">Any</span></span></td>
<td><span data-ttu-id="6274e-128">Aucune substitution utilisée</span><span class="sxs-lookup"><span data-stu-id="6274e-128">No substitution used</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6274e-129">1</span><span class="sxs-lookup"><span data-stu-id="6274e-129">1</span></span></td>
<td><span data-ttu-id="6274e-130">Aucune substitution utilisée.</span><span class="sxs-lookup"><span data-stu-id="6274e-130">No substitution used.</span></span> <span data-ttu-id="6274e-131">Compatibilité Unicode complète.</span><span class="sxs-lookup"><span data-stu-id="6274e-131">Full Unicode compatibility.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6274e-132">2</span><span class="sxs-lookup"><span data-stu-id="6274e-132">2</span></span></td>
<td><span data-ttu-id="6274e-133">Substitution de chiffres natifs.</span><span class="sxs-lookup"><span data-stu-id="6274e-133">Native digit substitution.</span></span> <span data-ttu-id="6274e-134">Les formes nationales sont affichées en fonction de LOCALE_SNATIVEDIGITS.</span><span class="sxs-lookup"><span data-stu-id="6274e-134">National shapes are displayed according to LOCALE_SNATIVEDIGITS.</span></span></td>
</tr>
</tbody>
</table>



 

 

 



