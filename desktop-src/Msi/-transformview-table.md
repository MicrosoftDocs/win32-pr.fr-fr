---
description: Il s’agit d’une table temporaire en lecture seule utilisée pour afficher des transformations à l’aide du mode d’affichage transformer. Cette table n’est jamais conservée par le programme d’installation.
ms.assetid: 4763ac0e-900f-45f1-bee5-34d413c5e401
title: Table _TransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08cc513b1aae388d01cda178bfbefdc88874f6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528882"
---
# <a name="_transformview-table"></a><span data-ttu-id="78997-104">\_Table TransformView</span><span class="sxs-lookup"><span data-stu-id="78997-104">\_TransformView Table</span></span>

<span data-ttu-id="78997-105">Il s’agit d’une table temporaire en lecture seule utilisée pour afficher des transformations à l’aide du mode d’affichage transformer.</span><span class="sxs-lookup"><span data-stu-id="78997-105">This is a read-only temporary table used to view transforms with the transform view mode.</span></span> <span data-ttu-id="78997-106">Cette table n’est jamais conservée par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="78997-106">This table is never persisted by the installer.</span></span>

<span data-ttu-id="78997-107">Pour appeler le mode d’affichage transformation, obtenez un handle et ouvrez la base de données de référence.</span><span class="sxs-lookup"><span data-stu-id="78997-107">To invoke the transform view mode, obtain a handle and open the reference database.</span></span> <span data-ttu-id="78997-108">Consultez [obtention d’un descripteur de base de données](obtaining-a-database-handle.md).</span><span class="sxs-lookup"><span data-stu-id="78997-108">See [Obtaining a Database Handle](obtaining-a-database-handle.md).</span></span> <span data-ttu-id="78997-109">Appelez [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) avec l' \_ erreur MSITRANSFORM \_ VIEWTRANSFORM.</span><span class="sxs-lookup"><span data-stu-id="78997-109">Call [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) with MSITRANSFORM\_ERROR\_VIEWTRANSFORM.</span></span> <span data-ttu-id="78997-110">Cela arrête l’application de la transformation à la base de données et vide le contenu de la transformation dans la \_ table TransformView.</span><span class="sxs-lookup"><span data-stu-id="78997-110">This stops the transform from being applied to the database and dumps the transform contents into the \_TransformView table.</span></span> <span data-ttu-id="78997-111">Vous pouvez accéder aux données de la table à l’aide de requêtes SQL.</span><span class="sxs-lookup"><span data-stu-id="78997-111">The data in the table can be accessed using SQL queries.</span></span> <span data-ttu-id="78997-112">Consultez [utilisation des requêtes](working-with-queries.md).</span><span class="sxs-lookup"><span data-stu-id="78997-112">See [Working with Queries](working-with-queries.md).</span></span>

<span data-ttu-id="78997-113">La \_ table TransformView n’est pas effacée lorsqu’une autre transformation est appliquée.</span><span class="sxs-lookup"><span data-stu-id="78997-113">The \_TransformView table is not cleared when another transform is applied.</span></span> <span data-ttu-id="78997-114">Le tableau reflète l’effet cumulatif des applications successives.</span><span class="sxs-lookup"><span data-stu-id="78997-114">The table reflects the cumulative effect of successive applications.</span></span> <span data-ttu-id="78997-115">Pour afficher les transformations séparément, vous devez libérer la table.</span><span class="sxs-lookup"><span data-stu-id="78997-115">To view the transforms separately you must release the table.</span></span>

<span data-ttu-id="78997-116">La \_ table TransformView contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="78997-116">The \_TransformView Table has the following columns.</span></span>



