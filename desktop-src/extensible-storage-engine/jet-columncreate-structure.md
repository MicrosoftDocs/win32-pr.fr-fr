---
description: 'En savoir plus sur : structure JET_COLUMNCREATE'
title: Structure JET_COLUMNCREATE
TOCTitle: JET_COLUMNCREATE Structure
ms:assetid: 553263a9-7d2c-4bd7-ad77-1dfb6d21ef2c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269252(v=EXCHG.10)
ms:contentKeyID: 32765554
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
ms.openlocfilehash: ee2d9d194a03cf575eb0296163526c1c50301cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528240"
---
# <a name="jet_columncreate-structure"></a><span data-ttu-id="d52ed-103">Structure JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="d52ed-103">JET_COLUMNCREATE Structure</span></span>


<span data-ttu-id="d52ed-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="d52ed-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columncreate-structure"></a><span data-ttu-id="d52ed-105">Structure JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="d52ed-105">JET_COLUMNCREATE Structure</span></span>

<span data-ttu-id="d52ed-106">La structure **JET_COLUMNCREATE** décrit une colonne à créer dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="d52ed-106">The **JET_COLUMNCREATE** structure describes a column to create in a database.</span></span>

```cpp
    typedef struct tag_JET_COLUMNCREATE {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_COLTYP coltyp;
      unsigned long cbMax;
      JET_GRBIT grbit;
      void* pvDefault;
      unsigned long cbDefault;
      unsigned long cp;
      JET_COLUMNID columnid;
      JET_ERR err;
    } JET_COLUMNCREATE;
```

### <a name="members"></a><span data-ttu-id="d52ed-107">Membres</span><span class="sxs-lookup"><span data-stu-id="d52ed-107">Members</span></span>

<span data-ttu-id="d52ed-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="d52ed-108">**cbStruct**</span></span>

<span data-ttu-id="d52ed-109">Taille de la structure en octets.</span><span class="sxs-lookup"><span data-stu-id="d52ed-109">The size of the structure, in bytes.</span></span> <span data-ttu-id="d52ed-110">Ce champ doit être initialisé à **sizeof (JET_COLUMNCREATE)**.</span><span class="sxs-lookup"><span data-stu-id="d52ed-110">This field must be initialized to **sizeof( JET_COLUMNCREATE )**.</span></span>

<span data-ttu-id="d52ed-111">**szColumnName**</span><span class="sxs-lookup"><span data-stu-id="d52ed-111">**szColumnName**</span></span>

<span data-ttu-id="d52ed-112">Nom de la colonne à créer.</span><span class="sxs-lookup"><span data-stu-id="d52ed-112">The name of the column to create.</span></span> <span data-ttu-id="d52ed-113">Le nom doit respecter les critères suivants :</span><span class="sxs-lookup"><span data-stu-id="d52ed-113">The name must meet the following criteria:</span></span>

  - <span data-ttu-id="d52ed-114">Sa longueur doit être inférieure à JET_cbNameMost caractères, à l’exclusion de la valeur NULL de fin.</span><span class="sxs-lookup"><span data-stu-id="d52ed-114">It must be fewer than JET_cbNameMost characters in length, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="d52ed-115">Il ne doit contenir que des caractères provenant des jeux suivants : de 0 à 9, de A à Z, de a à z et toutes les autres signes de ponctuation, à l’exception du point d’exclamation ( \! ), de la virgule (,), du crochet ouvrant ( \[ ) et du crochet fermant ( \] ), c’est-À-dire des caractères ASCII 0x20, 0X22 à 0x2D, 0x2F à 0x5A, 0x5c,</span><span class="sxs-lookup"><span data-stu-id="d52ed-115">It must contain characters only from the following sets: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="d52ed-116">Il ne peut pas commencer par un espace.</span><span class="sxs-lookup"><span data-stu-id="d52ed-116">It cannot begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="d52ed-117">Il doit contenir au moins un caractère autre qu’un espace.</span><span class="sxs-lookup"><span data-stu-id="d52ed-117">It must contain at least one non-space character.</span></span>

