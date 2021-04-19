---
title: DISPID standard
description: Un certain nombre de DISPID standard ont été définis pour la spécification de contrôles.
ms.assetid: f938b64f-5d45-40e7-ad02-665ce9c86a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657a7cd12ac92504bb5d63dcd486b6a45da47310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509789"
---
# <a name="standard-dispids"></a><span data-ttu-id="8553d-103">DISPID standard</span><span class="sxs-lookup"><span data-stu-id="8553d-103">Standard DISPIDS</span></span>

<span data-ttu-id="8553d-104">Un certain nombre de DISPID standard ont été définis pour la spécification de contrôles.</span><span class="sxs-lookup"><span data-stu-id="8553d-104">A number of standard dispids have been defined for the controls specification.</span></span>

## <a name="dispid_mousepointer"></a><span data-ttu-id="8553d-105">DISPID, \_ MOUSEPOINTER</span><span class="sxs-lookup"><span data-stu-id="8553d-105">DISPID\_MOUSEPOINTER</span></span>

<span data-ttu-id="8553d-106">Propriété de type entier.</span><span class="sxs-lookup"><span data-stu-id="8553d-106">Property of type integer.</span></span>

``` syntax
#define DISPID_MOUSEPOINTER            -521
```

<span data-ttu-id="8553d-107">La propriété MousePointer identifie les icônes de souris standard.</span><span class="sxs-lookup"><span data-stu-id="8553d-107">The Mousepointer property identifies standard mouse icons.</span></span>



| <span data-ttu-id="8553d-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="8553d-108">Value</span></span>         | <span data-ttu-id="8553d-109">Description</span><span class="sxs-lookup"><span data-stu-id="8553d-109">Description</span></span>                                                                |
|---------------|----------------------------------------------------------------------------|
| <span data-ttu-id="8553d-110">0</span><span class="sxs-lookup"><span data-stu-id="8553d-110">0</span></span><br/>  | <span data-ttu-id="8553d-111">Valeurs Forme déterminée par l’objet.</span><span class="sxs-lookup"><span data-stu-id="8553d-111">(Default) Shape determined by the object.</span></span><br/>                       |
| <span data-ttu-id="8553d-112">1</span><span class="sxs-lookup"><span data-stu-id="8553d-112">1</span></span><br/>  | <span data-ttu-id="8553d-113">Flèche</span><span class="sxs-lookup"><span data-stu-id="8553d-113">Arrow</span></span><br/>                                                           |
| <span data-ttu-id="8553d-114">2</span><span class="sxs-lookup"><span data-stu-id="8553d-114">2</span></span><br/>  | <span data-ttu-id="8553d-115">Croix (pointeur réticule)</span><span class="sxs-lookup"><span data-stu-id="8553d-115">Cross (cross-hair pointer)</span></span><br/>                                      |
| <span data-ttu-id="8553d-116">3</span><span class="sxs-lookup"><span data-stu-id="8553d-116">3</span></span><br/>  | <span data-ttu-id="8553d-117">Poutre</span><span class="sxs-lookup"><span data-stu-id="8553d-117">I Beam</span></span><br/>                                                          |
| <span data-ttu-id="8553d-118">4</span><span class="sxs-lookup"><span data-stu-id="8553d-118">4</span></span><br/>  | <span data-ttu-id="8553d-119">Icône (petit carré dans un carré)</span><span class="sxs-lookup"><span data-stu-id="8553d-119">Icon (small square within a square)</span></span><br/>                             |
| <span data-ttu-id="8553d-120">5</span><span class="sxs-lookup"><span data-stu-id="8553d-120">5</span></span><br/>  | <span data-ttu-id="8553d-121">Taille (flèche à quatre branches pointant vers le Nord, le sud, l’est et l’Ouest)</span><span class="sxs-lookup"><span data-stu-id="8553d-121">Size (four-pointed arrow pointing north, south, east, and west)</span></span><br/> |
| <span data-ttu-id="8553d-122">6</span><span class="sxs-lookup"><span data-stu-id="8553d-122">6</span></span><br/>  | <span data-ttu-id="8553d-123">Taille ne pas de SW (double flèche pointant vers le nord-est et sud-ouest)</span><span class="sxs-lookup"><span data-stu-id="8553d-123">Size NE SW (double arrow pointing northeast and southwest)</span></span><br/>      |
| <span data-ttu-id="8553d-124">7</span><span class="sxs-lookup"><span data-stu-id="8553d-124">7</span></span><br/>  | <span data-ttu-id="8553d-125">Taille N S (double flèche pointant vers le Nord et le sud)</span><span class="sxs-lookup"><span data-stu-id="8553d-125">Size N S (double arrow pointing north and south)</span></span><br/>                |
| <span data-ttu-id="8553d-126">8</span><span class="sxs-lookup"><span data-stu-id="8553d-126">8</span></span><br/>  | <span data-ttu-id="8553d-127">Taille NW, SE</span><span class="sxs-lookup"><span data-stu-id="8553d-127">Size NW, SE</span></span><br/>                                                     |
| <span data-ttu-id="8553d-128">9</span><span class="sxs-lookup"><span data-stu-id="8553d-128">9</span></span><br/>  | <span data-ttu-id="8553d-129">Taille E W (double flèche pointant vers l’est et Ouest)</span><span class="sxs-lookup"><span data-stu-id="8553d-129">Size E W (double arrow pointing east and west)</span></span><br/>                  |
| <span data-ttu-id="8553d-130">10</span><span class="sxs-lookup"><span data-stu-id="8553d-130">10</span></span><br/> | <span data-ttu-id="8553d-131">Flèche haut</span><span class="sxs-lookup"><span data-stu-id="8553d-131">Up Arrow</span></span><br/>                                                        |
| <span data-ttu-id="8553d-132">11</span><span class="sxs-lookup"><span data-stu-id="8553d-132">11</span></span><br/> | <span data-ttu-id="8553d-133">Sablier (attente)</span><span class="sxs-lookup"><span data-stu-id="8553d-133">Hourglass (wait)</span></span><br/>                                                |
| <span data-ttu-id="8553d-134">12</span><span class="sxs-lookup"><span data-stu-id="8553d-134">12</span></span><br/> | <span data-ttu-id="8553d-135">Aucune suppression</span><span class="sxs-lookup"><span data-stu-id="8553d-135">No Drop</span></span><br/>                                                         |
| <span data-ttu-id="8553d-136">13</span><span class="sxs-lookup"><span data-stu-id="8553d-136">13</span></span><br/> | <span data-ttu-id="8553d-137">Flèche et sablier</span><span class="sxs-lookup"><span data-stu-id="8553d-137">Arrow and hourglass</span></span><br/>                                             |
| <span data-ttu-id="8553d-138">14</span><span class="sxs-lookup"><span data-stu-id="8553d-138">14</span></span><br/> | <span data-ttu-id="8553d-139">Flèche et point d’interrogation</span><span class="sxs-lookup"><span data-stu-id="8553d-139">Arrow and question mark</span></span><br/>                                         |
| <span data-ttu-id="8553d-140">15</span><span class="sxs-lookup"><span data-stu-id="8553d-140">15</span></span><br/> | <span data-ttu-id="8553d-141">Ajuster la taille</span><span class="sxs-lookup"><span data-stu-id="8553d-141">Size all</span></span><br/>                                                        |
| <span data-ttu-id="8553d-142">99</span><span class="sxs-lookup"><span data-stu-id="8553d-142">99</span></span><br/> | <span data-ttu-id="8553d-143">Icône personnalisée spécifiée par la propriété MouseIcon</span><span class="sxs-lookup"><span data-stu-id="8553d-143">Custom icon specified by the MouseIcon property</span></span><br/>                 |



 

