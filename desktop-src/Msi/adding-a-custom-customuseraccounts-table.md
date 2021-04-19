---
description: Une spécification de l’exemple est que les informations de compte d’utilisateur sont lues à partir d’une table personnalisée dans la base de données d’installation et ne sont pas codées en dur dans l’action personnalisée.
ms.assetid: 1545b4f1-3ccf-4745-90d8-15f1f79d8455
title: Ajout d’une table CustomUserAccounts personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58366c725ecc135b9583c926a16383a5ad5a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525023"
---
# <a name="adding-a-custom-customuseraccounts-table"></a><span data-ttu-id="316ec-103">Ajout d’une table CustomUserAccounts personnalisée</span><span class="sxs-lookup"><span data-stu-id="316ec-103">Adding a Custom CustomUserAccounts Table</span></span>

<span data-ttu-id="316ec-104">Une spécification de l’exemple est que les informations de compte d’utilisateur sont lues à partir d’une table personnalisée dans la base de données d’installation et ne sont pas codées en dur dans l’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="316ec-104">A specification of the sample is that user account information be read from a custom table in the installation database and not hard-coded into the custom action.</span></span>

<span data-ttu-id="316ec-105">Ajoutez une table personnalisée à l’exemple de base de données d’installation nommée CustomUserAccounts pour contenir les informations du compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="316ec-105">Add a custom table to the sample installation database named CustomUserAccounts to hold user account information.</span></span> <span data-ttu-id="316ec-106">Pour obtenir un exemple d’ajout d’une table personnalisée [, consultez Exemples de requêtes de base de données avec SQL et script](examples-of-database-queries-using-sql-and-script.md) .</span><span class="sxs-lookup"><span data-stu-id="316ec-106">See [Examples of Database Queries Using SQL and Script](examples-of-database-queries-using-sql-and-script.md) for an example of how to add a custom table.</span></span> <span data-ttu-id="316ec-107">Utilisez le schéma suivant pour la table CustomUserAccounts.</span><span class="sxs-lookup"><span data-stu-id="316ec-107">Use the following schema for the CustomUserAccounts table.</span></span> <span data-ttu-id="316ec-108">Pour obtenir une explication des types de colonnes, consultez [format de définition de colonne](column-definition-format.md) .</span><span class="sxs-lookup"><span data-stu-id="316ec-108">See [Column Definition Format](column-definition-format.md) for an explanation of the column types.</span></span>



