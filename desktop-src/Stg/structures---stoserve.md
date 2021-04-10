---
title: Structures-StoServe
description: Le coemballage regroupe la couleur, la largeur et les coordonnées du stylet dans les structures INKDATA et les stocke dans un tableau alloué dynamiquement qu’il gère en mémoire.
ms.assetid: 25e68c39-5306-4ad6-85dd-a8a5e256abf0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9868f38d7915185b8d3511bd1bf6faa9c7a1e1b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939864"
---
# <a name="structures---stoserve"></a><span data-ttu-id="7dc37-103">Structures-StoServe</span><span class="sxs-lookup"><span data-stu-id="7dc37-103">Structures - StoServe</span></span>

<span data-ttu-id="7dc37-104">Le coemballage regroupe la couleur, la largeur et les coordonnées du stylet dans les structures **INKDATA** et les stocke dans un tableau alloué dynamiquement qu’il gère en mémoire.</span><span class="sxs-lookup"><span data-stu-id="7dc37-104">COPaper packages the pen color, width, and coordinates into **INKDATA** structures and stores them in a dynamically allocated array that it manages in memory.</span></span>

## <a name="inkdata-structure"></a><span data-ttu-id="7dc37-105">INKDATA, structure</span><span class="sxs-lookup"><span data-stu-id="7dc37-105">INKDATA Structure</span></span>

<span data-ttu-id="7dc37-106">Voici les déclarations de la structure **INKDATA** à partir de Paper. H.</span><span class="sxs-lookup"><span data-stu-id="7dc37-106">The following are the declarations for the **INKDATA** structure from PAPER.H.</span></span>

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

