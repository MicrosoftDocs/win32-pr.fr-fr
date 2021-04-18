---
description: Le \_ tableau Streams répertorie les flux de données OLE incorporés. Il s’agit d’une table temporaire, créée uniquement lorsqu’elle est référencée par une instruction SQL.
ms.assetid: 1e30472d-6ba5-410a-a81b-07ed225dcb69
title: Table _Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9607097b32acc8a3c2350a00db0b9721a4aa353
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519069"
---
# <a name="_streams-table"></a><span data-ttu-id="ee328-104">\_Table Streams</span><span class="sxs-lookup"><span data-stu-id="ee328-104">\_Streams Table</span></span>

<span data-ttu-id="ee328-105">Le \_ tableau Streams répertorie les flux de données OLE incorporés.</span><span class="sxs-lookup"><span data-stu-id="ee328-105">The \_Streams table lists embedded OLE data streams.</span></span> <span data-ttu-id="ee328-106">Il s’agit d’une table temporaire, créée uniquement lorsqu’elle est référencée par une instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="ee328-106">This is a temporary table, created only when referenced by a SQL statement.</span></span>



| <span data-ttu-id="ee328-107">Colonne</span><span class="sxs-lookup"><span data-stu-id="ee328-107">Column</span></span> | <span data-ttu-id="ee328-108">Type</span><span class="sxs-lookup"><span data-stu-id="ee328-108">Type</span></span>                 | <span data-ttu-id="ee328-109">Clé</span><span class="sxs-lookup"><span data-stu-id="ee328-109">Key</span></span> | <span data-ttu-id="ee328-110">Nullable</span><span class="sxs-lookup"><span data-stu-id="ee328-110">Nullable</span></span> |
|--------|----------------------|-----|----------|
| <span data-ttu-id="ee328-111">Nom</span><span class="sxs-lookup"><span data-stu-id="ee328-111">Name</span></span>   | [<span data-ttu-id="ee328-112">Text</span><span class="sxs-lookup"><span data-stu-id="ee328-112">Text</span></span>](text.md)     | <span data-ttu-id="ee328-113">O</span><span class="sxs-lookup"><span data-stu-id="ee328-113">Y</span></span>   | <span data-ttu-id="ee328-114">N</span><span class="sxs-lookup"><span data-stu-id="ee328-114">N</span></span>        |
| <span data-ttu-id="ee328-115">Données</span><span class="sxs-lookup"><span data-stu-id="ee328-115">Data</span></span>   | [<span data-ttu-id="ee328-116">Binaire</span><span class="sxs-lookup"><span data-stu-id="ee328-116">Binary</span></span>](binary.md) | <span data-ttu-id="ee328-117">N</span><span class="sxs-lookup"><span data-stu-id="ee328-117">N</span></span>   | <span data-ttu-id="ee328-118">O</span><span class="sxs-lookup"><span data-stu-id="ee328-118">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ee328-119">Colonnes</span><span class="sxs-lookup"><span data-stu-id="ee328-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ee328-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme</span><span class="sxs-lookup"><span data-stu-id="ee328-120"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="ee328-121">Clé unique qui identifie le flux.</span><span class="sxs-lookup"><span data-stu-id="ee328-121">A unique key that identifies the stream.</span></span> <span data-ttu-id="ee328-122">La longueur maximale du nom est de 62 caractères.</span><span class="sxs-lookup"><span data-stu-id="ee328-122">The maximum length of Name is 62 characters.</span></span>

</dd> <dt>

<span data-ttu-id="ee328-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Métadonnée</span><span class="sxs-lookup"><span data-stu-id="ee328-123"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="ee328-124">Données binaires non mises en forme.</span><span class="sxs-lookup"><span data-stu-id="ee328-124">The unformatted binary data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee328-125">Notes</span><span class="sxs-lookup"><span data-stu-id="ee328-125">Remarks</span></span>

