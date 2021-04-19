---
description: Commandes OPM
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: Commandes OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aa14026123656b26e978bc179d65c3b61913c62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545805"
---
# <a name="opm-commands"></a><span data-ttu-id="d0232-103">Commandes OPM</span><span class="sxs-lookup"><span data-stu-id="d0232-103">OPM Commands</span></span>

<span data-ttu-id="d0232-104">Cette section répertorie les commandes disponibles pour le [Gestionnaire de protection de sortie](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="d0232-104">This section lists the available commands for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

<span data-ttu-id="d0232-105">Pour envoyer une commande OPM, appelez [**IOPMVideoOutput :: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span><span class="sxs-lookup"><span data-stu-id="d0232-105">To send an OPM command, call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span></span> <span data-ttu-id="d0232-106">Pour chaque commande, les informations suivantes sont affichées.</span><span class="sxs-lookup"><span data-stu-id="d0232-106">For each command, the following information is listed.</span></span>



|              |                                                                                                                                                             |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0232-107">GUID de la commande</span><span class="sxs-lookup"><span data-stu-id="d0232-107">Command GUID</span></span> | <span data-ttu-id="d0232-108">Identifie la commande.</span><span class="sxs-lookup"><span data-stu-id="d0232-108">Identifies the command.</span></span> <span data-ttu-id="d0232-109">Définissez la valeur du membre **guidSetting** de la structure des [**\_ \_ paramètres de configuration OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) comme égale à cette valeur.</span><span class="sxs-lookup"><span data-stu-id="d0232-109">Set the **guidSetting** member of the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="d0232-110">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="d0232-110">Input data</span></span>   | <span data-ttu-id="d0232-111">Spécifie comment interpréter le tableau **abParameters** dans la structure des [**\_ \_ paramètres de configuration de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) .</span><span class="sxs-lookup"><span data-stu-id="d0232-111">Specifies how to interpret the **abParameters** array in the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure.</span></span>                      |



 

<span data-ttu-id="d0232-112">Les commandes suivantes sont définies :</span><span class="sxs-lookup"><span data-stu-id="d0232-112">The following commands are defined:</span></span>



| <span data-ttu-id="d0232-113">Commande</span><span class="sxs-lookup"><span data-stu-id="d0232-113">Command</span></span>                                                                                                       | <span data-ttu-id="d0232-114">Description</span><span class="sxs-lookup"><span data-stu-id="d0232-114">Description</span></span>                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d0232-115">**\_ \_ \_ signaux ACP et \_ CGMSA de \_ l’ensemble OPM**</span><span class="sxs-lookup"><span data-stu-id="d0232-115">**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-set-acp-and-cgmsa-signaling.md)                               | <span data-ttu-id="d0232-116">Spécifie des informations sur le signal vidéo, autres que le niveau de protection.</span><span class="sxs-lookup"><span data-stu-id="d0232-116">Specifies information about the video signal, other than the protection level.</span></span>                      |
| [<span data-ttu-id="d0232-117">**\_SRM Set \_ HDCP \_**</span><span class="sxs-lookup"><span data-stu-id="d0232-117">**OPM\_SET\_HDCP\_SRM**</span></span>](opm-set-hdcp-srm.md)                                                               | <span data-ttu-id="d0232-118">Met à jour le message de renouvellement du système (SRM) pour High-Bandwidth protection du contenu numérique (HDCP).</span><span class="sxs-lookup"><span data-stu-id="d0232-118">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span> |
| [<span data-ttu-id="d0232-119">**niveau de protection de l' \_ ensemble OPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d0232-119">**OPM\_SET\_PROTECTION\_LEVEL**</span></span>](opm-set-protection-level.md)                                               | <span data-ttu-id="d0232-120">Définit le niveau de protection d’un mécanisme de protection de sortie.</span><span class="sxs-lookup"><span data-stu-id="d0232-120">Sets the protection level for an output protection mechanism.</span></span>                                       |
| [<span data-ttu-id="d0232-121">**\_ \_ niveau de protection de l’ensemble OPM \_ selon le \_ \_ \_ \_ DVD CSS**</span><span class="sxs-lookup"><span data-stu-id="d0232-121">**OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD**</span></span>](opm-set-protection-level-according-to-css-dvd.md) | <span data-ttu-id="d0232-122">Définit le niveau de protection HDCP pour la lecture des DVD, en suivant les règles du système de brouillage du contenu DVD (CSS).</span><span class="sxs-lookup"><span data-stu-id="d0232-122">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d0232-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d0232-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0232-124">Informations de référence sur la programmation OPM</span><span class="sxs-lookup"><span data-stu-id="d0232-124">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="d0232-125">Gestionnaire de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="d0232-125">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



