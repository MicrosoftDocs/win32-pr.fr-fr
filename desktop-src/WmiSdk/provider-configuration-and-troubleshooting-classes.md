---
description: La \_ classe fournisseurs msft et les classes de résolution des problèmes WMI sont un groupe de classes d’événements msft associées aux événements du fournisseur WMI.
ms.assetid: 5eaf7026-87bf-416b-9a6d-7f92f85b0882
ms.tgt_platform: multiple
title: Classes de résolution des problèmes et de configuration du fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be63fb5693898541bffae2abcb05b7595ae7fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521228"
---
# <a name="provider-configuration-and-troubleshooting-classes"></a><span data-ttu-id="c7669-103">Classes de résolution des problèmes et de configuration du fournisseur</span><span class="sxs-lookup"><span data-stu-id="c7669-103">Provider Configuration and Troubleshooting Classes</span></span>

<span data-ttu-id="c7669-104">La [**classe \_ fournisseurs msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) et les classes de résolution des problèmes WMI sont un groupe de [classes d’événements msft](msft-classes.md) associées aux événements du fournisseur WMI.</span><span class="sxs-lookup"><span data-stu-id="c7669-104">The [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) class and the WMI troubleshooting classes are a group of the [MSFT event classes](msft-classes.md) coupled to WMI provider events.</span></span>

<span data-ttu-id="c7669-105">La [**classe \_ fournisseurs msft**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) contient des informations de configuration pour les fournisseurs et inclut les méthodes suivantes qui vous permettent de charger et de décharger des fournisseurs, ou d’interrompre et de reprendre les opérations du fournisseur :</span><span class="sxs-lookup"><span data-stu-id="c7669-105">The [**MSFT\_Providers**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) class contains configuration information for providers and includes the following methods that allow you to load and unload providers, or suspend and resume provider operations:</span></span>

-   [<span data-ttu-id="c7669-106">**Méthode Load de la \_ classe des fournisseurs msft**</span><span class="sxs-lookup"><span data-stu-id="c7669-106">**Load Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers)
-   [<span data-ttu-id="c7669-107">**Méthode Unload de la \_ classe des fournisseurs msft**</span><span class="sxs-lookup"><span data-stu-id="c7669-107">**UnLoad Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/unload-method-in-class-msft-providers)
-   [<span data-ttu-id="c7669-108">**Méthode Resume de la \_ classe des fournisseurs msft**</span><span class="sxs-lookup"><span data-stu-id="c7669-108">**Resume Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/resume-method-in-class-msft-providers)
-   [<span data-ttu-id="c7669-109">**Méthode suspend de la \_ classe des fournisseurs msft**</span><span class="sxs-lookup"><span data-stu-id="c7669-109">**Suspend Method of the MSFT\_Providers Class**</span></span>](/previous-versions/windows/desktop/wmisystemprov/suspend-method-in-class-msft-providers)

<span data-ttu-id="c7669-110">Les [classes de résolution des problèmes WMI](wmi-troubleshooting-classes.md) sont nommées pour indiquer si l’événement est déclenché avant ou après un événement de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="c7669-110">The [WMI troubleshooting classes](wmi-troubleshooting-classes.md) are named to indicate whether the event is fired before or after a provider event.</span></span> <span data-ttu-id="c7669-111">Par exemple, le [**pré-objet \_ wmiprovider \_ AccessCheck \_ msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) est généré immédiatement avant l’appel de l’implémentation du fournisseur de **IWbemEventSecurity :: AccessCheck**, tandis que l’objet [**msft \_ wmiprovider \_ AccessCheck \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) est appelé immédiatement après.</span><span class="sxs-lookup"><span data-stu-id="c7669-111">For example, the [**MSFT\_WmiProvider\_AccessCheck\_Pre**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) object is generated immediately before calling the provider's implementation of **IWbemEventSecurity::AccessCheck**, while the [**MSFT\_WmiProvider\_AccessCheck\_Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) object is called immediately after.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7669-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c7669-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7669-113">Résolution des problèmes WMI</span><span class="sxs-lookup"><span data-stu-id="c7669-113">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="c7669-114">Classes de résolution des problèmes WMI</span><span class="sxs-lookup"><span data-stu-id="c7669-114">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
