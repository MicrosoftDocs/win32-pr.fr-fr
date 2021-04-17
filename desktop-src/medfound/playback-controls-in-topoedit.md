---
description: Contrôles de lecture dans TopoEdit
ms.assetid: 36ebfa9e-7092-4a93-b633-8eefef8ac9e6
title: Contrôles de lecture dans TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174317fbf53dc6d2573414c60d5d4cde1a010f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557410"
---
# <a name="playback-controls-in-topoedit"></a><span data-ttu-id="af939-103">Contrôles de lecture dans TopoEdit</span><span class="sxs-lookup"><span data-stu-id="af939-103">Playback Controls in TopoEdit</span></span>

<span data-ttu-id="af939-104">Une fois la topologie résolue, elle est mise en file d’attente dans la session multimédia pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="af939-104">After a topology is resolved, it is queued on the Media Session for playback.</span></span> <span data-ttu-id="af939-105">TopoEdit fournit un contrôle de transport pour la modification de l’état de la topologie sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="af939-105">TopoEdit provides transport control for changing the state of topology on the Media Session.</span></span>

<span data-ttu-id="af939-106">Le tableau suivant présente la commande menu/barre d’outils et la méthode Media Foundation équivalente pour chaque opération.</span><span class="sxs-lookup"><span data-stu-id="af939-106">The following table shows the menu/toolbar command and the equivalent Media Foundation method for each operation.</span></span>



| <span data-ttu-id="af939-107">Menu/commande de barre d’outils</span><span class="sxs-lookup"><span data-stu-id="af939-107">Menu/Toolbar Command</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="af939-108">Méthode Media Foundation</span><span class="sxs-lookup"><span data-stu-id="af939-108">Media Foundation Method</span></span>                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="af939-109">Dans le menu **contrôles** , cliquez sur **lire**. \[ nouvelle ligne \] -ou- \[ saut de ligne \] cliquez sur le bouton **lecture** dans la barre d’outils (illustrée dans l’image suivante). \[ \] ![ capture d’écran de nouvelle ligne du bouton de lecture](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)</span><span class="sxs-lookup"><span data-stu-id="af939-109">On the **Controls** menu, click **Play**.\[newline\] -or-\[newline\] click the **play** button on the toolbar (shown in the following image).\[newline\]![screen shot of the play button](images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg)</span></span>    | [<span data-ttu-id="af939-110">**IMFMediaSession :: Start**</span><span class="sxs-lookup"><span data-stu-id="af939-110">**IMFMediaSession::Start**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) |
| <span data-ttu-id="af939-111">Dans le menu **contrôles** , cliquez sur **arrêter**. \[ nouvelle ligne \] -ou- \[ saut de ligne \] cliquez sur le bouton **arrêter** dans la barre d’outils (illustrée dans l’image suivante). \[ \] ![ capture d’écran de saut de ligne du bouton arrêter](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)</span><span class="sxs-lookup"><span data-stu-id="af939-111">On the **Controls** menu, click **Stop**.\[newline\] -or-\[newline\] click the **stop** button on the toolbar (shown in the following image).\[newline\]![screen shot of the stop button](images/f74657f8-12b3-414a-a1f1-39b7ae2b20f1.jpg)</span></span>    | [<span data-ttu-id="af939-112">**IMFMediaSession :: Stop**</span><span class="sxs-lookup"><span data-stu-id="af939-112">**IMFMediaSession::Stop**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)   |
| <span data-ttu-id="af939-113">Dans le menu **contrôles** , cliquez sur **suspendre**. \[ nouvelle ligne \] -ou- \[ saut de ligne \] cliquez sur le bouton **Pause** dans la barre d’outils (illustrée dans l’image suivante). \[ \] ![ capture d’écran de saut de ligne du bouton pause](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg)</span><span class="sxs-lookup"><span data-stu-id="af939-113">On the **Controls** menu, click **Pause**.\[newline\] -or-\[newline\] click the **pause** button on the toolbar (shown in the following image).\[newline\]![screen shot of the pause button](images/156351f1-7215-4062-b4a1-0a0aaa79d205.jpg)</span></span> | [<span data-ttu-id="af939-114">**IMFMediaSession ::P ause**</span><span class="sxs-lookup"><span data-stu-id="af939-114">**IMFMediaSession::Pause**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) |



 

