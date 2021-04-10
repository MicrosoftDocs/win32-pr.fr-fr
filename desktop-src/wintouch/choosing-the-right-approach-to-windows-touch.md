---
title: Choix de la bonne approche pour Windows Touch
description: Cette section explique les différentes approches de la fonction tactile Windows que vous pouvez utiliser.
ms.assetid: 983023e4-355b-45ba-8572-d93c460d2ff8
keywords:
- Tactile Windows, différentes approches
- Tactile Windows, choix des approches
- Tactile Windows, amélioration des applications
- Tactile Windows, prise en charge du zoom
- Tactile Windows, support hérité
- Tactile Windows, plug-in RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cdd35b73989541fadd5449efbb3f95d76bfa5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031616"
---
# <a name="choosing-the-right-approach-to-windows-touch"></a>Choix de la bonne approche pour Windows Touch

Cette section explique les différentes approches de la fonction tactile Windows que vous pouvez utiliser.

Vous pouvez améliorer les applications à l’aide des fonctionnalités tactiles de Windows de nombreuses façons. Avant d’adopter une méthode, vous devez prendre en compte ce que vous souhaitez faire avec votre application. Les scénarios suivants sont typiques pour Windows Touch :

-   Vous souhaitez que votre application se comporte de la même façon que dans les versions héritées de Windows, mais que les messages tactiles Windows se comportent de manière cohérente.
-   Vous souhaitez la prise en charge de la rotation, de la translation, de la panoramisation ou du zoom personnalisé dans votre application.
-   Vous souhaitez que votre application ait une interprétation fine des gestes tactiles Windows ou interprète plusieurs touches sur une application qui est spécifiquement optimisée pour l’entrée tactile Windows.
-   Vous avez une application qui utilise l’objet [**RealTimeStylus**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus) et que vous souhaitez l’améliorer avec les fonctionnalités tactiles de Windows.

## <a name="you-want-your-application-to-behave-as-it-did-in-legacy-versions-of-windows"></a>Vous souhaitez que votre application se comporte comme dans les versions héritées de Windows

Dans Windows 7, les applications génèrent par défaut des messages qui activent la fonctionnalité tactile Windows. Par exemple, les gestes de panoramique déclenchent des \_ \* messages de défilement WM. En plus de la prise en charge du panoramique, le \_ Gestionnaire de mouvements WM par défaut dans Windows 7 prend en charge les commentaires de limite, le zoom et l’appui sur. Les commentaires sur les limites sont également activés via la prise en charge héritée. Pour plus d’informations sur la façon dont les gestes sont mappés aux messages, consultez [vue d’ensemble des gestes tactiles Windows](windows-touch-gestures-overview.md) . Les développeurs qui souhaitent uniquement cette fonctionnalité de base n’ont pas besoin de travailler directement avec l’API tactile Windows.

> [!Note]  
> Les gestionnaires de barres de défilement personnalisés doivent prendre en charge la demande **SM \_ THUMBPOSITION** pour les messages **WM \_ VSCROLL** et doivent prendre en charge la demande **SB \_ LINELEFT** et la demande **SB \_ LINERIGHT** pour les messages **WM \_ HSCROLL** .

 

-   La section [prise en charge héritée du panorama avec des barres de défilement](legacy-support-for-panning-with-scrollbars.md) explique comment s’assurer que votre application se comporte comme les utilisateurs attendent dans Windows 7.

## <a name="you-want-custom-object-rotation-translation-panning-or-zoom-support"></a>Vous souhaitez la prise en charge de la rotation, de la translation, de la panoramisation ou du zoom personnalisé

