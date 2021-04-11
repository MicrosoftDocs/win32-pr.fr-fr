---
description: Les constantes suivantes sont utilisées par les applications ou les infrastructures d’interface utilisateur pour identifier comment les commentaires de l’interface utilisateur sont traités lorsqu’un contact d’entrée est détecté.
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: Visualisation des contacts (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100892624f3e656e33ddf798c5795eeab6b11a17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320253"
---
# <a name="contact-visualization"></a><span data-ttu-id="54330-103">Visualisation des contacts</span><span class="sxs-lookup"><span data-stu-id="54330-103">Contact Visualization</span></span>

<span data-ttu-id="54330-104">Les constantes suivantes sont utilisées par les applications ou les infrastructures d’interface utilisateur pour identifier comment les commentaires de l’interface utilisateur sont traités lorsqu’un contact d’entrée est détecté.</span><span class="sxs-lookup"><span data-stu-id="54330-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when an input contact is detected.</span></span>

<span data-ttu-id="54330-105">Ces constantes sont utilisées avec les paramètres **SPI \_ GETCONTACTVISUALIZATION** et **SPI \_ SETCONTACTVISUALIZATION** et la fonction [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="54330-105">These constants are used with the **SPI\_GETCONTACTVISUALIZATION** and **SPI\_SETCONTACTVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<dl> <dt>

<span data-ttu-id="54330-106"><span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION \_ désactivé**</span><span class="sxs-lookup"><span data-stu-id="54330-106"><span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54330-107">0x0000</span><span class="sxs-lookup"><span data-stu-id="54330-107">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="54330-108">Spécifie que les commentaires de l’interface utilisateur pour tous les contacts sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="54330-108">Specifies UI feedback for all contacts is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54330-109"><span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION \_ sur**</span><span class="sxs-lookup"><span data-stu-id="54330-109"><span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54330-110">0x0001</span><span class="sxs-lookup"><span data-stu-id="54330-110">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="54330-111">Spécifie les commentaires de l’interface utilisateur pour tous les contacts.</span><span class="sxs-lookup"><span data-stu-id="54330-111">Specifies UI feedback for all contacts is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54330-112"><span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**CONTACTVISUALIZATION \_ mode**</span><span class="sxs-lookup"><span data-stu-id="54330-112"><span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**CONTACTVISUALIZATION\_PRESENTATIONMODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54330-113">0x0002</span><span class="sxs-lookup"><span data-stu-id="54330-113">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="54330-114">Spécifie les commentaires de l’interface utilisateur pour tous les contacts sur les visuels en mode présentation.</span><span class="sxs-lookup"><span data-stu-id="54330-114">Specifies UI feedback for all contacts is on with presentation mode visuals.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54330-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54330-115">Requirements</span></span>



| <span data-ttu-id="54330-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54330-116">Requirement</span></span> | <span data-ttu-id="54330-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="54330-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="54330-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54330-118">Minimum supported client</span></span><br/> | <span data-ttu-id="54330-119">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54330-119">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="54330-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54330-120">Minimum supported server</span></span><br/> | <span data-ttu-id="54330-121">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54330-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="54330-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="54330-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="54330-123"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="54330-123"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54330-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54330-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54330-125">Constantes de configuration</span><span class="sxs-lookup"><span data-stu-id="54330-125">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="54330-126">**Visualisation de mouvement**</span><span class="sxs-lookup"><span data-stu-id="54330-126">**Gesture Visualization**</span></span>](gesture-visualization.md)
</dt> <dt>

[<span data-ttu-id="54330-127">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="54330-127">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="54330-128">Configuration des commentaires en entrée</span><span class="sxs-lookup"><span data-stu-id="54330-128">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

