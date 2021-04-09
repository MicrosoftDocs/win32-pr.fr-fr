---
description: Le fournisseur WMI du collecteur d’événements de démarrage fournit l’accès aux informations de connexion et de configuration pour la fonctionnalité de collecte d’événements d’installation et de démarrage sur Windows Server.
ms.assetid: ab9ac8f0-69a5-4a2d-8ee5-1f003aa1bb5b
ms.tgt_platform: multiple
title: Fournisseur WMI du collecteur d’événements de démarrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38ef27b2989f856fdcfda82d4ee0e68c3913167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846977"
---
# <a name="boot-event-collector-wmi-provider"></a><span data-ttu-id="23b6d-103">Fournisseur WMI du collecteur d’événements de démarrage</span><span class="sxs-lookup"><span data-stu-id="23b6d-103">Boot Event Collector WMI Provider</span></span>

## <a name="purpose"></a><span data-ttu-id="23b6d-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="23b6d-104">Purpose</span></span>

<span data-ttu-id="23b6d-105">Le fournisseur WMI du collecteur d’événements de démarrage fournit l’accès aux informations de connexion et de configuration pour la fonctionnalité de collecte d’événements d’installation et de démarrage sur Windows Server.</span><span class="sxs-lookup"><span data-stu-id="23b6d-105">The Boot Event Collector WMI provider provides access to connection and configuration information for the Setup and Boot Event Collection feature on Windows Server.</span></span> <span data-ttu-id="23b6d-106">Cela vous permet d’afficher la liste des connexions en cours et l’historique des connexions entre un serveur du collecteur et ses ordinateurs cibles.</span><span class="sxs-lookup"><span data-stu-id="23b6d-106">This allows you to view a list of the current connections and the connection history between a collector server and its target computers.</span></span> <span data-ttu-id="23b6d-107">En outre, ce fournisseur vous permet de gérer la configuration d’un serveur collecteur.</span><span class="sxs-lookup"><span data-stu-id="23b6d-107">In addition, this provider allows you to manage the configuration of a collector server.</span></span>

> [!Note]  
> <span data-ttu-id="23b6d-108">Le fournisseur WMI du collecteur d’événements de démarrage est implémenté dans BEvtCol.exe.</span><span class="sxs-lookup"><span data-stu-id="23b6d-108">The Boot Event Collector WMI provider is implemented in BEvtCol.exe.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="23b6d-109">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="23b6d-109">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="23b6d-110">**TargetForwarding**</span><span class="sxs-lookup"><span data-stu-id="23b6d-110">**TargetForwarding**</span></span>](targetforwarding.md)
</dt> <dd>

<span data-ttu-id="23b6d-111">Récupère les données de transfert d’un ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="23b6d-111">Retrieves forwarding data from a target computer.</span></span>

</dd> <dt>

[<span data-ttu-id="23b6d-112">**TargetForwardingDestination**</span><span class="sxs-lookup"><span data-stu-id="23b6d-112">**TargetForwardingDestination**</span></span>](targetforwardingdestination.md)
</dt> <dd>

<span data-ttu-id="23b6d-113">Destinations connues contenant les données collectées.</span><span class="sxs-lookup"><span data-stu-id="23b6d-113">The known destinations containing the collected data.</span></span> <span data-ttu-id="23b6d-114">Disponible uniquement si le collecteur est en cours d’exécution avec le journal d’état activé.</span><span class="sxs-lookup"><span data-stu-id="23b6d-114">Available only if the collector is running with the status log enabled.</span></span>

</dd> <dt>

[<span data-ttu-id="23b6d-115">**TargetForwardingHistory**</span><span class="sxs-lookup"><span data-stu-id="23b6d-115">**TargetForwardingHistory**</span></span>](targetforwardinghistory.md)
</dt> <dd>

<span data-ttu-id="23b6d-116">Historique récent des modifications apportées aux données de transfert pour un ordinateur cible.</span><span class="sxs-lookup"><span data-stu-id="23b6d-116">The recent history of changes to the forwarding data for a target computer.</span></span>

</dd> <dt>

[<span data-ttu-id="23b6d-117">**Contrôler**</span><span class="sxs-lookup"><span data-stu-id="23b6d-117">**Control**</span></span>](control.md)
</dt> <dd>

<span data-ttu-id="23b6d-118">Contrôle de l’instance du collecteur.</span><span class="sxs-lookup"><span data-stu-id="23b6d-118">Control of the collector instance.</span></span> <span data-ttu-id="23b6d-119">Requiert les privilèges d’administrateur (BA).</span><span class="sxs-lookup"><span data-stu-id="23b6d-119">Requires the Administrator (BA) privileges.</span></span>

</dd> </dl>

 

 



