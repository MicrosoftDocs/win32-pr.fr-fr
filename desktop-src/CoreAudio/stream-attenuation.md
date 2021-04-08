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
# <a name="default-ducking-experience"></a>Expérience de l’utilisation des canards par défaut

Imaginez un scénario dans lequel un utilisateur reçoit un appel téléphonique tout en écoutant de la musique sur l’ordinateur. Pendant l’appel téléphonique, l’utilisateur souhaite réduire le volume de la musique tout en participant à l’appel téléphonique et reprendre le volume d’origine après la fin de l’appel téléphonique. En fonction des options spécifiées par l’utilisateur dans le panneau de configuration **sons** , le système d’exploitation fournit automatiquement cette *fonctionnalité via* l' *atténuation* ou l’atténuation du flux, en réduisant l’intensité d’un flux audio.

L’expérience d’atténuation par défaut dépend des préférences de l’utilisateur, comme spécifié dans l’option **son** du panneau de configuration. Sous l’onglet **communications** , l’utilisateur peut choisir un niveau d’atténuation (la valeur par défaut est 80%), désactiver tous les flux de communication non-communication ou désactiver l’expérience d’atténuation de flux par défaut. Le système permet d’ouvrir de nouveaux flux de non-communication (à l’exception des nouveaux sons système) pendant la session de communication, mais les nouveaux flux ne sont pas automatiquement atténués. Lorsque tous les flux de communication sont fermés, le système met fin à la session de communication et restaure le volume des flux qui ont été atténués au cours de la session de communication.

Pour indiquer visuellement l’atténuation du flux, le système modifie les paramètres du mélangeur de volume en fonction de la préférence de l’utilisateur. Par exemple, si l’utilisateur spécifie un niveau d’atténuation, le mélangeur de volume réduit le curseur, affiche le nouveau volume atténué et affiche le niveau de volume d’origine. L’illustration suivante montre ce processus.

![diagramme du comportement d’atténuation de flux par défaut fourni dans Windows 7](images/stream-aatenuation.jpg)

Une application peut remplacer l’atténuation de flux et implémenter une expérience de canard personnalisée si elle sait à quel moment la session de communication démarre et se termine. Pour plus d’informations, consultez [la page fournir un comportement de canard personnalisé](providing-a-custom-ducking-experience.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’un appareil de communication](using-the-communication-device.md)
</dt> <dt>

[Désactivation de l’expérience de l’utilisation des canards par défaut](disabling-the-ducking-experience.md)
</dt> <dt>

[Fournir un comportement de canard personnalisé](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Considérations relatives à l’implémentation pour l’installation de notifications](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Obtention d’événements de canard](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



