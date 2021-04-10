---
description: La bibliothèque de l’utilitaire D3DX fournit l’interface ID3DXMATRIXStack.
ms.assetid: e3cfb29e-4ef6-4b48-ad6b-f0371f526507
title: Piles de matrices (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d535307fb99d8743b910f2f3f8c6d55e197748e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846421"
---
# <a name="matrix-stacks-direct3d-9"></a><span data-ttu-id="9de93-103">Piles de matrices (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9de93-103">Matrix Stacks (Direct3D 9)</span></span>

<span data-ttu-id="9de93-104">La bibliothèque de l’utilitaire D3DX fournit l’interface [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="9de93-104">The D3DX utility library provides the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface.</span></span> <span data-ttu-id="9de93-105">Il fournit un mécanisme pour permettre aux matrices d’être envoyées et dépilées d’une pile de matrices.</span><span class="sxs-lookup"><span data-stu-id="9de93-105">It supplies a mechanism to enable matrices to be pushed onto and popped off of a matrix stack.</span></span> <span data-ttu-id="9de93-106">L’implémentation d’une pile de matrices est un moyen efficace de suivre les matrices tout en parcourant une hiérarchie de transformation.</span><span class="sxs-lookup"><span data-stu-id="9de93-106">Implementing a matrix stack is an efficient way to track matrices while traversing a transform hierarchy.</span></span>

<span data-ttu-id="9de93-107">La bibliothèque de l’utilitaire D3DX utilise une pile de matrices pour stocker les transformations sous forme de matrices.</span><span class="sxs-lookup"><span data-stu-id="9de93-107">The D3DX utility library uses a matrix stack to store transformations as matrices.</span></span> <span data-ttu-id="9de93-108">Les différentes méthodes de l’interface [**ID3DXMATRIXStack**](id3dxmatrixstack.md) traitent de la matrice actuelle ou de la matrice située en haut de la pile.</span><span class="sxs-lookup"><span data-stu-id="9de93-108">The various methods of the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) interface deal with the current matrix, or the matrix located on top of the stack.</span></span> <span data-ttu-id="9de93-109">Vous pouvez effacer la matrice actuelle avec la méthode [**ID3DXMATRIXStack :: LoadIdentity**](id3dxmatrixstack--loadidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="9de93-109">You can clear the current matrix with the [**ID3DXMATRIXStack::LoadIdentity**](id3dxmatrixstack--loadidentity.md) method.</span></span> <span data-ttu-id="9de93-110">Pour spécifier explicitement une certaine matrice à charger comme matrice de transformation actuelle, utilisez la méthode [**ID3DXMATRIXStack :: LoadMatrix**](id3dxmatrixstack--loadmatrix.md) .</span><span class="sxs-lookup"><span data-stu-id="9de93-110">To explicitly specify a certain matrix to load as the current transformation matrix, use the [**ID3DXMATRIXStack::LoadMatrix**](id3dxmatrixstack--loadmatrix.md) method.</span></span> <span data-ttu-id="9de93-111">Ensuite, vous pouvez appeler la méthode [**ID3DXMATRIXStack :: MultMatrix**](id3dxmatrixstack--multmatrix.md) ou la méthode [**ID3DXMATRIXStack :: MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) pour multiplier la matrice actuelle par la matrice spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9de93-111">Then you can call either the [**ID3DXMATRIXStack::MultMatrix**](id3dxmatrixstack--multmatrix.md) method or the [**ID3DXMATRIXStack::MultMatrixLocal**](id3dxmatrixstack--multmatrixlocal.md) method to multiply the current matrix by the specified matrix.</span></span>

<span data-ttu-id="9de93-112">La méthode [**ID3DXMATRIXStack ::P op**](id3dxmatrixstack--pop.md) vous permet de revenir à la matrice de transformation précédente et la méthode [**ID3DXMATRIXStack ::P par émission**](id3dxmatrixstack--push.md) ajoute une matrice de transformation à la pile.</span><span class="sxs-lookup"><span data-stu-id="9de93-112">The [**ID3DXMATRIXStack::Pop**](id3dxmatrixstack--pop.md) method enables you to return to the previous transformation matrix and the [**ID3DXMATRIXStack::Push**](id3dxmatrixstack--push.md) method adds a transformation matrix to the stack.</span></span>

<span data-ttu-id="9de93-113">Les matrices individuelles sur la pile de matrices sont représentées sous forme de matrices homogènes 4x4, définies par la structure [**D3DXMATRIX**](d3dxmatrix.md) de la bibliothèque de l’utilitaire D3DX.</span><span class="sxs-lookup"><span data-stu-id="9de93-113">The individual matrices on the matrix stack are represented as 4x4 homogeneous matrices, defined by the D3DX utility library [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

<span data-ttu-id="9de93-114">La bibliothèque de l’utilitaire D3DX fournit une pile de matrice via un objet COM (Component Object Model).</span><span class="sxs-lookup"><span data-stu-id="9de93-114">The D3DX utility library provides a matrix stack through a component object model (COM) object.</span></span>

## <a name="implementing-a-scene-hierarchy"></a><span data-ttu-id="9de93-115">Implémentation d’une hiérarchie de scène</span><span class="sxs-lookup"><span data-stu-id="9de93-115">Implementing a Scene Hierarchy</span></span>

<span data-ttu-id="9de93-116">Une pile de matrices simplifie la construction de modèles hiérarchiques, dans lesquels des objets compliqués sont construits à partir d’une série d’objets plus simples.</span><span class="sxs-lookup"><span data-stu-id="9de93-116">A matrix stack simplifies the construction of hierarchical models, in which complicated objects are constructed from a series of simpler objects.</span></span>

<span data-ttu-id="9de93-117">Une scène, ou transformation, est généralement représentée par une structure de données d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="9de93-117">A scene, or transform, hierarchy is usually represented by a tree data structure.</span></span> <span data-ttu-id="9de93-118">Chaque nœud de la structure de données de l’arborescence contient une matrice.</span><span class="sxs-lookup"><span data-stu-id="9de93-118">Each node in the tree data structure contains a matrix.</span></span> <span data-ttu-id="9de93-119">Une matrice particulière représente la modification des systèmes de coordonnées du parent du nœud au nœud.</span><span class="sxs-lookup"><span data-stu-id="9de93-119">A particular matrix represents the change in coordinate systems from the node's parent to the node.</span></span> <span data-ttu-id="9de93-120">Par exemple, si vous modélisez un ARM humain, vous pouvez implémenter la hiérarchie présentée dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="9de93-120">For example, if you are modeling a human arm, you might implement the hierarchy that is shown in the following diagram.</span></span>

![diagramme de la hiérarchie d’un bras humain](images/stack1.png)

<span data-ttu-id="9de93-122">Dans cette hiérarchie, la matrice du corps place le corps dans le monde.</span><span class="sxs-lookup"><span data-stu-id="9de93-122">In this hierarchy, the Body matrix places the body in the world.</span></span> <span data-ttu-id="9de93-123">La matrice UpperArm contient la rotation de l’épaule, la matrice LowerArm contient la rotation du coude et la matrice de la main contient la rotation du poignet.</span><span class="sxs-lookup"><span data-stu-id="9de93-123">The UpperArm matrix contains the rotation of the shoulder, the LowerArm matrix contains the rotation of the elbow, and the Hand matrix contains the rotation of the wrist.</span></span> <span data-ttu-id="9de93-124">Pour déterminer où se trouve la main par rapport au monde, vous multipliez toutes les matrices du corps à la main.</span><span class="sxs-lookup"><span data-stu-id="9de93-124">To determine where the hand is relative to the world, you multiply all the matrices from Body down through Hand together.</span></span>

<span data-ttu-id="9de93-125">La hiérarchie précédente est trop simple, car chaque nœud n’a qu’un seul enfant.</span><span class="sxs-lookup"><span data-stu-id="9de93-125">The previous hierarchy is overly simplistic, because each node has only one child.</span></span> <span data-ttu-id="9de93-126">Si vous commencez à modéliser la main plus en détail, vous ajouterez probablement des doigts et un curseur de défilement.</span><span class="sxs-lookup"><span data-stu-id="9de93-126">If you begin to model the hand in more detail, you will probably add fingers and a thumb.</span></span> <span data-ttu-id="9de93-127">Chaque chiffre peut être ajouté à la hiérarchie en tant qu’enfant de main, comme indiqué dans le diagramme suivant.</span><span class="sxs-lookup"><span data-stu-id="9de93-127">Each digit can be added to the hierarchy as children of Hand, as shown in the following diagram.</span></span>

![diagramme de la hiérarchie d’une main humaine](images/stack2.png)

<span data-ttu-id="9de93-129">Si vous parcourez le graphique complet du bras dans l’ordre à profondeur prioritaire, en passant d’un seul chemin d’accès à l’autre, avant de passer au chemin suivant : pour dessiner la scène, vous effectuez une séquence de rendu segmenté.</span><span class="sxs-lookup"><span data-stu-id="9de93-129">If you traverse the complete graph of the arm in depth-first order - traversing as far down one path as possible before moving on to the next path - to draw the scene, you perform a sequence of segmented rendering.</span></span> <span data-ttu-id="9de93-130">Par exemple, pour afficher la main et les doigts, vous devez implémenter le modèle suivant.</span><span class="sxs-lookup"><span data-stu-id="9de93-130">For example, to render the hand and fingers, you implement the following pattern.</span></span>

1.  <span data-ttu-id="9de93-131">Poussez la matrice main sur la pile de matrice.</span><span class="sxs-lookup"><span data-stu-id="9de93-131">Push the Hand matrix onto the matrix stack.</span></span>
2.  <span data-ttu-id="9de93-132">Dessinez la main.</span><span class="sxs-lookup"><span data-stu-id="9de93-132">Draw the hand.</span></span>
3.  <span data-ttu-id="9de93-133">Exécute un push de la matrice Thumb sur la pile de matrice.</span><span class="sxs-lookup"><span data-stu-id="9de93-133">Push the Thumb matrix onto the matrix stack.</span></span>
4.  <span data-ttu-id="9de93-134">Dessinez le curseur.</span><span class="sxs-lookup"><span data-stu-id="9de93-134">Draw the thumb.</span></span>
5.  <span data-ttu-id="9de93-135">Affiche la matrice de curseur de défilement en dehors de la pile.</span><span class="sxs-lookup"><span data-stu-id="9de93-135">Pop the Thumb matrix off the stack.</span></span>
6.  <span data-ttu-id="9de93-136">Poussez la matrice Finger 1 sur la pile de matrice.</span><span class="sxs-lookup"><span data-stu-id="9de93-136">Push the Finger 1 matrix onto the matrix stack.</span></span>
7.  <span data-ttu-id="9de93-137">Dessinez le premier doigt.</span><span class="sxs-lookup"><span data-stu-id="9de93-137">Draw the first finger.</span></span>
8.  <span data-ttu-id="9de93-138">Dépilez la matrice Finger 1 de la pile.</span><span class="sxs-lookup"><span data-stu-id="9de93-138">Pop the Finger 1 matrix off the stack.</span></span>
9.  <span data-ttu-id="9de93-139">Poussez la matrice Finger 2 sur la pile de matrice.</span><span class="sxs-lookup"><span data-stu-id="9de93-139">Push the Finger 2 matrix onto the matrix stack.</span></span> <span data-ttu-id="9de93-140">Vous poursuivez cette procédure jusqu’à ce que tous les doigts et le curseur soient rendus.</span><span class="sxs-lookup"><span data-stu-id="9de93-140">You continue in this manner until all the fingers and thumb are rendered.</span></span>

<span data-ttu-id="9de93-141">Une fois que vous avez terminé le rendu des doigts, vous pouvez dépiler la matrice de la main.</span><span class="sxs-lookup"><span data-stu-id="9de93-141">After you have completed rendering the fingers, you would pop the Hand matrix off the stack.</span></span>

<span data-ttu-id="9de93-142">Vous pouvez suivre ce processus de base dans le code avec les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="9de93-142">You can follow this basic process in code with the following examples.</span></span> <span data-ttu-id="9de93-143">Lorsque vous rencontrez un nœud lors de la recherche à profondeur prioritaire de la structure des données de l’arborescence, poussez la matrice en haut de la pile de matrice.</span><span class="sxs-lookup"><span data-stu-id="9de93-143">When you encounter a node during the depth-first search of the tree data structure, push the matrix onto the top of the matrix stack.</span></span>


```
MatrixStack->Push();

MatrixStack->MultMatrix(pNode->matrix);
```



<span data-ttu-id="9de93-144">Lorsque vous avez terminé avec un nœud, affichez la matrice en haut de la pile de matrice.</span><span class="sxs-lookup"><span data-stu-id="9de93-144">When you are finished with a node, pop the matrix off the top of the matrix stack.</span></span>


```
MatrixStack->Pop();
```



<span data-ttu-id="9de93-145">De cette façon, la matrice située en haut de la pile représente toujours la transformation universelle du nœud actuel.</span><span class="sxs-lookup"><span data-stu-id="9de93-145">In this way, the matrix on the top of the stack always represents the world-transform of the current node.</span></span> <span data-ttu-id="9de93-146">Par conséquent, avant de dessiner chaque nœud, vous devez définir la matrice Direct3D.</span><span class="sxs-lookup"><span data-stu-id="9de93-146">Therefore, before drawing each node, you should set the Direct3D matrix.</span></span>


```
pD3DDevice->SetTransform(D3DTS_WORLDMATRIX(0), *MatrixStack->GetTop());
```



<span data-ttu-id="9de93-147">Pour plus d’informations sur les méthodes spécifiques que vous pouvez effectuer sur une pile de matrices D3DX, consultez la rubrique de référence [**ID3DXMATRIXStack**](id3dxmatrixstack.md) .</span><span class="sxs-lookup"><span data-stu-id="9de93-147">For more information about the specific methods that you can perform on a D3DX matrix stack, see the [**ID3DXMATRIXStack**](id3dxmatrixstack.md) reference topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9de93-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9de93-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9de93-149">Pipeline de vertex</span><span class="sxs-lookup"><span data-stu-id="9de93-149">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 



