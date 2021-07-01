---
description: Demandes d’État OPM
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: Demandes d’État OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbf7338fe1309feb49fd191e3f4a1a22f3639b4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120174"
---
# <a name="opm-status-requests"></a><span data-ttu-id="6908f-103">Demandes d’État OPM</span><span class="sxs-lookup"><span data-stu-id="6908f-103">OPM Status Requests</span></span>

<span data-ttu-id="6908f-104">Cette section répertorie les demandes d’état disponibles pour le [Gestionnaire de protection de sortie](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="6908f-104">This section lists the available status requests for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span> <span data-ttu-id="6908f-105">Pour envoyer une demande d’État OPM, appelez [**IOPMVideoOutput :: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span><span class="sxs-lookup"><span data-stu-id="6908f-105">To send an OPM status request, call [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation).</span></span> <span data-ttu-id="6908f-106">Pour chaque demande, les informations suivantes sont affichées.</span><span class="sxs-lookup"><span data-stu-id="6908f-106">For each request, the following information is listed.</span></span>



| <span data-ttu-id="6908f-107">Value</span><span class="sxs-lookup"><span data-stu-id="6908f-107">Value</span></span>             | <span data-ttu-id="6908f-108">Description</span><span class="sxs-lookup"><span data-stu-id="6908f-108">Description</span></span>                                                                                                                                                           |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6908f-109">GUID de la demande</span><span class="sxs-lookup"><span data-stu-id="6908f-109">Request GUID</span></span> | <span data-ttu-id="6908f-110">Identifie la requête.</span><span class="sxs-lookup"><span data-stu-id="6908f-110">Identifies the request.</span></span> <span data-ttu-id="6908f-111">Définissez la valeur du membre **guidSetting** de la structure des paramètres de l' [**extraction d' \_ \_ informations \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) égale à cette valeur.</span><span class="sxs-lookup"><span data-stu-id="6908f-111">Set the **guidSetting** member of the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="6908f-112">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="6908f-112">Input data</span></span>   | <span data-ttu-id="6908f-113">Spécifie comment interpréter le tableau **abParameters** dans la structure des paramètres de l' [**obtention d' \_ \_ informations \_ OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) .</span><span class="sxs-lookup"><span data-stu-id="6908f-113">Specifies how to interpret the **abParameters** array in the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure.</span></span>                      |
| <span data-ttu-id="6908f-114">Données de sortie</span><span class="sxs-lookup"><span data-stu-id="6908f-114">Output data</span></span>  | <span data-ttu-id="6908f-115">Spécifie comment interpréter le tableau **abRequestedInformation** dans la structure d' [**\_ \_ informations demandée par OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) .</span><span class="sxs-lookup"><span data-stu-id="6908f-115">Specifies how to interpret the **abRequestedInformation** array in the [**OPM\_REQUESTED\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) structure.</span></span>         |



 

<span data-ttu-id="6908f-116">Les demandes d’État suivantes sont définies :</span><span class="sxs-lookup"><span data-stu-id="6908f-116">The following status requests are defined:</span></span>



| <span data-ttu-id="6908f-117">Demande d’État</span><span class="sxs-lookup"><span data-stu-id="6908f-117">Status request</span></span>                                                                                      | <span data-ttu-id="6908f-118">Description</span><span class="sxs-lookup"><span data-stu-id="6908f-118">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6908f-119">**\_prise en \_ main \_ des signaux ACP et \_ CGMSA \_ pour OPM**</span><span class="sxs-lookup"><span data-stu-id="6908f-119">**OPM\_GET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-get-acp-and-cgmsa-signaling.md)                     | <span data-ttu-id="6908f-120">Retourne les informations suivantes sur une sortie vidéo :</span><span class="sxs-lookup"><span data-stu-id="6908f-120">Returns the following information about a video output:</span></span>                                                                                               |
| [<span data-ttu-id="6908f-121">**\_format de \_ \_ sortie OPM \_ obtenu**</span><span class="sxs-lookup"><span data-stu-id="6908f-121">**OPM\_GET\_ACTUAL\_OUTPUT\_FORMAT**</span></span>](opm-get-actual-output-format.md)                            | <span data-ttu-id="6908f-122">Retourne une description du signal vidéo qui est transmis sur le connecteur.</span><span class="sxs-lookup"><span data-stu-id="6908f-122">Returns a description of the video signal that is being transmitted over the connector.</span></span>                                                               |
| [<span data-ttu-id="6908f-123">**\_niveau de \_ \_ protection \_ de l’offre OPM**</span><span class="sxs-lookup"><span data-stu-id="6908f-123">**OPM\_GET\_ACTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-actual-protection-level.md)                      | <span data-ttu-id="6908f-124">Retourne le niveau de protection global pour un mécanisme de protection spécifié.</span><span class="sxs-lookup"><span data-stu-id="6908f-124">Returns the global protection level for a specified protection mechanism.</span></span>                                                                             |
| [<span data-ttu-id="6908f-125">**TYPE de bus d’accès de l' \_ \_ adaptateur OPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6908f-125">**OPM\_GET\_ADAPTER\_BUS\_TYPE**</span></span>](opm-get-adapter-bus-type.md)                                    | <span data-ttu-id="6908f-126">Retourne le type de bus d’e/s utilisé par la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="6908f-126">Returns the type of I/O bus used by the video output.</span></span>                                                                                                 |
| [<span data-ttu-id="6908f-127">**\_informations sur l’extraction de \_ codec OPM \_**</span><span class="sxs-lookup"><span data-stu-id="6908f-127">**OPM\_GET\_CODEC\_INFO**</span></span>](opm-get-codec-info.md)                                                 | <span data-ttu-id="6908f-128">Obtient la valeur mérite d’un codec matériel.</span><span class="sxs-lookup"><span data-stu-id="6908f-128">Gets the merit value of a hardware codec.</span></span>                                                                                                             |
| [<span data-ttu-id="6908f-129">**\_ \_ \_ \_ informations sur l’appareil HDCP \_ connexion à OPM**</span><span class="sxs-lookup"><span data-stu-id="6908f-129">**OPM\_GET\_CONNECTED\_HDCP\_DEVICE\_INFORMATION**</span></span>](opm-get-connected-hdcp-device-information.md) | <span data-ttu-id="6908f-130">Obtient des informations sur un appareil High-Bandwidth Digital protection du contenu (HDCP) attaché à la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="6908f-130">Gets information about a High-Bandwidth Digital Content Protection (HDCP) device attached to the video output.</span></span> <span data-ttu-id="6908f-131">Les informations suivantes sont retournées :</span><span class="sxs-lookup"><span data-stu-id="6908f-131">The following information is returned:</span></span> |
| [<span data-ttu-id="6908f-132">**\_type de \_ connecteur d’extraction OPM \_**</span><span class="sxs-lookup"><span data-stu-id="6908f-132">**OPM\_GET\_CONNECTOR\_TYPE**</span></span>](opm-get-connector-type.md)                                         | <span data-ttu-id="6908f-133">Retourne le type de connecteur physique de la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="6908f-133">Returns the physical connector type of the video output.</span></span>                                                                                              |
| [<span data-ttu-id="6908f-134">**Procurez-vous la \_ \_ \_ version actuelle HDCP \_ SRM \_**</span><span class="sxs-lookup"><span data-stu-id="6908f-134">**OPM\_GET\_CURRENT\_HDCP\_SRM\_VERSION**</span></span>](opm-get-current-hdcp-srm-version.md)                   | <span data-ttu-id="6908f-135">Retourne le numéro de version du message de renouvellement du système (SRM) actuellement utilisé par la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="6908f-135">Returns the version number of the system renewability message (SRM) currently used by the video output.</span></span>                                               |
| [<span data-ttu-id="6908f-136">**\_ \_ caractéristiques DVI de l’offre OPM \_**</span><span class="sxs-lookup"><span data-stu-id="6908f-136">**OPM\_GET\_DVI\_CHARACTERISTICS**</span></span>](opm-get-dvi-characteristics.md)                               | <span data-ttu-id="6908f-137">Demande si un connecteur DVI (Digital Video Interface) prend en charge DVI version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6908f-137">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>                                                          |
| [<span data-ttu-id="6908f-138">**ID de sortie de l' \_ extraction OPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6908f-138">**OPM\_GET\_OUTPUT\_ID**</span></span>](opm-get-output-id.md)                                                   | <span data-ttu-id="6908f-139">Retourne l’identificateur unique de l’analyseur associé à cette sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="6908f-139">Returns the unique identifier of the monitor associated with this video output.</span></span>                                                                       |
| [<span data-ttu-id="6908f-140">**\_types de \_ \_ protection compatibles \_ avec OPM**</span><span class="sxs-lookup"><span data-stu-id="6908f-140">**OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES**</span></span>](opm-get-supported-protection-types.md)                | <span data-ttu-id="6908f-141">Retourne la liste des mécanismes de protection pris en charge par le connecteur.</span><span class="sxs-lookup"><span data-stu-id="6908f-141">Returns the list of protection mechanisms that are supported by the connector.</span></span>                                                                        |
| [<span data-ttu-id="6908f-142">**\_niveau de \_ \_ protection \_ de l’offre OPM**</span><span class="sxs-lookup"><span data-stu-id="6908f-142">**OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL**</span></span>](opm-get-virtual-protection-level.md)                    | <span data-ttu-id="6908f-143">Retourne le niveau de protection virtuel pour un mécanisme de protection spécifié.</span><span class="sxs-lookup"><span data-stu-id="6908f-143">Returns the virtual protection level for a specified protection mechanism.</span></span>                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="6908f-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6908f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6908f-145">Informations de référence sur la programmation OPM</span><span class="sxs-lookup"><span data-stu-id="6908f-145">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="6908f-146">Gestionnaire de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="6908f-146">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



