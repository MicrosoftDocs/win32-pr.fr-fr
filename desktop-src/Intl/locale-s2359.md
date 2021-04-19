---
description: Paramètres régionaux \_ S2359 et paramètres régionaux \_
ms.assetid: 8a97073e-84f6-47d9-98fb-65760e8a6cd8
title: LOCALE_S2359 et LOCALE_SPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca0c22d541102fcdf0826778de591dc4100dda55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521085"
---
# <a name="locale_s2359-and-locale_spm"></a><span data-ttu-id="0404b-103">Paramètres régionaux \_ S2359 et paramètres régionaux \_</span><span class="sxs-lookup"><span data-stu-id="0404b-103">LOCALE\_S2359 and LOCALE\_SPM</span></span>

<span data-ttu-id="0404b-104">Chaîne pour l’indicateur PM (les 12 dernières heures du jour).</span><span class="sxs-lookup"><span data-stu-id="0404b-104">String for the PM designator (second 12 hours of the day).</span></span> <span data-ttu-id="0404b-105">Le nombre maximal de caractères autorisés pour cette chaîne est différent pour les différentes versions de Windows.</span><span class="sxs-lookup"><span data-stu-id="0404b-105">The maximum number of characters allowed for this string is different for different releases of Windows.</span></span>

<span data-ttu-id="0404b-106">**Windows XP :** Treize incluant un caractère null de fin pour [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="0404b-106">**Windows XP:** Thirteen including a terminating null character for [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span></span> <span data-ttu-id="0404b-107">Quinze incluant un caractère null de fin pour [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).</span><span class="sxs-lookup"><span data-stu-id="0404b-107">Fifteen including a terminating null character for [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).</span></span>

<span data-ttu-id="0404b-108">**Windows Me/98/95, Windows NT 4,0, windows 2000 :** Neuf incluant un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="0404b-108">**Windows Me/98/95, Windows NT 4.0, Windows 2000:** Nine including a terminating null character.</span></span>

<span data-ttu-id="0404b-109">**Windows Server 2003 et versions ultérieures :** Quinze incluant un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="0404b-109">**Windows Server 2003 and later:** Fifteen including a terminating null character.</span></span>

<span data-ttu-id="0404b-110">Windows 10 a ajouté la valeur **paramètres régionaux \_ SPM** comme synonyme plus lisible pour les **paramètres régionaux \_ S2359**.</span><span class="sxs-lookup"><span data-stu-id="0404b-110">Windows 10 added the value **LOCALE\_SPM** as a more readable synonym for **LOCALE\_S2359**.</span></span>

 

 



