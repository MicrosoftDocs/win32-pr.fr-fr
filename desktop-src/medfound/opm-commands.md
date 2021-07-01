---
description: Commandes OPM
ms.assetid: 52165e1b-a178-4483-bf76-4197281f856d
title: Commandes OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b00240925c28322b911ab55a0e4f026f051d6ec
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119144"
---
# <a name="opm-commands"></a><span data-ttu-id="c9173-103">Commandes OPM</span><span class="sxs-lookup"><span data-stu-id="c9173-103">OPM Commands</span></span>

<span data-ttu-id="c9173-104">Cette section répertorie les commandes disponibles pour le [Gestionnaire de protection de sortie](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="c9173-104">This section lists the available commands for [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>

<span data-ttu-id="c9173-105">Pour envoyer une commande OPM, appelez [**IOPMVideoOutput :: configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span><span class="sxs-lookup"><span data-stu-id="c9173-105">To send an OPM command, call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span></span> <span data-ttu-id="c9173-106">Pour chaque commande, les informations suivantes sont affichées.</span><span class="sxs-lookup"><span data-stu-id="c9173-106">For each command, the following information is listed.</span></span>



| <span data-ttu-id="c9173-107">Value</span><span class="sxs-lookup"><span data-stu-id="c9173-107">Value</span></span>             | <span data-ttu-id="c9173-108">Description</span><span class="sxs-lookup"><span data-stu-id="c9173-108">Description</span></span>                                                                                                                                                            |
|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9173-109">GUID de la commande</span><span class="sxs-lookup"><span data-stu-id="c9173-109">Command GUID</span></span> | <span data-ttu-id="c9173-110">Identifie la commande.</span><span class="sxs-lookup"><span data-stu-id="c9173-110">Identifies the command.</span></span> <span data-ttu-id="c9173-111">Définissez la valeur du membre **guidSetting** de la structure des [**\_ \_ paramètres de configuration OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) comme égale à cette valeur.</span><span class="sxs-lookup"><span data-stu-id="c9173-111">Set the **guidSetting** member of the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure equal to this value.</span></span> |
| <span data-ttu-id="c9173-112">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="c9173-112">Input data</span></span>   | <span data-ttu-id="c9173-113">Spécifie comment interpréter le tableau **abParameters** dans la structure des [**\_ \_ paramètres de configuration de OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) .</span><span class="sxs-lookup"><span data-stu-id="c9173-113">Specifies how to interpret the **abParameters** array in the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure.</span></span>                      |



 

<span data-ttu-id="c9173-114">Les commandes suivantes sont définies :</span><span class="sxs-lookup"><span data-stu-id="c9173-114">The following commands are defined:</span></span>



| <span data-ttu-id="c9173-115">Commande</span><span class="sxs-lookup"><span data-stu-id="c9173-115">Command</span></span>                                                                                                       | <span data-ttu-id="c9173-116">Description</span><span class="sxs-lookup"><span data-stu-id="c9173-116">Description</span></span>                                                                                         |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9173-117">**\_ \_ \_ signaux ACP et \_ CGMSA de \_ l’ensemble OPM**</span><span class="sxs-lookup"><span data-stu-id="c9173-117">**OPM\_SET\_ACP\_AND\_CGMSA\_SIGNALING**</span></span>](opm-set-acp-and-cgmsa-signaling.md)                               | <span data-ttu-id="c9173-118">Spécifie des informations sur le signal vidéo, autres que le niveau de protection.</span><span class="sxs-lookup"><span data-stu-id="c9173-118">Specifies information about the video signal, other than the protection level.</span></span>                      |
| [<span data-ttu-id="c9173-119">**\_SRM Set \_ HDCP \_**</span><span class="sxs-lookup"><span data-stu-id="c9173-119">**OPM\_SET\_HDCP\_SRM**</span></span>](opm-set-hdcp-srm.md)                                                               | <span data-ttu-id="c9173-120">Met à jour le message de renouvellement du système (SRM) pour High-Bandwidth protection du contenu numérique (HDCP).</span><span class="sxs-lookup"><span data-stu-id="c9173-120">Updates the system renewability message (SRM) for High-Bandwidth Digital Content Protection (HDCP).</span></span> |
| [<span data-ttu-id="c9173-121">**niveau de protection de l' \_ ensemble OPM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c9173-121">**OPM\_SET\_PROTECTION\_LEVEL**</span></span>](opm-set-protection-level.md)                                               | <span data-ttu-id="c9173-122">Définit le niveau de protection d’un mécanisme de protection de sortie.</span><span class="sxs-lookup"><span data-stu-id="c9173-122">Sets the protection level for an output protection mechanism.</span></span>                                       |
| [<span data-ttu-id="c9173-123">**\_ \_ niveau de protection de l’ensemble OPM \_ selon le \_ \_ \_ \_ DVD CSS**</span><span class="sxs-lookup"><span data-stu-id="c9173-123">**OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD**</span></span>](opm-set-protection-level-according-to-css-dvd.md) | <span data-ttu-id="c9173-124">Définit le niveau de protection HDCP pour la lecture des DVD, en suivant les règles du système de brouillage du contenu DVD (CSS).</span><span class="sxs-lookup"><span data-stu-id="c9173-124">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c9173-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9173-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9173-126">Informations de référence sur la programmation OPM</span><span class="sxs-lookup"><span data-stu-id="c9173-126">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="c9173-127">Gestionnaire de protection de sortie</span><span class="sxs-lookup"><span data-stu-id="c9173-127">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



