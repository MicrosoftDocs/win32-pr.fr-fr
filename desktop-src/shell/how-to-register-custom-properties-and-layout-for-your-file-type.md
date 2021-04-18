---
description: Une fois que vous avez compris le mode de résultats de la recherche, le mode de navigation et les modèles de disposition, vous pouvez inscrire une liste de propriétés personnalisées pour votre type de fichier. Pour inscrire une liste de propriétés personnalisées et un modèle de disposition pour votre type de fichier, procédez comme suit.
ms.assetid: 29B863B3-E5FD-4E0A-B76B-4AFE5A6A76E3
title: Comment inscrire des propriétés personnalisées et une disposition pour votre type de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da55d0a90d4dd0f3ca109a3ca9f628a3c0912520
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991553"
---
# <a name="how-to-register-custom-properties-and-layout-for-your-file-type"></a><span data-ttu-id="2310b-103">Comment inscrire des propriétés personnalisées et une disposition pour votre type de fichier</span><span class="sxs-lookup"><span data-stu-id="2310b-103">How to Register Custom Properties and Layout for Your File Type</span></span>

<span data-ttu-id="2310b-104">Une fois que vous avez compris le mode de résultats de la recherche, le mode de navigation et les modèles de disposition, vous pouvez inscrire une liste de propriétés personnalisées pour votre type de fichier.</span><span class="sxs-lookup"><span data-stu-id="2310b-104">After you understand the Search Result mode, the Browse mode, and the layout patterns, you can register a custom property list for your file type.</span></span>

<span data-ttu-id="2310b-105">Pour inscrire une liste de propriétés personnalisées et un modèle de disposition pour votre type de fichier, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="2310b-105">To register a custom property list and layout pattern for your file type, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="2310b-106">Instructions</span><span class="sxs-lookup"><span data-stu-id="2310b-106">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="2310b-107">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="2310b-107">Step 1:</span></span>

<span data-ttu-id="2310b-108">Choisissez parmi les quatre modèles de disposition : alpha, bêta, gamma ou Delta.</span><span class="sxs-lookup"><span data-stu-id="2310b-108">Choose from the four layout patterns: Alpha, Beta, Gamma, or Delta.</span></span>

### <a name="step-2"></a><span data-ttu-id="2310b-109">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="2310b-109">Step 2:</span></span>

<span data-ttu-id="2310b-110">Tenez compte des règles de mise en forme suivantes, qui s’appliquent également aux quatre modèles de disposition :</span><span class="sxs-lookup"><span data-stu-id="2310b-110">Consider the following formatting rules, which apply equally to all four layout patterns:</span></span>

-   <span data-ttu-id="2310b-111">La propriété 1 est toujours affichée dans une plus grande taille de police.</span><span class="sxs-lookup"><span data-stu-id="2310b-111">Property 1 is always displayed in a larger font size.</span></span> <span data-ttu-id="2310b-112">Taille de police importante généralement utilisée pour le nom de l’élément, mais peut également être utilisée pour la propriété d’ancrage ou d’autre élément.</span><span class="sxs-lookup"><span data-stu-id="2310b-112">The large font size usually used for the item name, but can also be used for the anchor or other item property.</span></span>
-   <span data-ttu-id="2310b-113">La propriété 4 est destinée aux extraits des modèles de disposition alpha, bêta et gamma.</span><span class="sxs-lookup"><span data-stu-id="2310b-113">Property 4 is intended for excerpts in the Alpha, Beta, and Gamma layout patterns.</span></span> <span data-ttu-id="2310b-114">Cette propriété est allouée en plus de l’espace dans ces modèles et s’affiche dans une couleur de police grise, par opposition aux autres propriétés, afin de les aider à se mettre en évidence.</span><span class="sxs-lookup"><span data-stu-id="2310b-114">This property is allotted more space in those patterns and is displayed in a gray font color, as opposed to black like the other properties, to help it stand out.</span></span>
-   <span data-ttu-id="2310b-115">Les mesures en pixels ci-dessous se trouvent en pixels relatifs, et la taille comprend l’icône/la miniature à gauche des propriétés et l’espace entre l’icône/la miniature et le rectangle de sélection.</span><span class="sxs-lookup"><span data-stu-id="2310b-115">The pixel measurements below are in relative pixels, and the size includes the icon/thumbnail to the left of the properties and the space between the icon/thumbnail and the selection rectangle.</span></span>
-   <span data-ttu-id="2310b-116">La plupart des propriétés ont une taille d’affichage minimale.</span><span class="sxs-lookup"><span data-stu-id="2310b-116">Most properties have a minimum display size.</span></span> <span data-ttu-id="2310b-117">Par conséquent, ils ne s’affichent pas s’il n’y a pas suffisamment d’espace pour une taille de vue particulière.</span><span class="sxs-lookup"><span data-stu-id="2310b-117">Therefore, they will not appear if there is not enough space for them at a particular view size.</span></span> <span data-ttu-id="2310b-118">La taille minimale est généralement de 100 pixels de largeur.</span><span class="sxs-lookup"><span data-stu-id="2310b-118">The minimum size is usually 100 pixels wide.</span></span>
-   <span data-ttu-id="2310b-119">Chaque modèle de disposition définit le nombre de lignes et le nombre de propriétés dans chaque ligne.</span><span class="sxs-lookup"><span data-stu-id="2310b-119">Each layout pattern defines the number of rows and the number of properties in each row.</span></span>

