---
title: Structures-StoServe
description: Le coemballage regroupe la couleur, la largeur et les coordonnées du stylet dans les structures INKDATA et les stocke dans un tableau alloué dynamiquement qu’il gère en mémoire.
ms.assetid: 25e68c39-5306-4ad6-85dd-a8a5e256abf0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f81b46f2f0a992f27ed405361734fe53db98cf9272697b88866451ef1d7d4b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796889"
---
# <a name="structures---stoserve"></a>Structures-StoServe

Le coemballage regroupe la couleur, la largeur et les coordonnées du stylet dans les structures **INKDATA** et les stocke dans un tableau alloué dynamiquement qu’il gère en mémoire.

## <a name="inkdata-structure"></a>INKDATA, structure

Voici les déclarations de la structure **INKDATA** à partir de Paper. H.

``` syntax
// The types of Ink Data.
#define INKTYPE_NONE  0
#define INKTYPE_START 1
#define INKTYPE_DRAW  2
#define INKTYPE_STOP  3

  // The Ink Data structure.
  typedef struct _INKDATA
  {
    SHORT nType;            // Ink Type.
    SHORT nX;               // X-coordinate of ink point.
    SHORT nY;               // Y-coordinate of ink point.
    SHORT nWidth;           // Ink line width in pixels.
    COLORREF crColor;       // Ink color.
  } INKDATA;
```

Le tableau dynamique de ces paquets **INKDATA** est pointé par m \_ paInkData, membre de la classe d’implémentation [**IPaper**](ipaper-methods.md) . Le tableau est créé dans la méthode **IPaper :: InitPaper** avec une allocation initiale. Pour plus d’informations, consultez la méthode **InitPaper** et la méthode de l’utilitaire NextSlot privé de l’implémentation CIMPIPAPER dans Paper. H. Les méthodes [**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md)et [**InkStop**](cguipaper-methods.md) utilisent NextSlot pour obtenir de nouveaux emplacements dans le tableau. Le tableau est développé dynamiquement par NextSlot en cas de besoin.

Le client appelle la méthode [**IPaper :: Erase**](ipaper-methods.md) pour effacer le dessin actuel. Cette méthode ne réalloue pas le tableau ; Il marque simplement toutes les données de l’encre en cours comme INKTYPE \_ None et réinitialise l’index de fin de données du tableau à zéro.

Le client appelle les méthodes [**IPaper :: Lock**](ipaper-methods.md) et **Unlock** pour gérer la propriété du codocument pour le dessin. Ces méthodes sont fournies pour organiser l’accès entre plusieurs clients au dessin détenu dans un codocument partagé.

## <a name="paper_properties-structure"></a>Structure des propriétés du papier \_

Le client appelle la méthode [**IPaper :: Resize**](ipaper-methods.md) pour indiquer au codocument que l’utilisateur a redimensionné le rectangle de papier de dessin actuel. Ces données de coordonnée sont conservées dans une structure de **\_ Propriétés de papier** , qui est stockée avec les données d’encre lorsque toutes les données de papier sont stockées dans un fichier composé.

Voici la déclaration sur **les \_ Propriétés de papier** de Paper. H.

``` syntax
#define PAPER_TITLE_SIZE 64
  typedef struct _PAPER_PROPERTIES
  {
    LONG lInkDataVersion;
    LONG lInkArraySize;
    COLORREF crWinColor;
    RECT WinRect;
    WCHAR wszTitle[PAPER_TITLE_SIZE];
    WCHAR wszAuthor[PAPER_TITLE_SIZE];
    WCHAR wszReserved1[PAPER_TITLE_SIZE];
    WCHAR wszReserved2[PAPER_TITLE_SIZE];
  } PAPER_PROPERTIES;
```

La structure des **\_ Propriétés de papier** est conçue afin que de nouveaux formats de données d’encre puissent être ajoutés à tout moment à mesure que le composant DllPaper évolue. L’interface [**IPaper**](ipaper-methods.md) est suffisamment générale pour qu’une version ultérieure du composant DllPaper puisse stocker un format de données manuscrites différent lors de l’implémentation de la même interface **IPaper** . Étant donné que les méthodes de **IPaper** ne dépendent pas d’un format de données manuscrites spécifique, une nouvelle version du composant DllPaper qui prend en charge un autre format de données manuscrites peut utiliser cette même interface.

Les propriétés de papier stockées dans un fichier composé enregistrent la taille actuelle du tableau de données manuscrites. La taille de tableau appropriée peut ensuite être allouée pour s’adapter aux données manuscrites lues à partir du fichier.

La structure des **\_ Propriétés du papier** stocke également la taille du rectangle de dessin de l’aire de papier et la couleur de la fenêtre d’arrière-plan.

Bien que cela ne soit pas utilisé dans les exemples **StoServe** / **StoClien** , il est également possible de stocker un titre de dessin et un nom d’auteur.

La date de création et les dates de dernière modification ne sont pas incluses dans les propriétés de ce document, car l’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) utilisée pour accéder aux fichiers composés gère ces informations.

 

 




