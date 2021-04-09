---
description: La surveillance des tons surveille le flux multimédia d’un appel pour des tonalités spécifiées.
ms.assetid: c3218013-b71f-41cd-9397-ba717c0cf556
title: Analyse des tons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a3275e5207999896792ee04dc1842b01f4ad0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034624"
---
# <a name="tone-monitoring"></a><span data-ttu-id="baf11-103">Analyse des tons</span><span class="sxs-lookup"><span data-stu-id="baf11-103">Tone Monitoring</span></span>

<span data-ttu-id="baf11-104">La surveillance des tons surveille le flux multimédia d’un appel pour des tonalités spécifiées.</span><span class="sxs-lookup"><span data-stu-id="baf11-104">Tone monitoring monitors the media stream of a call for specified tones.</span></span> <span data-ttu-id="baf11-105">Un ton est décrit par ses fréquences de composant et cadence.</span><span class="sxs-lookup"><span data-stu-id="baf11-105">A tone is described by its component frequencies and cadence.</span></span> <span data-ttu-id="baf11-106">Une implémentation de l’API peut permettre la surveillance simultanée de plusieurs tonalités différentes.</span><span class="sxs-lookup"><span data-stu-id="baf11-106">An implementation of the API may allow several different tones to be monitored simultaneously.</span></span> <span data-ttu-id="baf11-107">Une application peut étiqueter chaque nuance pour pouvoir distinguer les différentes tonalités pour lesquelles elle demande la détection.</span><span class="sxs-lookup"><span data-stu-id="baf11-107">An application can tag each tone to be able to distinguish the different tones for which it requests detection.</span></span>

<span data-ttu-id="baf11-108">Une application peut activer ou désactiver la surveillance des sons sur un appel spécifié avec [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones).</span><span class="sxs-lookup"><span data-stu-id="baf11-108">An application can enable or disable tone monitoring on a specified call with [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones).</span></span> <span data-ttu-id="baf11-109">Avec cette fonction, l’application indique les tonalités à détecter sur un appel spécifié.</span><span class="sxs-lookup"><span data-stu-id="baf11-109">With this function, the application indicates which tones to detect on a specified call.</span></span> <span data-ttu-id="baf11-110">Lorsque la surveillance des tons est activée, les chiffres détectés entraînent la notification de l’application avec le message de [**ligne \_ MONITORTONE**](line-monitortone.md) .</span><span class="sxs-lookup"><span data-stu-id="baf11-110">When tone monitoring is enabled, detected digits cause the application to be notified with the [**LINE\_MONITORTONE**](line-monitortone.md) message.</span></span> <span data-ttu-id="baf11-111">Ce message fournit le descripteur d’appel sur lequel le ton a été détecté, ainsi que la balise de l’application pour le ton.</span><span class="sxs-lookup"><span data-stu-id="baf11-111">This message provides the call handle on which the tone was detected as well as the application's tag for the tone.</span></span>

<span data-ttu-id="baf11-112">L’étendue de la surveillance des tons est liée par la durée de vie de l’appel.</span><span class="sxs-lookup"><span data-stu-id="baf11-112">The scope of tone monitoring is bound by the lifetime of the call.</span></span> <span data-ttu-id="baf11-113">La surveillance des tons sur un appel se termine dès que l’appel se *déconnecte* ou devient *inactif*.</span><span class="sxs-lookup"><span data-stu-id="baf11-113">Tone monitoring on a call ends as soon the call *disconnects* or goes *idle*.</span></span>

> [!Note]  
> <span data-ttu-id="baf11-114">La surveillance des tonalités, des chiffres ou des types de média requiert souvent l’utilisation de ressources dont le fournisseur de services peut uniquement avoir une quantité finie.</span><span class="sxs-lookup"><span data-stu-id="baf11-114">The monitoring of tones, digits, or media types often requires the use of resources of which the service provider can only have a finite amount.</span></span> <span data-ttu-id="baf11-115">Une demande de surveillance peut être rejetée si les ressources ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="baf11-115">A request for monitoring can be rejected if resources are not available.</span></span> <span data-ttu-id="baf11-116">Pour la même raison, une application doit désactiver toute analyse inutile.</span><span class="sxs-lookup"><span data-stu-id="baf11-116">For the same reason, an application should disable any unnecessary monitoring.</span></span>

 

 

 



