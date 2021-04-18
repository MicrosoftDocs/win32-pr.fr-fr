---
description: Le service de détection de langage ELS est appelé Microsoft Détection de langue. Ce service utilise la technologie brevetée par Microsoft pour permettre aux applications de détecter la langue dans laquelle un texte spécifique est écrit.
ms.assetid: 11438e0b-d841-44d0-b68f-77868be4c92f
title: Détection de langue Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b395f6a1a320b66f00d996510b7cafc28b8e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533774"
---
# <a name="microsoft-language-detection"></a><span data-ttu-id="83ec3-104">Détection de langue Microsoft</span><span class="sxs-lookup"><span data-stu-id="83ec3-104">Microsoft Language Detection</span></span>

<span data-ttu-id="83ec3-105">Le service de détection de langage ELS est appelé Microsoft Détection de langue.</span><span class="sxs-lookup"><span data-stu-id="83ec3-105">The ELS language detection service is called Microsoft Language Detection.</span></span> <span data-ttu-id="83ec3-106">Ce service utilise la technologie brevetée par Microsoft pour permettre aux applications de détecter la langue dans laquelle un texte spécifique est écrit.</span><span class="sxs-lookup"><span data-stu-id="83ec3-106">This service uses Microsoft-patented technology to allow applications to detect the language in which specific text is written.</span></span>

## <a name="input-to-microsoft-language-detection"></a><span data-ttu-id="83ec3-107">Entrée à Microsoft Détection de langue</span><span class="sxs-lookup"><span data-stu-id="83ec3-107">Input to Microsoft Language Detection</span></span>

<span data-ttu-id="83ec3-108">L’entrée du service de Détection de langue Microsoft est le texte UTF-16 (formulaire normalisé C).</span><span class="sxs-lookup"><span data-stu-id="83ec3-108">The input to the Microsoft Language Detection service is UTF-16 (normalized form C) text.</span></span> <span data-ttu-id="83ec3-109">Le service doit déterminer la langue de ce texte.</span><span class="sxs-lookup"><span data-stu-id="83ec3-109">The service has to determine the language for this text.</span></span>

## <a name="output-of-microsoft-language-detection"></a><span data-ttu-id="83ec3-110">Sortie de Microsoft Détection de langue</span><span class="sxs-lookup"><span data-stu-id="83ec3-110">Output of Microsoft Language Detection</span></span>

<span data-ttu-id="83ec3-111">Le service de Détection de langue Microsoft récupère une liste de chaînes UTF-16 se terminant par un caractère null, représentée par leurs noms, séparés par des délimiteurs de caractères null.</span><span class="sxs-lookup"><span data-stu-id="83ec3-111">The Microsoft Language Detection service retrieves a double-null-terminated, registry-formatted UTF-16 string listing languages, represented by their names, separated by null character delimiters.</span></span> <span data-ttu-id="83ec3-112">La liste est triée par pertinence.</span><span class="sxs-lookup"><span data-stu-id="83ec3-112">The list is sorted by relevance.</span></span> <span data-ttu-id="83ec3-113">Pour la plupart des langues, des noms neutres sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="83ec3-113">For most languages, neutral names are used.</span></span> <span data-ttu-id="83ec3-114">Toutefois, pour certains, par exemple SR-Cyrl, SR-LATN, zh-Hant et zh-Hans, les noms complets sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="83ec3-114">However, for some, for example, sr-Cyrl, sr-Latn, zh-Hant, and zh-Hans, full names are used.</span></span>

## <a name="microsoft-language-detection-operation"></a><span data-ttu-id="83ec3-115">Opération de Détection de langue Microsoft</span><span class="sxs-lookup"><span data-stu-id="83ec3-115">Microsoft Language Detection Operation</span></span>

<span data-ttu-id="83ec3-116">Le service de Détection de langue Microsoft vérifie le script Unicode du texte fourni par l’application.</span><span class="sxs-lookup"><span data-stu-id="83ec3-116">The Microsoft Language Detection service checks the Unicode script of the text provided by the application.</span></span> <span data-ttu-id="83ec3-117">Il segmente le texte en fonction des scripts qu’il détecte, puis détermine la langue dans laquelle chaque segment est écrit.</span><span class="sxs-lookup"><span data-stu-id="83ec3-117">It segments the text based on the scripts that it detects, and then determines the language in which each segment is written.</span></span> <span data-ttu-id="83ec3-118">Si un script indique une seule langue, il est garanti que la langue est présente dans la liste des langages de sortie.</span><span class="sxs-lookup"><span data-stu-id="83ec3-118">If a script indicates a single language, the language is guaranteed to be present in the output list of languages.</span></span> <span data-ttu-id="83ec3-119">Le service utilise un algorithme breveté pour déterminer la pertinence de chaque langue prise en charge.</span><span class="sxs-lookup"><span data-stu-id="83ec3-119">The service uses a patented algorithm to determine the relevance of each supported language.</span></span>

## <a name="microsoft-language-detection-guid"></a><span data-ttu-id="83ec3-120">GUID de Microsoft Détection de langue</span><span class="sxs-lookup"><span data-stu-id="83ec3-120">Microsoft Language Detection GUID</span></span>

<span data-ttu-id="83ec3-121">Le GUID du service de Détection de langue Microsoft est déclaré dans Elssrvc. h, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="83ec3-121">The GUID for the Microsoft Language Detection service is declared in Elssrvc.h, as shown in the following code.</span></span>


```C++
// {CF7E00B1-909B-4d95-A8F4-611F7C377702}
static const GUID ELS_GUID_LANGUAGE_DETECTION =
    { 0xCF7E00B1, 0x909B, 0x4D95, { 0xA8, 0xF4, 0x61, 0x1F, 0x7C, 0x37, 0x77, 0x02 } };
```



## <a name="related-topics"></a><span data-ttu-id="83ec3-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="83ec3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83ec3-123">À propos des services linguistiques étendus</span><span class="sxs-lookup"><span data-stu-id="83ec3-123">About Extended Linguistic Services</span></span>](about-extended-linguistic-services.md)
</dt> </dl>

 

 