<span data-ttu-id="ee328-126">Pour copier un flux de données OLE (par exemple, un objet de type de données [Binary](binary.md) ) à partir d’un fichier dans une base de données, créez un enregistrement dans la \_ table Streams et entrez le nom du flux de données dans la colonne Name de cet enregistrement, puis copiez les données du fichier dans la colonne de données à l’aide de [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama).</span><span class="sxs-lookup"><span data-stu-id="ee328-126">To copy an OLE data stream (for example, an object of the [Binary](binary.md) data type) from a file into a database, create a record in the \_Streams table and enter the name of the data stream into the Name column of this record and copy the data from the file into the Data column using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama).</span></span> <span data-ttu-id="ee328-127">Utilisez [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) pour insérer le nouvel enregistrement dans la table.</span><span class="sxs-lookup"><span data-stu-id="ee328-127">Use [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the new record into the table.</span></span>

<span data-ttu-id="ee328-128">Pour lire un flux de données binaires incorporé dans une base de données, utilisez une requête SQL pour rechercher et extraire l’enregistrement contenant les données binaires.</span><span class="sxs-lookup"><span data-stu-id="ee328-128">To read a binary data stream embedded in a database, use a SQL query to find and to fetch the record containing the binary data.</span></span> <span data-ttu-id="ee328-129">Utilisez [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) pour lire les données binaires dans une mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="ee328-129">Use [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) to read the binary data into a buffer.</span></span>

<span data-ttu-id="ee328-130">Pour déplacer un flux de données binaires d’une base de données vers une autre, exportez d’abord les données dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="ee328-130">To move a binary data stream from one database to another, first export the data to a file.</span></span> <span data-ttu-id="ee328-131">Utilisez une requête SQL pour rechercher le flux de données dans le fichier et utilisez [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) pour copier les données du fichier dans la colonne de données de \_ la table Streams de la deuxième base de données.</span><span class="sxs-lookup"><span data-stu-id="ee328-131">Use a SQL query to find the data stream in the file and use [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) to copy the data from the file into Data column of \_Streams table of the second database.</span></span> <span data-ttu-id="ee328-132">Cela garantit que chaque base de données possède sa propre copie des données binaires.</span><span class="sxs-lookup"><span data-stu-id="ee328-132">This ensures that each database has its own copy of the binary data.</span></span> <span data-ttu-id="ee328-133">Vous ne pouvez pas déplacer des données binaires d’une base de données vers une autre simplement en extrayant un enregistrement avec les données de la première base de données et en l’insérant dans la deuxième base de données.</span><span class="sxs-lookup"><span data-stu-id="ee328-133">You cannot move binary data from one database to another simply by fetching a record with the data from the first database and inserting it into the second database.</span></span>

<span data-ttu-id="ee328-134">Pour supprimer un flux de données, récupérez l’enregistrement et affectez la valeur null à la colonne de données avant de mettre à jour l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ee328-134">To delete a data stream, fetch the record and set the Data column to null before updating the record.</span></span> <span data-ttu-id="ee328-135">Une autre méthode consiste à supprimer l’enregistrement de la table, en le supprimant à l’aide de [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ou d’une requête SQL simple.</span><span class="sxs-lookup"><span data-stu-id="ee328-135">Another method is to remove the record from the table, deleting it using either [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) or a plain SQL query.</span></span> <span data-ttu-id="ee328-136">Un flux ne doit pas être extrait dans un enregistrement si le flux est supprimé de la table.</span><span class="sxs-lookup"><span data-stu-id="ee328-136">A stream should not be fetched into a record if the stream is deleted from the table.</span></span>

<span data-ttu-id="ee328-137">Pour renommer un flux de données OLE, mettez à jour la colonne « Name » de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ee328-137">To rename an OLE data stream, update the 'Name' column of the record.</span></span>

<span data-ttu-id="ee328-138">Si un blocage est placé sur cette table à l’aide de SQL (ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="ee328-138">If a hold is placed on this table using SQL (ALTER TABLE</span></span> <table> <span data-ttu-id="ee328-139">HOLD) ou une colonne est ajoutée avec HOLD, la table doit être libérée à l’aide de FREE.</span><span class="sxs-lookup"><span data-stu-id="ee328-139">HOLD) or a column is added with HOLD, the table must be released using FREE.</span></span> <span data-ttu-id="ee328-140">Les flux ne sont pas écrits tant que la table n’a pas été libérée ou validée.</span><span class="sxs-lookup"><span data-stu-id="ee328-140">Streams are not written until the table has been released or committed.</span></span>

 

 



