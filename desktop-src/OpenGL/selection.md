---
title: Sélection
description: Selection retourne le contenu actuel de la pile de noms, qui est un tableau de noms avec des valeurs entières.
ms.assetid: 66902d2c-0cd7-49b3-a685-5c0bdba0df1c
keywords:
- mode de sélection OpenGL
- accès à la sélection OpenGL
- enregistrements d’accès OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 851fac28cda979a383d183a12c79656bfebcbb0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310377"
---
# <a name="selection"></a><span data-ttu-id="61844-106">Sélection</span><span class="sxs-lookup"><span data-stu-id="61844-106">Selection</span></span>

<span data-ttu-id="61844-107">Selection retourne le contenu actuel de la pile de noms, qui est un tableau de noms avec des valeurs entières.</span><span class="sxs-lookup"><span data-stu-id="61844-107">Selection returns the current contents of the name stack, which is an array of names with integer values.</span></span> <span data-ttu-id="61844-108">Vous assignez les noms et créez la pile de noms dans le code de modélisation qui spécifie la géométrie des objets que vous souhaitez dessiner.</span><span class="sxs-lookup"><span data-stu-id="61844-108">You assign the names and build the name stack within the modeling code that specifies the geometry of objects you want to draw.</span></span> <span data-ttu-id="61844-109">Ensuite, en mode de sélection, chaque fois qu’une primitive croise le volume du clip, un accès à la sélection se produit.</span><span class="sxs-lookup"><span data-stu-id="61844-109">Then, in selection mode, whenever a primitive intersects the clip volume, a selection hit occurs.</span></span> <span data-ttu-id="61844-110">L’enregistrement d’accès, qui est écrit dans le tableau de sélection que vous avez fourni avec [**glSelectBuffer**](glselectbuffer.md), contient des informations sur le contenu de la pile de noms au moment de l’accès.</span><span class="sxs-lookup"><span data-stu-id="61844-110">The hit record, which is written into the selection array you've supplied with [**glSelectBuffer**](glselectbuffer.md), contains information about the contents of the name stack at the time of the hit.</span></span>

> [!Note]  
> <span data-ttu-id="61844-111">Appelez [**glSelectBuffer**](glselectbuffer.md) avant de mettre OpenGL en mode de sélection avec [**glRenderMode**](glrendermode.md).</span><span class="sxs-lookup"><span data-stu-id="61844-111">Call [**glSelectBuffer**](glselectbuffer.md) before you put OpenGL into selection mode with [**glRenderMode**](glrendermode.md).</span></span> <span data-ttu-id="61844-112">La totalité du contenu de la pile de noms n’est pas retournée tant que vous n’avez pas appelé **glRenderMode** pour utiliser OpenGL en mode de sélection.</span><span class="sxs-lookup"><span data-stu-id="61844-112">The entire contents of the name stack aren't guaranteed to be returned until you call **glRenderMode** to take OpenGL out of selection mode.</span></span>

 

<span data-ttu-id="61844-113">Manipuler la pile de noms avec [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)et [**glPopName**](glpopname.md).</span><span class="sxs-lookup"><span data-stu-id="61844-113">Manipulate the name stack with [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md), and [**glPopName**](glpopname.md).</span></span> <span data-ttu-id="61844-114">Vous pouvez également utiliser [**gluPickMatrix**](glupickmatrix.md) pour la sélection.</span><span class="sxs-lookup"><span data-stu-id="61844-114">You can also use [**gluPickMatrix**](glupickmatrix.md) for selection.</span></span>

 

 