Si vous souhaitez une prise en charge limitée de Touch, mais que le comportement par défaut proposé par Windows 7 n’est pas adapté à votre application, vous pouvez utiliser des gestes pour améliorer votre application. En utilisant des mouvements, vous pouvez interpréter les commandes de mouvement en gérant le message de [**\_ mouvement WM**](wm-gesture.md) . Vous trouverez plus d’informations sur les gestes dans la section [gestes tactiles Windows](guide-multi-touch-gestures.md). Si votre application a besoin d’une prise en charge uniquement pour les rotations à haute granularité, la prise en charge améliorée du zoom ou le panoramique à un seul doigt, les gestes constituent la meilleure approche pour le développement tactile Windows. En plus d’interpréter le message de mouvement, vous pouvez choisir de prendre en charge les commentaires de limite. Pour plus d’informations sur les commentaires sur les limites, consultez la section relative aux commentaires sur les [limites](boundary-feedback.md) de la [référence de programmation tactile Windows](windows-touch-programming-reference.md). Dans Windows 7, l’invite de commandes et Internet Explorer tirent parti des commentaires et des mouvements de limite.

-   La section [amélioration de l’expérience panoramique avec un seul doigt](improving-the-single-finger-panning-experience.md) explique comment personnaliser l’expérience de panoramique en gérant le message de [**\_ mouvement WM**](wm-gesture.md) .

## <a name="you-want-fine-grained-gesture-interpretation-or-custom-handling-of-multiple-touch-points"></a>Vous souhaitez une interprétation de mouvement affinée ou une gestion personnalisée de plusieurs points tactiles

Si vous souhaitez avoir un contrôle de mouvements encore plus spécifique que celui offert par le message [**de \_ mouvement WM**](wm-gesture.md) , ou que vous souhaitez interpréter plusieurs mouvements sur plusieurs objets, vous devez utiliser le processeur de manipulation. Le processeur de manipulation est essentiellement un sur-ensemble de gestes. L’utilisation du processeur de manipulation requiert l’implémentation d’un récepteur d’événements pour les manipulations auxquelles vous alimentez des données tactiles brutes.

Si vous souhaitez une physique d’objets simple en plus d’interpréter les gestes, vous devez utiliser un processeur d’inertie conjointement avec le processeur de manipulation. Le processeur d’inertie fonctionne avec le processeur de manipulation en acceptant les valeurs de vélocité du processeur de manipulation à la fin de la manipulation.

Si vous souhaitez interpréter plusieurs points tactiles dans votre application, vous devez créer un gestionnaire de messages pour le message [**WM \_ Touch**](wm-touchdown.md) .

-   La section [entrée tactile Windows](guide-multi-touch-input.md) explique comment interpréter le message [**WM \_ Touch**](wm-touchdown.md) .
-   La section [détection et suivi de plusieurs points tactiles](detecting-and-tracking-multiple-touch-points.md) montre comment créer une application simple qui interprète plusieurs entrées.
-   La section relative aux [manipulations et à l’inertie](manipulation-and-inertia.md) explique comment activer l’approche la plus souple pour Windows Touch.

## <a name="you-want-to-enable-windows-touch-input-to-an-application-that-uses-the-realtimestylus"></a>Vous souhaitez activer l’entrée tactile Windows dans une application qui utilise l’RealTimeStylus

Si vous souhaitez activer l’entrée pour plusieurs contacts sur la plateforme Tablet PC, vous devez implémenter un plug-in personnalisé RealTimeStylus qui interprète les données tactiles Windows. Microsoft a introduit les interfaces [**ITablet3**](/windows/desktop/tablet/itablet3) et [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3) pour permettre l’entrée de plusieurs contacts dans le plug-in RealTimeStylus. Ces interfaces simplifient l’extension des plug-ins RealTimeStylus pour prendre en charge plusieurs points de contact.

Pour vérifier si la prise en charge de plusieurs contacts est activée, appelez [**IsMultiTouch**](/windows/desktop/tablet/itablet3-ismultitouch). Pour vérifier le nombre de contacts pris en charge, appelez [**GetMaximumCursors**](/windows/desktop/tablet/itablet3-getmaximumcursors). Pour activer ou désactiver le support de plusieurs contacts, appelez [**MultiTouchEnabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled).

> [!Note]  
> Si vous n’activez pas plusieurs points de contact dans l’RealTimeStylus, vous recevrez des messages de mouvement tels que le panoramique et le zoom.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation](programming-guide.md)
</dt> </dl>

 

 