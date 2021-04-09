---
description: Le SDK Windows fournit des prototypes de fonction dans des versions génériques, de page de codes Windows et Unicode.
ms.assetid: 601d24b0-11bb-48fa-a257-207c3acee226
title: Conventions pour les prototypes de fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951860f72870dcbbcb88572f379e39dc843ecb11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865505"
---
# <a name="conventions-for-function-prototypes"></a><span data-ttu-id="eaac6-103">Conventions pour les prototypes de fonctions</span><span class="sxs-lookup"><span data-stu-id="eaac6-103">Conventions for Function Prototypes</span></span>

<span data-ttu-id="eaac6-104">Le SDK Windows fournit des prototypes de fonction dans des versions génériques, de [page de codes Windows](code-pages.md)et [Unicode](unicode.md) .</span><span class="sxs-lookup"><span data-stu-id="eaac6-104">The Windows SDK provides function prototypes in generic, [Windows code page](code-pages.md), and [Unicode](unicode.md) versions.</span></span> <span data-ttu-id="eaac6-105">Les prototypes peuvent être compilés pour produire des prototypes de page de code Windows ou des prototypes Unicode.</span><span class="sxs-lookup"><span data-stu-id="eaac6-105">The prototypes can be compiled to produce either Windows code page prototypes or Unicode prototypes.</span></span> <span data-ttu-id="eaac6-106">Les trois prototypes sont présentés dans cette rubrique et sont illustrés par des exemples de code pour la fonction [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="eaac6-106">All three prototypes are discussed in this topic and are illustrated by code samples for the [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta) function.</span></span>

<span data-ttu-id="eaac6-107">Voici un exemple de prototype générique.</span><span class="sxs-lookup"><span data-stu-id="eaac6-107">The following is an example of a generic prototype.</span></span>


```C++
BOOL SetWindowText(
  HWND hwnd,
  LPCTSTR lpText
);
```



<span data-ttu-id="eaac6-108">Le fichier d'en-tête fournit le nom de la fonction générique implémentée comme macro.</span><span class="sxs-lookup"><span data-stu-id="eaac6-108">The header file provides the generic function name implemented as a macro.</span></span>


```C++
#ifdef UNICODE
#define SetWindowText SetWindowTextW
#else
#define SetWindowText SetWindowTextA
#endif // !UNICODE
```



<span data-ttu-id="eaac6-109">Le préprocesseur développe la macro dans la page de codes Windows ou le nom de la fonction Unicode.</span><span class="sxs-lookup"><span data-stu-id="eaac6-109">The preprocessor expands the macro into either the Windows code page or Unicode function name.</span></span> <span data-ttu-id="eaac6-110">La lettre « A » (ANSI) ou « W » (Unicode) est ajoutée à la fin du nom de fonction générique, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="eaac6-110">The letter "A" (ANSI) or "W" (Unicode) is added at the end of the generic function name, as appropriate.</span></span> <span data-ttu-id="eaac6-111">Le fichier d’en-tête fournit ensuite deux prototypes spécifiques, l’un pour les pages de codes Windows et l’autre pour Unicode, comme indiqué dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="eaac6-111">The header file then provides two specific prototypes, one for Windows code pages and one for Unicode, as shown in the following examples.</span></span>


```C++
BOOL SetWindowTextA(
  HWND hwnd,
  LPCSTR lpText
);
```




```C++
BOOL SetWindowTextW(
  HWND hwnd,
  LPCWSTR lpText
);
```



<span data-ttu-id="eaac6-112">Comme expliqué dans [types de données Windows pour les chaînes](windows-data-types-for-strings.md), le prototype de fonction générique utilise le type de données LPCTSTR pour le paramètre text.</span><span class="sxs-lookup"><span data-stu-id="eaac6-112">As explained in [Windows Data Types for Strings](windows-data-types-for-strings.md), the generic function prototype uses the data type LPCTSTR for the text parameter.</span></span> <span data-ttu-id="eaac6-113">Toutefois, le prototype de page de codes Windows utilise le type LPCSTR, et le prototype Unicode utilise LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="eaac6-113">However, the Windows code page prototype uses the type LPCSTR, and the Unicode prototype uses LPCWSTR.</span></span>

<span data-ttu-id="eaac6-114">Pour toutes les fonctions avec des arguments de texte, les applications doivent normalement utiliser les prototypes des fonctions génériques.</span><span class="sxs-lookup"><span data-stu-id="eaac6-114">For all functions with text arguments, applications should normally use the generic function prototypes.</span></span> <span data-ttu-id="eaac6-115">Si une application définit « UNICODE » avant les instructions **\# include** pour les fichiers d’en-tête ou pendant la compilation, les instructions sont compilées en fonctions Unicode.</span><span class="sxs-lookup"><span data-stu-id="eaac6-115">If an application defines "UNICODE" either before the **\#include** statements for the header files or during compilation, the statements will be compiled into Unicode functions.</span></span>

> [!Note]  
> <span data-ttu-id="eaac6-116">Les nouvelles applications Windows doivent utiliser Unicode pour éviter les incohérences de pages de codes variées et pour faciliter la localisation.</span><span class="sxs-lookup"><span data-stu-id="eaac6-116">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and for ease of localization.</span></span> <span data-ttu-id="eaac6-117">Elles doivent être écrites avec des fonctions génériques et doivent définir UNICODE pour compiler les fonctions en fonctions Unicode.</span><span class="sxs-lookup"><span data-stu-id="eaac6-117">They should be written with generic functions, and should define UNICODE to compile the functions into Unicode functions.</span></span> <span data-ttu-id="eaac6-118">Dans les rares emplacements où une application doit fonctionner avec des données de caractères 8 bits, elle peut utiliser de façon explicite les fonctions pour les pages de codes Windows.</span><span class="sxs-lookup"><span data-stu-id="eaac6-118">In the few places where an application must work with 8-bit character data, it can make explicit use of the functions for Windows code pages.</span></span>

 

<span data-ttu-id="eaac6-119">Votre application doit toujours utiliser un prototype de fonction générique avec la chaîne et les types de caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="eaac6-119">Your application should always use a generic function prototype with the generic string and character types.</span></span> <span data-ttu-id="eaac6-120">Tous les noms de fonctions qui se terminent par un « W » majuscule utilisent Unicode, c.-à-d. des paramètres à caractère large.</span><span class="sxs-lookup"><span data-stu-id="eaac6-120">All function names that end with an uppercase "W" take Unicode, that is, wide character, parameters.</span></span> <span data-ttu-id="eaac6-121">Certaines fonctions existent uniquement dans les versions Unicode et peuvent être utilisées uniquement avec les types de données appropriés.</span><span class="sxs-lookup"><span data-stu-id="eaac6-121">Some functions exist only in Unicode versions and can be used only with the appropriate data types.</span></span> <span data-ttu-id="eaac6-122">Par exemple, [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) et [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) ont uniquement des versions Unicode.</span><span class="sxs-lookup"><span data-stu-id="eaac6-122">For example, [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) and [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) have only Unicode versions.</span></span>

<span data-ttu-id="eaac6-123">La section relative à la configuration requise de la documentation de référence pour chaque fonction Unicode et de jeu de caractères fournit des informations sur les versions de fonction implémentées par les systèmes d’exploitation pris en charge.</span><span class="sxs-lookup"><span data-stu-id="eaac6-123">The Requirements section in the reference documentation for each Unicode and character set function provides information on the function versions implemented by supported operating systems.</span></span> <span data-ttu-id="eaac6-124">Si une ligne commençant par « Unicode » est incluse, la fonction a des versions de page de codes Unicode et Windows distinctes.</span><span class="sxs-lookup"><span data-stu-id="eaac6-124">If a line beginning with "Unicode" is included, the function has separate Unicode and Windows code page versions.</span></span>

> [!Note]  
> <span data-ttu-id="eaac6-125">Lorsqu’une fonction a un paramètre de longueur pour une chaîne de caractères, la longueur doit être documentée en tant que nombre de valeurs TCHAR dans la chaîne.</span><span class="sxs-lookup"><span data-stu-id="eaac6-125">When a function has a length parameter for a character string, the length should be documented as a count of TCHAR values in the string.</span></span> <span data-ttu-id="eaac6-126">Ce type de données fait référence aux octets des versions de page de codes Windows de la fonction ou des mots de 16 bits pour les versions Unicode.</span><span class="sxs-lookup"><span data-stu-id="eaac6-126">This data type refers to bytes for Windows code page versions of the function or 16-bit words for Unicode versions.</span></span> <span data-ttu-id="eaac6-127">Toutefois, les fonctions qui requièrent ou retournent des pointeurs vers des blocs de mémoire non typés, tels que la fonction [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) , prennent généralement une taille en octets, quel que soit le prototype utilisé.</span><span class="sxs-lookup"><span data-stu-id="eaac6-127">However, functions that require or return pointers to untyped memory blocks, such as the [**GlobalAlloc**](/windows/win32/api/winbase/nf-winbase-globalalloc) function, generally take a size in bytes, regardless of the prototype that is used.</span></span> <span data-ttu-id="eaac6-128">Si l’allocation de mémoire non typée est pour une chaîne, l’application doit multiplier le nombre de caractères par sizeof (TCHAR).</span><span class="sxs-lookup"><span data-stu-id="eaac6-128">If the allocation of untyped memory is for a string, the application must multiply the number of characters by sizeof(TCHAR).</span></span> <span data-ttu-id="eaac6-129">Pour plus d’informations, consultez [utilisation des types de données génériques](using-generic-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="eaac6-129">For additional information, see [Using Generic Data Types](using-generic-data-types.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="eaac6-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eaac6-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaac6-131">Unicode dans l'API Windows</span><span class="sxs-lookup"><span data-stu-id="eaac6-131">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