| <span data-ttu-id="78997-117">Colonne</span><span class="sxs-lookup"><span data-stu-id="78997-117">Column</span></span>  | <span data-ttu-id="78997-118">Type</span><span class="sxs-lookup"><span data-stu-id="78997-118">Type</span></span>                         | <span data-ttu-id="78997-119">Clé</span><span class="sxs-lookup"><span data-stu-id="78997-119">Key</span></span> | <span data-ttu-id="78997-120">Nullable</span><span class="sxs-lookup"><span data-stu-id="78997-120">Nullable</span></span> |
|---------|------------------------------|-----|----------|
| <span data-ttu-id="78997-121">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="78997-121">Table</span></span>   | [<span data-ttu-id="78997-122">Identificateur</span><span class="sxs-lookup"><span data-stu-id="78997-122">Identifier</span></span>](identifier.md) | <span data-ttu-id="78997-123">O</span><span class="sxs-lookup"><span data-stu-id="78997-123">Y</span></span>   | <span data-ttu-id="78997-124">N</span><span class="sxs-lookup"><span data-stu-id="78997-124">N</span></span>        |
| <span data-ttu-id="78997-125">Colonne</span><span class="sxs-lookup"><span data-stu-id="78997-125">Column</span></span>  | [<span data-ttu-id="78997-126">Text</span><span class="sxs-lookup"><span data-stu-id="78997-126">Text</span></span>](text.md)             | <span data-ttu-id="78997-127">O</span><span class="sxs-lookup"><span data-stu-id="78997-127">Y</span></span>   | <span data-ttu-id="78997-128">N</span><span class="sxs-lookup"><span data-stu-id="78997-128">N</span></span>        |
| <span data-ttu-id="78997-129">Ligne</span><span class="sxs-lookup"><span data-stu-id="78997-129">Row</span></span>     | [<span data-ttu-id="78997-130">Text</span><span class="sxs-lookup"><span data-stu-id="78997-130">Text</span></span>](text.md)             | <span data-ttu-id="78997-131">O</span><span class="sxs-lookup"><span data-stu-id="78997-131">Y</span></span>   | <span data-ttu-id="78997-132">O</span><span class="sxs-lookup"><span data-stu-id="78997-132">Y</span></span>        |
| <span data-ttu-id="78997-133">Données</span><span class="sxs-lookup"><span data-stu-id="78997-133">Data</span></span>    | [<span data-ttu-id="78997-134">Text</span><span class="sxs-lookup"><span data-stu-id="78997-134">Text</span></span>](text.md)             | <span data-ttu-id="78997-135">N</span><span class="sxs-lookup"><span data-stu-id="78997-135">N</span></span>   | <span data-ttu-id="78997-136">O</span><span class="sxs-lookup"><span data-stu-id="78997-136">Y</span></span>        |
| <span data-ttu-id="78997-137">Actuel</span><span class="sxs-lookup"><span data-stu-id="78997-137">Current</span></span> | [<span data-ttu-id="78997-138">Text</span><span class="sxs-lookup"><span data-stu-id="78997-138">Text</span></span>](text.md)             | <span data-ttu-id="78997-139">N</span><span class="sxs-lookup"><span data-stu-id="78997-139">N</span></span>   | <span data-ttu-id="78997-140">O</span><span class="sxs-lookup"><span data-stu-id="78997-140">Y</span></span>        |



 

## <a name="column"></a><span data-ttu-id="78997-141">Colonne</span><span class="sxs-lookup"><span data-stu-id="78997-141">Column</span></span>

<dl> <dt>

<span data-ttu-id="78997-142"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tableau</span><span class="sxs-lookup"><span data-stu-id="78997-142"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="78997-143">Nom d’une table de base de données modifiée.</span><span class="sxs-lookup"><span data-stu-id="78997-143">Name of an altered database table.</span></span>

</dd> <dt>

<span data-ttu-id="78997-144"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Chronique</span><span class="sxs-lookup"><span data-stu-id="78997-144"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="78997-145">Nom d’une colonne de table modifiée ou d’une insertion, d’une suppression, d’une création ou d’une suppression.</span><span class="sxs-lookup"><span data-stu-id="78997-145">Name of an altered table column or INSERT, DELETE, CREATE, or DROP.</span></span>

</dd> <dt>

<span data-ttu-id="78997-146"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Haut</span><span class="sxs-lookup"><span data-stu-id="78997-146"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Row</span></span>
</dt> <dd>