<span data-ttu-id="d52ed-118">**coltyp**</span><span class="sxs-lookup"><span data-stu-id="d52ed-118">**coltyp**</span></span>

<span data-ttu-id="d52ed-119">Type de la colonne (par exemple, texte, binaire ou numérique).</span><span class="sxs-lookup"><span data-stu-id="d52ed-119">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="d52ed-120">Pour plus d’informations, consultez [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="d52ed-120">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="d52ed-121">**cbMax**</span><span class="sxs-lookup"><span data-stu-id="d52ed-121">**cbMax**</span></span>

<span data-ttu-id="d52ed-122">Longueur maximale, en octets, d’une colonne de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="d52ed-122">The maximum length, in bytes, of a variable-length column.</span></span> <span data-ttu-id="d52ed-123">Longueur de la colonne pour les colonnes de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="d52ed-123">The length of the column for fixed-length columns.</span></span>

<span data-ttu-id="d52ed-124">**grbit**</span><span class="sxs-lookup"><span data-stu-id="d52ed-124">**grbit**</span></span>

<span data-ttu-id="d52ed-125">Groupe de bits qui contiennent les options pour cette structure, et qui incluent zéro, une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d52ed-125">A group of bits that contain the options for this structure, and which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d52ed-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="d52ed-126">Value</span></span></p></th>
<th><p><span data-ttu-id="d52ed-127">Signification</span><span class="sxs-lookup"><span data-stu-id="d52ed-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d52ed-128">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="d52ed-128">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="d52ed-129">La colonne est fixe.</span><span class="sxs-lookup"><span data-stu-id="d52ed-129">The column is fixed.</span></span> <span data-ttu-id="d52ed-130">Elle utilise toujours la même quantité d’espace dans une ligne, quelle que soit la quantité de données stockées dans la colonne.</span><span class="sxs-lookup"><span data-stu-id="d52ed-130">It will always use the same amount of space in a row, regardless of how much data is being stored in the column.</span></span> <span data-ttu-id="d52ed-131">JET_bitColumnFixed ne peut pas être utilisé avec JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="d52ed-131">JET_bitColumnFixed cannot be used with JET_bitColumnTagged.</span></span> <span data-ttu-id="d52ed-132">Ce bit ne peut pas être utilisé avec des valeurs longues, telles que <strong>JET_coltypLongText</strong> et <strong>JET_coltypLongBinary</strong>.</span><span class="sxs-lookup"><span data-stu-id="d52ed-132">This bit cannot be used with long values such as <strong>JET_coltypLongText</strong> and <strong>JET_coltypLongBinary</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d52ed-133">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="d52ed-133">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="d52ed-134">La colonne est balisée.</span><span class="sxs-lookup"><span data-stu-id="d52ed-134">The column is tagged.</span></span> <span data-ttu-id="d52ed-135">Les colonnes avec balises n’occupent pas d’espace dans la base de données si elles ne contiennent pas de données.</span><span class="sxs-lookup"><span data-stu-id="d52ed-135">Tagged columns do not take up any space in the database if they do not contain data.</span></span> <span data-ttu-id="d52ed-136">Ce bit ne peut pas être utilisé avec JET_bitColumnFixed.</span><span class="sxs-lookup"><span data-stu-id="d52ed-136">This bit cannot be used with JET_bitColumnFixed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d52ed-137">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="d52ed-137">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="d52ed-138">La colonne ne doit jamais être définie sur une valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="d52ed-138">The column must never be set to a NULL value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d52ed-139">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="d52ed-139">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="d52ed-140">La colonne est incrémentée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="d52ed-140">The column is automatically incremented.</span></span> <span data-ttu-id="d52ed-141">Le nombre est un nombre plus important et il est garanti qu’il est unique dans une table.</span><span class="sxs-lookup"><span data-stu-id="d52ed-141">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="d52ed-142">Toutefois, le nombre ne peut pas être continu.</span><span class="sxs-lookup"><span data-stu-id="d52ed-142">The number, however, might not be continuous.</span></span> <span data-ttu-id="d52ed-143">Par exemple, si cinq lignes sont insérées dans une table, la colonne AutoIncrement peut contenir les valeurs {1, 2, 6, 7, 8}.</span><span class="sxs-lookup"><span data-stu-id="d52ed-143">For example, if five rows are inserted into a table, the autoincrement column could contain the values { 1, 2, 6, 7, 8 }.</span></span></p>
<p><span data-ttu-id="d52ed-144"><strong>Windows 2000 :  </strong> Ce bit ne peut être utilisé que sur des colonnes de type <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="d52ed-144"><strong>Windows 2000:  </strong>This bit can be used only on columns of type <strong>JET_coltypLong</strong>.</span></span></p>
<p><span data-ttu-id="d52ed-145"><strong>Windows Server 2003 et versions ultérieures :  </strong> Ce bit ne peut être utilisé que sur des colonnes de type <strong>JET_coltypLong</strong> ou <strong>JET_coltypCurrency</strong>.</span><span class="sxs-lookup"><span data-stu-id="d52ed-145"><strong>Windows Server 2003 and later:  </strong>This bit can only be used on columns of type <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d52ed-146">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="d52ed-146">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="d52ed-147">Ce bit n’est valide que sur les appels à <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span><span class="sxs-lookup"><span data-stu-id="d52ed-147">This bit is valid only on calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d52ed-148">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="d52ed-148">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="d52ed-149">Ce bit n’est valide que sur les appels à <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span><span class="sxs-lookup"><span data-stu-id="d52ed-149">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d52ed-150">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="d52ed-150">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="d52ed-151">Ce bit n’est valide que sur les appels à <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span><span class="sxs-lookup"><span data-stu-id="d52ed-151">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d52ed-152">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="d52ed-152">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="d52ed-153">La colonne peut être à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="d52ed-153">The column can be multi-valued.</span></span> <span data-ttu-id="d52ed-154">Une colonne à valeurs multiples peut avoir zéro, une ou plusieurs valeurs associées.</span><span class="sxs-lookup"><span data-stu-id="d52ed-154">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="d52ed-155">Les différentes valeurs d’une colonne à valeurs multiples sont identifiées par le membre <strong>itagSequence</strong> de différentes structures, par exemple, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="d52ed-155">The various values in a multi-valued column are identified by the <strong>itagSequence</strong> member of various structures, for example, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="d52ed-156">Les colonnes à valeurs multiples doivent être des colonnes avec balises ; autrement dit, ils ne peuvent pas être de longueur fixe ou de colonnes de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="d52ed-156">Multi-valued columns must be tagged columns; that is, they cannot be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d52ed-157">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="d52ed-157">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="d52ed-158">La colonne est une colonne de mise à jour du tiers de confiance.</span><span class="sxs-lookup"><span data-stu-id="d52ed-158">The column is an escrow update column.</span></span> <span data-ttu-id="d52ed-159">Une colonne de mise à jour de tiers de confiance peut être mise à jour simultanément par différentes sessions avec <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> et maintenir la cohérence transactionnelle.</span><span class="sxs-lookup"><span data-stu-id="d52ed-159">An escrow update column can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and maintain transactional consistency.</span></span></p>
<ul>
<li><p><span data-ttu-id="d52ed-160">Une colonne de mise à jour de dépôt ne peut être créée que si la table est vide.</span><span class="sxs-lookup"><span data-stu-id="d52ed-160">An escrow update column can be created only when the table is empty.</span></span></p></li>
<li><p><span data-ttu-id="d52ed-161">Une colonne de mise à jour de tiers de confiance doit être de type <strong>JET_coltypLong.</strong></span><span class="sxs-lookup"><span data-stu-id="d52ed-161">An escrow update column must be of type <strong>JET_coltypLong.</strong></span></span></p></li>
<li><p><span data-ttu-id="d52ed-162">Une colonne de mise à jour fiduciaire doit avoir une valeur par défaut ( <strong>cbDefault</strong> doit être positive).</span><span class="sxs-lookup"><span data-stu-id="d52ed-162">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
<li><p><span data-ttu-id="d52ed-163">JET_bitColumnEscrowUpdate ne peut pas être utilisé conjointement avec les constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d52ed-163">JET_bitColumnEscrowUpdate cannot be used in conjunction with the following constants:</span></span></p>
<ul>
<li><p><span data-ttu-id="d52ed-164">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="d52ed-164">JET_bitColumnTagged</span></span></p></li>
<li><p><span data-ttu-id="d52ed-165">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="d52ed-165">JET_bitColumnVersion</span></span></p></li>
<li><p><span data-ttu-id="d52ed-166">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="d52ed-166">JET_bitColumnAutoincrement</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d52ed-167">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="d52ed-167">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="d52ed-168">La colonne est créée sans version.</span><span class="sxs-lookup"><span data-stu-id="d52ed-168">The column is created without a version.</span></span> <span data-ttu-id="d52ed-169">Les autres transactions tentant d’ajouter une colonne portant le même nom échouent.</span><span class="sxs-lookup"><span data-stu-id="d52ed-169">Other transactions attempting to add a column with the same name will fail.</span></span> <span data-ttu-id="d52ed-170">Ce bit est utile uniquement avec <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span><span class="sxs-lookup"><span data-stu-id="d52ed-170">This bit is only useful with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="d52ed-171">Elle ne peut pas être utilisée dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="d52ed-171">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d52ed-172">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="d52ed-172">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="d52ed-173">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="d52ed-173">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d52ed-174">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="d52ed-174">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="d52ed-175">Utilisez JET_bitColumnDeleteOnZero au lieu de JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="d52ed-175">Use JET_bitColumnDeleteOnZero instead of JET_bitColumnFinalize.</span></span> <span data-ttu-id="d52ed-176">JET_bitColumnFinalize spécifie qu’une colonne peut être finalisée.</span><span class="sxs-lookup"><span data-stu-id="d52ed-176">JET_bitColumnFinalize specifies that a column can be finalized.</span></span> <span data-ttu-id="d52ed-177">Lorsqu’une colonne qui peut être finalisée a une colonne de mise à jour de dépôt qui atteint zéro, la ligne est supprimée.</span><span class="sxs-lookup"><span data-stu-id="d52ed-177">When a column that can be finalized has an escrow update column that reaches zero, the row will be deleted.</span></span> <span data-ttu-id="d52ed-178">Les versions ultérieures peuvent appeler une fonction de rappel à la place.</span><span class="sxs-lookup"><span data-stu-id="d52ed-178">Future versions can invoke a callback function instead.</span></span> <span data-ttu-id="d52ed-179">Pour plus d’informations, consultez <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="d52ed-179">For more information, see <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="d52ed-180">Une colonne pouvant être finalisée doit être une colonne de mise à jour de tiers de confiance.</span><span class="sxs-lookup"><span data-stu-id="d52ed-180">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="d52ed-181">JET_bitColumnFinalize ne peut pas être utilisé avec JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="d52ed-181">JET_bitColumnFinalize cannot be used with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d52ed-182">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="d52ed-182">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="d52ed-183">La valeur par défaut d’une colonne est fournie par la fonction de rappel, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="d52ed-183">The default value for a column is provided by the callback function, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="d52ed-184">Une colonne qui a une valeur par défaut définie par l’utilisateur doit être une colonne avec balises.</span><span class="sxs-lookup"><span data-stu-id="d52ed-184">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="d52ed-185"><strong>pvDefault</strong> doit pointer vers une structure <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> et <strong>cbDefault</strong> doit avoir la valeur sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span><span class="sxs-lookup"><span data-stu-id="d52ed-185"><strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span></span></p>
<p><span data-ttu-id="d52ed-186">JET_bitColumnUserDefinedDefault ne peut pas être utilisé conjointement avec les constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="d52ed-186">JET_bitColumnUserDefinedDefault cannot be used in conjunction with the following constants:</span></span></p>
<ul>
<li><p><span data-ttu-id="d52ed-187">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="d52ed-187">JET_bitColumnFixed</span></span></p></li>
<li><p><span data-ttu-id="d52ed-188">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="d52ed-188">JET_bitColumnNotNULL</span></span></p></li>
<li><p><span data-ttu-id="d52ed-189">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="d52ed-189">JET_bitColumnVersion</span></span></p></li>
<li><p><span data-ttu-id="d52ed-190">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="d52ed-190">JET_bitColumnAutoincrement</span></span></p></li>
<li><p><span data-ttu-id="d52ed-191">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="d52ed-191">JET_bitColumnUpdatable</span></span></p></li>
<li><p><span data-ttu-id="d52ed-192">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="d52ed-192">JET_bitColumnEscrowUpdate</span></span></p></li>
<li><p><span data-ttu-id="d52ed-193">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="d52ed-193">JET_bitColumnFinalize</span></span></p></li>
<li><p><span data-ttu-id="d52ed-194">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="d52ed-194">JET_bitColumnDeleteOnZero</span></span></p></li>
<li><p><span data-ttu-id="d52ed-195">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="d52ed-195">JET_bitColumnMaybeNull</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d52ed-196">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="d52ed-196">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="d52ed-197">La colonne est une colonne de mise à jour de dépôt, et lorsqu’elle atteint zéro, l’enregistrement est supprimé.</span><span class="sxs-lookup"><span data-stu-id="d52ed-197">The column is an escrow update column, and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="d52ed-198">Une utilisation courante d’une colonne qui peut être finalisée consiste à l’utiliser comme un champ de décompte de références et, lorsque le champ atteint zéro, l’enregistrement est supprimé.</span><span class="sxs-lookup"><span data-stu-id="d52ed-198">A common use for a column that can be finalized is to use it as a reference count field, and when the field reaches zero the record gets deleted.</span></span> <span data-ttu-id="d52ed-199">JET_bitColumnDeleteOnZero est lié à JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="d52ed-199">JET_bitColumnDeleteOnZero is related to JET_bitColumnFinalize.</span></span> <span data-ttu-id="d52ed-200">Une colonne de suppression sur zéro doit être une colonne de mise à jour de tiers de confiance.</span><span class="sxs-lookup"><span data-stu-id="d52ed-200">A delete-on-zero column must be an escrow update column.</span></span> <span data-ttu-id="d52ed-201">JET_bitColumnDeleteOnZero ne peut pas être utilisé avec JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="d52ed-201">JET_bitColumnDeleteOnZero cannot be used with JET_bitColumnFinalize.</span></span> <span data-ttu-id="d52ed-202">JET_bitColumnDeleteOnZero ne peut pas être utilisé avec des colonnes par défaut définies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d52ed-202">JET_bitColumnDeleteOnZero cannot be used with user defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d52ed-203">**pvDefault**</span><span class="sxs-lookup"><span data-stu-id="d52ed-203">**pvDefault**</span></span>

<span data-ttu-id="d52ed-204">Pointe vers une mémoire tampon qui sera la valeur par défaut pour une colonne.</span><span class="sxs-lookup"><span data-stu-id="d52ed-204">Points to a buffer which will be the default value for a column.</span></span> <span data-ttu-id="d52ed-205">La longueur de la mémoire tampon est **cbDefault**.</span><span class="sxs-lookup"><span data-stu-id="d52ed-205">The length of the buffer is **cbDefault**.</span></span> <span data-ttu-id="d52ed-206">S’il n’existe pas de valeur par défaut, **pvDefault** doit avoir la valeur null et **cbDefault** doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="d52ed-206">If there is no default, **pvDefault** should be set to NULL and **cbDefault** should be set to zero.</span></span> <span data-ttu-id="d52ed-207">Si *Grbit* a JET_bitColumnUserDefinedDefault défini, **pvDefault** est interprété comme un pointeur vers une structure JET_USERDEFINEDDEFAULT.</span><span class="sxs-lookup"><span data-stu-id="d52ed-207">If *grbit* has JET_bitColumnUserDefinedDefault set, **pvDefault** will be interpreted as a pointer to a JET_USERDEFINEDDEFAULT structure.</span></span> <span data-ttu-id="d52ed-208">Les valeurs par défaut ne peuvent pas dépasser 255 octets.</span><span class="sxs-lookup"><span data-stu-id="d52ed-208">Default values cannot be larger than 255 bytes.</span></span> <span data-ttu-id="d52ed-209">Si une valeur par défaut est supérieure à 255 octets, elle est tronquée en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="d52ed-209">If a default value is larger than 255 bytes, it will be silently truncated.</span></span>

<span data-ttu-id="d52ed-210">**cbDefault**</span><span class="sxs-lookup"><span data-stu-id="d52ed-210">**cbDefault**</span></span>

<span data-ttu-id="d52ed-211">Taille, en octets, de la mémoire tampon spécifiée par **pvDefault**.</span><span class="sxs-lookup"><span data-stu-id="d52ed-211">The size, in bytes, of the buffer specified by **pvDefault**.</span></span>

<span data-ttu-id="d52ed-212">**cp**</span><span class="sxs-lookup"><span data-stu-id="d52ed-212">**cp**</span></span>

<span data-ttu-id="d52ed-213">Page de codes de la colonne.</span><span class="sxs-lookup"><span data-stu-id="d52ed-213">The code page for the column.</span></span> <span data-ttu-id="d52ed-214">Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="d52ed-214">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="d52ed-215">La valeur zéro signifie que la valeur par défaut sera utilisée (anglais, 1252).</span><span class="sxs-lookup"><span data-stu-id="d52ed-215">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="d52ed-216">Si la colonne n’est pas une colonne de texte, la page de codes est automatiquement définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="d52ed-216">If the column is not a text column, the code page automatically gets set to zero.</span></span>

<span data-ttu-id="d52ed-217">**ColumnID**</span><span class="sxs-lookup"><span data-stu-id="d52ed-217">**columnid**</span></span>

<span data-ttu-id="d52ed-218">En cas de réussite, l’identificateur de colonne de la colonne qui vient d’être créée est renvoyé dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="d52ed-218">On success, the column identifier of the newly-created column will be passed back in this field.</span></span> <span data-ttu-id="d52ed-219">En cas d’échec, la valeur n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="d52ed-219">On failure, the value is undefined.</span></span>

<span data-ttu-id="d52ed-220">**Raise**</span><span class="sxs-lookup"><span data-stu-id="d52ed-220">**err**</span></span>

<span data-ttu-id="d52ed-221">Le champ **Err** contient l’état de la création de cette colonne.</span><span class="sxs-lookup"><span data-stu-id="d52ed-221">The **err** field will contain the status of creating this column.</span></span> <span data-ttu-id="d52ed-222">Pour obtenir la liste des valeurs de retour probables, consultez [JetAddColumn](./jetaddcolumn-function.md) .</span><span class="sxs-lookup"><span data-stu-id="d52ed-222">See [JetAddColumn](./jetaddcolumn-function.md) for a list of likely return values.</span></span>

### <a name="requirements"></a><span data-ttu-id="d52ed-223">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d52ed-223">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d52ed-224"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d52ed-224"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d52ed-225">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="d52ed-225">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d52ed-226"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="d52ed-226"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d52ed-227">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d52ed-227">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d52ed-228"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="d52ed-228"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d52ed-229">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="d52ed-229">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d52ed-230"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="d52ed-230"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="d52ed-231">Implémenté comme <strong>JET_COLUMNCREATE_W</strong> (Unicode) et <strong>JET_COLUMNCREATE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="d52ed-231">Implemented as <strong>JET_COLUMNCREATE_W</strong> (Unicode) and <strong>JET_COLUMNCREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="d52ed-232">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d52ed-232">See Also</span></span>

[<span data-ttu-id="d52ed-233">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="d52ed-233">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="d52ed-234">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="d52ed-234">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="d52ed-235">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d52ed-235">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d52ed-236">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d52ed-236">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d52ed-237">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="d52ed-237">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="d52ed-238">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="d52ed-238">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="d52ed-239">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="d52ed-239">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)  
[<span data-ttu-id="d52ed-240">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="d52ed-240">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="d52ed-241">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="d52ed-241">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="d52ed-242">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="d52ed-242">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="d52ed-243">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="d52ed-243">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="d52ed-244">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="d52ed-244">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="d52ed-245">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="d52ed-245">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)  
[<span data-ttu-id="d52ed-246">JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="d52ed-246">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)  
[<span data-ttu-id="d52ed-247">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="d52ed-247">JetSetColumns</span></span>](./jetsetcolumns-function.md)
