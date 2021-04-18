---
description: Un identificateur de langue est une abréviation numérique internationale standard pour la langue d’un pays ou d’une région géographique.
ms.assetid: 076e2a43-256a-4646-a5c8-1d48ab08ce1a
title: Identificateurs de langue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e3e8f88a64d49d04402c0e72a3946bcddc41e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519337"
---
# <a name="language-identifiers"></a><span data-ttu-id="6dc24-103">Identificateurs de langue</span><span class="sxs-lookup"><span data-stu-id="6dc24-103">Language Identifiers</span></span>

<span data-ttu-id="6dc24-104">Un identificateur de langue est une abréviation numérique internationale standard pour la [langue](locales-and-languages.md) d’un pays ou d’une région géographique.</span><span class="sxs-lookup"><span data-stu-id="6dc24-104">A language identifier is a standard international numeric abbreviation for the [language](locales-and-languages.md) in a country or geographical region.</span></span> <span data-ttu-id="6dc24-105">Chaque langue possède un identificateur de langue unique (LANGID de type de données), une valeur de 16 bits qui se compose d’un identificateur de langue primaire et d’un identificateur de sous-langue.</span><span class="sxs-lookup"><span data-stu-id="6dc24-105">Each language has a unique language identifier (data type LANGID), a 16-bit value that consists of a primary language identifier and a sublanguage identifier.</span></span> <span data-ttu-id="6dc24-106">Pour plus d’informations sur les identificateurs de langue, consultez [constantes et chaînes d’identificateur de langue](language-identifier-constants-and-strings.md).</span><span class="sxs-lookup"><span data-stu-id="6dc24-106">For details of language identifiers, see [Language Identifier Constants and Strings](language-identifier-constants-and-strings.md).</span></span>

<span data-ttu-id="6dc24-107">Un identificateur de langue est construit à l’aide de la macro [**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid) .</span><span class="sxs-lookup"><span data-stu-id="6dc24-107">A language identifier is constructed using the [**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid) macro.</span></span> <span data-ttu-id="6dc24-108">L’illustration suivante montre le format des bits dans un identificateur de langue.</span><span class="sxs-lookup"><span data-stu-id="6dc24-108">The following illustration shows the format of the bits in a language identifier.</span></span>

``` syntax
+-------------------------+-------------------------+
|     SubLanguage ID      |   Primary Language ID   |
+-------------------------+-------------------------+
15                    10  9                         0   bit
```

<span data-ttu-id="6dc24-109">Les identificateurs de langue prédéfinis sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="6dc24-109">The following are predefined language identifiers:</span></span>

-   <span data-ttu-id="6dc24-110">langue \_ par défaut du système lang \_ .</span><span class="sxs-lookup"><span data-stu-id="6dc24-110">LANG\_SYSTEM\_DEFAULT.</span></span> <span data-ttu-id="6dc24-111">Langue par défaut du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="6dc24-111">The operating system default language.</span></span>
-   <span data-ttu-id="6dc24-112">langue \_ par défaut de l’utilisateur lang \_ .</span><span class="sxs-lookup"><span data-stu-id="6dc24-112">LANG\_USER\_DEFAULT.</span></span> <span data-ttu-id="6dc24-113">La langue de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="6dc24-113">The language of the current user.</span></span>

<span data-ttu-id="6dc24-114">Votre application peut récupérer les identificateurs de langue actuels à l’aide des fonctions de l' [interface utilisateur multilingue](multilingual-user-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="6dc24-114">Your application can retrieve the current language identifiers by using the [Multilingual User Interface](multilingual-user-interface.md) functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6dc24-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6dc24-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6dc24-116">Paramètres régionaux et langues</span><span class="sxs-lookup"><span data-stu-id="6dc24-116">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="6dc24-117">Constantes et chaînes de l’identificateur de langue</span><span class="sxs-lookup"><span data-stu-id="6dc24-117">Language Identifier Constants and Strings</span></span>](language-identifier-constants-and-strings.md)
</dt> <dt>

[<span data-ttu-id="6dc24-118">Interface utilisateur multilingue</span><span class="sxs-lookup"><span data-stu-id="6dc24-118">Multilingual User Interface</span></span>](multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="6dc24-119">**MAKELANGID**</span><span class="sxs-lookup"><span data-stu-id="6dc24-119">**MAKELANGID**</span></span>](/windows/desktop/api/Winnt/nf-winnt-makelangid)
</dt> </dl>

 

 



