---
description: Répertorie les interfaces fournies par le moteur de pièce jointe.
ms.assetid: 451587bd-a7ab-446b-b647-be98de251915
title: Interfaces de gestion de la sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b3a205757a3bf324a5308a5f6fbc3d63374b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520107"
---
# <a name="security-management-interfaces"></a><span data-ttu-id="15522-103">Interfaces de gestion de la sécurité</span><span class="sxs-lookup"><span data-stu-id="15522-103">Security Management Interfaces</span></span>

<span data-ttu-id="15522-104">Cette section contient des pages de référence pour les groupes d’interfaces suivants :</span><span class="sxs-lookup"><span data-stu-id="15522-104">This section contains reference pages for the following groups of interfaces:</span></span>

-   [<span data-ttu-id="15522-105">Interfaces du moteur de pièce jointe</span><span class="sxs-lookup"><span data-stu-id="15522-105">Attachment Engine Interfaces</span></span>](#attachment-engine-interfaces)

## <a name="attachment-engine-interfaces"></a><span data-ttu-id="15522-106">Interfaces du moteur de pièce jointe</span><span class="sxs-lookup"><span data-stu-id="15522-106">Attachment Engine Interfaces</span></span>



| <span data-ttu-id="15522-107">Interface</span><span class="sxs-lookup"><span data-stu-id="15522-107">Interface</span></span>                                                            | <span data-ttu-id="15522-108">Description</span><span class="sxs-lookup"><span data-stu-id="15522-108">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15522-109">**ISceSvcAttachmentData**</span><span class="sxs-lookup"><span data-stu-id="15522-109">**ISceSvcAttachmentData**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)               | <span data-ttu-id="15522-110">Récupère les données de configuration et d’analyse relatives à un service de sécurité spécifié à partir des composants logiciels enfichables de configuration de sécurité. Les composants logiciels enfichables de configuration de la sécurité exposent cette interface, qui permet d’appeler les extensions de composant logiciel enfichable d’attachement pour demander des informations sur la configuration ou l’analyse.</span><span class="sxs-lookup"><span data-stu-id="15522-110">Retrieves configuration and analysis data about a specified security service from the Security Configuration snap-ins. The Security Configuration snap-ins expose this interface, which attachment snap-in extensions call to query configuration or analysis information.</span></span>                                                 |
| [<span data-ttu-id="15522-111">**ISceSvcAttachmentPersistInfo**</span><span class="sxs-lookup"><span data-stu-id="15522-111">**ISceSvcAttachmentPersistInfo**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) | <span data-ttu-id="15522-112">Récupère les informations de configuration ou d’analyse modifiées à partir d’un composant logiciel enfichable pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="15522-112">Retrieves modified configuration or analysis information from an attachment snap-in.</span></span> <span data-ttu-id="15522-113">Les composants logiciels enfichables de configuration de la sécurité appellent cette interface pour récupérer toutes les informations modifiées à partir de l’extension du composant logiciel enfichable pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="15522-113">The Security Configuration snap-ins calls this interface to retrieve any modified information from the attachment snap-in extension.</span></span> <span data-ttu-id="15522-114">Le composant logiciel enfichable Configuration de la sécurité stocke ensuite ces données de manière appropriée dans la base de données de sécurité.</span><span class="sxs-lookup"><span data-stu-id="15522-114">The Security Configuration snap-in then stores this data appropriately in the security database.</span></span> |



 

<span data-ttu-id="15522-115">Pour plus d’informations sur les interfaces COM qui doivent être implémentées par les extensions de composant logiciel enfichable, consultez la documentation de la console MMC ( [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) ).</span><span class="sxs-lookup"><span data-stu-id="15522-115">For more information about the COM interfaces that must be implemented by snap-in extensions, see the [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) documentation.</span></span>

 

 
