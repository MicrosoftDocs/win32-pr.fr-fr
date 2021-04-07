---
title: Dictionnaire des noms d’affichage des jeux de propriétés
description: Un dictionnaire de noms d’affichage de propriété permet aux utilisateurs de jeux de propriétés d’attacher la signification aux propriétés, au-delà de celles fournies par l’indicateur de type.
ms.assetid: b6813a86-39d3-4754-86e4-51035a7c91d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd844b4d37d4f10434fc5b73f936b4b6565c1506
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729069"
---
# <a name="property-set-display-name-dictionary"></a><span data-ttu-id="f337b-103">Dictionnaire des noms d’affichage des jeux de propriétés</span><span class="sxs-lookup"><span data-stu-id="f337b-103">Property Set Display Name Dictionary</span></span>

<span data-ttu-id="f337b-104">Un dictionnaire de noms d’affichage de propriété permet aux utilisateurs de jeux de propriétés d’attacher la signification aux propriétés, au-delà de celles fournies par l’indicateur de type.</span><span class="sxs-lookup"><span data-stu-id="f337b-104">A dictionary of property display names enables property set users to attach meaning to properties - beyond those provided by the type indicator.</span></span>

## <a name="dictionary-structure"></a><span data-ttu-id="f337b-105">Structure du dictionnaire</span><span class="sxs-lookup"><span data-stu-id="f337b-105">Dictionary Structure</span></span>

<span data-ttu-id="f337b-106">Le dictionnaire contient un nombre d’entrées dans la liste, suivi d’une liste d’entrées de dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="f337b-106">The dictionary contains a count of entries in the list, followed by a list of dictionary entries.</span></span>

``` syntax
typedef struct tagDICTIONARY 
{ 
    DWORD  cEntries ;               // Count of entries in the list 
    ENTRY  rgEntry[ cEntries ] ;    // Property ID/String pair 
} DICTIONARY ;
```

## <a name="dictionary-entry-structure"></a><span data-ttu-id="f337b-107">Structure d’entrée de dictionnaire</span><span class="sxs-lookup"><span data-stu-id="f337b-107">Dictionary Entry Structure</span></span>

<span data-ttu-id="f337b-108">Chaque entrée de dictionnaire de la liste est une paire identificateur de propriété/chaîne.</span><span class="sxs-lookup"><span data-stu-id="f337b-108">Each dictionary entry in the list is a Property Identifier/String pair.</span></span> <span data-ttu-id="f337b-109">Voici une définition de Pseudo-structure pour une entrée de dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="f337b-109">The following is a pseudo-structure definition for a dictionary entry.</span></span> <span data-ttu-id="f337b-110">Il s’agit d’une Pseudo-structure, car la \[ \] taille du membre SZ est variable.</span><span class="sxs-lookup"><span data-stu-id="f337b-110">It's a pseudo-structure because the sz\[\] member is variable in size.</span></span>

``` syntax
typedef struct tagENTRY 
{ 
    DWORD  propid ;    // Property ID 
    DWORD  cch ;       // Count of characters in the string 
    char  sz[cch];     // Zero-terminated string 
} ENTRY ;
```

## <a name="sample-dictionary"></a><span data-ttu-id="f337b-111">Exemple de dictionnaire</span><span class="sxs-lookup"><span data-stu-id="f337b-111">Sample Dictionary</span></span>

<span data-ttu-id="f337b-112">L’exemple de transfert de données boursières suivant peut inclure un nom affichable « stock quote » pour l’ensemble du jeu et « Symbol ticker » pour le \_ symbole PID.</span><span class="sxs-lookup"><span data-stu-id="f337b-112">The following stock market data transfer example might include a displayable name "Stock Quote" for the entire set, and "Ticker Symbol" for PID\_SYMBOL.</span></span> <span data-ttu-id="f337b-113">Si un jeu de propriétés ne contenait qu’un symbole et le dictionnaire, la section Property Set aurait un flux d’octets qui ressemble à ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="f337b-113">If a property set contained just a symbol and the dictionary, the property set section would have a byte stream that looked like the following.</span></span>

