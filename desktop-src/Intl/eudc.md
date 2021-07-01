---
description: La clé de Registre EUDC contient une ou plusieurs sous-clés contenant des valeurs définissant les polices associées aux caractères définis par l’utilisateur (EUDCs) pour une page de codes donnée.
ms.assetid: d78a1d8f-a239-4388-aa21-c162953fe355
title: EUDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b583c7a0bfaa67684901e8d0a4a95ac5e45658
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120704"
---
# <a name="eudc"></a><span data-ttu-id="8572d-103">EUDC</span><span class="sxs-lookup"><span data-stu-id="8572d-103">EUDC</span></span>

<span data-ttu-id="8572d-104">La clé de Registre EUDC contient une ou plusieurs sous-clés contenant des valeurs définissant les polices associées aux [caractères définis par l’utilisateur (EUDCs)](end-user-defined-characters.md) pour une page de codes donnée.</span><span class="sxs-lookup"><span data-stu-id="8572d-104">The EUDC registry key contains one or more subkeys containing values defining the fonts associated with [end-user-defined characters (EUDCs)](end-user-defined-characters.md) for a given code page.</span></span> <span data-ttu-id="8572d-105">Il a l’emplacement de Registre suivant :</span><span class="sxs-lookup"><span data-stu-id="8572d-105">It has the following registry location:</span></span>

<span data-ttu-id="8572d-106">HKEY \_ Current \_ User \\ EUDC</span><span class="sxs-lookup"><span data-stu-id="8572d-106">HKEY\_CURRENT\_USER\\EUDC</span></span>

<span data-ttu-id="8572d-107">Le format est le suivant :</span><span class="sxs-lookup"><span data-stu-id="8572d-107">The format is:</span></span>

<span data-ttu-id="8572d-108">EUDC SystemDefaultEUDCFont = TrueTypeEUDCFontFileName TrueTypeFontTypeface = TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="8572d-108">EUDC SystemDefaultEUDCFont=TrueTypeEUDCFontFileName TrueTypeFontTypeface=TrueTypeEUDCFontFileName</span></span>

<span data-ttu-id="8572d-109">où :</span><span class="sxs-lookup"><span data-stu-id="8572d-109">where:</span></span>



| <span data-ttu-id="8572d-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="8572d-110">Value</span></span>                         | <span data-ttu-id="8572d-111">Description</span><span class="sxs-lookup"><span data-stu-id="8572d-111">Description</span></span>                                                                                                                                         |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8572d-112">SystemDefaultEUDCFont</span><span class="sxs-lookup"><span data-stu-id="8572d-112">SystemDefaultEUDCFont</span></span>    | <span data-ttu-id="8572d-113">Nom prédéfini utilisé pour définir la police par défaut du système.</span><span class="sxs-lookup"><span data-stu-id="8572d-113">Predefined name used to set the system default font.</span></span> <span data-ttu-id="8572d-114">Il n’existe aucune police EUDC par défaut du système, sauf si cette entrée est explicitement spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8572d-114">There is no system default EUDC font unless this entry is explicitly specified.</span></span>     |
| <span data-ttu-id="8572d-115">TrueTypeFontTypeface</span><span class="sxs-lookup"><span data-stu-id="8572d-115">TrueTypeFontTypeface</span></span>     | <span data-ttu-id="8572d-116">Nom défini par l’utilisateur associé à une police TrueType non-EUDC.</span><span class="sxs-lookup"><span data-stu-id="8572d-116">User-defined name associated with a non-EUDC TrueType font.</span></span>                                                                              |
| <span data-ttu-id="8572d-117">TrueTypeEUDCFontFileName</span><span class="sxs-lookup"><span data-stu-id="8572d-117">TrueTypeEUDCFontFileName</span></span> | <span data-ttu-id="8572d-118">Chaîne composée du nom de fichier d’un fichier de police EUDC distinct.</span><span class="sxs-lookup"><span data-stu-id="8572d-118">String consisting of the file name of a separate EUDC font file.</span></span> <span data-ttu-id="8572d-119">Ce fichier identifie une police à associer à TrueTypeFontTypeface.</span><span class="sxs-lookup"><span data-stu-id="8572d-119">This file identifies a font to be associated with TrueTypeFontTypeface.</span></span> |



 