| <span data-ttu-id="316ec-109">Colonne</span><span class="sxs-lookup"><span data-stu-id="316ec-109">Column</span></span>     | <span data-ttu-id="316ec-110">Type</span><span class="sxs-lookup"><span data-stu-id="316ec-110">Type</span></span> | <span data-ttu-id="316ec-111">Clé</span><span class="sxs-lookup"><span data-stu-id="316ec-111">Key</span></span> | <span data-ttu-id="316ec-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="316ec-112">Nullable</span></span> | <span data-ttu-id="316ec-113">Description</span><span class="sxs-lookup"><span data-stu-id="316ec-113">Description</span></span>                                                                                                                                                                                                                                                                                                |
|------------|------|-----|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="316ec-114">UserName</span><span class="sxs-lookup"><span data-stu-id="316ec-114">UserName</span></span>   | <span data-ttu-id="316ec-115">S72</span><span class="sxs-lookup"><span data-stu-id="316ec-115">s72</span></span>  | <span data-ttu-id="316ec-116">O</span><span class="sxs-lookup"><span data-stu-id="316ec-116">Y</span></span>   | <span data-ttu-id="316ec-117">N</span><span class="sxs-lookup"><span data-stu-id="316ec-117">N</span></span>        | <span data-ttu-id="316ec-118">Nom du compte d’utilisateur en cours de création.</span><span class="sxs-lookup"><span data-stu-id="316ec-118">Name of user account being created.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="316ec-119">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="316ec-119">Password</span></span>   | <span data-ttu-id="316ec-120">S72</span><span class="sxs-lookup"><span data-stu-id="316ec-120">s72</span></span>  |     | <span data-ttu-id="316ec-121">N</span><span class="sxs-lookup"><span data-stu-id="316ec-121">N</span></span>        | <span data-ttu-id="316ec-122">Nom de la propriété contenant le mot de passe du compte.</span><span class="sxs-lookup"><span data-stu-id="316ec-122">Name of property containing the password for the account.</span></span> <span data-ttu-id="316ec-123">Il s’agit d’une [propriété publique](public-properties.md) définie sur la ligne de commande ou par le biais d’un [contrôle d’édition](edit-control.md) dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="316ec-123">This is a [public property](public-properties.md) set on the command line or through an [edit control](edit-control.md) in the user interface.</span></span> <span data-ttu-id="316ec-124">Ce contrôle d’édition doit avoir l' [attribut de contrôle de mot de passe](password-control-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="316ec-124">This edit control should have the [Password Control Attribute](password-control-attribute.md).</span></span> |
| <span data-ttu-id="316ec-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="316ec-125">Attributes</span></span> | <span data-ttu-id="316ec-126">i4</span><span class="sxs-lookup"><span data-stu-id="316ec-126">i4</span></span>   |     | <span data-ttu-id="316ec-127">O</span><span class="sxs-lookup"><span data-stu-id="316ec-127">Y</span></span>        | <span data-ttu-id="316ec-128">Attributs du compte.</span><span class="sxs-lookup"><span data-stu-id="316ec-128">Attributes for account.</span></span> <span data-ttu-id="316ec-129">Celles-ci sont définies en tant que valeurs **DWORD** pour le \_ membre indicateurs usri1 de la \_ structure informations utilisateur \_ 1.</span><span class="sxs-lookup"><span data-stu-id="316ec-129">These are defined as the **DWORD** values for the usri1\_flags member of the USER\_INFO\_1 structure.</span></span>                                                                                                                                                                              |



 

<span data-ttu-id="316ec-130">Une fois la table CustomUserAccounts ajoutée à la base de données, vous pouvez modifier cette table à l’aide d’Orca, un éditeur de tables fourni avec le kit de développement logiciel (SDK) Windows Installer, ou un autre éditeur.</span><span class="sxs-lookup"><span data-stu-id="316ec-130">After the CustomUserAccounts table has been added to the database you may edit this table using Orca, a table editor provided with the Windows Installer SDK, or another editor.</span></span> <span data-ttu-id="316ec-131">Entrez l’enregistrement suivant dans la table CustomUserAccounts pour créer un compte d’utilisateur sécurisé par mot de passe pour un utilisateur nommé TestUser.</span><span class="sxs-lookup"><span data-stu-id="316ec-131">Enter the following record in the CustomUserAccounts table to create a password secured user account for a user called TestUser.</span></span> <span data-ttu-id="316ec-132">Notez que 512 est la valeur numérique du \_ compte normal UF \_ .</span><span class="sxs-lookup"><span data-stu-id="316ec-132">Note that 512 is the numeric value for UF\_NORMAL\_ACCOUNT.</span></span>

<span data-ttu-id="316ec-133">Table CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="316ec-133">CustomUserAccounts Table</span></span>



| <span data-ttu-id="316ec-134">UserName</span><span class="sxs-lookup"><span data-stu-id="316ec-134">UserName</span></span> | <span data-ttu-id="316ec-135">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="316ec-135">Password</span></span>         | <span data-ttu-id="316ec-136">Attributs</span><span class="sxs-lookup"><span data-stu-id="316ec-136">Attributes</span></span> |
|----------|------------------|------------|
| <span data-ttu-id="316ec-137">UtilisateurTest</span><span class="sxs-lookup"><span data-stu-id="316ec-137">TestUser</span></span> | <span data-ttu-id="316ec-138">TESTUSERPASSWORD</span><span class="sxs-lookup"><span data-stu-id="316ec-138">TESTUSERPASSWORD</span></span> | <span data-ttu-id="316ec-139">512</span><span class="sxs-lookup"><span data-stu-id="316ec-139">512</span></span>        |



 

<span data-ttu-id="316ec-140">Ajoutez les enregistrements suivants au \_ tableau de validation pour la table personnalisée.</span><span class="sxs-lookup"><span data-stu-id="316ec-140">Add the following records to the \_Validation table for the custom table.</span></span>

