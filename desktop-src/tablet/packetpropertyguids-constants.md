---
description: Définit des valeurs qui spécifient les propriétés du paquet.
ms.assetid: 3e8495f6-0860-4ea8-a258-784eaade85c7
title: Constantes PacketPropertyGuids (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aadb664cb3783932dc2e7063d7cfab07133ad9fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210607"
---
# <a name="packetpropertyguids-constants"></a><span data-ttu-id="4cc0b-103">Constantes PacketPropertyGuids</span><span class="sxs-lookup"><span data-stu-id="4cc0b-103">PacketPropertyGuids Constants</span></span>

<span data-ttu-id="4cc0b-104">Définit des valeurs qui spécifient les propriétés du paquet.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-104">Defines values that specify the packet properties.</span></span> <span data-ttu-id="4cc0b-105">La tablette PCAPI utilise des identificateurs globaux uniques (GUID) pour identifier les propriétés des paquets, qui sont des chaînes constantes dans COM.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-105">The Tablet PCAPI uses globally unique identifiers (GUIDs) to identify packet properties, which in COM are constant strings.</span></span>

<span data-ttu-id="4cc0b-106">En C++, vous pouvez accéder à ces constantes dans le fichier d’en-tête Msinkaut. h, qui se trouve dans le dossier <systemdrive> : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 6.0 \\ include si vous avez installé le kit de développement logiciel (SDK) à l’emplacement par défaut.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-106">In C++, you can access these constants in the Msinkaut.h header file, which is located in the <systemdrive>:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Include directory if you installed the SDK in the default location.</span></span> <span data-ttu-id="4cc0b-107">En C++, ces constantes sont WCHARs, et non BSTR.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-107">In C++, these constants are WCHARs, not BSTRs.</span></span> <span data-ttu-id="4cc0b-108">Convertissez-les en BSTR avant d’utiliser.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-108">Convert them into BSTRs before use.</span></span> <span data-ttu-id="4cc0b-109">Pour plus d’informations sur le type de données BSTR, consultez [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="4cc0b-109">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

<span data-ttu-id="4cc0b-110">Le tableau suivant répertorie les champs de propriété de paquet GUID (globally unique identifier) disponibles.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-110">The following table lists the available packet property globally unique identifier (GUID) fields.</span></span> <span data-ttu-id="4cc0b-111">Utilisez ces GUID pour spécifier les propriétés que le paquet contient lorsque vous créez le contexte de tablette.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-111">Use these GUIDs to specify which properties the packet contains when you create the tablet context.</span></span> <span data-ttu-id="4cc0b-112">Pour déterminer la plage et la résolution d’une propriété, appelez la méthode [**GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) .</span><span class="sxs-lookup"><span data-stu-id="4cc0b-112">To determine the range and resolution of a property, call the [**GetPropertyMetrics**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics) method.</span></span> <span data-ttu-id="4cc0b-113">Les constantes dans le tableau ci-dessous, commençant par « STR \_ », sont des représentations sous forme de chaîne des constantes binaires correspondantes indiquées dans la même cellule de table.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-113">The constants in the table below beginning with "STR\_" are string representations of the corresponding binary constants shown in the same table cell.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="4cc0b-114">Constante</span><span class="sxs-lookup"><span data-stu-id="4cc0b-114">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="4cc0b-115">Description</span><span class="sxs-lookup"><span data-stu-id="4cc0b-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_X_or_GUID_PACKETPROPERTY_GUID_X"></span><span id="str_guid_x_or_guid_packetproperty_guid_x"></span><span id="STR_GUID_X_OR_GUID_PACKETPROPERTY_GUID_X"></span><dl> <span data-ttu-id="4cc0b-116"><dt><strong>STR_GUID_X ou GUID_PACKETPROPERTY_GUID_X</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-116"><dt><strong>STR_GUID_X or GUID_PACKETPROPERTY_GUID_X</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-117">Coordonnée x dans l’espace de coordonnées de la tablette.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-117">The x-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="4cc0b-118">Chaque paquet contient cette propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-118">Each packet contains this property by default.</span></span> <span data-ttu-id="4cc0b-119">L’origine (0,0) de la tablette est l’angle supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-119">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <span data-ttu-id="4cc0b-120"><dt><strong>STR_GUID_Y ou GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-120"><dt><strong>STR_GUID_Y or GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-121">Coordonnée y dans l’espace de coordonnées de la tablette.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-121">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="4cc0b-122">Chaque paquet contient cette propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-122">Each packet contains this property by default.</span></span> <span data-ttu-id="4cc0b-123">L’origine (0,0) de la tablette est l’angle supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-123">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_Y_or_GUID_PACKETPROPERTY_GUID_Y"></span><span id="str_guid_y_or_guid_packetproperty_guid_y"></span><span id="STR_GUID_Y_OR_GUID_PACKETPROPERTY_GUID_Y"></span><dl> <span data-ttu-id="4cc0b-124"><dt><strong>STR_GUID_Y ou GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-124"><dt><strong>STR_GUID_Y or GUID_PACKETPROPERTY_GUID_Y</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-125">Coordonnée y dans l’espace de coordonnées de la tablette.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-125">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="4cc0b-126">Chaque paquet contient cette propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-126">Each packet contains this property by default.</span></span> <span data-ttu-id="4cc0b-127">L’origine (0,0) de la tablette est l’angle supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-127">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_Z_or_GUID_PACKETPROPERTY_GUID_Z"></span><span id="str_guid_z_or_guid_packetproperty_guid_z"></span><span id="STR_GUID_Z_OR_GUID_PACKETPROPERTY_GUID_Z"></span><dl> <span data-ttu-id="4cc0b-128"><dt><strong>STR_GUID_Z ou GUID_PACKETPROPERTY_GUID_Z</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-128"><dt><strong>STR_GUID_Z or GUID_PACKETPROPERTY_GUID_Z</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-129">La coordonnée z ou la distance de la pointe du stylet à partir de la surface du Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-129">The z-coordinate or distance of the pen tip from the tablet surface.</span></span> <span data-ttu-id="4cc0b-130">Le type d’énumération <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit</strong></a> détermine l’unité de mesure de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-130">The <a href="/windows/desktop/api/msinkaut/ne-msinkaut-tabletpropertymetricunit"><strong>TabletPropertyMetricUnit</strong></a> enumeration type determines the unit of measurement for this property.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PAKETSTATUS_or_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><span id="str_guid_paketstatus_or_guid_packetproperty_guid_packet_status"></span><span id="STR_GUID_PAKETSTATUS_OR_GUID_PACKETPROPERTY_GUID_PACKET_STATUS"></span><dl> <span data-ttu-id="4cc0b-131"><dt><strong>STR_GUID_PAKETSTATUS ou GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-131"><dt><strong>STR_GUID_PAKETSTATUS or GUID_PACKETPROPERTY_GUID_PACKET_STATUS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-132">Contient une ou plusieurs des valeurs d’indicateur suivantes :</span><span class="sxs-lookup"><span data-stu-id="4cc0b-132">Contains one or more of the following flag values:</span></span><br/>
<ul>
<li><span data-ttu-id="4cc0b-133">Le curseur touche la surface de dessin (valeur = 1).</span><span class="sxs-lookup"><span data-stu-id="4cc0b-133">The cursor is touching the drawing surface (Value = 1).</span></span></li>
<li><span data-ttu-id="4cc0b-134">Le curseur est inversé.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-134">The cursor is inverted.</span></span> <span data-ttu-id="4cc0b-135">Par exemple, la fin de la gomme du stylet pointe vers la surface (valeur = 2).</span><span class="sxs-lookup"><span data-stu-id="4cc0b-135">For example, the eraser end of the pen is pointing toward the surface (Value = 2).</span></span></li>
<li><span data-ttu-id="4cc0b-136">Non utilisé (valeur = 4).</span><span class="sxs-lookup"><span data-stu-id="4cc0b-136">Not used (Value = 4).</span></span></li>
<li><span data-ttu-id="4cc0b-137">Le bouton en barillet est enfoncé (valeur = 8).</span><span class="sxs-lookup"><span data-stu-id="4cc0b-137">The barrel button is pressed (Value = 8).</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <span data-ttu-id="4cc0b-138"><dt><strong>STR_GUID_TIMERTICK ou GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-138"><dt><strong>STR_GUID_TIMERTICK or GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-139">Heure à laquelle le paquet a été généré.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-139">The time the packet was generated.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_TIMERTICK_or_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><span id="str_guid_timertick_or_guid_packetproperty_guid_timer_tick"></span><span id="STR_GUID_TIMERTICK_OR_GUID_PACKETPROPERTY_GUID_TIMER_TICK"></span><dl> <span data-ttu-id="4cc0b-140"><dt><strong>STR_GUID_TIMERTICK ou GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-140"><dt><strong>STR_GUID_TIMERTICK or GUID_PACKETPROPERTY_GUID_TIMER_TICK</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-141">Heure à laquelle le paquet a été généré.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-141">The time the packet was generated.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_SERIALNUMBER_or_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><span id="str_guid_serialnumber_or_guid_packetproperty_guid_serial_number"></span><span id="STR_GUID_SERIALNUMBER_OR_GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER"></span><dl> <span data-ttu-id="4cc0b-142"><dt><strong>STR_GUID_SERIALNUMBER ou GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-142"><dt><strong>STR_GUID_SERIALNUMBER or GUID_PACKETPROPERTY_GUID_SERIAL_NUMBER</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-143">Propriété de paquet permettant d’identifier le paquet.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-143">The packet property for identifying the packet.</span></span><br/> <span data-ttu-id="4cc0b-144">Il s’agit de la même valeur que celle utilisée pour récupérer le paquet de la file d’attente de paquets.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-144">This is the same value you use to retrieve the packet from the packet queue.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_NORMALPRESSURE_or_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><span id="str_guid_normalpressure_or_guid_packetproperty_guid_normal_pressure"></span><span id="STR_GUID_NORMALPRESSURE_OR_GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE"></span><dl> <span data-ttu-id="4cc0b-145"><dt><strong>STR_GUID_NORMALPRESSURE ou GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-145"><dt><strong>STR_GUID_NORMALPRESSURE or GUID_PACKETPROPERTY_GUID_NORMAL_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-146">Pression de l’extrémité du stylet perpendiculairement à la surface du Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-146">The pressure of the pen tip perpendicular to the tablet surface.</span></span><br/> <span data-ttu-id="4cc0b-147">Plus la pression sur la pointe du stylet est importante, plus l’encre est dessinée.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-147">The greater the pressure on the pen tip, the more ink that is drawn.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TANGENTPRESSURE_or_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><span id="str_guid_tangentpressure_or_guid_packetproperty_guid_tangent_pressure"></span><span id="STR_GUID_TANGENTPRESSURE_OR_GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE"></span><dl> <span data-ttu-id="4cc0b-148"><dt><strong>STR_GUID_TANGENTPRESSURE ou GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-148"><dt><strong>STR_GUID_TANGENTPRESSURE or GUID_PACKETPROPERTY_GUID_TANGENT_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-149">Pression de l’extrémité du stylet le long du plan de la surface de la tablette.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-149">The pressure of the pen tip along the plane of the tablet surface.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_BUTTONPRESSURE_or_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><span id="str_guid_buttonpressure_or_guid_packetproperty_guid_button_pressure"></span><span id="STR_GUID_BUTTONPRESSURE_OR_GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE"></span><dl> <span data-ttu-id="4cc0b-150"><dt><strong>STR_GUID_BUTTONPRESSURE ou GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-150"><dt><strong>STR_GUID_BUTTONPRESSURE or GUID_PACKETPROPERTY_GUID_BUTTON_PRESSURE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-151">Pression sur un bouton sensible à la pression.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-151">The pressure on a pressure sensitive button.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_XTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><span id="str_guid_xtiltorientation_or_guid_packetproperty_guid_x_tilt_orientation"></span><span id="STR_GUID_XTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION"></span><dl> <span data-ttu-id="4cc0b-152"><dt><strong>STR_GUID_XTILTORIENTATION ou GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-152"><dt><strong>STR_GUID_XTILTORIENTATION or GUID_PACKETPROPERTY_GUID_X_TILT_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-153">Angle entre le plan y, le plan z et le plan de l’axe y et du stylet.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-153">The angle between the y,z-plane and the pen and y-axis plane.</span></span><br/> <span data-ttu-id="4cc0b-154">S’applique à un curseur de stylet.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-154">Applies to a pen cursor.</span></span><br/> <span data-ttu-id="4cc0b-155">La valeur est 0 lorsque le stylet est perpendiculaire à la surface de dessin et est positif lorsque le stylet est à droite de Perpendicular.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-155">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YTILTORIENTATION_or_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><span id="str_guid_ytiltorientation_or_guid_packetproperty_guid_y_tilt_orientation"></span><span id="STR_GUID_YTILTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION"></span><dl> <span data-ttu-id="4cc0b-156"><dt><strong>STR_GUID_YTILTORIENTATION ou GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-156"><dt><strong>STR_GUID_YTILTORIENTATION or GUID_PACKETPROPERTY_GUID_Y_TILT_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-157">Angle entre le plan x, z et le plan de l’axe x et du stylet.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-157">The angle between the x,z-plane and the pen and x-axis plane.</span></span><br/> <span data-ttu-id="4cc0b-158">S’applique à un curseur de stylet.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-158">Applies to a pen cursor.</span></span><br/> <span data-ttu-id="4cc0b-159">La valeur est 0 lorsque le stylet est perpendiculaire à la surface de dessin et est positif lorsque le stylet est vers le haut ou l’extérieur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-159">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is upward or away from the user.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_AZIMUTHORIENTATION_or_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><span id="str_guid_azimuthorientation_or_guid_packetproperty_guid_azimuth_orientation"></span><span id="STR_GUID_AZIMUTHORIENTATION_OR_GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION"></span><dl> <span data-ttu-id="4cc0b-160"><dt><strong>STR_GUID_AZIMUTHORIENTATION ou GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-160"><dt><strong>STR_GUID_AZIMUTHORIENTATION or GUID_PACKETPROPERTY_GUID_AZIMUTH_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-161">Rotation dans le sens des aiguilles d’une montre autour de l’axe z dans une plage circulaire complète.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-161">The clockwise rotation of the cursor about the z-axis through a full circular range.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_ALTITUDEORIENTATION_or_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><span id="str_guid_altitudeorientation_or_guid_packetproperty_guid_altitude_orientation"></span><span id="STR_GUID_ALTITUDEORIENTATION_OR_GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION"></span><dl> <span data-ttu-id="4cc0b-162"><dt><strong>STR_GUID_ALTITUDEORIENTATION ou GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-162"><dt><strong>STR_GUID_ALTITUDEORIENTATION or GUID_PACKETPROPERTY_GUID_ALTITUDE_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-163">Angle entre l’axe du stylet et la surface de la tablette.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-163">The angle between the axis of the pen and the surface of the tablet.</span></span><br/> <span data-ttu-id="4cc0b-164">La valeur est 0 lorsque le stylet est parallèle à la surface et 90 lorsque le stylet est perpendiculaire à la surface.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-164">The value is 0 when the pen is parallel to the surface and 90 when the pen is perpendicular to the surface.</span></span><br/> <span data-ttu-id="4cc0b-165">Les valeurs sont négatives lorsque le stylet est inversé.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-165">The values are negative when the pen is inverted.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_TWISTORIENTATION_or_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><span id="str_guid_twistorientation_or_guid_packetproperty_guid_twist_orientation"></span><span id="STR_GUID_TWISTORIENTATION_OR_GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION"></span><dl> <span data-ttu-id="4cc0b-166"><dt><strong>STR_GUID_TWISTORIENTATION ou GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-166"><dt><strong>STR_GUID_TWISTORIENTATION or GUID_PACKETPROPERTY_GUID_TWIST_ORIENTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-167">Rotation dans le sens des aiguilles d’une montre autour de son propre axe.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-167">The clockwise rotation of the cursor about its own axis.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_PITCHROTATION_or_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><span id="str_guid_pitchrotation_or_guid_packetproperty_guid_pitch_rotation"></span><span id="STR_GUID_PITCHROTATION_OR_GUID_PACKETPROPERTY_GUID_PITCH_ROTATION"></span><dl> <span data-ttu-id="4cc0b-168"><dt><strong>STR_GUID_PITCHROTATION ou GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-168"><dt><strong>STR_GUID_PITCHROTATION or GUID_PACKETPROPERTY_GUID_PITCH_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-169">Propriété de paquet qui indique si l’info-bulle se trouve au-dessus ou en dessous d’une ligne horizontale perpendiculaire à la surface d’écriture.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-169">The packet property that indicates whether the tip is above or below a horizontal line that is perpendicular to the writing surface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4cc0b-170">Cela nécessite un digitaliseur 3D.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-170">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="4cc0b-171">La valeur est positive si l’info-bulle se trouve au-dessus de la ligne et est négative si elle est inférieure à la ligne.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-171">The value is positive if the tip is above the line and negative if it is below the line.</span></span> <span data-ttu-id="4cc0b-172">Par exemple, si vous tenez le stylet devant vous et écrivez sur un mur imaginaire, le pas est positif si le Conseil se trouve au-dessus d’une ligne qui s’étend de vous au mur.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-172">For example, if you hold the pen in front of you and write on an imaginary wall, the pitch is positive if the tip is above a line extending from you to the wall.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_ROLLROTATION_or_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><span id="str_guid_rollrotation_or_guid_packetproperty_guid_roll_rotation"></span><span id="STR_GUID_ROLLROTATION_OR_GUID_PACKETPROPERTY_GUID_ROLL_ROTATION"></span><dl> <span data-ttu-id="4cc0b-173"><dt><strong>STR_GUID_ROLLROTATION ou GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-173"><dt><strong>STR_GUID_ROLLROTATION or GUID_PACKETPROPERTY_GUID_ROLL_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-174">Rotation du stylet dans le sens horaire autour de son axe.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-174">The clockwise rotation of the pen around its own axis.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4cc0b-175">Cela nécessite un digitaliseur 3D.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-175">This requires a 3D digitizer.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <span data-ttu-id="4cc0b-176"><dt><strong>STR_GUID_YAWROTATION ou GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-176"><dt><strong>STR_GUID_YAWROTATION or GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-177">Angle du stylet vers la gauche ou vers la droite autour du centre de son axe horizontal lorsque le stylet est horizontal.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-177">The angle of the pen to the left or right around the center of its horizontal axis when the pen is horizontal.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4cc0b-178">Cela nécessite un digitaliseur 3D.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-178">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="4cc0b-179">Si vous maintenez le stylet devant vous et écrivez sur un mur imaginaire, le lacet zéro indique que le stylet est perpendiculaire au mur.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-179">If you hold the pen in front of you and write on an imaginary wall, zero yaw indicates that the pen is perpendicular to the wall.</span></span> <span data-ttu-id="4cc0b-180">La valeur est négative si l’info-bulle est à gauche de la perpendiculaire et positive si l’embout est à droite de Perpendicular.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-180">The value is negative if the tip is to the left of perpendicular and positive if the tip is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_YAWROTATION_or_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><span id="str_guid_yawrotation_or_guid_packetproperty_guid_yaw_rotation"></span><span id="STR_GUID_YAWROTATION_OR_GUID_PACKETPROPERTY_GUID_YAW_ROTATION"></span><dl> <span data-ttu-id="4cc0b-181"><dt><strong>STR_GUID_YAWROTATION ou GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-181"><dt><strong>STR_GUID_YAWROTATION or GUID_PACKETPROPERTY_GUID_YAW_ROTATION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-182">Angle du stylet vers la gauche ou vers la droite autour du centre de son axe horizontal lorsque le stylet est horizontal.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-182">The angle of the pen to the left or right around the center of its horizontal axis when the pen is horizontal.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="4cc0b-183">Cela nécessite un digitaliseur 3D.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-183">This requires a 3D digitizer.</span></span>
</blockquote>
<br/> <span data-ttu-id="4cc0b-184">Si vous maintenez le stylet devant vous et écrivez sur un mur imaginaire, le lacet zéro indique que le stylet est perpendiculaire au mur.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-184">If you hold the pen in front of you and write on an imaginary wall, zero yaw indicates that the pen is perpendicular to the wall.</span></span> <span data-ttu-id="4cc0b-185">La valeur est négative si l’info-bulle est à gauche de la perpendiculaire et positive si l’embout est à droite de Perpendicular.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-185">The value is negative if the tip is to the left of perpendicular and positive if the tip is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_WIDTH_or_GUID_PACKETPROPERTY_GUID_WIDTH"></span><span id="str_guid_width_or_guid_packetproperty_guid_width"></span><span id="STR_GUID_WIDTH_OR_GUID_PACKETPROPERTY_GUID_WIDTH"></span><dl> <span data-ttu-id="4cc0b-186"><dt><strong>STR_GUID_WIDTH ou GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-186"><dt><strong>STR_GUID_WIDTH or GUID_PACKETPROPERTY_GUID_WIDTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-187">Largeur de la zone de contact sur un digitaliseur tactile.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-187">The width of the contact area on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_HEIGHT_or_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><span id="str_guid_height_or_guid_packetproperty_guid_height"></span><span id="STR_GUID_HEIGHT_OR_GUID_PACKETPROPERTY_GUID_HEIGHT"></span><dl> <span data-ttu-id="4cc0b-188"><dt><strong>STR_GUID_HEIGHT ou GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-188"><dt><strong>STR_GUID_HEIGHT or GUID_PACKETPROPERTY_GUID_HEIGHT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-189">Hauteur de la zone de contact sur un digitaliseur tactile.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-189">The height of the contact area on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="STR_GUID_FINGERCONTACTCONFIDENCE_or_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><span id="str_guid_fingercontactconfidence_or_guid_packetproperty_guid_fingercontactconfidence"></span><span id="STR_GUID_FINGERCONTACTCONFIDENCE_OR_GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE"></span><dl> <span data-ttu-id="4cc0b-190"><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE ou GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-190"><dt><strong>STR_GUID_FINGERCONTACTCONFIDENCE or GUID_PACKETPROPERTY_GUID_FINGERCONTACTCONFIDENCE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-191">Le niveau de confiance d’un contact Finger sur un digitaliseur tactile.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-191">The level of confidence that there was finger contact on a touch digitizer.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="STR_GUID_DEVICE_CONTACT_ID_or_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><span id="str_guid_device_contact_id_or_guid_packetproperty_guid_device_contact_id"></span><span id="STR_GUID_DEVICE_CONTACT_ID_OR_GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID"></span><dl> <span data-ttu-id="4cc0b-192"><dt><strong>STR_GUID_DEVICE_CONTACT_ID ou GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4cc0b-192"><dt><strong>STR_GUID_DEVICE_CONTACT_ID or GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="4cc0b-193">Identificateur de contact de l’appareil pour un paquet.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-193">The device contact identifier for a packet.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="4cc0b-194">Notes</span><span class="sxs-lookup"><span data-stu-id="4cc0b-194">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4cc0b-195">Toutes les valeurs de paquets provenant du matériel de tablette sont des entiers de taille 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-195">All packet values coming from the tablet hardware are 32-bit size integers.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4cc0b-196">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4cc0b-196">Requirements</span></span>



| <span data-ttu-id="4cc0b-197">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4cc0b-197">Requirement</span></span> | <span data-ttu-id="4cc0b-198">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cc0b-198">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cc0b-199">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cc0b-199">Minimum supported client</span></span><br/> | <span data-ttu-id="4cc0b-200">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4cc0b-200">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="4cc0b-201">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cc0b-201">Minimum supported server</span></span><br/> | <span data-ttu-id="4cc0b-202">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cc0b-202">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="4cc0b-203">En-tête</span><span class="sxs-lookup"><span data-stu-id="4cc0b-203">Header</span></span><br/>                   | <dl> <span data-ttu-id="4cc0b-204"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="4cc0b-204"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cc0b-205">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cc0b-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cc0b-206">**Méthode IsPacketPropertySupported**</span><span class="sxs-lookup"><span data-stu-id="4cc0b-206">**IsPacketPropertySupported Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-ispacketpropertysupported)
</dt> <dt>

[<span data-ttu-id="4cc0b-207">**Méthode GetPropertyMetrics**</span><span class="sxs-lookup"><span data-stu-id="4cc0b-207">**GetPropertyMetrics Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablet-getpropertymetrics)
</dt> <dt>

[<span data-ttu-id="4cc0b-208">**Interface IInkTablet**</span><span class="sxs-lookup"><span data-stu-id="4cc0b-208">**IInkTablet Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet)
</dt> </dl>

 

 




