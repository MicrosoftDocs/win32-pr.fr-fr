---
description: 'En savoir plus sur : structure JET_COLUMNDEF'
title: Structure JET_COLUMNDEF
TOCTitle: JET_COLUMNDEF Structure
ms:assetid: ee1fc473-bff5-438e-98ae-247de12e76f9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294130(v=EXCHG.10)
ms:contentKeyID: 32765744
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
ms.openlocfilehash: c541b5801c95f4b269e33360f5ffa2404ff8fc06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953117"
---
# <a name="jet_columndef-structure"></a><span data-ttu-id="d68ac-103">Structure JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="d68ac-103">JET_COLUMNDEF Structure</span></span>


<span data-ttu-id="d68ac-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="d68ac-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columndef-structure"></a><span data-ttu-id="d68ac-105">Structure JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="d68ac-105">JET_COLUMNDEF Structure</span></span>

<span data-ttu-id="d68ac-106">La structure **JET_COLUMNDEF** définit les données qui peuvent être stockées dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="d68ac-106">The **JET_COLUMNDEF** structure defines the data that can be stored in a column.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wCollate;
      unsigned long cbMax;
      JET_GRBIT grbit;
    } JET_COLUMNDEF;
```

### <a name="members"></a><span data-ttu-id="d68ac-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d68ac-107">Members</span></span>

<span data-ttu-id="d68ac-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="d68ac-108">**cbStruct**</span></span>

<span data-ttu-id="d68ac-109">Taille de la structure en octets.</span><span class="sxs-lookup"><span data-stu-id="d68ac-109">The size of the structure, in bytes.</span></span> <span data-ttu-id="d68ac-110">Elle doit être définie sur sizeof (JET_COLUMNDEF).</span><span class="sxs-lookup"><span data-stu-id="d68ac-110">It must be set to sizeof( JET_COLUMNDEF).</span></span>

<span data-ttu-id="d68ac-111">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="d68ac-111">**columnid**</span></span>

<span data-ttu-id="d68ac-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="d68ac-112">Reserved.</span></span> <span data-ttu-id="d68ac-113">**ColumnID** doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="d68ac-113">**columnid** must be set to 0 (zero).</span></span>

<span data-ttu-id="d68ac-114">**coltyp**</span><span class="sxs-lookup"><span data-stu-id="d68ac-114">**coltyp**</span></span>

<span data-ttu-id="d68ac-115">Type de la colonne (par exemple, texte, binaire ou numérique).</span><span class="sxs-lookup"><span data-stu-id="d68ac-115">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="d68ac-116">Pour plus d’informations, consultez [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d68ac-116">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="d68ac-117">**wCountry**</span><span class="sxs-lookup"><span data-stu-id="d68ac-117">**wCountry**</span></span>

<span data-ttu-id="d68ac-118">Réservé.</span><span class="sxs-lookup"><span data-stu-id="d68ac-118">Reserved.</span></span> <span data-ttu-id="d68ac-119">**wCountry** doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="d68ac-119">**wCountry** must be set to 0 (zero).</span></span>

<span data-ttu-id="d68ac-120">**langid**</span><span class="sxs-lookup"><span data-stu-id="d68ac-120">**langid**</span></span>

<span data-ttu-id="d68ac-121">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="d68ac-121">Obsolete.</span></span> <span data-ttu-id="d68ac-122">**LangID** doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="d68ac-122">**langid** should be set to 0 (zero).</span></span>

<span data-ttu-id="d68ac-123">**cp**</span><span class="sxs-lookup"><span data-stu-id="d68ac-123">**cp**</span></span>

<span data-ttu-id="d68ac-124">Page de codes de la colonne.</span><span class="sxs-lookup"><span data-stu-id="d68ac-124">The code page for the column.</span></span> <span data-ttu-id="d68ac-125">Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="d68ac-125">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="d68ac-126">La valeur zéro signifie que la valeur par défaut sera utilisée (anglais, 1252).</span><span class="sxs-lookup"><span data-stu-id="d68ac-126">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="d68ac-127">Si la colonne n’est pas une colonne de texte, la page de codes est automatiquement définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="d68ac-127">If the column is not a text column, the code page automatically gets set to zero.</span></span>

<span data-ttu-id="d68ac-128">**wCollate**</span><span class="sxs-lookup"><span data-stu-id="d68ac-128">**wCollate**</span></span>

<span data-ttu-id="d68ac-129">Réservé.</span><span class="sxs-lookup"><span data-stu-id="d68ac-129">Reserved.</span></span> <span data-ttu-id="d68ac-130">**wCollate** doit avoir la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="d68ac-130">**wCollate** must be set to 0 (zero).</span></span>

<span data-ttu-id="d68ac-131">**cbMax**</span><span class="sxs-lookup"><span data-stu-id="d68ac-131">**cbMax**</span></span>

<span data-ttu-id="d68ac-132">La longueur maximale, en octets, d’une colonne de longueur variable, ou la longueur d’une colonne de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="d68ac-132">The maximum length, in bytes, of a variable-length column, or the length of a fixed-length column.</span></span>

<span data-ttu-id="d68ac-133">**grbit**</span><span class="sxs-lookup"><span data-stu-id="d68ac-133">**grbit**</span></span>

<span data-ttu-id="d68ac-134">Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro, une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d68ac-134">A group of bits that contain the options to be used for this call, which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d68ac-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="d68ac-135">Value</span></span></p></th>
<th><p><span data-ttu-id="d68ac-136">Signification</span><span class="sxs-lookup"><span data-stu-id="d68ac-136">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d68ac-137">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="d68ac-137">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="d68ac-138">La colonne sera fixe.</span><span class="sxs-lookup"><span data-stu-id="d68ac-138">The column will be fixed.</span></span> <span data-ttu-id="d68ac-139">Elle utilise toujours la même quantité d’espace dans une ligne, quelle que soit la quantité de données stockées dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="d68ac-139">It will always use the same amount of space in a row, regardless of how much data is being stored in the column.</span></span> <span data-ttu-id="d68ac-140">JET_bitColumnFixed ne peut pas être utilisé avec JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="d68ac-140">JET_bitColumnFixed cannot be used with JET_bitColumnTagged.</span></span> <span data-ttu-id="d68ac-141">Ce bit ne peut pas être utilisé avec des valeurs longues ( <strong>JET_coltypLongText</strong> et <strong>JET_coltypLongBinary</strong>).</span><span class="sxs-lookup"><span data-stu-id="d68ac-141">This bit cannot be used with long values (that is <strong>JET_coltypLongText</strong> and <strong>JET_coltypLongBinary</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d68ac-142">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="d68ac-142">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="d68ac-143">La colonne est balisée.</span><span class="sxs-lookup"><span data-stu-id="d68ac-143">The column will be tagged.</span></span> <span data-ttu-id="d68ac-144">Les colonnes avec balises n’occupent pas d’espace dans la base de données si elles ne contiennent pas de données.</span><span class="sxs-lookup"><span data-stu-id="d68ac-144">Tagged columns do not take up any space in the database if they do not contain data.</span></span> <span data-ttu-id="d68ac-145">Ce bit ne peut pas être utilisé avec JET_bitColumnFixed.</span><span class="sxs-lookup"><span data-stu-id="d68ac-145">This bit cannot be used with JET_bitColumnFixed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d68ac-146">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="d68ac-146">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="d68ac-147">La colonne ne doit jamais être définie sur une valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="d68ac-147">The column must never be set to a NULL value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d68ac-148">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="d68ac-148">JET_bitColumnVersion</span></span></p></td>
<td><p><span data-ttu-id="d68ac-149">La colonne est une colonne de version qui spécifie la version de la ligne.</span><span class="sxs-lookup"><span data-stu-id="d68ac-149">The column is a version column that specifies the version of the row.</span></span> <span data-ttu-id="d68ac-150">La valeur de cette colonne commence à zéro et est incrémentée automatiquement pour chaque mise à jour sur la ligne.</span><span class="sxs-lookup"><span data-stu-id="d68ac-150">The value of this column starts at zero and will be automatically incremented for each update on the row.</span></span></p>
<p><span data-ttu-id="d68ac-151">Ce bit ne peut être appliqué qu’à des colonnes <strong>JET_coltypLong</strong> .</span><span class="sxs-lookup"><span data-stu-id="d68ac-151">This bit can only be applied to <strong>JET_coltypLong</strong> columns.</span></span> <span data-ttu-id="d68ac-152">Ce bit ne peut pas être utilisé avec JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate ou JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="d68ac-152">This bit cannot be used with JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, or JET_bitColumnTagged.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d68ac-153">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="d68ac-153">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="d68ac-154">La colonne est automatiquement incrémentée.</span><span class="sxs-lookup"><span data-stu-id="d68ac-154">The column will automatically be incremented.</span></span> <span data-ttu-id="d68ac-155">Le nombre est un nombre plus important et il est garanti qu’il est unique dans une table.</span><span class="sxs-lookup"><span data-stu-id="d68ac-155">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="d68ac-156">Toutefois, les nombres ne peuvent pas être continus.</span><span class="sxs-lookup"><span data-stu-id="d68ac-156">The numbers, however, might not be continuous.</span></span> <span data-ttu-id="d68ac-157">Par exemple, si cinq lignes sont insérées dans une table, &quot; la &quot; colonne AutoIncrement peut contenir les valeurs {1, 2, 6, 7, 8}.</span><span class="sxs-lookup"><span data-stu-id="d68ac-157">For example, if five rows are inserted into a table, the &quot;autoincrement&quot; column could contain the values { 1, 2, 6, 7, 8 }.</span></span> <span data-ttu-id="d68ac-158">Ce bit ne peut être utilisé que sur des colonnes de type <strong>JET_coltypLong</strong> ou <strong>JET_coltypCurrency</strong>.</span><span class="sxs-lookup"><span data-stu-id="d68ac-158">This bit can only be used on columns of type <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong>.</span></span></p>
<p><span data-ttu-id="d68ac-159"><strong>Windows 2000 :  </strong> Dans Windows 2000, ce bit ne peut être utilisé que sur des colonnes de type <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="d68ac-159"><strong>Windows 2000:  </strong>In Windows 2000, this bit can only be used on columns of type <strong>JET_coltypLong</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d68ac-160">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="d68ac-160">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="d68ac-161">Ce bit n’est valide que sur les appels à <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span><span class="sxs-lookup"><span data-stu-id="d68ac-161">This bit is valid only on calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d68ac-162">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="d68ac-162">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="d68ac-163">Ce bit n’est valide que sur les appels à <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span><span class="sxs-lookup"><span data-stu-id="d68ac-163">This bit is valid only on calls to <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d68ac-164">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="d68ac-164">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="d68ac-165">Ce bit n’est valide que sur les appels à <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span><span class="sxs-lookup"><span data-stu-id="d68ac-165">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d68ac-166">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="d68ac-166">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="d68ac-167">La colonne peut être à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="d68ac-167">The column can be multi-valued.</span></span> <span data-ttu-id="d68ac-168">Une colonne à valeurs multiples peut avoir zéro, une ou plusieurs valeurs associées.</span><span class="sxs-lookup"><span data-stu-id="d68ac-168">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="d68ac-169">Les différentes valeurs d’une colonne à valeurs multiples sont identifiées par un nombre appelé le membre <strong>itagSequence</strong> , qui appartient à différentes structures, notamment : <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>et <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="d68ac-169">The various values in a multi-valued column are identified by a number called the <strong>itagSequence</strong> member, which belongs to various structures, including: <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, and <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="d68ac-170">Les colonnes à valeurs multiples doivent être des colonnes avec balises ; autrement dit, ils ne peuvent pas être de longueur fixe ou de colonnes de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="d68ac-170">Multi-valued columns must be tagged columns; that is, they cannot be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d68ac-171">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="d68ac-171">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="d68ac-172">Spécifie qu’une colonne est une colonne de mise à jour de dépôt.</span><span class="sxs-lookup"><span data-stu-id="d68ac-172">Specifies that a column is an escrow update column.</span></span> <span data-ttu-id="d68ac-173">Une colonne de mise à jour de tiers de confiance peut être mise à jour simultanément par différentes sessions avec <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> et assurer la cohérence transactionnelle.</span><span class="sxs-lookup"><span data-stu-id="d68ac-173">An escrow update column can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and will maintain transactional consistency.</span></span> <span data-ttu-id="d68ac-174">Une colonne de mise à jour de dépôt doit également remplir les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="d68ac-174">An escrow update column must also meet the following conditions:</span></span></p>
<ul>
<li><p><span data-ttu-id="d68ac-175">Une colonne de mise à jour de dépôt ne peut être créée que si la table est vide.</span><span class="sxs-lookup"><span data-stu-id="d68ac-175">An escrow update column can be created only when the table is empty.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="d68ac-176">Une colonne de mise à jour de tiers de confiance doit être de type <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="d68ac-176">An escrow update column must be of type <strong>JET_coltypLong</strong>.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="d68ac-177">Une colonne de mise à jour fiduciaire doit avoir une valeur par défaut ( <strong>cbDefault</strong> doit être positive).</span><span class="sxs-lookup"><span data-stu-id="d68ac-177">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="d68ac-178">JET_bitColumnEscrowUpdate ne peut pas être utilisé conjointement avec JET_bitColumnTagged, JET_bitColumnVersion ou JET_bitColumnAutoincrement.</span><span class="sxs-lookup"><span data-stu-id="d68ac-178">JET_bitColumnEscrowUpdate cannot be used in conjunction with JET_bitColumnTagged, JET_bitColumnVersion, or JET_bitColumnAutoincrement.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d68ac-179">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="d68ac-179">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="d68ac-180">La colonne sera créée dans un sans informations sur la version.</span><span class="sxs-lookup"><span data-stu-id="d68ac-180">The column will be created in an without version information.</span></span> <span data-ttu-id="d68ac-181">Cela signifie que les autres transactions qui tentent d’ajouter une colonne portant le même nom échoueront.</span><span class="sxs-lookup"><span data-stu-id="d68ac-181">This means that other transactions that attempt to add a column with the same name will fail.</span></span> <span data-ttu-id="d68ac-182">Ce bit est utile uniquement avec <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span><span class="sxs-lookup"><span data-stu-id="d68ac-182">This bit is only useful with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="d68ac-183">Elle ne peut pas être utilisée dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="d68ac-183">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d68ac-184">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="d68ac-184">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="d68ac-185">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="d68ac-185">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d68ac-186">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="d68ac-186">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="d68ac-187">Utilisez JET_bitColumnDeleteOnZero au lieu de JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="d68ac-187">Use JET_bitColumnDeleteOnZero instead of JET_bitColumnFinalize.</span></span> <span data-ttu-id="d68ac-188">JET_bitColumnFinalize qu’une colonne peut être finalisée.</span><span class="sxs-lookup"><span data-stu-id="d68ac-188">JET_bitColumnFinalize that a column can be finalized.</span></span> <span data-ttu-id="d68ac-189">Lorsqu’une colonne qui peut être finalisée a une colonne de mise à jour de dépôt qui atteint zéro, la ligne est supprimée.</span><span class="sxs-lookup"><span data-stu-id="d68ac-189">When a column that can be finalized has an escrow update column that reaches zero, the row will be deleted.</span></span> <span data-ttu-id="d68ac-190">Les versions ultérieures peuvent appeler une fonction de rappel à la place (pour plus d’informations, consultez <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span><span class="sxs-lookup"><span data-stu-id="d68ac-190">Future versions might invoke a callback function instead (For more information, see <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span></span> <span data-ttu-id="d68ac-191">Une colonne pouvant être finalisée doit être une colonne de mise à jour de tiers de confiance.</span><span class="sxs-lookup"><span data-stu-id="d68ac-191">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="d68ac-192">JET_bitColumnFinalize ne peut pas être utilisé avec JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="d68ac-192">JET_bitColumnFinalize cannot be used with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d68ac-193">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="d68ac-193">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="d68ac-194">La valeur par défaut d’une colonne est fournie par une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="d68ac-194">The default value for a column will be provided by a callback function.</span></span> <span data-ttu-id="d68ac-195">Consultez <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="d68ac-195">See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="d68ac-196">Une colonne qui a une valeur par défaut définie par l’utilisateur doit être une colonne avec balises.</span><span class="sxs-lookup"><span data-stu-id="d68ac-196">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="d68ac-197">Si vous spécifiez JET_bitColumnUserDefinedDefault, <strong>pvDefault</strong> doit pointer vers une structure <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> et <strong>cbDefault</strong> doit avoir la valeur sizeof ( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</span><span class="sxs-lookup"><span data-stu-id="d68ac-197">Specifying JET_bitColumnUserDefinedDefault means that <strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof( <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> ).</span></span></p>
<ul>
<li><p><span data-ttu-id="d68ac-198">JET_bitColumnUserDefinedDefault ne peut pas être utilisé conjointement avec JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero ou JET_bitColumnMaybeNull.</span><span class="sxs-lookup"><span data-stu-id="d68ac-198">JET_bitColumnUserDefinedDefault cannot be used in conjunction with JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero, or JET_bitColumnMaybeNull.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d68ac-199">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="d68ac-199">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="d68ac-200">La colonne est une colonne de mise à jour de dépôt, et lorsqu’elle atteint zéro, l’enregistrement est supprimé.</span><span class="sxs-lookup"><span data-stu-id="d68ac-200">The column is an escrow update column, and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="d68ac-201">Une utilisation courante d’une colonne qui peut être finalisée consiste à l’utiliser comme un champ de décompte de références et, lorsque le champ atteint zéro, l’enregistrement est supprimé.</span><span class="sxs-lookup"><span data-stu-id="d68ac-201">A common use for a column that can be finalized is to use it as a reference count field, and when the field reaches zero the record gets deleted.</span></span> <span data-ttu-id="d68ac-202">JET_bitColumnDeleteOnZero est lié à JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="d68ac-202">JET_bitColumnDeleteOnZero is related to JET_bitColumnFinalize.</span></span> <span data-ttu-id="d68ac-203">Une colonne de suppression sur zéro doit être une colonne de mise à jour de tiers de confiance.</span><span class="sxs-lookup"><span data-stu-id="d68ac-203">A Delete-on-zero column must be an escrow update column.</span></span> <span data-ttu-id="d68ac-204">JET_bitColumnDeleteOnZero ne peut pas être utilisé avec JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="d68ac-204">JET_bitColumnDeleteOnZero cannot be used with JET_bitColumnFinalize.</span></span> <span data-ttu-id="d68ac-205">JET_bitColumnDeleteOnZero ne peut pas être utilisé avec des colonnes par défaut définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d68ac-205">JET_bitColumnDeleteOnZero cannot be used with user defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="d68ac-206">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d68ac-206">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d68ac-207"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d68ac-207"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d68ac-208">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="d68ac-208">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d68ac-209"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="d68ac-209"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d68ac-210">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d68ac-210">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d68ac-211"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="d68ac-211"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d68ac-212">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="d68ac-212">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="d68ac-213">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d68ac-213">See Also</span></span>

[<span data-ttu-id="d68ac-214">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="d68ac-214">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="d68ac-215">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="d68ac-215">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="d68ac-216">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="d68ac-216">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="d68ac-217">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="d68ac-217">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="d68ac-218">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d68ac-218">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d68ac-219">JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="d68ac-219">JET_USERDEFINEDDEFAULT</span></span>](./jet-userdefineddefault-structure.md)  
[<span data-ttu-id="d68ac-220">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="d68ac-220">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="d68ac-221">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="d68ac-221">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)  
[<span data-ttu-id="d68ac-222">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="d68ac-222">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)  
[<span data-ttu-id="d68ac-223">JetOpenTempTable</span><span class="sxs-lookup"><span data-stu-id="d68ac-223">JetOpenTempTable</span></span>](./jetopentemptable-function.md)  
[<span data-ttu-id="d68ac-224">JetOpenTempTable2</span><span class="sxs-lookup"><span data-stu-id="d68ac-224">JetOpenTempTable2</span></span>](./jetopentemptable2-function.md)  
[<span data-ttu-id="d68ac-225">JetOpenTempTable3</span><span class="sxs-lookup"><span data-stu-id="d68ac-225">JetOpenTempTable3</span></span>](./jetopentemptable3-function.md)  
[<span data-ttu-id="d68ac-226">JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="d68ac-226">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)