<span data-ttu-id="8572d-120">L’exemple suivant illustre la clé EUDC pour la page de codes 932.</span><span class="sxs-lookup"><span data-stu-id="8572d-120">The following example shows the EUDC key for code page 932.</span></span>


```C++
HKEY_CURRENT_USER\EUDC\932
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GTEUDC.TTF
```



<span data-ttu-id="8572d-121">L’exemple suivant définit la police EUDC par défaut du système sur EUDC. ttf et associe les polices EUDC distinctes Mineudc. ttf et Goteudc. ttf aux noms de police MS Mincho et MS Gothic, respectivement.</span><span class="sxs-lookup"><span data-stu-id="8572d-121">The following example sets the system default EUDC font to be Eudc.ttf and associates the separate EUDC fonts Mineudc.ttf and Goteudc.ttf with the font names MS Mincho and MS Gothic, respectively.</span></span>


```C++
SystemDefaultEUDCFont=EUDC.TTF
MS Mincho=MINEUDC.TTF
MS Gothic=GOTEUDC.TTF
```



<span data-ttu-id="8572d-122">Lorsque la page de codes Windows (système ACP) associée à la langue des programmes non-Unicode correspond à la sous-clé, le sous-système GDI recherche les paires de valeurs de la sous-clé pour obtenir des informations d’affichage sur le caractère.</span><span class="sxs-lookup"><span data-stu-id="8572d-122">When the Windows code page (system ACP) associated with the language for non-Unicode programs matches the subkey, the GDI subsystem looks to the subkey value pairs to obtain display information about the character.</span></span> <span data-ttu-id="8572d-123">Il recherche d’abord un nom correspondant à la police actuelle.</span><span class="sxs-lookup"><span data-stu-id="8572d-123">It first looks for a name matching the current font.</span></span> <span data-ttu-id="8572d-124">S’il n’y en a aucun, il examine la valeur SystemDefaultEUDCFont.</span><span class="sxs-lookup"><span data-stu-id="8572d-124">If there is none, it examines the SystemDefaultEUDCFont value.</span></span> <span data-ttu-id="8572d-125">Si aucune valeur n’est définie, GDI traite le caractère comme non défini.</span><span class="sxs-lookup"><span data-stu-id="8572d-125">If no value is defined, GDI treats the character as undefined.</span></span>

<span data-ttu-id="8572d-126">Notez que le texte lui-même n’a pas besoin d’être dans la page de codes Windows.</span><span class="sxs-lookup"><span data-stu-id="8572d-126">Note that the text itself does not have to be in the Windows code page.</span></span> <span data-ttu-id="8572d-127">Par exemple, supposons que la page de codes possède l’identificateur 1252, la page de codes Windows par défaut pour l’anglais.</span><span class="sxs-lookup"><span data-stu-id="8572d-127">For example, assume that the code page has the identifier 1252, the default Windows code page for English.</span></span> <span data-ttu-id="8572d-128">Une application transmet le point de code Unicode unique U + E000, dans la zone d’utilisation privée Unicode (PUA), à [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span><span class="sxs-lookup"><span data-stu-id="8572d-128">An application passes the single Unicode code point U+E000, in the Unicode private use area (PUA), to [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext).</span></span> <span data-ttu-id="8572d-129">Dans ce cas, GDI examine les valeurs de Registre inférieures à 1252 pour obtenir les informations de police pour les propriétés d’affichage de caractères.</span><span class="sxs-lookup"><span data-stu-id="8572d-129">In this case, GDI looks at the registry values under 1252 to obtain the font information for the character display properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8572d-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8572d-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8572d-131">Entrées de Registre EUDC</span><span class="sxs-lookup"><span data-stu-id="8572d-131">EUDC Registry Entries</span></span>](eudc-registry-entries.md)
</dt> <dt>

[<span data-ttu-id="8572d-132">EUDCCodeRange</span><span class="sxs-lookup"><span data-stu-id="8572d-132">EUDCCodeRange</span></span>](eudccoderange.md)
</dt> </dl>

 

 
