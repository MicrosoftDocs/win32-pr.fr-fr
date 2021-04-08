---
description: L’interface IUpdateDownloader définit les propriétés suivantes.
ms.assetid: b6a30356-f97d-408f-becd-a467e9f8e79f
title: Propriétés IUpdateDownloader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c16aa762bcc14dc1919ef91d162752652c327e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752084"
---
# <a name="iupdatedownloader-properties"></a><span data-ttu-id="54150-103">Propriétés IUpdateDownloader</span><span class="sxs-lookup"><span data-stu-id="54150-103">IUpdateDownloader Properties</span></span>

<span data-ttu-id="54150-104">L’interface [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) définit les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="54150-104">The [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) interface defines the following properties.</span></span>



| <span data-ttu-id="54150-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="54150-105">Property</span></span>                                                             | <span data-ttu-id="54150-106">Description</span><span class="sxs-lookup"><span data-stu-id="54150-106">Description</span></span>                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54150-107">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="54150-107">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid) | <span data-ttu-id="54150-108">Obtient et définit l’application cliente actuelle.</span><span class="sxs-lookup"><span data-stu-id="54150-108">Gets and sets the current client application.</span></span>                                                                                                                              |
| [<span data-ttu-id="54150-109">**IsForced**</span><span class="sxs-lookup"><span data-stu-id="54150-109">**IsForced**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_isforced)                       | <span data-ttu-id="54150-110">Obtient et définit une valeur booléenne qui indique si l’agent de Windows Update (WUA) force le téléchargement des mises à jour déjà installées ou qui ne peuvent pas être installées.</span><span class="sxs-lookup"><span data-stu-id="54150-110">Gets and sets a Boolean value that indicates whether the Windows Update Agent (WUA) forces the download of updates that are already installed or that cannot be installed.</span></span> |
| [<span data-ttu-id="54150-111">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="54150-111">**Priority**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_priority)                       | <span data-ttu-id="54150-112">Obtient et définit le niveau de priorité du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="54150-112">Gets and sets the priority level of the download.</span></span>                                                                                                                          |
| [<span data-ttu-id="54150-113">**Mises à jour**</span><span class="sxs-lookup"><span data-stu-id="54150-113">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_updates)                         | <span data-ttu-id="54150-114">Obtient et définit une interface qui contient une collection en lecture seule des mises à jour spécifiées pour le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="54150-114">Gets and sets an interface that contains a read-only collection of the updates that are specified for download.</span></span>                                                            |



 

 

 



