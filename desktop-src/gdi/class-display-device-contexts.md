---
description: En utilisant un contexte de périphérique de classe, une application peut utiliser un contexte de périphérique d’affichage unique pour chaque fenêtre appartenant à une classe spécifiée.
ms.assetid: fc76abbf-68da-47f2-8145-4fad806297b4
title: Affichage de la classe contextes de périphérique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5a4cc0268d948e1a6f95050409698217e3f13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972763"
---
# <a name="class-display-device-contexts"></a>Affichage de la classe contextes de périphérique

En utilisant un *contexte de périphérique de classe*, une application peut utiliser un contexte de périphérique d’affichage unique pour chaque fenêtre appartenant à une classe spécifiée. Les contextes de périphérique de classe sont souvent utilisés avec les fenêtres de contrôle qui sont dessinées à l’aide des mêmes valeurs d’attribut. À l’instar des contextes de périphérique privé, les contextes de périphérique de classe réduisent le temps nécessaire pour préparer un contexte de périphérique pour le dessin.

Le système fournit un contexte de périphérique de classe pour une fenêtre s’il appartient à une classe de fenêtre avec le \_ style cs CLASSDC. Le système crée le contexte de périphérique lors de la création de la première fenêtre appartenant à la classe, puis utilise le même contexte de périphérique pour toutes les fenêtres créées par la suite dans la classe. Initialement, le contexte de périphérique de la classe a les mêmes valeurs par défaut pour les attributs qu’un contexte de périphérique courant, mais l’application peut les modifier à tout moment. Le système conserve toutes les modifications, à l’exception de la région de découpage et de l’origine de l’appareil, jusqu’à ce que la dernière fenêtre de la classe ait été détruite. Une modification apportée à une fenêtre s’applique à toutes les fenêtres de cette classe.

Une application peut récupérer le descripteur du contexte de périphérique de la classe à l’aide de la fonction [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) à tout moment après la création de la première fenêtre. L’application peut conserver et utiliser le handle sans le libérer, car le contexte de périphérique de la classe ne fait pas partie du cache de contexte de périphérique d’affichage. Si l’application crée une autre fenêtre dans la même classe de fenêtre, l’application doit récupérer à nouveau le contexte de périphérique de la classe. La récupération du contexte de périphérique définit l’origine de l’appareil et la région de découpage appropriées pour la nouvelle fenêtre. Une fois que l’application a récupéré la classe du contexte de périphérique pour une nouvelle fenêtre de la classe, le contexte de périphérique ne peut plus être utilisé pour dessiner dans la fenêtre d’origine sans la récupérer pour cette fenêtre. En général, chaque fois qu’il doit dessiner dans une fenêtre, une application doit récupérer explicitement le contexte de périphérique de la classe pour la fenêtre.

Les applications qui utilisent des contextes de périphérique de classe doivent toujours appeler [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) lors du traitement d’un message de [**\_ peinture WM**](wm-paint.md) . La fonction définit l’origine de l’appareil et la région de découpage appropriées pour la fenêtre et intègre la région de mise à jour. L’application doit également appeler [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) pour restaurer le signe insertion si **BeginPaint** le rend HID. **EndPaint** n’a aucun autre effet sur un contexte de périphérique de classe.

Le système transmet le contexte de périphérique de la classe lors de l’envoi du message [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) à l’application, ce qui permet aux valeurs d’attribut actuelles d’affecter tout dessin effectué par l’application ou le système lors du traitement de ce message. Comme c’est le cas avec une fenêtre ayant un contexte de périphérique privé, une application peut utiliser [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) pour forcer le système à retourner un contexte de périphérique courant pour la fenêtre qui a un contexte de périphérique de classe.

L’utilisation de contextes de périphérique de classe n’est pas recommandée.

 

 
