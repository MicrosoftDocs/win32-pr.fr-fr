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
# <a name="property-set-display-name-dictionary"></a>Dictionnaire des noms d’affichage des jeux de propriétés

Un dictionnaire de noms d’affichage de propriété permet aux utilisateurs de jeux de propriétés d’attacher la signification aux propriétés, au-delà de celles fournies par l’indicateur de type.

## <a name="dictionary-structure"></a>Structure du dictionnaire

Le dictionnaire contient un nombre d’entrées dans la liste, suivi d’une liste d’entrées de dictionnaire.

``` syntax
typedef struct tagDICTIONARY 
{ 
    DWORD  cEntries ;               // Count of entries in the list 
    ENTRY  rgEntry[ cEntries ] ;    // Property ID/String pair 
} DICTIONARY ;
```

## <a name="dictionary-entry-structure"></a>Structure d’entrée de dictionnaire

Chaque entrée de dictionnaire de la liste est une paire identificateur de propriété/chaîne. Voici une définition de Pseudo-structure pour une entrée de dictionnaire. Il s’agit d’une Pseudo-structure, car la \[ \] taille du membre SZ est variable.

``` syntax
typedef struct tagENTRY 
{ 
    DWORD  propid ;    // Property ID 
    DWORD  cch ;       // Count of characters in the string 
    char  sz[cch];     // Zero-terminated string 
} ENTRY ;
```

## <a name="sample-dictionary"></a>Exemple de dictionnaire

L’exemple de transfert de données boursières suivant peut inclure un nom affichable « stock quote » pour l’ensemble du jeu et « Symbol ticker » pour le \_ symbole PID. Si un jeu de propriétés ne contenait qu’un symbole et le dictionnaire, la section Property Set aurait un flux d’octets qui ressemble à ce qui suit.

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

Tenez compte des problèmes suivants concernant les dictionnaires de jeux de propriétés :

-   L’ID de propriété 0 n’a pas d’indicateur de type. Le type de données **DWORD** qui indique le nombre d’entrées se trouve dans la position de l’indicateur de type.
-   Le nombre de caractères dans la chaîne *CCH* comprend le caractère zéro qui termine la chaîne. Lorsque la page de codes du jeu de propriétés n’est pas Unicode, ce champ est en fait un nombre d' **octets** . Pour les jeux de propriétés dont la version de format est égale à 0, ce nombre ne peut pas dépasser 256. Pour les jeux de propriétés avec une version de format égale à 1, ce nombre peut être aussi élevé que celui autorisé par la taille totale du jeu de propriétés.
-   Le dictionnaire est facultatif. Tous les noms des propriétés de l’ensemble ne doivent pas nécessairement apparaître dans le dictionnaire. À l’inverse, tous les noms du dictionnaire ne sont pas requis pour correspondre aux propriétés dans le jeu. Le dictionnaire doit omettre les entrées pour les propriétés supposées être universellement reconnues par les applications qui manipulent le jeu de propriétés. En règle générale, les noms des jeux de propriétés de base pour les normes largement acceptées sont omis, mais les jeux de propriétés à usage spécifique peuvent inclure des dictionnaires à utiliser par les navigateurs.
-   Les noms de propriété dans le dictionnaire sont stockés dans la page de codes indiquée par l' [ID de propriété 1](/windows/desktop/Stg/reserved-property-identifiers). Pour les pages de codes ANSI, chaque entrée de dictionnaire est alignée sur les octets. Ainsi, il n’y a pas d’espace entre les noms de propriété avec l’ID de propriété 0. C’est le seul cas où les valeurs des types de données **DWORD** (ID de propriété et nom de propriété-longueur **DWORD** s) ne doivent pas obligatoirement être alignées sur les limites de 32 bits. Pour les pages Unicode, chaque entrée de dictionnaire est alignée sur 32 bits.
-   Les noms de propriété qui commencent par les caractères Unicode binaires 0x0001 à 0x001F sont réservés pour une utilisation ultérieure.
-   Le nom de propriété associé à l’ID de propriété 0 représente le nom du jeu de propriétés entier.

 

 