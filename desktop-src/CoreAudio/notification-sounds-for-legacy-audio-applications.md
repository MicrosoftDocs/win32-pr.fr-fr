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
# <a name="notification-sounds-for-legacy-audio-applications"></a>Sons de notification pour les applications audio héritées

Dans Windows Vista, le système d’exploitation affecte tous ses sons de notification système à une session audio interprocessus qui s’exécute via l’appareil de point de terminaison de rendu qui est actuellement affecté au [rôle d’appareil](device-roles.md)eConsole. Le programme de contrôle du volume système, sndvol, affiche un curseur de volume dédié aux sons de notification du système.

Certaines applications lisent des sons de notification. Au lieu de demander à l’utilisateur de gérer les sons de notification d’une application via un curseur de volume distinct dans sndvol, l’application peut attribuer ses sons de notification à la même session que les sons de notification du système. Le curseur de volume sndvol qui contrôle les sons de notification du système contrôle ensuite les sons de notification de l’application.

Pour activer ce comportement, Windows Vista définit un \_ indicateur système SND pour la fonction [**PlaySound**](/previous-versions//dd743680(v=vs.85)) héritée. (Cet indicateur n’est pas pris en charge dans les versions antérieures de Windows, notamment Windows Server 2003, Windows XP et Windows 2000.) Si l’appelant définit cet indicateur, la fonction **PlaySound** affecte le son qu’elle joue à la session inter-processus que le système d’exploitation utilise pour ses sons de notification. Si l’appelant ne définit pas l’indicateur, **PlaySound** affecte le son qu’il joue à la session par défaut : la session spécifique au processus qui est identifiée par la valeur GUID de la session GUID \_ null. SND \_ System est défini dans le fichier d’en-tête MMSYSTEM. h. Pour plus d’informations sur **PlaySound**, consultez la documentation SDK Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Interopérabilité avec les API audio héritées](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 
