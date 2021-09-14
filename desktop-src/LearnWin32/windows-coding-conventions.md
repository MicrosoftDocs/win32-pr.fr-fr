---
title: Windows Conventions de codage
description: si vous débutez avec la programmation de Windows, il peut être déconcerté quand vous consultez un programme Windows pour la première fois.
ms.assetid: 466a66db-7681-4fce-9672-07849cd1b096
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365a9c8509d7cb799bafdfa70c326f1074b64d93
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094261"
---
# <a name="windows-coding-conventions"></a>Windows Conventions de codage

si vous débutez avec la programmation de Windows, il peut être déconcerté quand vous consultez un programme Windows pour la première fois. Le code est rempli avec des définitions de type étrange comme **DWORD \_ ptr** et **LPRECT**, et les variables ont des noms tels que *HWND* et *PWSZ* (appelé notation hongroise). il est judicieux de prendre un moment pour apprendre certaines des conventions de codage Windows.

la grande majorité des api Windows se composent de fonctions ou d’interfaces COM (component Object Model). très peu d’api Windows sont fournies en tant que classes C++. (une exception notable est GDI+, l’une des api graphiques 2d.)

## <a name="typedefs"></a>Typedefs

les en-têtes Windows contiennent un grand nombre de typedefs. Un grand nombre d’entre eux sont définis dans le fichier d’en-tête WinDef. h. Voici quelques-uns que vous rencontrerez souvent.

### <a name="integer-types"></a>Types d'entier



| Type de données     | Taille    | Abonné?  |
|---------------|---------|----------|
| **BYTE**      | 8 bits  | Non signé |
| **DWORD**     | 32 bits | Non signé |
| **ENTIER**     | 32 bits | Signé   |
| **INT64**     | 64 bits | Signé   |
| **LONG**      | 32 bits | Signé   |
| **LONGLONG**  | 64 bits | Signé   |
| **UINT32**    | 32 bits | Non signé |
| **UINT64**    | 64 bits | Non signé |
| **ULONG**     | 32 bits | Non signé |
| **ULONGLONG** | 64 bits | Non signé |
| **WORD**      | 16 bits | Non signé |



 

Comme vous pouvez le voir, il existe une certaine redondance dans ces typedefs. une partie de ce chevauchement est simplement due à l’historique des api Windows. Les types répertoriés ici ont une taille fixe et les tailles sont les mêmes dans les applications 32 bits et 64. Par exemple, le type **DWORD** est toujours de 32 bits de largeur.

### <a name="boolean-type"></a>Type booléen

**Bool** est un typedef pour une valeur entière qui est utilisée dans un contexte booléen. Le fichier d’en-tête WinDef. h définit également deux valeurs à utiliser avec **bool**.


```C++
#define FALSE    0 
#define TRUE     1
```



Toutefois, en dépit de cette définition de **true**, la plupart des fonctions qui retournent un type **bool** peuvent retourner toute valeur différente de zéro pour indiquer la vérité booléenne. Par conséquent, vous devez toujours écrire ce qui suit :


```C++
// Right way.
BOOL result = SomeFunctionThatReturnsBoolean();
if (result) 
{ 
    ...
}
```



et non :


```C++
// Wrong!
if (result == TRUE) 
{
    ... 
}
```



N’oubliez pas que **bool** est un type entier et qu’il n’est pas interchangeable avec le type **bool** C++.

### <a name="pointer-types"></a>Types pointeur

Windows définit de nombreux types de données de la forme *pointeur vers X*. Ils ont généralement le préfixe *P* ou *LP* dans le nom. Par exemple, **LPRECT** est un pointeur vers [**Rect**](/previous-versions//dd162897(v=vs.85)), où **Rect** est une structure qui décrit un rectangle. Les déclarations de variables suivantes sont équivalentes.


```C++
RECT*  rect;  // Pointer to a RECT structure.
LPRECT rect;  // The same
PRECT  rect;  // Also the same.
```



Historiquement, *P* correspond à « pointeur » et la *LP* à « pointeur long ». les pointeurs longs (également appelés *pointeurs far*) sont un holdover de 16 bits Windows, lorsqu’ils étaient nécessaires pour adresser des plages de mémoire en dehors du segment actuel. Le préfixe *LP* a été conservé pour faciliter le portage du code 16 bits vers le Windows 32 bits. À l’heure actuelle, il n’existe aucune distinction : un pointeur est un pointeur.

### <a name="pointer-precision-types"></a>Types de précision des pointeurs

Les types de données suivants sont toujours la taille d’un pointeur, c’est-à-dire 32 bits de largeur dans les applications 32 bits et 64 bits de largeur dans les applications 64 bits. La taille est déterminée au moment de la compilation. quand une application 32 bits s’exécute sur le Windows 64 bits, ces types de données ont toujours une largeur de 4 octets. (une application 64 bits ne peut pas s’exécuter sur le Windows 32 bits, donc la situation inverse ne se produit pas.)

-   **\_ptr DWORD**
-   **\_pointeur int**
-   **\_ptr long**
-   **ULONG ( \_ PTR)**
-   **UINT \_ ptr**

Ces types sont utilisés dans les situations où un entier peut être casté en un pointeur. Elles servent également à définir des variables pour les opérations arithmétiques sur les pointeurs et à définir des compteurs de boucle qui effectuent une itération sur la plage complète d’octets dans les mémoires tampons. Plus généralement, elles apparaissent à des endroits où une valeur 32 bits existante a été étendue à 64 bits sur une Windows 64 bits.

## <a name="hungarian-notation"></a>Notation hongroise

La *notation hongroise* est la pratique consistant à ajouter des préfixes aux noms de variables, afin de fournir des informations supplémentaires sur la variable. (L’invente de la notation, Charles Simonyi, était hongrois, donc son nom).

Dans sa forme d’origine, la notation hongroise fournit des informations *sémantiques* sur une variable, en vous indiquant l’utilisation prévue. Par exemple, *je* signifie un index, *CB* signifie une taille en octets (« nombre d’octets ») et les numéros de ligne et de colonne pour les colonnes *RW* et *col* . Ces préfixes sont conçus pour éviter l’utilisation accidentelle d’une variable dans un contexte incorrect. Par exemple, si vous avez vu l’expression `rwPosition +  cbTable` , vous savez qu’un numéro de ligne est ajouté à une taille, ce qui est presque certainement un bogue dans le code

Une forme plus courante de notation hongroise utilise des préfixes pour fournir des informations de *type* , par exemple, *DW* pour **DWORD** et *w* pour **Word**.

Si vous recherchez « notation hongroise » sur le Web, vous trouverez un grand nombre d’opinions indiquant si la notation hongroise est correcte ou incorrecte. Certains programmeurs ont une plus forte non-notation hongroise. D’autres le trouvent utiles. Quoi qu’il en soit, un grand nombre d’exemples de code sur MSDN utilisent la notation hongroise, mais vous n’avez pas besoin de mémoriser les préfixes pour comprendre le code.

## <a name="next"></a>Suivant

[Utilisation de chaînes](working-with-strings.md)

 

 