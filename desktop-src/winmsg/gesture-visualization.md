---
description: Les constantes suivantes sont utilisées par les applications ou les infrastructures d’interface utilisateur pour identifier comment les commentaires de l’interface utilisateur sont traités lorsque l’un des mouvements répertoriés est détecté.
ms.assetid: 76D3DFF4-7BB2-49A9-8251-0B5D9376B649
title: Visualisation des mouvements (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 551934380e1d5ec0902818466f5840e1dc6718e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538935"
---
# <a name="gesture-visualization"></a><span data-ttu-id="c37f8-103">Visualisation de mouvement</span><span class="sxs-lookup"><span data-stu-id="c37f8-103">Gesture Visualization</span></span>

<span data-ttu-id="c37f8-104">Les constantes suivantes sont utilisées par les applications ou les infrastructures d’interface utilisateur pour identifier comment les commentaires de l’interface utilisateur sont traités lorsque l’un des mouvements répertoriés est détecté.</span><span class="sxs-lookup"><span data-stu-id="c37f8-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when one of the listed gestures is detected.</span></span>

<span data-ttu-id="c37f8-105">Ces constantes sont utilisées avec les paramètres **SPI \_ GETGESTUREVISUALIZATION** et **SPI \_ SETGESTUREVISUALIZATION** et la fonction [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="c37f8-105">These constants are used with the **SPI\_GETGESTUREVISUALIZATION** and **SPI\_SETGESTUREVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<span data-ttu-id="c37f8-106">**Remarque**</span><span class="sxs-lookup"><span data-stu-id="c37f8-106">**Note**</span></span>  

<span data-ttu-id="c37f8-107">Pour récupérer ou définir des informations de visualisation du stylet, nous vous recommandons d’utiliser les paramètres **SPI \_ GETPENVISUALIZATION** et **SPI \_ SETPENVISUALIZATION** , ainsi que les constantes répertoriées dans la [**visualisation du stylet**](pen-visualization.md).</span><span class="sxs-lookup"><span data-stu-id="c37f8-107">For retrieving or setting pen visualization info, we recommend that you use the **SPI\_GETPENVISUALIZATION** and **SPI\_SETPENVISUALIZATION** parameters and the constants listed in [**Pen Visualization**](pen-visualization.md).</span></span>

<dl> <dt>

<span data-ttu-id="c37f8-108"><span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION \_ désactivé**</span><span class="sxs-lookup"><span data-stu-id="c37f8-108"><span id="GESTUREVISUALIZATION_OFF"></span><span id="gesturevisualization_off"></span>**GESTUREVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c37f8-109">0x0000</span><span class="sxs-lookup"><span data-stu-id="c37f8-109">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="c37f8-110">Spécifie que les commentaires de l’interface utilisateur pour tous les mouvements sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="c37f8-110">Specifies that UI feedback for all gestures is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c37f8-111"><span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION \_ sur**</span><span class="sxs-lookup"><span data-stu-id="c37f8-111"><span id="GESTUREVISUALIZATION_ON"></span><span id="gesturevisualization_on"></span>**GESTUREVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c37f8-112">0x001F</span><span class="sxs-lookup"><span data-stu-id="c37f8-112">0x001F</span></span>
</dt> <dt>



<span data-ttu-id="c37f8-113">Spécifie que les commentaires de l’interface utilisateur pour tous les mouvements sont activés.</span><span class="sxs-lookup"><span data-stu-id="c37f8-113">Specifies that UI feedback for all gestures is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c37f8-114"><span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**GESTUREVISUALIZATION \_ Tap**</span><span class="sxs-lookup"><span data-stu-id="c37f8-114"><span id="GESTUREVISUALIZATION_TAP"></span><span id="gesturevisualization_tap"></span>**GESTUREVISUALIZATION\_TAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c37f8-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="c37f8-115">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="c37f8-116">Spécifie les commentaires de l’interface utilisateur pour un TAP.</span><span class="sxs-lookup"><span data-stu-id="c37f8-116">Specifies UI feedback for a tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c37f8-117"><span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**GESTUREVISUALIZATION \_ DOUBLETAP**</span><span class="sxs-lookup"><span data-stu-id="c37f8-117"><span id="GESTUREVISUALIZATION_DOUBLETAP"></span><span id="gesturevisualization_doubletap"></span>**GESTUREVISUALIZATION\_DOUBLETAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c37f8-118">0x0002</span><span class="sxs-lookup"><span data-stu-id="c37f8-118">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="c37f8-119">Spécifie les commentaires de l’interface utilisateur pour un double-clic.</span><span class="sxs-lookup"><span data-stu-id="c37f8-119">Specifies UI feedback for a double tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c37f8-120"><span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**GESTUREVISUALIZATION \_ PRESSANDTAP**</span><span class="sxs-lookup"><span data-stu-id="c37f8-120"><span id="GESTUREVISUALIZATION_PRESSANDTAP"></span><span id="gesturevisualization_pressandtap"></span>**GESTUREVISUALIZATION\_PRESSANDTAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c37f8-121">0x0004</span><span class="sxs-lookup"><span data-stu-id="c37f8-121">0x0004</span></span>
</dt> <dt>



<span data-ttu-id="c37f8-122">Spécifie les commentaires de l’interface utilisateur pour une pression et un TAP.</span><span class="sxs-lookup"><span data-stu-id="c37f8-122">Specifies UI feedback for a press and tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c37f8-123"><span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**GESTUREVISUALIZATION \_ PRESSANDHOLD**</span><span class="sxs-lookup"><span data-stu-id="c37f8-123"><span id="GESTUREVISUALIZATION_PRESSANDHOLD"></span><span id="gesturevisualization_pressandhold"></span>**GESTUREVISUALIZATION\_PRESSANDHOLD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c37f8-124">0x0008</span><span class="sxs-lookup"><span data-stu-id="c37f8-124">0x0008</span></span>
</dt> <dt>



<span data-ttu-id="c37f8-125">Spécifie les commentaires de l’interface utilisateur pour une pression et un blocage.</span><span class="sxs-lookup"><span data-stu-id="c37f8-125">Specifies UI feedback for a press and hold.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c37f8-126"><span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**GESTUREVISUALIZATION \_ RIGHTTAP**</span><span class="sxs-lookup"><span data-stu-id="c37f8-126"><span id="GESTUREVISUALIZATION_RIGHTTAP"></span><span id="gesturevisualization_righttap"></span>**GESTUREVISUALIZATION\_RIGHTTAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c37f8-127">0x0010</span><span class="sxs-lookup"><span data-stu-id="c37f8-127">0x0010</span></span>
</dt> <dt>



<span data-ttu-id="c37f8-128">Spécifie les commentaires de l’interface utilisateur pour un TAP droit.</span><span class="sxs-lookup"><span data-stu-id="c37f8-128">Specifies UI feedback for a right tap.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c37f8-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c37f8-129">Requirements</span></span>



| <span data-ttu-id="c37f8-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c37f8-130">Requirement</span></span> | <span data-ttu-id="c37f8-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="c37f8-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c37f8-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c37f8-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c37f8-133">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c37f8-133">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c37f8-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c37f8-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c37f8-135">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c37f8-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c37f8-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="c37f8-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c37f8-137"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="c37f8-137"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c37f8-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c37f8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c37f8-139">Constantes de configuration</span><span class="sxs-lookup"><span data-stu-id="c37f8-139">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="c37f8-140">**Visualisation des contacts**</span><span class="sxs-lookup"><span data-stu-id="c37f8-140">**Contact Visualization**</span></span>](contact-visualization.md)
</dt> <dt>

[<span data-ttu-id="c37f8-141">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="c37f8-141">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="c37f8-142">Configuration des commentaires en entrée</span><span class="sxs-lookup"><span data-stu-id="c37f8-142">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

