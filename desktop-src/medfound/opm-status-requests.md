---
description: Demandes d’État OPM
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: Demandes d’État OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd994d7cb8d43db23fe59352dba830e741b74b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753916"
---
# <a name="opm-status-requests"></a><span data-ttu-id="27ce6-103">Demandes d’État OPM</span><span class="sxs-lookup"><span data-stu-id="27ce6-103">OPM Status Requests</span></span>

<span data-ttu-id="27ce6-104">Cette section répertorie les demandes d’état disponibles pour le [Gestionnaire de protection de sortie](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="27ce6-104">This section lists the available status requests for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span> <span data-ttu-id="27ce6-105">Pour envoyer une demande d’État OPM, appelez [**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span><span class="sxs-lookup"><span data-stu-id="27ce6-105">To send an OPM status request, call [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span></span> <span data-ttu-id="27ce6-106">Pour chaque demande, les informations suivantes sont affichées.</span><span class="sxs-lookup"><span data-stu-id="27ce6-106">For each request, the following information is listed.</span></span>



|              |                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27ce6-107">GUID de la demande</span><span class="sxs-lookup"><span data-stu-id="27ce6-107">Request GUID</span></span> | <span data-ttu-id="27ce6-108">Identifie la requête.</span><span class="sxs-lookup"><span data-stu-id="27ce6-108">Identifies the request.</span></span> <span data-ttu-id="27ce6-109">Définissez la valeur du membre **guidSetting** de la structure des paramètres de l' [**extraction d' \_ \_ informations \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) égale à cette valeur.</span><span class="sxs-lookup"><span data-stu-id="27ce6-109">Set the **guidSetting** member of the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="27ce6-110">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="27ce6-110">Input data</span></span>   | <span data-ttu-id="27ce6-111">Spécifie comment interpréter le tableau **abParameters** dans la structure des paramètres de l' [**obtention d' \_ \_ informations \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) .</span><span class="sxs-lookup"><span data-stu-id="27ce6-111">Specifies how to interpret the **abParameters** array in the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure.</span></span>                      |
| <span data-ttu-id="27ce6-112">Données de sortie</span><span class="sxs-lookup"><span data-stu-id="27ce6-112">Output data</span></span>  | <span data-ttu-id="27ce6-113">Spécifie comment interpréter le tableau **abRequestedInformation** dans la structure d' [**\_ \_ informations demandée par OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) .</span><span class="sxs-lookup"><span data-stu-id="27ce6-113">Specifies how to interpret the **abRequestedInformation** array in the [**OPM\_REQUESTED\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) structure.</span></span>         |



 

<span data-ttu-id="27ce6-114">Les demandes d’État suivantes sont définies :</span><span class="sxs-lookup"><span data-stu-id="27ce6-114">The following status requests are defined:</span></span>



| <span data-ttu-id="27ce6-115">Demande d’État</span><span class="sxs-lookup"><span data-stu-id="27ce6-115">Status request</span></span>                                                                                      | <span data-ttu-id="27ce6-116">Description</span><span class="sxs-lookup"><span data-stu-id="27ce6-116">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27ce6-117">**\_prise en \_ main \_ des signaux ACP et \_ CGMSA \_ pour OPM**</span><span class="sxs-lookup"><span data-stu-id="27ce6-117">**OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-get-acp-and-cgmsa-signaling.md)                     | <span data-ttu-id="27ce6-118">Retourne les informations suivantes sur une sortie vidéo :</span><span class="sxs-lookup"><span data-stu-id="27ce6-118">Returns the following information about a video output:</span></span>                                                                                               |
| [<span data-ttu-id="27ce6-119">**\_format de \_ \_ sortie OPM \_ obtenu**</span><span class="sxs-lookup"><span data-stu-id="27ce6-119">**OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT**</span></span>](opm-get-actual-output-format.md)                            | <span data-ttu-id="27ce6-120">Retourne une description du signal vidéo qui est transmis sur le connecteur.</span><span class="sxs-lookup"><span data-stu-id="27ce6-120">Returns a description of the video signal that is being transmitted over the connector.</span></span>                                                               |
| [<span data-ttu-id="27ce6-121">**\_niveau de \_ \_ protection \_ de l’offre OPM**</span><span class="sxs-lookup"><span data-stu-id="27ce6-121">**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-actual-protection-level.md)                      | <span data-ttu-id="27ce6-122">Retourne le niveau de protection global pour un mécanisme de protection spécifié.</span><span class="sxs-lookup"><span data-stu-id="27ce6-122">Returns the global protection level for a specified protection mechanism.</span></span>                                                                             |
| [<span data-ttu-id="27ce6-123">**TYPE de bus d’accès de l' \_ \_ adaptateur OPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="27ce6-123">**OPM\_GET\_ADAPTER\_BUS\_TYPE**</span></span>](opm-get-adapter-bus-type.md)                                    | <span data-ttu-id="27ce6-124">Retourne le type de bus d’e/s utilisé par la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="27ce6-124">Returns the type of I/O bus used by the video output.</span></span>                                                                                                 |
| [<span data-ttu-id="27ce6-125">**\_informations sur l’extraction de \_ codec OPM \_**</span><span class="sxs-lookup"><span data-stu-id="27ce6-125">**OPM\_GET\_CODEC\_INFO**</span></span>](opm-get-codec-info.md)                                                 | <span data-ttu-id="27ce6-126">Obtient la valeur mérite d’un codec matériel.</span><span class="sxs-lookup"><span data-stu-id="27ce6-126">Gets the merit value of a hardware codec.</span></span>                                                                                                             |
| [<span data-ttu-id="27ce6-127">**\_ \_ \_ \_ informations sur l’appareil HDCP \_ connexion à OPM**</span><span class="sxs-lookup"><span data-stu-id="27ce6-127">**OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**</span></span>](opm-get-connected-hdcp-device-information.md) | <span data-ttu-id="27ce6-128">Obtient des informations sur un appareil High-Bandwidth Digital protection du contenu (HDCP) attaché à la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="27ce6-128">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="27ce6-129">Les informations suivantes sont retournées :</span><span class="sxs-lookup"><span data-stu-id="27ce6-129">The following information is returned:</span></span> |
| [<span data-ttu-id="27ce6-130">**\_type de \_ connecteur d’extraction OPM \_**</span><span class="sxs-lookup"><span data-stu-id="27ce6-130">**OPM\_GET\_CONNECTOR\_TYPE**</span></span>](opm-get-connector-type.md)                                         | <span data-ttu-id="27ce6-131">Retourne le type de connecteur physique de la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="27ce6-131">Returns the physical connector type of the video output.</span></span>                                                                                              |
| [<span data-ttu-id="27ce6-132">**Procurez-vous la \_ \_ \_ version actuelle HDCP \_ SRM \_**</span><span class="sxs-lookup"><span data-stu-id="27ce6-132">**OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION**</span></span>](opm-get-current-hdcp-srm-version.md)                   | <span data-ttu-id="27ce6-133">Retourne le numéro de version du message de renouvellement du système (SRM) actuellement utilisé par la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="27ce6-133">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>                                               |
| [<span data-ttu-id="27ce6-134">**\_ \_ caractéristiques DVI de l’offre OPM \_**</span><span class="sxs-lookup"><span data-stu-id="27ce6-134">**OPM\_GET\_DVI\_CHARACTERISTICS**</span></span>](opm-get-dvi-characteristics.md)                               | <span data-ttu-id="27ce6-135">Demande si un connecteur DVI (Digital Video Interface) prend en charge DVI version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="27ce6-135">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>                                                          |
| [<span data-ttu-id="27ce6-136">**ID de sortie de l' \_ extraction OPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="27ce6-136">**OPM\_GET\_OUTPUT\_ID**</span></span>](opm-get-output-id.md)                                                   | <span data-ttu-id="27ce6-137">Retourne l’identificateur unique de l’analyseur associé à cette sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="27ce6-137">Returns the unique identifier of the monitor associated with this video output.</span></span>                                                                       |
| [<span data-ttu-id="27ce6-138">**\_types de \_ \_ protection compatibles \_ avec OPM**</span><span class="sxs-lookup"><span data-stu-id="27ce6-138">**OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES**</span></span>](opm-get-supported-protection-types.md)                | <span data-ttu-id="27ce6-139">Retourne la liste des mécanismes de protection pris en charge par le connecteur.</span><span class="sxs-lookup"><span data-stu-id="27ce6-139">Returns the list of protection mechanisms that are supported by the connector.</span></span>                                                                        |
| [<span data-ttu-id="27ce6-140">**\_niveau de \_ \_ protection \_ de l’offre OPM**</span><span class="sxs-lookup"><span data-stu-id="27ce6-140">**OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-virtual-protection-level.md)                    | <span data-ttu-id="27ce6-141">Retourne le niveau de protection virtuel pour un mécanisme de protection spécifié.</span><span class="sxs-lookup"><span data-stu-id="27ce6-141">Returns the virtual protection level for a specified protection mechanism.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="27ce6-142">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="27ce6-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27ce6-143">Informations de référence sur la programmation OPM</span><span class="sxs-lookup"><span data-stu-id="27ce6-143">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="27ce6-144">Gestionnaire de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="27ce6-144">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



