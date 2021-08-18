---
description: Contrôle de flux
ms.assetid: b529b38c-a25c-42dd-aee1-5d263c94202d
title: Contrôle de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8da9f317137904a87356bbdcc10dc68357513cf168a0b7b7ea46398ed47a81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072383"
---
# <a name="stream-control"></a>Contrôle de flux

L’interface [**IVMRVideoStreamControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol) sur la ou les broches d’entrée de VMR permet aux applications et aux filtres en amont de contrôler le comportement du composant de mixage, y compris l’ordre de plan et l’état actif des flux d’entrée de VMR. Même si cette interface est exposée sur les broches, elle opère sur le composant mixer de VMR. elle n’est donc disponible que lors du chargement du mélangeur, ce qui se passe quand VMR traite plusieurs flux d’entrée. Les filtres en amont utilisent les méthodes [**SetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey) et [**GetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey) pour contrôler la clé de couleur source. Ces méthodes permettent des effets tels que la superposition de l’animation sur la vidéo. Il vous suffit de définir la clé de couleur sur la couleur d’arrière-plan du flux d’animation, et VMR doit mélanger ce flux avec un autre flux vidéo. Les applications doivent prendre soin de ne pas modifier la clé de couleur sur une valeur différente de la valeur utilisée par un filtre en amont, tel qu’un décodeur.

Les filtres utilisent les méthodes [**GetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate) et [**SetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate) pour indiquer au mélangeur s’il faut attendre des données d’entrée à partir d’un code confidentiel spécifié. Par exemple, le décodeur Line21 utilise ces méthodes pour activer la broche d’entrée de VMR pour les données Line21 uniquement lorsque ces données sont présentes dans le flux. Le fait de définir un code PIN sur un état inactif indique au mélangeur de ne pas attendre les données d’un code confidentiel spécifié avant de procéder à la composition de l’image.

 

 



