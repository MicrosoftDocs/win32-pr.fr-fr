---
description: Les modifications apportées à la base de données d’installation ne sont pas écrites dans la base de données tant que vous n’avez pas appelé MsiDatabaseCommit.
ms.assetid: 65271631-457c-4d3e-9384-126d2c9d63d7
title: Validation des bases de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1336b094703e61b14966e7a73a6e67f73762024
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866725"
---
# <a name="committing-databases"></a><span data-ttu-id="a66ea-103">Validation des bases de données</span><span class="sxs-lookup"><span data-stu-id="a66ea-103">Committing Databases</span></span>

<span data-ttu-id="a66ea-104">Les modifications apportées à la base de données d’installation ne sont pas écrites dans la base de données tant que vous n’avez pas appelé [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span><span class="sxs-lookup"><span data-stu-id="a66ea-104">Changes made to the installation database are not written to the database until you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span>

<span data-ttu-id="a66ea-105">**Pour garantir la finalisation des modifications apportées à une base de données**</span><span class="sxs-lookup"><span data-stu-id="a66ea-105">**To ensure changes made in a database are finalized**</span></span>

1.  <span data-ttu-id="a66ea-106">Vérifiez si une table est écrite quand vous appelez [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) en appelant [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).</span><span class="sxs-lookup"><span data-stu-id="a66ea-106">Check to see whether a table will be written when you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) by calling [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).</span></span>
2.  <span data-ttu-id="a66ea-107">Appelez la fonction [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) pour finaliser les modifications apportées à la base de données.</span><span class="sxs-lookup"><span data-stu-id="a66ea-107">Call the [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) function to finalize changes to the database.</span></span>

<span data-ttu-id="a66ea-108">Les modifications apportées dans une base de données sont accumulées et ne sont pas reflétées dans la base de données réelle tant que vous n’avez pas appelé [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span><span class="sxs-lookup"><span data-stu-id="a66ea-108">Changes made in a database are accumulated and are not reflected in the actual database until you call [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span> <span data-ttu-id="a66ea-109">Les colonnes ou les lignes temporaires ne sont pas validées dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="a66ea-109">Temporary columns or rows are not committed to the database.</span></span> <span data-ttu-id="a66ea-110">Quand une base de données est fermée, toutes les modifications apportées depuis le dernier **MsiDatabaseCommit** sont automatiquement annulées.</span><span class="sxs-lookup"><span data-stu-id="a66ea-110">When a database is closed, all changes made since the last **MsiDatabaseCommit** are automatically rolled back.</span></span>

 

 



