---
description: Le tableau suivant répertorie les GUID de propriété de paquet utilisés par la structure de propriété de paquet \_ .
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: GUID PacketProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c897e19aea30db6e5dfa026fbdcfec77de5afa4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481645"
---
# <a name="packetproperty-guids"></a>GUID PacketProperty

Le tableau suivant répertorie les GUID de propriété de paquet utilisés par la structure de [**\_ propriété de paquet**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) .




| GUID | Description | 
|------|-------------|
| GUID_ALTITUDE_ORIENTATION<br /> | Angle entre l’axe du stylet et la surface de la tablette. La valeur est 0 lorsque le stylet est parallèle à la surface et 90 lorsque le stylet est perpendiculaire à la surface. Les valeurs sont négatives lorsque le stylet est inversé.<br /> | 
| GUID_AZIMUTH_ORIENTATION<br /> | Rotation dans le sens des aiguilles d’une montre autour de l’axe z dans une plage circulaire complète.<br /> | 
| GUID_BOXNUMBER<br /> | GUID utilisé pour récupérer le numéro de zone d’un autre module de reconnaissance de l’encre lorsque le module de reconnaissance fonctionne en mode Box.<br /> | 
| GUID_BUTTON_PRESSURE<br /> | Pression sur un bouton sensible à la pression.<br /> | 
| GUID_NORMAL_PRESSURE<br /> | GUID de l’objet PacketProperty qui représente la pression de l’extrémité du stylet perpendiculairement à la surface du Tablet PC. Plus la pression placée sur la pointe du stylet est importante, plus l’encre est dessinée.<br /> | 
| GUID_PACKET_STATUS<br /> | Contient une ou plusieurs des valeurs d’indicateur suivantes :<br /><ul><li>Le curseur touche la surface de dessin (valeur = 1).</li><li>Le curseur est inversé. Par exemple, la fin de la gomme du stylet pointe vers la surface (valeur = 2).</li><li>Non utilisé (valeur = 4).</li><li>Le bouton en barillet est enfoncé (valeur = 8).</li></ul> | 
| GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID<br /> | Identificateur de contact de l’appareil pour un paquet.<br /> | 
| GUID_SERIAL_NUMBER<br /> | Identifie le paquet. Il s’agit de la même valeur que celle utilisée pour récupérer le paquet de la file d’attente de paquets.<br /> | 
| GUID_TANGENT_PRESSURE<br /> | GUID de l’objet PacketProperty qui représente la pression de l’extrémité du stylet le long du plan de la surface de la tablette.<br /> | 
| GUID_TIMER_TICK<br /> | Heure de génération du paquet.<br /> | 
| GUID_TWIST_ORIENTATION<br /> | Rotation du curseur dans le sens horaire autour de son axe.<br /> | 
| GUID_X<br /> | Coordonnée x dans l’espace de coordonnées de la tablette. Chaque paquet contient cette propriété par défaut. L’origine (0,0) de la tablette est l’angle supérieur gauche.<br /> | 
| GUID_X_TILT_ORIENTATION<br /> | Pour un curseur de stylet, l’orientation de l’inclinaison x est l’angle entre le plan y, le plan z et le plan de l’axe y et du stylet. La valeur est 0 lorsque le stylet est perpendiculaire à la surface de dessin et est positif lorsque le stylet est à droite de Perpendicular.<br /> | 
| GUID_Y<br /> | Coordonnée y dans l’espace de coordonnées de la tablette. Chaque paquet contient cette propriété par défaut. L’origine (0,0) de la tablette est l’angle supérieur gauche.<br /> | 
| GUID_Y_TILT_ORIENTATION<br /> | Pour un curseur de stylet, l’orientation de l’inclinaison y est l’angle entre le plan x, z et le plan de l’axe x et du stylet. La valeur est égale à 0 lorsque le stylet est perpendiculaire à la surface de dessin et est positif lorsque le stylet est vers le haut ou à l’extérieur de l’utilisateur.<br /> | 
| GUID_Z<br /> | La coordonnée z ou la distance de la pointe du stylet à partir de la surface du Tablet PC. Le type d’énumération <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> détermine l’unité de mesure de cette propriété. <br /> | 




 

> [!Note]  
> Le champ TangentPressure représente une pression le long du plan de la surface de la tablette. le champ NormalPressure représente une pression perpendiculaire au plan de la surface de la tablette.

 

 

 




