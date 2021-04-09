---
description: 'En savoir plus sur : structure JET_TUPLELIMITS'
title: Structure JET_TUPLELIMITS
TOCTitle: JET_TUPLELIMITS Structure
ms:assetid: 2610e2e5-5883-4aec-bc66-e6160b76c264
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269207(v=EXCHG.10)
ms:contentKeyID: 32765510
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
ms.openlocfilehash: 491f9248db607836b34f1fc0fcacc504b3c1d3f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953111"
---
# <a name="jet_tuplelimits-structure"></a><span data-ttu-id="37f4e-103">Structure JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="37f4e-103">JET_TUPLELIMITS Structure</span></span>


<span data-ttu-id="37f4e-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="37f4e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_tuplelimits-structure"></a><span data-ttu-id="37f4e-105">Structure JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="37f4e-105">JET_TUPLELIMITS Structure</span></span>

<span data-ttu-id="37f4e-106">La structure **JET_TUPLELIMITS** permet de personnaliser les caractéristiques de l’index de tuples par index, plutôt qu’une base par instance, à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="37f4e-106">The **JET_TUPLELIMITS** structure allows customization of the tuple index characteristics on a per-index basis, rather than a per-instance basis, using [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span>

<span data-ttu-id="37f4e-107">**Windows Server 2003 :** La structure **JET_TUPLELIMITS** est introduite dans Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="37f4e-107">**Windows Server 2003:** The **JET_TUPLELIMITS** structure is introduced in Windows Server 2003.</span></span>

```cpp
    typedef struct tagJET_TUPLELIMITS {
      unsigned long chLengthMin;
      unsigned long chLengthMax;
      unsigned long chToIndexMax;
      unsigned long cchIncrement;
      unsigned long ichStart;
    } JET_TUPLELIMITS;
```

### <a name="members"></a><span data-ttu-id="37f4e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="37f4e-108">Members</span></span>

<span data-ttu-id="37f4e-109">**chLengthMin**</span><span class="sxs-lookup"><span data-stu-id="37f4e-109">**chLengthMin**</span></span>

<span data-ttu-id="37f4e-110">Longueur minimale d’un tuple.</span><span class="sxs-lookup"><span data-stu-id="37f4e-110">The minimum length of a tuple.</span></span> <span data-ttu-id="37f4e-111">La valeur par défaut est 3.</span><span class="sxs-lookup"><span data-stu-id="37f4e-111">The default value is 3.</span></span>

<span data-ttu-id="37f4e-112">**chLengthMax**</span><span class="sxs-lookup"><span data-stu-id="37f4e-112">**chLengthMax**</span></span>

<span data-ttu-id="37f4e-113">Longueur maximale d’un tuple.</span><span class="sxs-lookup"><span data-stu-id="37f4e-113">The maximum length of a tuple.</span></span> <span data-ttu-id="37f4e-114">La valeur par défaut est 10.</span><span class="sxs-lookup"><span data-stu-id="37f4e-114">The default value is 10.</span></span>

<span data-ttu-id="37f4e-115">**chToIndexMax**</span><span class="sxs-lookup"><span data-stu-id="37f4e-115">**chToIndexMax**</span></span>

<span data-ttu-id="37f4e-116">Longueur maximale d’une chaîne à indexer.</span><span class="sxs-lookup"><span data-stu-id="37f4e-116">The maximum length of a string to index.</span></span> <span data-ttu-id="37f4e-117">Par exemple, si une colonne a une longueur de 100 caractères et que **chToIndexMax** est défini sur 60, seuls les 60 premiers caractères de la colonne seront indexés.</span><span class="sxs-lookup"><span data-stu-id="37f4e-117">For example, if a column is 100 characters long, and **chToIndexMax** is set to 60, then only the first 60 characters of the column will be indexed.</span></span> <span data-ttu-id="37f4e-118">La valeur par défaut est 32767.</span><span class="sxs-lookup"><span data-stu-id="37f4e-118">The default value is 32767.</span></span>

<span data-ttu-id="37f4e-119">**cchIncrement**</span><span class="sxs-lookup"><span data-stu-id="37f4e-119">**cchIncrement**</span></span>

<span data-ttu-id="37f4e-120">Cela permet de configurer le Stride sur une base par index.</span><span class="sxs-lookup"><span data-stu-id="37f4e-120">This allows the stride to be configured on a per index basis.</span></span>

<span data-ttu-id="37f4e-121">**Windows Vista :** Le membre **cchIncrement** est introduit dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="37f4e-121">**Windows Vista:** The **cchIncrement** member is introduced in Windows Vista.</span></span> <span data-ttu-id="37f4e-122">Avant Windows Vista, la quantité de décalage de la fenêtre (« Stride ») était toujours de 1, comme indiqué dans l’exemple de la section Notes.</span><span class="sxs-lookup"><span data-stu-id="37f4e-122">Prior to Windows Vista, the amount to shift the window (the "stride") was always 1, as is shown in the example in the remarks section.</span></span>

<span data-ttu-id="37f4e-123">**ichStart**</span><span class="sxs-lookup"><span data-stu-id="37f4e-123">**ichStart**</span></span>

<span data-ttu-id="37f4e-124">Offset dans la valeur pour commencer à récupérer des tuples à partir de la valeur.</span><span class="sxs-lookup"><span data-stu-id="37f4e-124">The offset into the value to begin taking retrieving tuples from the value.</span></span>

<span data-ttu-id="37f4e-125">**Windows Vista :** Le membre **ichStart** est introduit dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="37f4e-125">**Windows Vista:** The **ichStart** member is introduced in Windows Vista.</span></span>

### <a name="remarks"></a><span data-ttu-id="37f4e-126">Notes</span><span class="sxs-lookup"><span data-stu-id="37f4e-126">Remarks</span></span>

<span data-ttu-id="37f4e-127">Un index de tuple parcourt une chaîne et indexe toutes ses sous-chaînes possibles de **chLengthMax**.</span><span class="sxs-lookup"><span data-stu-id="37f4e-127">A tuple index walks a string and indexes all of its possible substrings of **chLengthMax**.</span></span> <span data-ttu-id="37f4e-128">À la fin de la chaîne (ou à la position **chToIndexMax**, selon ce qui se produit en premier), les sous-chaînes d’au moins **chLengthMin** seront indexées.</span><span class="sxs-lookup"><span data-stu-id="37f4e-128">At the end of the string (or at position **chToIndexMax**, whichever occurs first), the substrings of at least **chLengthMin** will be indexed.</span></span>

<span data-ttu-id="37f4e-129">Un index de tuple peut être utilisé pour rechercher des chaînes avec des caractères génériques de début et de fin.</span><span class="sxs-lookup"><span data-stu-id="37f4e-129">A tuple index can be used for searching strings with both leading and trailing wildcards.</span></span>

<span data-ttu-id="37f4e-130">En supposant une ligne avec un champ de texte « pluie en Espagne \! », si un index de tuple est créé avec les paramètres **chLengthMin**= 2 et **chLengthMax**= 3, les entrées suivantes sont créées dans l’index :</span><span class="sxs-lookup"><span data-stu-id="37f4e-130">Assuming a row with a text field of "RAIN IN SPAIN\!", if a tuple index gets created with parameters **chLengthMin**=2, and **chLengthMax**=3, the following entries are created in the index:</span></span>

<span data-ttu-id="37f4e-131">"RAI"</span><span class="sxs-lookup"><span data-stu-id="37f4e-131">"RAI"</span></span>  
<span data-ttu-id="37f4e-132">Ayn</span><span class="sxs-lookup"><span data-stu-id="37f4e-132">"AIN"</span></span>  
<span data-ttu-id="37f4e-133">DANS</span><span class="sxs-lookup"><span data-stu-id="37f4e-133">"IN "</span></span>  
<span data-ttu-id="37f4e-134">« N I »</span><span class="sxs-lookup"><span data-stu-id="37f4e-134">"N I"</span></span>  
<span data-ttu-id="37f4e-135">DANS</span><span class="sxs-lookup"><span data-stu-id="37f4e-135">" IN"</span></span>  
<span data-ttu-id="37f4e-136">DANS</span><span class="sxs-lookup"><span data-stu-id="37f4e-136">"IN "</span></span>  
<span data-ttu-id="37f4e-137">« N S »</span><span class="sxs-lookup"><span data-stu-id="37f4e-137">"N S"</span></span>  
<span data-ttu-id="37f4e-138">SR</span><span class="sxs-lookup"><span data-stu-id="37f4e-138">" SP"</span></span>  
<span data-ttu-id="37f4e-139">Spa</span><span class="sxs-lookup"><span data-stu-id="37f4e-139">"SPA"</span></span>  
<span data-ttu-id="37f4e-140">"PAI"</span><span class="sxs-lookup"><span data-stu-id="37f4e-140">"PAI"</span></span>  
<span data-ttu-id="37f4e-141">Ayn</span><span class="sxs-lookup"><span data-stu-id="37f4e-141">"AIN"</span></span>  
<span data-ttu-id="37f4e-142">« IN \! »</span><span class="sxs-lookup"><span data-stu-id="37f4e-142">"IN\!"</span></span>  
<span data-ttu-id="37f4e-143">« N \! »</span><span class="sxs-lookup"><span data-stu-id="37f4e-143">"N\!"</span></span>

<span data-ttu-id="37f4e-144">Notez que « IN » se produit deux fois, et que la dernière entrée (« N \! ») est plus petite que 3 (**chLengthMax**).</span><span class="sxs-lookup"><span data-stu-id="37f4e-144">Note that "IN " occurs twice, and that the last entry ("N\!") is shorter than 3 (**chLengthMax**).</span></span> <span data-ttu-id="37f4e-145">Notez également que l’algorithme de fractionnement ne tient pas compte des espaces ou des mots et traite tous les caractères de la même façon.</span><span class="sxs-lookup"><span data-stu-id="37f4e-145">Also note that the splitting algorithm is not aware of spaces or words, and treats all characters identically.</span></span>

<span data-ttu-id="37f4e-146">**Windows XP :** Windows XP prend en charge les index de tuple, mais n’a pas de **JET_TUPLELIMITS**.</span><span class="sxs-lookup"><span data-stu-id="37f4e-146">**Windows XP:** Windows XP supports tuple indexes, but does not have **JET_TUPLELIMITS**.</span></span> <span data-ttu-id="37f4e-147">Le moteur de base de données utilisera les valeurs par défaut (**chLengthMin**= 3, **chLengthMax**= 10, **chToIndexMax**= 32767).</span><span class="sxs-lookup"><span data-stu-id="37f4e-147">The database engine will used the default values (**chLengthMin**=3, **chLengthMax**=10, **chToIndexMax**=32767).</span></span> <span data-ttu-id="37f4e-148">Il est toujours possible de modifier ces valeurs, mais elles sont définies en fonction de l’instance à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md) avec [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md)et [JET_paramIndexTuplesToIndexMax](./index-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="37f4e-148">It is still possible to change these values, but they are set on a per-instance basis using [JetSetSystemParameter](./jetsetsystemparameter-function.md) with [JET_paramIndexTuplesLengthMin](./index-parameters.md), [JET_paramIndexTuplesLengthMax](./index-parameters.md), and [JET_paramIndexTuplesToIndexMax](./index-parameters.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="37f4e-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37f4e-149">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37f4e-150"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="37f4e-150"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="37f4e-151">Nécessite Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="37f4e-151">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37f4e-152"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="37f4e-152"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="37f4e-153">Requiert Windows Server 2008, Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="37f4e-153">Requires Windows Server 2008, Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37f4e-154"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="37f4e-154"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="37f4e-155">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="37f4e-155">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="37f4e-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37f4e-156">See Also</span></span>

[<span data-ttu-id="37f4e-157">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="37f4e-157">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="37f4e-158">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="37f4e-158">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="37f4e-159">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="37f4e-159">JET_TUPLELIMITS</span></span>]()  
[<span data-ttu-id="37f4e-160">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="37f4e-160">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
