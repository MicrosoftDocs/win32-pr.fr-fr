---
description: Les tables du groupe tables système suivent les tables et les colonnes de la base de données d’installation.
ms.assetid: d20be8b6-f456-4f90-aa9e-dc122c20d20c
title: Groupe de tables système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 482333ec3f6f483d431aced9a984c7db1ae5cef4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114154"
---
# <a name="system-tables-group"></a><span data-ttu-id="57a47-103">Groupe de tables système</span><span class="sxs-lookup"><span data-stu-id="57a47-103">System Tables Group</span></span>

<span data-ttu-id="57a47-104">Les tables du groupe tables système suivent les tables et les colonnes de la base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="57a47-104">The tables of the system tables group track the tables and columns of the installation database.</span></span>

-   <span data-ttu-id="57a47-105">La [ \_ table tables](-tables-table.md) effectue le suivi de toutes les tables de la base de données.</span><span class="sxs-lookup"><span data-stu-id="57a47-105">The [\_Tables table](-tables-table.md) tracks all the tables in the database.</span></span> <span data-ttu-id="57a47-106">Cela comprend les tables que vous avez créées pour vos propres actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="57a47-106">This includes tables that you may have created for your own custom actions.</span></span> <span data-ttu-id="57a47-107">Interrogez cette table pour savoir si une table existe.</span><span class="sxs-lookup"><span data-stu-id="57a47-107">Query this table to find out if a table exists.</span></span>
-   <span data-ttu-id="57a47-108">La [ \_ Table Columns](-columns-table.md) effectue le suivi des colonnes dans la base de données d’installation.</span><span class="sxs-lookup"><span data-stu-id="57a47-108">The [\_Columns table](-columns-table.md) tracks columns in the installation database.</span></span> <span data-ttu-id="57a47-109">Les colonnes temporaires ne sont pas suivies actuellement par cette table.</span><span class="sxs-lookup"><span data-stu-id="57a47-109">Temporary columns are currently not tracked by this table.</span></span> <span data-ttu-id="57a47-110">Interrogez cette table pour savoir si une colonne donnée existe.</span><span class="sxs-lookup"><span data-stu-id="57a47-110">Query this table to find out if a given column exists.</span></span>
-   <span data-ttu-id="57a47-111">Le [ \_ tableau Streams](-streams-table.md) répertorie les flux de données OLE incorporés.</span><span class="sxs-lookup"><span data-stu-id="57a47-111">The [\_Streams table](-streams-table.md) lists embedded OLE data streams.</span></span>
-   <span data-ttu-id="57a47-112">Le [ \_ tableau stockages](-storages-table.md) répertorie les stockages de données OLE incorporés.</span><span class="sxs-lookup"><span data-stu-id="57a47-112">The [\_Storages table](-storages-table.md) lists embedded OLE data storages.</span></span>
-   <span data-ttu-id="57a47-113">[ \_ Tableau de validation](-validation-table.md).</span><span class="sxs-lookup"><span data-stu-id="57a47-113">The [\_Validation table](-validation-table.md).</span></span> <span data-ttu-id="57a47-114">Le \_ tableau de validation effectue le suivi des types et des plages autorisées de chaque colonne de la base de données.</span><span class="sxs-lookup"><span data-stu-id="57a47-114">The \_Validation table tracks the types and allowed ranges of every column in the database.</span></span> <span data-ttu-id="57a47-115">Le \_ tableau de validation est utilisé pendant le processus de validation de la base de données pour s’assurer que toutes les colonnes sont comptabilisées et ont les valeurs correctes.</span><span class="sxs-lookup"><span data-stu-id="57a47-115">The \_Validation table is used during the database validation process to ensure that all columns are accounted for and have the correct values.</span></span> <span data-ttu-id="57a47-116">Cette table n’est pas fournie avec la base de données du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="57a47-116">This table is not shipped with the installer database.</span></span>

 

 



