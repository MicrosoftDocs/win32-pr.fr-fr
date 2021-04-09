---
description: Pour sélectionner une carte réseau à partir d’une table d’objets BLOB NPP renvoyée par Moniteur réseau, appelez la fonction GetNPPBlobTable. Cette fonction retourne une table d’objets BLOB NPP, qui peut ensuite être énumérée par votre application pour sélectionner la carte réseau qui vous intéresse.
ms.assetid: 51428cc9-0b48-4da6-bbf6-b22798e01263
title: Sélection d’une carte d’interface réseau à partir d’une table BLOB NPP retournée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08215bb647482ba8544d7eaa033dea7efd9a5ad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865185"
---
# <a name="selecting-a-nic-from-a-returned-npp-blob-table"></a><span data-ttu-id="3a365-104">Sélection d’une carte d’interface réseau à partir d’une table BLOB NPP retournée</span><span class="sxs-lookup"><span data-stu-id="3a365-104">Selecting a NIC from a Returned NPP BLOB table</span></span>

<span data-ttu-id="3a365-105">Pour sélectionner une carte réseau à partir d’une table d’objets BLOB NPP renvoyée par Moniteur réseau, appelez la fonction [**GetNPPBlobTable**](getnppblobtable.md) .</span><span class="sxs-lookup"><span data-stu-id="3a365-105">To select a NIC from an NPP BLOB table returned by Network Monitor, call the [**GetNPPBlobTable**](getnppblobtable.md) function.</span></span> <span data-ttu-id="3a365-106">Cette fonction retourne une table d’objets BLOB NPP, qui peut ensuite être énumérée par votre application pour sélectionner la carte réseau qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="3a365-106">This function returns an NPP BLOB table, which can then be enumerated by your application to select the NIC you are interested in.</span></span>

<span data-ttu-id="3a365-107">Lorsque vous appelez cette fonction, vous pouvez retourner une table d’objets BLOB de toutes les cartes réseau inscrites sur l’ordinateur local ou un plus petit ensemble de cartes réseau filtrées.</span><span class="sxs-lookup"><span data-stu-id="3a365-107">When you call this function you can return either a BLOB table of all the NICs registered on the local computer or a smaller set of filtered NICs.</span></span> <span data-ttu-id="3a365-108">Pour filtrer les cartes réseau qui sont renvoyées, vous pouvez fournir un [*objet blob de filtre*](f.md) lorsque l’appel est effectué.</span><span class="sxs-lookup"><span data-stu-id="3a365-108">To filter the NICs that are returned, you can provide a [*filter BLOB*](f.md) when the call is made.</span></span>



| <span data-ttu-id="3a365-109">Pour obtenir des informations sur</span><span class="sxs-lookup"><span data-stu-id="3a365-109">For information about</span></span>                                                       | <span data-ttu-id="3a365-110">Consultez</span><span class="sxs-lookup"><span data-stu-id="3a365-110">See</span></span>                                                                                                  |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a365-111">Comment spécifier un filtre qui limite les cartes réseau retournées dans une table d’objets BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="3a365-111">How to specify a filter that limits the NICs returned in an NPP BLOB table.</span></span> | [<span data-ttu-id="3a365-112">Spécification d’un objet BLOB de filtre</span><span class="sxs-lookup"><span data-stu-id="3a365-112">Specifying a Filter BLOB</span></span>](specifying-a-filter-blob.md)                                             |
| <span data-ttu-id="3a365-113">Comment sélectionner une carte réseau inscrite sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="3a365-113">How to select a NIC registered on a local computer.</span></span>                         | [<span data-ttu-id="3a365-114">Sélection d’une carte réseau enregistrée</span><span class="sxs-lookup"><span data-stu-id="3a365-114">Selecting a Registered NIC</span></span>](selecting-a-registered-nic.md)                                         |
| <span data-ttu-id="3a365-115">Comment sélectionner une carte réseau à partir d’une table d’objets BLOB NPP fournie</span><span class="sxs-lookup"><span data-stu-id="3a365-115">How to select a NIC from a supplied NPP BLOB table</span></span>                          | [<span data-ttu-id="3a365-116">Sélection d’une carte d’interface réseau à partir d’une table d’objets BLOB NPP fournie</span><span class="sxs-lookup"><span data-stu-id="3a365-116">Selecting a NIC from a Supplied NPP BLOB Table</span></span>](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