[<span data-ttu-id="316ec-141">\_Tableau de validation</span><span class="sxs-lookup"><span data-stu-id="316ec-141">\_Validation Table</span></span>](-validation-table.md)



| <span data-ttu-id="316ec-142">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="316ec-142">Table</span></span>              | <span data-ttu-id="316ec-143">Colonne</span><span class="sxs-lookup"><span data-stu-id="316ec-143">Column</span></span>     | <span data-ttu-id="316ec-144">Nullable</span><span class="sxs-lookup"><span data-stu-id="316ec-144">Nullable</span></span> | <span data-ttu-id="316ec-145">MinValue</span><span class="sxs-lookup"><span data-stu-id="316ec-145">MinValue</span></span> | <span data-ttu-id="316ec-146">MaxValue</span><span class="sxs-lookup"><span data-stu-id="316ec-146">MaxValue</span></span>   | <span data-ttu-id="316ec-147">Keytable</span><span class="sxs-lookup"><span data-stu-id="316ec-147">KeyTable</span></span> | <span data-ttu-id="316ec-148">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="316ec-148">KeyColumn</span></span> | <span data-ttu-id="316ec-149">Category</span><span class="sxs-lookup"><span data-stu-id="316ec-149">Category</span></span>                     | <span data-ttu-id="316ec-150">Définissez</span><span class="sxs-lookup"><span data-stu-id="316ec-150">Set</span></span> | <span data-ttu-id="316ec-151">Description</span><span class="sxs-lookup"><span data-stu-id="316ec-151">Description</span></span> |
|--------------------|------------|----------|----------|------------|----------|-----------|------------------------------|-----|-------------|
| <span data-ttu-id="316ec-152">CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="316ec-152">CustomUserAccounts</span></span> | <span data-ttu-id="316ec-153">UserName</span><span class="sxs-lookup"><span data-stu-id="316ec-153">UserName</span></span>   | <span data-ttu-id="316ec-154">N</span><span class="sxs-lookup"><span data-stu-id="316ec-154">N</span></span>        |          |            |          |           | [<span data-ttu-id="316ec-155">Text</span><span class="sxs-lookup"><span data-stu-id="316ec-155">Text</span></span>](text.md)             |     |             |
| <span data-ttu-id="316ec-156">CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="316ec-156">CustomUserAccounts</span></span> | <span data-ttu-id="316ec-157">Mot de passe</span><span class="sxs-lookup"><span data-stu-id="316ec-157">Password</span></span>   | <span data-ttu-id="316ec-158">N</span><span class="sxs-lookup"><span data-stu-id="316ec-158">N</span></span>        |          |            |          |           | [<span data-ttu-id="316ec-159">Identificateur</span><span class="sxs-lookup"><span data-stu-id="316ec-159">Identifier</span></span>](identifier.md) |     |             |
| <span data-ttu-id="316ec-160">CustomUserAccounts</span><span class="sxs-lookup"><span data-stu-id="316ec-160">CustomUserAccounts</span></span> | <span data-ttu-id="316ec-161">Attributs</span><span class="sxs-lookup"><span data-stu-id="316ec-161">Attributes</span></span> | <span data-ttu-id="316ec-162">O</span><span class="sxs-lookup"><span data-stu-id="316ec-162">Y</span></span>        | <span data-ttu-id="316ec-163">0</span><span class="sxs-lookup"><span data-stu-id="316ec-163">0</span></span>        | <span data-ttu-id="316ec-164">2147483647</span><span class="sxs-lookup"><span data-stu-id="316ec-164">2147483647</span></span> |          |           | <span data-ttu-id="316ec-165">null</span><span class="sxs-lookup"><span data-stu-id="316ec-165">null</span></span>                         |     |             |



 

<span data-ttu-id="316ec-166">Continuez à [créer les tables ActionText et Error](authoring-the-actiontext-and-error-tables.md).</span><span class="sxs-lookup"><span data-stu-id="316ec-166">Continue to [Authoring the ActionText and Error Tables](authoring-the-actiontext-and-error-tables.md).</span></span>

 

 



