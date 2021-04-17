---
description: Toutes les machines virtuelles reflètent la présence d’un contrôleur vidéo S3 émulé et d’un contrôleur vidéo synthétique accéléré.
ms.assetid: 93BDC827-E84A-4460-A2DD-18EE87254426
title: Classes vidéo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8687dc1f4c00c363ca9277c8404b338a0b7f7851
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485696"
---
# <a name="video-classes"></a><span data-ttu-id="41cbf-103">Classes vidéo</span><span class="sxs-lookup"><span data-stu-id="41cbf-103">Video classes</span></span>

<span data-ttu-id="41cbf-104">Toutes les machines virtuelles reflètent la présence d’un contrôleur vidéo S3 émulé et d’un contrôleur vidéo synthétique accéléré.</span><span class="sxs-lookup"><span data-stu-id="41cbf-104">All virtual machines reflect the presence of an emulated S3 video controller and an accelerated, synthetic video controller.</span></span>

<span data-ttu-id="41cbf-105">Un objet tête vidéo est associé à chaque contrôleur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="41cbf-105">Each display controller has a video head object associated with it.</span></span> <span data-ttu-id="41cbf-106">Un seul contrôleur d’affichage peut être actif sur une machine virtuelle à tout moment.</span><span class="sxs-lookup"><span data-stu-id="41cbf-106">Only one display controller can be active in a virtual machine at any time.</span></span>

<span data-ttu-id="41cbf-107">Une connexion de terminal est présente pour chaque session à distance active connectée à une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="41cbf-107">A terminal connection is present for every active remote session connected to a virtual machine.</span></span>

<span data-ttu-id="41cbf-108">Voici les classes WMI de virtualisation associées à Video.</span><span class="sxs-lookup"><span data-stu-id="41cbf-108">The following are virtualization WMI classes related to video.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="41cbf-109">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="41cbf-109">In this section</span></span>



| <span data-ttu-id="41cbf-110">Rubrique</span><span class="sxs-lookup"><span data-stu-id="41cbf-110">Topic</span></span>                                                                                  | <span data-ttu-id="41cbf-111">Description</span><span class="sxs-lookup"><span data-stu-id="41cbf-111">Description</span></span>                                                                                                                |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41cbf-112">**MSVM \_ S3DisplayController**</span><span class="sxs-lookup"><span data-stu-id="41cbf-112">**Msvm\_S3DisplayController**</span></span>](msvm-s3displaycontroller.md)<br/>               | <span data-ttu-id="41cbf-113">Représente l’état du contrôleur S3 émulé qui est présent dans chaque configuration d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="41cbf-113">Represents the state of the emulated S3 controller that is present in each virtual machine configuration.</span></span><br/>       |
| [<span data-ttu-id="41cbf-114">**MSVM \_ SyntheticDisplayController**</span><span class="sxs-lookup"><span data-stu-id="41cbf-114">**Msvm\_SyntheticDisplayController**</span></span>](msvm-syntheticdisplaycontroller.md)<br/> | <span data-ttu-id="41cbf-115">Représente l’état du contrôleur d’affichage synthétique qui est présent dans chaque configuration d’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="41cbf-115">Represents the state of the synthetic display controller that is present in each virtual machine configuration.</span></span><br/> |
| [<span data-ttu-id="41cbf-116">**MSVM \_ SystemTerminalConnection**</span><span class="sxs-lookup"><span data-stu-id="41cbf-116">**Msvm\_SystemTerminalConnection**</span></span>](msvm-systemterminalconnection.md)<br/>     | <span data-ttu-id="41cbf-117">Associe un ordinateur virtuel à une connexion de terminal.</span><span class="sxs-lookup"><span data-stu-id="41cbf-117">Associates a virtual machine with a terminal connection.</span></span><br/>                                                        |
| [<span data-ttu-id="41cbf-118">**MSVM \_ TerminalConnection**</span><span class="sxs-lookup"><span data-stu-id="41cbf-118">**Msvm\_TerminalConnection**</span></span>](msvm-terminalconnection.md)<br/>                 | <span data-ttu-id="41cbf-119">Indique l’état d’une session à distance active qui interagit avec un ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="41cbf-119">Indicates the state of an active remote session interacting with a virtual machine.</span></span><br/>                             |
| [<span data-ttu-id="41cbf-120">**MSVM \_ VideoHead**</span><span class="sxs-lookup"><span data-stu-id="41cbf-120">**Msvm\_VideoHead**</span></span>](msvm-videohead.md)<br/>                                   | <span data-ttu-id="41cbf-121">Décrit la surface de dessin principale sur un contrôleur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="41cbf-121">Describes the primary drawing surface on a display controller.</span></span><br/>                                                  |
| [<span data-ttu-id="41cbf-122">**MSVM \_ VideoHeadOnController**</span><span class="sxs-lookup"><span data-stu-id="41cbf-122">**Msvm\_VideoHeadOnController**</span></span>](msvm-videoheadoncontroller.md)<br/>           | <span data-ttu-id="41cbf-123">Associe une tête vidéo au contrôleur vidéo qui l’intègre.</span><span class="sxs-lookup"><span data-stu-id="41cbf-123">Associates a video head with the video controller that includes it.</span></span><br/>                                             |



 

 

 




