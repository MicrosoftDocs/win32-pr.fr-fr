---
description: Étant donné que le programme d’installation utilise une base de données relationnelle, il existe des fonctions permettant d’effectuer des requêtes langage SQL (SQL) à la base de données. La procédure suivante décrit comment utiliser SQL pour interroger une base de données.
ms.assetid: 1b8fd935-4964-4875-801b-cc6765b16924
title: Utilisation des requêtes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0be4839c1e97f05d09769d69d62345b0602b789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952224"
---
# <a name="working-with-queries"></a><span data-ttu-id="6ab93-104">Utilisation des requêtes</span><span class="sxs-lookup"><span data-stu-id="6ab93-104">Working with Queries</span></span>

<span data-ttu-id="6ab93-105">Étant donné que le programme d’installation utilise une base de données relationnelle, il existe des fonctions permettant d’effectuer des requêtes langage SQL (SQL) à la base de données.</span><span class="sxs-lookup"><span data-stu-id="6ab93-105">Because the installer uses a relational database, there are functions for making Structured Query Language (SQL) queries to the database.</span></span> <span data-ttu-id="6ab93-106">La procédure suivante décrit comment utiliser SQL pour interroger une base de données.</span><span class="sxs-lookup"><span data-stu-id="6ab93-106">The following procedure describes how to use SQL to query a database.</span></span>

<span data-ttu-id="6ab93-107">**Pour interroger une base de données avec SQL**</span><span class="sxs-lookup"><span data-stu-id="6ab93-107">**To query a database with SQL**</span></span>

1.  <span data-ttu-id="6ab93-108">Ouvrez l’objet de [**vue**](view-object.md) , avec l’instruction SQL appropriée, en appelant la fonction [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .</span><span class="sxs-lookup"><span data-stu-id="6ab93-108">Open the [**View**](view-object.md) object, with the appropriate SQL statement, by calling the [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) function.</span></span>

    <span data-ttu-id="6ab93-109">Un objet de [**vue**](view-object.md) est la table logique créée par l’application d’une requête à un ensemble de tables.</span><span class="sxs-lookup"><span data-stu-id="6ab93-109">A [**View**](view-object.md) object is the logical table created by applying a query to a set of tables.</span></span> <span data-ttu-id="6ab93-110">Les requêtes SQL doivent adhérer à la [syntaxe SQL](sql-syntax.md) fournie par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="6ab93-110">SQL queries must adhere to the [SQL syntax](sql-syntax.md) provided by the installer.</span></span> <span data-ttu-id="6ab93-111">Cette instruction SQL peut contenir des marqueurs de paramètres qui ne sont pas spécifiés tant que l’objet de **vue** n’est pas exécuté.</span><span class="sxs-lookup"><span data-stu-id="6ab93-111">This SQL statement can contain parameter markers that are not specified until the **View** object runs.</span></span>

2.  <span data-ttu-id="6ab93-112">Exécutez l’objet de [**vue**](view-object.md) en appelant la fonction [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) .</span><span class="sxs-lookup"><span data-stu-id="6ab93-112">Run the [**View**](view-object.md) object by calling the [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) function.</span></span>
3.  <span data-ttu-id="6ab93-113">Récupérez l’enregistrement suivant d’un objet de [**vue**](view-object.md) en appelant la fonction [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) .</span><span class="sxs-lookup"><span data-stu-id="6ab93-113">Retrieve the next record from a [**View**](view-object.md) object by calling the [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) function.</span></span>
4.  <span data-ttu-id="6ab93-114">Modifiez l’objet de [**vue**](view-object.md) en appelant la fonction [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) .</span><span class="sxs-lookup"><span data-stu-id="6ab93-114">Modify the [**View**](view-object.md) object by calling the [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) function.</span></span>

    <span data-ttu-id="6ab93-115">Vous pouvez également valider les données avec [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) en passant les indicateurs appropriés.</span><span class="sxs-lookup"><span data-stu-id="6ab93-115">You can also validate data with [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) by passing the appropriate flags.</span></span> <span data-ttu-id="6ab93-116">Si **MsiViewModify** retourne \_ des données d’erreur non valides \_ d’une demande de validation, les données sous-jacentes sont endommagées.</span><span class="sxs-lookup"><span data-stu-id="6ab93-116">If **MsiViewModify** returns ERROR\_INVALID\_DATA from a validation request, the underlying data is corrupt.</span></span>

5.  <span data-ttu-id="6ab93-117">Obtenez des informations détaillées sur l’erreur sur l’objet de [**vue**](view-object.md) en appelant la fonction [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) .</span><span class="sxs-lookup"><span data-stu-id="6ab93-117">Obtain detailed error information on the [**View**](view-object.md) object by calling the [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) function.</span></span>
6.  <span data-ttu-id="6ab93-118">Fermez l’objet de [**vue**](view-object.md) en appelant la fonction [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) .</span><span class="sxs-lookup"><span data-stu-id="6ab93-118">Close the [**View**](view-object.md) object by calling the [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) function.</span></span>

<span data-ttu-id="6ab93-119">Pour plus d’informations, consultez [exemples de requêtes de base de données avec SQL et script](examples-of-database-queries-using-sql-and-script.md).</span><span class="sxs-lookup"><span data-stu-id="6ab93-119">For more information, see [Examples of Database Queries Using SQL and Script](examples-of-database-queries-using-sql-and-script.md).</span></span>

 

 



