---
description: Passez en revue la liste des valeurs du mode de conversion de l’éditeur de méthode d’entrée (IME). Ces valeurs sont utilisées avec les fonctions ImmGetConversionStatus et ImmSetConversionStatus.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Valeurs du mode de conversion IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c52bc2f8f6f9fc87df48a15c66ce24b33e51742
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406752"
---
# <a name="ime-conversion-mode-values"></a><span data-ttu-id="96756-104">Valeurs du mode de conversion IME</span><span class="sxs-lookup"><span data-stu-id="96756-104">IME Conversion Mode Values</span></span>

<span data-ttu-id="96756-105">Ces valeurs sont utilisées avec les fonctions [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) et [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="96756-105">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="96756-106">bit</span><span class="sxs-lookup"><span data-stu-id="96756-106">Bit</span></span>                      | <span data-ttu-id="96756-107">Signification</span><span class="sxs-lookup"><span data-stu-id="96756-107">Meaning</span></span>                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="96756-108">IME \_ CMODE \_ alphanumérique</span><span class="sxs-lookup"><span data-stu-id="96756-108">IME\_CMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="96756-109">Mode de saisie alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="96756-109">Alphanumeric input mode.</span></span> <span data-ttu-id="96756-110">Il s’agit de la valeur par défaut, définie comme 0x0000.</span><span class="sxs-lookup"><span data-stu-id="96756-110">This is the default, defined as 0x0000.</span></span>                          |
| <span data-ttu-id="96756-111">\_CHARCODE CMODE \_ IME</span><span class="sxs-lookup"><span data-stu-id="96756-111">IME\_CMODE\_CHARCODE</span></span>     | <span data-ttu-id="96756-112">Défini sur 1 si le mode de saisie du code du caractère ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="96756-112">Set to 1 if character code input mode; 0 if not.</span></span>                                          |
| <span data-ttu-id="96756-113">CMODE de l’IME \_ \_</span><span class="sxs-lookup"><span data-stu-id="96756-113">IME\_CMODE\_EUDC</span></span>         | <span data-ttu-id="96756-114">Défini sur 1 si le mode de conversion EUDC ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="96756-114">Set to 1 if EUDC conversion mode; 0 if not.</span></span>                                               |
| <span data-ttu-id="96756-115">\_CMODE IME \_ corrigé</span><span class="sxs-lookup"><span data-stu-id="96756-115">IME\_CMODE\_FIXED</span></span>        | <span data-ttu-id="96756-116">Windows **Me/98, windows 2000, Windows XP :** Défini sur 1 si le mode de conversion est fixe ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="96756-116">**Windows Me/98, Windows 2000, Windows XP:** Set to 1 if fixed conversion mode; 0 if not.</span></span> |
| <span data-ttu-id="96756-117">IME \_ CMODE \_ FULLSHAPE</span><span class="sxs-lookup"><span data-stu-id="96756-117">IME\_CMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="96756-118">Défini sur 1 en mode de forme complète ; 0 s’il s’agit du mode demi-forme.</span><span class="sxs-lookup"><span data-stu-id="96756-118">Set to 1 if full shape mode; 0 if half shape mode.</span></span>                                        |
| <span data-ttu-id="96756-119">IME \_ CMODE \_ HANJACONVERT</span><span class="sxs-lookup"><span data-stu-id="96756-119">IME\_CMODE\_HANJACONVERT</span></span> | <span data-ttu-id="96756-120">Défini sur 1 si le mode de conversion HANJA ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="96756-120">Set to 1 if HANJA convert mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="96756-121">\_CMODE IME \_ Katakana</span><span class="sxs-lookup"><span data-stu-id="96756-121">IME\_CMODE\_KATAKANA</span></span>     | <span data-ttu-id="96756-122">Défini sur 1 si le mode KATAKANA ; 0 en mode HIRAGANA.</span><span class="sxs-lookup"><span data-stu-id="96756-122">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                                            |
| <span data-ttu-id="96756-123">IME \_ CMODE \_ natif</span><span class="sxs-lookup"><span data-stu-id="96756-123">IME\_CMODE\_NATIVE</span></span>       | <span data-ttu-id="96756-124">Défini sur 1 en mode natif ; 0 si le mode est alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="96756-124">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                                          |
| <span data-ttu-id="96756-125">\_CMODE \_ NOconversion IME</span><span class="sxs-lookup"><span data-stu-id="96756-125">IME\_CMODE\_NOCONVERSION</span></span> | <span data-ttu-id="96756-126">Défini sur 1 pour empêcher le traitement des conversions par l’IME ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="96756-126">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span>                           |
| <span data-ttu-id="96756-127">\_CMODE \_ roman IME</span><span class="sxs-lookup"><span data-stu-id="96756-127">IME\_CMODE\_ROMAN</span></span>        | <span data-ttu-id="96756-128">Défini sur 1 si le mode d’entrée romain ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="96756-128">Set to 1 if ROMAN input mode; 0 if not.</span></span>                                                   |
| <span data-ttu-id="96756-129">IME \_ CMODE \_ SOFTKBD</span><span class="sxs-lookup"><span data-stu-id="96756-129">IME\_CMODE\_SOFTKBD</span></span>      | <span data-ttu-id="96756-130">Défini sur 1 si le mode de clavier logiciel est activé ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="96756-130">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="96756-131">\_symbole IME CMODE \_</span><span class="sxs-lookup"><span data-stu-id="96756-131">IME\_CMODE\_SYMBOL</span></span>       | <span data-ttu-id="96756-132">Défini sur 1 si le mode de conversion des symboles ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="96756-132">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                                             |



 

<span data-ttu-id="96756-133">Tous les autres bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="96756-133">All other bits are reserved.</span></span>

 

 



