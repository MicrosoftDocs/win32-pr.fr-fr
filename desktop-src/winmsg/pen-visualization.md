---
description: Les constantes suivantes sont utilisées par les applications ou les infrastructures d’interface utilisateur pour identifier comment les commentaires de l’interface utilisateur sont traités lorsque l’un des mouvements de stylet répertoriés est détecté.
ms.assetid: 434DC272-DC1C-4091-BB38-DDCB1A635D8D
title: Visualisation du stylet (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a09aa8892647315eccbb1e8b3ca443e01c1ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529163"
---
# <a name="pen-visualization"></a><span data-ttu-id="97e61-103">Visualisation du stylet</span><span class="sxs-lookup"><span data-stu-id="97e61-103">Pen Visualization</span></span>

<span data-ttu-id="97e61-104">Les constantes suivantes sont utilisées par les applications ou les infrastructures d’interface utilisateur pour identifier comment les commentaires de l’interface utilisateur sont traités lorsque l’un des mouvements de stylet répertoriés est détecté.</span><span class="sxs-lookup"><span data-stu-id="97e61-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when one of the listed pen gestures is detected.</span></span>

<span data-ttu-id="97e61-105">Ces constantes sont utilisées avec les paramètres **SPI \_ GETPENVISUALIZATION** et **SPI \_ SETPENVISUALIZATION** et la fonction [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="97e61-105">These constants are used with the **SPI\_GETPENVISUALIZATION** and **SPI\_SETPENVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<dl> <dt>

<span data-ttu-id="97e61-106"><span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZATION \_ désactivé**</span><span class="sxs-lookup"><span data-stu-id="97e61-106"><span id="PENVISUALIZATION_OFF"></span><span id="penvisualization_off"></span>**PENVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97e61-107">0x0000</span><span class="sxs-lookup"><span data-stu-id="97e61-107">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="97e61-108">Spécifie que les commentaires de l’interface utilisateur pour tous les mouvements de stylet sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="97e61-108">Specifies that UI feedback for all pen gestures is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97e61-109"><span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION \_ sur**</span><span class="sxs-lookup"><span data-stu-id="97e61-109"><span id="PENVISUALIZATION_ON"></span><span id="penvisualization_on"></span>**PENVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97e61-110">0x0023</span><span class="sxs-lookup"><span data-stu-id="97e61-110">0x0023</span></span>
</dt> <dt>



<span data-ttu-id="97e61-111">Spécifie que les commentaires de l’interface utilisateur pour tous les mouvements de stylet sont activés.</span><span class="sxs-lookup"><span data-stu-id="97e61-111">Specifies that UI feedback for all pen gestures is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97e61-112"><span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**PENVISUALIZATION \_ Tap**</span><span class="sxs-lookup"><span data-stu-id="97e61-112"><span id="PENVISUALIZATION_TAP"></span><span id="penvisualization_tap"></span>**PENVISUALIZATION\_TAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97e61-113">0x0001</span><span class="sxs-lookup"><span data-stu-id="97e61-113">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="97e61-114">Spécifie les commentaires de l’interface utilisateur pour un robinet Pen.</span><span class="sxs-lookup"><span data-stu-id="97e61-114">Specifies UI feedback for a pen tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97e61-115"><span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**PENVISUALIZATION \_ DOUBLETAP**</span><span class="sxs-lookup"><span data-stu-id="97e61-115"><span id="PENVISUALIZATION_DOUBLETAP"></span><span id="penvisualization_doubletap"></span>**PENVISUALIZATION\_DOUBLETAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97e61-116">0x0002</span><span class="sxs-lookup"><span data-stu-id="97e61-116">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="97e61-117">Spécifie les commentaires de l’interface utilisateur pour un double-appui sur le stylet.</span><span class="sxs-lookup"><span data-stu-id="97e61-117">Specifies UI feedback for a pen double tap.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97e61-118"><span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**\_curseur PENVISUALIZATION**</span><span class="sxs-lookup"><span data-stu-id="97e61-118"><span id="PENVISUALIZATION_CURSOR"></span><span id="penvisualization_cursor"></span>**PENVISUALIZATION\_CURSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97e61-119">0x0020</span><span class="sxs-lookup"><span data-stu-id="97e61-119">0x0020</span></span>
</dt> <dt>



<span data-ttu-id="97e61-120">Spécifie les commentaires de l’interface utilisateur pour le curseur de stylet.</span><span class="sxs-lookup"><span data-stu-id="97e61-120">Specifies UI feedback for the pen cursor.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97e61-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97e61-121">Requirements</span></span>



| <span data-ttu-id="97e61-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97e61-122">Requirement</span></span> | <span data-ttu-id="97e61-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="97e61-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="97e61-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97e61-124">Minimum supported client</span></span><br/> | <span data-ttu-id="97e61-125">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97e61-125">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="97e61-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97e61-126">Minimum supported server</span></span><br/> | <span data-ttu-id="97e61-127">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97e61-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="97e61-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="97e61-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="97e61-129"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="97e61-129"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97e61-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97e61-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97e61-131">Constantes de configuration</span><span class="sxs-lookup"><span data-stu-id="97e61-131">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="97e61-132">**Visualisation des contacts**</span><span class="sxs-lookup"><span data-stu-id="97e61-132">**Contact Visualization**</span></span>](contact-visualization.md)
</dt> <dt>

[<span data-ttu-id="97e61-133">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="97e61-133">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="97e61-134">Configuration des commentaires en entrée</span><span class="sxs-lookup"><span data-stu-id="97e61-134">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

