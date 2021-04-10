---
description: Lorsque vous utilisez les infrastructures de représentation graphique d’homologue ou de regroupement d’homologues, les informations (enregistrements) que les homologues publient sur un graphique ou un groupe sont stockées en tant que base de données sur chaque ordinateur homologue.
ms.assetid: 1412b2eb-c97d-4415-998c-5f21eaadcc66
title: Importation et exportation de base de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b48fc09259c06e6ebaf537d26c7288d0ad09c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952036"
---
# <a name="database-import-and-export"></a><span data-ttu-id="72109-103">Importation et exportation de base de données</span><span class="sxs-lookup"><span data-stu-id="72109-103">Database Import and Export</span></span>

<span data-ttu-id="72109-104">Lorsque vous utilisez les infrastructures de représentation graphique d’homologue ou de regroupement d’homologues, les informations (enregistrements) que les homologues publient sur un graphique ou un groupe sont stockées en tant que base de données sur chaque ordinateur homologue.</span><span class="sxs-lookup"><span data-stu-id="72109-104">When using the Peer Graphing or the Peer Grouping Infrastructures, the information (records) that peers publish to a graph or group is stored as a database on each peer computer.</span></span> <span data-ttu-id="72109-105">Pour migrer une application d’un ordinateur à un autre, vous pouvez exporter une base de données de représentation graphique ou de regroupement d’homologues à partir d’un ordinateur, puis l’importer vers une autre.</span><span class="sxs-lookup"><span data-stu-id="72109-105">To migrate an application from one computer to another computer, you can export a Peer Graphing or Peer Grouping database from one computer, and then import it to another.</span></span>

<span data-ttu-id="72109-106">La liste suivante identifie les informations importantes sur l’utilisation des bases de données :</span><span class="sxs-lookup"><span data-stu-id="72109-106">The following list identifies important information about working with databases:</span></span>

-   <span data-ttu-id="72109-107">Vous pouvez uniquement importer une base de données qui a le même graphique et l’ID homologue.</span><span class="sxs-lookup"><span data-stu-id="72109-107">You can only import a database that has the same graph and peer ID.</span></span>
-   <span data-ttu-id="72109-108">Vous ne pouvez pas appeler les fonctions d’importation et d’exportation si [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten), [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)ou [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) ont été appelés.</span><span class="sxs-lookup"><span data-stu-id="72109-108">You cannot call the import and export functions if [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten), [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect), or [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) have been called.</span></span>

<span data-ttu-id="72109-109">L' **infrastructure de représentation graphique des pairs** utilise les appels suivants pour importer et exporter une base de données d’enregistrement :</span><span class="sxs-lookup"><span data-stu-id="72109-109">**Peer Graphing Infrastructure** uses the following calls to import and export a record database:</span></span>

-   [<span data-ttu-id="72109-110">**PeerGraphExportDatabase**</span><span class="sxs-lookup"><span data-stu-id="72109-110">**PeerGraphExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase)
-   [<span data-ttu-id="72109-111">**PeerGraphImportDatabase**</span><span class="sxs-lookup"><span data-stu-id="72109-111">**PeerGraphImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase)

<span data-ttu-id="72109-112">L' **infrastructure de regroupement de pairs** utilise les appels suivants pour importer et exporter une base de données d’enregistrement :</span><span class="sxs-lookup"><span data-stu-id="72109-112">**Peer Grouping Infrastructure** uses the following calls to import and export a record database:</span></span>

-   [<span data-ttu-id="72109-113">**PeerGroupExportDatabase**</span><span class="sxs-lookup"><span data-stu-id="72109-113">**PeerGroupExportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)
-   [<span data-ttu-id="72109-114">**PeerGroupImportDatabase**</span><span class="sxs-lookup"><span data-stu-id="72109-114">**PeerGroupImportDatabase**</span></span>](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)

 

 



