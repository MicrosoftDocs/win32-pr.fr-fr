---
description: 'En savoir plus sur : fonction JetAddColumn'
title: Fonction JetAddColumn
TOCTitle: JetAddColumn Function
ms:assetid: e146f784-2cbd-42c0-bf64-b37dc6f9ee43
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294122(v=EXCHG.10)
ms:contentKeyID: 32765736
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAddColumnW
- JetAddColumnA
- JetAddColumn
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1b8c3eac113daeae43ec4a8e62b7fcda9ddbf9f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534692"
---
# <a name="jetaddcolumn-function"></a><span data-ttu-id="2d9b2-103">Fonction JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="2d9b2-103">JetAddColumn Function</span></span>


<span data-ttu-id="2d9b2-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="2d9b2-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetaddcolumn-function"></a><span data-ttu-id="2d9b2-105">Fonction JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="2d9b2-105">JetAddColumn Function</span></span>

<span data-ttu-id="2d9b2-106">La fonction **JetAddColumn** ajoute une nouvelle colonne à une table existante dans une base de données ESE.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-106">The **JetAddColumn** function adds a new column to an existing table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetAddColumn(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szColumnName,
      __in          const JET_COLUMNDEF* pcolumndef,
      __in_opt      const void* pvDefault,
      __in          unsigned long cbDefault,
      __out_opt     JET_COLUMNID* pcolumnid
    );
