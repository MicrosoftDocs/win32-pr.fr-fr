---
description: Le tableau suivant répertorie les GUID de propriété de paquet utilisés par la structure de propriété de paquet \_ .
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: GUID PacketProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94591ccda5cd1f40b79c5cbb4fe80ca3ef99d2e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868929"
---
# <a name="packetproperty-guids"></a><span data-ttu-id="21544-103">GUID PacketProperty</span><span class="sxs-lookup"><span data-stu-id="21544-103">PacketProperty GUIDs</span></span>

<span data-ttu-id="21544-104">Le tableau suivant répertorie les GUID de propriété de paquet utilisés par la structure de [**\_ propriété de paquet**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) .</span><span class="sxs-lookup"><span data-stu-id="21544-104">The following table lists packet property GUIDs used by the [**PACKET\_PROPERTY**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property) structure.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="21544-105">GUID</span><span class="sxs-lookup"><span data-stu-id="21544-105">GUID</span></span></th>
<th><span data-ttu-id="21544-106">Description</span><span class="sxs-lookup"><span data-stu-id="21544-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="21544-107">GUID_ALTITUDE_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="21544-107">GUID_ALTITUDE_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="21544-108">Angle entre l’axe du stylet et la surface de la tablette.</span><span class="sxs-lookup"><span data-stu-id="21544-108">Angle between the axis of the pen and the surface of the tablet.</span></span> <span data-ttu-id="21544-109">La valeur est 0 lorsque le stylet est parallèle à la surface et 90 lorsque le stylet est perpendiculaire à la surface.</span><span class="sxs-lookup"><span data-stu-id="21544-109">The value is 0 when the pen is parallel to the surface and 90 when the pen is perpendicular to the surface.</span></span> <span data-ttu-id="21544-110">Les valeurs sont négatives lorsque le stylet est inversé.</span><span class="sxs-lookup"><span data-stu-id="21544-110">The values are negative when the pen is inverted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21544-111">GUID_AZIMUTH_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="21544-111">GUID_AZIMUTH_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="21544-112">Rotation dans le sens des aiguilles d’une montre autour de l’axe z dans une plage circulaire complète.</span><span class="sxs-lookup"><span data-stu-id="21544-112">Clockwise rotation of the cursor around the z-axis through a full circular range.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21544-113">GUID_BOXNUMBER</span><span class="sxs-lookup"><span data-stu-id="21544-113">GUID_BOXNUMBER</span></span><br/></td>
<td><span data-ttu-id="21544-114">GUID utilisé pour récupérer le numéro de zone d’un autre module de reconnaissance de l’encre lorsque le module de reconnaissance fonctionne en mode Box.</span><span class="sxs-lookup"><span data-stu-id="21544-114">The GUID that is used to retrieve the box number for an ink recognition alternate when the recognizer is operating in box mode.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21544-115">GUID_BUTTON_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="21544-115">GUID_BUTTON_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="21544-116">Pression sur un bouton sensible à la pression.</span><span class="sxs-lookup"><span data-stu-id="21544-116">Pressure on a pressure-sensitive button.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21544-117">GUID_NORMAL_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="21544-117">GUID_NORMAL_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="21544-118">GUID de l’objet PacketProperty qui représente la pression de l’extrémité du stylet perpendiculairement à la surface du Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="21544-118">The GUID for the PacketProperty object that represents pressure of the pen tip perpendicular to the tablet surface.</span></span> <span data-ttu-id="21544-119">Plus la pression placée sur la pointe du stylet est importante, plus l’encre est dessinée.</span><span class="sxs-lookup"><span data-stu-id="21544-119">The greater the pressure put on the pen tip, the more ink that is drawn.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21544-120">GUID_PACKET_STATUS</span><span class="sxs-lookup"><span data-stu-id="21544-120">GUID_PACKET_STATUS</span></span><br/></td>
<td><span data-ttu-id="21544-121">Contient une ou plusieurs des valeurs d’indicateur suivantes :</span><span class="sxs-lookup"><span data-stu-id="21544-121">Contains one or more of the following flag values:</span></span><br/>
<ul>
<li><span data-ttu-id="21544-122">Le curseur touche la surface de dessin (valeur = 1).</span><span class="sxs-lookup"><span data-stu-id="21544-122">The cursor is touching the drawing surface (Value = 1).</span></span></li>
<li><span data-ttu-id="21544-123">Le curseur est inversé.</span><span class="sxs-lookup"><span data-stu-id="21544-123">The cursor is inverted.</span></span> <span data-ttu-id="21544-124">Par exemple, la fin de la gomme du stylet pointe vers la surface (valeur = 2).</span><span class="sxs-lookup"><span data-stu-id="21544-124">For example, the eraser end of the pen is pointing toward the surface (Value = 2).</span></span></li>
<li><span data-ttu-id="21544-125">Non utilisé (valeur = 4).</span><span class="sxs-lookup"><span data-stu-id="21544-125">Not used (Value = 4).</span></span></li>
<li><span data-ttu-id="21544-126">Le bouton en barillet est enfoncé (valeur = 8).</span><span class="sxs-lookup"><span data-stu-id="21544-126">The barrel button is pressed (Value = 8).</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21544-127">GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</span><span class="sxs-lookup"><span data-stu-id="21544-127">GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID</span></span><br/></td>
<td><span data-ttu-id="21544-128">Identificateur de contact de l’appareil pour un paquet.</span><span class="sxs-lookup"><span data-stu-id="21544-128">The device contact identifier for a packet.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21544-129">GUID_SERIAL_NUMBER</span><span class="sxs-lookup"><span data-stu-id="21544-129">GUID_SERIAL_NUMBER</span></span><br/></td>
<td><span data-ttu-id="21544-130">Identifie le paquet.</span><span class="sxs-lookup"><span data-stu-id="21544-130">Identifies the packet.</span></span> <span data-ttu-id="21544-131">Il s’agit de la même valeur que celle utilisée pour récupérer le paquet de la file d’attente de paquets.</span><span class="sxs-lookup"><span data-stu-id="21544-131">This is the same value you use to retrieve the packet from the packet queue.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21544-132">GUID_TANGENT_PRESSURE</span><span class="sxs-lookup"><span data-stu-id="21544-132">GUID_TANGENT_PRESSURE</span></span><br/></td>
<td><span data-ttu-id="21544-133">GUID de l’objet PacketProperty qui représente la pression de l’extrémité du stylet le long du plan de la surface de la tablette.</span><span class="sxs-lookup"><span data-stu-id="21544-133">The GUID for the PacketProperty object that represents pressure of the pen tip along the plane of the tablet surface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21544-134">GUID_TIMER_TICK</span><span class="sxs-lookup"><span data-stu-id="21544-134">GUID_TIMER_TICK</span></span><br/></td>
<td><span data-ttu-id="21544-135">Heure de génération du paquet.</span><span class="sxs-lookup"><span data-stu-id="21544-135">Time the packet was generated.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21544-136">GUID_TWIST_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="21544-136">GUID_TWIST_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="21544-137">Rotation du curseur dans le sens horaire autour de son axe.</span><span class="sxs-lookup"><span data-stu-id="21544-137">Clockwise rotation of the cursor around its own axis.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21544-138">GUID_X</span><span class="sxs-lookup"><span data-stu-id="21544-138">GUID_X</span></span><br/></td>
<td><span data-ttu-id="21544-139">Coordonnée x dans l’espace de coordonnées de la tablette.</span><span class="sxs-lookup"><span data-stu-id="21544-139">The x-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="21544-140">Chaque paquet contient cette propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="21544-140">Each packet contains this property by default.</span></span> <span data-ttu-id="21544-141">L’origine (0,0) de la tablette est l’angle supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="21544-141">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21544-142">GUID_X_TILT_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="21544-142">GUID_X_TILT_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="21544-143">Pour un curseur de stylet, l’orientation de l’inclinaison x est l’angle entre le plan y, le plan z et le plan de l’axe y et du stylet.</span><span class="sxs-lookup"><span data-stu-id="21544-143">For a pen cursor, the x-tilt orientation is the angle between the y,z-plane and the pen and y-axis plane.</span></span> <span data-ttu-id="21544-144">La valeur est 0 lorsque le stylet est perpendiculaire à la surface de dessin et est positif lorsque le stylet est à droite de Perpendicular.</span><span class="sxs-lookup"><span data-stu-id="21544-144">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is to the right of perpendicular.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21544-145">GUID_Y</span><span class="sxs-lookup"><span data-stu-id="21544-145">GUID_Y</span></span><br/></td>
<td><span data-ttu-id="21544-146">Coordonnée y dans l’espace de coordonnées de la tablette.</span><span class="sxs-lookup"><span data-stu-id="21544-146">The y-coordinate in the tablet coordinate space.</span></span> <span data-ttu-id="21544-147">Chaque paquet contient cette propriété par défaut.</span><span class="sxs-lookup"><span data-stu-id="21544-147">Each packet contains this property by default.</span></span> <span data-ttu-id="21544-148">L’origine (0,0) de la tablette est l’angle supérieur gauche.</span><span class="sxs-lookup"><span data-stu-id="21544-148">The origin (0,0) of the tablet is the upper-left corner.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="21544-149">GUID_Y_TILT_ORIENTATION</span><span class="sxs-lookup"><span data-stu-id="21544-149">GUID_Y_TILT_ORIENTATION</span></span><br/></td>
<td><span data-ttu-id="21544-150">Pour un curseur de stylet, l’orientation de l’inclinaison y est l’angle entre le plan x, z et le plan de l’axe x et du stylet.</span><span class="sxs-lookup"><span data-stu-id="21544-150">For a pen cursor, the y-tilt orientation is the angle between the x,z-plane and the pen and x-axis plane.</span></span> <span data-ttu-id="21544-151">La valeur est égale à 0 lorsque le stylet est perpendiculaire à la surface de dessin et est positif lorsque le stylet est vers le haut ou à l’extérieur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="21544-151">The value is 0 when the pen is perpendicular to the drawing surface and is positive when the pen is upward, or away from the user.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="21544-152">GUID_Z</span><span class="sxs-lookup"><span data-stu-id="21544-152">GUID_Z</span></span><br/></td>
<td><span data-ttu-id="21544-153">La coordonnée z ou la distance de la pointe du stylet à partir de la surface du Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="21544-153">The z-coordinate or distance of the pen tip from the tablet surface.</span></span> <span data-ttu-id="21544-154">Le type d’énumération <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> détermine l’unité de mesure de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="21544-154">The <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> enumeration type determines the unit of measurement for this property.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="21544-155">Le champ TangentPressure représente une pression le long du plan de la surface de la tablette. le champ NormalPressure représente une pression perpendiculaire au plan de la surface de la tablette.</span><span class="sxs-lookup"><span data-stu-id="21544-155">The TangentPressure field represents pressure along the plane of the tablet surface; the NormalPressure field represents pressure perpendicular to the plane of the tablet surface.</span></span>

 

 

 




