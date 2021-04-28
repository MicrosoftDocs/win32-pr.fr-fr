---
title: Utilisation des chaînes
description: Utilisation des chaînes
ms.assetid: 876ff8bb-67c3-4dcc-aa94-7fbd915c67dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4661c6b07a267d90e0fca05d04354c018be04527
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110967"
---
# <a name="working-with-strings"></a><span data-ttu-id="78d9f-103">Utilisation des chaînes</span><span class="sxs-lookup"><span data-stu-id="78d9f-103">Working with Strings</span></span>

<span data-ttu-id="78d9f-104">Windows prend en charge en mode natif les chaînes Unicode pour les éléments d’interface utilisateur, les noms de fichiers, etc.</span><span class="sxs-lookup"><span data-stu-id="78d9f-104">Windows natively supports Unicode strings for UI elements, file names, and so forth.</span></span> <span data-ttu-id="78d9f-105">Unicode est l’encodage de caractères par défaut, car il prend en charge tous les jeux de caractères et toutes les langues.</span><span class="sxs-lookup"><span data-stu-id="78d9f-105">Unicode is the preferred character encoding, because it supports all character sets and languages.</span></span> <span data-ttu-id="78d9f-106">Windows représente des caractères Unicode à l’aide de l’encodage UTF-16, dans lequel chaque caractère est encodé sous la forme d’une valeur de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="78d9f-106">Windows represents Unicode characters using UTF-16 encoding, in which each character is encoded as a 16-bit value.</span></span> <span data-ttu-id="78d9f-107">Les caractères UTF-16 sont appelés caractères *larges* , afin de les distinguer des caractères ANSI 8 bits.</span><span class="sxs-lookup"><span data-stu-id="78d9f-107">UTF-16 characters are called *wide* characters, to distinguish them from 8-bit ANSI characters.</span></span> <span data-ttu-id="78d9f-108">Le compilateur Visual C++ prend en charge le type de données intégré **WCHAR \_ t** pour les caractères larges.</span><span class="sxs-lookup"><span data-stu-id="78d9f-108">The Visual C++ compiler supports the built-in data type **wchar\_t** for wide characters.</span></span> <span data-ttu-id="78d9f-109">Le fichier d’en-tête Winnt. h définit également le **typedef** suivant.</span><span class="sxs-lookup"><span data-stu-id="78d9f-109">The header file WinNT.h also defines the following **typedef**.</span></span>


```C++
typedef wchar_t WCHAR;
```



<span data-ttu-id="78d9f-110">Vous verrez les deux versions dans l’exemple de code MSDN.</span><span class="sxs-lookup"><span data-stu-id="78d9f-110">You will see both versions in MSDN example code.</span></span> <span data-ttu-id="78d9f-111">Pour déclarer un littéral à caractères larges ou un littéral de chaîne à caractères larges, placez **L** avant le littéral.</span><span class="sxs-lookup"><span data-stu-id="78d9f-111">To declare a wide-character literal or a wide-character string literal, put **L** before the literal.</span></span>


```C++
wchar_t a = L'a';
wchar_t *str = L"hello";
```



<span data-ttu-id="78d9f-112">Voici d’autres typedefs liés à la chaîne qui s’affichent :</span><span class="sxs-lookup"><span data-stu-id="78d9f-112">Here are some other string-related typedefs that you will see:</span></span>



| <span data-ttu-id="78d9f-113">Typedef</span><span class="sxs-lookup"><span data-stu-id="78d9f-113">Typedef</span></span>                   | <span data-ttu-id="78d9f-114">Définition</span><span class="sxs-lookup"><span data-stu-id="78d9f-114">Definition</span></span>       |
|---------------------------|------------------|
| <span data-ttu-id="78d9f-115">**CHAR**</span><span class="sxs-lookup"><span data-stu-id="78d9f-115">**CHAR**</span></span>                  | `char`           |
| <span data-ttu-id="78d9f-116">**PSTR** ou **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="78d9f-116">**PSTR** or **LPSTR**</span></span>     | `char*`          |
| <span data-ttu-id="78d9f-117">**PCSTR** ou **LPCSTR**</span><span class="sxs-lookup"><span data-stu-id="78d9f-117">**PCSTR** or **LPCSTR**</span></span>   | `const char*`    |
| <span data-ttu-id="78d9f-118">**PWSTR** ou **LPWStr**</span><span class="sxs-lookup"><span data-stu-id="78d9f-118">**PWSTR** or **LPWSTR**</span></span>   | `wchar_t*`       |
| <span data-ttu-id="78d9f-119">**PCWSTR** ou **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="78d9f-119">**PCWSTR** or **LPCWSTR**</span></span> | `const wchar_t*` |



 

