---
description: Une application peut utiliser le découpage et les tracés pour créer des effets graphiques spéciaux. L’illustration suivante montre une chaîne de texte dessinée avec une grande police Arial.
ms.assetid: fda0d627-406c-44f9-9061-7aea3e2d7f66
title: Tracés de clip et effets graphiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8156a8670747175502b2385e6c24a340345a54f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528390"
---
# <a name="clip-paths-and-graphic-effects"></a><span data-ttu-id="8680c-104">Tracés de clip et effets graphiques</span><span class="sxs-lookup"><span data-stu-id="8680c-104">Clip Paths and Graphic Effects</span></span>

<span data-ttu-id="8680c-105">Une application peut utiliser le découpage et les tracés pour créer des effets graphiques spéciaux.</span><span class="sxs-lookup"><span data-stu-id="8680c-105">An application can use clipping and paths to create special graphic effects.</span></span> <span data-ttu-id="8680c-106">L’illustration suivante montre une chaîne de texte dessinée avec une grande police Arial.</span><span class="sxs-lookup"><span data-stu-id="8680c-106">The following illustration shows a string of text drawn with a large Arial font.</span></span>

![Illustration montrant du texte noir sur un arrière-plan blanc](images/cspth-02.png)

<span data-ttu-id="8680c-108">L’illustration suivante montre le résultat obtenu en sélectionnant le texte comme tracé de clip et en dessinant des lignes radiales pour un cercle dont le Centre se trouve au-dessus et à gauche de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="8680c-108">The next illustration shows the result of selecting the text as a clip path and drawing radial lines for a circle whose center is located above and left of the string.</span></span>

![Illustration montrant le même texte, mais remplie de lignes au lieu de noir Uni](images/cspth-03.png)

> [!Note]  
> <span data-ttu-id="8680c-110">Avant que GDI (Graphics Device Interface) ajoute un texte créé avec une police bitmap à un tracé, il convertit la police en police vectorielle ou vectorielle.</span><span class="sxs-lookup"><span data-stu-id="8680c-110">Before graphics device interface (GDI) adds text created with a bitmapped font to a path, it converts the font to an outline or vector font.</span></span>

 

<span data-ttu-id="8680c-111">Une application crée un tracé de clip en générant un crochet de chemin d’accès, puis en appelant la fonction [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) .</span><span class="sxs-lookup"><span data-stu-id="8680c-111">An application creates a clip path by generating a path bracket and then calling the [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) function.</span></span> <span data-ttu-id="8680c-112">Une fois qu’un tracé de clip est sélectionné dans un DC, la sortie s’affiche uniquement dans les bordures du tracé.</span><span class="sxs-lookup"><span data-stu-id="8680c-112">After a clip path is selected into a DC, output only appears within the borders of the path.</span></span>

<span data-ttu-id="8680c-113">Outre la création d’effets graphiques spéciaux, les tracés de clip sont également utiles dans les applications qui enregistrent des images en tant que sous-fichiers améliorés.</span><span class="sxs-lookup"><span data-stu-id="8680c-113">In addition to creating special graphics effects, clip paths are also useful in applications that save images as enhanced metafiles.</span></span> <span data-ttu-id="8680c-114">En utilisant un tracé de clip, une application peut garantir l’indépendance des appareils, car les unités utilisées pour spécifier un chemin d’accès sont des unités logiques.</span><span class="sxs-lookup"><span data-stu-id="8680c-114">By using a clip path, an application is able to ensure device independence because the units used to specify a path are logical units.</span></span>

 

 



