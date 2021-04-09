---
description: Le \_ tableau stockages répertorie les stockages de données OLE incorporés. Il s’agit d’une table temporaire, créée uniquement lorsqu’elle est référencée par une instruction SQL.
ms.assetid: b2f2907d-6966-4b63-9589-c1580f8db574
title: Table _Storages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27995dd61c7d25100fc0e1ae2297695e361f44f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864549"
---
# <a name="_storages-table"></a><span data-ttu-id="3a71b-104">\_Table de stockage</span><span class="sxs-lookup"><span data-stu-id="3a71b-104">\_Storages Table</span></span>

<span data-ttu-id="3a71b-105">Le \_ tableau stockages répertorie les stockages de données OLE incorporés.</span><span class="sxs-lookup"><span data-stu-id="3a71b-105">The \_Storages table lists embedded OLE data storages.</span></span> <span data-ttu-id="3a71b-106">Il s’agit d’une table temporaire, créée uniquement lorsqu’elle est référencée par une instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="3a71b-106">This is a temporary table, created only when referenced by a SQL statement.</span></span>



| <span data-ttu-id="3a71b-107">Colonne</span><span class="sxs-lookup"><span data-stu-id="3a71b-107">Column</span></span> | <span data-ttu-id="3a71b-108">Type</span><span class="sxs-lookup"><span data-stu-id="3a71b-108">Type</span></span>                 | <span data-ttu-id="3a71b-109">Clé</span><span class="sxs-lookup"><span data-stu-id="3a71b-109">Key</span></span> | <span data-ttu-id="3a71b-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="3a71b-110">Nullable</span></span> |
|--------|----------------------|-----|----------|
| <span data-ttu-id="3a71b-111">Nom</span><span class="sxs-lookup"><span data-stu-id="3a71b-111">Name</span></span>   | [<span data-ttu-id="3a71b-112">Text</span><span class="sxs-lookup"><span data-stu-id="3a71b-112">Text</span></span>](text.md)     | <span data-ttu-id="3a71b-113">O</span><span class="sxs-lookup"><span data-stu-id="3a71b-113">Y</span></span>   | <span data-ttu-id="3a71b-114">N</span><span class="sxs-lookup"><span data-stu-id="3a71b-114">N</span></span>        |
| <span data-ttu-id="3a71b-115">Données</span><span class="sxs-lookup"><span data-stu-id="3a71b-115">Data</span></span>   | [<span data-ttu-id="3a71b-116">Binaire</span><span class="sxs-lookup"><span data-stu-id="3a71b-116">Binary</span></span>](binary.md) | <span data-ttu-id="3a71b-117">N</span><span class="sxs-lookup"><span data-stu-id="3a71b-117">N</span></span>   | <span data-ttu-id="3a71b-118">O</span><span class="sxs-lookup"><span data-stu-id="3a71b-118">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="3a71b-119">Colonnes</span><span class="sxs-lookup"><span data-stu-id="3a71b-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="3a71b-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme</span><span class="sxs-lookup"><span data-stu-id="3a71b-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="3a71b-121">Clé unique qui identifie le stockage.</span><span class="sxs-lookup"><span data-stu-id="3a71b-121">A unique key that identifies the storage.</span></span> <span data-ttu-id="3a71b-122">La longueur maximale du nom est de 31 caractères.</span><span class="sxs-lookup"><span data-stu-id="3a71b-122">The maximum length of Name is 31 characters.</span></span>

</dd> <dt>

<span data-ttu-id="3a71b-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Métadonnée</span><span class="sxs-lookup"><span data-stu-id="3a71b-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="3a71b-124">Données binaires non mises en forme.</span><span class="sxs-lookup"><span data-stu-id="3a71b-124">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3a71b-125">Notes</span><span class="sxs-lookup"><span data-stu-id="3a71b-125">Remarks</span></span>

<span data-ttu-id="3a71b-126">Pour ajouter un stockage OLE à une base de données, créez un nouvel enregistrement dans la \_ table de stockage et entrez le nom du stockage dans la colonne nom.</span><span class="sxs-lookup"><span data-stu-id="3a71b-126">To add an OLE storage to a database, create a new record in the \_Storages table and enter the name of the storage into the Name column.</span></span> <span data-ttu-id="3a71b-127">Utilisez [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) pour copier des données dans la colonne de données de cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="3a71b-127">Use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) to copy data into the Data column of this record.</span></span> <span data-ttu-id="3a71b-128">Enfin, utilisez [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) pour insérer l’enregistrement dans la \_ table storages.</span><span class="sxs-lookup"><span data-stu-id="3a71b-128">Finally, use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the \_Storages table.</span></span>

<span data-ttu-id="3a71b-129">Les données ne peuvent pas être lues à partir de la \_ table de stockage.</span><span class="sxs-lookup"><span data-stu-id="3a71b-129">Data cannot be read from the \_Storages table.</span></span> <span data-ttu-id="3a71b-130">Toutefois, la \_ table de stockage peut être interrogée pour vérifier l’existence d’un stockage spécifique.</span><span class="sxs-lookup"><span data-stu-id="3a71b-130">However, the \_Storages table can be queried to check for the existence of a specific storage.</span></span> <span data-ttu-id="3a71b-131">Cela signifie qu’il n’est pas possible de déplacer un stockage OLE d’une base de données vers une autre.</span><span class="sxs-lookup"><span data-stu-id="3a71b-131">This means that it is not possible to move an OLE storage from one database to another.</span></span> <span data-ttu-id="3a71b-132">Au lieu de cela, vous devez importer le fichier de stockage d’origine dans la nouvelle base de données. Pour supprimer un stockage OLE, récupérez l’enregistrement contenant les données binaires, affectez la valeur null à la colonne de données de la \_ table storages, puis mettez à jour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="3a71b-132">You must instead import the original storage file into the new database.To delete an OLE storage, fetch the record containing the binary data, set the Data column in the \_Storages table to null, and then update the record.</span></span> <span data-ttu-id="3a71b-133">Une autre méthode consiste simplement à supprimer l’enregistrement à l’aide de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ou d’une requête SQL simple.</span><span class="sxs-lookup"><span data-stu-id="3a71b-133">An alternative method is to simply delete the record using either [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) or a plain SQL query.</span></span>

<span data-ttu-id="3a71b-134">Pour renommer un stockage OLE, mettez à jour la colonne Name de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="3a71b-134">To rename an OLE storage, update the Name column of the record.</span></span>

<span data-ttu-id="3a71b-135">Si un blocage est placé sur cette table à l’aide de SQL (ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="3a71b-135">If a hold is placed on this table using SQL (ALTER TABLE</span></span> <table> <span data-ttu-id="3a71b-136">HOLD) ou une colonne est ajoutée avec HOLD, la table doit être libérée à l’aide de FREE.</span><span class="sxs-lookup"><span data-stu-id="3a71b-136">HOLD) or a column is added with HOLD, the table must be released using FREE.</span></span> <span data-ttu-id="3a71b-137">Les stockages ne sont pas écrits tant que la table n’a pas été libérée ou validée.</span><span class="sxs-lookup"><span data-stu-id="3a71b-137">Storages are not written until the table has been released or committed.</span></span>

 

 