<span data-ttu-id="78997-147">Liste des valeurs de clé primaire séparées par des tabulations.</span><span class="sxs-lookup"><span data-stu-id="78997-147">A list of the primary key values separated by tabs.</span></span> <span data-ttu-id="78997-148">Les valeurs de clé primaire NULL sont représentées par un caractère d’espace unique.</span><span class="sxs-lookup"><span data-stu-id="78997-148">Null primary key values are represented by a single space character.</span></span> <span data-ttu-id="78997-149">Une valeur null dans cette colonne indique une modification de schéma.</span><span class="sxs-lookup"><span data-stu-id="78997-149">A Null value in this column indicates a schema change.</span></span>

</dd> <dt>

<span data-ttu-id="78997-150"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Métadonnée</span><span class="sxs-lookup"><span data-stu-id="78997-150"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="78997-151">Les données, le nom d’un flux de données ou une définition de colonne.</span><span class="sxs-lookup"><span data-stu-id="78997-151">Data, name of a data stream, or a column definition.</span></span>

</dd> <dt>

<span data-ttu-id="78997-152"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Actif</span><span class="sxs-lookup"><span data-stu-id="78997-152"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Current</span></span>
</dt> <dd>

<span data-ttu-id="78997-153">Valeur actuelle de la base de données de référence ou numéro de colonne.</span><span class="sxs-lookup"><span data-stu-id="78997-153">Current value from reference database, or column a number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78997-154">Notes</span><span class="sxs-lookup"><span data-stu-id="78997-154">Remarks</span></span>

<span data-ttu-id="78997-155">Le \_ TransformView est conservé en mémoire par un nombre de verrous, qui peut être libéré avec la commande SQL suivante.</span><span class="sxs-lookup"><span data-stu-id="78997-155">The \_TransformView is held in memory by a lock count, that can be released with the following SQL command.</span></span>

<span data-ttu-id="78997-156">« ALTER TABLE \_ TRANSFORMVIEW Free ».</span><span class="sxs-lookup"><span data-stu-id="78997-156">"ALTER TABLE \_TransformView FREE".</span></span>

<span data-ttu-id="78997-157">Vous pouvez accéder aux données de la table à l’aide de requêtes SQL.</span><span class="sxs-lookup"><span data-stu-id="78997-157">The data in the table can be accessed using SQL queries.</span></span> <span data-ttu-id="78997-158">Le langage SQL a deux divisions principales : le langage de définition de données (DDL) utilisé pour définir tous les objets dans une base de données SQL, et le langage de manipulation de données (DML) utilisé pour sélectionner, insérer, mettre à jour et supprimer des données dans les objets définis à l’aide de DDL.</span><span class="sxs-lookup"><span data-stu-id="78997-158">The SQL language has two main divisions: Data Definition Language (DDL) that is used to define all the objects in an SQL database, and Data Manipulation Language (DML) that is used to select, insert, update, and delete data in the objects defined using DDL.</span></span>

<span data-ttu-id="78997-159">Les opérations de transformation de langage de manipulation de données (DML) sont indiquées comme suit.</span><span class="sxs-lookup"><span data-stu-id="78997-159">The Data Manipulation Language (DML) transform operations are indicated as follows.</span></span> <span data-ttu-id="78997-160">Le langage de manipulation de données (DML) sont les instructions dans SQL qui manipulent, au lieu de définir, des données.</span><span class="sxs-lookup"><span data-stu-id="78997-160">Data Manipulation Language (DML) are those statements in SQL that manipulate, as opposed to define, data.</span></span>



