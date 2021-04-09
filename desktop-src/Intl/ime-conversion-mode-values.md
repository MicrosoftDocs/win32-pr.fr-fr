---
description: Ces valeurs sont utilisées avec les fonctions ImmGetConversionStatus et ImmSetConversionStatus.
ms.assetid: 0b0afb4e-f7aa-4ca6-9174-21983b2a422b
title: Valeurs du mode de conversion IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59b9f1a8d5015e78a5249d3499fc55e1a94d941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113623"
---
# <a name="ime-conversion-mode-values"></a><span data-ttu-id="ed15e-103">Valeurs du mode de conversion IME</span><span class="sxs-lookup"><span data-stu-id="ed15e-103">IME Conversion Mode Values</span></span>

<span data-ttu-id="ed15e-104">Ces valeurs sont utilisées avec les fonctions [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) et [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) .</span><span class="sxs-lookup"><span data-stu-id="ed15e-104">These values are used with the [**ImmGetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immgetconversionstatus) and [**ImmSetConversionStatus**](/windows/desktop/api/Imm/nf-imm-immsetconversionstatus) functions.</span></span>



| <span data-ttu-id="ed15e-105">bit</span><span class="sxs-lookup"><span data-stu-id="ed15e-105">Bit</span></span>                      | <span data-ttu-id="ed15e-106">Signification</span><span class="sxs-lookup"><span data-stu-id="ed15e-106">Meaning</span></span>                                                                                   |
|--------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed15e-107">IME \_ CMODE \_ alphanumérique</span><span class="sxs-lookup"><span data-stu-id="ed15e-107">IME\_CMODE\_ALPHANUMERIC</span></span> | <span data-ttu-id="ed15e-108">Mode de saisie alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="ed15e-108">Alphanumeric input mode.</span></span> <span data-ttu-id="ed15e-109">Il s’agit de la valeur par défaut, définie comme 0x0000.</span><span class="sxs-lookup"><span data-stu-id="ed15e-109">This is the default, defined as 0x0000.</span></span>                          |
| <span data-ttu-id="ed15e-110">\_CHARCODE CMODE \_ IME</span><span class="sxs-lookup"><span data-stu-id="ed15e-110">IME\_CMODE\_CHARCODE</span></span>     | <span data-ttu-id="ed15e-111">Défini sur 1 si le mode de saisie du code du caractère ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ed15e-111">Set to 1 if character code input mode; 0 if not.</span></span>                                          |
| <span data-ttu-id="ed15e-112">CMODE de l’IME \_ \_</span><span class="sxs-lookup"><span data-stu-id="ed15e-112">IME\_CMODE\_EUDC</span></span>         | <span data-ttu-id="ed15e-113">Défini sur 1 si le mode de conversion EUDC ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ed15e-113">Set to 1 if EUDC conversion mode; 0 if not.</span></span>                                               |
| <span data-ttu-id="ed15e-114">\_CMODE IME \_ corrigé</span><span class="sxs-lookup"><span data-stu-id="ed15e-114">IME\_CMODE\_FIXED</span></span>        | <span data-ttu-id="ed15e-115">Windows **Me/98, windows 2000, Windows XP :** Défini sur 1 si le mode de conversion est fixe ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ed15e-115">**Windows Me/98, Windows 2000, Windows XP:** Set to 1 if fixed conversion mode; 0 if not.</span></span> |
| <span data-ttu-id="ed15e-116">IME \_ CMODE \_ FULLSHAPE</span><span class="sxs-lookup"><span data-stu-id="ed15e-116">IME\_CMODE\_FULLSHAPE</span></span>    | <span data-ttu-id="ed15e-117">Défini sur 1 en mode de forme complète ; 0 s’il s’agit du mode demi-forme.</span><span class="sxs-lookup"><span data-stu-id="ed15e-117">Set to 1 if full shape mode; 0 if half shape mode.</span></span>                                        |
| <span data-ttu-id="ed15e-118">IME \_ CMODE \_ HANJACONVERT</span><span class="sxs-lookup"><span data-stu-id="ed15e-118">IME\_CMODE\_HANJACONVERT</span></span> | <span data-ttu-id="ed15e-119">Défini sur 1 si le mode de conversion HANJA ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ed15e-119">Set to 1 if HANJA convert mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="ed15e-120">\_CMODE IME \_ Katakana</span><span class="sxs-lookup"><span data-stu-id="ed15e-120">IME\_CMODE\_KATAKANA</span></span>     | <span data-ttu-id="ed15e-121">Défini sur 1 si le mode KATAKANA ; 0 en mode HIRAGANA.</span><span class="sxs-lookup"><span data-stu-id="ed15e-121">Set to 1 if KATAKANA mode; 0 if HIRAGANA mode.</span></span>                                            |
| <span data-ttu-id="ed15e-122">IME \_ CMODE \_ natif</span><span class="sxs-lookup"><span data-stu-id="ed15e-122">IME\_CMODE\_NATIVE</span></span>       | <span data-ttu-id="ed15e-123">Défini sur 1 en mode natif ; 0 si le mode est alphanumérique.</span><span class="sxs-lookup"><span data-stu-id="ed15e-123">Set to 1 if NATIVE mode; 0 if ALPHANUMERIC mode.</span></span>                                          |
| <span data-ttu-id="ed15e-124">\_CMODE \_ NOconversion IME</span><span class="sxs-lookup"><span data-stu-id="ed15e-124">IME\_CMODE\_NOCONVERSION</span></span> | <span data-ttu-id="ed15e-125">Défini sur 1 pour empêcher le traitement des conversions par l’IME ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ed15e-125">Set to 1 to prevent processing of conversions by IME; 0 if not.</span></span>                           |
| <span data-ttu-id="ed15e-126">\_CMODE \_ roman IME</span><span class="sxs-lookup"><span data-stu-id="ed15e-126">IME\_CMODE\_ROMAN</span></span>        | <span data-ttu-id="ed15e-127">Défini sur 1 si le mode d’entrée romain ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ed15e-127">Set to 1 if ROMAN input mode; 0 if not.</span></span>                                                   |
| <span data-ttu-id="ed15e-128">IME \_ CMODE \_ SOFTKBD</span><span class="sxs-lookup"><span data-stu-id="ed15e-128">IME\_CMODE\_SOFTKBD</span></span>      | <span data-ttu-id="ed15e-129">Défini sur 1 si le mode de clavier logiciel est activé ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ed15e-129">Set to 1 if Soft Keyboard mode; 0 if not.</span></span>                                                 |
| <span data-ttu-id="ed15e-130">\_symbole IME CMODE \_</span><span class="sxs-lookup"><span data-stu-id="ed15e-130">IME\_CMODE\_SYMBOL</span></span>       | <span data-ttu-id="ed15e-131">Défini sur 1 si le mode de conversion des symboles ; 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ed15e-131">Set to 1 if SYMBOL conversion mode; 0 if not.</span></span>                                             |



 

<span data-ttu-id="ed15e-132">Tous les autres bits sont réservés.</span><span class="sxs-lookup"><span data-stu-id="ed15e-132">All other bits are reserved.</span></span>

 

 



