---
description: Expérience de l’utilisation des canards par défaut
ms.assetid: 2ad9482f-1888-4f19-bc41-9d47a8e0ed15
title: Expérience de l’utilisation des canards par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d81aa22254ab33ee7396fd4a22d83cc7f5a58041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748532"
---
# <a name="default-ducking-experience"></a><span data-ttu-id="cdfec-103">Expérience de l’utilisation des canards par défaut</span><span class="sxs-lookup"><span data-stu-id="cdfec-103">Default Ducking Experience</span></span>

<span data-ttu-id="cdfec-104">Imaginez un scénario dans lequel un utilisateur reçoit un appel téléphonique tout en écoutant de la musique sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="cdfec-104">Consider a scenario where a user receives a phone call while listening to music on the computer.</span></span> <span data-ttu-id="cdfec-105">Pendant l’appel téléphonique, l’utilisateur souhaite réduire le volume de la musique tout en participant à l’appel téléphonique et reprendre le volume d’origine après la fin de l’appel téléphonique.</span><span class="sxs-lookup"><span data-stu-id="cdfec-105">During the phone call, the user wants to reduce the volume level of the music while attending to the phone call, and resume the original volume after the phone call has ended.</span></span> <span data-ttu-id="cdfec-106">En fonction des options spécifiées par l’utilisateur dans le panneau de configuration **sons** , le système d’exploitation fournit automatiquement cette *fonctionnalité via* l' *atténuation* ou l’atténuation du flux, en réduisant l’intensité d’un flux audio.</span><span class="sxs-lookup"><span data-stu-id="cdfec-106">Depending on the options specified by the user in the **Sounds** control panel, the operating system automatically provides this functionality through *ducking* or *stream attenuation*—reduction in the intensity of an audio stream.</span></span>

<span data-ttu-id="cdfec-107">L’expérience d’atténuation par défaut dépend des préférences de l’utilisateur, comme spécifié dans l’option **son** du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="cdfec-107">The default attenuation experience depends on the user's preference, as specified in the control panel's **Sound** option.</span></span> <span data-ttu-id="cdfec-108">Sous l’onglet **communications** , l’utilisateur peut choisir un niveau d’atténuation (la valeur par défaut est 80%), désactiver tous les flux de communication non-communication ou désactiver l’expérience d’atténuation de flux par défaut.</span><span class="sxs-lookup"><span data-stu-id="cdfec-108">On the **Communications** tab, the user can choose an attenuation level (default value is 80%), mute all non-communication streams, or disable the default stream attenuation experience.</span></span> <span data-ttu-id="cdfec-109">Le système permet d’ouvrir de nouveaux flux de non-communication (à l’exception des nouveaux sons système) pendant la session de communication, mais les nouveaux flux ne sont pas automatiquement atténués.</span><span class="sxs-lookup"><span data-stu-id="cdfec-109">The system allows new non-communication streams (except for new system sounds) to be opened during the communication session but the new streams are not automatically attenuated.</span></span> <span data-ttu-id="cdfec-110">Lorsque tous les flux de communication sont fermés, le système met fin à la session de communication et restaure le volume des flux qui ont été atténués au cours de la session de communication.</span><span class="sxs-lookup"><span data-stu-id="cdfec-110">When all of the communication streams are closed, the system ends the communication session and restores the volume of the streams that were attenuated during the communication session.</span></span>

<span data-ttu-id="cdfec-111">Pour indiquer visuellement l’atténuation du flux, le système modifie les paramètres du mélangeur de volume en fonction de la préférence de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cdfec-111">To indicate stream attenuation visually, the system changes the volume mixer settings depending on the user's preference.</span></span> <span data-ttu-id="cdfec-112">Par exemple, si l’utilisateur spécifie un niveau d’atténuation, le mélangeur de volume réduit le curseur, affiche le nouveau volume atténué et affiche le niveau de volume d’origine.</span><span class="sxs-lookup"><span data-stu-id="cdfec-112">For example, if the user specifies an attenuation level, the volume mixer lowers the slider, displays the new attenuated volume, and displays the original volume level.</span></span> <span data-ttu-id="cdfec-113">L’illustration suivante montre ce processus.</span><span class="sxs-lookup"><span data-stu-id="cdfec-113">The following image illustrates this process.</span></span>

![diagramme du comportement d’atténuation de flux par défaut fourni dans Windows 7](images/stream-aatenuation.jpg)

<span data-ttu-id="cdfec-115">Une application peut remplacer l’atténuation de flux et implémenter une expérience de canard personnalisée si elle sait à quel moment la session de communication démarre et se termine.</span><span class="sxs-lookup"><span data-stu-id="cdfec-115">An application can override stream attenuation and implement a custom ducking experience if it knows when the communication session starts and ends.</span></span> <span data-ttu-id="cdfec-116">Pour plus d’informations, consultez [la page fournir un comportement de canard personnalisé](providing-a-custom-ducking-experience.md).</span><span class="sxs-lookup"><span data-stu-id="cdfec-116">For more information, see [Providing a Custom Ducking Behavior](providing-a-custom-ducking-experience.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdfec-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cdfec-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdfec-118">Utilisation d’un appareil de communication</span><span class="sxs-lookup"><span data-stu-id="cdfec-118">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="cdfec-119">Désactivation de l’expérience de l’utilisation des canards par défaut</span><span class="sxs-lookup"><span data-stu-id="cdfec-119">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="cdfec-120">Fournir un comportement de canard personnalisé</span><span class="sxs-lookup"><span data-stu-id="cdfec-120">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="cdfec-121">Considérations relatives à l’implémentation pour l’installation de notifications</span><span class="sxs-lookup"><span data-stu-id="cdfec-121">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="cdfec-122">Obtention d’événements de canard</span><span class="sxs-lookup"><span data-stu-id="cdfec-122">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