<span data-ttu-id="af939-115">Pour plus d’informations sur le contrôle de la lecture par programme à l’aide d’API Media Foundation, consultez Guide pratique [pour contrôler les États de présentation](how-to-control-presentation-states.md).</span><span class="sxs-lookup"><span data-stu-id="af939-115">For information about controlling the playback programmatically by using Media Foundation APIs, see [How to Control Presentation States](how-to-control-presentation-states.md).</span></span>

## <a name="seeking"></a><span data-ttu-id="af939-116">Cherche</span><span class="sxs-lookup"><span data-stu-id="af939-116">Seeking</span></span>

<span data-ttu-id="af939-117">Si la topologie est recherchée, vous pouvez effectuer une recherche à l’aide de la barre de recherche (illustrée dans l’image suivante) pour spécifier un emplacement dans la chronologie de la topologie pour commencer la lecture.</span><span class="sxs-lookup"><span data-stu-id="af939-117">If the topology is seekable, you can seek by using the seek bar (shown in the following image) to specify a place in the topology's timeline to begin playback.</span></span>

![capture d’écran de la barre de recherche](images/95a4e3ef-8489-4e26-9f02-436f81d8a96e.jpg)

> [!Note]  
> <span data-ttu-id="af939-119">Si la source du média est recherchée, la commande Stop rétablit également la topologie jusqu’au début du flux.</span><span class="sxs-lookup"><span data-stu-id="af939-119">If the media source is seekable, the Stop command also seeks the topology back to the start of the stream.</span></span>

 

## <a name="changing-the-playback-rate"></a><span data-ttu-id="af939-120">Modification de la vitesse de lecture</span><span class="sxs-lookup"><span data-stu-id="af939-120">Changing the Playback Rate</span></span>

<span data-ttu-id="af939-121">Si la source du média sous-jacent pour la topologie prend en charge plusieurs vitesses de lecture, vous pouvez utiliser la barre de taux pour modifier la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="af939-121">If the underlying media source for the topology supports multiple playback rates, you can use the rate bar to change the playback rate.</span></span> <span data-ttu-id="af939-122">Pour avancer rapidement une topologie sur la session multimédia, augmentez la vitesse en faisant glisser le curseur vers la droite, comme illustré dans l’image suivante.</span><span class="sxs-lookup"><span data-stu-id="af939-122">To fast-forward a topology on the Media Session, increase the rate by dragging the slider to the right, as shown in the following image.</span></span>

![capture d’écran de la barre de taux](images/6e094ecf-c87f-4f27-bca7-a53cc790f5c2.jpg)

> [!Note]  
> <span data-ttu-id="af939-124">Dans cette version, TopoEdit prend uniquement en charge les taux positifs.</span><span class="sxs-lookup"><span data-stu-id="af939-124">In this version, TopoEdit only supports positive rates.</span></span> <span data-ttu-id="af939-125">La lecture inversée n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="af939-125">Reverse playback is not supported.</span></span>

 

<span data-ttu-id="af939-126">Pour plus d’informations sur la modification par programmation de la vitesse de lecture à l’aide d’API Media Foundation, consultez [à propos du contrôle de la fréquence](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="af939-126">For information about changing the playback rate programmatically by using Media Foundation APIs, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="af939-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="af939-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af939-128">Menus TopoEdit</span><span class="sxs-lookup"><span data-stu-id="af939-128">TopoEdit Menus</span></span>](topoedit-menus.md)
</dt> <dt>

[<span data-ttu-id="af939-129">Barre d’outils TopoEdit</span><span class="sxs-lookup"><span data-stu-id="af939-129">TopoEdit Toolbar</span></span>](topoedit-toolbar.md)
</dt> <dt>

[<span data-ttu-id="af939-130">TopoEdit</span><span class="sxs-lookup"><span data-stu-id="af939-130">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



