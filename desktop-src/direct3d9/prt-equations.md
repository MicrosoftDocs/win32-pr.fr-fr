---
description: Pour bien comprendre un nuanceur qui implémente PRT, il est utile de dériver la formule utilisée par le nuanceur pour calculer Exit luminance.
ms.assetid: 66876e9e-cde1-4d04-9b31-30be1c115e6b
title: Équations PRT (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65559fada82fda7f7eed1c7d05543883a06a19e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109379"
---
# <a name="prt-equations-direct3d-9"></a><span data-ttu-id="07a9f-103">Équations PRT (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="07a9f-103">PRT Equations (Direct3D 9)</span></span>

<span data-ttu-id="07a9f-104">Pour bien comprendre un nuanceur qui implémente PRT, il est utile de dériver la formule utilisée par le nuanceur pour calculer Exit luminance.</span><span class="sxs-lookup"><span data-stu-id="07a9f-104">To fully understand a shader that implements PRT, it is useful to derive the formula the shader uses to calculate exit radiance.</span></span>

<span data-ttu-id="07a9f-105">Pour commencer, l’équation suivante est l’équation générale permettant de calculer les luminance de sortie résultant d’un éclairage direct sur un objet diffus avec un éclairage distant arbitraire.</span><span class="sxs-lookup"><span data-stu-id="07a9f-105">To start off, the following equation is the general equation to calculate exit radiance resulting from direct lighting on a diffuse object with arbitrary distant lighting.</span></span>

![équation de l’luminance de sortie résultant d’un éclairage direct sur un objet diffus avec un éclairage distant arbitraire](images/prt-theory-eq1.png)

<span data-ttu-id="07a9f-107">où :</span><span class="sxs-lookup"><span data-stu-id="07a9f-107">where:</span></span>



| <span data-ttu-id="07a9f-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="07a9f-108">Parameter</span></span>     | <span data-ttu-id="07a9f-109">Description</span><span class="sxs-lookup"><span data-stu-id="07a9f-109">Description</span></span>                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07a9f-110">PR</span><span class="sxs-lookup"><span data-stu-id="07a9f-110">Rₚ</span></span>            | <span data-ttu-id="07a9f-111">Luminance de sortie au sommet p.</span><span class="sxs-lookup"><span data-stu-id="07a9f-111">The exit radiance at vertex p.</span></span> <span data-ttu-id="07a9f-112">Évalué à chaque vertex sur la maille.</span><span class="sxs-lookup"><span data-stu-id="07a9f-112">Evaluated at every vertex on the mesh.</span></span>                                   |
| <span data-ttu-id="07a9f-113">p<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="07a9f-113">p<sub>d</sub></span></span> | <span data-ttu-id="07a9f-114">Albedo de l’aire.</span><span class="sxs-lookup"><span data-stu-id="07a9f-114">The albedo of the surface.</span></span>                                                                              |
| <span data-ttu-id="07a9f-115">pi</span><span class="sxs-lookup"><span data-stu-id="07a9f-115">pi</span></span>            | <span data-ttu-id="07a9f-116">Constante, utilisée comme facteur de normalisation de la conservation de l’énergie.</span><span class="sxs-lookup"><span data-stu-id="07a9f-116">A constant, used as an energy conservation normalization factor.</span></span>                                        |
| <span data-ttu-id="07a9f-117">L (s)</span><span class="sxs-lookup"><span data-stu-id="07a9f-117">L(s)</span></span>          | <span data-ttu-id="07a9f-118">Environnement d’éclairage (source luminance).</span><span class="sxs-lookup"><span data-stu-id="07a9f-118">The lighting environment (source radiance).</span></span>                                                             |
| <span data-ttu-id="07a9f-119">VP ₍ s ₎</span><span class="sxs-lookup"><span data-stu-id="07a9f-119">Vₚ₍ₛ₎</span></span>         | <span data-ttu-id="07a9f-120">Fonction de visibilité binaire pour le point p.</span><span class="sxs-lookup"><span data-stu-id="07a9f-120">A binary visibility function for point p.</span></span> <span data-ttu-id="07a9f-121">La valeur est 1 si le point peut voir la lumière, 0 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="07a9f-121">It is 1 if the point can see the light, 0 if not.</span></span>             |
| <span data-ttu-id="07a9f-122">HNP ₍ s ₎</span><span class="sxs-lookup"><span data-stu-id="07a9f-122">Hₙₚ₍ₛ₎</span></span>        | <span data-ttu-id="07a9f-123">Terme cosinus de la Loi de Lambert.</span><span class="sxs-lookup"><span data-stu-id="07a9f-123">The cosine term from Lambert's law.</span></span> <span data-ttu-id="07a9f-124">Égal à Max ((NP · s), 0) où NP correspond à la surface normale au point p.</span><span class="sxs-lookup"><span data-stu-id="07a9f-124">Equal to max((Nₚ· s), 0) where Nₚ is the surface normal at point p.</span></span> |
| <span data-ttu-id="07a9f-125">s</span><span class="sxs-lookup"><span data-stu-id="07a9f-125">s</span></span>             | <span data-ttu-id="07a9f-126">Variable qui s’intègre sur la sphère.</span><span class="sxs-lookup"><span data-stu-id="07a9f-126">The variable that integrates over the sphere.</span></span>                                                           |



 

<span data-ttu-id="07a9f-127">À l’aide de fonctions sphériques, telles que les harmoniques sphériques, l’équation suivante est proche de l’environnement d’éclairage.</span><span class="sxs-lookup"><span data-stu-id="07a9f-127">Using spherical basis functions, such as spherical harmonics, the following equation approximates the lighting environment.</span></span>

![équation de l’environnement d’éclairage](images/prt-theory-eq2.png)

<span data-ttu-id="07a9f-129">où :</span><span class="sxs-lookup"><span data-stu-id="07a9f-129">where:</span></span>



| <span data-ttu-id="07a9f-130">Paramètre</span><span class="sxs-lookup"><span data-stu-id="07a9f-130">Parameter</span></span>        | <span data-ttu-id="07a9f-131">Description</span><span class="sxs-lookup"><span data-stu-id="07a9f-131">Description</span></span>                                              |
|------------------|----------------------------------------------------------|
| <span data-ttu-id="07a9f-132">L (s)</span><span class="sxs-lookup"><span data-stu-id="07a9f-132">L(s)</span></span>             | <span data-ttu-id="07a9f-133">Environnement d’éclairage (source luminance).</span><span class="sxs-lookup"><span data-stu-id="07a9f-133">The lighting environment (source radiance).</span></span>              |
| <span data-ttu-id="07a9f-134">i</span><span class="sxs-lookup"><span data-stu-id="07a9f-134">i</span></span>                | <span data-ttu-id="07a9f-135">Entier qui totalise le nombre de fonctions de base.</span><span class="sxs-lookup"><span data-stu-id="07a9f-135">An integer that sums over the number of basis functions.</span></span> |
| <span data-ttu-id="07a9f-136">O</span><span class="sxs-lookup"><span data-stu-id="07a9f-136">O</span></span>                | <span data-ttu-id="07a9f-137">Ordre des harmoniques sphériques.</span><span class="sxs-lookup"><span data-stu-id="07a9f-137">The order of spherical harmonics.</span></span>                        |
| <span data-ttu-id="07a9f-138">l<sub></sub></span><span class="sxs-lookup"><span data-stu-id="07a9f-138">l<sub>i</sub></span></span>    | <span data-ttu-id="07a9f-139">Un coefficient.</span><span class="sxs-lookup"><span data-stu-id="07a9f-139">A coefficient.</span></span>                                           |
| <span data-ttu-id="07a9f-140">Y<sub>(s)</sub></span><span class="sxs-lookup"><span data-stu-id="07a9f-140">Y<sub>i(s)</sub></span></span> | <span data-ttu-id="07a9f-141">Certaines fonctions de base sur la sphère.</span><span class="sxs-lookup"><span data-stu-id="07a9f-141">Some basis function over the sphere.</span></span>                     |



 

<span data-ttu-id="07a9f-142">La collection de ces coefficients, L', fournit la approximation optimale pour la ou les fonctions L avec les fonctions de base Y (s).</span><span class="sxs-lookup"><span data-stu-id="07a9f-142">The collection of these coefficients, L', provides the optimal approximation for function L(s) with the basis functions Y(s).</span></span> <span data-ttu-id="07a9f-143">Le remplacement et la distribution produisent l’équation suivante.</span><span class="sxs-lookup"><span data-stu-id="07a9f-143">Substituting and distributing yields the following equation.</span></span>

![équation de l’luminance de sortie après remplacement de l (s) et distribution](images/prt-theory-eq3.png)

<span data-ttu-id="07a9f-145">L’intégrale de Y<sub>i (s)</sub>VP ₍ s ₎ HNP ₍ s ₎ est un coefficient de transfert t<sub>pi</sub> que le simulateur Précalcule pour chaque vertex sur la maille.</span><span class="sxs-lookup"><span data-stu-id="07a9f-145">The integral of Y<sub>i(s)</sub>Vₚ₍ₛ₎Hₙₚ₍ₛ₎ is a transfer coefficient t<sub>pi</sub> that the simulator precomputes for every vertex on the mesh.</span></span> <span data-ttu-id="07a9f-146">La substitution de ce code génère l’équation suivante.</span><span class="sxs-lookup"><span data-stu-id="07a9f-146">Substituting this yields the following equation.</span></span>

![équation de Exit luminance après avoir remplacé le coefficient de transfert](images/prt-theory-eq4.png)

<span data-ttu-id="07a9f-148">La modification de cette notation vectorielle produit l’équation non compressée suivante pour calculer les luminance de sortie pour chaque canal.</span><span class="sxs-lookup"><span data-stu-id="07a9f-148">Changing this to vector notation yields the following uncompressed equation to calculate exit radiance for each channel.</span></span>

![équation de Exit luminance après avoir changé en notation Vector](images/prt-theory-eq5.png)

<span data-ttu-id="07a9f-150">où :</span><span class="sxs-lookup"><span data-stu-id="07a9f-150">where:</span></span>



| <span data-ttu-id="07a9f-151">Paramètre</span><span class="sxs-lookup"><span data-stu-id="07a9f-151">Parameter</span></span>     | <span data-ttu-id="07a9f-152">Description</span><span class="sxs-lookup"><span data-stu-id="07a9f-152">Description</span></span>                                                                                                                                                                         |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07a9f-153">PR</span><span class="sxs-lookup"><span data-stu-id="07a9f-153">Rₚ</span></span>            | <span data-ttu-id="07a9f-154">Luminance de sortie au sommet p.</span><span class="sxs-lookup"><span data-stu-id="07a9f-154">The exit radiance at vertex p.</span></span>                                                                                                                                                      |
| <span data-ttu-id="07a9f-155">p<sub>d</sub></span><span class="sxs-lookup"><span data-stu-id="07a9f-155">p<sub>d</sub></span></span> | <span data-ttu-id="07a9f-156">Albedo de l’aire.</span><span class="sxs-lookup"><span data-stu-id="07a9f-156">The albedo of the surface.</span></span>                                                                                                                                                          |
| <span data-ttu-id="07a9f-157">Budget</span><span class="sxs-lookup"><span data-stu-id="07a9f-157">L'</span></span>            | <span data-ttu-id="07a9f-158">Le vecteur de l<sub>i</sub>et est la projection de la source luminance dans les fonctions de base d’harmoniques sphériques.</span><span class="sxs-lookup"><span data-stu-id="07a9f-158">The vector of l<sub>i</sub>, and is the projection of the source radiance into the spherical harmonic basis functions.</span></span> <span data-ttu-id="07a9f-159">Il s’agit d’un vecteur de commande ² de coefficients d’harmonique sphérique.</span><span class="sxs-lookup"><span data-stu-id="07a9f-159">This is an order² vector of spherical harmonic coefficients.</span></span> |
| <span data-ttu-id="07a9f-160">PM</span><span class="sxs-lookup"><span data-stu-id="07a9f-160">Tₚ</span></span>            | <span data-ttu-id="07a9f-161">Vecteur de transfert de commande ² pour le vertex p.</span><span class="sxs-lookup"><span data-stu-id="07a9f-161">An order² transfer vector for vertex p.</span></span> <span data-ttu-id="07a9f-162">Le simulateur divise les coefficients de transfert par p.</span><span class="sxs-lookup"><span data-stu-id="07a9f-162">The simulator divides the transfer coefficients by p.</span></span>                                                                                       |



 

<span data-ttu-id="07a9f-163">Ces deux vecteurs sont un vecteur de commande ² de coefficients d’harmonique sphérique. Notez donc qu’il s’agit simplement d’un point.</span><span class="sxs-lookup"><span data-stu-id="07a9f-163">Both of these vectors are an order² vector of spherical harmonic coefficients, so notice that this is simply a dot product.</span></span> <span data-ttu-id="07a9f-164">En fonction de la commande, le point peut être coûteux afin que la compression puisse être utilisée.</span><span class="sxs-lookup"><span data-stu-id="07a9f-164">Depending on the order, the dot can be expensive so compression can be used.</span></span> <span data-ttu-id="07a9f-165">Un algorithme appelé CPCA (cluster principal Component Analysis) compresse efficacement les données.</span><span class="sxs-lookup"><span data-stu-id="07a9f-165">An algorithm called Clustered Principal Component Analysis (CPCA) efficiently compresses the data.</span></span> <span data-ttu-id="07a9f-166">Cela permet l’utilisation d’une approximation d’harmonique sphérique d’ordre supérieur qui produit des ombres plus nettes.</span><span class="sxs-lookup"><span data-stu-id="07a9f-166">This enables the use of a higher-order spherical harmonic approximation which results in sharper shadows.</span></span>

<span data-ttu-id="07a9f-167">CPCA fournit l’équation suivante pour rapprocher le vecteur de transfert.</span><span class="sxs-lookup"><span data-stu-id="07a9f-167">CPCA provides the following equation to approximate the transfer vector.</span></span>

![équation du vecteur de transfert approximatif](images/prt-theory-eq6.png)

<span data-ttu-id="07a9f-169">où :</span><span class="sxs-lookup"><span data-stu-id="07a9f-169">where:</span></span>



| <span data-ttu-id="07a9f-170">Paramètre</span><span class="sxs-lookup"><span data-stu-id="07a9f-170">Parameter</span></span>      | <span data-ttu-id="07a9f-171">Description</span><span class="sxs-lookup"><span data-stu-id="07a9f-171">Description</span></span>                                          |
|----------------|------------------------------------------------------|
| <span data-ttu-id="07a9f-172">PM</span><span class="sxs-lookup"><span data-stu-id="07a9f-172">Tₚ</span></span>             | <span data-ttu-id="07a9f-173">Vecteur de transfert pour le vertex p.</span><span class="sxs-lookup"><span data-stu-id="07a9f-173">The transfer vector for vertex p.</span></span>                    |
| <span data-ttu-id="07a9f-174">MK</span><span class="sxs-lookup"><span data-stu-id="07a9f-174">Mₖ</span></span>             | <span data-ttu-id="07a9f-175">Moyenne du cluster k.</span><span class="sxs-lookup"><span data-stu-id="07a9f-175">The mean for cluster k.</span></span>                              |
| <span data-ttu-id="07a9f-176">j</span><span class="sxs-lookup"><span data-stu-id="07a9f-176">j</span></span>              | <span data-ttu-id="07a9f-177">Entier qui additionne le nombre de vecteurs PCA.</span><span class="sxs-lookup"><span data-stu-id="07a9f-177">An integer that sums over the number of PCA vectors.</span></span> |
| <span data-ttu-id="07a9f-178">N</span><span class="sxs-lookup"><span data-stu-id="07a9f-178">N</span></span>              | <span data-ttu-id="07a9f-179">Nombre de vecteurs PCA.</span><span class="sxs-lookup"><span data-stu-id="07a9f-179">The number of PCA vectors.</span></span>                           |
| <span data-ttu-id="07a9f-180">w<sub>PJ</sub></span><span class="sxs-lookup"><span data-stu-id="07a9f-180">w<sub>pj</sub></span></span> | <span data-ttu-id="07a9f-181">Poids de JTH PCA pour le point p.</span><span class="sxs-lookup"><span data-stu-id="07a9f-181">The jth PCA weight for point p.</span></span>                      |
| <span data-ttu-id="07a9f-182">B<sub>kJ</sub></span><span class="sxs-lookup"><span data-stu-id="07a9f-182">B<sub>kj</sub></span></span> | <span data-ttu-id="07a9f-183">Le vecteur de base JTH PCA pour le cluster k.</span><span class="sxs-lookup"><span data-stu-id="07a9f-183">The jth PCA basis vector for cluster k.</span></span>              |



 

<span data-ttu-id="07a9f-184">Un cluster est tout simplement un nombre de vertex qui partagent le même vecteur de moyenne.</span><span class="sxs-lookup"><span data-stu-id="07a9f-184">A cluster is simply some number of vertices that share the same mean vector.</span></span> <span data-ttu-id="07a9f-185">L’obtention de la moyenne du cluster, des pondérations de l’APC, des vecteurs de base de l’APC et des ID de cluster pour les vertex est décrite ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="07a9f-185">How to get the cluster mean, the PCA weights, the PCA basis vectors, and the cluster ids for the vertices is discussed below.</span></span>

<span data-ttu-id="07a9f-186">Le remplacement de ces deux équations donne :</span><span class="sxs-lookup"><span data-stu-id="07a9f-186">Substituting these two equations yields:</span></span>

![équation de Exit luminance après avoir remplacé le vecteur de transfert](images/prt-theory-eq7.png)

<span data-ttu-id="07a9f-188">Ensuite, la distribution du produit scalaire produit l’équation suivante.</span><span class="sxs-lookup"><span data-stu-id="07a9f-188">Then distributing the dot product yields the following equation.</span></span>

![équation de l’luminance de sortie après la distribution du produit scalaire](images/prt-theory-eq8.png)

<span data-ttu-id="07a9f-190">Parce que les deux (MK · L') et (B<sub>kJ</sub>· L') sont des constantes par vertex, l’exemple calcule ces valeurs avec l’UC et les passe comme constantes dans le nuanceur de sommets. étant donné que w<sub>PJ</sub> change pour chaque vertex, l’exemple stocke ces données par vertex dans la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="07a9f-190">Because both (Mₖ· L') and (B<sub>kj</sub>· L') are constant per vertex, the sample calculates these values with the CPU and passes them as constants into the vertex shader; because w<sub>pj</sub> changes for each vertex, the sample stores this per-vertex data in the vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="07a9f-191">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="07a9f-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07a9f-192">Transfert de luminance précalculé</span><span class="sxs-lookup"><span data-stu-id="07a9f-192">Precomputed Radiance Transfer</span></span>](precomputed-radiance-transfer.md)
</dt> </dl>

 

 



