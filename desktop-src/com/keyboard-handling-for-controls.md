---
title: Gestion du clavier pour les contrôles
description: Un contrôle répond aux accélérateurs de clavier afin que l’utilisateur final puisse lancer des actions effectuées par le contrôle.
ms.assetid: 59aca5cb-f109-49ee-897d-43610501f7f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe03058fdb0192a0f8f7b13032612288045775b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293679"
---
# <a name="keyboard-handling-for-controls"></a>Gestion du clavier pour les contrôles

Un contrôle répond aux accélérateurs de clavier afin que l’utilisateur final puisse lancer des actions effectuées par le contrôle. Le conteneur gère l’activité du clavier pour tous ses contrôles incorporés. Avec les documents composés, les accélérateurs de clavier s’appliquent uniquement à l’objet actuellement actif. Avec les contrôles, un mécanisme a été ajouté de manière à ce qu’un contrôle puisse répondre à ses mnémoniques de clavier, même s’il n’est pas actuellement actif dans l’interface utilisateur.

Les méthodes [**IOleControl :: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) et [**IOleControl :: OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) et la méthode [**IOleControlSite :: OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) gèrent les mnémoniques du clavier d’un contrôle. Une structure [**CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) décrit les accélérateurs mnémoniques d’un contrôle, et les indicateurs renvoyés avec celle-ci via la méthode **GetControlInfo** décrivent le comportement des contrôles avec les touches entrée et ÉCHAP. Lorsqu’un contrôle modifie ses mnémoniques, il appelle **OnControlInfoChanged** afin que le conteneur puisse recharger la structure si nécessaire.

Lorsqu’un contrôle est activé par l’interface utilisateur, il s’agit également du contrôle avec le focus. À mesure que les contrôles sont activés et désactivés entre les États active et active de l’interface utilisateur sur place, le contrôle appelle [**IOleControlSite :: onfocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) pour indiquer au conteneur de telles modifications.

En outre, lorsqu’un contrôle est activé par l’interface utilisateur, il aura la possibilité de traiter toutes les séquences de touches. Pour permettre à un conteneur de traiter la séquence de touches avant le contrôle, le contrôle appelle [**IOleControlSite :: TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator). Si le conteneur ne gère pas la séquence de touches, le contrôle le traite.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[ActiveX Commandes](activex-controls.md)
</dt> </dl>

 

 




