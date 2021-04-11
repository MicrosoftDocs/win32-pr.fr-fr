---
description: Les fonctions qui n’ont pas été implémentées avec une version Unicode ont généralement été remplacées par des fonctions plus puissantes ou étendues qui prennent en charge Unicode.
ms.assetid: 9e02c8fe-4fed-4b77-9b09-35850350859a
title: Utilisation de fonctions qui n’ont pas d’équivalents Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0850eea442b98c81918c7c6733da65f730936be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210940"
---
# <a name="using-functions-that-have-no-unicode-equivalents"></a><span data-ttu-id="83ffc-103">Utilisation de fonctions qui n’ont pas d’équivalents Unicode</span><span class="sxs-lookup"><span data-stu-id="83ffc-103">Using Functions That Have No Unicode Equivalents</span></span>

<span data-ttu-id="83ffc-104">Les fonctions qui n’ont pas été implémentées avec une version [Unicode](unicode.md) ont généralement été remplacées par des fonctions plus puissantes ou étendues qui prennent en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="83ffc-104">Functions that have not been implemented with a [Unicode](unicode.md) version have typically been replaced by more powerful or extended functions that do support Unicode.</span></span> <span data-ttu-id="83ffc-105">Par exemple, si vous portez du code qui appelle la fonction [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) , votre application peut prendre en charge Unicode à l’aide de la fonction [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) à la place.</span><span class="sxs-lookup"><span data-stu-id="83ffc-105">For example, if you are porting code that calls the [**OpenFile**](/windows/win32/api/winbase/nf-winbase-openfile) function, your application can support Unicode by using the [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) function instead.</span></span>

<span data-ttu-id="83ffc-106">Si une fonction n’a pas d’équivalent Unicode, l’application peut mapper des caractères vers et depuis des jeux de caractères 8 bits avant et après l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="83ffc-106">If a function has no Unicode equivalent, the application can map characters to and from 8-bit character sets before and after the function call.</span></span> <span data-ttu-id="83ffc-107">Par exemple, les fonctions de mise en forme des nombres **atoi** et **ITOA** utilisent uniquement les chiffres de 0 à 9.</span><span class="sxs-lookup"><span data-stu-id="83ffc-107">For example, the number-formatting functions **atoi** and **itoa** use only the digits 0 through 9.</span></span> <span data-ttu-id="83ffc-108">Normalement, le mappage Unicode sur des caractères 8 bits entraîne une perte de données, mais cela peut être évité en rendant le type de code indépendant et en rendant les expressions conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="83ffc-108">Normally, mapping Unicode to 8-bit characters causes loss of data, but this can be avoided by making the code type-independent and making the expressions conditional.</span></span> <span data-ttu-id="83ffc-109">Les instructions de l’exemple suivant, écrites pour les caractères de 8 bits, sont dépendantes du type et doivent être modifiées pour prendre en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="83ffc-109">The statements in the following example, written for 8-bit characters, are type-dependent and should be changed to support Unicode.</span></span>


```C++
char str[4] = "137";

int num = atoi(str);
```



<span data-ttu-id="83ffc-110">Ces instructions peuvent être réécrites comme suit pour les rendre indépendantes du type.</span><span class="sxs-lookup"><span data-stu-id="83ffc-110">These statements can be rewritten as follows to make them type-independent.</span></span>


```C++
TCHAR tstr[4] = TEXT("137");

#ifdef UNICODE
size_t cCharsConverted;
CHAR strTmp[SIZE]; // SIZE equals (2*(sizeof(tstr)+1)). This ensures enough
                   // room for the multibyte characters if they are two 
                   // bytes long and a terminating null character. See Security 
                   // Alert below. 

wcstombs_s(&cCharsConverted, strTmp, sizeof(strTmp), (const wchar_t *)tstr, sizeof(strTmp));
num = atoi(strTmp);

#else

int num = atoi(tstr);

#endif 
```



<span data-ttu-id="83ffc-111">Dans cet exemple, la fonction de bibliothèque C standard **wcstombs** traduit Unicode en ASCII.</span><span class="sxs-lookup"><span data-stu-id="83ffc-111">In this example, the standard C library function **wcstombs** translates Unicode to ASCII.</span></span> <span data-ttu-id="83ffc-112">L’exemple repose sur le fait que les chiffres de 0 à 9 peuvent toujours être convertis du format Unicode au format ASCII, même si une partie du texte environnant ne l’est pas.</span><span class="sxs-lookup"><span data-stu-id="83ffc-112">The example relies on the fact that the digits 0 through 9 can always be translated from Unicode to ASCII, even if some of the surrounding text cannot.</span></span> <span data-ttu-id="83ffc-113">La fonction **atoi** s’arrête à n’importe quel caractère qui n’est pas un chiffre.</span><span class="sxs-lookup"><span data-stu-id="83ffc-113">The **atoi** function stops at any character that is not a digit.</span></span>

<span data-ttu-id="83ffc-114">Votre application peut utiliser la fonction [**LCMAPSTRING**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) NLS (National Language Support) pour traiter le texte qui comprend les [chiffres natifs](digit-shapes.md) fournis pour certains scripts Unicode.</span><span class="sxs-lookup"><span data-stu-id="83ffc-114">Your application can use the National Language Support (NLS) [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) function to process text that includes the [native digits](digit-shapes.md) provided for some of the scripts in Unicode.</span></span>

> [!Caution]  
> <span data-ttu-id="83ffc-115">L’utilisation incorrecte de la fonction **wcstombs** peut compromettre la sécurité de votre application.</span><span class="sxs-lookup"><span data-stu-id="83ffc-115">Using the **wcstombs** function incorrectly can compromise the security of your application.</span></span> <span data-ttu-id="83ffc-116">Assurez-vous que la mémoire tampon d’application pour la chaîne de caractères de 8 bits est d’au moins la taille 2 \* (*\_ longueur de caractère* + 1), où la *\_ longueur de caractère* représente la longueur de la chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="83ffc-116">Make sure that the application buffer for the string of 8-bit characters is at least of size 2\*(*char\_length* +1), where *char\_length* represents the length of the Unicode string.</span></span> <span data-ttu-id="83ffc-117">Cette restriction est effectuée car, avec des [jeux de caractères codés sur deux octets](double-byte-character-sets.md) (DBCS), chaque caractère Unicode peut être mappé à deux caractères 8 bits consécutifs.</span><span class="sxs-lookup"><span data-stu-id="83ffc-117">This restriction is made because, with [double-byte character sets](double-byte-character-sets.md) (DBCSs), each Unicode character can be mapped to two consecutive 8-bit characters.</span></span> <span data-ttu-id="83ffc-118">Si la mémoire tampon ne contient pas la chaîne entière, la chaîne de résultat ne se termine pas par un caractère null, ce qui pose un risque de sécurité.</span><span class="sxs-lookup"><span data-stu-id="83ffc-118">If the buffer does not hold the entire string, the result string is not null-terminated, posing a security risk.</span></span> <span data-ttu-id="83ffc-119">Pour plus d’informations sur la sécurité des applications, consultez Considérations sur la [sécurité : fonctionnalités internationales](security-considerations--international-features.md).</span><span class="sxs-lookup"><span data-stu-id="83ffc-119">For more information about application security, see [Security Considerations: International Features](security-considerations--international-features.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="83ffc-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="83ffc-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83ffc-121">Utilisation d’Unicode et de jeux de caractères</span><span class="sxs-lookup"><span data-stu-id="83ffc-121">Using Unicode and Character Sets</span></span>](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
