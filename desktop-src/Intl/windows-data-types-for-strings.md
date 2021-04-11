---
description: La plupart des opérations de chaîne peuvent utiliser la même logique pour Unicode et pour les pages de code Windows.
ms.assetid: 5364ec09-68e1-444c-9493-ca9426ac9c34
title: Types de données Windows pour les chaînes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e24be1024736ce324e040e58f6ac45636a11d4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042854"
---
# <a name="windows-data-types-for-strings"></a><span data-ttu-id="d5d68-103">Types de données Windows pour les chaînes</span><span class="sxs-lookup"><span data-stu-id="d5d68-103">Windows Data Types for Strings</span></span>

<span data-ttu-id="d5d68-104">La plupart des opérations de chaîne peuvent utiliser la même logique pour [Unicode](unicode.md) et pour les [pages de code Windows](code-pages.md).</span><span class="sxs-lookup"><span data-stu-id="d5d68-104">Most string operations can use the same logic for [Unicode](unicode.md) and for [Windows code pages](code-pages.md).</span></span> <span data-ttu-id="d5d68-105">La seule différence est que l’unité de base de l’opération est un caractère 16 bits (également appelé caractère élargi) pour Unicode et un caractère 8 bits pour les pages de codes Windows.</span><span class="sxs-lookup"><span data-stu-id="d5d68-105">The only difference is that the basic unit of operation is a 16-bit character (also known as a wide character) for Unicode and an 8-bit character for Windows code pages.</span></span> <span data-ttu-id="d5d68-106">Les fichiers d’en-tête Windows fournissent plusieurs définitions de type qui facilitent la création de sources pouvant être compilées pour Unicode ou pour les pages de codes Windows.</span><span class="sxs-lookup"><span data-stu-id="d5d68-106">The Windows header files provide several type definitions that make it easy to create sources that can be compiled for Unicode or for Windows code pages.</span></span>

<span data-ttu-id="d5d68-107">Windows prend en charge trois ensembles de types de données caractère et chaîne : un ensemble de définitions de types génériques qui peuvent être compilés pour les pages de codes Unicode ou Windows, et deux ensembles de définitions de types spécifiques.</span><span class="sxs-lookup"><span data-stu-id="d5d68-107">Windows supports three sets of character and string data types: a set of generic type definitions that can compile for either Unicode or Windows code pages, and two sets of specific type definitions.</span></span> <span data-ttu-id="d5d68-108">Un ensemble de définitions de types spécifiques est destiné à être utilisé avec Unicode, tandis que l’autre est destiné à être utilisé avec les pages de codes Windows.</span><span class="sxs-lookup"><span data-stu-id="d5d68-108">One set of specific type definitions is for use with Unicode, and the other is for use with Windows code pages.</span></span>

<span data-ttu-id="d5d68-109">Une application utilisant des types de données génériques peut être compilée pour Unicode simplement en définissant « UNICODE » avant les instructions **\# include** pour les fichiers d’en-tête, ou pendant la compilation.</span><span class="sxs-lookup"><span data-stu-id="d5d68-109">An application using generic data types can be compiled for Unicode simply by defining "UNICODE" before the **\#include** statements for the header files, or during compilation.</span></span> <span data-ttu-id="d5d68-110">Les nouvelles applications Windows doivent utiliser Unicode pour éviter les incohérences de pages de codes variées et simplifier la localisation.</span><span class="sxs-lookup"><span data-stu-id="d5d68-110">New Windows applications should use Unicode to avoid the inconsistencies of varied code pages and to simplify localization.</span></span> <span data-ttu-id="d5d68-111">Elles doivent être écrites avec des types de données génériques et doivent définir « UNICODE » afin de compiler ces types en types Unicode.</span><span class="sxs-lookup"><span data-stu-id="d5d68-111">They should be written with generic data types, and should define "UNICODE" in order to compile these types into Unicode types.</span></span> <span data-ttu-id="d5d68-112">Dans les rares emplacements où une application doit fonctionner avec des données de type caractère 8 bits, elle peut utiliser les types pour les pages de codes Windows de façon explicite.</span><span class="sxs-lookup"><span data-stu-id="d5d68-112">In the few places where an application must work with 8-bit character data, it can make explicit use of the types for Windows code pages.</span></span>

<span data-ttu-id="d5d68-113">La possibilité de compiler les types génériques en types pour les pages de codes Windows existe principalement pour prendre en charge les applications héritées.</span><span class="sxs-lookup"><span data-stu-id="d5d68-113">The ability to compile the generic types into types for Windows code pages exists mainly to support legacy applications.</span></span> <span data-ttu-id="d5d68-114">Pour compiler des pages de codes Windows, l’application omet simplement la définition UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d5d68-114">To compile for Windows code pages, the application just omits the UNICODE definition.</span></span>

<span data-ttu-id="d5d68-115">L’exemple suivant illustre la méthode utilisée dans les fichiers d’en-tête Windows pour définir les trois jeux de types de données.</span><span class="sxs-lookup"><span data-stu-id="d5d68-115">The following example shows the method used in the Windows header files to define the three sets of data types.</span></span> <span data-ttu-id="d5d68-116">Pour l’implémentation, consultez le fichier d’en-tête Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="d5d68-116">For the implementation, see the Winnt.h header file.</span></span>


```C++
// Generic types

#ifdef UNICODE
    typedef wchar_t TCHAR;
#else
    typedef unsigned char TCHAR;
#endif

typedef TCHAR *LPTSTR, *LPTCH;

// 8-bit character specific

typedef unsigned char CHAR;
typedef CHAR *LPSTR, *LPCH;

// Unicode specific (wide characters)

typedef unsigned wchar_t WCHAR;
typedef WCHAR *LPWSTR, *LPWCH;
```



<span data-ttu-id="d5d68-117">La lettre « T » dans une définition de type, par exemple TCHAR ou LPTSTR, désigne un type générique qui peut être compilé pour les pages de codes Windows ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="d5d68-117">The letter "T" in a type definition, for example, TCHAR or LPTSTR, designates a generic type that can be compiled for either Windows code pages or Unicode.</span></span> <span data-ttu-id="d5d68-118">La lettre « W » dans une définition de type, par exemple WCHAR ou LPWSTR, désigne un type Unicode.</span><span class="sxs-lookup"><span data-stu-id="d5d68-118">The letter "W" in a type definition, for example, WCHAR or LPWSTR, designates a Unicode type.</span></span> <span data-ttu-id="d5d68-119">Étant donné que les pages de codes Windows sont de l’ancien formulaire, elles ont des définitions de type simples, telles que CHAR et LPSTR.</span><span class="sxs-lookup"><span data-stu-id="d5d68-119">Because Windows code pages are of the older form, they have simple type definitions, such as CHAR and LPSTR.</span></span> <span data-ttu-id="d5d68-120">Pour obtenir une description complète des types de données dans Windows, consultez [types de données Windows](../winprog/windows-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="d5d68-120">For a complete description of data types in Windows, see [Windows Data Types](../winprog/windows-data-types.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5d68-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5d68-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5d68-122">Unicode dans l'API Windows</span><span class="sxs-lookup"><span data-stu-id="d5d68-122">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