``` syntax
Offset     Bytes 
; Start of section 
0000    5C 01 00 00    ; DWORD size of section 
0004    04 00 00 00    ; DWORD number of properties in section 
 
; Start of PropID/Offset pairs 
0008    01 00 00 00    ; DWORD Property ID (1 == code page) 
000C    28 00 00 00    ; DWORD offset to property ID 
0010    00 00 00 80    ; DWORD Property ID (0x80000000 == locale
                                                 ID) 
0014    30 00 00 00    ; DWORD offset to property ID 
0018    00 00 00 00    ; DWORD Property ID (0 == dictionary) 
001C    38 00 00 00    ; DWORD offset to property ID 
0020    07 00 00 00    ; DWORD Property ID (7 == PID_SYMBOL)
0024    5C 01 00 00    ; DWORD offset to property ID
 
; Start of Property 1 (code page)
0028    01 00 00 00    ; DWORD type indicator (VT_12)
002C    B0 04          ; USHORT codepage (0x04b0 == 1200 ==
                                                 unicode)
002E    00 00          ; Pad to 32-bit boundary
 
; Start of Property 0x80000000 (Local ID)
0030    13 00 00 00    ; DWORD type indicator (VT_U14)
0034    09 04 00 00    ; ULONG locale ID (0x0409 == American 
                                                 English)
 
; Start of Property 0 (the dictionary)
0038    08 00 00 00    ; DWORD number of entries in dictionary
                             (Note:  No type indicator)
003C    00 00 00 00    ; DWORD propid == 0 (the dictionary)
0040    0C 00 00 00    ; DWORD cch == wcslen(L"Stock Quote") +
                                                 sizeof(L'\0') == 12
0044    L"Stock Quote" ; wchar_t wsz(12)
005C    05 00 00 00    ; DWORD propid == 5 (PID_HIGH)
0060    0B 00 00 00    ; DWORD cch == wcslen(L"High Price") + 
                                                 sizeof(L'\0') == 11
0064    L"High Price\0"; wchar_t wsz(11)
007A    00 00          ; padding for 32-bit alignment (necessary
                             because the codepage is unicode)
007C    07 00 00 00    ; DWORD propid == 7 (PID_SYMBOL)
0080    0E 00 00 00    ; DWORD cch - wcslen(L"Ticker Symbol\0") 
                             == 14
0084    L"Ticker Symbol\0" ; wchar_t wsz(14)
 
    // The dictionary would continue, but may not contain entries 
    // for every possible property, and may contain entries for 
    // properties that are not present. Entries are not required  
    // to be in order.
```

<span data-ttu-id="f337b-114">Tenez compte des problèmes suivants concernant les dictionnaires de jeux de propriétés :</span><span class="sxs-lookup"><span data-stu-id="f337b-114">Be aware of the following issues regarding property set dictionaries:</span></span>

