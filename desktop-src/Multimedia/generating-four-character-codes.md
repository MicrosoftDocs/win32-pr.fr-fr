---
title: Génération de codes Four-Character
description: Génération de codes Four-Character
ms.assetid: dfb771f1-9273-4f60-a3af-3a62a3794e59
keywords:
- e/s de fichier multimédia, codes à quatre caractères
- e/s de fichier, codes à quatre caractères
- entrées et sorties (e/s), codes à quatre caractères
- E/s (entrée et sortie), codes à quatre caractères
- codes à quatre caractères
- mmioStringToFOURCC fonction)
- mmioFOURCC macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c83540b49d83ee325479542e5a2917ac61ce19b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725124"
---
# <a name="generating-four-character-codes"></a><span data-ttu-id="0b3cf-110">Génération de codes Four-Character</span><span class="sxs-lookup"><span data-stu-id="0b3cf-110">Generating Four-Character Codes</span></span>

<span data-ttu-id="0b3cf-111">Vous pouvez utiliser la macro [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) ou la fonction [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) pour générer des codes à quatre caractères.</span><span class="sxs-lookup"><span data-stu-id="0b3cf-111">You can use the [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc) macro or the [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) function to generate four-character codes.</span></span> <span data-ttu-id="0b3cf-112">L’exemple suivant utilise **mmioFOURCC** pour générer un code à quatre caractères pour « Wave ».</span><span class="sxs-lookup"><span data-stu-id="0b3cf-112">The following example uses **mmioFOURCC** to generate a four-character code for "WAVE".</span></span>


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioFOURCC('W', 'A', 'V', 'E'); 
 
```



<span data-ttu-id="0b3cf-113">L’exemple suivant utilise [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) pour générer un code à quatre caractères pour « Wave ».</span><span class="sxs-lookup"><span data-stu-id="0b3cf-113">The following example uses [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) to generate a four-character code for "WAVE".</span></span>


```C++
FOURCC fourccID; 
. 
. 
. 
fourccID = mmioStringToFOURCC("WAVE", 0); 
```



<span data-ttu-id="0b3cf-114">Le deuxième paramètre dans [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) spécifie des indicateurs pour la conversion de la chaîne en code à quatre caractères.</span><span class="sxs-lookup"><span data-stu-id="0b3cf-114">The second parameter in [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc) specifies flags for converting the string to a four-character code.</span></span> <span data-ttu-id="0b3cf-115">Si vous spécifiez l' \_ indicateur MMIO TOUPPER, **mmioStringToFOURCC** convertit tous les caractères alphabétiques de la chaîne en majuscules.</span><span class="sxs-lookup"><span data-stu-id="0b3cf-115">If you specify the MMIO\_TOUPPER flag, **mmioStringToFOURCC** converts all alphabetic characters in the string to uppercase.</span></span> <span data-ttu-id="0b3cf-116">Cela est utile lorsque vous devez spécifier un code à quatre caractères pour identifier une procédure d’e/s personnalisée, car les codes à quatre caractères identifiant les noms d’extension de fichier doivent être en majuscules.</span><span class="sxs-lookup"><span data-stu-id="0b3cf-116">This is useful when you need to specify a four-character code to identify a custom I/O procedure because four-character codes identifying file-extension names must be all uppercase.</span></span>

 

 