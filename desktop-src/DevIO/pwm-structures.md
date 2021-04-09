---
description: En savoir plus sur les structures PWM
ms.assetid: 992E3913-C1C4-48C1-A550-475CF44AB065
title: Structures PWM
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99511820f8500cd8df827a80664f6c274d732665
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950580"
---
# <a name="pwm-structures"></a><span data-ttu-id="d4828-103">Structures PWM</span><span class="sxs-lookup"><span data-stu-id="d4828-103">PWM Structures</span></span>

<span data-ttu-id="d4828-104">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="d4828-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="d4828-105">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="d4828-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="d4828-106">Les structures suivantes sont utilisées avec la modulation de largeur d’impulsion :</span><span class="sxs-lookup"><span data-stu-id="d4828-106">The following structures are used with Pulse Width Modulation:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="d4828-107">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="d4828-107">In this section</span></span>



| <span data-ttu-id="d4828-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="d4828-108">Topic</span></span>                                                                                                                        | <span data-ttu-id="d4828-109">Description</span><span class="sxs-lookup"><span data-stu-id="d4828-109">Description</span></span>                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4828-110">**\_sortie de \_ la \_ période réelle d’extraction du contrôleur \_ PWM \_**</span><span class="sxs-lookup"><span data-stu-id="d4828-110">**PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD\_OUTPUT**</span></span>](pwm-controller-get-actual-period-output.md)<br/>                   | <span data-ttu-id="d4828-111">Contient la période de signal de sortie effective pour un contrôleur de modulation d’impulsions (PWM).</span><span class="sxs-lookup"><span data-stu-id="d4828-111">Contains the effective output signal period for a Pulse Width Modulation (PWM) controller.</span></span><br/>                    |
| [<span data-ttu-id="d4828-112">**\_informations sur le contrôleur PWM \_**</span><span class="sxs-lookup"><span data-stu-id="d4828-112">**PWM\_CONTROLLER\_INFO**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_info)<br/>                                                              | <span data-ttu-id="d4828-113">Représente les informations statiques qui caractérisent un contrôleur de modulation d’impulsions en largeur (PWM).</span><span class="sxs-lookup"><span data-stu-id="d4828-113">Represents the static information that characterizes a Pulse Width Modulation (PWM) controller.</span></span> <br/>              |
| [<span data-ttu-id="d4828-114">**\_entrée de \_ la \_ \_ période souhaitée \_ de l’ensemble de contrôleurs PWM**</span><span class="sxs-lookup"><span data-stu-id="d4828-114">**PWM\_CONTROLLER\_SET\_DESIRED\_PERIOD\_INPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_set_desired_period_input)<br/>                   | <span data-ttu-id="d4828-115">Contient une valeur d’entrée pour une période de signal suggérée pour le contrôleur de modulation d’impulsions (PWM).</span><span class="sxs-lookup"><span data-stu-id="d4828-115">Contains an input value for a suggested signal period for the Pulse Width Modulation (PWM) controller.</span></span> <br/>       |
| [<span data-ttu-id="d4828-116">**\_sortie de \_ la \_ \_ période souhaitée \_ de l’ensemble de contrôleurs PWM**</span><span class="sxs-lookup"><span data-stu-id="d4828-116">**PWM\_CONTROLLER\_SET\_DESIRED\_PERIOD\_OUTPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_controller_set_desired_period_output)<br/>                 | <span data-ttu-id="d4828-117">Contient la période de signal de sortie effective du contrôleur de modulation d’impulsions (PWM).</span><span class="sxs-lookup"><span data-stu-id="d4828-117">Contains the effective output signal period of the Pulse Width Modulation (PWM) controller.</span></span><br/>                   |
| [<span data-ttu-id="d4828-118">**\_sortie de \_ pourcentage du \_ cycle de \_ \_ vie \_ \_ de l’affichage des codes confidentiels**</span><span class="sxs-lookup"><span data-stu-id="d4828-118">**PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_OUTPUT**</span></span>](pwm-pin-get-active-duty-cycle-percentage-output.md)<br/> | <span data-ttu-id="d4828-119">Contient le pourcentage de cycle de responsabilité actuel d’un pin ou d’un canal dans un contrôleur de modulation d’impulsions (PWM).</span><span class="sxs-lookup"><span data-stu-id="d4828-119">Contains the current duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span><br/> |
| [<span data-ttu-id="d4828-120">**\_entrée de \_ pourcentage du \_ cycle de \_ \_ vie actif \_ \_ du pin PWM**</span><span class="sxs-lookup"><span data-stu-id="d4828-120">**PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE\_INPUT**</span></span>](pwm-pin-set-active-duty-cycle-percentage-input.md)<br/>   | <span data-ttu-id="d4828-121">Contient un pourcentage de cycle de responsabilité souhaité pour un pin ou un canal dans un contrôleur de modulation d’impulsions en largeur (PWM).</span><span class="sxs-lookup"><span data-stu-id="d4828-121">Contains a desired duty cycle percentage for a pin or channel in a Pulse Width Modulation (PWM) controller.</span></span><br/>   |
| [<span data-ttu-id="d4828-122">**\_sortie de \_ \_ polarité du code confidentiel PWM \_**</span><span class="sxs-lookup"><span data-stu-id="d4828-122">**PWM\_PIN\_GET\_POLARITY\_OUTPUT**</span></span>](pwm-pin-get-polarity-output.md)<br/>                                            | <span data-ttu-id="d4828-123">Contient une valeur de polarité à retourner.</span><span class="sxs-lookup"><span data-stu-id="d4828-123">Contains a polarity value to return.</span></span><br/>                                                                          |
| [<span data-ttu-id="d4828-124">**\_entrée de \_ polarité du jeu de codes CONFIDENTIELs PWM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4828-124">**PWM\_PIN\_SET\_POLARITY\_INPUT**</span></span>](/windows/desktop/api/Pwm/ns-pwm-pwm_pin_set_polarity_input)<br/>                                              | <span data-ttu-id="d4828-125">Contient la valeur souhaitée pour la polarité d’un code confidentiel ou d’un canal.</span><span class="sxs-lookup"><span data-stu-id="d4828-125">Contains a desired value for polarity of a pin or channel.</span></span><br/>                                                    |
| [<span data-ttu-id="d4828-126">**la \_ sortie du code confidentiel PWM \_ est \_ démarrée \_**</span><span class="sxs-lookup"><span data-stu-id="d4828-126">**PWM\_PIN\_IS\_STARTED\_OUTPUT**</span></span>](pwm-pin-is-started-output.md)<br/>                                                | <span data-ttu-id="d4828-127">Contient l’état actuel de génération de signal d’un code confidentiel.</span><span class="sxs-lookup"><span data-stu-id="d4828-127">Contains the current signal generation state of a pin.</span></span><br/>                                                        |



 

 

 




