---
title: Ajout de BUTTONGROUP
description: Ajout de BUTTONGROUP
ms.assetid: 07a4a347-b3da-4dcb-b3e4-bee0d002b2e2
keywords:
- création d’apparences, élément BUTTONGROUP
- Apparences du lecteur Windows Media, élément BUTTONGROUP
- habillages, élément BUTTONGROUP
- fichiers de définition d’apparence, élément BUTTONGROUP
- Élément BUTTONGROUP
- éléments, BUTTONGROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90659a2e867a65d2751532701b71810a532c8ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309581"
---
# <a name="adding-buttongroup"></a><span data-ttu-id="871ba-109">Ajout de BUTTONGROUP</span><span class="sxs-lookup"><span data-stu-id="871ba-109">Adding BUTTONGROUP</span></span>

<span data-ttu-id="871ba-110">Cet exemple utilise l’élément **BUTTONGROUP** pour le codage dans le fichier de définition d’apparence.</span><span class="sxs-lookup"><span data-stu-id="871ba-110">This example uses the **BUTTONGROUP** element for the coding in the skin definition file.</span></span> <span data-ttu-id="871ba-111">**BUTTONGROUP** crée un moyen simple de traiter des événements de souris sans avoir à calculer des emplacements exacts sur l’écran et utilise la couleur au lieu des coordonnées x et y.</span><span class="sxs-lookup"><span data-stu-id="871ba-111">**BUTTONGROUP** creates an easy way to process mouse events without having to calculate exact locations on the screen and uses color instead of x and y-coordinates.</span></span>

<span data-ttu-id="871ba-112">Tout d’abord, vous devez ajouter les balises **BUTTONGROUP** au fichier de définition d’apparence que vous avez créé.</span><span class="sxs-lookup"><span data-stu-id="871ba-112">First you must add the **BUTTONGROUP** tags to the skin definition file you created.</span></span> <span data-ttu-id="871ba-113">Placez-les après les attributs de balise de **thème** .</span><span class="sxs-lookup"><span data-stu-id="871ba-113">Put them after the **THEME** tag attributes.</span></span>


```C++
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">


        </BUTTONGROUP>

```



<span data-ttu-id="871ba-114">Laissez quelques lignes vides au-dessus de la balise de fermeture **BUTTONGROUP** pour les boutons que vous ajouterez ensuite.</span><span class="sxs-lookup"><span data-stu-id="871ba-114">Leave a few blank lines above the closing **BUTTONGROUP** tag for the buttons you will add next.</span></span>

<span data-ttu-id="871ba-115">Les attributs suivants sont utilisés pour définir **BUTTONGROUP**:</span><span class="sxs-lookup"><span data-stu-id="871ba-115">The following attributes are used to define **BUTTONGROUP**:</span></span>

<span data-ttu-id="871ba-116">**mappingImage**</span><span class="sxs-lookup"><span data-stu-id="871ba-116">**mappingImage**</span></span>

<span data-ttu-id="871ba-117">Il s’agit du nom de fichier du fichier d’illustration de mappage que vous avez créé précédemment, celui avec les cercles rouge et vert.</span><span class="sxs-lookup"><span data-stu-id="871ba-117">This is the file name of the mapping art file you created before, the one with the red and green circles.</span></span> <span data-ttu-id="871ba-118">Cet attribut est obligatoire pour les **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="871ba-118">This attribute is required for any **BUTTONGROUP**.</span></span>

<span data-ttu-id="871ba-119">**hoverImage**</span><span class="sxs-lookup"><span data-stu-id="871ba-119">**hoverImage**</span></span>

<span data-ttu-id="871ba-120">Il s’agit du nom de fichier du fichier image de survol que vous avez créé précédemment, celui avec les deux boutons jaunes qui lisent « lire » et « fermer ».</span><span class="sxs-lookup"><span data-stu-id="871ba-120">This is the file name of the hover art file you created before, the one with the two yellow buttons that read "Play" and "Close".</span></span> <span data-ttu-id="871ba-121">Ce n’est pas obligatoire, mais une image de survol permet de fournir des commentaires à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="871ba-121">This is not required, but a hover image helps to provide feedback to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="871ba-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="871ba-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="871ba-123">**Création du fichier de définition d’apparence**</span><span class="sxs-lookup"><span data-stu-id="871ba-123">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




