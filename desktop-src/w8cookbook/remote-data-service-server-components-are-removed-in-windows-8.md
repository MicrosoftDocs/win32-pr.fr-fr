---
title: Service de données distant supprimé
description: Les composants du serveur de services de données distants sont supprimés de Windows 8
ms.assetid: 53ECB92C-8868-4A1A-82BD-4ADE75F7BB59
keywords:
- Serveur RDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6588b029fe37f1312c709be168fd695bdc5738
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103941433"
---
# <a name="remote-data-service-server-components-are-removed-in-windows-8"></a><span data-ttu-id="8ce4a-104">Les composants du serveur de services de données distants sont supprimés de Windows 8</span><span class="sxs-lookup"><span data-stu-id="8ce4a-104">Remote data service server components are removed in Windows 8</span></span>

## <a name="platforms"></a><span data-ttu-id="8ce4a-105">Plateformes</span><span class="sxs-lookup"><span data-stu-id="8ce4a-105">Platforms</span></span>

 <span data-ttu-id="8ce4a-106">**Clients** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="8ce4a-106">**Clients** - Windows 8</span></span>  
<span data-ttu-id="8ce4a-107">**Serveurs** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8ce4a-107">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="8ce4a-108">Description</span><span class="sxs-lookup"><span data-stu-id="8ce4a-108">Description</span></span>

<span data-ttu-id="8ce4a-109">Le serveur RDS (Remote Data Service) n’est pas disponible dans Windows 8 :</span><span class="sxs-lookup"><span data-stu-id="8ce4a-109">The remote data service (RDS) server is not available in Windows 8:</span></span>

-   <span data-ttu-id="8ce4a-110">Le msadcf.dll de fichiers, qui héberge le « Business Object » par défaut, RDSServer. DataFactory, est supprimé et ses fichiers associés (msadcfr.dll, msadcfr.dll. mui, handler. reg et handsafe. reg) sont supprimés</span><span class="sxs-lookup"><span data-stu-id="8ce4a-110">File msadcf.dll, which hosts the default "business object" RDSServer.DataFactory, is removed, and its associated files (msadcfr.dll, msadcfr.dll.mui, handler.reg and handsafe.reg) are removed</span></span>
-   <span data-ttu-id="8ce4a-111">Le fichier msdfmap.dll, qui est le gestionnaire par défaut, est supprimé et le fichier msdfmap.ini est supprimé</span><span class="sxs-lookup"><span data-stu-id="8ce4a-111">File msdfmap.dll, which is the default Handler, is removed, and the file msdfmap.ini is removed</span></span>
-   <span data-ttu-id="8ce4a-112">Le msadcs.dll de fichier, ISAPI, est supprimé</span><span class="sxs-lookup"><span data-stu-id="8ce4a-112">File msadcs.dll, the ISAPI, is removed</span></span>

## <a name="manifestation"></a><span data-ttu-id="8ce4a-113">Manifestation</span><span class="sxs-lookup"><span data-stu-id="8ce4a-113">Manifestation</span></span>

<span data-ttu-id="8ce4a-114">Les clients ne peuvent pas héberger un serveur RDS sur Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8ce4a-114">Customers cannot host an RDS server on Windows 8.</span></span>

## <a name="mitigation"></a><span data-ttu-id="8ce4a-115">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="8ce4a-115">Mitigation</span></span>

<span data-ttu-id="8ce4a-116">Les clients peuvent conserver leur serveur RDS sur un ordinateur équipé de Windows 7 ou d’autres systèmes d’exploitation de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="8ce4a-116">Customers can keep their RDS server on a machine with Windows 7 or other down-level operating systems.</span></span>

## <a name="solution"></a><span data-ttu-id="8ce4a-117">Solution</span><span class="sxs-lookup"><span data-stu-id="8ce4a-117">Solution</span></span>

<span data-ttu-id="8ce4a-118">Les clients peuvent conserver leur serveur RDS sur un ordinateur équipé de Windows 7 ou d’autres systèmes d’exploitation de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="8ce4a-118">Customers can keep their RDS server on a machine with Windows 7 or other down-level operating systems.</span></span>

## <a name="resources"></a><span data-ttu-id="8ce4a-119">Ressources</span><span class="sxs-lookup"><span data-stu-id="8ce4a-119">Resources</span></span>

[<span data-ttu-id="8ce4a-120">Feuille de route des technologies d’accès aux données</span><span class="sxs-lookup"><span data-stu-id="8ce4a-120">Data Access Technologies Roadmap</span></span>](/sql/connect/connect-history?view=sqlallproducts-allversions)

 

 