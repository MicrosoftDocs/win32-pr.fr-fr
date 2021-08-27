---
description: Définit des valeurs qui spécifient les propriétés du paquet.
ms.assetid: 3e8495f6-0860-4ea8-a258-784eaade85c7
title: Constantes PacketPropertyGuids (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9eb946b170b1004deea7eb1f2faafeee5bc5dba
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884508"
---
# <a name="packetpropertyguids-constants"></a>Constantes PacketPropertyGuids

Définit des valeurs qui spécifient les propriétés du paquet. La tablette PCAPI utilise des identificateurs globaux uniques (GUID) pour identifier les propriétés des paquets, qui sont des chaînes constantes dans COM.

en C++, vous pouvez accéder à ces constantes dans le fichier d’en-tête Msinkaut. h, qui se trouve dans le &lt; &gt; répertoire lecteur_système : \\ Program Files \\ Microsoft sdk \\ Windows \\ v 6.0 \\ include si vous avez installé le kit de développement logiciel (sdk) à l’emplacement par défaut. En C++, ces constantes sont WCHARs, et non BSTR. Convertissez-les en BSTR avant d’utiliser. Pour plus d’informations sur le type de données BSTR, consultez [utilisation de la bibliothèque com](using-the-com-library.md).

Le tableau suivant répertorie les champs de propriété de paquet GUID (globally unique identifier) disponibles. Utilisez ces GUID pour spécifier les propriétés que le paquet contient lorsque vous créez le contexte de tablette. Pour déterminer la plage et la résolution d’une propriété, appelez la méthode [**GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) . Les constantes dans le tableau ci-dessous, commençant par « STR \_ », sont des représentations sous forme de chaîne des constantes binaires correspondantes indiquées dans la même cellule de table.




| Constante | Description | 
|----------|-------------|
| <span id="STR_GUID_X_or_GUID_PACKETPROPERTY_GUID_X"></span><span id="str_guid_x_or_guid_packetproperty_guid_x"></span><span id="STR_GUID_X_OR_GUID_PACKETPROPERTY_GUID_X"></span><dl><dt><strong>STR_GUID_X ou GUID_PACKETPROPERTY_GUID_X</strong></dt></dl> | Coordonnée x dans l’espace de coordonnées de la tablette. Chaque paquet contient cette propriété par défaut. L’origine (0,0) de la tablette est l’angle supérieur gauche.<br /> | 
| <span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl><dt><strong>STR_GUID_Y ou GUID_PACKETPROPERTY_GUID_Y</strong></dt></dl> | Coordonnée y dans l’espace de coordonnées de la tablette. Chaque paquet contient cette propriété par défaut. L’origine (0,0) de la tablette est l’angle supérieur gauche.<br /> | 
| <span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl><dt><strong>STR_GUID_Y ou GUID_PACKETPROPERTY_GUID_Y</strong></dt></dl> | Coordonnée y dans l’espace de coordonnées de la tablette. Chaque paquet contient cette propriété par défaut. L’origine (0,0) de la tablette est l’angle supérieur gauche.<br /> | 
| <span id="STR_GUID_Z_or_GUID_PACKETPROPERTY_GUID_Z"></span><span id="str_guid_z_or_guid_packetproperty_guid_z"></span><span id="STR_GUID_Z_OR_GUID_PACKETPROPERTY_GUID_Z"></span><dl><dt><strong>STR_GUID_Z ou GUID_PACKETPROPERTY_GUID_Z</strong></dt></dl> | La coordonnée z ou la distance de la pointe du stylet à partir de la surface du Tablet PC. Le type d’énumération <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit</strong></a> détermine l’unité de mesure de cette propriété.<br /> | 
| <span id="STR_GUID_PAKETSTATUS_or_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><span id="str_guid_paketstatus_or_guid_packetproperty_guid_packet_status"></span><span id="STR_GUID_PAKETSTATUS_OR_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><dl><dt><strong>STR_GUID_PAKETSTATUS ou GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt></dl> | Contient une ou plusieurs des valeurs d’indicateur suivantes :<br /><ul><li>Le curseur touche la surface de dessin (valeur = 1).</li><li>Le curseur est inversé. Par exemple, la fin de la gomme du stylet pointe vers la surface (valeur = 2).</li><li>Non utilisé (valeur = 4).</li><li>Le bouton en barillet est enfoncé (valeur = 8).</li></ul> | 
| <span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl><dt><strong>STR_GUID_TIMERTICK ou GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt></dl> | Heure à laquelle le paquet a été généré.<br /> | 
| <span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl><dt><strong>STR_GUID_TIMERTICK ou GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt></dl> | Heure à laquelle le paquet a été généré.<br /> | 
| <span id="STR_GUID_SERIALNUMBER_or_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><span id="str_guid_serialnumber_or_guid_packetproperty_guid_serial_number"></span><span id="STR_GUID_SERIALNUMBER_OR_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><dl><dt><strong>STR_GUID_SERIALNUMBER ou GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt></dl> | Propriété de paquet permettant d’identifier le paquet.<br /> Il s’agit de la même valeur que celle utilisée pour récupérer le paquet de la file d’attente de paquets.<br /> | 
| <span id="STR_GUID_NORMALPRESSURE_or_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><span id="str_guid_normalpressure_or_guid_packetproperty_guid_normal_pressure"></span><span id="STR_GUID_NORMALPRESSURE_OR_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><dl><dt><strong>STR_GUID_NORMALPRESSURE ou GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt></dl> | Pression de l’extrémité du stylet perpendiculairement à la surface du Tablet PC.<br /> Plus la pression sur la pointe du stylet est importante, plus l’encre est dessinée.<br /> | 
| <span id="STR_GUID_TANGENTPRESSURE_or_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><span id="str_guid_tangentpressure_or_guid_packetproperty_guid_tangent_pressure"></span><span id="STR_GUID_TANGENTPRESSURE_OR_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><dl><dt><strong>STR_GUID_TANGENTPRESSURE ou GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt></dl> | Pression de l’extrémité du stylet le long du plan de la surface de la tablette.<br /> | 
| <span id="STR_GUID_BUTTONPRESSURE_or_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><span id="str_guid_buttonpressure_or_guid_packetproperty_guid_button_pressure"></span><span id="STR_GUID_BUTTONPRESSURE_OR_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><dl><dt><strong>STR_GUID_BUTTONPRESSURE ou GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt></dl> | Pression sur un bouton sensible à la pression.<br /> | 
| <span id="STR_GUID_XTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><span id="str_guid_xtiltorientation_or_guid_packetproperty_guid_x_tilt_orientation"></span><span id="STR_GUID_XTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><dl><dt><strong>STR_GUID_XTILTORIENTATION ou GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt></dl> | Angle entre le plan y, le plan z et le plan de l’axe y et du stylet.<br /> S’applique à un curseur de stylet.<br /> La valeur est 0 lorsque le stylet est perpendiculaire à la surface de dessin et est positif lorsque le stylet est à droite de Perpendicular.<br /> | 
| <span id="STR_GUID_YTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><span id="str_guid_ytiltorientation_or_guid_packetproperty_guid_y_tilt_orientation"></span><span id="STR_GUID_YTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><dl><dt><strong>STR_GUID_YTILTORIENTATION ou GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt></dl> | Angle entre le plan x, z et le plan de l’axe x et du stylet.<br /> S’applique à un curseur de stylet.<br /> La valeur est 0 lorsque le stylet est perpendiculaire à la surface de dessin et est positif lorsque le stylet est vers le haut ou l’extérieur de l’utilisateur.<br /> | 
| <span id="STR_GUID_AZIMUTHORIENTATION_or_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><span id="str_guid_azimuthorientation_or_guid_packetproperty_guid_azimuth_orientation"></span><span id="STR_GUID_AZIMUTHORIENTATION_OR_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><dl><dt><strong>STR_GUID_AZIMUTHORIENTATION ou GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt></dl> | Rotation dans le sens des aiguilles d’une montre autour de l’axe z dans une plage circulaire complète.<br /> | 
| <span id="STR_GUID_ALTITUDEORIENTATION_or_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><span id="str_guid_altitudeorientation_or_guid_packetproperty_guid_altitude_orientation"></span><span id="STR_GUID_ALTITUDEORIENTATION_OR_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><dl><dt><strong>STR_GUID_ALTITUDEORIENTATION ou GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt></dl> | Angle entre l’axe du stylet et la surface de la tablette.<br /> La valeur est 0 lorsque le stylet est parallèle à la surface et 90 lorsque le stylet est perpendiculaire à la surface.<br /> Les valeurs sont négatives lorsque le stylet est inversé.<br /> | 
| <span id="STR_GUID_TWISTORIENTATION_or_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><span id="str_guid_twistorientation_or_guid_packetproperty_guid_twist_orientation"></span><span id="STR_GUID_TWISTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><dl><dt><strong>STR_GUID_TWISTORIENTATION ou GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt></dl> | Rotation dans le sens des aiguilles d’une montre autour de son propre axe.<br /> | 
| <span id="STR_GUID_PITCHROTATION_or_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><span id="str_guid_pitchrotation_or_guid_packetproperty_guid_pitch_rotation"></span><span id="STR_GUID_PITCHROTATION_OR_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><dl><dt><strong>STR_GUID_PITCHROTATION ou GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt></dl> | Propriété de paquet qui indique si l’info-bulle se trouve au-dessus ou en dessous d’une ligne horizontale perpendiculaire à la surface d’écriture.<br /><blockquote>[!Note]<br />Cela nécessite un digitaliseur 3D.</blockquote><br /> La valeur est positive si l’info-bulle se trouve au-dessus de la ligne et est négative si elle est inférieure à la ligne. Par exemple, si vous tenez le stylet devant vous et écrivez sur un mur imaginaire, le pas est positif si le Conseil se trouve au-dessus d’une ligne qui s’étend de vous au mur.<br /> | 
| <span id="STR_GUID_ROLLROTATION_or_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><span id="str_guid_rollrotation_or_guid_packetproperty_guid_roll_rotation"></span><span id="STR_GUID_ROLLROTATION_OR_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><dl><dt><strong>STR_GUID_ROLLROTATION ou GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt></dl> | Rotation du stylet dans le sens horaire autour de son axe. <br /><blockquote>[!Note]<br />Cela nécessite un digitaliseur 3D.</blockquote><br /> | 
| <span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl><dt><strong>STR_GUID_YAWROTATION ou GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt></dl> | Angle du stylet vers la gauche ou vers la droite autour du centre de son axe horizontal lorsque le stylet est horizontal.<br /><blockquote>[!Note]<br />Cela nécessite un digitaliseur 3D.</blockquote><br /> Si vous maintenez le stylet devant vous et écrivez sur un mur imaginaire, le lacet zéro indique que le stylet est perpendiculaire au mur. La valeur est négative si l’info-bulle est à gauche de la perpendiculaire et positive si l’embout est à droite de Perpendicular.<br /> | 
| <span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl><dt><strong>STR_GUID_YAWROTATION ou GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt></dl> | Angle du stylet vers la gauche ou vers la droite autour du centre de son axe horizontal lorsque le stylet est horizontal.<br /><blockquote>[!Note]<br />Cela nécessite un digitaliseur 3D.</blockquote><br /> Si vous maintenez le stylet devant vous et écrivez sur un mur imaginaire, le lacet zéro indique que le stylet est perpendiculaire au mur. La valeur est négative si l’info-bulle est à gauche de la perpendiculaire et positive si l’embout est à droite de Perpendicular.<br /> | 
| <span id="STR_GUID_WIDTH_or_GUID_PACKETPROPERTY_GUID_WIDTH"></span><span id="str_guid_width_or_guid_packetproperty_guid_width"></span><span id="STR_GUID_WIDTH_OR_GUID_PACKETPROPERTY_GUID_WIDTH"></span><dl><dt><strong>STR_GUID_WIDTH ou GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt></dl> | Largeur de la zone de contact sur un digitaliseur tactile.<br /> | 
| <span id="STR_GUID_HEIGHT_or_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><span id="str_guid_height_or_guid_packetproperty_guid_height"></span><span id="STR_GUID_HEIGHT_OR_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><dl><dt><strong>STR_GUID_HEIGHT ou GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt></dl> | Hauteur de la zone de contact sur un digitaliseur tactile.<br /> | 
| <span id="STR_GUID_FINGERCONTACTCONFIDENCE_or_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><span id="str_guid_fingercontactconfidence_or_guid_packetproperty_guid_fingercontactconfidence"></span><span id="STR_GUID_FINGERCONTACTCONFIDENCE_OR_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><dl><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE ou GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt></dl> | Le niveau de confiance d’un contact Finger sur un digitaliseur tactile.<br /> | 
| <span id="STR_GUID_DEVICE_CONTACT_ID_or_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><span id="str_guid_device_contact_id_or_guid_packetproperty_guid_device_contact_id"></span><span id="STR_GUID_DEVICE_CONTACT_ID_OR_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><dl><dt><strong>STR_GUID_DEVICE_CONTACT_ID ou GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt></dl> | Identificateur de contact de l’appareil pour un paquet.<br /> | 




## <a name="remarks"></a>Remarques

> [!Note]  
> Toutes les valeurs de paquets provenant du matériel de tablette sont des entiers de taille 32 bits.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Méthode IsPacketPropertySupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-ispacketpropertysupported)
</dt> <dt>

[**Méthode GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics)
</dt> <dt>

[**Interface IInkTablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




