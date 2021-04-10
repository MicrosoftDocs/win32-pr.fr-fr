---
description: Vous trouverez un exemple d’utilisation de requêtes de base de données basées sur des scripts dans le kit de développement logiciel (SDK) Windows Installer, car l’utilitaire WiRunSQL.vbs.
ms.assetid: aa38dbe5-411d-432e-b3fe-09994fc59c75
title: Exemples de requêtes de base de données utilisant SQL et script
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbd839151b40ddd5e9a265c6c370c27a4a9fd125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755628"
---
# <a name="examples-of-database-queries-using-sql-and-script"></a><span data-ttu-id="359f4-103">Exemples de requêtes de base de données utilisant SQL et script</span><span class="sxs-lookup"><span data-stu-id="359f4-103">Examples of Database Queries Using SQL and Script</span></span>

<span data-ttu-id="359f4-104">Vous trouverez un exemple d’utilisation de requêtes de base de données basées sur des scripts dans le [Kit de développement logiciel](platform-sdk-components-for-windows-installer-developers.md) (SDK) Windows Installer en tant qu' WiRunSQL.vbs de l’utilitaire.</span><span class="sxs-lookup"><span data-stu-id="359f4-104">An example of using script-driven database queries is provided in the Windows [Installer Software Development Kit](platform-sdk-components-for-windows-installer-developers.md) (SDK) as the utility WiRunSQL.vbs.</span></span> <span data-ttu-id="359f4-105">Cet utilitaire gère les requêtes de base de données à l’aide de la version Windows Installer de SQL décrite dans la section [syntaxe SQL](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="359f4-105">This utility handles database queries using the Windows Installer version of SQL described in the section [SQL Syntax](sql-syntax.md).</span></span>

<span data-ttu-id="359f4-106">**Supprimer un enregistrement d’une table**</span><span class="sxs-lookup"><span data-stu-id="359f4-106">**Delete a record from a table**</span></span>

