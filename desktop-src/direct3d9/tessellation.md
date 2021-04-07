---
description: Pavage (Direct3D 9)
ms.assetid: ae39b0e1-d2ae-449e-89db-0a2b24171531
title: Pavage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82378caac1218158ffc1834c9a9b56fb8cbd250e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746933"
---
# <a name="tessellation-direct3d-9"></a><span data-ttu-id="31da5-103">Pavage (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="31da5-103">Tessellation (Direct3D 9)</span></span>

## <a name="tessellator-unit"></a><span data-ttu-id="31da5-104">Unité du paveur</span><span class="sxs-lookup"><span data-stu-id="31da5-104">Tessellator Unit</span></span>

<span data-ttu-id="31da5-105">L’unité du paveur a été améliorée.</span><span class="sxs-lookup"><span data-stu-id="31da5-105">The tessellator unit has been enhanced.</span></span> <span data-ttu-id="31da5-106">Vous pouvez maintenant l’utiliser pour :</span><span class="sxs-lookup"><span data-stu-id="31da5-106">You can now use it to:</span></span>

-   <span data-ttu-id="31da5-107">Effectue un pavage adaptatif de toutes les primitives d’ordre supérieur.</span><span class="sxs-lookup"><span data-stu-id="31da5-107">Perform adaptive tessellation of all higher-order primitives.</span></span>
-   <span data-ttu-id="31da5-108">Recherchez des valeurs de remplacement par vertex d’un mappage de déplacement et passez-les à un nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="31da5-108">Look up per-vertex displacement values from a displacement map and pass them on to a vertex shader.</span></span>
-   <span data-ttu-id="31da5-109">Prendre en charge le pavage rectangle-patch.</span><span class="sxs-lookup"><span data-stu-id="31da5-109">Support rectangle-patch tessellation.</span></span> <span data-ttu-id="31da5-110">Cela est spécifié par le biais d’une déclaration de vertex utilisant D3DDECLMETHOD \_ partial ou D3DDECLMETHOD \_ PARTIALV.</span><span class="sxs-lookup"><span data-stu-id="31da5-110">This is specified through a vertex declaration using D3DDECLMETHOD\_PARTIALU or D3DDECLMETHOD\_PARTIALV.</span></span> <span data-ttu-id="31da5-111">Si une déclaration de vertex contenant ces méthodes est utilisée pour dessiner un correctif triangulaire, [**IDirect3DDevice9 ::D rawtripatch**](/windows/desktop/api) échoue.</span><span class="sxs-lookup"><span data-stu-id="31da5-111">If a vertex declaration containing these methods is used to draw a triangle patch, [**IDirect3DDevice9::DrawTriPatch**](/windows/desktop/api) will fail.</span></span> <span data-ttu-id="31da5-112">Pour plus d’informations sur les déclarations de vertex, consultez [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="31da5-112">For more information about vertex declarations, see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

<span data-ttu-id="31da5-113">Dans DirectX 8. x, ce qui était appelé ORDER était vraiment le degré.</span><span class="sxs-lookup"><span data-stu-id="31da5-113">In DirectX 8.x, what was called ORDER was really the degree.</span></span> <span data-ttu-id="31da5-114">Dans Direct3D 9, le degré est maintenant spécifié par [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="31da5-114">In Direct3D 9, the degree is now specified by [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>


```
 // This used to be D3DORDERTYPE and D3DORDER* 
 typedef enum _D3DDEGREETYPE 
 { 
 D3DDEGREE_LINEAR = 1, 
 D3DDEGREE_QUADRATIC = 2, 
 D3DDEGREE_CUBIC = 3, 
 D3DDEGREE_QUINTIC = 5, 
 D3DDEGREE_FORCE_DWORD = 0x7fffffff, 
 } D3DDEGREETYPE; 
```



<span data-ttu-id="31da5-115">La modification du type de degré a affecté deux autres structures.</span><span class="sxs-lookup"><span data-stu-id="31da5-115">The change in degree type affected two other structures.</span></span>


```
typedef struct _D3DRECTPATCH_INFO 
 { 
 UINT StartVertexOffsetWidth; 
 UINT StartVertexOffsetHeight; 
 UINT Width; 
 UINT Height; 
 UINT Stride; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DRECTPATCH_INFO; 
```




```
 typedef struct _D3DTRIPATCH_INFO 
 { 
 UINT StartVertexOffset; 
 UINT NumVertices; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DTRIPATCH_INFO; 
```



<span data-ttu-id="31da5-116">Les pilotes doivent corriger les erreurs de compilation qui résultent de cette modification quand elles se compilent avec les nouveaux en-têtes.</span><span class="sxs-lookup"><span data-stu-id="31da5-116">Drivers need to fix compilation errors that will result from this change when they compile with the new headers.</span></span> <span data-ttu-id="31da5-117">Aucune fonctionnalité ne doit être modifiée.</span><span class="sxs-lookup"><span data-stu-id="31da5-117">No functionality has to be changed.</span></span>

## <a name="adaptive-tessellation"></a><span data-ttu-id="31da5-118">Pavage adaptative</span><span class="sxs-lookup"><span data-stu-id="31da5-118">Adaptive Tessellation</span></span>

<span data-ttu-id="31da5-119">Le pavage adaptatif peut être appliqué à des primitives d’ordre élevé, y compris N-patchs, des carreaux de rectangles et des carreaux de triangle.</span><span class="sxs-lookup"><span data-stu-id="31da5-119">Adaptive tessellation can be applied to high-order primitives including N-patches, rectangle patches, and triangle patches.</span></span> <span data-ttu-id="31da5-120">Cette fonctionnalité est activée par le \_ ENABLEADAPTIVETESSELLATION D3DRS et Adaptive tessellates un correctif, en fonction de la valeur de profondeur du vertex de contrôle dans l’espace œil.</span><span class="sxs-lookup"><span data-stu-id="31da5-120">This feature is enabled by the D3DRS\_ENABLEADAPTIVETESSELLATION and adaptively tessellates a patch, based on the depth value of the control vertex in eye space.</span></span>

<span data-ttu-id="31da5-121">Les coordonnées z (ZI) des vertex de contrôle (VI), qui sont transformées en espace œil (Zieye) en effectuant un produit scalaire avec un vecteur 4, sont utilisées comme valeurs de profondeur.</span><span class="sxs-lookup"><span data-stu-id="31da5-121">The z-coordinates (Zi) of control vertices (Vi), which are transformed into eye space (Zieye) by performing a dot product with a 4-vector, are used as the depth values.</span></span> <span data-ttu-id="31da5-122">Le vecteur 4D (MDM) est spécifié par l’application à l’aide de quatre États de rendu (D3DRS \_ ADAPTIVETESS \_ X, D3DRS \_ ADAPTIVETESS \_ Y, D3DRS \_ ADAPTIVETESS \_ Z et D3DRS \_ ADAPTIVETESS \_ W).</span><span class="sxs-lookup"><span data-stu-id="31da5-122">The 4D vector (Mdm) is specified by the application using four render states (D3DRS\_ADAPTIVETESS\_X, D3DRS\_ADAPTIVETESS\_Y, D3DRS\_ADAPTIVETESS\_Z, and D3DRS\_ADAPTIVETESS\_W).</span></span> <span data-ttu-id="31da5-123">Ce 4-Vector peut être la troisième colonne des matrices de monde et de vue concaténées.</span><span class="sxs-lookup"><span data-stu-id="31da5-123">This 4-vector could be the third column of the concatenated world and view matrices.</span></span> <span data-ttu-id="31da5-124">Elle peut également être utilisée pour appliquer une mise à l’échelle à Zieye.</span><span class="sxs-lookup"><span data-stu-id="31da5-124">It also could be used to apply a scale to Zieye.</span></span>

<span data-ttu-id="31da5-125">La fonction de calcul de l’TI de niveau de pavage à partir de Zieye est supposée être (MaxTessellationLevel/Zieye), ce qui signifie que le MaxTessellationLevel est le niveau de pavage à Z = 1 dans l’espace œil.</span><span class="sxs-lookup"><span data-stu-id="31da5-125">The function to compute a tessellation level Ti from Zieye is assumed to be (MaxTessellationLevel/Zieye), which means that the MaxTessellationLevel is the tessellation level at Z = 1 in eye space.</span></span> <span data-ttu-id="31da5-126">Le MaxTessellationLevel est égal à une valeur définie par [**IDirect3DDevice9 :: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) pour N-patchs et, pour RT-patchs, il est égal à pNumSegs.</span><span class="sxs-lookup"><span data-stu-id="31da5-126">The MaxTessellationLevel is equal to a value set by [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) for N-patches and, for RT-patches, it is equal to pNumSegs.</span></span> <span data-ttu-id="31da5-127">Le niveau de pavage est ensuite ancré aux valeurs définies par les deux États de rendu supplémentaires D3DRS \_ MINTESSELLATIONLEVEL et D3DRS \_ MAXTESSELLATIONLEVEL, qui définissent les niveaux de pavage minimal et maximal à fixer.</span><span class="sxs-lookup"><span data-stu-id="31da5-127">The tessellation level is then clamped to values, defined by the two additional render states D3DRS\_MINTESSELLATIONLEVEL and D3DRS\_MAXTESSELLATIONLEVEL, which define the minimum and maximum tessellation levels to be clamped to.</span></span> <span data-ttu-id="31da5-128">La moyenne de l’TI pour chaque vertex le long d’un bord d’un correctif est calculée pour obtenir un niveau de pavage pour cette arête.</span><span class="sxs-lookup"><span data-stu-id="31da5-128">The Ti's for each vertex along an edge of a patch are averaged to obtain a tessellation level for that edge.</span></span> <span data-ttu-id="31da5-129">L’algorithme pour le calcul du TI pour les correctifs de rectangle, les correctifs de triangle et les N-patchs diffère dans les vertex de contrôle utilisés pour calculer le niveau de pavage.</span><span class="sxs-lookup"><span data-stu-id="31da5-129">The algorithm for computing Ti for rectangle patches, triangle patches, and N-patches differs in what control vertices are used to compute the tessellation level.</span></span>

<span data-ttu-id="31da5-130">Pour les correctifs de rectangle avec une base B-spline, les quatre sommets de contrôle les plus extérieurs sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="31da5-130">For the rectangle patches with a B-spline basis, the four outermost control vertices are used.</span></span> <span data-ttu-id="31da5-131">Par exemple, avec D3DORDER \_ cubique Order : vertex (1,1) et (1, la largeur-2) sont utilisées avec pNumSegs \[ 0 \] , les sommets (1, largeur-2) et (hauteur-2, hauteur-2) sont utilisés avec pNumSegs \[ 1, les \] sommets (hauteur-2, largeur-2) et (1, largeur-2) sont utilisés avec le pNumSegs \[ 2 \] , et les sommets (2, 1) et (1,1) sont utilisés avec \[ \]</span><span class="sxs-lookup"><span data-stu-id="31da5-131">For example, with D3DORDER\_CUBIC order: vertices (1,1) and (1,width-2) are used with pNumSegs\[0\], vertices (1,width-2) and (height-2,height-2) are used with pNumSegs\[1\], vertices (height-2,width-2) and (1,width-2) are used with pNumSegs\[2\], and vertices (2,1) and (1,1) are used with pNumSegs\[3\].</span></span>

<span data-ttu-id="31da5-132">Pour les correctifs triangulaires, les sommets des correctifs d’angle sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="31da5-132">For the triangle patches, the corner patch vertices are used.</span></span> <span data-ttu-id="31da5-133">Avec l' \_ ordre D3DORDER cubique : les sommets (0) et (9) sont utilisés avec pNumSegs \[ 0 \] , les sommets (9) et (6) sont utilisés avec pNumSegs \[ 1 \] et les sommets (6) et (0) sont utilisés avec pNumSegs \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="31da5-133">With D3DORDER\_CUBIC order: vertices (0) and (9) are used with pNumSegs\[0\], vertices (9) and (6) are used with pNumSegs\[1\] and vertices (6) and (0) are used with pNumSegs\[3\].</span></span>

<span data-ttu-id="31da5-134">Pour les N-patchs, les sommets triangulaires sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="31da5-134">For N-patches the triangle vertices are used.</span></span>

<span data-ttu-id="31da5-135">Pour les carreaux de rectangle et de triangle avec une base Bézier, les sommets de contrôle d’angle sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="31da5-135">For the rectangle and triangle patches with a Bezier basis, the corner-control vertices are used.</span></span>

<span data-ttu-id="31da5-136">Contrôle du taux de pavage par vertex.</span><span class="sxs-lookup"><span data-stu-id="31da5-136">Per-vertex tessellation rate control.</span></span> <span data-ttu-id="31da5-137">Une application peut éventuellement fournir une valeur à virgule flottante positive unique par vertex, qui peut être utilisée pour contrôler le taux de pavage.</span><span class="sxs-lookup"><span data-stu-id="31da5-137">An application can optionally supply a single positive floating-point value per vertex, which can be used to control the rate of tessellation.</span></span> <span data-ttu-id="31da5-138">Celui-ci est fourni à l’aide de l’D3DDECLUSAGE \_ TESSFACTOR, pour lequel l’index d’utilisation doit avoir la valeur 0 et le type d’entrée doit être D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="31da5-138">This is supplied using the D3DDECLUSAGE\_TESSFACTOR, for which usage index must be 0 and input type must be D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="31da5-139">Cette valeur est multipliée par le niveau de pavage par vertex.</span><span class="sxs-lookup"><span data-stu-id="31da5-139">This is multiplied to the per-vertex tessellation level.</span></span>

### <a name="math"></a><span data-ttu-id="31da5-140">Math</span><span class="sxs-lookup"><span data-stu-id="31da5-140">Math</span></span>

<span data-ttu-id="31da5-141">Le niveau de pavage (te) d’un bord e, représenté par deux vertex de contrôle (VE1, VE2), est calculé comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="31da5-141">The tessellation level (Te) for an edge e, represented by two control vertices (Ve1, Ve2), is computed as shown below :</span></span>


```
Vertex Vi: (Xi, Yi, Zi, TFactori (optional)). 
Ze1eye = Ve1 . Mdm 
Ze2eye = Ve2 . Mdm 
Te1 = MaxTessellationLevel * TFactore1 / Ze1eye 
Te2 = MaxTessellationLevel * TFactore2 / Ze2eye 
Te = ( Te1 + Te2 ) / 2; 
if Te > D3DRS_MAXTESSELLATIONLEVEL || Te < 0, then Te = D3DRS_MAXTESSELLATIONLEVEL 
if Te < D3DRS_MINTESSELLATIONLEVEL, then Te = D3DRS_MINTESSELLATIONLEVEL 
```



<span data-ttu-id="31da5-142">Quand D3DRS \_ ENABLEADAPTIVETESSELLATION a la **valeur true**, les primitives de triangle (listes de triangles, ventilateurs, bandes) sont dessinées en tant que N-patchs, [**IDirect3DDevice9 :: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) a une valeur définie inférieure à 1,0.</span><span class="sxs-lookup"><span data-stu-id="31da5-142">When D3DRS\_ENABLEADAPTIVETESSELLATION is **TRUE**, triangle primitives (triangle lists, fans, strips) are drawn as N-patches, [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) has set value less than 1.0.</span></span>

### <a name="api-changes"></a><span data-ttu-id="31da5-143">Modifications de l’API</span><span class="sxs-lookup"><span data-stu-id="31da5-143">API Changes</span></span>

<span data-ttu-id="31da5-144">Nouveaux États de rendu :</span><span class="sxs-lookup"><span data-stu-id="31da5-144">New render states:</span></span>


```
 D3DRS_ENABLEADAPTIVETESSELLATION // BOOL 
 D3DRS_MAXTESSELLATIONLEVEL       // Float 
 D3DRS_MINTESSELLATIONLEVEL       // Float 
 D3DRS_ADAPTIVETESS_X             // Float 
 D3DRS_ADAPTIVETESS_Y             // Float 
 D3DRS_ADAPTIVETESS_Z             // Float 
 D3DRS_ADAPTIVETESS_W             // Float 
 
 // D3DRS_MINTESSELLATIONLEVEL and D3DRS_MAXTESSELLATIONLEVEL 
 // cannot be less than 1 
```



<span data-ttu-id="31da5-145">Et leurs valeurs par défaut :</span><span class="sxs-lookup"><span data-stu-id="31da5-145">And their default values:</span></span>


```
D3DRS_MAXTESSELLATIONLEVEL = 1.0f 
D3DRS_MINTESSELLATIONLEVEL = 1.0f 
D3DRS_ADAPTIVETESS_X = 0.0f 
D3DRS_ADAPTIVETESS_Y = 0.0f 
D3DRS_ADAPTIVETESS_Z = 1.0f 
D3DRS_ADAPTIVETESS_W = 0.0f 
D3DRS_ENABLEADAPTIVETESSELLATION = FALSE 
```



<span data-ttu-id="31da5-146">Nouvelles extrémités matérielles :</span><span class="sxs-lookup"><span data-stu-id="31da5-146">New hardware caps:</span></span>


```
D3DDEVCAPS2_ADAPTIVETESSRTPATCH // Can adaptively tessellate RT-patches 
D3DDEVCAPS2_ADAPTIVETESSNPATCH  // Can adaptively tessellate N-patches 
```



## <a name="related-topics"></a><span data-ttu-id="31da5-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="31da5-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31da5-148">Pipeline de vertex</span><span class="sxs-lookup"><span data-stu-id="31da5-148">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
