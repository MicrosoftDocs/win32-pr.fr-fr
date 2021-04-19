---
description: paramètres régionaux \_ ILANGUAGE
ms.assetid: 8f80a941-8ba6-4a0d-92fa-77230fe0a9d1
title: LOCALE_ILANGUAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b68ccd270319fa00cd2e983b5f9159d454f160
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516407"
---
# <a name="locale_ilanguage"></a><span data-ttu-id="a8efc-103">paramètres régionaux \_ ILANGUAGE</span><span class="sxs-lookup"><span data-stu-id="a8efc-103">LOCALE\_ILANGUAGE</span></span>

<span data-ttu-id="a8efc-104">[Identificateur de langue](language-identifiers.md) avec une valeur hexadécimale.</span><span class="sxs-lookup"><span data-stu-id="a8efc-104">[Language identifier](language-identifiers.md) with a hexadecimal value.</span></span> <span data-ttu-id="a8efc-105">Par exemple, l’anglais (États-Unis) a la valeur 0409, qui indique 0x0409 hexadécimal, et est équivalent à 1033 décimal.</span><span class="sxs-lookup"><span data-stu-id="a8efc-105">For example, English (United States) has the value 0409, which indicates 0x0409 hexadecimal, and is equivalent to 1033 decimal.</span></span> <span data-ttu-id="a8efc-106">Le nombre maximal de caractères autorisés pour cette chaîne est de cinq, y compris un caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="a8efc-106">The maximum number of characters allowed for this string is five, including a terminating null character.</span></span>

<span data-ttu-id="a8efc-107">**Windows Vista et versions ultérieures :** L’utilisation de cette constante peut entraîner le renvoi d’un identificateur de paramètres régionaux non valides par [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) .</span><span class="sxs-lookup"><span data-stu-id="a8efc-107">**Windows Vista and later:** Use of this constant can cause [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) to return an invalid locale identifier.</span></span> <span data-ttu-id="a8efc-108">Votre application doit utiliser la constante [locale \_ sName](locale-sname.md) lors de l’appel de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="a8efc-108">Your application should use the [LOCALE\_SNAME](locale-sname.md) constant when calling this function.</span></span>

 

 



