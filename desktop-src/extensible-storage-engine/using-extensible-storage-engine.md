---
description: 'En savoir plus sur : utilisation du moteur de stockage extensible'
title: Utilisation du moteur de stockage extensible
TOCTitle: Using Extensible Storage Engine
ms:assetid: d0249519-4c7c-49c1-9c80-b3cae2537d61
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294096(v=EXCHG.10)
ms:contentKeyID: 32765711
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 636c3fa96692b8c48f9a175b5fa7d34c53314e1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527382"
---
# <a name="using-extensible-storage-engine"></a><span data-ttu-id="ef00f-103">Utilisation du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="ef00f-103">Using Extensible Storage Engine</span></span>


<span data-ttu-id="ef00f-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="ef00f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="using-extensible-storage-engine"></a><span data-ttu-id="ef00f-105">Utilisation du moteur de stockage extensible</span><span class="sxs-lookup"><span data-stu-id="ef00f-105">Using Extensible Storage Engine</span></span>

<span data-ttu-id="ef00f-106">Cette section contient des informations générales sur l’utilisation des éléments suivants de l’API ESE.</span><span class="sxs-lookup"><span data-stu-id="ef00f-106">This section contains general information about how to use the following parts of the ESE API.</span></span>

  - [<span data-ttu-id="ef00f-107">Colonnes</span><span class="sxs-lookup"><span data-stu-id="ef00f-107">Columns</span></span>](./columns.md)

  - [<span data-ttu-id="ef00f-108">Indexation dans la table</span><span class="sxs-lookup"><span data-stu-id="ef00f-108">Indexing in the Table</span></span>](./indexing-in-the-table.md)

  - [<span data-ttu-id="ef00f-109">Création de bases de données</span><span class="sxs-lookup"><span data-stu-id="ef00f-109">Creating Databases</span></span>](./creating-databases.md)

  - [<span data-ttu-id="ef00f-110">Transactions</span><span class="sxs-lookup"><span data-stu-id="ef00f-110">Transactions</span></span>](./transactions.md)

  - [<span data-ttu-id="ef00f-111">Erreurs ESE</span><span class="sxs-lookup"><span data-stu-id="ef00f-111">ESE Errors</span></span>](./extensible-storage-engine-errors.md)

  - [<span data-ttu-id="ef00f-112">Fichiers ESE</span><span class="sxs-lookup"><span data-stu-id="ef00f-112">ESE Files</span></span>](./extensible-storage-engine-files.md)

<span data-ttu-id="ef00f-113">Les fichiers sources de votre programme doivent inclure le fichier d’en-tête esent. h pour accéder aux prototypes de fonction et aux définitions de structure pour l’API ESE (Extensible Storage Engine).</span><span class="sxs-lookup"><span data-stu-id="ef00f-113">Your program source files should include the esent.h header file to access function prototypes and structure definitions for the Extensible Storage Engine API.</span></span> <span data-ttu-id="ef00f-114">Les développeurs peuvent utiliser le fichier de bibliothèque esent. lib pour créer des applications qui utilisent l’API ESE (Extensible Storage Engine).</span><span class="sxs-lookup"><span data-stu-id="ef00f-114">Developers can use the esent.lib library file to build applications that use the Extensible Storage Engine API.</span></span> <span data-ttu-id="ef00f-115">Au moment de l’exécution, les applications sont liées au esent.dll.</span><span class="sxs-lookup"><span data-stu-id="ef00f-115">At runtime, applications link to the esent.dll.</span></span>
