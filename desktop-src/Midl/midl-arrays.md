---
title: Tableaux MIDL
description: Tableaux MIDL.
ms.assetid: dee30788-0575-4b49-a6b8-5208ad295183
keywords:
- types de données MIDL, tableaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c5ca08740084783f615d2cd34b46f0de4a4020
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093410"
---
# <a name="midl-arrays"></a>Tableaux MIDL

Les déclarateurs de tableau apparaissent dans le corps de l’interface du fichier IDL comme l’un des éléments suivants :

-   Partie d’une déclaration générale
-   Membre d’un déclarateur de structure ou d’Union
-   Paramètre d’un appel de procédure distante

Les limites de chaque dimension du tableau sont exprimées à l’intérieur d’une paire de crochets distincts. Une expression qui prend la valeur *n* signifie une limite inférieure de zéro et une limite supérieure de *n-1*. Si les crochets sont vides ou contiennent un seul astérisque ( \* ), la limite inférieure est égale à zéro et la limite supérieure est déterminée au moment de l’exécution.

Le tableau peut également contenir deux valeurs séparées par des points de suspension représentant les limites inférieure et supérieure du tableau, comme dans l’exemple \[ *inférieur*... *supérieur* \] . Microsoft RPC requiert une limite inférieure de zéro. Le compilateur MIDL ne reconnaît pas les constructions qui spécifient des limites inférieures égales à zéro.

Les tableaux peuvent être associés à la taille des attributs du champ : la [**taille \_**](size-is.md) [**maximale \_**](max-is.md), la [**longueur \_ est**](length-is.md), la [**première \_ est**](first-is.md)et la [**dernière \_ la valeur**](last-is.md) de la taille du tableau ou de la partie du tableau qui contient des données valides. Ces attributs de champ identifient le paramètre, le champ de structure ou la constante qui spécifie la dimension ou l’index du tableau.

Le tableau doit être associé à l’identificateur spécifié par l’attribut field de la manière suivante : quand le tableau est un paramètre, l’identificateur doit également être un paramètre de la même fonction. Lorsque le tableau est un champ de structure, l’identificateur doit être un autre champ de structure de cette même structure.

Un tableau est appelé « conforme » si la limite supérieure d’une dimension est déterminée au moment de l’exécution. (Seules les limites supérieures peuvent être déterminées au moment de l’exécution.) Pour déterminer la limite supérieure, la déclaration de tableau doit inclure [**une \_ taille**](size-is.md) ou un attribut [**Max \_ est**](max-is.md) un attribut.

Un tableau est appelé « varying » quand ses limites sont déterminées au moment de la compilation, mais la plage d’éléments transmis est déterminée au moment de l’exécution. Pour déterminer la plage d’éléments transmis, la déclaration de tableau doit inclure [**une \_ longueur**](length-is.md), [**First \_ is**](first-is.md)ou [**Last \_ is**](last-is.md) Attribute.

Un tableau variable conforme (également appelé « Open ») est un tableau dont la limite supérieure et la plage d’éléments transmis sont déterminées au moment de l’exécution. Au maximum, un tableau variable conforme ou conforme peut être imbriqué dans une structure C et doit être le dernier élément de la structure. En revanche, les tableaux à variation non conformes peuvent apparaître n’importe où dans une structure.

## <a name="examples"></a>Exemples

``` syntax
/* IDL file interface body */ 
#define MAX_INDEX 10 
 
typedef char  ATYPE[MAX_INDEX]; 
typedef short BTYPE[];        // Equivalent to [*]; 
typedef long  CTYPE[*][10];   // [][10] 
typedef float DTYPE[0..10];   // Equivalent to [11] 
typedef float ETYPE[0..(MAX_INDEX)];  
 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string; 
 
HRESULT MyFunction( 
     [in, out] short * pSize,  
     [in, out, string, size_is(*pSize)] char a[0..*] 
);
```

Pour plus d’informations, consultez [tableaux et pointeurs](/windows/desktop/Rpc/arrays-and-pointers).

## <a name="multidimensional-arrays"></a>Tableaux multidimensionnels

L’utilisateur peut déclarer des types qui sont des tableaux, puis déclarer des tableaux d’objets de ce type. La sémantique des tableaux *m*-dimensionnels de types de tableau à *n* dimensions est identique à la sémantique des tableaux *m* + *n*-dimension.

Par exemple, le type RECT \_ type peut être défini comme un tableau à deux dimensions et la variable *Rect* peut être définie en tant que tableau de \_ type Rect. Cette valeur est équivalente à l' *équivalent \_ Rect* du tableau à trois dimensions :

``` syntax
typedef short int RECT_TYPE[10][20]; 
RECT_TYPE rect[15]; 
short int equivalent_rect[15][10][20];  // ~RECT_TYPE rect[15]
```

Microsoft RPC est orienté C. Conformément aux conventions de langage C, seule la première dimension d’un tableau multidimensionnel peut être déterminée au moment de l’exécution. L’interopérabilité avec des tableaux IDL DCE prenant en charge d’autres langues est limitée à :

-   Tableaux multidimensionnels avec limites (au moment de la compilation).
-   Tableaux multidimensionnels avec toutes les limites constantes, à l’exception de la première dimension. La limite supérieure et la plage d’éléments transmis de la première dimension dépendent du Runtime.
-   Tableau unidimensionnel avec une limite inférieure de zéro.

Lorsque l' **\[** [](string.md) **\]** attribut de chaîne est utilisé sur des tableaux multidimensionnels, l’attribut s’applique au tableau le plus à droite.

## <a name="arrays-of-pointers"></a>Tableaux de pointeurs

Les pointeurs de référence doivent pointer vers des données valides. L’application cliente doit allouer toute la mémoire pour un **\[** [**dans**](in.md) **\]** ou **\[** **dans,**[](out-idl.md) un **\]** tableau de pointeurs de référence, en particulier lorsque le tableau est associé à **\[ dans \]**, ou **\[** **dans, out \]**, la **\[** [**longueur \_ est**](length-is.md)ou que la **\]** **\[** [**dernière valeur \_ est**](last-is.md) **\]** . L’application cliente doit également initialiser tous les éléments de tableau avant l’appel. Avant de retourner au client, l’application serveur doit vérifier que tous les éléments de tableau de la plage transmis pointent vers un stockage valide.

Côté serveur, le stub alloue le stockage pour tous les éléments de tableau, quelle que soit la **\[** [**longueur \_**](length-is.md) **\]** ou la **\[** [**dernière \_**](last-is.md) **\]** valeur au moment de l’appel. Cette fonctionnalité peut affecter les performances de votre application.

Aucune restriction n’est placée sur les tableaux de pointeurs uniques. Sur le client et sur le serveur, le stockage est alloué pour les pointeurs null. Lorsque les pointeurs ne sont pas null, les données sont placées dans un stockage préalloué.

Un déclarateur de pointeur facultatif peut précéder le déclarateur de tableau.

Lorsque les pointeurs de référence incorporés sont des **\[** [](out-idl.md) **\]** paramètres de sortie uniquement, le code du gestionnaire de serveur doit assigner des valeurs valides au tableau de pointeurs de référence. Par exemple :

``` syntax
typedef [ref] short * ARefPointer;
typedef ARefPointer ArrayOfRef[10];
HRESULT proc1( [out] ArrayOfRef Parameter );
```

Les stubs générés allouent le tableau et assignent des valeurs NULL à tous les pointeurs incorporés dans le tableau.

 

 