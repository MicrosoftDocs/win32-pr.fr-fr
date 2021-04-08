---
title: Conventions de style de codage
description: Les conventions de style de codage sont utilisées dans cette série d’exemples pour faciliter la clarté et la cohérence.
ms.assetid: d5e81a52-79f6-4561-891c-05fee125a1b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28e65e19d69f060a5f85d86976c4bd3694f7611
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734964"
---
# <a name="coding-style-conventions"></a>Conventions de style de codage

Les conventions de style de codage sont utilisées dans cette série d’exemples pour faciliter la clarté et la cohérence. Les conventions de notation « hongrois » sont utilisées. Ils sont devenus une pratique de codage courante dans la programmation Win32. Elles incluent des notations de préfixe variables qui donnent à des noms de variables une suggestion du type de la variable.

Le tableau suivant répertorie les préfixes courants.



| Préfixe | Description                         |
|--------|-------------------------------------|
| a      | Array                               |
| b      | BOOL (int)                          |
| c      | Char                                |
| libéré     | Nombre d’octets                      |
| cr     | Valeur de référence de couleur               |
| adéquat     | Nombre de x (short)                  |
| dw     | DWORD (unsigned long)               |
| f      | Indicateurs (généralement plusieurs valeurs de bits) |
| fn     | Fonction                            |
| activée\_    | Global                              |
| h      | Handle                              |
| i      | Integer                             |
| l      | Long                                |
| lp     | Pointeur long                        |
| lecteur\_    | Données membres d’une classe              |
| n      | Entier Short                           |
| p      | Pointeur                             |
| s      | String                              |
| sz     | Chaîne terminée par zéro              |
| tm     | Mesure du texte                         |
| u      | Entier non signé                        |
| UL     | Unsigned long (ULONG)               |
| w      | WORD (unsigned short)               |
| x, y    | coordonnées x, y (short)            |



 

Elles sont souvent combinées, comme dans l’exemple suivant.



| Combinaison de préfixes | Description                                             |
|--------------------|---------------------------------------------------------|
| pszMyString        | Pointeur vers une chaîne.                                  |
| m \_ pszMyString     | Pointeur vers une chaîne qui est un membre de données d’une classe. |



 

Les autres conventions sont répertoriées dans le tableau suivant.



| Convention       | Description                                              |
|------------------|----------------------------------------------------------|
| Étiquettes         | Préfixe’C’pour les noms de classe C++.                          |
| COMyObjectClass  | Préfixe’CO’pour les noms de classes d’objets COM.                  |
| CFMyClassFactory | Préfixe « CF » pour les noms de fabrique de classes COM.                 |
| IMyInterface     | Préfixe’I’pour les noms de classe d’interface COM.                |
| CImpIMyInterface | Préfixe’CImpI’pour les classes d’implémentation de l’interface COM. |



 

Certaines conventions cohérentes pour les blocs d’en-tête de commentaire sont utilisées dans cette série d’exemples comme suit.

## <a name="file-header"></a>En-tête de fichier

``` syntax
/*+===================================================================
  File:      MYFILE.EXT

  Summary:   Brief summary of the file contents and purpose.

  Classes:   Classes declared or used (in source files).

  Functions: Functions exported (in source files).

  Origin:    Indications of where content may have come from. This
             is not a change history but rather a reference to the
             editor-inheritance behind the content or other
             indications about the origin of the source.

  Copyright and Legal notices.
  Copyright and Legal notices.
===================================================================+*/
```

## <a name="plain-comment-block"></a>Bloc de commentaire brut

``` syntax
/*--------------------------------------------------------------------
  Plain block of comment text that usually takes several lines.
  Plain block of comment text that usually takes several lines.
--------------------------------------------------------------------*/
```

## <a name="class-declaration-header"></a>En-tête de déclaration de classe

``` syntax
/*C+C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C+++C
  Class:    CMyClass

  Summary:  Short summary of purpose and content of CMyClass.
            Short summary of purpose and content of CMyClass.

  Methods:  MyMethodOne
              Short description of MyMethodOne.
            MyMethodTwo
              Short description of MyMethodTwo.
            CMyClass
              Constructor.
            ~CMyClass
              Destructor.
C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C---C-C*/
```

## <a name="class-method-definition-header"></a>En-tête de définition de méthode de classe

