---
description: Les fonctions suivantes sont utilisées avec les jeux de caractères.
ms.assetid: 1799f5da-1391-4b6e-ac13-718017a77557
title: Unicode et fonctions de jeu de caractères
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6996139d8a9bb426c21a460ac2bcb1358e6c8e7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035055"
---
# <a name="unicode-and-character-set-functions"></a><span data-ttu-id="4ba93-103">Unicode et fonctions de jeu de caractères</span><span class="sxs-lookup"><span data-stu-id="4ba93-103">Unicode and Character Set Functions</span></span>

<span data-ttu-id="4ba93-104">Les fonctions suivantes sont utilisées avec les jeux de caractères.</span><span class="sxs-lookup"><span data-stu-id="4ba93-104">The following functions are used with character sets.</span></span>



| <span data-ttu-id="4ba93-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="4ba93-105">Function</span></span>                                                       | <span data-ttu-id="4ba93-106">Description</span><span class="sxs-lookup"><span data-stu-id="4ba93-106">Description</span></span>                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4ba93-107">**GetTextCharset**</span><span class="sxs-lookup"><span data-stu-id="4ba93-107">**GetTextCharset**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharset)                       | <span data-ttu-id="4ba93-108">Récupère un identificateur de jeu de caractères pour la police actuellement sélectionnée dans un contexte de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="4ba93-108">Retrieves a character set identifier for the font that is currently selected into a specified device context.</span></span>         |
| [<span data-ttu-id="4ba93-109">**GetTextCharsetInfo**</span><span class="sxs-lookup"><span data-stu-id="4ba93-109">**GetTextCharsetInfo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharsetinfo)               | <span data-ttu-id="4ba93-110">Récupère des informations sur le jeu de caractères de la police actuellement sélectionnée dans un contexte de périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="4ba93-110">Retrieves information about the character set of the font that is currently selected into a specified device context.</span></span> |
| [<span data-ttu-id="4ba93-111">**IsDBCSLeadByte**</span><span class="sxs-lookup"><span data-stu-id="4ba93-111">**IsDBCSLeadByte**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte)                       | <span data-ttu-id="4ba93-112">Détermine si un caractère spécifié est un octet de tête pour la page de codes Windows ANSI par défaut du système (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="4ba93-112">Determines if a specified character is a lead byte for the system default Windows ANSI code page (CP\_ACP).</span></span>           |
| [<span data-ttu-id="4ba93-113">**IsDBCSLeadByteEx**</span><span class="sxs-lookup"><span data-stu-id="4ba93-113">**IsDBCSLeadByteEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyteex)                   | <span data-ttu-id="4ba93-114">Détermine si un caractère spécifié est potentiellement un octet de tête.</span><span class="sxs-lookup"><span data-stu-id="4ba93-114">Determines if a specified character is potentially a lead byte.</span></span>                                                       |
| [<span data-ttu-id="4ba93-115">**IsTextUnicode**</span><span class="sxs-lookup"><span data-stu-id="4ba93-115">**IsTextUnicode**</span></span>](/windows/desktop/api/Winbase/nf-winbase-istextunicode)                         | <span data-ttu-id="4ba93-116">Détermine si une mémoire tampon est susceptible de contenir un formulaire de texte Unicode.</span><span class="sxs-lookup"><span data-stu-id="4ba93-116">Determines if a buffer is likely to contain a form of Unicode text.</span></span>                                                   |
| [<span data-ttu-id="4ba93-117">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="4ba93-117">**MultiByteToWideChar**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)             | <span data-ttu-id="4ba93-118">Mappe une chaîne de caractères à une chaîne UTF-16 (caractère élargi).</span><span class="sxs-lookup"><span data-stu-id="4ba93-118">Maps a character string to a UTF-16 (wide character) string.</span></span>                                                          |
| [<span data-ttu-id="4ba93-119">**TranslateCharsetInfo**</span><span class="sxs-lookup"><span data-stu-id="4ba93-119">**TranslateCharsetInfo**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-translatecharsetinfo)           | <span data-ttu-id="4ba93-120">Traduit les informations du jeu de caractères et définit tous les membres d’une structure de destination sur les valeurs appropriées.</span><span class="sxs-lookup"><span data-stu-id="4ba93-120">Translates character set information and sets all members of a destination structure to appropriate values.</span></span>           |
| [<span data-ttu-id="4ba93-121">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="4ba93-121">**WideCharToMultiByte**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)             | <span data-ttu-id="4ba93-122">Mappe une chaîne UTF-16 (caractère élargi) à une nouvelle chaîne de caractères.</span><span class="sxs-lookup"><span data-stu-id="4ba93-122">Maps a UTF-16 (wide character) string to a new character string.</span></span>                                                      |
| <span data-ttu-id="4ba93-123">[**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4ba93-123">[**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))</span></span>                       | <span data-ttu-id="4ba93-124">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="4ba93-124">Do not use.</span></span>                                                                                                           |
| [<span data-ttu-id="4ba93-125">**NlsDllCodePageTranslation**</span><span class="sxs-lookup"><span data-stu-id="4ba93-125">**NlsDllCodePageTranslation**</span></span>](/windows/desktop/api/Gb18030/nf-gb18030-nlsdllcodepagetranslation) | <span data-ttu-id="4ba93-126">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="4ba93-126">Do not use.</span></span>                                                                                                           |
| <span data-ttu-id="4ba93-127">[**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4ba93-127">[**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))</span></span>                       | <span data-ttu-id="4ba93-128">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="4ba93-128">Do not use.</span></span>                                                                                                           |



 

 

 
