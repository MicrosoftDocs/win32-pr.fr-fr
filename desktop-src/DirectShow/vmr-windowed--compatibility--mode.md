---
description: Mode avec fenêtres VMR (compatibilité)
ms.assetid: e9fb1c83-860a-44c1-9633-c86f5d0fdadd
title: Mode avec fenêtres VMR (compatibilité)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d27a5a115ac87475a27365a0211d93cf18e785983cda12ee338e73b24fb0f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049292"
---
# <a name="vmr-windowed-compatibility-mode"></a>Mode avec fenêtres VMR (compatibilité)

VMR est conçu pour être compatible avec toutes les applications de DirectShow existantes. Lorsqu’il est utilisé avec une application existante, VMR fonctionne en mode fenêtre avec un seul flux vidéo, également appelé mode de compatibilité. ce mode est fourni, car VMR-7 est le convertisseur par défaut sur Windows XP et est donc automatiquement utilisé dans les appels à des méthodes de [Connecter intelligentes](intelligent-connect.md) telles que [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile). si votre application utilise des Connecter intelligents et nécessite uniquement des fonctionnalités de rendu de base, vous n’avez pas besoin de code spécial pour effectuer une restitution correcte avec VMR-7 sur Windows XP.

VMR-9 s’exécute également en mode fenêtre/compatibilité par défaut. Toutefois, VMR-9 n’est jamais le convertisseur vidéo par défaut. Pour utiliser VMR-9 dans une application, vous devez l’ajouter explicitement au graphique de filtre. Pour cette raison, et étant donné que le mode sans fenêtre offre de meilleures fonctionnalités que le mode fenêtre, il n’existe aucun avantage particulier à utiliser VMR-9 en mode fenêtre/compatibilité.

**Utilisation de VMR-7 en mode fenêtre/compatibilité**

Aucune programmation spéciale n’est requise pour configurer ou contrôler VMR-7 en mode fenêtre/compatibilité. Il vous suffit de générer le graphique de filtre à l’aide des appels de génération de graphiques standard, et VMR-7 utilise par défaut ce mode.

En mode fenêtre/compatibilité, VMR-7 crée sa propre fenêtre pour afficher la vidéo. Pour ce faire, il charge le composant Gestionnaire de fenêtres, qui expose les interfaces [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) et [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) . votre application peut interroger le gestionnaire de Graph de filtre pour ces interfaces, exactement comme vous le feriez avec l’ancien filtre de convertisseur vidéo. Pour plus d’informations, consultez [utilisation du mode fenêtre](using-windowed-mode.md).

L’illustration suivante montre VMR-7 en mode fenêtre/compatibilité.

![VMR en mode de compatibilité](images/vmr-compat-mode.png)

Pour garantir le niveau de compatibilité maximal, la fenêtre vidéo a le même nom de classe que celui créé par l’ancien filtre de convertisseur vidéo, et la plupart du code du gestionnaire de fenêtres de l’ancien convertisseur vidéo est toujours utilisé par VMR. En mode fenêtre/compatibilité, VMR n’utilise plus de ressources système que l’ancien convertisseur vidéo. Dans la mesure où VMR-7 n’a qu’un seul flux d’entrée en mode fenêtre/compatibilité, il ne charge pas ses composants mixer ou compositeur.

Par défaut, VMR étire l’image pour remplir la fenêtre vidéo. Pour conserver les proportions de la source, appelez la méthode [**IVMRAspectRatioControl :: SetAspectRatioMode**](/windows/desktop/api/Strmif/nf-strmif-ivmraspectratiocontrol-setaspectratiomode) avec l' \_ indicateur de zone de lettre VMR ARMODE \_ \_ .

> [!Note]  
> Les applications MFC qui placent la fenêtre vidéo dans une fenêtre enfant doivent définir un \_ Gestionnaire de messages WM ERASEBKGND vide, sans quoi la zone d’affichage vidéo ne se repeintra pas correctement.

 

**Utilisation de VMR-7 en mode fenêtre/compatibilité avec plusieurs Flux**

En mode fenêtre/compatibilité, VMR-7 crée une seule broche d’entrée par défaut et désactive le mode de mixage. Pour activer le mode de mixage, vous devez configurer VMR avant de le connecter. pour plus d’informations, consultez [VMR avec plusieurs Flux (Mode de mixage)](vmr-with-multiple-streams--mixing-mode.md). En mode de mixage, VMR charge les composants de mixage et de compositeur, qui nécessitent davantage de ressources système.

**Utilisation de VMR-9 en mode fenêtre**

Étant donné que VMR-9 n’est pas le convertisseur par défaut, il n’a pas de mode de compatibilité comme tel. Au lieu de cela, VMR-9 passe par défaut au mode fenêtre avec quatre broches d’entrée. Vous pouvez utiliser ce mode pour mélanger jusqu’à quatre flux vidéo. si vous devez mélanger un plus grand nombre de flux, vous devez le configurer comme décrit dans [VMR avec plusieurs Flux (Mode de mixage)](vmr-with-multiple-streams--mixing-mode.md). Sinon, VMR-9 en mode fenêtre se comporte exactement comme VMR-7 en mode fenêtre/compatibilité.

 

 



