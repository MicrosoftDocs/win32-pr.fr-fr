---
description: L’analyse des chiffres surveille l’appel de chiffres.
ms.assetid: 6ba28fdf-87d5-4d39-9e12-8201585a86ee
title: Analyse des chiffres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2454f6886bba4e859348df929c1a35f10c3d481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515424"
---
# <a name="digit-monitoring"></a><span data-ttu-id="32831-103">Analyse des chiffres</span><span class="sxs-lookup"><span data-stu-id="32831-103">Digit Monitoring</span></span>

<span data-ttu-id="32831-104">L’analyse des chiffres surveille l’appel de chiffres.</span><span class="sxs-lookup"><span data-stu-id="32831-104">Digit monitoring monitors the call for digits.</span></span> <span data-ttu-id="32831-105">L’interface TAPI permet aux chiffres d’être signalés selon deux méthodes (modes numériques) :</span><span class="sxs-lookup"><span data-stu-id="32831-105">TAPI allows digits to be signaled according to two methods (digit modes):</span></span>

-   <span data-ttu-id="32831-106">Les chiffres de l’impulsion sont signalés comme des séquences d’impulsions ou de rotation.</span><span class="sxs-lookup"><span data-stu-id="32831-106">Pulse Digits are signaled as pulse or rotary sequences.</span></span> <span data-ttu-id="32831-107">Pour la détection, ces impulsions se manifestent comme rien de plus que les séquences de clics audibles.</span><span class="sxs-lookup"><span data-stu-id="32831-107">For detection, these pulses manifest themselves as nothing more than sequences of audible clicks.</span></span> <span data-ttu-id="32831-108">Les chiffres de l’impulsion valides sont « 0 » à « 9 ».</span><span class="sxs-lookup"><span data-stu-id="32831-108">Valid pulse digits are '0' through '9'.</span></span>
-   <span data-ttu-id="32831-109">Les chiffres DTMF sont signalés comme des tonalités DTMF (fréquence multiple de tonalité double).</span><span class="sxs-lookup"><span data-stu-id="32831-109">DTMF Digits are signaled as DTMF (Dual Tone Multiple Frequency) tones.</span></span> <span data-ttu-id="32831-110">Les chiffres DTMF valides sont « 0 » à « 9 », « A ».</span><span class="sxs-lookup"><span data-stu-id="32831-110">Valid DTMF digits are '0' through '9', 'A'.</span></span> <span data-ttu-id="32831-111">'B', 'C', 'd', ' \* 'et' \# '.</span><span class="sxs-lookup"><span data-stu-id="32831-111">'B', 'C', 'D', '\*', and '\#'.</span></span> <span data-ttu-id="32831-112">Le bord de début et le bas des chiffres DTMF peuvent être surveillés.</span><span class="sxs-lookup"><span data-stu-id="32831-112">Both the beginning and the down edge of DTMF digits can be monitored.</span></span>

<span data-ttu-id="32831-113">Une application peut activer ou désactiver la surveillance des chiffres sur un appel spécifié avec [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits).</span><span class="sxs-lookup"><span data-stu-id="32831-113">An application can enable or disable digit monitoring on a specified call with [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits).</span></span> <span data-ttu-id="32831-114">Lorsque l’analyse des chiffres est activée, les chiffres détectés entraînent la notification de l’application avec le message de [**ligne \_ MONITORDIGITS**](line-monitordigits.md) .</span><span class="sxs-lookup"><span data-stu-id="32831-114">When digit monitoring is enabled, detected digits cause the application to be notified with the [**LINE\_MONITORDIGITS**](line-monitordigits.md) message.</span></span> <span data-ttu-id="32831-115">Ce message fournit le descripteur d’appel sur lequel le chiffre a été détecté, ainsi que la valeur de chiffre et le mode de chiffre.</span><span class="sxs-lookup"><span data-stu-id="32831-115">This message provides the call handle on which the digit was detected as well as the digit value and the digit mode.</span></span> <span data-ttu-id="32831-116">La portée de l’analyse des chiffres est liée par la durée de vie de l’appel.</span><span class="sxs-lookup"><span data-stu-id="32831-116">The scope of digit monitoring is bound by the lifetime of the call.</span></span> <span data-ttu-id="32831-117">La surveillance des chiffres sur un appel se termine dès que l’appel *se déconnecte* ou devient *inactif*.</span><span class="sxs-lookup"><span data-stu-id="32831-117">Digit monitoring on a call ends as soon as the call *disconnects* or goes *idle*.</span></span>

 

 



