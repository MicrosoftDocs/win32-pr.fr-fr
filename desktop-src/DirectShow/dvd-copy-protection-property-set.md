---
description: Le jeu de propriétés protection de copie de DVD permet d’authentifier les informations de protection contre la copie à partir de déchiffreurs matériels ou logiciels. Utilisez cette propriété pour empêcher toute copie non autorisée à partir d’un DVD-vidéo préenregistré.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: Jeu de propriétés de protection de copie de DVD (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14146ce0be19a4ed49c23517987a2c91a85da87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537624"
---
# <a name="dvd-copy-protection-property-set"></a><span data-ttu-id="6fa16-104">Jeu de propriétés protection de copie de DVD</span><span class="sxs-lookup"><span data-stu-id="6fa16-104">DVD Copy Protection Property Set</span></span>

<span data-ttu-id="6fa16-105">Le jeu de propriétés protection de copie de DVD permet d’authentifier les informations de protection contre la copie à partir de déchiffreurs matériels ou logiciels.</span><span class="sxs-lookup"><span data-stu-id="6fa16-105">The DVD Copy Protection property set provides authentication of copy protection information from hardware or software decrypters.</span></span> <span data-ttu-id="6fa16-106">Utilisez cette propriété pour empêcher toute copie non autorisée à partir d’un DVD-vidéo préenregistré.</span><span class="sxs-lookup"><span data-stu-id="6fa16-106">Use this property set to prevent unauthorized copying from prerecorded DVD-Video.</span></span>

<span data-ttu-id="6fa16-107">Microsoft fournit des logiciels qui facilitent le processus d’authentification requis par le schéma de chiffrement, ce qui permet à un lecteur de DVD-ROM d’authentifier et de transférer des clés avec un DVD Decrypter.</span><span class="sxs-lookup"><span data-stu-id="6fa16-107">Microsoft provides software that facilitates the authentication process required by the encryption scheme, thus enabling a DVD-ROM drive to authenticate and transfer keys with a DVD decrypter.</span></span> <span data-ttu-id="6fa16-108">Microsoft n’a pas de plan actuel pour envoyer un DVD Decrypter et, à la place, il fournit un code de système d’exploitation qui servira d’agent pour permettre l’authentification de déchiffreurs matériels ou logiciels.</span><span class="sxs-lookup"><span data-stu-id="6fa16-108">Microsoft has no current plans to ship a DVD decrypter and, instead, is providing operating system code that will act as the agent to enable authentication of either hardware or software decrypters.</span></span>

<span data-ttu-id="6fa16-109">Le navigateur DVD lance et contrôle le processus d’échange de clés.</span><span class="sxs-lookup"><span data-stu-id="6fa16-109">The DVD navigator initiates and controls the key exchange process.</span></span> <span data-ttu-id="6fa16-110">Le minipilote de DVD n’a besoin que d’implémenter les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="6fa16-110">The DVD minidriver needs only to implement the following properties.</span></span> <span data-ttu-id="6fa16-111">Les autres composants gèrent le reste.</span><span class="sxs-lookup"><span data-stu-id="6fa16-111">Other components handle the rest.</span></span>

<span data-ttu-id="6fa16-112">Chaque flux d’entrée DVD recevra les propriétés de protection de copie.</span><span class="sxs-lookup"><span data-stu-id="6fa16-112">Each DVD input stream will receive copy protection properties.</span></span> <span data-ttu-id="6fa16-113">Cela est vrai même si le même matériel contrôle tous les flux de DVD.</span><span class="sxs-lookup"><span data-stu-id="6fa16-113">This is true even if the same hardware controls all DVD streams.</span></span>

<span data-ttu-id="6fa16-114">Les informations suivantes présentent les constantes et types de données nécessaires à utiliser pour ce jeu de propriétés dans les appels aux méthodes [**IKsPropertySet**](ikspropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="6fa16-114">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="6fa16-115">Il fournit des valeurs pour les paramètres **GUID** (*GUIDPROPSET*), ID de propriété (*dwPropID*) et type de données de propriété (*pPropData*).</span><span class="sxs-lookup"><span data-stu-id="6fa16-115">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



|                   |                           |
|-------------------|---------------------------|
| <span data-ttu-id="6fa16-116">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="6fa16-116">Property Set GUID</span></span> | <span data-ttu-id="6fa16-117">AM \_ KSPROPSETID \_ CopyProt</span><span class="sxs-lookup"><span data-stu-id="6fa16-117">AM\_KSPROPSETID\_CopyProt</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6fa16-118">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="6fa16-118">Property ID</span></span></th>
<th><span data-ttu-id="6fa16-119">Description</span><span class="sxs-lookup"><span data-stu-id="6fa16-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6fa16-120"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="6fa16-120"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="6fa16-121">Recherche si la sortie vidéo est une vidéo de composant analogique de définition standard.</span><span class="sxs-lookup"><span data-stu-id="6fa16-121">Queries whether the video output is standard-definition, analog component video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fa16-122">AM_PROPERTY_COPY_MACROVISION</span><span class="sxs-lookup"><span data-stu-id="6fa16-122">AM_PROPERTY_COPY_MACROVISION</span></span></td>
<td><span data-ttu-id="6fa16-123">Il s’agit d’une propriété définie uniquement.</span><span class="sxs-lookup"><span data-stu-id="6fa16-123">This is a set-only property.</span></span> <span data-ttu-id="6fa16-124">Cette propriété définit le niveau de protection de copie analogique pour l’encodeur NTSC à l’extrémité de sortie du code confidentiel de réception.</span><span class="sxs-lookup"><span data-stu-id="6fa16-124">This property sets the analog copy protection level for the NTSC encoder on the output end of the receiving pin.</span></span> <span data-ttu-id="6fa16-125">Utilise <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6fa16-125">Uses <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fa16-126">AM_PROPERTY_DVDCOPY_CHLG_KEY</span><span class="sxs-lookup"><span data-stu-id="6fa16-126">AM_PROPERTY_DVDCOPY_CHLG_KEY</span></span></td>
<td><span data-ttu-id="6fa16-127">Les opérations d’extraction et de définition sont prises en charge sur cette propriété.</span><span class="sxs-lookup"><span data-stu-id="6fa16-127">Both get and set operations are supported on this property.</span></span> <span data-ttu-id="6fa16-128">Une opération d’extraction demande au décodeur de fournir sa clé de Challenge de bus.</span><span class="sxs-lookup"><span data-stu-id="6fa16-128">A get operation requests the decoder to provide its bus challenge key.</span></span> <span data-ttu-id="6fa16-129">Une opération ensembliste fournit le décodeur avec la clé de Challenge du bus à partir du lecteur de DVD.</span><span class="sxs-lookup"><span data-stu-id="6fa16-129">A set operation provides the decoder with the bus challenge key from the DVD drive.</span></span> <span data-ttu-id="6fa16-130">Les données passées dans cette propriété seront une structure de type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6fa16-130">The data passed in this property will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fa16-131">AM_PROPERTY_DVDCOPY_DEC_KEY2</span><span class="sxs-lookup"><span data-stu-id="6fa16-131">AM_PROPERTY_DVDCOPY_DEC_KEY2</span></span></td>
<td><span data-ttu-id="6fa16-132">Il s’agit d’une propriété de récupération uniquement.</span><span class="sxs-lookup"><span data-stu-id="6fa16-132">This is a get-only property.</span></span> <span data-ttu-id="6fa16-133">Cette propriété demande que la clé de bus du décodeur 2 soit transférée vers le lecteur de DVD.</span><span class="sxs-lookup"><span data-stu-id="6fa16-133">This property requests that the decoder's bus key 2 be transferred to the DVD drive.</span></span> <span data-ttu-id="6fa16-134">Les données passées sont une structure de type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6fa16-134">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fa16-135">AM_PROPERTY_DVDCOPY_DISC_KEY</span><span class="sxs-lookup"><span data-stu-id="6fa16-135">AM_PROPERTY_DVDCOPY_DISC_KEY</span></span></td>
<td><span data-ttu-id="6fa16-136">Propriété Set-only.</span><span class="sxs-lookup"><span data-stu-id="6fa16-136">Set-only property.</span></span> <span data-ttu-id="6fa16-137">Cela fournit une clé de disque.</span><span class="sxs-lookup"><span data-stu-id="6fa16-137">This provides disc key.</span></span> <span data-ttu-id="6fa16-138">La clé est une structure de type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6fa16-138">The key is a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fa16-139">AM_PROPERTY_DVDCOPY_DVD_KEY1</span><span class="sxs-lookup"><span data-stu-id="6fa16-139">AM_PROPERTY_DVDCOPY_DVD_KEY1</span></span></td>
<td><span data-ttu-id="6fa16-140">Il s’agit d’une propriété définie uniquement.</span><span class="sxs-lookup"><span data-stu-id="6fa16-140">This is a set-only property.</span></span> <span data-ttu-id="6fa16-141">Cette propriété fournit la clé de bus de lecteur de DVD 1 au décodeur.</span><span class="sxs-lookup"><span data-stu-id="6fa16-141">This property provides the DVD drive bus key 1 to the decoder.</span></span> <span data-ttu-id="6fa16-142">Les données passées sont une structure de type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6fa16-142">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fa16-143">AM_PROPERTY_DVDCOPY_REGION</span><span class="sxs-lookup"><span data-stu-id="6fa16-143">AM_PROPERTY_DVDCOPY_REGION</span></span></td>
<td><span data-ttu-id="6fa16-144">Code de région demande la définition de région que le décodeur est autorisé à lire comme défini par le consortium de DVD.</span><span class="sxs-lookup"><span data-stu-id="6fa16-144">Region code requests the region definition that the decoder is allowed to play in as defined by the DVD consortium.</span></span> <span data-ttu-id="6fa16-145">Cette région est définie en tant que structure de <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6fa16-145">This region is defined as a <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fa16-146">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span><span class="sxs-lookup"><span data-stu-id="6fa16-146">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span></span></td>
<td><span data-ttu-id="6fa16-147">Les options d’extraction et de définition sont prises en charge sur cette propriété.</span><span class="sxs-lookup"><span data-stu-id="6fa16-147">Both get and set are supported on this property.</span></span> <span data-ttu-id="6fa16-148">La méthode est appelée en premier pour déterminer si l’authentification est requise.</span><span class="sxs-lookup"><span data-stu-id="6fa16-148">Get is called first to determine if authentication is required.</span></span> <span data-ttu-id="6fa16-149">Les propriétés définies sont des indications relatives à la phase de la négociation de la protection contre la copie que le filtre entre.</span><span class="sxs-lookup"><span data-stu-id="6fa16-149">The set properties are indications as to which phase of copy protection negotiation the filter is entering.</span></span> <span data-ttu-id="6fa16-150">Les données passées sont une structure de type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6fa16-150">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6fa16-151">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span><span class="sxs-lookup"><span data-stu-id="6fa16-151">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span></span></td>
<td><span data-ttu-id="6fa16-152">Si cette propriété a la <strong>valeur true</strong>, le navigateur DVD n’envoie pas d’échantillons <strong>AM_UseNewCSSKey</strong> avant de négocier la clé de disque.</span><span class="sxs-lookup"><span data-stu-id="6fa16-152">If this property is <strong>TRUE</strong>, the DVD Navigator does not send <strong>AM_UseNewCSSKey</strong> samples before negotiating the disc key.</span></span> <span data-ttu-id="6fa16-153">Consultez <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6fa16-153">See <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span></span><br/> <span data-ttu-id="6fa16-154">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6fa16-154">Read-only.</span></span> <span data-ttu-id="6fa16-155">Les données de propriété sont une valeur <strong>bool</strong> .</span><span class="sxs-lookup"><span data-stu-id="6fa16-155">The property data is a <strong>BOOL</strong> value.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="6fa16-156">S’applique à Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6fa16-156">Applies to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6fa16-157">AM_PROPERTY_DVDCOPY_TITLE_KEY</span><span class="sxs-lookup"><span data-stu-id="6fa16-157">AM_PROPERTY_DVDCOPY_TITLE_KEY</span></span></td>
<td><span data-ttu-id="6fa16-158">Il s’agit d’une propriété définie uniquement.</span><span class="sxs-lookup"><span data-stu-id="6fa16-158">This is a set-only property.</span></span> <span data-ttu-id="6fa16-159">Cela fournit une clé de titre à partir du contenu actuel.</span><span class="sxs-lookup"><span data-stu-id="6fa16-159">This provides title key from current content.</span></span> <span data-ttu-id="6fa16-160">La clé est une structure de type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6fa16-160">The key is a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="6fa16-161">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fa16-161">Requirements</span></span>



| <span data-ttu-id="6fa16-162">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fa16-162">Requirement</span></span> | <span data-ttu-id="6fa16-163">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fa16-163">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa16-164">En-tête</span><span class="sxs-lookup"><span data-stu-id="6fa16-164">Header</span></span><br/> | <dl> <span data-ttu-id="6fa16-165"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fa16-165"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fa16-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fa16-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fa16-167">Jeux de propriétés</span><span class="sxs-lookup"><span data-stu-id="6fa16-167">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




