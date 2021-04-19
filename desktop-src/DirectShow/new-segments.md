---
description: Nouveaux segments
ms.assetid: 6c470b38-481f-4e52-93b8-eb6b343dcefc
title: Nouveaux segments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5438cb3b457ed8ea0f77bd2ac1dcc5d6d2c72698
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517365"
---
# <a name="new-segments"></a>Nouveaux segments

Un *segment* est un groupe d’exemples de médias qui partagent une heure de début, une heure d’arrêt et une vitesse de lecture communes. La méthode [**IPIN :: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) signale le début d’un nouveau segment. Il permet à un filtre source d’informer les filtres en aval que les informations relatives au temps et au taux ont changé. Par exemple, si le filtre source cherche à un nouveau point dans le flux, il appelle **NewSegment** avec la nouvelle heure de début.

Certains filtres en aval utilisent les informations de segment lorsqu’ils traitent des exemples. Par exemple, dans un format qui utilise la compression interframe, si l’heure d’arrêt tombe sur un frame Delta, le filtre source peut avoir besoin d’envoyer des échantillons supplémentaires après l’heure d’arrêt. Cela permet au décodeur de décoder le frame Delta final. Pour déterminer le cadre final correct, le décodeur fait référence à l’heure d’arrêt du segment. Autre exemple, les convertisseurs audio utilisent le taux de segment, ainsi que le taux d’échantillonnage audio pour générer la sortie audio correcte.

Dans le modèle push, le filtre source lance l’appel **NewSegment** . Dans le modèle d’extraction, cette opération est effectuée par le filtre de l’analyseur. Dans les deux cas, le filtre appelle **NewSegment** sur la broche d’entrée en aval, qui propage l’appel au filtre suivant, jusqu’à ce que l’appel atteigne le convertisseur. Les filtres doivent sérialiser les appels **NewSegment** avec d’autres appels de diffusion, tels que [**IMemInputPin :: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).

Temps de flux rétablit à zéro après chaque nouveau segment. Horodatages sur les échantillons fournis après le début du segment à partir de zéro.

 

 



