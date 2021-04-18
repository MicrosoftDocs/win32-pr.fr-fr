---
description: 'En savoir plus sur : structure JET_COLUMNBASE'
title: Structure JET_COLUMNBASE
TOCTitle: JET_COLUMNBASE Structure
ms:assetid: 171275c3-966d-409d-ad20-a8f240f7500d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269194(v=EXCHG.10)
ms:contentKeyID: 32765497
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
ms.openlocfilehash: 9276c36a08a429f44568b3a909af77f5ae038c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523047"
---
# <a name="jet_columnbase-structure"></a><span data-ttu-id="2de11-103">Structure JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="2de11-103">JET_COLUMNBASE Structure</span></span>


<span data-ttu-id="2de11-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="2de11-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columnbase-structure"></a><span data-ttu-id="2de11-105">Structure JET_COLUMNBASE</span><span class="sxs-lookup"><span data-stu-id="2de11-105">JET_COLUMNBASE Structure</span></span>

<span data-ttu-id="2de11-106">La structure **JET_COLUMNBASE** décrit les paramètres d’une colonne de base.</span><span class="sxs-lookup"><span data-stu-id="2de11-106">The **JET_COLUMNBASE** structure describes the parameters of a base column.</span></span> <span data-ttu-id="2de11-107">Les fonctions [JetGetColumnInfo](./jetgetcolumninfo-function.md) et [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) utilisent la structure **JET_COLUMNBASE** .</span><span class="sxs-lookup"><span data-stu-id="2de11-107">The [JetGetColumnInfo](./jetgetcolumninfo-function.md) and [JetGetTableColumnInfo](./jetgettablecolumninfo-function.md) functions use the **JET_COLUMNBASE** structure.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_COLUMNID columnid;
      JET_COLTYP coltyp;
      unsigned short wCountry;
      unsigned short langid;
      unsigned short cp;
      unsigned short wFiller;
      unsigned long cbMax;
      JET_GRBIT grbit;
      tchar szBaseTableName[256];
      tchar szBaseColumnName[256];
    } JET_COLUMNBASE;
