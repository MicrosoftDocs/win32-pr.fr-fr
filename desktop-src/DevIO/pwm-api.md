---
description: La modulation d’impulsions en largeur (PWM) est la technique de la génération d’une onde d’impulsion rectangulaire qui a une largeur d’impulsion modulée pour produire la variation de la valeur moyenne de la forme d’onde.
ms.assetid: 16B1E46F-2C42-4D94-949E-BE8F53EB1E1E
title: API PWM
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 10b1951d9d96f49a9df9a51604767dbce360f9e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523644"
---
# <a name="pwm-api"></a><span data-ttu-id="aedfd-103">API PWM</span><span class="sxs-lookup"><span data-stu-id="aedfd-103">PWM API</span></span>

<span data-ttu-id="aedfd-104">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="aedfd-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="aedfd-105">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="aedfd-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="aedfd-106">La modulation d’impulsions en largeur (PWM) est la technique de la génération d’une onde d’impulsion rectangulaire qui a une largeur d’impulsion modulée pour produire la variation de la valeur moyenne de la forme d’onde.</span><span class="sxs-lookup"><span data-stu-id="aedfd-106">Pulse Width Modulation (PWM) is the technique of generating a rectangular pulse wave that has a pulse width that is modulated to result in the variation of the average value of the waveform.</span></span> <span data-ttu-id="aedfd-107">Les utilisations les plus courantes incluent les moteurs d’asservissement, les voyants de gradation ou d’autres fonctions associées.</span><span class="sxs-lookup"><span data-stu-id="aedfd-107">Most common uses include driving servo motors, dimming LEDs, or other related functions.</span></span> <span data-ttu-id="aedfd-108">Le PWM est destiné à être principalement utilisé pour les scénarios de Internet des objets.</span><span class="sxs-lookup"><span data-stu-id="aedfd-108">PWM is intended to be used primarily for Internet of Things scenarios.</span></span>

## <a name="about-pulse-width-modulation"></a><span data-ttu-id="aedfd-109">À propos de la modulation par impulsions de largeur</span><span class="sxs-lookup"><span data-stu-id="aedfd-109">About Pulse Width Modulation</span></span>

<span data-ttu-id="aedfd-110">Une forme d’onde PWM peut être catégorisée par deux paramètres :</span><span class="sxs-lookup"><span data-stu-id="aedfd-110">A PWM waveform can be categorized by two parameters:</span></span>

-   <span data-ttu-id="aedfd-111">Une période de forme d’onde (T)</span><span class="sxs-lookup"><span data-stu-id="aedfd-111">A waveform period (T)</span></span>

-   <span data-ttu-id="aedfd-112">Le cycle de l’utilisation, où la fréquence de la forme d’onde (f) est la réciproque de la période f = 1/T</span><span class="sxs-lookup"><span data-stu-id="aedfd-112">The duty cycle, where the waveform frequency (f) is the reciprocal of the period f=1/T</span></span>

<span data-ttu-id="aedfd-113">Le cycle de responsabilité décrit la proportion de **la durée d'** / **activité** par rapport à l’intervalle régulier ou à la **période** de temps.</span><span class="sxs-lookup"><span data-stu-id="aedfd-113">The duty cycle describes the proportion of the **on**/**Active** time with respect to the regular interval or **Period** of time.</span></span> <span data-ttu-id="aedfd-114">Un cycle d’utilisation faible correspond à une puissance moyenne de sortie basse, car l’alimentation est désactivée pour la plupart du temps.</span><span class="sxs-lookup"><span data-stu-id="aedfd-114">A low duty cycle corresponds to an average of low output power, because the power is off for most of the time.</span></span> <span data-ttu-id="aedfd-115">Le cycle de l’utilisation est exprimé sous la forme d’un pourcentage.</span><span class="sxs-lookup"><span data-stu-id="aedfd-115">Duty cycle is expressed as a percentage.</span></span> <span data-ttu-id="aedfd-116">Entièrement sur 100%.</span><span class="sxs-lookup"><span data-stu-id="aedfd-116">Fully on is 100%.</span></span> <span data-ttu-id="aedfd-117">La valeur OFF est égale à 0%.</span><span class="sxs-lookup"><span data-stu-id="aedfd-117">Fully off is 0%.</span></span> <span data-ttu-id="aedfd-118">La moitié **active** est de 50%.</span><span class="sxs-lookup"><span data-stu-id="aedfd-118">**Active** half the time is 50%.</span></span>

<span data-ttu-id="aedfd-119">Les développeurs qui cherchent à implémenter le PWM dans leurs applications IoT doivent examiner la [documentation du PWM WinRT.](/uwp/api/windows.devices.pwm)</span><span class="sxs-lookup"><span data-stu-id="aedfd-119">Developers looking to implement PWM in their IoT applications should investigate the [WinRT PWM documentation.](/uwp/api/windows.devices.pwm)</span></span>

## <a name="pulse-width-modulation-types"></a><span data-ttu-id="aedfd-120">Types de modulation d’impulsions en largeur</span><span class="sxs-lookup"><span data-stu-id="aedfd-120">Pulse Width Modulation types</span></span>

<span data-ttu-id="aedfd-121">PWM utilise ces codes, [structures](pwm-structures.md)et [énumérations](pwm-enumeration-types.md) de [contrôle d’e/s](pwm-control-codes.md).</span><span class="sxs-lookup"><span data-stu-id="aedfd-121">PWM uses [these IO control codes](pwm-control-codes.md), [structures](pwm-structures.md), and [enumerations.](pwm-enumeration-types.md)</span></span>

<span data-ttu-id="aedfd-122">Le PWM utilise également la fonction suivante : [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).</span><span class="sxs-lookup"><span data-stu-id="aedfd-122">PWM also uses the following function: [**PwmParsePinPath**](/windows-hardware/drivers/ddi/content/pwmutil/nf-pwmutil-pwmparsepinpath).</span></span>

 

 