| <span data-ttu-id="78997-161">Opération de transformation</span><span class="sxs-lookup"><span data-stu-id="78997-161">Transform operation</span></span> | <span data-ttu-id="78997-162">Résultat SQL</span><span class="sxs-lookup"><span data-stu-id="78997-162">SQL result</span></span>                                    |
|---------------------|-----------------------------------------------|
| <span data-ttu-id="78997-163">Modifier des données</span><span class="sxs-lookup"><span data-stu-id="78997-163">Modify data</span></span>         | <span data-ttu-id="78997-164">Tableau chronique haut métadonnée {valeur actuelle}</span><span class="sxs-lookup"><span data-stu-id="78997-164">{table} {column} {row} {data} {current value}</span></span> |
| <span data-ttu-id="78997-165">Insérer une ligne</span><span class="sxs-lookup"><span data-stu-id="78997-165">Insert row</span></span>          | <span data-ttu-id="78997-166">Tableau « INSERT » {Row} NULL NULL</span><span class="sxs-lookup"><span data-stu-id="78997-166">{table} "INSERT" {row} NULL NULL</span></span>              |
| <span data-ttu-id="78997-167">Supprimer la ligne</span><span class="sxs-lookup"><span data-stu-id="78997-167">Delete row</span></span>          | <span data-ttu-id="78997-168">Tableau « DELETE » {Row} NULL NULL</span><span class="sxs-lookup"><span data-stu-id="78997-168">{table} "DELETE" {row} NULL NULL</span></span>              |



 

<span data-ttu-id="78997-169">Les opérations de transformation DDL (Data Definition Language) sont indiquées comme suit.</span><span class="sxs-lookup"><span data-stu-id="78997-169">The Data Definition Language (DDL) transform operations are indicated as follows.</span></span> <span data-ttu-id="78997-170">Le langage de définition de données (DDL) sont les instructions dans SQL qui définissent, par opposition à manipuler, les données.</span><span class="sxs-lookup"><span data-stu-id="78997-170">Data Definition Language (DDL) are those statements in SQL that define, as opposed to manipulate, data.</span></span>



| <span data-ttu-id="78997-171">Opération de transformation</span><span class="sxs-lookup"><span data-stu-id="78997-171">Transform operation</span></span> | <span data-ttu-id="78997-172">Résultat SQL</span><span class="sxs-lookup"><span data-stu-id="78997-172">SQL result</span></span>                                   |
|---------------------|----------------------------------------------|
| <span data-ttu-id="78997-173">Add column</span><span class="sxs-lookup"><span data-stu-id="78997-173">Add column</span></span>          | <span data-ttu-id="78997-174">Tableau chronique NULL {defn} {numéro de colonne}</span><span class="sxs-lookup"><span data-stu-id="78997-174">{table} {column} NULL {defn} {column number}</span></span> |
| <span data-ttu-id="78997-175">Ajoute une table</span><span class="sxs-lookup"><span data-stu-id="78997-175">Add table</span></span>           | <span data-ttu-id="78997-176">Tableau « CREATE » NULL NULL NULL</span><span class="sxs-lookup"><span data-stu-id="78997-176">{table} "CREATE" NULL NULL NULL</span></span>              |
| <span data-ttu-id="78997-177">Supprimer une table</span><span class="sxs-lookup"><span data-stu-id="78997-177">Drop table</span></span>          | <span data-ttu-id="78997-178">Tableau "DROP" NULL NULL NULL</span><span class="sxs-lookup"><span data-stu-id="78997-178">{table} "DROP" NULL NULL NULL</span></span>                |



 

<span data-ttu-id="78997-179">Lorsque l’application d’une transformation ajoute cette table, le champ de données reçoit du texte qui peut être interprété comme une valeur entière de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="78997-179">When the application of a transform adds this table, the Data field receives text that can be interpreted as a 16-bit integer value.</span></span> <span data-ttu-id="78997-180">La valeur décrit la colonne nommée dans le champ de colonne.</span><span class="sxs-lookup"><span data-stu-id="78997-180">The value describes the column named in the Column field.</span></span> <span data-ttu-id="78997-181">Vous pouvez comparer la valeur entière aux constantes dans le tableau suivant pour déterminer la définition de la colonne modifiée.</span><span class="sxs-lookup"><span data-stu-id="78997-181">You can compare the integer value to the constants in the following table to determine the definition of the altered column.</span></span>



