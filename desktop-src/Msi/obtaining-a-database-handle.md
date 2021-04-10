---
description: Avant d’utiliser une base de données, vous devez d’abord obtenir un descripteur.
ms.assetid: 53cf73bc-4d52-471c-8384-46d106a36e38
title: Obtention d’un descripteur de base de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5f37f1abd329d0c51b00839d43ef85784fdad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114323"
---
# <a name="obtaining-a-database-handle"></a><span data-ttu-id="90f47-103">Obtention d’un descripteur de base de données</span><span class="sxs-lookup"><span data-stu-id="90f47-103">Obtaining a Database Handle</span></span>

<span data-ttu-id="90f47-104">Avant d’utiliser une base de données, vous devez d’abord obtenir un descripteur.</span><span class="sxs-lookup"><span data-stu-id="90f47-104">Before working with a database you must first obtain a handle to it.</span></span>

<span data-ttu-id="90f47-105">**Pour accéder aux informations relatives à une base de données de programme d’installation**</span><span class="sxs-lookup"><span data-stu-id="90f47-105">**To access information about an installer database**</span></span>

1.  <span data-ttu-id="90f47-106">Obtenez un descripteur de la base de données de deux façons :</span><span class="sxs-lookup"><span data-stu-id="90f47-106">Obtain a handle to the database in one of two ways:</span></span>
    -   <span data-ttu-id="90f47-107">Si une installation est en cours, récupérez un descripteur de la base de données active en appelant la fonction [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) .</span><span class="sxs-lookup"><span data-stu-id="90f47-107">If an installation is in progress, get a handle to the active database by calling the [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) function.</span></span>
    -   <span data-ttu-id="90f47-108">Si une installation n’est pas en cours, ouvrez une base de données spécifiée en appelant la fonction [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) .</span><span class="sxs-lookup"><span data-stu-id="90f47-108">If an installation is not in progress, open any specified database by calling the [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) function.</span></span>
2.  <span data-ttu-id="90f47-109">Une fois la base de données ouverte, vous pouvez appeler des fonctions pour obtenir des informations sur la base de données ou pour manipuler la base de données.</span><span class="sxs-lookup"><span data-stu-id="90f47-109">After the database has been opened, you can call functions to obtain information about the database or to manipulate the database.</span></span>
    -   <span data-ttu-id="90f47-110">Créez un objet de **vue** et spécifiez une requête SQL de la base de données ouverte en appelant la fonction [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .</span><span class="sxs-lookup"><span data-stu-id="90f47-110">Create a **View** object and specify a SQL query of the open database by calling the [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) function.</span></span>
    -   <span data-ttu-id="90f47-111">Obtenez un enregistrement qui contient toutes les clés primaires d’une table spécifiée dans la base de données ouverte en appelant la fonction [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) .</span><span class="sxs-lookup"><span data-stu-id="90f47-111">Obtain a record that contains all primary keys of a specified table in the open database by calling the [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) function.</span></span>
    -   <span data-ttu-id="90f47-112">Vérifiez l’état actuel d’une base de données ouverte en appelant la fonction [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) .</span><span class="sxs-lookup"><span data-stu-id="90f47-112">Check the current state of an open database by calling the [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) function.</span></span> <span data-ttu-id="90f47-113">Avec la fonction **MsiGetDatabaseState** , vous pouvez déterminer l’état de lecture/écriture d’une base de données ou si le descripteur est valide.</span><span class="sxs-lookup"><span data-stu-id="90f47-113">With the **MsiGetDatabaseState** function, you can determine the read/write status for a database or if the handle is valid.</span></span>

 

 



