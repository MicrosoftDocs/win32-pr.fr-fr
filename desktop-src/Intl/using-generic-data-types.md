---
description: Si vous utilisez des types de données génériques dans votre code, il peut être compilé pour Unicode simplement à l’aide d’une directive de préprocesseur pour définir &\# 0034 ; UNICODE&\# 0034 ; avant les \# instructions include pour les fichiers d’en-tête.
ms.assetid: 1c9cbb18-9295-4847-86c1-d596668cbe57
title: Utilisation des types de données génériques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e2604f87b12e86076bed47f509c6398fa8482b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531202"
---
# <a name="using-generic-data-types"></a><span data-ttu-id="52dea-103">Utilisation des types de données génériques</span><span class="sxs-lookup"><span data-stu-id="52dea-103">Using Generic Data Types</span></span>

<span data-ttu-id="52dea-104">Si vous utilisez des types de données génériques dans votre code, il peut être compilé pour [Unicode](unicode.md) simplement à l’aide d’une directive de préprocesseur pour définir « Unicode » avant les instructions **\# include** pour les fichiers d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="52dea-104">If you use generic data types in your code, it can be compiled for [Unicode](unicode.md) simply by using a preprocessor directive to define "UNICODE" before the **\#include** statements for the header files.</span></span> <span data-ttu-id="52dea-105">Pour compiler le code pour les [pages de codes Windows (ANSI)](code-pages.md), omettez la définition « Unicode ».</span><span class="sxs-lookup"><span data-stu-id="52dea-105">To compile the code for [Windows (ANSI) code pages](code-pages.md), omit the "UNICODE" definition.</span></span> <span data-ttu-id="52dea-106">Les nouvelles applications Windows doivent utiliser Unicode pour éviter les incohérences de pages de codes variées et simplifier la localisation.</span><span class="sxs-lookup"><span data-stu-id="52dea-106">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and simplify localization.</span></span>

<span data-ttu-id="52dea-107">Pour créer du code source qui peut être compilé pour utiliser des chaînes et des caractères Unicode ou pour utiliser des caractères et des chaînes à partir de pages de codes Windows :</span><span class="sxs-lookup"><span data-stu-id="52dea-107">To create source code that can be compiled either to use Unicode characters and strings or to use characters and strings from Windows code pages:</span></span>

1.  <span data-ttu-id="52dea-108">Utilisez des types de données génériques, tels que TCHAR, LPTSTR et LPTCH, pour tous les types de caractères et de chaînes utilisés pour le texte.</span><span class="sxs-lookup"><span data-stu-id="52dea-108">Use generic data types, such as TCHAR, LPTSTR, and LPTCH, for all character and string types used for text.</span></span> <span data-ttu-id="52dea-109">Pour plus d’informations sur les types génériques, consultez [types de données Windows pour les chaînes](windows-data-types-for-strings.md).</span><span class="sxs-lookup"><span data-stu-id="52dea-109">For more about generic types, see [Windows Data Types for Strings](windows-data-types-for-strings.md).</span></span>
2.  <span data-ttu-id="52dea-110">Assurez-vous que les pointeurs vers des mémoires tampons de données non textuelles ou des tableaux d’octets binaires sont codés avec des types de données tels que LPBYTE ou LPWORD, au lieu du type LPTSTR ou LPTCH.</span><span class="sxs-lookup"><span data-stu-id="52dea-110">Be sure that pointers to non-text data buffers or binary byte arrays are coded with data types such as LPBYTE or LPWORD, instead of the LPTSTR or LPTCH type.</span></span>
3.  <span data-ttu-id="52dea-111">Déclarez les pointeurs de type indéterminé explicitement comme pointeurs void en utilisant LPVOID comme il convient.</span><span class="sxs-lookup"><span data-stu-id="52dea-111">Declare pointers of indeterminate type explicitly as void pointers by using LPVOID as appropriate.</span></span>
4.  <span data-ttu-id="52dea-112">Rendre le type arithmétique du pointeur indépendant.</span><span class="sxs-lookup"><span data-stu-id="52dea-112">Make pointer arithmetic type-independent.</span></span> <span data-ttu-id="52dea-113">L’utilisation d’unités de taille TCHAR génère des variables de 2 octets si UNICODE est défini et 1 octet si UNICODE n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="52dea-113">Using units of TCHAR size yields variables that are 2 bytes if UNICODE is defined, and 1 byte if UNICODE is not defined.</span></span> <span data-ttu-id="52dea-114">L’utilisation de l’arithmétique de pointeur retourne toujours le nombre d’éléments indiqués par le pointeur, que la taille des éléments soit de 1 ou 2 octets.</span><span class="sxs-lookup"><span data-stu-id="52dea-114">Using pointer arithmetic always returns the number of elements indicated by the pointer, whether the elements are 1 or 2 bytes in size.</span></span> <span data-ttu-id="52dea-115">L’expression suivante récupère toujours le nombre d’éléments, qu’UNICODE soit défini ou non.</span><span class="sxs-lookup"><span data-stu-id="52dea-115">The following expression always retrieves the number of elements, regardless of whether UNICODE is defined.</span></span>

    ```C++
    cCount = lpEnd - lpStart;
    ```

    

    <span data-ttu-id="52dea-116">L’expression suivante détermine le nombre d’octets utilisés.</span><span class="sxs-lookup"><span data-stu-id="52dea-116">The following expression determines the number of bytes used.</span></span>

    ```C++
    cByteCount = (lpEnd - lpStart) * sizeof(TCHAR);
    ```

    

    <span data-ttu-id="52dea-117">Il n’est pas nécessaire de modifier une instruction comme celle qui suit, car l’incrément du pointeur pointe vers l’élément de caractère suivant.</span><span class="sxs-lookup"><span data-stu-id="52dea-117">There is no need to change a statement like the following one, because the pointer increment points to the next character element.</span></span>

    ```C++
    chNext = *++lpText;
    ```

    

