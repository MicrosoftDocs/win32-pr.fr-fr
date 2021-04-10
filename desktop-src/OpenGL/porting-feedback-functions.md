---
title: Portage des fonctions de commentaires
description: Avec IRIS GL, la façon dont les commentaires sont traités diffère selon l’ordinateur exécutant IRIS GL.
ms.assetid: 170a3eae-5e0e-47f5-80dc-f8db5af98f76
keywords:
- Portage de l’IRIS dans le GL, commentaires
- Portage à partir de IRIS GL, Feedback
- portage vers OpenGL à partir de IRIS GL, Feedback
- Portage OpenGL depuis IRIS GL, Feedback
- feedback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a04bcfe2c1d914a178ad7ad0dca95fb85d86bbc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197167"
---
# <a name="porting-feedback-functions"></a><span data-ttu-id="c4f5e-108">Portage des fonctions de commentaires</span><span class="sxs-lookup"><span data-stu-id="c4f5e-108">Porting Feedback Functions</span></span>

<span data-ttu-id="c4f5e-109">Avec IRIS GL, la façon dont les commentaires sont traités diffère selon l’ordinateur exécutant IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="c4f5e-109">With IRIS GL, the way that feedback is handled differs depending on the computer running IRIS GL.</span></span> <span data-ttu-id="c4f5e-110">OpenGL normalise les fonctions de commentaires pour vous permettre de vous reposer sur des commentaires cohérents entre différentes plateformes matérielles.</span><span class="sxs-lookup"><span data-stu-id="c4f5e-110">OpenGL standardizes feedback functions so you can rely on consistent feedback among various hardware platforms.</span></span> <span data-ttu-id="c4f5e-111">Le tableau suivant répertorie les fonctions d’évaluation du GL de l’IRIS et leurs fonctions OpenGL équivalentes.</span><span class="sxs-lookup"><span data-stu-id="c4f5e-111">The following table lists the IRIS GL feedback functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="c4f5e-112">Fonction IRIS GL</span><span class="sxs-lookup"><span data-stu-id="c4f5e-112">IRIS GL function</span></span> | <span data-ttu-id="c4f5e-113">Fonction OpenGL</span><span class="sxs-lookup"><span data-stu-id="c4f5e-113">OpenGL function</span></span>                                                                                            | <span data-ttu-id="c4f5e-114">Signification</span><span class="sxs-lookup"><span data-stu-id="c4f5e-114">Meaning</span></span>                                       |
|------------------|------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="c4f5e-115">**Commentaires**</span><span class="sxs-lookup"><span data-stu-id="c4f5e-115">**feedback**</span></span>     | <span data-ttu-id="c4f5e-116">[**glRenderMode**](glrendermode.md) (commentaires sur le GL \_ )</span><span class="sxs-lookup"><span data-stu-id="c4f5e-116">[**glRenderMode**](glrendermode.md) ( GL\_FEEDBACK )</span></span>                                                      | <span data-ttu-id="c4f5e-117">Bascule en mode commentaires.</span><span class="sxs-lookup"><span data-stu-id="c4f5e-117">Switches to feedback mode.</span></span>                    |
| <span data-ttu-id="c4f5e-118">**endfeedback**</span><span class="sxs-lookup"><span data-stu-id="c4f5e-118">**endfeedback**</span></span>  | <span data-ttu-id="c4f5e-119">[**glRenderMode**](glrendermode.md) ( \_ rendu GL)[**glFeedbackBuffer**](glfeedbackbuffer.md)</span><span class="sxs-lookup"><span data-stu-id="c4f5e-119">[**glRenderMode**](glrendermode.md) ( GL\_RENDER )[**glFeedbackBuffer**](glfeedbackbuffer.md)</span></span><br/> | <span data-ttu-id="c4f5e-120">Bascule en mode de rendu.</span><span class="sxs-lookup"><span data-stu-id="c4f5e-120">Switches to rendering mode.</span></span>                   |
| <span data-ttu-id="c4f5e-121">**passage**</span><span class="sxs-lookup"><span data-stu-id="c4f5e-121">**passthrough**</span></span>  | [<span data-ttu-id="c4f5e-122">**glPassThrough**</span><span class="sxs-lookup"><span data-stu-id="c4f5e-122">**glPassThrough**</span></span>](glpassthrough.md)                                                                     | <span data-ttu-id="c4f5e-123">Place un marqueur de jeton dans la mémoire tampon de commentaires.</span><span class="sxs-lookup"><span data-stu-id="c4f5e-123">Places a token marker in the feedback buffer.</span></span> |



 

 

 





