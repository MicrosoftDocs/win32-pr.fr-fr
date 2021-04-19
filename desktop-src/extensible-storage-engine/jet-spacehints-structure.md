---
description: 'En savoir plus sur : structure JET_SPACEHINTS'
title: Structure JET_SPACEHINTS
TOCTitle: JET_SPACEHINTS Structure
ms:assetid: 23328993-93c9-4a23-892b-e6a9f434d1d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269205(v=EXCHG.10)
ms:contentKeyID: 32765508
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf786d1f47b5eaae3f9540c8635853020f9b0521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517435"
---
# <a name="jet_spacehints-structure"></a><span data-ttu-id="5c64a-103">Structure JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="5c64a-103">JET_SPACEHINTS Structure</span></span>


<span data-ttu-id="5c64a-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="5c64a-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_spacehints-structure"></a><span data-ttu-id="5c64a-105">Structure JET_SPACEHINTS</span><span class="sxs-lookup"><span data-stu-id="5c64a-105">JET_SPACEHINTS Structure</span></span>

<span data-ttu-id="5c64a-106">La structure **JET_SPACEHINTS** contient des informations sur les modèles d’allocation d’espace quand une arborescence binaire (b-Tree) s’agrandit via les fractionnements Append ou Hotpoint.</span><span class="sxs-lookup"><span data-stu-id="5c64a-106">The **JET_SPACEHINTS** structure contains information about space allocation patterns when a b-tree grows through append or hotpoint splits.</span></span> <span data-ttu-id="5c64a-107">Les fractionnements d’ajout se produisent lorsque des enregistrements sont ajoutés à la fin d’un arbre b (b-Tree) et que des fractionnements Hotpoint se produisent lorsque plusieurs enregistrements sont ajoutés au même point d’insertion virtuel (par exemple, en ajoutant « Marie », « Mark », « Martin' », « Mary » au milieu d’une arborescence binaire qui est triée par ordre alphabétique).</span><span class="sxs-lookup"><span data-stu-id="5c64a-107">Append splits happen when records are added to the end of a b-tree and hotpoint splits happen when multiple records are added to the same virtual insertion point (for example, adding 'Marie', 'Mark', 'Martin', 'Mary' to the middle of a b-tree that is sorted alphabetically).</span></span>

<span data-ttu-id="5c64a-108">**Windows 7 :** La structure **JET_SPACEHINTS** est introduite dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5c64a-108">**Windows 7:** The **JET_SPACEHINTS** structure is introduced in Windows 7.</span></span>

```cpp
    typedef struct tagJET_SPACEHINTS {
      unsigned long cbStruct;
      unsigned long ulInitialDensity;
      unsigned long cbInitial;
      JET_GRBIT grbit;
      unsigned long ulMaintDensity;
      unsigned long ulGrowth;
      unsigned long cbMinExtent;
      unsigned long cbMaxExtent;
    } JET_SPACEHINTS;
```

### <a name="members"></a><span data-ttu-id="5c64a-109">Membres</span><span class="sxs-lookup"><span data-stu-id="5c64a-109">Members</span></span>

<span data-ttu-id="5c64a-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="5c64a-110">**cbStruct**</span></span>

<span data-ttu-id="5c64a-111">Taille, en octets, de cette structure.</span><span class="sxs-lookup"><span data-stu-id="5c64a-111">The size, in bytes, of this structure.</span></span> <span data-ttu-id="5c64a-112">Affectez à ce membre la valeur sizeof (JET_SPACEHINTS).</span><span class="sxs-lookup"><span data-stu-id="5c64a-112">Set this member to sizeof( JET_SPACEHINTS ).</span></span>

<span data-ttu-id="5c64a-113">**ulInitialDensity**</span><span class="sxs-lookup"><span data-stu-id="5c64a-113">**ulInitialDensity**</span></span>

<span data-ttu-id="5c64a-114">La densité au format (Append).</span><span class="sxs-lookup"><span data-stu-id="5c64a-114">The density at (append) layout.</span></span>

<span data-ttu-id="5c64a-115">**cbInitial**</span><span class="sxs-lookup"><span data-stu-id="5c64a-115">**cbInitial**</span></span>

<span data-ttu-id="5c64a-116">Taille initiale (en octets) de l’objet en cours de création.</span><span class="sxs-lookup"><span data-stu-id="5c64a-116">The initial size (in bytes) of the object being created.</span></span> <span data-ttu-id="5c64a-117">Il doit s’agir d’un multiple de la taille de page de la base de données.</span><span class="sxs-lookup"><span data-stu-id="5c64a-117">This must be a multiple of the database page size.</span></span>

<span data-ttu-id="5c64a-118">**grbit**</span><span class="sxs-lookup"><span data-stu-id="5c64a-118">**grbit**</span></span>

<span data-ttu-id="5c64a-119">Groupe de bits qui contient les options à utiliser pour cette structure, qui incluent zéro ou plusieurs des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="5c64a-119">A group of bits that contain the options to be used for this structure, which include zero or more of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5c64a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c64a-120">Value</span></span></p></th>
<th><p><span data-ttu-id="5c64a-121">Signification</span><span class="sxs-lookup"><span data-stu-id="5c64a-121">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c64a-122">JET_bitSpaceHintsUtilizeParentSpace</span><span class="sxs-lookup"><span data-stu-id="5c64a-122">JET_bitSpaceHintsUtilizeParentSpace</span></span><br />
<span data-ttu-id="5c64a-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5c64a-123">0x00000001</span></span></p></td>
<td><p><span data-ttu-id="5c64a-124">Modifie la stratégie d’allocation interne pour obtenir l’espace heirarchically à partir du parent immédiat d’une arborescence binaire (b-Tree).</span><span class="sxs-lookup"><span data-stu-id="5c64a-124">Changes the internal allocation policy to get space heirarchically from the immediate parent of a b-tree.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c64a-125">JET_bitCreateHintAppendSequential</span><span class="sxs-lookup"><span data-stu-id="5c64a-125">JET_bitCreateHintAppendSequential</span></span><br />
<span data-ttu-id="5c64a-126">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5c64a-126">0x00000002</span></span></p></td>
<td><p><span data-ttu-id="5c64a-127">Active le comportement de fractionnement d’ajout pour augmenter en fonction de la dynamique de croissance de la table (définie par cbMinExtent, ulGrowth, cbMaxExtent).</span><span class="sxs-lookup"><span data-stu-id="5c64a-127">Enables append split behavior to grow according to the growth dynamics of the table (set by cbMinExtent, ulGrowth, cbMaxExtent).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c64a-128">JET_bitCreateHintHotpointSequential</span><span class="sxs-lookup"><span data-stu-id="5c64a-128">JET_bitCreateHintHotpointSequential</span></span><br />
<span data-ttu-id="5c64a-129">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5c64a-129">0x00000004</span></span></p></td>
<td><p><span data-ttu-id="5c64a-130">Active le comportement de fractionnement Hotpoint pour augmenter en fonction de la dynamique de croissance de la table (définie par cbMinExtent, ulGrowth, cbMaxExtent).</span><span class="sxs-lookup"><span data-stu-id="5c64a-130">Enables hotpoint split behavior to grow according to the growth dynamics of the table (set by cbMinExtent, ulGrowth, cbMaxExtent).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c64a-131">JET_bitRetrieveHintTableScanForward</span><span class="sxs-lookup"><span data-stu-id="5c64a-131">JET_bitRetrieveHintTableScanForward</span></span><br />
<span data-ttu-id="5c64a-132">0x00000010</span><span class="sxs-lookup"><span data-stu-id="5c64a-132">0x00000010</span></span></p></td>
<td><p><span data-ttu-id="5c64a-133">Si cette valeur est définie, le client indique que l’analyse par progression séquentielle est le modèle d’utilisation prédominant de ce tableau.</span><span class="sxs-lookup"><span data-stu-id="5c64a-133">If set, the client indicates that forward sequential scan is the predominant usage pattern of this table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c64a-134">JET_bitRetrieveHintTableScanBackward</span><span class="sxs-lookup"><span data-stu-id="5c64a-134">JET_bitRetrieveHintTableScanBackward</span></span><br />
<span data-ttu-id="5c64a-135">0x00000020</span><span class="sxs-lookup"><span data-stu-id="5c64a-135">0x00000020</span></span></p></td>
<td><p><span data-ttu-id="5c64a-136">Si cette valeur est définie, le client indique que l’analyse de séquence arrière est le modèle d’utilisation prédominant de cette table.</span><span class="sxs-lookup"><span data-stu-id="5c64a-136">If set, the client indicates that backward sequential scan is the predominant usage pattern of this table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c64a-137">JET_bitDeleteHintTableSequential</span><span class="sxs-lookup"><span data-stu-id="5c64a-137">JET_bitDeleteHintTableSequential</span></span><br />
<span data-ttu-id="5c64a-138">0x00000100</span><span class="sxs-lookup"><span data-stu-id="5c64a-138">0x00000100</span></span></p></td>
<td><p><span data-ttu-id="5c64a-139">Si cette valeur est définie, l’application s’attend à ce que cette table soit nettoyée dans l’ordre séquentiel, de la clé la plus basse à la clé la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="5c64a-139">If set, the application expects this table to be cleaned up in sequential order, from lowest key to highest key.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5c64a-140">**ulMaintDensity**</span><span class="sxs-lookup"><span data-stu-id="5c64a-140">**ulMaintDensity**</span></span>

<span data-ttu-id="5c64a-141">densité à mulMaintDensity</span><span class="sxs-lookup"><span data-stu-id="5c64a-141">density to mulMaintDensity</span></span>

<span data-ttu-id="5c64a-142">Densité à gérer à.</span><span class="sxs-lookup"><span data-stu-id="5c64a-142">Density to maintain at.</span></span> <span data-ttu-id="5c64a-143">Si les indicateurs d’espace spécifient JET_bitRetrieveHintTableScanForward ou JET_bitRetrieveHintTableScanBackward, la défragmentation de table est déclenchée lorsque l’espace utilisé dans le tableau chute sous ce seuil.</span><span class="sxs-lookup"><span data-stu-id="5c64a-143">If the space hints specify JET_bitRetrieveHintTableScanForward or JET_bitRetrieveHintTableScanBackward, table defragmentation will be triggered when the used space in the table drops below this threshold.</span></span> <span data-ttu-id="5c64a-144">La défragmentation de table peut être désactivée en affectant à ce membre la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="5c64a-144">Table defragmentation can be disabled by setting this member to zero.</span></span> <span data-ttu-id="5c64a-145">La définition de ce membre sur 100 entraînera l’exécution de la défragmentation de la table dès qu’une page sera libérée.</span><span class="sxs-lookup"><span data-stu-id="5c64a-145">Setting this member to 100 will cause table defragmentation to run as soon as a page is freed.</span></span>

<span data-ttu-id="5c64a-146">**ulGrowth**</span><span class="sxs-lookup"><span data-stu-id="5c64a-146">**ulGrowth**</span></span>

<span data-ttu-id="5c64a-147">Croissance en pourcentage de la dernière croissance ou taille initiale, arrondie à la taille d’allocation JET Native la plus proche.</span><span class="sxs-lookup"><span data-stu-id="5c64a-147">The percent growth from the last growth or initial size, rounded to nearest native JET allocation size.</span></span>

<span data-ttu-id="5c64a-148">**cbMinExtent trop petit**</span><span class="sxs-lookup"><span data-stu-id="5c64a-148">**cbMinExtent too small**</span></span>

<span data-ttu-id="5c64a-149">Cela remplace ulGrowth s’il est trop petit.</span><span class="sxs-lookup"><span data-stu-id="5c64a-149">This overrides ulGrowth if too small.</span></span>

<span data-ttu-id="5c64a-150">**cbMaxExtent**</span><span class="sxs-lookup"><span data-stu-id="5c64a-150">**cbMaxExtent**</span></span>

<span data-ttu-id="5c64a-151">Valeur maximale pour la croissance en octets.</span><span class="sxs-lookup"><span data-stu-id="5c64a-151">The maximum value for growth in bytes.</span></span> <span data-ttu-id="5c64a-152">Ce cap ulGrowth.</span><span class="sxs-lookup"><span data-stu-id="5c64a-152">This caps ulGrowth.</span></span>

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a><span data-ttu-id="5c64a-153">Quand une arborescence binaire (b-Tree) croît par le biais d’ajouts ou de fractionnements Hotpoint (par opposition aux insertions d’enregistrements aléatoires), la quantité d’espace que la table augmentera est calculée comme suit :</span><span class="sxs-lookup"><span data-stu-id="5c64a-153">When a b-tree grows through append or hotpoint splits (as opposed to random record insertions), the amount of space the table will grow by is calculated as follows:</span></span>

1.  <span data-ttu-id="5c64a-154">Lors de la création, nous offrons toujours le cbInitial d’arbre b (b-Tree).</span><span class="sxs-lookup"><span data-stu-id="5c64a-154">At creation, we give the b-tree cbInitial, always.</span></span>

2.  <span data-ttu-id="5c64a-155">Lors de la première allocation d’une zone donnée, nous allons allouer : cbInitial \* ulGrowth/100 (arrondi à la taille de page de la base de données) ou cbMinExtent s’il est plus grand.</span><span class="sxs-lookup"><span data-stu-id="5c64a-155">During the first allocation of a given area, we will allocate: cbInitial \* ulGrowth / 100 (rounded to the DB's page size), or cbMinExtent if larger.</span></span>

3.  <span data-ttu-id="5c64a-156">Lors de la prochaine allocation, cbLastAlloc \* ulGrowth/100 (arrondi à la taille de page de la base de la base de la base de la base de la base) ou cbMinExtent s’il est plus grand.</span><span class="sxs-lookup"><span data-stu-id="5c64a-156">During the next allocation, cbLastAlloc \* ulGrowth / 100 (rounded to the page size of the DB), or cbMinExtent if larger.</span></span>

4.  <span data-ttu-id="5c64a-157">À une certaine allocation (qui peut être la première allocation), la taille calculée dépassera cbMaxExtent et sera la taille de croissance par la suite.</span><span class="sxs-lookup"><span data-stu-id="5c64a-157">At some allocation (which could be the first allocation), the calculated size will exceed cbMaxExtent, and that will be the growth size thereafter.</span></span>

### <a name="requirements"></a><span data-ttu-id="5c64a-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c64a-158">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c64a-159"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="5c64a-159"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="5c64a-160">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="5c64a-160">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c64a-161"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="5c64a-161"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="5c64a-162">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="5c64a-162">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c64a-163"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="5c64a-163"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="5c64a-164">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="5c64a-164">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="5c64a-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c64a-165">See Also</span></span>

[<span data-ttu-id="5c64a-166">JET_TABLECREATE2</span><span class="sxs-lookup"><span data-stu-id="5c64a-166">JET_TABLECREATE2</span></span>](./jet-tablecreate2-structure.md)  
[<span data-ttu-id="5c64a-167">JET_TABLECREATE3</span><span class="sxs-lookup"><span data-stu-id="5c64a-167">JET_TABLECREATE3</span></span>](./jet-tablecreate3-structure.md)