| <span data-ttu-id="78997-182">bit</span><span class="sxs-lookup"><span data-stu-id="78997-182">Bit</span></span>                                                                                                       | <span data-ttu-id="78997-183">Description</span><span class="sxs-lookup"><span data-stu-id="78997-183">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78997-184"><span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bits 0 7</span><span class="sxs-lookup"><span data-stu-id="78997-184"><span id="Bits_07"></span><span id="bits_07"></span><span id="BITS_07"></span>Bits 0 7</span></span><br/>         | <span data-ttu-id="78997-185">Hexadécimal : 0x0000 0x0100</span><span class="sxs-lookup"><span data-stu-id="78997-185">Hexadecimal: 0x0000 0x0100</span></span><br/> <span data-ttu-id="78997-186">Décimal : 0 255</span><span class="sxs-lookup"><span data-stu-id="78997-186">Decimal: 0 255</span></span><br/> <span data-ttu-id="78997-187">Largeur de colonne</span><span class="sxs-lookup"><span data-stu-id="78997-187">Column width</span></span><br/>                                                                                                                                                                                                                                  |
| <span data-ttu-id="78997-188"><span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8</span><span class="sxs-lookup"><span data-stu-id="78997-188"><span id="Bit_8"></span><span id="bit_8"></span><span id="BIT_8"></span>Bit 8</span></span><br/>                  | <span data-ttu-id="78997-189">Hexadécimal : 0x0100</span><span class="sxs-lookup"><span data-stu-id="78997-189">Hexadecimal: 0x0100</span></span><br/> <span data-ttu-id="78997-190">Décimal : 256</span><span class="sxs-lookup"><span data-stu-id="78997-190">Decimal: 256</span></span><br/> <span data-ttu-id="78997-191">Colonne persistante.</span><span class="sxs-lookup"><span data-stu-id="78997-191">A persistent column.</span></span> <span data-ttu-id="78997-192">Zéro signifie une colonne temporaire.</span><span class="sxs-lookup"><span data-stu-id="78997-192">Zero means a temporary column.</span></span> <br/>                                                                                                                                                                                                   |
| <span data-ttu-id="78997-193"><span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9</span><span class="sxs-lookup"><span data-stu-id="78997-193"><span id="Bit_9"></span><span id="bit_9"></span><span id="BIT_9"></span>Bit 9</span></span><br/>                  | <span data-ttu-id="78997-194">Hexadécimal : 0x0200</span><span class="sxs-lookup"><span data-stu-id="78997-194">Hexadecimal: 0x0200</span></span><br/> <span data-ttu-id="78997-195">Décimal : 1023</span><span class="sxs-lookup"><span data-stu-id="78997-195">Decimal: 1023</span></span><br/> <span data-ttu-id="78997-196">Colonne localisable.</span><span class="sxs-lookup"><span data-stu-id="78997-196">A localizable column.</span></span> <span data-ttu-id="78997-197">Zéro signifie que la colonne ne peut pas être localisée.</span><span class="sxs-lookup"><span data-stu-id="78997-197">Zero means the column cannot be localized.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="78997-198"><span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11</span><span class="sxs-lookup"><span data-stu-id="78997-198"><span id="Bits_1011"></span><span id="bits_1011"></span><span id="BITS_1011"></span>Bits 10 11</span></span><br/> | <span data-ttu-id="78997-199">Hexadécimal : 0x0000</span><span class="sxs-lookup"><span data-stu-id="78997-199">Hexadecimal: 0x0000</span></span><br/> <span data-ttu-id="78997-200">Décimal : 0</span><span class="sxs-lookup"><span data-stu-id="78997-200">Decimal: 0</span></span><br/> <span data-ttu-id="78997-201">Entier long</span><span class="sxs-lookup"><span data-stu-id="78997-201">Long integer</span></span><br/> <span data-ttu-id="78997-202">Hexadécimal : 0x0400</span><span class="sxs-lookup"><span data-stu-id="78997-202">Hexadecimal: 0x0400</span></span><br/> <span data-ttu-id="78997-203">Décimal : 1024</span><span class="sxs-lookup"><span data-stu-id="78997-203">Decimal: 1024</span></span><br/> <span data-ttu-id="78997-204">Entier Short</span><span class="sxs-lookup"><span data-stu-id="78997-204">Short integer</span></span><br/> <span data-ttu-id="78997-205">Hexadécimal : 0x0800</span><span class="sxs-lookup"><span data-stu-id="78997-205">Hexadecimal: 0x0800</span></span><br/> <span data-ttu-id="78997-206">Décimal : 2048</span><span class="sxs-lookup"><span data-stu-id="78997-206">Decimal: 2048</span></span><br/> <span data-ttu-id="78997-207">Objet binaire</span><span class="sxs-lookup"><span data-stu-id="78997-207">Binary object</span></span><br/> <span data-ttu-id="78997-208">Hexadécimal : 0x0C00</span><span class="sxs-lookup"><span data-stu-id="78997-208">Hexadecimal: 0x0C00</span></span><br/> <span data-ttu-id="78997-209">Décimal : 3072</span><span class="sxs-lookup"><span data-stu-id="78997-209">Decimal: 3072</span></span><br/> <span data-ttu-id="78997-210">String</span><span class="sxs-lookup"><span data-stu-id="78997-210">String</span></span><br/> |
| <span data-ttu-id="78997-211"><span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12</span><span class="sxs-lookup"><span data-stu-id="78997-211"><span id="Bit_12"></span><span id="bit_12"></span><span id="BIT_12"></span>Bit 12</span></span><br/>              | <span data-ttu-id="78997-212">Hexadécimal : 0x1000</span><span class="sxs-lookup"><span data-stu-id="78997-212">Hexadecimal: 0x1000</span></span><br/> <span data-ttu-id="78997-213">Décimal : 4096</span><span class="sxs-lookup"><span data-stu-id="78997-213">Decimal: 4096</span></span><br/> <span data-ttu-id="78997-214">Colonne Nullable.</span><span class="sxs-lookup"><span data-stu-id="78997-214">Nullable column.</span></span> <span data-ttu-id="78997-215">Zéro signifie que la colonne n’accepte pas les valeurs NULL.</span><span class="sxs-lookup"><span data-stu-id="78997-215">Zero means the column is non-nullable.</span></span><br/>                                                                                                                                                                                               |
| <span data-ttu-id="78997-216"><span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13</span><span class="sxs-lookup"><span data-stu-id="78997-216"><span id="Bit_13"></span><span id="bit_13"></span><span id="BIT_13"></span>Bit 13</span></span><br/>              | <span data-ttu-id="78997-217">Hexadécimal : 0x2000</span><span class="sxs-lookup"><span data-stu-id="78997-217">Hexadecimal: 0x2000</span></span><br/> <span data-ttu-id="78997-218">Décimal : 8192</span><span class="sxs-lookup"><span data-stu-id="78997-218">Decimal: 8192</span></span><br/> <span data-ttu-id="78997-219">Colonne de clé primaire.</span><span class="sxs-lookup"><span data-stu-id="78997-219">Primary key column.</span></span> <span data-ttu-id="78997-220">Zéro signifie que cette colonne n’est pas une clé primaire.</span><span class="sxs-lookup"><span data-stu-id="78997-220">Zero means this column is not a primary key.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="78997-221"><span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bits 14 15</span><span class="sxs-lookup"><span data-stu-id="78997-221"><span id="Bits_1415"></span><span id="bits_1415"></span><span id="BITS_1415"></span>Bits 14 15</span></span><br/> | <span data-ttu-id="78997-222">Hexadécimal : 0x4000 0x8000</span><span class="sxs-lookup"><span data-stu-id="78997-222">Hexadecimal: 0x4000 0x8000</span></span><br/> <span data-ttu-id="78997-223">Décimal : 16384 32768</span><span class="sxs-lookup"><span data-stu-id="78997-223">Decimal: 16384 32768</span></span><br/> <span data-ttu-id="78997-224">Réservé</span><span class="sxs-lookup"><span data-stu-id="78997-224">Reserved</span></span><br/>                                                                                                                                                                                                                                |



 

<span data-ttu-id="78997-225">Pour obtenir un exemple de script qui illustre la \_ table TransformView, consultez [View a Transform](view-a-transform.md).</span><span class="sxs-lookup"><span data-stu-id="78997-225">For a script sample that demonstrates the \_TransformView table, see [View a Transform](view-a-transform.md).</span></span>

 

 