<span data-ttu-id="7dc37-107">Le tableau dynamique de ces paquets **INKDATA** est pointé par m \_ paInkData, membre de la classe d’implémentation [**IPaper**](ipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="7dc37-107">The dynamic array of these **INKDATA** packets is pointed to by m\_paInkData, a member of the [**IPaper**](ipaper-methods.md) implementation class.</span></span> <span data-ttu-id="7dc37-108">Le tableau est créé dans la méthode **IPaper :: InitPaper** avec une allocation initiale.</span><span class="sxs-lookup"><span data-stu-id="7dc37-108">The array is created within the **IPaper::InitPaper** method with an initial allocation.</span></span> <span data-ttu-id="7dc37-109">Pour plus d’informations, consultez la méthode **InitPaper** et la méthode de l’utilitaire NextSlot privé de l’implémentation CIMPIPAPER dans Paper. H.</span><span class="sxs-lookup"><span data-stu-id="7dc37-109">For details, see the **InitPaper** method and the private NextSlot utility method of the CImpIPaper implementation in PAPER.H.</span></span> <span data-ttu-id="7dc37-110">Les méthodes [**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md)et [**InkStop**](cguipaper-methods.md) utilisent NextSlot pour obtenir de nouveaux emplacements dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="7dc37-110">The [**InkStart**](inkstart-method.md), [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods use NextSlot to obtain new slots in the array.</span></span> <span data-ttu-id="7dc37-111">Le tableau est développé dynamiquement par NextSlot en cas de besoin.</span><span class="sxs-lookup"><span data-stu-id="7dc37-111">The array is expanded dynamically by NextSlot as the need arises.</span></span>

<span data-ttu-id="7dc37-112">Le client appelle la méthode [**IPaper :: Erase**](ipaper-methods.md) pour effacer le dessin actuel.</span><span class="sxs-lookup"><span data-stu-id="7dc37-112">The client calls the [**IPaper::Erase**](ipaper-methods.md) method to erase the current drawing.</span></span> <span data-ttu-id="7dc37-113">Cette méthode ne réalloue pas le tableau ; Il marque simplement toutes les données de l’encre en cours comme INKTYPE \_ None et réinitialise l’index de fin de données du tableau à zéro.</span><span class="sxs-lookup"><span data-stu-id="7dc37-113">This method does not reallocate the array; it simply marks all current ink data as INKTYPE\_NONE and resets the array's end-of-data index to zero.</span></span>

<span data-ttu-id="7dc37-114">Le client appelle les méthodes [**IPaper :: Lock**](ipaper-methods.md) et **Unlock** pour gérer la propriété du codocument pour le dessin.</span><span class="sxs-lookup"><span data-stu-id="7dc37-114">The client calls the [**IPaper::Lock**](ipaper-methods.md) and **Unlock** methods to manage ownership of COPaper for drawing.</span></span> <span data-ttu-id="7dc37-115">Ces méthodes sont fournies pour organiser l’accès entre plusieurs clients au dessin détenu dans un codocument partagé.</span><span class="sxs-lookup"><span data-stu-id="7dc37-115">These methods are provided to organize access among multiple clients to the drawing held in a shared COPaper.</span></span>

## <a name="paper_properties-structure"></a><span data-ttu-id="7dc37-116">Structure des propriétés du papier \_</span><span class="sxs-lookup"><span data-stu-id="7dc37-116">PAPER\_PROPERTIES Structure</span></span>

<span data-ttu-id="7dc37-117">Le client appelle la méthode [**IPaper :: Resize**](ipaper-methods.md) pour indiquer au codocument que l’utilisateur a redimensionné le rectangle de papier de dessin actuel.</span><span class="sxs-lookup"><span data-stu-id="7dc37-117">The client calls the [**IPaper::Resize**](ipaper-methods.md) method to tell COPaper that the user resized the current drawing paper rectangle.</span></span> <span data-ttu-id="7dc37-118">Ces données de coordonnée sont conservées dans une structure de **\_ Propriétés de papier** , qui est stockée avec les données d’encre lorsque toutes les données de papier sont stockées dans un fichier composé.</span><span class="sxs-lookup"><span data-stu-id="7dc37-118">This coordinate data is kept in a **PAPER\_PROPERTIES** structure, which is stored with the ink data when all the paper data is stored in a compound file.</span></span>

<span data-ttu-id="7dc37-119">Voici la déclaration sur **les \_ Propriétés de papier** de Paper. H.</span><span class="sxs-lookup"><span data-stu-id="7dc37-119">The following is the **PAPER\_PROPERTIES** declaration from PAPER.H.</span></span>

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

<span data-ttu-id="7dc37-120">La structure des **\_ Propriétés de papier** est conçue afin que de nouveaux formats de données d’encre puissent être ajoutés à tout moment à mesure que le composant DllPaper évolue.</span><span class="sxs-lookup"><span data-stu-id="7dc37-120">The **PAPER\_PROPERTIES** structure is designed so that new ink data formats can be added at any time as the DllPaper component evolves.</span></span> <span data-ttu-id="7dc37-121">L’interface [**IPaper**](ipaper-methods.md) est suffisamment générale pour qu’une version ultérieure du composant DllPaper puisse stocker un format de données manuscrites différent lors de l’implémentation de la même interface **IPaper** .</span><span class="sxs-lookup"><span data-stu-id="7dc37-121">The [**IPaper**](ipaper-methods.md) interface is general enough that a subsequent version of the DllPaper component may store a different ink data format while implementing the same **IPaper** interface.</span></span> <span data-ttu-id="7dc37-122">Étant donné que les méthodes de **IPaper** ne dépendent pas d’un format de données manuscrites spécifique, une nouvelle version du composant DllPaper qui prend en charge un autre format de données manuscrites peut utiliser cette même interface.</span><span class="sxs-lookup"><span data-stu-id="7dc37-122">Because the methods of **IPaper** do not depend on a specific ink data format, a new version of the DllPaper component that does support a different ink data format can use this same interface.</span></span>

<span data-ttu-id="7dc37-123">Les propriétés de papier stockées dans un fichier composé enregistrent la taille actuelle du tableau de données manuscrites.</span><span class="sxs-lookup"><span data-stu-id="7dc37-123">The paper properties stored in a compound file record the current size of the ink data array.</span></span> <span data-ttu-id="7dc37-124">La taille de tableau appropriée peut ensuite être allouée pour s’adapter aux données manuscrites lues à partir du fichier.</span><span class="sxs-lookup"><span data-stu-id="7dc37-124">The proper array size can then be allocated to accommodate the ink data read from the file.</span></span>

<span data-ttu-id="7dc37-125">La structure des **\_ Propriétés du papier** stocke également la taille du rectangle de dessin de l’aire de papier et la couleur de la fenêtre d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="7dc37-125">The **PAPER\_PROPERTIES** structure also stores the paper surface's drawing rectangle size and background window color.</span></span>

<span data-ttu-id="7dc37-126">Bien que cela ne soit pas utilisé dans les exemples **StoServe** / **StoClien** , il est également possible de stocker un titre de dessin et un nom d’auteur.</span><span class="sxs-lookup"><span data-stu-id="7dc37-126">Though not used in the **StoServe**/**StoClien** samples, a drawing title and an author name can also be stored.</span></span>

<span data-ttu-id="7dc37-127">La date de création et les dates de dernière modification ne sont pas incluses dans les propriétés de ce document, car l’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) utilisée pour accéder aux fichiers composés gère ces informations.</span><span class="sxs-lookup"><span data-stu-id="7dc37-127">Creation date and last modified dates are not included in these paper properties, because the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface used to access compound files manages this information.</span></span>

 

 




