---
description: 'Les fonctions API Windows qui manipulent des caractères sont généralement implémentées dans l’un des trois formats suivants :'
ms.assetid: e7698f0b-dbcb-4cd0-9cb5-23a26edb966a
title: Unicode dans l'API Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5686a7f65edefb11458374b7f72262448becd6d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543722"
---
# <a name="unicode-in-the-windows-api"></a><span data-ttu-id="2a62a-103">Unicode dans l'API Windows</span><span class="sxs-lookup"><span data-stu-id="2a62a-103">Unicode in the Windows API</span></span>

<span data-ttu-id="2a62a-104">Les fonctions API Windows qui manipulent des caractères sont généralement implémentées dans l’un des trois formats suivants :</span><span class="sxs-lookup"><span data-stu-id="2a62a-104">Windows API functions that manipulate characters are generally implemented in one of three formats:</span></span>

-   <span data-ttu-id="2a62a-105">Une version générique qui peut être compilée pour les pages de codes Windows ou Unicode</span><span class="sxs-lookup"><span data-stu-id="2a62a-105">A generic version that can be compiled for either Windows code pages or Unicode</span></span>
-   <span data-ttu-id="2a62a-106">Une version de [page de codes Windows](code-pages.md) avec la lettre « A » utilisée pour indiquer « ANSI »</span><span class="sxs-lookup"><span data-stu-id="2a62a-106">A [Windows code page](code-pages.md) version with the letter "A" used to indicate "ANSI"</span></span>
-   <span data-ttu-id="2a62a-107">Une version [Unicode](unicode.md) avec la lettre « W » utilisée pour indiquer « grande »</span><span class="sxs-lookup"><span data-stu-id="2a62a-107">A [Unicode](unicode.md) version with the letter "W" used to indicate "wide"</span></span>

<span data-ttu-id="2a62a-108">Certaines fonctions plus récentes prennent uniquement en charge les versions Unicode.</span><span class="sxs-lookup"><span data-stu-id="2a62a-108">Some newer functions support only Unicode versions.</span></span> <span data-ttu-id="2a62a-109">Pour plus d’informations, consultez [conventions pour les prototypes de fonction](conventions-for-function-prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="2a62a-109">For more information, see [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span>

<span data-ttu-id="2a62a-110">Les rubriques suivantes traitent des types de données Unicode et de la façon dont ils sont utilisés dans les fonctions et les messages ; l’utilisation des ressources, des noms de fichiers et des arguments de ligne de commande ; et méthodes de conversion entre différents types de chaînes.</span><span class="sxs-lookup"><span data-stu-id="2a62a-110">The following topics discuss Unicode data types and how they are used in functions and messages; the use of resources, file names, and command line arguments; and methods of translating between different types of strings.</span></span>

-   [<span data-ttu-id="2a62a-111">Traduction automatique des messages</span><span class="sxs-lookup"><span data-stu-id="2a62a-111">Automatic Message Translation</span></span>](automatic-message-translation.md)
-   [<span data-ttu-id="2a62a-112">Jeux de caractères utilisés dans les noms de fichiers</span><span class="sxs-lookup"><span data-stu-id="2a62a-112">Character Sets Used in File Names</span></span>](character-sets-used-in-file-names.md)
-   [<span data-ttu-id="2a62a-113">Arguments de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="2a62a-113">Command Line Arguments</span></span>](command-line-arguments.md)
-   [<span data-ttu-id="2a62a-114">Conventions pour les prototypes de fonctions</span><span class="sxs-lookup"><span data-stu-id="2a62a-114">Conventions for Function Prototypes</span></span>](conventions-for-function-prototypes.md)
-   [<span data-ttu-id="2a62a-115">Fonctions C standard</span><span class="sxs-lookup"><span data-stu-id="2a62a-115">Standard C Functions</span></span>](standard-c-functions.md)
-   [<span data-ttu-id="2a62a-116">Différences de fonction de chaîne</span><span class="sxs-lookup"><span data-stu-id="2a62a-116">String Function Differences</span></span>](string-function-differences.md)
-   [<span data-ttu-id="2a62a-117">Conversion entre types chaîne</span><span class="sxs-lookup"><span data-stu-id="2a62a-117">Translation Between String Types</span></span>](translation-between-string-types.md)
-   [<span data-ttu-id="2a62a-118">Types de données Windows pour les chaînes</span><span class="sxs-lookup"><span data-stu-id="2a62a-118">Windows Data Types for Strings</span></span>](windows-data-types-for-strings.md)

## <a name="related-topics"></a><span data-ttu-id="2a62a-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a62a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a62a-120">À propos d’Unicode et des jeux de caractères</span><span class="sxs-lookup"><span data-stu-id="2a62a-120">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