### <a name="step-3"></a><span data-ttu-id="2310b-120">Étape 3 :</span><span class="sxs-lookup"><span data-stu-id="2310b-120">Step 3:</span></span>

<span data-ttu-id="2310b-121">Choisissez les propriétés que vous souhaitez afficher dans la mise en page et la propriété que vous souhaitez afficher dans chaque emplacement.</span><span class="sxs-lookup"><span data-stu-id="2310b-121">Decide which properties you want to display in the layout, and which property you want to display in each location.</span></span> <span data-ttu-id="2310b-122">Lorsque vous choisissez la propriété à afficher à chaque position dans la disposition, tenez compte de la longueur typique de la propriété, de son importance pour l’utilisateur et de la nécessité de la supprimer lorsque la taille de la fenêtre est trop petite pour contenir toutes les propriétés.</span><span class="sxs-lookup"><span data-stu-id="2310b-122">When deciding which property to display in each position in the layout, consider the typical length of the property, its importance to the user, and whether it should be dropped when the window size is too small to contain all properties.</span></span>

### <a name="step-4"></a><span data-ttu-id="2310b-123">Étape 4 :</span><span class="sxs-lookup"><span data-stu-id="2310b-123">Step 4:</span></span>

<span data-ttu-id="2310b-124">Inscrivez un modèle de disposition et une liste de propriétés pour votre type de fichier ou type d’élément en ajoutant les clés suivantes sous la clé de Registre ProgID pour le type de fichier ou l’élément (dans cet exemple, pour le type de fichier. xyz).</span><span class="sxs-lookup"><span data-stu-id="2310b-124">Register a layout pattern and a property list for your file type or item type by adding the following keys under the ProgID registry key for the file type or item (in this example, for the .xyz file type).</span></span>

```
HKEY_CLASSES_ROOT\*
   Contoso.xyzfile
      (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
      (ContentViewModeLayoutPatternForSearch) = <PropertyList>
```

### <a name="step-5"></a><span data-ttu-id="2310b-125">Étape 5 :</span><span class="sxs-lookup"><span data-stu-id="2310b-125">Step 5:</span></span>

<span data-ttu-id="2310b-126">Respectez les instructions de mise en forme suivantes pour l’inscription des propriétés :</span><span class="sxs-lookup"><span data-stu-id="2310b-126">Observe the following formatting guidelines for registering properties:</span></span>

-   <span data-ttu-id="2310b-127">Chaque inscription commence par `prop:`</span><span class="sxs-lookup"><span data-stu-id="2310b-127">Each registration starts with `prop:`</span></span>
-   <span data-ttu-id="2310b-128">Chaque propriété requiert le nom complet de la propriété.</span><span class="sxs-lookup"><span data-stu-id="2310b-128">Each property requires the full property name.</span></span>
-   <span data-ttu-id="2310b-129">Les propriétés sont séparées par un point-virgule sans espace.</span><span class="sxs-lookup"><span data-stu-id="2310b-129">Properties are separated by a semicolon with no space.</span></span>
-   <span data-ttu-id="2310b-130">Les propriétés sont affichées dans l’ordre défini par le modèle de disposition sélectionné.</span><span class="sxs-lookup"><span data-stu-id="2310b-130">Properties are displayed in the order defined by the selected layout pattern.</span></span>
-   <span data-ttu-id="2310b-131">`~` indique que l’étiquette de la propriété ne doit pas être affichée.</span><span class="sxs-lookup"><span data-stu-id="2310b-131">`~` indicates that the property label should not be displayed.</span></span>
-   <span data-ttu-id="2310b-132">`~System.LayoutPattern.PlaceHolder` doit être utilisé si vous souhaitez laisser vide une propriété qui est spécifiée dans le modèle de disposition.</span><span class="sxs-lookup"><span data-stu-id="2310b-132">`~System.LayoutPattern.PlaceHolder` should be used if you want to leave blank a property that is specified in the layout pattern.</span></span>

<span data-ttu-id="2310b-133">L’exemple de clé de Registre suivant illustre ces instructions de mise en forme.</span><span class="sxs-lookup"><span data-stu-id="2310b-133">The following sample registry key illustrates these formatting guidelines.</span></span>

```
HKEY_CLASSES_ROOT\
   Kind.Document
      (ContentViewModeForBrowse) = <PropertyList>
```

<span data-ttu-id="2310b-134">Les valeurs possibles pour (ContentViewModeForBrowse) sont les suivantes : `prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified;~System.Size`</span><span class="sxs-lookup"><span data-stu-id="2310b-134">Possible values for (ContentViewModeForBrowse) include the following: `prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified;~System.Size`</span></span>

 

 