## <a name="unicode-and-ansi-functions"></a><span data-ttu-id="78d9f-120">Fonctions Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="78d9f-120">Unicode and ANSI Functions</span></span>

<span data-ttu-id="78d9f-121">Lorsque Microsoft a introduit la prise en charge d’Unicode pour Windows, il a facilité la transition en fournissant deux jeux d’API parallèles, l’un pour les chaînes ANSI et l’autre pour les chaînes Unicode.</span><span class="sxs-lookup"><span data-stu-id="78d9f-121">When Microsoft introduced Unicode support to Windows, it eased the transition by providing two parallel sets of APIs, one for ANSI strings and the other for Unicode strings.</span></span> <span data-ttu-id="78d9f-122">Par exemple, il existe deux fonctions pour définir le texte de la barre de titre d’une fenêtre :</span><span class="sxs-lookup"><span data-stu-id="78d9f-122">For example, there are two functions to set the text of a window's title bar:</span></span>

-   <span data-ttu-id="78d9f-123">**SetWindowTextA** prend une chaîne ANSI.</span><span class="sxs-lookup"><span data-stu-id="78d9f-123">**SetWindowTextA** takes an ANSI string.</span></span>
-   <span data-ttu-id="78d9f-124">**SetWindowTextW** prend une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="78d9f-124">**SetWindowTextW** takes a Unicode string.</span></span>

<span data-ttu-id="78d9f-125">En interne, la version ANSI convertit la chaîne en Unicode.</span><span class="sxs-lookup"><span data-stu-id="78d9f-125">Internally, the ANSI version translates the string to Unicode.</span></span> <span data-ttu-id="78d9f-126">Les en-têtes Windows définissent également une macro qui correspond à la version Unicode lorsque le symbole de préprocesseur `UNICODE` est défini ou la version ANSI dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="78d9f-126">The Windows headers also define a macro that resolves to the Unicode version when the preprocessor symbol `UNICODE` is defined or the ANSI version otherwise.</span></span>


```C++
#ifdef UNICODE
#define SetWindowText  SetWindowTextW
#else
#define SetWindowText  SetWindowTextA
#endif 
```



<span data-ttu-id="78d9f-127">Dans MSDN, la fonction est documentée sous le nom [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), bien que c’est vraiment le nom de la macro, et non le nom réel de la fonction.</span><span class="sxs-lookup"><span data-stu-id="78d9f-127">In MSDN, the function is documented under the name [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta), even though that is really the macro name, not the actual function name.</span></span>

<span data-ttu-id="78d9f-128">Les nouvelles applications doivent toujours appeler les versions Unicode.</span><span class="sxs-lookup"><span data-stu-id="78d9f-128">New applications should always call the Unicode versions.</span></span> <span data-ttu-id="78d9f-129">De nombreux langages mondiaux requièrent Unicode.</span><span class="sxs-lookup"><span data-stu-id="78d9f-129">Many world languages require Unicode.</span></span> <span data-ttu-id="78d9f-130">Si vous utilisez des chaînes ANSI, il est impossible de localiser votre application.</span><span class="sxs-lookup"><span data-stu-id="78d9f-130">If you use ANSI strings, it will be impossible to localize your application.</span></span> <span data-ttu-id="78d9f-131">Les versions ANSI sont également moins efficaces, car le système d’exploitation doit convertir les chaînes ANSI au format Unicode au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="78d9f-131">The ANSI versions are also less efficient, because the operating system must convert the ANSI strings to Unicode at run time.</span></span> <span data-ttu-id="78d9f-132">Selon votre préférence, vous pouvez appeler les fonctions Unicode explicitement, telles que **SetWindowTextW**, ou utiliser les macros.</span><span class="sxs-lookup"><span data-stu-id="78d9f-132">Depending on your preference, you can call the Unicode functions explicitly, such as **SetWindowTextW**, or use the macros.</span></span> <span data-ttu-id="78d9f-133">L’exemple de code sur MSDN appelle généralement les macros, mais les deux formes sont équivalentes exactement.</span><span class="sxs-lookup"><span data-stu-id="78d9f-133">The example code on MSDN typically calls the macros, but the two forms are exactly equivalent.</span></span> <span data-ttu-id="78d9f-134">La plupart des API plus récentes dans Windows ont simplement une version Unicode, sans version ANSI correspondante.</span><span class="sxs-lookup"><span data-stu-id="78d9f-134">Most newer APIs in Windows have just a Unicode version, with no corresponding ANSI version.</span></span>

## <a name="tchars"></a><span data-ttu-id="78d9f-135">TCHARs</span><span class="sxs-lookup"><span data-stu-id="78d9f-135">TCHARs</span></span>