5.  <span data-ttu-id="52dea-118">Remplacez les chaînes littérales et les constantes de caractère de manifeste par des macros.</span><span class="sxs-lookup"><span data-stu-id="52dea-118">Replace literal strings and manifest character constants with macros.</span></span> <span data-ttu-id="52dea-119">Modifiez les expressions comme suit.</span><span class="sxs-lookup"><span data-stu-id="52dea-119">Change expressions like the following one.</span></span>

    ```C++
    while(*lpFileName++ != '\\')
    {
        // ...
    }
    ```

    

    <span data-ttu-id="52dea-120">Utilisez la macro [**Text**](/windows/desktop/api/Winnt/nf-winnt-text) comme suit dans cette expression.</span><span class="sxs-lookup"><span data-stu-id="52dea-120">Use the [**TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) macro as follows in this expression.</span></span>

    ```C++
    while(*lpFileName++ != TEXT('\\'))
    {
        // ...
    }
    ```

    

    <span data-ttu-id="52dea-121">La macro [**Text**](/windows/desktop/api/Winnt/nf-winnt-text) fait en sorte que les chaînes soient évaluées en tant que L "String" lorsque Unicode est défini, et en tant que "String" dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="52dea-121">The [**TEXT**](/windows/desktop/api/Winnt/nf-winnt-text) macro causes strings to be evaluated as L"string" when UNICODE is defined, and as "string" otherwise.</span></span> <span data-ttu-id="52dea-122">Pour faciliter la gestion, déplacez des chaînes littérales dans des ressources, en particulier si elles contiennent des caractères en dehors de la plage ASCII (0x00 à 0x7F) ou sont exposées au niveau de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="52dea-122">For easier management, move literal strings into resources, especially if they contain characters outside the ASCII range (0x00 through 0x7F) or are exposed at the user interface.</span></span> <span data-ttu-id="52dea-123">Pour prendre en charge la localisation de votre application dans différentes langues nationales, il est très important que toutes les chaînes d’interface utilisateur se trouvent dans des ressources localisables.</span><span class="sxs-lookup"><span data-stu-id="52dea-123">To support localization of your application for different national languages, it is very important for all user interface strings to be in localizable resources.</span></span>

6.  <span data-ttu-id="52dea-124">Utilisez les versions génériques des fonctions Windows.</span><span class="sxs-lookup"><span data-stu-id="52dea-124">Use the generic versions of the Windows functions.</span></span> <span data-ttu-id="52dea-125">Pour plus d’informations, consultez [conventions pour les prototypes de fonction](conventions-for-function-prototypes.md).</span><span class="sxs-lookup"><span data-stu-id="52dea-125">For more information, see [Conventions for Function Prototypes](conventions-for-function-prototypes.md).</span></span>
7.  <span data-ttu-id="52dea-126">Utilisez les versions génériques des fonctions de chaîne de la bibliothèque C standard et n’oubliez pas de définir « Unicode », ainsi que \_ « Unicode », comme indiqué dans [fonctions C standard](standard-c-functions.md).</span><span class="sxs-lookup"><span data-stu-id="52dea-126">Use the generic versions of the standard C library string functions, and remember to define "\_UNICODE" as well as "UNICODE", as discussed in [Standard C Functions](standard-c-functions.md).</span></span>
8.  <span data-ttu-id="52dea-127">Si vous adaptez une application écrite à l’origine pour les pages de code Windows, n’oubliez pas de modifier le code qui s’appuie sur 255 comme la plus grande valeur d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="52dea-127">If you are adapting an application originally written for Windows code pages, remember to change any code that relies on 255 as the largest value for a character.</span></span>

<span data-ttu-id="52dea-128">Quand vous compilez le code que vous avez écrit comme indiqué ci-dessus, le compilateur peut créer des versions de page de codes Unicode et Windows de votre application à partir de la même source.</span><span class="sxs-lookup"><span data-stu-id="52dea-128">When you compile code that you have written as outlined above, the compiler can create both Unicode and Windows code page versions of your application from the same source.</span></span> <span data-ttu-id="52dea-129">Selon les définitions pour UNICODE, les fonctions génériques sont résolues pour produire les mêmes fichiers binaires que si vous avez écrit du code exclusivement pour Unicode ou exclusivement pour les pages de codes Windows.</span><span class="sxs-lookup"><span data-stu-id="52dea-129">Depending on the definitions for UNICODE, the generic functions are resolved to produce the same binary files as if you wrote code exclusively for Unicode or exclusively for Windows code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52dea-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="52dea-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52dea-131">Utilisation d’Unicode et de jeux de caractères</span><span class="sxs-lookup"><span data-stu-id="52dea-131">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 