``` syntax
/*M+M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M+++M
  Method:   CMyClass::MyMethodOne

  Summary:  Short summary of purpose and content of MyMethodOne.
            Short summary of purpose and content of MyMethodOne.

  Args:     MYTYPE MyArgOne
              Short description of argument MyArgOne.
            MYTYPE MyArgTwo
              Short description of argument MyArgTwo.

  Modifies: [list of member data variables modified by this method].

  Returns:  MYRETURNTYPE
              Short description of meaning of the return type values.
M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M---M-M*/
```

## <a name="unexported-or-local-function"></a>Fonction non exportée ou locale

``` syntax
/*F+F+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
  Function: MyLocalFunction

  Summary:  What MyLocalFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
-----------------------------------------------------------------F-F*/
```

## <a name="exported-function-definition-header"></a>En-tête de définition de fonction exportée

``` syntax
/*F+F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F+++F
  Function: MyFunction

  Summary:  What MyFunction is for and what it does.

  Args:     MYTYPE MyFunctionArgument1
              Description.
            MYTYPE MyFunctionArgument1
              Description.

  Returns:  MyReturnType
              Description.
F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F---F-F*/
```

## <a name="com-interface-declaration-header"></a>En-tête de déclaration de l’interface COM

``` syntax
/*I+I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I+++I
  Interface: IMyInterface

  Summary:   Short summary of what features the interface can bring to
             a COM Component.

  Methods:   MYTYPE MyMethodOne
               Description.
             MYTYPE MyMethodTwo
               Description.
I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I---I-I*/
```

## <a name="com-object-class-declaration-header"></a>En-tête de déclaration de classe d’objets COM

``` syntax
/*O+O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O+++O
  ObjectClass: COMyCOMObject

  Summary:     Short summary of purpose and content of this object.

  Interfaces:  IUnknown
                 Standard interface providing COM object features.
               IMyInterfaceOne
                 Description.
               IMyInterfaceTwo
                 Description.

  Aggregation: [whether this COM Object is aggregatable or not]
O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O---O-O*/
```

Toutes ces conventions de bloc de commentaires ont des chaînes de jeton de début et de fin cohérentes. Cette cohérence prend en charge le traitement automatique des en-têtes d’une certaine manière. Par exemple, les scripts AWK peuvent être écrits pour filtrer les en-têtes de fonction dans un fichier texte distinct qui peut ensuite servir de base pour un document de spécification. De même, les outils tels que l’utilitaire autoduck non pris en charge (actuellement disponible sur le CD-ROM de la bibliothèque de développement Microsoft Developer Network) peuvent être utilisés pour traiter les blocs de commentaires dans ces en-têtes.

Le tableau suivant répertorie les chaînes de jetons de début et de fin utilisées dans les exemples de didacticiels.



| par jeton | Description                      |
|-------|----------------------------------|
| /\*+  | Début de l’en-tête de fichier                |
| +\*/  | Fin d’en-tête de fichier                  |
| /\*-  | Début de l’en-tête de bloc de commentaire brut |
| -\*/  | Fin d’en-tête de bloc de commentaire brut   |
| /\*Secteur  | Début de l’en-tête de classe               |
| Secteur\*/  | Fin d’en-tête de classe                 |
| /\*Lecteur  | Début de l’en-tête de méthode              |
| Lecteur\*/  | Fin de l’en-tête de méthode                |
| /\*FA  | Début de l’en-tête de fonction            |
| FA\*/  | Fin d’en-tête de fonction              |
| /\*Cliqu  | Début de l’en-tête d’interface           |
| Cliqu\*/  | Fin d’en-tête d’interface             |
| /\*Sorties  | Début de l’en-tête de classe d’objet COM    |
| Sorties\*/  | Fin d’en-tête de classe d’objet COM      |



 

Ces en-têtes peuvent également être utilisés comme signaux visuels pour une analyse rapide des fichiers sources. Ils facilitent également l’obtention rapide d’un emplacement source si vous configurez des chaînes de recherche dans votre éditeur, puis « répéter la dernière recherche » pour localiser rapidement ces en-têtes.

Par exemple, la chaîne de recherche « M + M » localise le début des en-têtes de la méthode et « M-M » localise le début du code réel de la définition de la méthode/de l’implémentation.

 

 