-   <span data-ttu-id="f337b-115">L’ID de propriété 0 n’a pas d’indicateur de type.</span><span class="sxs-lookup"><span data-stu-id="f337b-115">Property ID 0 does not have a type indicator.</span></span> <span data-ttu-id="f337b-116">Le type de données **DWORD** qui indique le nombre d’entrées se trouve dans la position de l’indicateur de type.</span><span class="sxs-lookup"><span data-stu-id="f337b-116">The **DWORD** data type that indicates the count of entries sits in the type-indicator position.</span></span>
-   <span data-ttu-id="f337b-117">Le nombre de caractères dans la chaîne *CCH* comprend le caractère zéro qui termine la chaîne.</span><span class="sxs-lookup"><span data-stu-id="f337b-117">The count of characters in the *cch* string includes the zero character that terminates the string.</span></span> <span data-ttu-id="f337b-118">Lorsque la page de codes du jeu de propriétés n’est pas Unicode, ce champ est en fait un nombre d' **octets** .</span><span class="sxs-lookup"><span data-stu-id="f337b-118">When the codepage of the property set is not Unicode, this field is actually a **byte** count.</span></span> <span data-ttu-id="f337b-119">Pour les jeux de propriétés dont la version de format est égale à 0, ce nombre ne peut pas dépasser 256.</span><span class="sxs-lookup"><span data-stu-id="f337b-119">For property sets with a format version of 0, this count may not exceed 256.</span></span> <span data-ttu-id="f337b-120">Pour les jeux de propriétés avec une version de format égale à 1, ce nombre peut être aussi élevé que celui autorisé par la taille totale du jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="f337b-120">For property sets with a format version of 1, this count may be as large as is allowed by the total property set size.</span></span>
-   <span data-ttu-id="f337b-121">Le dictionnaire est facultatif.</span><span class="sxs-lookup"><span data-stu-id="f337b-121">The dictionary is optional.</span></span> <span data-ttu-id="f337b-122">Tous les noms des propriétés de l’ensemble ne doivent pas nécessairement apparaître dans le dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="f337b-122">Not all the names of properties in the set are required to appear in the dictionary.</span></span> <span data-ttu-id="f337b-123">À l’inverse, tous les noms du dictionnaire ne sont pas requis pour correspondre aux propriétés dans le jeu.</span><span class="sxs-lookup"><span data-stu-id="f337b-123">Conversely, not all names in the dictionary are required to correspond to properties in the set.</span></span> <span data-ttu-id="f337b-124">Le dictionnaire doit omettre les entrées pour les propriétés supposées être universellement reconnues par les applications qui manipulent le jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="f337b-124">The dictionary should omit entries for properties assumed to be universally recognized by applications manipulating the property set.</span></span> <span data-ttu-id="f337b-125">En règle générale, les noms des jeux de propriétés de base pour les normes largement acceptées sont omis, mais les jeux de propriétés à usage spécifique peuvent inclure des dictionnaires à utiliser par les navigateurs.</span><span class="sxs-lookup"><span data-stu-id="f337b-125">Typically, names for the base property sets for widely-accepted standards are omitted, but special-purpose property sets may include dictionaries for use by browsers.</span></span>
-   <span data-ttu-id="f337b-126">Les noms de propriété dans le dictionnaire sont stockés dans la page de codes indiquée par l' [ID de propriété 1](/windows/desktop/Stg/reserved-property-identifiers).</span><span class="sxs-lookup"><span data-stu-id="f337b-126">Property names in the dictionary are stored in the code page indicated by [Property ID 1](/windows/desktop/Stg/reserved-property-identifiers).</span></span> <span data-ttu-id="f337b-127">Pour les pages de codes ANSI, chaque entrée de dictionnaire est alignée sur les octets.</span><span class="sxs-lookup"><span data-stu-id="f337b-127">For ANSI code pages, each dictionary entry is byte-aligned.</span></span> <span data-ttu-id="f337b-128">Ainsi, il n’y a pas d’espace entre les noms de propriété avec l’ID de propriété 0.</span><span class="sxs-lookup"><span data-stu-id="f337b-128">Thus, there is no spacing between property names with Property ID 0.</span></span> <span data-ttu-id="f337b-129">C’est le seul cas où les valeurs des types de données **DWORD** (ID de propriété et nom de propriété-longueur **DWORD** s) ne doivent pas obligatoirement être alignées sur les limites de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f337b-129">This is the only case where values of **DWORD** data types (the property ID and property name-length **DWORD** s) are not required to be aligned on 32-bit boundaries.</span></span> <span data-ttu-id="f337b-130">Pour les pages Unicode, chaque entrée de dictionnaire est alignée sur 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f337b-130">For Unicode pages, each dictionary entry is 32-bit aligned.</span></span>
-   <span data-ttu-id="f337b-131">Les noms de propriété qui commencent par les caractères Unicode binaires 0x0001 à 0x001F sont réservés pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f337b-131">Property names that begin with the binary Unicode characters 0x0001 through 0x001F are reserved for future use.</span></span>
-   <span data-ttu-id="f337b-132">Le nom de propriété associé à l’ID de propriété 0 représente le nom du jeu de propriétés entier.</span><span class="sxs-lookup"><span data-stu-id="f337b-132">The property name associated with Property ID 0 represents the name of the entire property set.</span></span>

 

 