---
description: Sons de notification pour les applications audio héritées
ms.assetid: c5ad67d9-56fb-4bf0-aea4-5b49b0e5bf95
title: Sons de notification pour les applications audio héritées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e9ee2ef1155694e32a21779c55d290da6b3799c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523804"
---
# <a name="notification-sounds-for-legacy-audio-applications"></a><span data-ttu-id="411b6-103">Sons de notification pour les applications audio héritées</span><span class="sxs-lookup"><span data-stu-id="411b6-103">Notification Sounds for Legacy Audio Applications</span></span>

<span data-ttu-id="411b6-104">Dans Windows Vista, le système d’exploitation affecte tous ses sons de notification système à une session audio interprocessus qui s’exécute via l’appareil de point de terminaison de rendu qui est actuellement affecté au [rôle d’appareil](device-roles.md)eConsole.</span><span class="sxs-lookup"><span data-stu-id="411b6-104">In Windows Vista, the operating system assigns all of its system notification sounds to a cross-process audio session that plays through the rendering endpoint device that is currently assigned to the eConsole [device role](device-roles.md).</span></span> <span data-ttu-id="411b6-105">Le programme de contrôle du volume système, sndvol, affiche un curseur de volume dédié aux sons de notification du système.</span><span class="sxs-lookup"><span data-stu-id="411b6-105">The system volume-control program, Sndvol, displays a volume slider that is dedicated to system notification sounds.</span></span>

<span data-ttu-id="411b6-106">Certaines applications lisent des sons de notification.</span><span class="sxs-lookup"><span data-stu-id="411b6-106">Some applications play notification sounds.</span></span> <span data-ttu-id="411b6-107">Au lieu de demander à l’utilisateur de gérer les sons de notification d’une application via un curseur de volume distinct dans sndvol, l’application peut attribuer ses sons de notification à la même session que les sons de notification du système.</span><span class="sxs-lookup"><span data-stu-id="411b6-107">Instead of requiring the user to manage an application's notification sounds through a separate volume slider in Sndvol, the application can assign its notification sounds to the same session as the system notification sounds.</span></span> <span data-ttu-id="411b6-108">Le curseur de volume sndvol qui contrôle les sons de notification du système contrôle ensuite les sons de notification de l’application.</span><span class="sxs-lookup"><span data-stu-id="411b6-108">The Sndvol volume slider that controls the system notification sounds then controls the notification sounds from the application.</span></span>

<span data-ttu-id="411b6-109">Pour activer ce comportement, Windows Vista définit un \_ indicateur système SND pour la fonction [**PlaySound**](/previous-versions//dd743680(v=vs.85)) héritée.</span><span class="sxs-lookup"><span data-stu-id="411b6-109">To enable this behavior, Windows Vista defines a SND\_SYSTEM flag for the legacy [**PlaySound**](/previous-versions//dd743680(v=vs.85)) function.</span></span> <span data-ttu-id="411b6-110">(Cet indicateur n’est pas pris en charge dans les versions antérieures de Windows, notamment Windows Server 2003, Windows XP et Windows 2000.) Si l’appelant définit cet indicateur, la fonction **PlaySound** affecte le son qu’elle joue à la session inter-processus que le système d’exploitation utilise pour ses sons de notification.</span><span class="sxs-lookup"><span data-stu-id="411b6-110">(This flag is not supported in earlier versions of Windows, including Windows Server 2003, Windows XP, and Windows 2000.) If the caller sets this flag, then the **PlaySound** function assigns the sound that it plays to the cross-process session that the operating system uses for its notification sounds.</span></span> <span data-ttu-id="411b6-111">Si l’appelant ne définit pas l’indicateur, **PlaySound** affecte le son qu’il joue à la session par défaut : la session spécifique au processus qui est identifiée par la valeur GUID de la session GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="411b6-111">If the caller does not set the flag, then **PlaySound** assigns the sound that it plays to the default session—the process-specific session that is identified by the session GUID value GUID\_NULL.</span></span> <span data-ttu-id="411b6-112">SND \_ System est défini dans le fichier d’en-tête MMSYSTEM. h.</span><span class="sxs-lookup"><span data-stu-id="411b6-112">SND\_SYSTEM is defined in the header file Mmsystem.h.</span></span> <span data-ttu-id="411b6-113">Pour plus d’informations sur **PlaySound**, consultez la documentation SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="411b6-113">For more information about **PlaySound**, see the Windows SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="411b6-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="411b6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="411b6-115">Interopérabilité avec les API audio héritées</span><span class="sxs-lookup"><span data-stu-id="411b6-115">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
