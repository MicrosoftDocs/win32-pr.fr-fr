---
description: Événements MSWebDVD
ms.assetid: e43ea4ad-8ebe-4096-a9f3-a8f618b46877
title: Événements MSWebDVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e61a37eda7b8c2ebafc704d96195cc9e92e70fbd9d8bfda4aa7c971cd890e41c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042709"
---
# <a name="mswebdvd-events"></a>Événements MSWebDVD

> [!Note]  
> ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003. Il sera peut-être modifié ou indisponible dans les versions ultérieures.

 

> [!Note]  
> Cette API est déconseillée. pour plus d’informations sur la lecture et la navigation des dvd dans DirectShow, consultez [Applications dvd](dvd-applications.md).

 

le contrôle MSWebDVD Microsoft® ActiveX® notifie votre application lorsque divers types d’événements internes se produisent ou lorsque certaines informations sont rencontrées sur le disque.

La plupart des événements sont liés aux contrôles de l’opération de l’utilisateur (UOP). Les auteurs de DVD peuvent encoder le disque afin que toute commande de DVD (telle que **PlayForwards**, **Pause**, **ShowMenu**, etc.) puisse être désactivée à tout moment. Par exemple, la plupart des disques n’autorisent pas les utilisateurs à avancer rapidement ou à afficher un menu pendant que l’avertissement du FBI est lu. Une fois l’avertissement terminé, le disque autorise ces opérations. En gérant les événements UOP, votre application peut mettre à jour son interface utilisateur pour montrer à l’utilisateur les commandes qui sont actuellement autorisées par le disque. Pour ce faire, la méthode la plus courante consiste à désactiver un bouton. Par exemple, si votre application a reçu un événement PlayForwards avec **bEnabled** défini sur **false**, vous pouvez désactiver le bouton de lecture. Lors de la réception de cet événement avec **bEnabled** défini sur **true**, vous pouvez réactiver le bouton.

Il existe trois événements qui ne sont pas liés aux contrôles UOP. L’événement **DVDNotify** notifie votre application de nombreux types différents d’événements relatifs aux DVD, qui sont identifiés dans le paramètre *eventCode* . Certains événements ont des informations supplémentaires dans les paramètres *param1* et *param2* . l’événement **ReadyStateChange** avertit votre application des modifications apportées à la propriété ReadyState MSWebDVD, qui est une propriété commune à tous les contrôles ActiveX. L’événement **UpdateOverlay** est envoyé aux applications uniquement si elles hébergent des mswebdvd en mode sans fenêtre. Les applications doivent répondre à cet événement uniquement si elles affichent des boutons flottants sur le rectangle vidéo en mode plein écran.



| Événement                                                                  | Description                                                                           |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**ChangeCurrentAngle**](changecurrentangle.md)                       | Envoyé lorsque le disque active ou désactive la modification de l’angle.                            |
| [**ChangeCurrentAudioStream**](changecurrentaudiostream.md)           | Envoyé lorsque le disque active ou désactive la modification du flux audio.                     |
| [**ChangeCurrentSubpictureStream**](changecurrentsubpicturestream.md) | Envoyé lorsque la commande **ChangeCurrentSubpictureStream** a été activée ou désactivée. |
| [**DVDNotify**](dvdnotify.md)                                         | Notifie une application de nombreux événements DVD et instructions sur le disque.           |
| [**PauseOn**](pauseon.md)                                             | Envoyé lorsque la commande **Pause** a été activée ou désactivée.                         |
| [**PlayAtTime**](playattime.md)                                       | Envoyé lorsque la commande **PlayAtTime** a été activée ou désactivée.                    |
| [**PlayAtTimeInTitle**](playattimeintitle.md)                         | Envoyé lorsque la commande **PlayAtTimeInTitle** a été activée ou désactivée.             |
| [**PlayBackwards**](playbackwards.md)                                 | Envoyé lorsque la commande **PlayBackwards** a été activée ou désactivée.                 |
| [**PlayChapter**](playchapter.md)                                     | Envoyé lorsque la commande **PlayChapter** a été activée ou désactivée.                   |
| [**PlayChapterInTitle**](playchapterintitle.md)                       | Envoyé lorsque la commande **PlayChapterInTitle** a été activée ou désactivée.            |
| [**PlayForwards**](playforwards.md)                                   | Envoyé lorsque la commande **PlayForwards** a été activée ou désactivée.                  |
| [**PlayNextChapter**](playnextchapter.md)                             | Envoyé lorsque la commande **PlayNextChapter** a été activée ou désactivée.               |
| [**PlayPrevChapter**](playprevchapter.md)                             | Envoyé lorsque la commande **PlayPrevChapter** a été activée ou désactivée.               |
| [**PlayTitle**](playtitle.md)                                         | Envoyé lorsque la commande **PlayTitle** a été activée ou désactivée.                     |
| [**ReadyStateChange**](readystatechange.md)                           | Envoyé lorsque la propriété **ReadyState** du contrôle mswebdvd a changé.            |
| [**ReplayChapter**](replaychapter.md)                                 | Envoyé lorsque la commande **ReplayChapter** a été activée ou désactivée.                 |
| [**Reprendre**](resume.md)                                               | Envoyé lorsque la commande de **reprise** a été activée ou désactivée.                        |
| [**ReturnFromSubmenu**](returnfromsubmenu.md)                         | Envoyé lorsque la commande **ReturnFromSubmenu** a été activée ou désactivée.             |
| [**SelectOrActivatButton**](selectoractivatbutton.md)                 | Envoyé lorsque le disque active ou désactive la sélection ou l’activation de boutons de menu.   |
| [**ShowMenu**](showmenu.md)                                           | Envoyé lorsque le disque active ou désactive l’émission d’un menu.                         |
| [**StillOff**](stilloff.md)                                           | Envoyé lorsque la commande **StillOff** a été activée ou désactivée.                      |
| [**Erreur**](stop.md)                                                   | Envoyé lorsque la commande **arrêter** a été activée ou désactivée.                          |
| [**UpdateOverlay**](updateoverlay.md)                                 | Envoyé lorsque la surface de recouvrement a été déplacée ou redimensionnée ou sa clé de couleur a changé. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objet MSWebDVD](mswebdvd-object.md)
</dt> </dl>

 

 