```

### <a name="members"></a><span data-ttu-id="2de11-108">Membres</span><span class="sxs-lookup"><span data-stu-id="2de11-108">Members</span></span>

<span data-ttu-id="2de11-109">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="2de11-109">**cbStruct**</span></span>

<span data-ttu-id="2de11-110">Taille de cette structure, en octets.</span><span class="sxs-lookup"><span data-stu-id="2de11-110">The size of this structure, in bytes.</span></span> <span data-ttu-id="2de11-111">Affectez à **cbStruct** la valeur sizeof (JET_COLUMNBASE).</span><span class="sxs-lookup"><span data-stu-id="2de11-111">Set **cbStruct** to sizeof( JET_COLUMNBASE ).</span></span>

<span data-ttu-id="2de11-112">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="2de11-112">**columnid**</span></span>

<span data-ttu-id="2de11-113">Réservé.</span><span class="sxs-lookup"><span data-stu-id="2de11-113">Reserved.</span></span> <span data-ttu-id="2de11-114">Affectez à **ColumnID** la valeur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="2de11-114">Set **columnid** to 0 (zero).</span></span>

<span data-ttu-id="2de11-115">**coltyp**</span><span class="sxs-lookup"><span data-stu-id="2de11-115">**coltyp**</span></span>

<span data-ttu-id="2de11-116">Type de la colonne (par exemple, texte, binaire ou numérique).</span><span class="sxs-lookup"><span data-stu-id="2de11-116">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="2de11-117">Pour plus d’informations, consultez [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="2de11-117">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="2de11-118">**wCountry**</span><span class="sxs-lookup"><span data-stu-id="2de11-118">**wCountry**</span></span>

<span data-ttu-id="2de11-119">Réservé.</span><span class="sxs-lookup"><span data-stu-id="2de11-119">Reserved.</span></span> <span data-ttu-id="2de11-120">Défini sur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="2de11-120">Set to 0 (zero).</span></span>

<span data-ttu-id="2de11-121">**langid**</span><span class="sxs-lookup"><span data-stu-id="2de11-121">**langid**</span></span>

<span data-ttu-id="2de11-122">Réservé.</span><span class="sxs-lookup"><span data-stu-id="2de11-122">Reserved.</span></span> <span data-ttu-id="2de11-123">Défini sur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="2de11-123">Set to 0 (zero).</span></span>

<span data-ttu-id="2de11-124">**cp**</span><span class="sxs-lookup"><span data-stu-id="2de11-124">**cp**</span></span>

<span data-ttu-id="2de11-125">Page de codes de la colonne.</span><span class="sxs-lookup"><span data-stu-id="2de11-125">The code page for the column.</span></span> <span data-ttu-id="2de11-126">Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="2de11-126">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="2de11-127">La valeur zéro signifie que la valeur par défaut sera utilisée (anglais, 1252).</span><span class="sxs-lookup"><span data-stu-id="2de11-127">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="2de11-128">Si la colonne n’est pas une colonne de texte, la page de codes est automatiquement définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="2de11-128">If the column is not a text column, the code page is automatically set to zero.</span></span>

<span data-ttu-id="2de11-129">**wFiller**</span><span class="sxs-lookup"><span data-stu-id="2de11-129">**wFiller**</span></span>

<span data-ttu-id="2de11-130">Réservé.</span><span class="sxs-lookup"><span data-stu-id="2de11-130">Reserved.</span></span> <span data-ttu-id="2de11-131">Défini sur 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="2de11-131">Set to 0 (zero).</span></span>

<span data-ttu-id="2de11-132">**cbMax**</span><span class="sxs-lookup"><span data-stu-id="2de11-132">**cbMax**</span></span>

<span data-ttu-id="2de11-133">Longueur maximale, en octets, d’une colonne de longueur variable, ou longueur réelle, en octets, d’une colonne de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="2de11-133">The maximum length, in bytes, of a variable-length column, or the actual length, in bytes, of a fixed-length column.</span></span>

<span data-ttu-id="2de11-134">**grbit**</span><span class="sxs-lookup"><span data-stu-id="2de11-134">**grbit**</span></span>

<span data-ttu-id="2de11-135">Options de la colonne, y compris zéro, une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="2de11-135">Options for the column, including zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2de11-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="2de11-136">Value</span></span></p></th>
<th><p><span data-ttu-id="2de11-137">Signification</span><span class="sxs-lookup"><span data-stu-id="2de11-137">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2de11-138">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="2de11-138">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="2de11-139">La colonne est fixe et occupe la même quantité d’espace dans une ligne, quelle que soit la quantité de données qu’elle contient.</span><span class="sxs-lookup"><span data-stu-id="2de11-139">The column is fixed and occupies the same amount of space in a row regardless of how much data it contains.</span></span> <span data-ttu-id="2de11-140">JET_bitColumnFixed ne peut pas être combiné avec JET_bitColumnTagged et ne peut pas être utilisé lorsque le membre <strong>coltyp</strong> a la valeur <strong>JET_coltypLongText</strong> ou <strong>JET_coltypLongBinary</strong>.</span><span class="sxs-lookup"><span data-stu-id="2de11-140">JET_bitColumnFixed cannot be combined with JET_bitColumnTagged, and cannot be used when the <strong>coltyp</strong> member is set to <strong>JET_coltypLongText</strong> or <strong>JET_coltypLongBinary</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2de11-141">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="2de11-141">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="2de11-142">La colonne est balisée et occupe de l’espace dans la base de données uniquement si elle contient des données.</span><span class="sxs-lookup"><span data-stu-id="2de11-142">The column is tagged and occupies space in the database only if it contains data.</span></span> <span data-ttu-id="2de11-143">JET_bitColumnTagged ne peut pas être combiné avec JET_bitColumnFixed, JET_bitColumnVersion ou JET_bitColumnEscrowUpdate.</span><span class="sxs-lookup"><span data-stu-id="2de11-143">JET_bitColumnTagged cannot be combined with JET_bitColumnFixed, JET_bitColumnVersion, or JET_bitColumnEscrowUpdate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2de11-144">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="2de11-144">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="2de11-145">La colonne ne doit pas être définie sur une valeur <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="2de11-145">The column must not be set to a <strong>NULL</strong> value.</span></span></p>
<p><span data-ttu-id="2de11-146">JET_bitColumnNotNULL ne peut pas être combiné avec JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="2de11-146">JET_bitColumnNotNULL cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2de11-147">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="2de11-147">JET_bitColumnVersion</span></span></p></td>
<td><p><span data-ttu-id="2de11-148">La colonne est une colonne de version qui spécifie la version de la ligne.</span><span class="sxs-lookup"><span data-stu-id="2de11-148">The column is a version column that specifies the version of the row.</span></span> <span data-ttu-id="2de11-149">La valeur de cette colonne commence à zéro et est incrémentée automatiquement pour chaque mise à jour de la ligne.</span><span class="sxs-lookup"><span data-stu-id="2de11-149">The value of this column starts at zero and is automatically incremented for each update of the row.</span></span></p>
<p><span data-ttu-id="2de11-150">JET_bitColumnVersion peut être utilisé uniquement lorsque le membre <strong>coltyp</strong> est défini sur <strong>JET_coltypLong</strong> et ne peut pas être combiné avec JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged ou JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="2de11-150">JET_bitColumnVersion can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong> and cannot be combined with JET_bitColumnAutoincrement, JET_bitColumnEscrowUpdate, JET_bitColumnTagged, or JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2de11-151">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="2de11-151">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="2de11-152">La colonne est incrémentée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="2de11-152">The column is automatically incremented.</span></span> <span data-ttu-id="2de11-153">Le nombre est un nombre plus important et il est garanti qu’il est unique dans une table.</span><span class="sxs-lookup"><span data-stu-id="2de11-153">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="2de11-154">Toutefois, les nombres ne peuvent pas être séquentiels.</span><span class="sxs-lookup"><span data-stu-id="2de11-154">The numbers, however, may not be sequential.</span></span> <span data-ttu-id="2de11-155">Par exemple, si cinq lignes sont insérées dans une table, la colonne incrémentée automatiquement peut contenir les valeurs {1, 2, 6, 7, 8}.</span><span class="sxs-lookup"><span data-stu-id="2de11-155">For example, if five rows are inserted into a table, the automatically incremented column could contain the values { 1, 2, 6, 7, 8 }.</span></span></p>
<p><span data-ttu-id="2de11-156">JET_bitColumnAutoincrement peut être utilisé uniquement lorsque le membre <strong>coltyp</strong> est défini sur <strong>JET_coltypLong</strong> ou <strong>JET_coltypCurrency</strong> et ne peut pas être combiné avec JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault ou JET_bitColumnVersion.</span><span class="sxs-lookup"><span data-stu-id="2de11-156">JET_bitColumnAutoincrement can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong> and cannot be combined with JET_bitColumnEscrowUpdate, JET_bitColumnUserDefinedDefault, or JET_bitColumnVersion.</span></span></p>
<p><span data-ttu-id="2de11-157"><strong>Windows 2000 :  </strong> JET_bitColumnVersion peut être utilisé uniquement lorsque le membre <strong>coltyp</strong> est défini sur <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="2de11-157"><strong>Windows 2000:  </strong>JET_bitColumnVersion can be used only when the <strong>coltyp</strong> member is set to <strong>JET_coltypLong</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2de11-158">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="2de11-158">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="2de11-159">Valide uniquement pour les appels à <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span><span class="sxs-lookup"><span data-stu-id="2de11-159">Valid only for calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span> <span data-ttu-id="2de11-160">JET_bitColumnUpdatable ne peut pas être combiné avec JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="2de11-160">JET_bitColumnUpdatable cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2de11-161">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="2de11-161">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="2de11-162">Valide uniquement sur les appels à <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span><span class="sxs-lookup"><span data-stu-id="2de11-162">Valid only on calls to <a href="gg294118(v=exchg.10).md">JetOpenTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2de11-163">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="2de11-163">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="2de11-164">Valide uniquement sur les appels à <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span><span class="sxs-lookup"><span data-stu-id="2de11-164">Valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2de11-165">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="2de11-165">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="2de11-166">La colonne peut être à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="2de11-166">The column can be multi-valued.</span></span> <span data-ttu-id="2de11-167">Une colonne à valeurs multiples peut avoir zéro, une ou plusieurs valeurs associées.</span><span class="sxs-lookup"><span data-stu-id="2de11-167">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="2de11-168">Les différentes valeurs d’une colonne à valeurs multiples sont identifiées par un nombre dans le membre <strong>itagSequence</strong> de différentes structures, par exemple, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="2de11-168">The various values in a multi-valued column are identified by a number in the <strong>itagSequence</strong> member of various structures, for example, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="2de11-169">Les colonnes à valeurs multiples doivent être des colonnes avec balises ; autrement dit, ils ne peuvent pas être de longueur fixe ou de colonnes de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="2de11-169">Multi-valued columns must be tagged columns; that is, they may not be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2de11-170">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="2de11-170">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="2de11-171">Spécifie qu’une colonne est une colonne de mise à jour de dépôt qui peut être mise à jour simultanément par différentes sessions avec <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> et qui aura une cohérence transactionnelle.</span><span class="sxs-lookup"><span data-stu-id="2de11-171">Specifies that a column is an escrow update column that can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and will have transactional consistency.</span></span></p>
<ul>
<li><p><span data-ttu-id="2de11-172">Une colonne de mise à jour de dépôt ne peut être créée que si la table est vide.</span><span class="sxs-lookup"><span data-stu-id="2de11-172">An escrow update column can be created only when the table is empty.</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="2de11-173">Pour une colonne de mise à jour de dépôt, le membre <strong>coltyp</strong> doit être défini sur <strong>JET_coltypLong.</strong></span><span class="sxs-lookup"><span data-stu-id="2de11-173">For an escrow update column, the <strong>coltyp</strong> member must be set to <strong>JET_coltypLong.</strong></span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="2de11-174">Une colonne de mise à jour fiduciaire doit avoir une valeur par défaut ( <strong>cbDefault</strong> doit être positive).</span><span class="sxs-lookup"><span data-stu-id="2de11-174">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
</ul>
<ul>
<li><p><span data-ttu-id="2de11-175">JET_bitColumnEscrowUpdate ne peut pas être combiné avec JET_bitColumnTagged, JET_bitColumnVersion ou JET_bitColumnAutoincrement.</span><span class="sxs-lookup"><span data-stu-id="2de11-175">JET_bitColumnEscrowUpdate cannot be combined with JET_bitColumnTagged, JET_bitColumnVersion, or JET_bitColumnAutoincrement.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2de11-176">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="2de11-176">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="2de11-177">La colonne est créée sans numéro de version.</span><span class="sxs-lookup"><span data-stu-id="2de11-177">The column is created without a version number.</span></span> <span data-ttu-id="2de11-178">Cela signifie que les autres transactions tentant d’ajouter une colonne portant le même nom échoueront.</span><span class="sxs-lookup"><span data-stu-id="2de11-178">This means that other transactions attempting to add a column with the same name will fail.</span></span> <span data-ttu-id="2de11-179">JET_bitColumnUnversioned est utilisé uniquement avec <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span><span class="sxs-lookup"><span data-stu-id="2de11-179">JET_bitColumnUnversioned is used only with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="2de11-180">Elle ne peut pas être utilisée dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="2de11-180">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2de11-181">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="2de11-181">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="2de11-182">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="2de11-182">Reserved for future use.</span></span></p>
<p><span data-ttu-id="2de11-183">JET_bitColumnMaybeNull ne peut pas être combiné avec JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="2de11-183">JET_bitColumnMaybeNull cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2de11-184">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="2de11-184">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="2de11-185">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="2de11-185">Do not use.</span></span> <span data-ttu-id="2de11-186">Utilisez à la place JET_bitColumnDeleteOnZero.</span><span class="sxs-lookup"><span data-stu-id="2de11-186">Use JET_bitColumnDeleteOnZero instead.</span></span></p>
<p><span data-ttu-id="2de11-187">La colonne peut être finalisée.</span><span class="sxs-lookup"><span data-stu-id="2de11-187">The column can be finalized.</span></span> <span data-ttu-id="2de11-188">Une colonne qui peut être finalisée est une colonne de mise à jour de dépôt qui provoque la suppression de la ligne lorsque la colonne atteint zéro.</span><span class="sxs-lookup"><span data-stu-id="2de11-188">A column that can be finalized is an escrow update column that causes the row to be deleted when the column reaches zero.</span></span> <span data-ttu-id="2de11-189">Les versions ultérieures peuvent appeler une fonction de rappel à la place (voir <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span><span class="sxs-lookup"><span data-stu-id="2de11-189">Future versions may invoke a callback function instead (See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>).</span></span> <span data-ttu-id="2de11-190">Une colonne pouvant être finalisée doit être une colonne de mise à jour de tiers de confiance.</span><span class="sxs-lookup"><span data-stu-id="2de11-190">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="2de11-191">JET_bitColumnFinalize ne peut pas être combiné avec JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="2de11-191">JET_bitColumnFinalize cannot be combined with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2de11-192">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="2de11-192">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="2de11-193">La valeur par défaut d’une colonne est fournie par une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="2de11-193">The default value for a column will be provided by a callback function.</span></span> <span data-ttu-id="2de11-194">Consultez <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="2de11-194">See <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="2de11-195">Une colonne qui a une valeur par défaut définie par l’utilisateur doit être une colonne avec balises.</span><span class="sxs-lookup"><span data-stu-id="2de11-195">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="2de11-196">Si JET_bitColumnUserDefinedDefault est spécifié, <strong>pvDefault</strong> doit pointer vers une structure <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> et <strong>cbDefault</strong> doit avoir la valeur sizeof (JET_USERDEFINEDDEFAULT).</span><span class="sxs-lookup"><span data-stu-id="2de11-196">If JET_bitColumnUserDefinedDefault is specified, the <strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof( JET_USERDEFINEDDEFAULT ).</span></span></p>
<p><span data-ttu-id="2de11-197">JET_bitColumnUserDefinedDefault ne peut pas être combiné avec JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero ou JET_bitColumnMaybeNull.</span><span class="sxs-lookup"><span data-stu-id="2de11-197">JET_bitColumnUserDefinedDefault cannot be combined with JET_bitColumnFixed, JET_bitColumnNotNULL, JET_bitColumnVersion, JET_bitColumnAutoincrement, JET_bitColumnUpdatable, JET_bitColumnEscrowUpdate, JET_bitColumnFinalize, JET_bitColumnDeleteOnZero, or JET_bitColumnMaybeNull.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2de11-198">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="2de11-198">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="2de11-199">La colonne est une colonne de mise à jour de dépôt et lorsqu’elle atteint zéro, l’enregistrement est supprimé.</span><span class="sxs-lookup"><span data-stu-id="2de11-199">The column is an escrow update column and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="2de11-200">Les champs de décompte de références sont couramment utilisés pour les colonnes de suppression sur zéro.</span><span class="sxs-lookup"><span data-stu-id="2de11-200">A common use for delete-on-zero columns is as reference count fields.</span></span> <span data-ttu-id="2de11-201">Lorsque le nombre de références est égal à zéro, l’enregistrement est supprimé.</span><span class="sxs-lookup"><span data-stu-id="2de11-201">When the number of references fall to zero, the record is deleted.</span></span> <span data-ttu-id="2de11-202">Une colonne de suppression sur zéro doit être une colonne de mise à jour de tiers de confiance.</span><span class="sxs-lookup"><span data-stu-id="2de11-202">A delete-on-zero column must be an escrow update column.</span></span></p>
<p><span data-ttu-id="2de11-203">JET_bitColumnDeleteOnZero remplace JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="2de11-203">JET_bitColumnDeleteOnZero replaces JET_bitColumnFinalize.</span></span></p>
<p><span data-ttu-id="2de11-204">JET_bitColumnDeleteOnZero ne peut pas être combiné avec JET_bitColumnFinalize ou JET_bitColumnUserDefinedDefault, et ne peut pas être utilisé avec des colonnes par défaut définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2de11-204">JET_bitColumnDeleteOnZero cannot be combined with JET_bitColumnFinalize or JET_bitColumnUserDefinedDefault, and cannot be used with user-defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2de11-205">**szBaseTableName**</span><span class="sxs-lookup"><span data-stu-id="2de11-205">**szBaseTableName**</span></span>

<span data-ttu-id="2de11-206">Table à partir de laquelle la table actuelle hérite de son DDL.</span><span class="sxs-lookup"><span data-stu-id="2de11-206">The table from which the current table inherits its DDL.</span></span>

<span data-ttu-id="2de11-207">**szBaseColumnName**</span><span class="sxs-lookup"><span data-stu-id="2de11-207">**szBaseColumnName**</span></span>

<span data-ttu-id="2de11-208">Nom de la colonne dans la table de modèle.</span><span class="sxs-lookup"><span data-stu-id="2de11-208">The name of the column in the template table.</span></span>

### <a name="remarks"></a><span data-ttu-id="2de11-209">Notes</span><span class="sxs-lookup"><span data-stu-id="2de11-209">Remarks</span></span>

<span data-ttu-id="2de11-210">**JET_COLUMNBASE** contient une grande partie des mêmes informations que [JET_COLUMNDEF](./jet-columndef-structure.md), mais il ajoute des champs de chaîne pour décrire la table de base (si une DDL hiérarchique a été utilisée).</span><span class="sxs-lookup"><span data-stu-id="2de11-210">**JET_COLUMNBASE** contains much of the same information as [JET_COLUMNDEF](./jet-columndef-structure.md), but it adds string fields to describe the base table (if a hierarchical DDL was used).</span></span>

### <a name="requirements"></a><span data-ttu-id="2de11-211">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2de11-211">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2de11-212"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2de11-212"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2de11-213">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="2de11-213">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2de11-214"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="2de11-214"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2de11-215">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2de11-215">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2de11-216"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="2de11-216"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2de11-217">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="2de11-217">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2de11-218"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="2de11-218"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="2de11-219">Implémenté comme <strong>JET_COLUMNBASE_W</strong> (Unicode) et <strong>JET_COLUMNBASE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="2de11-219">Implemented as <strong>JET_COLUMNBASE_W</strong> (Unicode) and <strong>JET_COLUMNBASE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="2de11-220">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2de11-220">See Also</span></span>

[<span data-ttu-id="2de11-221">JET_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="2de11-221">JET_CALLBACK</span></span>](./jet-callback-callback-function.md)  
[<span data-ttu-id="2de11-222">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="2de11-222">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="2de11-223">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="2de11-223">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="2de11-224">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="2de11-224">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="2de11-225">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="2de11-225">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="2de11-226">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="2de11-226">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="2de11-227">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="2de11-227">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="2de11-228">JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="2de11-228">JET_USERDEFINEDDEFAULT</span></span>](./jet-userdefineddefault-structure.md)  
[<span data-ttu-id="2de11-229">JetGetColumnInfo</span><span class="sxs-lookup"><span data-stu-id="2de11-229">JetGetColumnInfo</span></span>](./jetgetcolumninfo-function.md)  
[<span data-ttu-id="2de11-230">JetGetTableColumnInfo</span><span class="sxs-lookup"><span data-stu-id="2de11-230">JetGetTableColumnInfo</span></span>](./jetgettablecolumninfo-function.md)  
[<span data-ttu-id="2de11-231">JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="2de11-231">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)