<span data-ttu-id="359f4-107">La ligne de commande suivante supprime l’enregistrement dont la clé primaire est rouge de la table des [fonctionnalités](feature-table.md) de la base de données Test.msi.</span><span class="sxs-lookup"><span data-stu-id="359f4-107">The following command line deletes the record having the primary key RED from the [Feature](feature-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="359f4-108">**Cscript WiRunSQL.vbs Test.msi fonctionnalité «supprimer de la \` fonctionnalité \` where \` \` . \` Feature \` = 'Red' "**</span><span class="sxs-lookup"><span data-stu-id="359f4-108">**Cscript WiRunSQL.vbs Test.msi "DELETE FROM \`Feature\` WHERE \`Feature\`.\`Feature\`='RED'"**</span></span>

<span data-ttu-id="359f4-109">**Ajouter une table à une base de données**</span><span class="sxs-lookup"><span data-stu-id="359f4-109">**Add a table to a database**</span></span>

<span data-ttu-id="359f4-110">La ligne de commande suivante ajoute la table de [répertoires](directory-table.md) à la base de données Test.msi.</span><span class="sxs-lookup"><span data-stu-id="359f4-110">The following command line adds the [Directory](directory-table.md) table to the Test.msi database.</span></span>

<span data-ttu-id="359f4-111">**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \` Directory \` ( \` répertoire \` char (72) not null, \` répertoire \_ parent \` char (72), \` DefaultDir \` char (255) not null répertoire de clé primaire localisable \` \` )"**</span><span class="sxs-lookup"><span data-stu-id="359f4-111">**CScript WiRunSQL.vbs Test.msi "CREATE TABLE \`Directory\` (\`Directory\` CHAR(72) NOT NULL, \`Directory\_Parent\` CHAR(72), \`DefaultDir\` CHAR(255) NOT NULL LOCALIZABLE PRIMARY KEY \`Directory\`)"**</span></span>

<span data-ttu-id="359f4-112">**Supprimer une table d’une base de données**</span><span class="sxs-lookup"><span data-stu-id="359f4-112">**Remove a table from a database**</span></span>

<span data-ttu-id="359f4-113">La ligne de commande suivante supprime la table des [fonctionnalités](feature-table.md) de la base de données Test.msi.</span><span class="sxs-lookup"><span data-stu-id="359f4-113">The following command line removes the [Feature](feature-table.md) table from the Test.msi database.</span></span>

<span data-ttu-id="359f4-114">**Cscript WiRunSQL.vbs Test.msi « supprimer la \` fonctionnalité de table \` »**</span><span class="sxs-lookup"><span data-stu-id="359f4-114">**Cscript WiRunSQL.vbs Test.msi "DROP TABLE \`Feature\`"**</span></span>

<span data-ttu-id="359f4-115">**Ajouter une nouvelle colonne à une table**</span><span class="sxs-lookup"><span data-stu-id="359f4-115">**Add a new column to a table**</span></span>

<span data-ttu-id="359f4-116">La ligne de commande suivante ajoute la colonne test à la table [CustomAction](customaction-table.md) de la base de données Test.msi.</span><span class="sxs-lookup"><span data-stu-id="359f4-116">The following command line adds the Test column to the [CustomAction](customaction-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="359f4-117">**CScript WiRunSQL.vbs Test.msi « ALTER TABLE \` CustomAction \` Add \` test \` Integer »**</span><span class="sxs-lookup"><span data-stu-id="359f4-117">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`CustomAction\` ADD \`Test\` INTEGER"**</span></span>

<span data-ttu-id="359f4-118">**Insérer un nouvel enregistrement dans une table**</span><span class="sxs-lookup"><span data-stu-id="359f4-118">**Insert a new record into a table**</span></span>

<span data-ttu-id="359f4-119">La ligne de commande suivante insère un nouvel enregistrement dans la table des [fonctionnalités](feature-table.md) de la base de données Test.msi.</span><span class="sxs-lookup"><span data-stu-id="359f4-119">The following command line inserts a new record into the [Feature](feature-table.md) table of the Test.msi database.</span></span>

<span data-ttu-id="359f4-120">**Cscript WiRunSQL.vbs Test.msi fonctionnalité d’insertion \` \` ( \` fonctionnalité) \` . \` Fonctionnalité \` \` \` . \` Fonction \_ parente \` , \` fonctionnalité \` . \` Titre \` , \` fonctionnalité \` . \` Description \` , \` fonctionnalité \` . \` Affichage \` , \` fonctionnalité \` . \` Niveau \` , \` fonctionnalité \` . \` Répertoire \_ \` , \` fonctionnalité \` . \` Valeurs d’attribut \` ) (« tennis », « sport », « tennis », « tournoi », 25, 3, « SPORTDIR », 2)»**</span><span class="sxs-lookup"><span data-stu-id="359f4-120">**Cscript WiRunSQL.vbs Test.msi "INSERT INTO \`Feature\` (\`Feature\`.\`Feature\`,\`Feature\`.\`Feature\_Parent\`,\`Feature\`.\`Title\`,\`Feature\`.\`Description\`, \`Feature\`.\`Display\`,\`Feature\`.\`Level\`,\`Feature\`.\`Directory\_\`,\`Feature\`.\`Attributes\`) VALUES ('Tennis','Sport','Tennis','Tournament',25,3,'SPORTDIR',2)"**</span></span>

<span data-ttu-id="359f4-121">Cela insère l’enregistrement suivant dans la table des [fonctionnalités](feature-table.md) de Test.msi.</span><span class="sxs-lookup"><span data-stu-id="359f4-121">This inserts the following record into the [Feature](feature-table.md) table of Test.msi.</span></span>

<span data-ttu-id="359f4-122">[Fonctionnalité](feature-table.md) Tableau</span><span class="sxs-lookup"><span data-stu-id="359f4-122">[Feature](feature-table.md) Table</span></span>



| <span data-ttu-id="359f4-123">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="359f4-123">Feature</span></span> | <span data-ttu-id="359f4-124">Parent de la fonctionnalité \_</span><span class="sxs-lookup"><span data-stu-id="359f4-124">Feature\_Parent</span></span> | <span data-ttu-id="359f4-125">Intitulé</span><span class="sxs-lookup"><span data-stu-id="359f4-125">Title</span></span>  | <span data-ttu-id="359f4-126">Description</span><span class="sxs-lookup"><span data-stu-id="359f4-126">Description</span></span> | <span data-ttu-id="359f4-127">Afficher</span><span class="sxs-lookup"><span data-stu-id="359f4-127">Display</span></span> | <span data-ttu-id="359f4-128">Level</span><span class="sxs-lookup"><span data-stu-id="359f4-128">Level</span></span> | <span data-ttu-id="359f4-129">Répertoire\_</span><span class="sxs-lookup"><span data-stu-id="359f4-129">Directory\_</span></span> | <span data-ttu-id="359f4-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="359f4-130">Attributes</span></span> |
|---------|-----------------|--------|-------------|---------|-------|-------------|------------|
| <span data-ttu-id="359f4-131">Tennis</span><span class="sxs-lookup"><span data-stu-id="359f4-131">Tennis</span></span>  | <span data-ttu-id="359f4-132">Sport</span><span class="sxs-lookup"><span data-stu-id="359f4-132">Sport</span></span>           | <span data-ttu-id="359f4-133">Tennis</span><span class="sxs-lookup"><span data-stu-id="359f4-133">Tennis</span></span> | <span data-ttu-id="359f4-134">Oppos</span><span class="sxs-lookup"><span data-stu-id="359f4-134">Tournament</span></span>  | <span data-ttu-id="359f4-135">25</span><span class="sxs-lookup"><span data-stu-id="359f4-135">25</span></span>      | <span data-ttu-id="359f4-136">3</span><span class="sxs-lookup"><span data-stu-id="359f4-136">3</span></span>     | <span data-ttu-id="359f4-137">SPORTDIR</span><span class="sxs-lookup"><span data-stu-id="359f4-137">SPORTDIR</span></span>    | <span data-ttu-id="359f4-138">2</span><span class="sxs-lookup"><span data-stu-id="359f4-138">2</span></span>          |



 

<span data-ttu-id="359f4-139">Notez que les données binaires ne peuvent pas être insérées directement dans une table à l’aide de l’instruction INSERT INTO ou de la mise à jour de requêtes SQL.</span><span class="sxs-lookup"><span data-stu-id="359f4-139">Note that binary data cannot be inserted into a table directly using the INSERT INTO or UPDATE SQL queries.</span></span> <span data-ttu-id="359f4-140">Pour plus d’informations, consultez [Ajout de données binaires à une table à l’aide de SQL](adding-binary-data-to-a-table-using-sql.md).</span><span class="sxs-lookup"><span data-stu-id="359f4-140">For information see [Adding Binary Data to a Table Using SQL](adding-binary-data-to-a-table-using-sql.md).</span></span>

<span data-ttu-id="359f4-141">**Modifier un enregistrement existant dans une table**</span><span class="sxs-lookup"><span data-stu-id="359f4-141">**Modify an existing record in a table**</span></span>

<span data-ttu-id="359f4-142">La ligne de commande suivante remplace la valeur existante dans le champ titre par « performances ».</span><span class="sxs-lookup"><span data-stu-id="359f4-142">The following command line changes the existing value in the Title field to "Performances."</span></span> <span data-ttu-id="359f4-143">L’enregistrement mis à jour comporte « arts » comme clé primaire et figure dans la table des fonctionnalités de la base de données Test.msi.</span><span class="sxs-lookup"><span data-stu-id="359f4-143">The updated record has "Arts" as its primary key and is in the Feature table of the Test.msi database.</span></span>

<span data-ttu-id="359f4-144">**Cscript WiRunSQL.vbs Test.msi «mettre à jour la \` fonctionnalité de jeu de fonctionnalités \` \` \` . \` Title \` = « performance » où se trouve la \` fonctionnalité \` . \` Fonctionnalité \` = « Arts »**</span><span class="sxs-lookup"><span data-stu-id="359f4-144">**Cscript WiRunSQL.vbs Test.msi "UPDATE \`Feature\` SET \`Feature\`.\`Title\`='Performances' WHERE \`Feature\`.\`Feature\`='Arts'"**</span></span>

<span data-ttu-id="359f4-145">**Sélectionner un groupe d’enregistrements**</span><span class="sxs-lookup"><span data-stu-id="359f4-145">**Select a group of records**</span></span>

<span data-ttu-id="359f4-146">La ligne de commande suivante sélectionne le nom et le type de tous les contrôles qui appartiennent au ErrorDialog dans la base de données Test.msi.</span><span class="sxs-lookup"><span data-stu-id="359f4-146">The following command line selects the name and type of all controls that belong to the ErrorDialog in the Test.msi database.</span></span>

<span data-ttu-id="359f4-147">**CScript WiRunSQL.vbs Test.msi « sélectionner \` le contrôle \` , \` tapez \` à partir du \` contrôle \` où boîte de \` dialogue \_ \` = «ErrorDialog »»**</span><span class="sxs-lookup"><span data-stu-id="359f4-147">**CScript WiRunSQL.vbs Test.msi "SELECT \`Control\`, \`Type\` FROM \`Control\` WHERE \`Dialog\_\`='ErrorDialog' "**</span></span>

<span data-ttu-id="359f4-148">**Conserver une table en mémoire**</span><span class="sxs-lookup"><span data-stu-id="359f4-148">**Hold a table in memory**</span></span>

<span data-ttu-id="359f4-149">La ligne de commande suivante verrouille la table des [composants](component-table.md) de la base de données Test.msi en mémoire.</span><span class="sxs-lookup"><span data-stu-id="359f4-149">The following command line locks the [Component](component-table.md) table of the Test.msi database in memory.</span></span>

<span data-ttu-id="359f4-150">**CScript WiRunSQL.vbs Test.msi « ALTER TABLE \` Component \` Hold »**</span><span class="sxs-lookup"><span data-stu-id="359f4-150">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`Component\` HOLD"**</span></span>

<span data-ttu-id="359f4-151">**Libérer une table en mémoire**</span><span class="sxs-lookup"><span data-stu-id="359f4-151">**Free a table in memory**</span></span>

<span data-ttu-id="359f4-152">La ligne de commande suivante libère la table des [composants](component-table.md) de la base de données Test.msi à partir de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="359f4-152">The following command line frees the [Component](component-table.md) table of the Test.msi database from memory.</span></span>

<span data-ttu-id="359f4-153">**CScript WiRunSQL.vbs Test.msi « ALTER TABLE \` Component \` Free »**</span><span class="sxs-lookup"><span data-stu-id="359f4-153">**CScript WiRunSQL.vbs Test.msi "ALTER TABLE \`Component\` FREE"**</span></span>

 

 



