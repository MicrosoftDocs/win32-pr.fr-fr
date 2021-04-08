---
title: Transformation des coordonnées
description: La bibliothèque d’utilitaires OpenGL (GLU) fournit plusieurs fonctions de transformation de matrice couramment utilisées.
ms.assetid: 9ca32be8-3bc0-4fca-a58c-69a4800c3c55
keywords:
- Utilitaire OpenGL (GLU), fonctions de transformation de matrice
- GLU (utilitaire OpenGL), fonctions de transformation de matrice
- fonctions de transformation de matrice OpenGL
- Utilitaire OpenGL (GLU), transformation des coordonnées
- GLU (utilitaire OpenGL), transformation des coordonnées
- transformation de coordonnées OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a5a58c723dcccfc54ce2f47a01710133ccc30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675490"
---
# <a name="transforming-coordinates"></a><span data-ttu-id="5c4e9-109">Transformation des coordonnées</span><span class="sxs-lookup"><span data-stu-id="5c4e9-109">Transforming Coordinates</span></span>

<span data-ttu-id="5c4e9-110">La bibliothèque d’utilitaires OpenGL (GLU) fournit plusieurs fonctions de transformation de matrice couramment utilisées.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-110">The OpenGL Utility library (GLU) provides several commonly used matrix transformation functions.</span></span> <span data-ttu-id="5c4e9-111">Vous pouvez configurer une région d’affichage orthographique à deux dimensions avec [**gluOrtho2D**](gluortho2d.md), un volume de vue de perspective standard à l’aide de [**gluPerspective**](gluperspective.md)ou un volume de vue centré sur un Eyepoint spécifié avec [**gluLookAt**](glulookat.md).</span><span class="sxs-lookup"><span data-stu-id="5c4e9-111">You can set up a two-dimensional orthographic viewing region with [**gluOrtho2D**](gluortho2d.md), a standard perspective view volume using [**gluPerspective**](gluperspective.md), or a view volume that is centered on a specified eyepoint with [**gluLookAt**](glulookat.md).</span></span> <span data-ttu-id="5c4e9-112">Chacune de ces fonctions crée la matrice souhaitée et l’applique à la matrice actuelle à l’aide de [**glMultMatrix**](glmultmatrix.md).</span><span class="sxs-lookup"><span data-stu-id="5c4e9-112">Each of these functions creates the desired matrix and applies it to the current matrix using [**glMultMatrix**](glmultmatrix.md).</span></span>

<span data-ttu-id="5c4e9-113">La fonction [**gluPickMatrix**](glupickmatrix.md) simplifie la sélection d’une matrice de prélèvement en créant une matrice qui restreint le dessin à une petite zone de la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-113">The [**gluPickMatrix**](glupickmatrix.md) function simplifies selection of a picking matrix by creating a matrix that restricts drawing to a small region of the viewport.</span></span> <span data-ttu-id="5c4e9-114">Si vous rerendez la scène en mode de sélection après l’application de cette matrice, tous les objets qui seraient dessinés près du curseur seront sélectionnés et les informations les concernant seront stockées dans la mémoire tampon de sélection.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-114">If you re-render the scene in selection mode after this matrix has been applied, all objects that would be drawn near the cursor will be selected, and information about them will be stored in the selection buffer.</span></span> <span data-ttu-id="5c4e9-115">Pour plus d’informations sur le mode de sélection, consultez « sélection de la sélection et des commentaires » [exécution de la sélection et des commentaires](performing-selection-and-feedback.md).</span><span class="sxs-lookup"><span data-stu-id="5c4e9-115">For more information about selection mode, see "Performing Selection and Feedback" [Performing Selection and Feedback](performing-selection-and-feedback.md).</span></span>

<span data-ttu-id="5c4e9-116">Pour déterminer l’emplacement dans la fenêtre où un objet est dessiné, utilisez [**gluProject**](gluproject.md), qui convertit les coordonnées de l’objet spécifié *objX*, *objy* et *objz* en coordonnées de fenêtre à l’aide de *modelMatrix*, *projMatrix* et *Viewport*.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-116">To determine where in the window an object is being drawn, use [**gluProject**](gluproject.md), which converts the specified object coordinates *objx*, *objy*, and *objz* into window coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="5c4e9-117">Le résultat est stocké dans *Winx*, *winy* et *WINZ*.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-117">The result is stored in *winx*, *winy*, and *winz*.</span></span> <span data-ttu-id="5c4e9-118">Si la fonction est réussie, la valeur de retour est GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-118">If the function succeeds, the return value is GL\_TRUE.</span></span> <span data-ttu-id="5c4e9-119">Si la fonction échoue, la valeur de retour est GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-119">If the function fails, the return value is GL\_FALSE.</span></span>

<span data-ttu-id="5c4e9-120">La fonction [**gluUnProject**](gluunproject.md) effectue la conversion inverse : elle transforme les coordonnées de fenêtre spécifiées *Winx*, *winy* et *WINZ* en coordonnées d’objet à l’aide de *modelMatrix*, *projMatrix* et *Viewport*.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-120">The [**gluUnProject**](gluunproject.md) function performs the inverse conversion: it transforms the specified window coordinates *winx*, *winy*, and *winz* into object coordinates using *modelMatrix*, *projMatrix*, and *viewport*.</span></span> <span data-ttu-id="5c4e9-121">Le résultat est stocké dans *objX*, *objy* et *objz*.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-121">The result is stored in *objx*, *objy*, and *objz*.</span></span> <span data-ttu-id="5c4e9-122">Si la fonction est réussie, la valeur de retour est GL \_ true.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-122">If the function succeeds, the return value is GL\_TRUE.</span></span> <span data-ttu-id="5c4e9-123">Si la fonction échoue, la valeur de retour est GL \_ false.</span><span class="sxs-lookup"><span data-stu-id="5c4e9-123">If the function fails, the return value is GL\_FALSE.</span></span>

 

 