## <a name="dispid_mouseicon"></a><span data-ttu-id="8553d-144">DISPID \_ MOUSEICON</span><span class="sxs-lookup"><span data-stu-id="8553d-144">DISPID\_MOUSEICON</span></span>

<span data-ttu-id="8553d-145">Propriété de type image.</span><span class="sxs-lookup"><span data-stu-id="8553d-145">Property of type picture.</span></span>

``` syntax
#define DISPID_MOUSEICON               -522
```

## <a name="dispid_picture"></a><span data-ttu-id="8553d-146">\_image DISPID</span><span class="sxs-lookup"><span data-stu-id="8553d-146">DISPID\_PICTURE</span></span>

<span data-ttu-id="8553d-147">Propriété de type image.</span><span class="sxs-lookup"><span data-stu-id="8553d-147">Property of type picture.</span></span>

``` syntax
#define DISPID_PICTURE                 -523
```

## <a name="dispid_valid"></a><span data-ttu-id="8553d-148">DISPID \_ valide</span><span class="sxs-lookup"><span data-stu-id="8553d-148">DISPID\_VALID</span></span>

<span data-ttu-id="8553d-149">Utilisé pour déterminer si le contrôle a ou non des données valides.</span><span class="sxs-lookup"><span data-stu-id="8553d-149">Used to determine if the control has valid data or not.</span></span>

<span data-ttu-id="8553d-150">Propriété de type BOOL.</span><span class="sxs-lookup"><span data-stu-id="8553d-150">Property of type BOOL.</span></span>

``` syntax
#define DISPID_VALID                   -524
```

## <a name="dispid_-ambient_palette"></a><span data-ttu-id="8553d-151">\_palette ambiante \_ DISPID</span><span class="sxs-lookup"><span data-stu-id="8553d-151">DISPID\_ AMBIENT\_PALETTE</span></span>

<span data-ttu-id="8553d-152">Utilisé pour permettre au contrôle d’accéder au HPAL du conteneur.</span><span class="sxs-lookup"><span data-stu-id="8553d-152">Used to allow the control to get the container's HPAL.</span></span> <span data-ttu-id="8553d-153">Si le conteneur fournit une palette ambiante, il s’agit de la seule palette qui peut être réalisée au premier plan.</span><span class="sxs-lookup"><span data-stu-id="8553d-153">If the container supplies an ambient palette then that is the only palette that may be realized into the foreground.</span></span> <span data-ttu-id="8553d-154">Les contrôles qui veulent réaliser leurs propres palettes doivent le faire en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="8553d-154">Controls that want to realize their own palettes must do so in the background.</span></span> <span data-ttu-id="8553d-155">Si aucune palette ambiante n’est fournie par le conteneur, le contrôle actif peut réaliser sa palette au premier plan.</span><span class="sxs-lookup"><span data-stu-id="8553d-155">If there is no ambient palette provided by the container, then the active control can realize its palette in the foreground.</span></span> <span data-ttu-id="8553d-156">La gestion de palette est décrite plus en détail dans comportement de la palette pour les contrôles OLE qui se trouvent dans le SDK ActiveX.</span><span class="sxs-lookup"><span data-stu-id="8553d-156">Palette handling is further discussed in Palette Behavior for OLE Controls which is in the ActiveX SDK.</span></span>

``` syntax
#define DISPID_AMBIENT_PALETTE         -726
```

 

 