<span data-ttu-id="78d9f-136">De retour lorsque les applications devaient prendre en charge à la fois Windows NT et Windows 95, Windows 98 et Windows Me, il était utile de compiler le même code pour les chaînes ANSI ou Unicode, en fonction de la plateforme cible.</span><span class="sxs-lookup"><span data-stu-id="78d9f-136">Back when applications needed to support both Windows NT as well as Windows 95, Windows 98, and Windows Me, it was useful to compile the same code for either ANSI or Unicode strings, depending on the target platform.</span></span> <span data-ttu-id="78d9f-137">À cette fin, le SDK Windows fournit des macros qui mappent les chaînes au format Unicode ou ANSI, en fonction de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="78d9f-137">To this end, the Windows SDK provides macros that map strings to Unicode or ANSI, depending on the platform.</span></span>



| <span data-ttu-id="78d9f-138">Macro</span><span class="sxs-lookup"><span data-stu-id="78d9f-138">Macro</span></span>     | <span data-ttu-id="78d9f-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="78d9f-139">Unicode</span></span>   | <span data-ttu-id="78d9f-140">ANSI</span><span class="sxs-lookup"><span data-stu-id="78d9f-140">ANSI</span></span>   |
|-----------|-----------|--------|
| <span data-ttu-id="78d9f-141">TCHAR</span><span class="sxs-lookup"><span data-stu-id="78d9f-141">TCHAR</span></span>     | `wchar_t` | `char` |
| <span data-ttu-id="78d9f-142">TEXTE ("x")</span><span class="sxs-lookup"><span data-stu-id="78d9f-142">TEXT("x")</span></span> | `L"x"`    | `"x"`  |



 

<span data-ttu-id="78d9f-143">Par exemple, le code suivant :</span><span class="sxs-lookup"><span data-stu-id="78d9f-143">For example, the following code:</span></span>


```C++
SetWindowText(TEXT("My Application"));
```



<span data-ttu-id="78d9f-144">correspond à l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="78d9f-144">resolves to one of the following:</span></span>


```C++
SetWindowTextW(L"My Application"); // Unicode function with wide-character string.

SetWindowTextA("My Application");  // ANSI function.
```



<span data-ttu-id="78d9f-145">Les macros **Text** et **TCHAR** sont moins utiles aujourd’hui, car toutes les applications doivent utiliser Unicode.</span><span class="sxs-lookup"><span data-stu-id="78d9f-145">The **TEXT** and **TCHAR** macros are less useful today, because all applications should use Unicode.</span></span> <span data-ttu-id="78d9f-146">Toutefois, vous pouvez les voir dans du code plus ancien et dans certains exemples de code MSDN.</span><span class="sxs-lookup"><span data-stu-id="78d9f-146">However, you might see them in older code and in some of the MSDN code examples.</span></span>

<span data-ttu-id="78d9f-147">Les en-têtes des bibliothèques Runtime C de Microsoft définissent un ensemble de macros similaire.</span><span class="sxs-lookup"><span data-stu-id="78d9f-147">The headers for the Microsoft C run-time libraries define a similar set of macros.</span></span> <span data-ttu-id="78d9f-148">Par exemple, **\_ tcslen** se résout en **strlen** si `_UNICODE` n’est pas défini ; dans le cas contraire, il est résolu en **wcslen**, qui est la version à caractères larges de **strlen**.</span><span class="sxs-lookup"><span data-stu-id="78d9f-148">For example, **\_tcslen** resolves to **strlen** if `_UNICODE` is undefined; otherwise it resolves to **wcslen**, which is the wide-character version of **strlen**.</span></span>


```C++
#ifdef _UNICODE
#define _tcslen     wcslen
#else
#define _tcslen     strlen
#endif 
```



<span data-ttu-id="78d9f-149">ATTENTION : certains en-têtes utilisent le symbole de préprocesseur `UNICODE` , d’autres utilisent `_UNICODE` un préfixe de trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="78d9f-149">Be careful: Some headers use the preprocessor symbol `UNICODE`, others use `_UNICODE` with an underscore prefix.</span></span> <span data-ttu-id="78d9f-150">Définissez toujours les deux symboles.</span><span class="sxs-lookup"><span data-stu-id="78d9f-150">Always define both symbols.</span></span> <span data-ttu-id="78d9f-151">Visual C++ les définit toutes les deux par défaut lorsque vous créez un projet.</span><span class="sxs-lookup"><span data-stu-id="78d9f-151">Visual C++ sets them both by default when you create a new project.</span></span>

## <a name="next"></a><span data-ttu-id="78d9f-152">Suivant</span><span class="sxs-lookup"><span data-stu-id="78d9f-152">Next</span></span>

[<span data-ttu-id="78d9f-153">Qu’est-ce qu’une fenêtre ?</span><span class="sxs-lookup"><span data-stu-id="78d9f-153">What Is a Window?</span></span>](what-is-a-window-.md)

 

 
