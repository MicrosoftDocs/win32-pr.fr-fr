---
description: Le tableau suivant répertorie les GUID de propriété de paquet utilisés par la structure de propriété de paquet \_ .
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: GUID PacketProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fb7db9f2d5e05000bdccd5a09b2b799f38aa1bb692fea110ea153a57912cfc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449369"
---
# <a name="packetproperty-guids"></a>GUID PacketProperty

Le tableau suivant répertorie les GUID de propriété de paquet utilisés par la structure de [**\_ propriété de paquet**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GUID_ALTITUDE_ORIENTATION<br/></td>
<td>Angle entre l’axe du stylet et la surface de la tablette. La valeur est 0 lorsque le stylet est parallèle à la surface et 90 lorsque le stylet est perpendiculaire à la surface. Les valeurs sont négatives lorsque le stylet est inversé.<br/></td>
</tr>
<tr class="even">
<td>GUID_AZIMUTH_ORIENTATION<br/></td>
<td>Rotation dans le sens des aiguilles d’une montre autour de l’axe z dans une plage circulaire complète.<br/></td>
</tr>
<tr class="odd">
<td>GUID_BOXNUMBER<br/></td>
<td>GUID utilisé pour récupérer le numéro de zone d’un autre module de reconnaissance de l’encre lorsque le module de reconnaissance fonctionne en mode Box.<br/></td>
</tr>
<tr class="even">
<td>GUID_BUTTON_PRESSURE<br/></td>
<td>Pression sur un bouton sensible à la pression.<br/></td>
</tr>
<tr class="odd">
<td>GUID_NORMAL_PRESSURE<br/></td>
<td>GUID de l’objet PacketProperty qui représente la pression de l’extrémité du stylet perpendiculairement à la surface du Tablet PC. Plus la pression placée sur la pointe du stylet est importante, plus l’encre est dessinée.<br/></td>
</tr>
<tr class="even">
<td>GUID_PACKET_STATUS<br/></td>
<td>Contient une ou plusieurs des valeurs d’indicateur suivantes :<br/>
<ul>
<li>Le curseur touche la surface de dessin (valeur = 1).</li>
<li>Le curseur est inversé. Par exemple, la fin de la gomme du stylet pointe vers la surface (valeur = 2).</li>
<li>Non utilisé (valeur = 4).</li>
<li>Le bouton en barillet est enfoncé (valeur = 8).</li>
</ul></td>
</tr>
<tr class="odd">
<td>GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID<br/></td>
<td>Identificateur de contact de l’appareil pour un paquet.<br/></td>
</tr>
<tr class="even">
<td>GUID_SERIAL_NUMBER<br/></td>
<td>Identifie le paquet. Il s’agit de la même valeur que celle utilisée pour récupérer le paquet de la file d’attente de paquets.<br/></td>
</tr>
<tr class="odd">
<td>GUID_TANGENT_PRESSURE<br/></td>
<td>GUID de l’objet PacketProperty qui représente la pression de l’extrémité du stylet le long du plan de la surface de la tablette.<br/></td>
</tr>
<tr class="even">
<td>GUID_TIMER_TICK<br/></td>
<td>Heure de génération du paquet.<br/></td>
</tr>
<tr class="odd">
<td>GUID_TWIST_ORIENTATION<br/></td>
<td>Rotation du curseur dans le sens horaire autour de son axe.<br/></td>
</tr>
<tr class="even">
<td>GUID_X<br/></td>
<td>Coordonnée x dans l’espace de coordonnées de la tablette. Chaque paquet contient cette propriété par défaut. L’origine (0,0) de la tablette est l’angle supérieur gauche.<br/></td>
</tr>
<tr class="odd">
<td>GUID_X_TILT_ORIENTATION<br/></td>
<td>Pour un curseur de stylet, l’orientation de l’inclinaison x est l’angle entre le plan y, le plan z et le plan de l’axe y et du stylet. La valeur est 0 lorsque le stylet est perpendiculaire à la surface de dessin et est positif lorsque le stylet est à droite de Perpendicular.<br/></td>
</tr>
<tr class="even">
<td>GUID_Y<br/></td>
<td>Coordonnée y dans l’espace de coordonnées de la tablette. Chaque paquet contient cette propriété par défaut. L’origine (0,0) de la tablette est l’angle supérieur gauche.<br/></td>
</tr>
<tr class="odd">
<td>GUID_Y_TILT_ORIENTATION<br/></td>
<td>Pour un curseur de stylet, l’orientation de l’inclinaison y est l’angle entre le plan x, z et le plan de l’axe x et du stylet. La valeur est égale à 0 lorsque le stylet est perpendiculaire à la surface de dessin et est positif lorsque le stylet est vers le haut ou à l’extérieur de l’utilisateur.<br/></td>
</tr>
<tr class="even">
<td>GUID_Z<br/></td>
<td>La coordonnée z ou la distance de la pointe du stylet à partir de la surface du Tablet PC. Le type d’énumération <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> détermine l’unité de mesure de cette propriété. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Le champ TangentPressure représente une pression le long du plan de la surface de la tablette. le champ NormalPressure représente une pression perpendiculaire au plan de la surface de la tablette.

 

 

 




