---
description: La liste suivante contient les méthodes CMSPStream appelées par l’objet MSPCall.
ms.assetid: 7a59ca78-b5e8-45e9-8fdb-89402ffef916
title: Méthodes CMSPStream appelées par l’objet MSPCall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89744f9e4cf2739fa11f07edc4be7e331beb620a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544286"
---
# <a name="cmspstream-public-methods-called-by-mspcall-object"></a>CMSPStream, méthodes publiques appelées par l’objet MSPCall



| Méthodes publiques CMSPStream                                 | Description                                                                             |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Rein**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-init)                           | Appelée par **MSPCall** lors de la création du flux.                                   |
| [**Correct**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-shutdown)                   | Appelée par **MSPCall** pour désélectionner tous les objets terminal et libérer l’objet d’appel. |
| [**GetState**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-getstate)                   | Appelée par l’objet MSPCall pour recevoir l’état actuel du flux.                   |
| [**HandleTSPData**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-handletspdata)         | L’objet d’appel dérivé peut appeler cette méthode pour permettre au flux de gérer les commandes TSP.     |
| [**ProcessGraphEvent**](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-processgraphevent) | Appelée par l’objet MSPCall pour permettre au flux de gérer les événements de graphique.                     |



 

 

 



