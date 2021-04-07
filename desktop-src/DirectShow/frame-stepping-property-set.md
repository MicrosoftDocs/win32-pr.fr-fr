---
description: Jeu de propriétés du pas à pas de frame
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Jeu de propriétés du pas à pas de frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f503a38a2f548e0df0a6e88b3ae7afaebdd8cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746637"
---
# <a name="frame-stepping-property-set"></a><span data-ttu-id="c2be9-103">Jeu de propriétés du pas à pas de frame</span><span class="sxs-lookup"><span data-stu-id="c2be9-103">Frame Stepping Property Set</span></span>

<span data-ttu-id="c2be9-104">Les décodeurs qui implémentent une recherche de précision des frames sous Microsoft DirectShow doivent implémenter le \_ \_ jeu de propriétés FrameStep am KSPROPSETID, qui est utilisé conjointement avec l’interface [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) .</span><span class="sxs-lookup"><span data-stu-id="c2be9-104">Decoders that implement frame-accurate seeking under Microsoft DirectShow must implement the AM\_KSPROPSETID\_FrameStep property set, which is used in conjunction with the [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface.</span></span>



|                   |                            |
|-------------------|----------------------------|
| <span data-ttu-id="c2be9-105">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="c2be9-105">Property Set GUID</span></span> | <span data-ttu-id="c2be9-106">AM \_ KSPROPSETID \_ FrameStep</span><span class="sxs-lookup"><span data-stu-id="c2be9-106">AM\_KSPROPSETID\_FrameStep</span></span> |



 



| <span data-ttu-id="c2be9-107">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="c2be9-107">Property ID</span></span>                              | <span data-ttu-id="c2be9-108">Description</span><span class="sxs-lookup"><span data-stu-id="c2be9-108">Description</span></span>                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2be9-109">\_FRAMESTEP, propriété, \_ \_ étape</span><span class="sxs-lookup"><span data-stu-id="c2be9-109">AM\_PROPERTY\_FRAMESTEP\_STEP</span></span>            | <span data-ttu-id="c2be9-110">Indique au décodeur de commencer une opération d’étape et passe une [**structure \_ \_ FRAMESTEP de propriété am**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) qui spécifie le nombre d’étapes.</span><span class="sxs-lookup"><span data-stu-id="c2be9-110">Instructs the decoder to begin a step operation and passes an [**AM\_PROPERTY\_FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) structure that specifies the number of steps.</span></span>            |
| <span data-ttu-id="c2be9-111">AM, \_ propriété \_ FRAMESTEP \_ Annuler</span><span class="sxs-lookup"><span data-stu-id="c2be9-111">AM\_PROPERTY\_FRAMESTEP\_CANCEL</span></span>          | <span data-ttu-id="c2be9-112">Indique au décodeur d’annuler l’opération d’étape en cours.</span><span class="sxs-lookup"><span data-stu-id="c2be9-112">Instructs the decoder to cancel the current step operation.</span></span> <span data-ttu-id="c2be9-113">Aucune donnée d’instance n’est associée à cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c2be9-113">No instance data is associated with this property.</span></span>                                                                  |
| <span data-ttu-id="c2be9-114">AM, \_ propriété \_ FRAMESTEP \_ CANSTEP</span><span class="sxs-lookup"><span data-stu-id="c2be9-114">AM\_PROPERTY\_FRAMESTEP\_CANSTEP</span></span>         | <span data-ttu-id="c2be9-115">Le décodeur retourne S \_ OK sur cette instruction pour indiquer qu’il peut effectuer l’exécution pas à pas, ou \_ false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c2be9-115">The decoder returns S\_OK on this instruction to indicate that it can perform frame stepping, S\_FALSE otherwise.</span></span> <span data-ttu-id="c2be9-116">Aucune donnée d’instance n’est passée lorsque cette propriété est définie.</span><span class="sxs-lookup"><span data-stu-id="c2be9-116">No instance data is passed when this property is set.</span></span>         |
| <span data-ttu-id="c2be9-117">AM, \_ propriété \_ FRAMESTEP \_ CANSTEPMULTIPLE</span><span class="sxs-lookup"><span data-stu-id="c2be9-117">AM\_PROPERTY\_FRAMESTEP\_CANSTEPMULTIPLE</span></span> | <span data-ttu-id="c2be9-118">Le décodeur retourne S \_ OK sur cette instruction pour indiquer qu’il peut exécuter pas à pas plusieurs frames à la fois, ou \_ false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c2be9-118">The decoder returns S\_OK on this instruction to indicate that it can step multiple frames at a time, S\_FALSE otherwise.</span></span> <span data-ttu-id="c2be9-119">Aucune donnée d’instance n’est passée lorsque cette propriété est définie.</span><span class="sxs-lookup"><span data-stu-id="c2be9-119">No instance data is passed when this property is set.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="c2be9-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c2be9-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2be9-121">Jeux de propriétés</span><span class="sxs-lookup"><span data-stu-id="c2be9-121">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