```

### <a name="parameters"></a><span data-ttu-id="2d9b2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d9b2-107">Parameters</span></span>

<span data-ttu-id="2d9b2-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="2d9b2-108">*sesid*</span></span>

<span data-ttu-id="2d9b2-109">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="2d9b2-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="2d9b2-110">*tableid*</span></span>

<span data-ttu-id="2d9b2-111">Table à laquelle ajouter la colonne.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-111">The table to which to add the column.</span></span>

<span data-ttu-id="2d9b2-112">*szColumnName*</span><span class="sxs-lookup"><span data-stu-id="2d9b2-112">*szColumnName*</span></span>

<span data-ttu-id="2d9b2-113">Nom de la colonne à ajouter.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-113">The name of the column to add.</span></span> <span data-ttu-id="2d9b2-114">Le nom doit respecter les critères suivants :</span><span class="sxs-lookup"><span data-stu-id="2d9b2-114">The name must meet the following criteria:</span></span>

  - <span data-ttu-id="2d9b2-115">Sa longueur doit être inférieure à JET_cbNameMost caractères, à l’exclusion de la **valeur null** de fin.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-115">It must be fewer than JET_cbNameMost characters in length, not including the terminating **NULL**.</span></span>

  - <span data-ttu-id="2d9b2-116">Il ne doit contenir que des caractères issus des jeux suivants : de 0 à 9, de A à Z, de a à z et toutes les autres signes de ponctuation, à l’exception du point d’exclamation ( \! ), de la virgule (,), du crochet ouvrant () et du \[ crochet fermant ( \] ).</span><span class="sxs-lookup"><span data-stu-id="2d9b2-116">It must contain characters only from the following sets: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]) — that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, and 0x5d through 0x7f.</span></span>

  - <span data-ttu-id="2d9b2-117">Il ne peut pas commencer par un espace.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-117">It cannot begin with a space.</span></span>

  - <span data-ttu-id="2d9b2-118">Il doit contenir au moins un caractère autre qu’un espace.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-118">It must contain at least one non-space character.</span></span>

<span data-ttu-id="2d9b2-119">*pcolumndef*</span><span class="sxs-lookup"><span data-stu-id="2d9b2-119">*pcolumndef*</span></span>

<span data-ttu-id="2d9b2-120">Pointeur vers une structure [JET_COLUMNDEF](./jet-columndef-structure.md) , qui définit les données qui peuvent être stockées dans une colonne.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-120">A pointer to a [JET_COLUMNDEF](./jet-columndef-structure.md) structure, which defines the data that can be stored in a column.</span></span>

<span data-ttu-id="2d9b2-121">*pvDefault*</span><span class="sxs-lookup"><span data-stu-id="2d9b2-121">*pvDefault*</span></span>

<span data-ttu-id="2d9b2-122">Pointeur vers une mémoire tampon qui contient la valeur par défaut de la colonne.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-122">A pointer to a buffer that contains the default value for the column.</span></span> <span data-ttu-id="2d9b2-123">La longueur de la mémoire tampon est **cbDefault**.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-123">The length of the buffer is **cbDefault**.</span></span> <span data-ttu-id="2d9b2-124">S’il n’y a pas de valeur par défaut, affectez la valeur **null** à **pvDefault** et **cbDefault** à zéro.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-124">If there is no default, set **pvDefault** to **NULL** and **cbDefault** to zero.</span></span> <span data-ttu-id="2d9b2-125">Les valeurs par défaut ne peuvent pas être supérieures à JET_cbColumnMost octets pour les colonnes fixes ou les octets JET_cbLVDefaultValueMost pour les valeurs longues.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-125">Default values cannot be larger than JET_cbColumnMost bytes for fixed columns or JET_cbLVDefaultValueMost bytes for long values.</span></span> <span data-ttu-id="2d9b2-126">Si une valeur par défaut est supérieure à celle-ci, elle sera tronquée en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-126">If a default value is larger than that, it will be silently truncated.</span></span>

<span data-ttu-id="2d9b2-127">Si *Grbit* a JET_bitColumnUserDefinedDefault défini, **pvDefault** est interprété comme un pointeur vers une structure [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="2d9b2-127">If *grbit* has JET_bitColumnUserDefinedDefault set, **pvDefault** will be interpreted as a pointer to a [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) structure.</span></span>

<span data-ttu-id="2d9b2-128">*cbDefault*</span><span class="sxs-lookup"><span data-stu-id="2d9b2-128">*cbDefault*</span></span>

<span data-ttu-id="2d9b2-129">Taille, en octets, de la mémoire tampon spécifiée dans **pvDefault**.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-129">The size, in bytes, of the buffer that is specified in **pvDefault**.</span></span>

<span data-ttu-id="2d9b2-130">*pColumnID*</span><span class="sxs-lookup"><span data-stu-id="2d9b2-130">*pcolumnid*</span></span>

<span data-ttu-id="2d9b2-131">Pointeur vers une structure [JET_COLUMNID](./jet-columnid.md) , qui, en cas de réussite, reçoit l’identificateur de la colonne qui vient d’être créée.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-131">A pointer to a [JET_COLUMNID](./jet-columnid.md) structure, which, on success, will receive the identifier of the newly created column.</span></span> <span data-ttu-id="2d9b2-132">En cas d’échec, la valeur n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-132">On failure, the value is undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="2d9b2-133">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2d9b2-133">Return Value</span></span>

<span data-ttu-id="2d9b2-134">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-134">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2d9b2-135">Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2d9b2-135">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d9b2-136">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2d9b2-136">Return code</span></span></p></th>
<th><p><span data-ttu-id="2d9b2-137">Description</span><span class="sxs-lookup"><span data-stu-id="2d9b2-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d9b2-138">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2d9b2-138">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-139">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-139">The operation was successful.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9b2-140">JET_errFixedDDL</span><span class="sxs-lookup"><span data-stu-id="2d9b2-140">JET_errFixedDDL</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-141">Une tentative de modification de la définition des données d’une table DDL fixe a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-141">An attempt was made to modify the data definition of a fixed DDL table.</span></span> <span data-ttu-id="2d9b2-142">Une table de modèle est un exemple de table avec une DDL fixe.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-142">An example of a table with fixed DDL is a Template Table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9b2-143">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2d9b2-143">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-144">Un paramètre non valide a été passé dans l’API.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-144">An invalid parameter was passed into the API.</span></span> <span data-ttu-id="2d9b2-145">Voici quelques exemples de paramètres non valides :</span><span class="sxs-lookup"><span data-stu-id="2d9b2-145">Some examples of invalid parameters are:</span></span></p>
<ul>
<li><p><span data-ttu-id="2d9b2-146">Passage de la taille incorrecte de la structure <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> dans son membre <em>cbStruct</em> .</span><span class="sxs-lookup"><span data-stu-id="2d9b2-146">Passing in the wrong size of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure in its <em>cbStruct</em> member.</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-147">Le passage de JET_bitColumnUserDefinedDefault, mais pas la définition de <strong>cbDefault</strong> sur sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span><span class="sxs-lookup"><span data-stu-id="2d9b2-147">Passing in JET_bitColumnUserDefinedDefault, but not setting <strong>cbDefault</strong> to sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9b2-148">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="2d9b2-148">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-149">Une tentative a été effectuée pour ajouter une colonne avec le bit JET_bitColumnUnversioned défini, mais la session est actuellement dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-149">An attempt was made to add a column with the JET_bitColumnUnversioned bit set, but the session is currently in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9b2-150">JET_errColumnDuplicate</span><span class="sxs-lookup"><span data-stu-id="2d9b2-150">JET_errColumnDuplicate</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-151">Une colonne existe déjà.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-151">A column already exists.</span></span> <span data-ttu-id="2d9b2-152">Une tentative d’ajout d’une colonne sans informations de version a été effectuée et cette colonne existe déjà.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-152">An attempt was made to add a column without version information, and that column already exists.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9b2-153">JET_errTableNotEmpty</span><span class="sxs-lookup"><span data-stu-id="2d9b2-153">JET_errTableNotEmpty</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-154">La table contient des données.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-154">The table contains data.</span></span> <span data-ttu-id="2d9b2-155">Une colonne de mise à jour de tiers de confiance ne peut être ajoutée qu’à une table vide.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-155">An Escrow Update column can only be added to an empty table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9b2-156">JET_errRecordTooBig</span><span class="sxs-lookup"><span data-stu-id="2d9b2-156">JET_errRecordTooBig</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-157">L’enregistrement est trop volumineux.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-157">The record is too big.</span></span> <span data-ttu-id="2d9b2-158">La somme du paramètre <strong>cbMax</strong> pour les colonnes fixes ne doit pas dépasser une certaine valeur.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-158">The sum of the <strong>cbMax</strong> parameter for the fixed columns must not exceed a certain value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9b2-159">JET_errTooManyColumns</span><span class="sxs-lookup"><span data-stu-id="2d9b2-159">JET_errTooManyColumns</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-160">Une tentative d’ajout d’un trop grand nombre de colonnes à la table a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-160">An attempt was made to add too many columns to the table.</span></span> <span data-ttu-id="2d9b2-161">Une table ne peut pas comporter plus de JET_ccolFixedMost colonnes fixes, ni plus de JET_ccolVarMost colonnes de longueur variable, ni plus de JET_ccolTaggedMost colonnes avec balises.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-161">A table can have no more than JET_ccolFixedMost fixed columns, no more than JET_ccolVarMost variable-length columns, and no more than JET_ccolTaggedMost tagged columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9b2-162">JET_errColumnRedundant</span><span class="sxs-lookup"><span data-stu-id="2d9b2-162">JET_errColumnRedundant</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-163">Une tentative d’ajout d’une colonne redondante a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-163">An attempt was made to add a redundant column.</span></span> <span data-ttu-id="2d9b2-164">Il ne doit y avoir qu’une seule colonne AutoIncrement et pas plus d’une colonne version par table.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-164">There should be no more than one autoincrement column, and no more than one version column per table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9b2-165">JET_errCallbackNotResolved</span><span class="sxs-lookup"><span data-stu-id="2d9b2-165">JET_errCallbackNotResolved</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-166">La fonction de rappel n’a pas pu être résolue.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-166">The callback function could not be resolved.</span></span> <span data-ttu-id="2d9b2-167">La DLL n’a peut-être pas été trouvée, ou la fonction dans la DLL n’a peut-être pas été trouvée.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-167">The DLL might not have been found, or the function in the DLL might not have been found.</span></span> <span data-ttu-id="2d9b2-168">Le journal des événements fournit plus de détails si la journalisation suffisante est activée.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-168">The event log will provide more details if sufficient logging is enabled.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9b2-169">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="2d9b2-169">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-170">Un avertissement indiquant que la longueur maximale (<strong>cbMax</strong>) d’une colonne fixe ou variable était supérieure à JET_cbColumnMost.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-170">A warning indicating that the maximum length (<strong>cbMax</strong>) of a fixed or variable column was greater than JET_cbColumnMost.</span></span> <span data-ttu-id="2d9b2-171">Cette limite ne s’applique pas aux valeurs longues ( <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> et <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="2d9b2-171">This limit does not apply to Long Values (that is <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> and <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9b2-172">JET_errInvalidName</span><span class="sxs-lookup"><span data-stu-id="2d9b2-172">JET_errInvalidName</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-173">Un nom non valide a été passé en tant que <strong>szColumnName</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-173">An invalid name was passed as <strong>szColumnName</strong>.</span></span> <span data-ttu-id="2d9b2-174">Pour plus d’informations sur les restrictions, consultez les critères pour <strong>szColumnName</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-174">For more information about the restrictions, see the criteria for <strong>szColumnName</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9b2-175">JET_errInvalidColumnType</span><span class="sxs-lookup"><span data-stu-id="2d9b2-175">JET_errInvalidColumnType</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-176">Le champ <strong>coltyp</strong> n’est pas défini sur un type de colonne valide.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-176">The <strong>coltyp</strong> field was not set to a valid column type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9b2-177">JET_errInvalidCodePage</span><span class="sxs-lookup"><span data-stu-id="2d9b2-177">JET_errInvalidCodePage</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-178">Le paramètre <strong>CP</strong> de la structure <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> n’a pas été défini sur une page de codes valide.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-178">The <strong>cp</strong> parameter of the <a href="gg294130(v=exchg.10).md">JET_COLUMNDEF</a> structure was not set to a valid code page.</span></span> <span data-ttu-id="2d9b2-179">Les seules valeurs valides pour les colonnes de texte sont l’anglais (1252) et Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="2d9b2-179">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="2d9b2-180">La valeur 0 signifie que la valeur par défaut sera utilisée (anglais, 1252).</span><span class="sxs-lookup"><span data-stu-id="2d9b2-180">A value of 0 means the default will be used (English, 1252).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9b2-181">JET_errTaggedNotNULL</span><span class="sxs-lookup"><span data-stu-id="2d9b2-181">JET_errTaggedNotNULL</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-182">JET_bitColumnNotNULL ne peut pas être utilisé avec des colonnes avec balises, de valeurs longues ou SLV.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-182">JET_bitColumnNotNULL cannot be used with tagged, Long Value, or SLV columns.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9b2-183">JET_errInvalidgrbit</span><span class="sxs-lookup"><span data-stu-id="2d9b2-183">JET_errInvalidgrbit</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-184">Une combinaison non valide de <em>grbits</em> a été spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-184">An invalid combination of <em>grbits</em> was specified.</span></span> <span data-ttu-id="2d9b2-185">Voici quelques-unes des raisons de cette erreur :</span><span class="sxs-lookup"><span data-stu-id="2d9b2-185">Some of the reasons for this error are:</span></span></p>
<ul>
<li><p><span data-ttu-id="2d9b2-186">JET_bitColumnFixed a été utilisé sur une colonne avec balises, une valeur longue ou une colonne SLV.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-186">JET_bitColumnFixed was used on a tagged, Long Value, or SLV column.</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-187">JET_bitColumnEscrowUpdate a été utilisé sur une colonne qui n’était pas de type <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-187">JET_bitColumnEscrowUpdate was used on a column that was not of type <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-188">JET_bitColumnEscrowUpdate a été utilisé sur une colonne de version (JET_bitColumnVersion).</span><span class="sxs-lookup"><span data-stu-id="2d9b2-188">JET_bitColumnEscrowUpdate was used on a Version column (JET_bitColumnVersion).</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-189">JET_bitColumnEscrowUpdate a été utilisé sur une colonne AutoIncrememnt (JET_bitColumnAutoincrement).</span><span class="sxs-lookup"><span data-stu-id="2d9b2-189">JET_bitColumnEscrowUpdate was used on an AutoIncrememnt column (JET_bitColumnAutoincrement).</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-190">JET_bitColumnEscrowUpdate a été utilisé sur une colonne qui n’a pas de valeur par défaut (<strong>cbDefault</strong> était égal à zéro).</span><span class="sxs-lookup"><span data-stu-id="2d9b2-190">JET_bitColumnEscrowUpdate was used on a column that did not have a default value (<strong>cbDefault</strong> was equal to zero).</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-191">JET_bitColumnFinalize a été utilisé sur une colonne qui n’est pas une colonne de mise à jour de dépôt (JET_bitColumnEscrowUpdate n’a pas été définie).</span><span class="sxs-lookup"><span data-stu-id="2d9b2-191">JET_bitColumnFinalize was used on a column that was not an Escrow Update column (JET_bitColumnEscrowUpdate was not set).</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-192">JET_bitColumnDeleteOnZero a été utilisé sur une colonne qui n’est pas une colonne de mise à jour de dépôt (JET_bitColumnEscrowUpdate n’a pas été définie).</span><span class="sxs-lookup"><span data-stu-id="2d9b2-192">JET_bitColumnDeleteOnZero was used on a column that was not an Escrow Update column (JET_bitColumnEscrowUpdate was not set).</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-193">JET_bitColumnAutoincrement a été utilisé sur une colonne qui n’a pas été <a href="gg269213(v=exchg.10).md">JET_coltypLonge</a>.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-193">JET_bitColumnAutoincrement was used on a column that was not <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p>
<p><span data-ttu-id="2d9b2-194"><strong>Windows 2000 :  </strong> Cette raison du code d’erreur est utilisée uniquement dans Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-194"><strong>Windows 2000:  </strong>This reason for the error code is used only in Windows 2000.</span></span></p>
<p><span data-ttu-id="2d9b2-195">JET_bitColumnAutoincrement a été utilisé sur une colonne qui n’était ni <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> ni <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-195">JET_bitColumnAutoincrement was used on a column that was neither <a href="gg269213(v=exchg.10).md">JET_coltypLong</a> nor <a href="gg269213(v=exchg.10).md">JET_coltypCurrency</a>.</span></span></p>
<p><span data-ttu-id="2d9b2-196"><strong>Windows XP :  </strong> Cette raison du code d’erreur est utilisée dans Windows XP et les systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-196"><strong>Windows XP:  </strong>This reason for the error code is used in Windows XP and later operating systems.</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-197">JET_bitColumnVersion a été utilisé sur une colonne qui n’a pas été <a href="gg269213(v=exchg.10).md">JET_coltypLonge</a>.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-197">JET_bitColumnVersion was used on a column that was not <a href="gg269213(v=exchg.10).md">JET_coltypLong</a>.</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-198">JET_bitColumnVersion a été utilisé sur une colonne AutoIncrement.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-198">JET_bitColumnVersion was used on an autoincrement column.</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-199">JET_bitColumnUserDefinedDefault a été utilisé conjointement avec JET_bitColumnFixed.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-199">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnFixed.</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-200">JET_bitColumnUserDefinedDefault a été utilisé conjointement avec JET_bitColumnNotNULL.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-200">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnNotNULL.</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-201">JET_bitColumnUserDefinedDefault a été utilisé conjointement avec JET_bitColumnVersion.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-201">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnVersion.</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-202">JET_bitColumnUserDefinedDefault a été utilisé conjointement avec JET_bitColumnAutoincrement.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-202">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnAutoincrement.</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-203">JET_bitColumnUserDefinedDefault a été utilisé conjointement avec JET_bitColumnUpdatable.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-203">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnUpdatable.</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-204">JET_bitColumnUserDefinedDefault a été utilisé conjointement avec JET_bitColumnEscrowUpdate.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-204">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnEscrowUpdate.</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-205">JET_bitColumnUserDefinedDefault a été utilisé conjointement avec JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-205">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnFinalize.</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-206">JET_bitColumnUserDefinedDefault a été utilisé conjointement avec JET_bitColumnDeleteOnZero.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-206">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnDeleteOnZero.</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-207">JET_bitColumnUserDefinedDefault a été utilisé conjointement avec JET_bitColumnMaybeNull.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-207">JET_bitColumnUserDefinedDefault was used in conjunction with JET_bitColumnMaybeNull.</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-208">JET_bitColumnUserDefinedDefault a été utilisé sur une colonne non balisée (qui est fixe ou variable).</span><span class="sxs-lookup"><span data-stu-id="2d9b2-208">JET_bitColumnUserDefinedDefault was used on a non-tagged column (that is fixed or variable).</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9b2-209">JET_errMultiValuedColumnMustBeTagged</span><span class="sxs-lookup"><span data-stu-id="2d9b2-209">JET_errMultiValuedColumnMustBeTagged</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-210">Une colonne à valeurs multiples (JET_bitColumnMultiValued) peut uniquement être utilisée sur une colonne avec balises ou de valeurs longues (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="2d9b2-210">A multi-valued column (JET_bitColumnMultiValued) can only be used on a tagged or Long Value (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) column.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9b2-211">JET_errCannotBeTagged</span><span class="sxs-lookup"><span data-stu-id="2d9b2-211">JET_errCannotBeTagged</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-212">Une tentative d’utilisation d’une colonne avec balises a été effectuée lorsque la colonne n’est peut-être pas référencée.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-212">An attempt was made to use a tagged column when the column might not be tagged.</span></span> <span data-ttu-id="2d9b2-213">Voici quelques-unes des contraintes pour interdire les colonnes avec balises :</span><span class="sxs-lookup"><span data-stu-id="2d9b2-213">Some of the constraints for disallowing tagged columns are:</span></span></p>
<ul>
<li><p><span data-ttu-id="2d9b2-214">Une colonne de mise à jour de dépôt (JET_bitColumnEscrowUpdate) ne peut pas être utilisée sur une colonne avec balises ou de valeurs longues (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> ou <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="2d9b2-214">An Escrow Update column (JET_bitColumnEscrowUpdate) cannot be used on a tagged or Long Value (<a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> or <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>) column.</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-215">Une colonne AutoIncrement ne peut pas être référencée.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-215">An autoincrement column might not be tagged.</span></span></p></li>
<li><p><span data-ttu-id="2d9b2-216">Une colonne de version n’est peut-être pas référencée.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-216">A Version column might not be tagged.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9b2-217">JET_errExclusiveTableLockRequired</span><span class="sxs-lookup"><span data-stu-id="2d9b2-217">JET_errExclusiveTableLockRequired</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-218">Un verrou exclusif sur la table était requis pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-218">An exclusive lock on the table was required for this operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9b2-219">JET_wrnColumnMaxTruncated</span><span class="sxs-lookup"><span data-stu-id="2d9b2-219">JET_wrnColumnMaxTruncated</span></span></p></td>
<td><p><span data-ttu-id="2d9b2-220">Un avertissement indiquant que la longueur maximale (<em>cbMax</em>) d’une colonne fixe ou variable était supérieure à JET_cbColumnMost.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-220">A warning indicating that the maximum length (<em>cbMax</em>) of a fixed or variable column was greater than JET_cbColumnMost.</span></span> <span data-ttu-id="2d9b2-221">Cette limite ne s’applique pas aux valeurs longues ( <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> et <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span><span class="sxs-lookup"><span data-stu-id="2d9b2-221">This limit does not apply to Long Values (that is <a href="gg269213(v=exchg.10).md">JET_coltypLongBinary</a> and <a href="gg269213(v=exchg.10).md">JET_coltypLongText</a>).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="2d9b2-222">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d9b2-222">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d9b2-223"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="2d9b2-223"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2d9b2-224">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-224">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9b2-225"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="2d9b2-225"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2d9b2-226">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-226">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9b2-227"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="2d9b2-227"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2d9b2-228">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-228">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9b2-229"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="2d9b2-229"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2d9b2-230">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-230">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d9b2-231"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2d9b2-231"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2d9b2-232">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2d9b2-232">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d9b2-233"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="2d9b2-233"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="2d9b2-234">Implémenté en tant que <strong>JetAddColumnW</strong> (Unicode) et <strong>JetAddColumnA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="2d9b2-234">Implemented as <strong>JetAddColumnW</strong> (Unicode) and <strong>JetAddColumnA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2d9b2-235">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d9b2-235">See Also</span></span>

[<span data-ttu-id="2d9b2-236">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="2d9b2-236">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="2d9b2-237">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="2d9b2-237">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="2d9b2-238">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="2d9b2-238">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)  
[<span data-ttu-id="2d9b2-239">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="2d9b2-239">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="2d9b2-240">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2d9b2-240">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2d9b2-241">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="2d9b2-241">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="2d9b2-242">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="2d9b2-242">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="2d9b2-243">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="2d9b2-243">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="2d9b2-244">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="2d9b2-244">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="2d9b2-245">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="2d9b2-245">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)
