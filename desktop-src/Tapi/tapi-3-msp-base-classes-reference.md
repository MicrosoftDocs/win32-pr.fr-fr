---
description: La documentation suivante fournit des détails sur les classes de base du fournisseur de services de média.
ms.assetid: ef845c44-1ff5-42a1-8e91-38d66e6fe363
title: Référence des classes de base TAPI 3 MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1c0b2f19f372e60972c66d965f689ec79f930f343080be21471fbc4ba59f67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905739"
---
# <a name="tapi-3-msp-base-classes-reference"></a>Référence des classes de base TAPI 3 MSP

La documentation suivante fournit des détails sur les classes de base du fournisseur de services de média.



| Classes de base du fournisseur de services multimédia (ordre alphabétique) | Description                                                                                                                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CAudioCaptureTerminal](caudiocaptureterminal.md)       | dérivé de [CSingleFilterTerminal](csinglefilterterminal.md) et implémente un terminal de capture audio statique pour les appareils wave à l’aide du filtre DirectShow wave. Défini dans MSPtmac. h.               |
| [CAudioRenderTerminal](caudiorenderterminal.md)         | dérivé de [CSingleFilterTerminal](csinglefilterterminal.md) et implémente un terminal de rendu audio statique pour les appareils wave à l’aide du filtre waveout DirectShow. Défini dans MSPtrmar. h.              |
| [CBaseTerminal](cbaseterminal.md)                       | Classe de base de terminal applicable aux terminaux statiques et dynamiques. Comme elle est entièrement générique, toute implémentation de terminal peut dériver de cette classe directement ou indirectement. Défini dans MSPterm. h |
| [**CMSPAddress**](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)                       | Implémente l’objet d’adresse MSP et prend en charge l’interface [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress) . Défini dans MSPaddr. h.                                                                                |
| [CMSPArray](cmsparray.md)                               | Modèle qui implémente un tableau intelligent qui s’agrandit à la demande. Défini dans MSPutils. h.                                                                                                               |
| [**CMSPCallBase**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallbase)                     | Fournit une implémentation générique de l’objet d’appel et prend en charge l’interface [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) . Défini dans MSPcall. h.                                                       |
| [**CMSPCallMultiGraph**](/windows/desktop/api/Mspcall/nl-mspcall-cmspcallmultigraph)         | Définit un appel qui utilise un graphique de filtre pour chaque flux. Défini dans MSPcall. h.                                                                                                                          |
| [**CMSPStream**](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)                         | Expose des méthodes qui permettent à une application de démarrer, suspendre ou arrêter un sous-flux, et de sélectionner ou désélectionner des terminaux. Défini dans MSPstrm. h.                                                              |
| [CMSPThread](cmspthread.md)                             | Implémente le thread de travail du MSP. Défini dans MSPthrd. h.                                                                                                                                               |
| [CSingleFilterTerminal](csinglefilterterminal.md)       | Classe de base de terminal supplémentaire applicable aux terminaux statiques et dynamiques. rend l’implémentation plus spécifique en supposant que le terminal possède un filtre de DirectShow unique. Défini dans MSPterm. h.    |
| [CVideoCaptureTerminal](cvideocaptureterminal.md)       | dérivé de [CSingleFilterTerminal](csinglefilterterminal.md) et implémente un terminal de capture vidéo statique à l’aide d’un filtre de DirectShow unique. Défini dans MSPtmvc. h.                                  |



 

 

 
