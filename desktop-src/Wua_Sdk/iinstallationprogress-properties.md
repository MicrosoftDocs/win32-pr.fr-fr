---
description: L’interface IInstallationProgress définit les propriétés suivantes.
ms.assetid: f16c682f-3e9f-4767-8f26-d7af0a14d720
title: Propriétés IInstallationProgress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcbcdb162c544c81b96326ec7b2b7657d81538a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517535"
---
# <a name="iinstallationprogress-properties"></a><span data-ttu-id="b94b4-103">Propriétés IInstallationProgress</span><span class="sxs-lookup"><span data-stu-id="b94b4-103">IInstallationProgress Properties</span></span>

<span data-ttu-id="b94b4-104">L’interface [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) définit les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="b94b4-104">The [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) interface defines the following properties.</span></span>



| <span data-ttu-id="b94b4-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="b94b4-105">Property</span></span>                                                                                   | <span data-ttu-id="b94b4-106">Description</span><span class="sxs-lookup"><span data-stu-id="b94b4-106">Description</span></span>                                                                                                                                        |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b94b4-107">**CurrentUpdateIndex**</span><span class="sxs-lookup"><span data-stu-id="b94b4-107">**CurrentUpdateIndex**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdateindex)                     | <span data-ttu-id="b94b4-108">Obtient une valeur d’index de base zéro qui spécifie la mise à jour en cours d’installation ou de désinstallation lorsque plusieurs mises à jour ont été sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="b94b4-108">Gets a zero-based index value that specifies the update that is currently being installed or uninstalled when multiple updates have been selected.</span></span> |
| [<span data-ttu-id="b94b4-109">**CurrentUpdatePercentComplete**</span><span class="sxs-lookup"><span data-stu-id="b94b4-109">**CurrentUpdatePercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdatepercentcomplete) | <span data-ttu-id="b94b4-110">Obtient la progression du processus d’installation ou de désinstallation de la mise à jour actuelle, sous forme de pourcentage.</span><span class="sxs-lookup"><span data-stu-id="b94b4-110">Gets how far the installation or uninstallation process for the current update has progressed, as a percentage.</span></span>                                    |
| [<span data-ttu-id="b94b4-111">**PourcentageAchevé**</span><span class="sxs-lookup"><span data-stu-id="b94b4-111">**PercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_percentcomplete)                           | <span data-ttu-id="b94b4-112">Obtient le pourcentage de progression de l’installation ou de la désinstallation globale.</span><span class="sxs-lookup"><span data-stu-id="b94b4-112">Gets how far the overall installation or uninstallation process has progressed, as a percentage.</span></span>                                                   |



 

 

 



