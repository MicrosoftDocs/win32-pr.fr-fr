---
title: Données d’entrée
description: Le pipeline OpenGL vous oblige à entrer plusieurs types de données
ms.assetid: e820d093-3e39-4feb-ab2a-0c28e298bde4
keywords:
- Pipeline de traitement OpenGL, données d’entrée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 121cf032e0e718b95fd42f3001d2ff8efee1f6b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509380"
---
# <a name="input-data"></a><span data-ttu-id="14363-104">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="14363-104">Input Data</span></span>

<span data-ttu-id="14363-105">Le pipeline OpenGL vous oblige à entrer plusieurs types de données :</span><span class="sxs-lookup"><span data-stu-id="14363-105">The OpenGL pipeline requires you to input several types of data:</span></span>

-   <span data-ttu-id="14363-106">**Vertex**.</span><span class="sxs-lookup"><span data-stu-id="14363-106">**Vertices**.</span></span> <span data-ttu-id="14363-107">Les vertex décrivent la forme de l’objet géométrique souhaité.</span><span class="sxs-lookup"><span data-stu-id="14363-107">Vertices describe the shape of the desired geometric object.</span></span> <span data-ttu-id="14363-108">Pour spécifier des vertex, utilisez les fonctions [**\* glVertex**](glvertex-functions.md) conjointement à [**glBegin**](glbegin.md) et [**glEnd**](glend.md) pour créer un point, une ligne ou un polygone.</span><span class="sxs-lookup"><span data-stu-id="14363-108">To specify vertices, use [**glVertex\***](glvertex-functions.md) functions in conjunction with [**glBegin**](glbegin.md) and [**glEnd**](glend.md) to create a point, line, or polygon.</span></span> <span data-ttu-id="14363-109">Vous pouvez également utiliser [**glRect**](glrect-functions.md) pour décrire un rectangle entier à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="14363-109">You can also use [**glRect**](glrect-functions.md) to describe an entire rectangle at one time.</span></span>
-   <span data-ttu-id="14363-110">**Indicateur de périphérie**.</span><span class="sxs-lookup"><span data-stu-id="14363-110">**Edge flag**.</span></span> <span data-ttu-id="14363-111">Par défaut, tous les bords des polygones sont des bords limites.</span><span class="sxs-lookup"><span data-stu-id="14363-111">By default, all edges of polygons are boundary edges.</span></span> <span data-ttu-id="14363-112">Utilisez [**glEdgeFlag \***](gledgeflag-functions.md) pour définir explicitement l’indicateur de périphérie.</span><span class="sxs-lookup"><span data-stu-id="14363-112">Use [**glEdgeFlag\***](gledgeflag-functions.md) to explicitly set the edge flag.</span></span>
-   <span data-ttu-id="14363-113">**Position de la trame actuelle**.</span><span class="sxs-lookup"><span data-stu-id="14363-113">**Current raster position**.</span></span> <span data-ttu-id="14363-114">Spécifié avec [**glRasterPos \***](glrasterpos-functions.md), la position raster actuelle est utilisée pour déterminer les coordonnées raster pour les opérations de dessin de pixel et de bitmap.</span><span class="sxs-lookup"><span data-stu-id="14363-114">Specified with [**glRasterPos\***](glrasterpos-functions.md), the current raster position is used to determine raster coordinates for pixel- and bitmap-drawing operations.</span></span>
-   <span data-ttu-id="14363-115">**Normal actuel**.</span><span class="sxs-lookup"><span data-stu-id="14363-115">**Current normal**.</span></span> <span data-ttu-id="14363-116">Un vecteur normal associé à un vertex particulier détermine la façon dont une surface au niveau de ce vertex est orientée dans l’espace tridimensionnel. Cela affecte à son tour la quantité de lumière reçue par un vertex particulier.</span><span class="sxs-lookup"><span data-stu-id="14363-116">A normal vector associated with a particular vertex determines how a surface at that vertex is oriented in three-dimensional space; this in turn affects how much light that particular vertex receives.</span></span> <span data-ttu-id="14363-117">Utilisez [**glNormal \***](glnormal-functions.md) pour spécifier un vecteur normal.</span><span class="sxs-lookup"><span data-stu-id="14363-117">Use [**glNormal\***](glnormal-functions.md) to specify a normal vector.</span></span>
-   <span data-ttu-id="14363-118">**Couleur actuelle**.</span><span class="sxs-lookup"><span data-stu-id="14363-118">**Current color**.</span></span> <span data-ttu-id="14363-119">La couleur d’un vertex, ainsi que les conditions d’éclairage, déterminent la couleur finale et allumée.</span><span class="sxs-lookup"><span data-stu-id="14363-119">The color of a vertex, together with the lighting conditions, determine the final, lit color.</span></span> <span data-ttu-id="14363-120">La couleur est spécifiée [**avec \* glColor**](glcolor-functions.md) en mode RVBA, ou avec [**glIndex \***](glindex-functions.md) si en mode d’index des couleurs.</span><span class="sxs-lookup"><span data-stu-id="14363-120">Color is specified with [**glColor\***](glcolor-functions.md) if in RGBA mode, or with [**glIndex\***](glindex-functions.md) if in color-index mode.</span></span>
-   <span data-ttu-id="14363-121">**Coordonnées de texture actuelles**.</span><span class="sxs-lookup"><span data-stu-id="14363-121">**Current texture coordinates**.</span></span> <span data-ttu-id="14363-122">Spécifié avec [**glTexCoord \***](gltexcoord-functions.md), les coordonnées de texture déterminent l’emplacement dans une carte de texture à associer à un vertex d’un objet.</span><span class="sxs-lookup"><span data-stu-id="14363-122">Specified with [**glTexCoord\***](gltexcoord-functions.md), texture coordinates determine the location in a texture map to associate with a vertex of an object.</span></span>

> [!Note]  
> <span data-ttu-id="14363-123">Quand **glVertex \*** est appelé, le vertex obtenu hérite de l’indicateur de bord actuel, de la couleur normale, de la couleur et des coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="14363-123">When **glVertex\*** is called, the resulting vertex inherits the current edge flag, normal, color, and texture coordinates.</span></span> <span data-ttu-id="14363-124">Par conséquent **, \* glEdgeFlag**, **glNormal \***, **\* glColor** et **glTexCoord \*** doivent être appelés avant **glVertex \***, s’ils doivent affecter le vertex résultant.</span><span class="sxs-lookup"><span data-stu-id="14363-124">Therefore, **glEdgeFlag\***, **glNormal\***, **glColor\***, and **glTexCoord\*** must be called before **glVertex\***, if they are to affect the resulting vertex.</span></span>

 

 

 




