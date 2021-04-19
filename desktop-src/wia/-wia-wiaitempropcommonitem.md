---
description: Les constantes de propriété d’appareil suivantes doivent être prises en charge par toutes les interfaces d’interface IWiaItem, IWiaItem2 et IWiaDrvItem, sauf indication contraire dans leurs descriptions.
ms.assetid: ef48313e-4df4-4ccd-a085-f714100885a7
title: Constantes de propriété d’élément WIA communes (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPA_ACCESS_RIGHTS
- WIA_IPA_APP_COLOR_MAPPING
- WIA_IPA_BITS_PER_CHANNEL
- WIA_IPA_BUFFER_SIZE
- WIA_IPA_BYTES_PER_LINE
- WIA_IPA_CHANNELS_PER_PIXEL
- WIA_IPA_COLOR_PROFILE
- WIA_IPA_COMPRESSION
- WIA_IPA_DATATYPE
- WIA_IPA_DEPTH
- WIA_IPA_FILENAME_EXTENSION
- WIA_IPA_FORMAT
- WIA_IPA_FULL_ITEM_NAME
- WIA_IPA_GAMMA_CURVES
- WIA_IPA_ICM_PROFILE_NAME
- WIA_IPA_ITEM_CATEGORY
- WIA_IPA_ITEM_FLAGS
- WIA_IPA_ITEM_NAME
- WIA_IPA_ITEM_SIZE
- WIA_IPA_ITEM_TIME
- WIA_IPA_ITEMS_STORED
- WIA_IPA_MIN_BUFFER_SIZE
- WIA_IPA_NUMBER_OF_LINES
- WIA_IPA_PIXELS_PER_LINE
- WIA_IPA_PLANAR
- WIA_IPA_PREFERRED_FORMAT
- WIA_IPA_PROP_STREAM_COMPAT_ID
- WIA_IPA_RAW_BITS_PER_CHANNEL
- WIA_IPA_REGION_TYPE
- WIA_IPA_SUPPRESS_PROPERTY_PAGE
- WIA_IPA_TYMED
- WIA_IPA_UPLOAD_ITEM_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: d36a390256c6a9d183caa0f9231d2a92035d83da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517278"
---
# <a name="common-wia-item-property-constants"></a><span data-ttu-id="88511-103">Constantes de propriété d’élément WIA courantes</span><span class="sxs-lookup"><span data-stu-id="88511-103">Common WIA Item Property Constants</span></span>

<span data-ttu-id="88511-104">Les constantes de propriété d’appareil suivantes doivent être prises en charge par toutes les interfaces d’interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem), [**IWiaItem2**](-wia-iwiaitem2.md) et [IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) , sauf indication contraire dans leurs descriptions.</span><span class="sxs-lookup"><span data-stu-id="88511-104">The following device property constants must be supported by all [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem), [**IWiaItem2**](-wia-iwiaitem2.md) and [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) interfaces unless otherwise noted in their descriptions.</span></span>

<span data-ttu-id="88511-105">Le préfixe « WIA » \_ \_ indique une propriété d’élément pour tous les appareils et est la Convention d’affectation de noms utilisée dans C/C++.</span><span class="sxs-lookup"><span data-stu-id="88511-105">The prefix "WIA\_IPA\_" indicates an item property for all devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="88511-106">À des fins de script, ces constantes utilisent le préfixe « image » et font partie du type énuméré [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="88511-106">For scripting purposes these constants use the prefix "Picture" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="88511-107">Le nom de membre correspondant de cette énumération de script apparaît entre parenthèses à côté du nom de constante C/C++ dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="88511-107">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="88511-108">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="88511-108">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="88511-109">Description</span><span class="sxs-lookup"><span data-stu-id="88511-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ACCESS_RIGHTS"></span><span id="wia_ipa_access_rights"></span><dl> <span data-ttu-id="88511-110"><dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-110"><dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="88511-111">Cet indicateur contrôle l’accès à l’élément et indique si l’élément est supprimé.</span><span class="sxs-lookup"><span data-stu-id="88511-111">This flag controls access to the item as well as whether the item is deleted.</span></span><br/> <span data-ttu-id="88511-112">Obligatoire pour tous les éléments WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="88511-112">Required for all WIA 2.0 items.</span></span><br/> <span data-ttu-id="88511-113">Type : <strong>VT_I4</strong>; En lecture/écriture ou en lecture seule, en fonction de la capacité de l’élément à modifier ses droits d’accès ; Valeurs valides : WIA_PROP_FLAG</span><span class="sxs-lookup"><span data-stu-id="88511-113">Type: <strong>VT_I4</strong>; Read/Write or Read Only, depending on the item's ability to have its access rights changed; Valid values: WIA_PROP_FLAG</span></span><br/> <span data-ttu-id="88511-114">Le tableau suivant contient les cinq indicateurs qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-114">The following table has the five flags that are valid with this property.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="88511-115">Droit d'accès</span><span class="sxs-lookup"><span data-stu-id="88511-115">Access Right</span></span></th>
<th><span data-ttu-id="88511-116">Description</span><span class="sxs-lookup"><span data-stu-id="88511-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88511-117">WIA_ITEM_READ</span><span class="sxs-lookup"><span data-stu-id="88511-117">WIA_ITEM_READ</span></span></td>
<td><span data-ttu-id="88511-118">L’élément possède un accès en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="88511-118">Item has read-only access.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-119">WIA_ITEM_WRITE</span><span class="sxs-lookup"><span data-stu-id="88511-119">WIA_ITEM_WRITE</span></span></td>
<td><span data-ttu-id="88511-120">L’élément possède un accès en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="88511-120">Item has write-only access.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-121">WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="88511-121">WIA_ITEM_CAN_BE_DELETED</span></span></td>
<td><span data-ttu-id="88511-122">L’élément possède un accès en suppression seule.</span><span class="sxs-lookup"><span data-stu-id="88511-122">Item has delete-only access.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-123">WIA_ITEM_RD</span><span class="sxs-lookup"><span data-stu-id="88511-123">WIA_ITEM_RD</span></span></td>
<td><span data-ttu-id="88511-124">WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="88511-124">WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-125">WIA_ITEM_RWD</span><span class="sxs-lookup"><span data-stu-id="88511-125">WIA_ITEM_RWD</span></span></td>
<td><span data-ttu-id="88511-126">WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</span><span class="sxs-lookup"><span data-stu-id="88511-126">WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_APP_COLOR_MAPPING"></span><span id="wia_ipa_app_color_mapping"></span><dl> <span data-ttu-id="88511-127"><dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-127"><dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-128">Cette propriété est réservée par pour une utilisation future et n’est pas implémentée pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="88511-128">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="88511-129">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-129">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BITS_PER_CHANNEL"></span><span id="wia_ipa_bits_per_channel"></span><dl> <span data-ttu-id="88511-130"><dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-130"><dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-131">Contient le nombre de bits par canal pour l’image.</span><span class="sxs-lookup"><span data-stu-id="88511-131">Contains the number of bits per channel for the image.</span></span> <span data-ttu-id="88511-132">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-132">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="88511-133">Obligatoire pour tous les éléments d’image stockés et compatibles avec l’acquisition WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="88511-133">Required for all WIA 2.0 acquisition-enabled or stored image items.</span></span></p>
<p><span data-ttu-id="88511-134">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-134">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_BUFFER_SIZE"></span><span id="wia_ipa_buffer_size"></span><dl> <span data-ttu-id="88511-135"><dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-135"><dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-136">Contient la taille de la mémoire tampon, en octets, utilisée pendant un transfert de données.</span><span class="sxs-lookup"><span data-stu-id="88511-136">Contains the size of the buffer, in bytes, used during a data transfer.</span></span> <span data-ttu-id="88511-137">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-137">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="88511-138">Une application peut lire cette propriété pour déterminer la taille de mémoire tampon spécifiée par le pilote pour les transferts de données.</span><span class="sxs-lookup"><span data-stu-id="88511-138">An application can read this property to determine the driver-specified buffer size for data transfers.</span></span> <span data-ttu-id="88511-139">Le service WIA lit également cette propriété pour allouer de la mémoire au minipilote pendant le transfert de données.</span><span class="sxs-lookup"><span data-stu-id="88511-139">The WIA service also reads this property to allocate memory for the minidriver during the data transfer</span></span></p>
<p><span data-ttu-id="88511-140">Facultatif pour tous les éléments WIA 2,0 avec transfert.</span><span class="sxs-lookup"><span data-stu-id="88511-140">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="88511-141">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-141">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="88511-142">La propriété <strong>WIA_IPA_BUFFER_SIZE</strong> contient la quantité minimale de données qu’une application peut demander à un moment donné.</span><span class="sxs-lookup"><span data-stu-id="88511-142">The <strong>WIA_IPA_BUFFER_SIZE</strong> property contains is the minimum amount of data an application can request at any given time.</span></span> <span data-ttu-id="88511-143">Plus la taille de la mémoire tampon est grande, plus les demandes de l’appareil sont volumineuses.</span><span class="sxs-lookup"><span data-stu-id="88511-143">The larger the buffer size, the larger the requests to the device will be.</span></span> <span data-ttu-id="88511-144">Cela peut rendre l’appareil plus lent et ne pas répondre, peut ralentir les performances globales du système et consommer une quantité excessive de ressources.</span><span class="sxs-lookup"><span data-stu-id="88511-144">This can make the device seem slow and unresponsive, can slow the overall system performance, and can consume excessive resources.</span></span> <span data-ttu-id="88511-145">Les tailles de mémoire tampon trop petites peuvent ralentir les performances du transfert de données en exigeant de nombreuses requêtes plus petites.</span><span class="sxs-lookup"><span data-stu-id="88511-145">Buffer sizes that are too small can slow performance of the data transfer by requiring many smaller requests.</span></span> <span data-ttu-id="88511-146">Choisissez une taille de mémoire tampon raisonnable en prenant en compte la taille standard d’une demande de données sur votre appareil et en équilibrant le nombre de demandes par rapport à la taille de ces demandes.</span><span class="sxs-lookup"><span data-stu-id="88511-146">Choose a reasonable buffer size by considering the typical size of a data request to your device and balancing the number of requests against the size of those requests.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BYTES_PER_LINE"></span><span id="wia_ipa_bytes_per_line"></span><dl> <span data-ttu-id="88511-147"><dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-147"><dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-148">Contient le nombre d’octets d’une ligne d’analyse de l’image.</span><span class="sxs-lookup"><span data-stu-id="88511-148">Contains the number of bytes in one scan line of the image.</span></span> <span data-ttu-id="88511-149">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-149">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="88511-150">Facultatif pour tous les éléments WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="88511-150">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="88511-151">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-151">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_CHANNELS_PER_PIXEL"></span><span id="wia_ipa_channels_per_pixel"></span><dl> <span data-ttu-id="88511-152"><dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-152"><dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-153">Contient le nombre de canaux par pixel pour l’image.</span><span class="sxs-lookup"><span data-stu-id="88511-153">Contains the number of channels per pixel for the image.</span></span> <span data-ttu-id="88511-154">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-154">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="88511-155">Obligatoire pour tous les éléments d’image stockés et compatibles avec l’acquisition WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="88511-155">Required for all WIA 2.0 acquisition-enabled or stored image items.</span></span></p>
<p><span data-ttu-id="88511-156">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-156">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_COLOR_PROFILE"></span><span id="wia_ipa_color_profile"></span><dl> <span data-ttu-id="88511-157"><dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-157"><dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-158">Cette propriété est réservée par pour une utilisation future et n’est pas implémentée pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="88511-158">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="88511-159">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-159">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_COMPRESSION"></span><span id="wia_ipa_compression"></span><dl> <span data-ttu-id="88511-160"><dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-160"><dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-161">Contient le type de compression actuel utilisé.</span><span class="sxs-lookup"><span data-stu-id="88511-161">Contains the current compression type used.</span></span> <span data-ttu-id="88511-162">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-162">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="88511-163">Une application lit cette propriété pour déterminer le type de compression d’image ou définit cette propriété pour configurer le paramètre de compression.</span><span class="sxs-lookup"><span data-stu-id="88511-163">An application reads this property to determine the image compression type or sets this property to configure the compression setting.</span></span></p>
<p><span data-ttu-id="88511-164">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="88511-164">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="88511-165">Le tableau suivant contient les constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-165">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="88511-166">Le symbole <strong>V</strong> indique que la constante est prise en charge uniquement dans Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="88511-166">The <strong>V</strong> symbol indicates that the constant is supported only in Windows Vista and later.</span></span> <span data-ttu-id="88511-167">(Disponible uniquement par le biais de l’interface <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .)</span><span class="sxs-lookup"><span data-stu-id="88511-167">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="88511-168">Type de compression</span><span class="sxs-lookup"><span data-stu-id="88511-168">Compression Type</span></span></th>
<th><span data-ttu-id="88511-169">Description</span><span class="sxs-lookup"><span data-stu-id="88511-169">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88511-170">WIA_COMPRESSION_NONE</span><span class="sxs-lookup"><span data-stu-id="88511-170">WIA_COMPRESSION_NONE</span></span></td>
<td><span data-ttu-id="88511-171">Aucune compression.</span><span class="sxs-lookup"><span data-stu-id="88511-171">No compression.</span></span> <span data-ttu-id="88511-172">Pour plus d’informations, consultez <strong>Remarque</strong> .</span><span class="sxs-lookup"><span data-stu-id="88511-172">See <strong>Note</strong> for more information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-173">WIA_COMPRESSION_AUTO</span><span class="sxs-lookup"><span data-stu-id="88511-173">WIA_COMPRESSION_AUTO</span></span></td>
<td><span data-ttu-id="88511-174">Mode de compression automatique.</span><span class="sxs-lookup"><span data-stu-id="88511-174">Automatic compression mode.</span></span> <span data-ttu-id="88511-175">Pour plus d’informations, consultez <strong>Remarque</strong> .</span><span class="sxs-lookup"><span data-stu-id="88511-175">See <strong>Note</strong> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-176">WIA_COMPRESSION_BI_RLE4</span><span class="sxs-lookup"><span data-stu-id="88511-176">WIA_COMPRESSION_BI_RLE4</span></span></td>
<td><span data-ttu-id="88511-177">Compression RLE4</span><span class="sxs-lookup"><span data-stu-id="88511-177">RLE4 compression</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-178">WIA_COMPRESSION_BI_RLE8</span><span class="sxs-lookup"><span data-stu-id="88511-178">WIA_COMPRESSION_BI_RLE8</span></span></td>
<td><span data-ttu-id="88511-179">Compression RLE8</span><span class="sxs-lookup"><span data-stu-id="88511-179">RLE8 compression</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-180">WIA_COMPRESSION_G3</span><span class="sxs-lookup"><span data-stu-id="88511-180">WIA_COMPRESSION_G3</span></span></td>
<td><span data-ttu-id="88511-181">Compression de groupe 3</span><span class="sxs-lookup"><span data-stu-id="88511-181">Group 3 compression</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-182">WIA_COMPRESSION_G4</span><span class="sxs-lookup"><span data-stu-id="88511-182">WIA_COMPRESSION_G4</span></span></td>
<td><span data-ttu-id="88511-183">Compression de groupe 4</span><span class="sxs-lookup"><span data-stu-id="88511-183">Group 4 compression</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-184">WIA_COMPRESSION_JPEG</span><span class="sxs-lookup"><span data-stu-id="88511-184">WIA_COMPRESSION_JPEG</span></span></td>
<td><span data-ttu-id="88511-185">Compression JPEG.</span><span class="sxs-lookup"><span data-stu-id="88511-185">JPEG compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-186">WIA_COMPRESSION_JBIG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="88511-186">WIA_COMPRESSION_JBIG<strong>V</strong></span></span></td>
<td><span data-ttu-id="88511-187">Compression JBIG.</span><span class="sxs-lookup"><span data-stu-id="88511-187">JBIG compression.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-188">WIA_COMPRESSION_JPEG2K<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="88511-188">WIA_COMPRESSION_JPEG2K<strong>V</strong></span></span></td>
<td><span data-ttu-id="88511-189">Compression JPEG 2000.</span><span class="sxs-lookup"><span data-stu-id="88511-189">JPEG 2000 compression.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-190">WIA_COMPRESSION_PNG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="88511-190">WIA_COMPRESSION_PNG<strong>V</strong></span></span></td>
<td><span data-ttu-id="88511-191">Compression PNG.</span><span class="sxs-lookup"><span data-stu-id="88511-191">PNG compression.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
<p>[!Note]</p>
<p><span data-ttu-id="88511-192">Lorsque cette propriété est WIA_COMPRESSION_NONE, et WIA_IPA_FORMAT est soit WiaImgFmt_PDFA, soit WiaImgFmt_XPS ; WIA_COMPRESSION_NONE signifie alors que le mode de compression n’est pas défini et que le scanneur doit décider d’un mode.</span><span class="sxs-lookup"><span data-stu-id="88511-192">When this property is WIA_COMPRESSION_NONE, and WIA_IPA_FORMAT is either WiaImgFmt_PDFA or WiaImgFmt_XPS; then WIA_COMPRESSION_NONE means that the compression mode is undefined and the scanner must decide on a mode.</span></span></p>
<p><span data-ttu-id="88511-193">WIA_COMPRESSION_AUTO est une nouvelle valeur de propriété définie pour la propriété WIA_IPA_COMPRESSION.</span><span class="sxs-lookup"><span data-stu-id="88511-193">WIA_COMPRESSION_AUTO is a new property value defined for the WIA_IPA_COMPRESSION property.</span></span> <span data-ttu-id="88511-194">Cette valeur est valide pour tous les éléments de source de données d’image programmable, y compris le plateau et le chargeur.</span><span class="sxs-lookup"><span data-stu-id="88511-194">This value is valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="88511-195">Lorsque cette valeur est prise en charge par le mini-pilote WIA, le client d’application WIA peut définir WIA_IPA_COMPRESSION afin d’activer la détection automatique du mode de compression au niveau de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="88511-195">When this value is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_COMPRESSION in order to enable automatic compression mode detection at the device.</span></span> <span data-ttu-id="88511-196">WIA_COMPRESSION_AUTO pouvez travailler avec et sans une couleur automatique complète prise en charge ou activée (WIA_DATA_AUTO et WIA_DEPTH_AUTO).</span><span class="sxs-lookup"><span data-stu-id="88511-196">WIA_COMPRESSION_AUTO can work with and without full auto-color being supported or enabled (WIA_DATA_AUTO and WIA_DEPTH_AUTO).</span></span></p>
<p><span data-ttu-id="88511-197">WIA_COMPRESSION_AUTO est très utile avec les formats de fichier de transfert qui prennent en charge plusieurs types de données et des profondeurs de bits, comme WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="88511-197">WIA_COMPRESSION_AUTO is most useful with transfer file formats that support multiple data types and bit depths, such as WiaImgFmt_RAW.</span></span> <span data-ttu-id="88511-198">Pour plus d’informations sur les formats de fichier de transfert, consultez WIA_IPA_FORMAT dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="88511-198">For more information about transfer file formats, see WIA_IPA_FORMAT in this table.</span></span></p>
<p><span data-ttu-id="88511-199">La WIA_COMPRESSION_AUTO pour le mini-pilote WIA est opitonal.</span><span class="sxs-lookup"><span data-stu-id="88511-199">It is opitonal for the WIA mini-driver to suport WIA_COMPRESSION_AUTO.</span></span> <span data-ttu-id="88511-200">Lorsqu’il est pris en charge, le mini-pilote WIA ne doit jamais le définir comme valeur par défaut pour WIA_IPA_COMPRESSION ; seule l’application WIA peut définir cette valeur.</span><span class="sxs-lookup"><span data-stu-id="88511-200">When it is supported, the WIA mini-driver must never set it as the default value for WIA_IPA_COMPRESSION; only the WIA application can set this value.</span></span></p>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_DATATYPE"></span><span id="wia_ipa_datatype"></span><dl> <span data-ttu-id="88511-201"><dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-201"><dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-202">Contient le paramètre de type de données actuel pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="88511-202">Contains the current data type setting for the device.</span></span> <span data-ttu-id="88511-203">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-203">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="88511-204">Une application lit cette propriété pour déterminer le type de données de l’image.</span><span class="sxs-lookup"><span data-stu-id="88511-204">An application reads this property to determine the data type of the image.</span></span> <span data-ttu-id="88511-205">Une application écrit cette propriété pour définir le type de données actuel de l’image à transférer.</span><span class="sxs-lookup"><span data-stu-id="88511-205">An application writes this property to set the current data type of the image about to be transferred.</span></span></p>
<p><span data-ttu-id="88511-206">Cette propriété est obligatoire pour tous les éléments WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="88511-206">This property is required for all WIA 2.0 items.</span></span> <span data-ttu-id="88511-207">Il doit être en lecture/écriture pour tous les éléments de l’acquisition WIA 2,0 et lecture uniquement pour les éléments de stockage WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="88511-207">It must be Read/Write for all WIA 2.0 acquisition enabled items and Read Only for WIA 2.0 storage items.</span></span></p>
<p><span data-ttu-id="88511-208">Type : <strong>VT_I4</strong>; Accès pour les systèmes d’exploitation antérieurs à Windows Vista : cette propriété est en lecture seule pour les appareils photo et en lecture/écriture pour les scanneurs ; Accès pour Windows Vista et versions ultérieures : cette propriété est en lecture seule pour les éléments WIA_CATEGORY_FOLDER et WIA_CATEGORY_FINISHED_FILE, et en lecture/écriture pour toutes les autres catégories d’éléments WIA 2,0 ; Valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="88511-208">Type: <strong>VT_I4</strong>; Access for pre-Windows Vista operating systems: This property is Read Only for cameras and Read/Write for scanners; Access for Windows Vista and later: This property is Read Only for WIA_CATEGORY_FOLDER and WIA_CATEGORY_FINISHED_FILE items, and Read/Write for all other WIA 2.0 item categories; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="88511-209">Le tableau suivant contient les six constantes qui sont valides avec lorsque <strong>WIA_IPA_FORMAT</strong> n’est pas défini sur WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="88511-209">The following table has the six constants that are valid with when <strong>WIA_IPA_FORMAT</strong> is not set to WiaImgFmt_RAW.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="88511-210">Type de données</span><span class="sxs-lookup"><span data-stu-id="88511-210">Data Type</span></span></th>
<th><span data-ttu-id="88511-211">Description</span><span class="sxs-lookup"><span data-stu-id="88511-211">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88511-212">WIA_DATA_AUTO</span><span class="sxs-lookup"><span data-stu-id="88511-212">WIA_DATA_AUTO</span></span></td>
<td><span data-ttu-id="88511-213">Valide pour tous les éléments de source de données d’image programmable, y compris le plateau et le chargeur.</span><span class="sxs-lookup"><span data-stu-id="88511-213">Valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="88511-214">Lorsque cette valeur est prise en charge par le mini-pilote WIA, le client d’application WIA peut définir WIA_IPA_DATATYPE afin d’activer la détection automatique des couleurs au niveau de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="88511-214">When this value is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_DATATYPE in order to enable automatic color detection at the device.</span></span> <span data-ttu-id="88511-215">Lorsque WIA_DATA_AUTO est définie, le mini-pilote WIA doit mettre à jour WIA_IPA_DEPTH sur le même élément à WIA_DEPTH_AUTO (qui doit être une valeur prise en charge si l’appareil prend en charge la couleur automatique).</span><span class="sxs-lookup"><span data-stu-id="88511-215">When WIA_DATA_AUTO is set, the WIA mini-driver must update WIA_IPA_DEPTH on the same item to WIA_DEPTH_AUTO (which must be a supported value if the device supports automatic color).</span></span><br/> <span data-ttu-id="88511-216">Il s’agit d’une valeur facultative, mais elle est requise lorsque WIA_DEPTH_AUTO est pris en charge pour WIA_IPA_DEPTH.</span><span class="sxs-lookup"><span data-stu-id="88511-216">This is an optional value, but it is required when WIA_DEPTH_AUTO is supported for WIA_IPA_DEPTH.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-217">WIA_DATA_COLOR</span><span class="sxs-lookup"><span data-stu-id="88511-217">WIA_DATA_COLOR</span></span></td>
<td><span data-ttu-id="88511-218">Les données d’analyse sont de couleur rouge, verte, bleue (RVB).</span><span class="sxs-lookup"><span data-stu-id="88511-218">Scan data is red, green, blue (RGB) color.</span></span> <span data-ttu-id="88511-219">Le format de couleur complet est décrit à l’aide des propriétés WIA suivantes : <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></span><span class="sxs-lookup"><span data-stu-id="88511-219">The full color format is described using the following WIA properties: <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></span></span><br/> <span data-ttu-id="88511-220"><strong>WIA_IPA_BITS_PER_CHANNEL</strong></span><span class="sxs-lookup"><span data-stu-id="88511-220"><strong>WIA_IPA_BITS_PER_CHANNEL</strong></span></span><br/> <span data-ttu-id="88511-221"><strong>WIA_IPA_PLANAR</strong></span><span class="sxs-lookup"><span data-stu-id="88511-221"><strong>WIA_IPA_PLANAR</strong></span></span><br/> <span data-ttu-id="88511-222"><strong>WIA_IPA_PIXELS_PER_LINE</strong></span><span class="sxs-lookup"><span data-stu-id="88511-222"><strong>WIA_IPA_PIXELS_PER_LINE</strong></span></span><br/> <span data-ttu-id="88511-223"><strong>WIA_IPA_BYTES_PER_LINE</strong></span><span class="sxs-lookup"><span data-stu-id="88511-223"><strong>WIA_IPA_BYTES_PER_LINE</strong></span></span><br/> <span data-ttu-id="88511-224"><strong>WIA_IPA_NUMBER_OF_LINES</strong></span><span class="sxs-lookup"><span data-stu-id="88511-224"><strong>WIA_IPA_NUMBER_OF_LINES</strong></span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-225">WIA_DATA_COLOR_DITHER</span><span class="sxs-lookup"><span data-stu-id="88511-225">WIA_DATA_COLOR_DITHER</span></span></td>
<td><span data-ttu-id="88511-226">Identique à WIA_DATA_COLOR à la différence que les données sont tramées à l’aide du modèle de trame actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="88511-226">Same as WIA_DATA_COLOR except that the data is dithered using the currently selected dither pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-227">WIA_DATA_COLOR_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="88511-227">WIA_DATA_COLOR_THRESHOLD</span></span></td>
<td><span data-ttu-id="88511-228">Identique à WIA_DATA_COLOR sauf que la valeur de seuil est utilisée lors de l’analyse des données.</span><span class="sxs-lookup"><span data-stu-id="88511-228">Same as WIA_DATA_COLOR except that the threshold value is used when scanning the data.</span></span> <span data-ttu-id="88511-229">Les valeurs de couleur sur la valeur de <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> sont converties en luminosité complète. les couleurs sous cette valeur sont converties en noir.</span><span class="sxs-lookup"><span data-stu-id="88511-229">Color values over the <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> value are converted to full brightness; colors under this value are converted to black.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-230">WIA_DATA_DITHER</span><span class="sxs-lookup"><span data-stu-id="88511-230">WIA_DATA_DITHER</span></span></td>
<td><span data-ttu-id="88511-231">Les données d’analyse sont tramées à l’aide du modèle de trame actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="88511-231">Scan data is dithered using the currently selected dither pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-232">WIA_DATA_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="88511-232">WIA_DATA_GRAYSCALE</span></span></td>
<td><span data-ttu-id="88511-233">Les données d’analyse représentent l’intensité.</span><span class="sxs-lookup"><span data-stu-id="88511-233">Scan data represents intensity.</span></span> <span data-ttu-id="88511-234">La palette est une échelle grise fixe et à espacement identique avec une profondeur spécifiée par <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-234">The palette is a fixed, equally-spaced gray scale with a depth specified by <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-235">WIA_DATA_THRESHOLD</span><span class="sxs-lookup"><span data-stu-id="88511-235">WIA_DATA_THRESHOLD</span></span></td>
<td><span data-ttu-id="88511-236">Le seuil est un bit par pixel de données en noir et blanc.</span><span class="sxs-lookup"><span data-stu-id="88511-236">The threshold is one bit per pixel of black-and-white data.</span></span> <span data-ttu-id="88511-237">Les données sur la valeur actuelle de <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> sont converties en blanc ; les données de cette valeur sont converties en noir.</span><span class="sxs-lookup"><span data-stu-id="88511-237">Data over the current value of <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> is converted to white; data under this value is converted to black.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="88511-238">La propriété <strong>WIA_IPA_DATATYPE</strong> est également utilisée pour décrire le type de transfert de données brutes à utiliser lorsque l’application définit WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="88511-238">The <strong>WIA_IPA_DATATYPE</strong> property is also used to describe the type of RAW data transfer to be used when the application sets WiaImgFmt_RAW.</span></span> <span data-ttu-id="88511-239">Le pilote doit définir la propriété <strong>WIA_IPA_DATATYPE</strong> sur une liste de valeurs autorisées à partir desquelles l’application peut en choisir une.</span><span class="sxs-lookup"><span data-stu-id="88511-239">The driver should set the <strong>WIA_IPA_DATATYPE</strong> property to a list of allowed values from which the application can pick one.</span></span></p>
<p><span data-ttu-id="88511-240">Si l’appareil peut être défini sur une seule valeur, créez un <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type et placez la valeur valide dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="88511-240">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="88511-241">Vérifiez la propriété <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> pour déterminer la profondeur de bit.</span><span class="sxs-lookup"><span data-stu-id="88511-241">Check the <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property to determine the bit depth.</span></span> <span data-ttu-id="88511-242">Cette propriété contient généralement une valeur unique pour les appareils photo.</span><span class="sxs-lookup"><span data-stu-id="88511-242">This property usually contains a single value for cameras.</span></span></p>
<p><span data-ttu-id="88511-243">Le tableau suivant répertorie les constantes qui sont valides avec <strong>WIA_IPA_DATATYPE</strong> lorsque <strong>WIA_IPA_FORMAT</strong> a la valeur WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="88511-243">The following table lists the constants that are valid with <strong>WIA_IPA_DATATYPE</strong> when <strong>WIA_IPA_FORMAT</strong> is set to WiaImgFmt_RAW.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="88511-244">Type de données</span><span class="sxs-lookup"><span data-stu-id="88511-244">Data Type</span></span></th>
<th><span data-ttu-id="88511-245">Description</span><span class="sxs-lookup"><span data-stu-id="88511-245">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88511-246">WIA_DATA_GRAYSCALE</span><span class="sxs-lookup"><span data-stu-id="88511-246">WIA_DATA_GRAYSCALE</span></span></td>
<td><span data-ttu-id="88511-247">Les données d’analyse représentent l’intensité.</span><span class="sxs-lookup"><span data-stu-id="88511-247">Scan data represents intensity.</span></span> <span data-ttu-id="88511-248">La palette est un niveau de nuances de gris fixe et uniformément espacé avec une profondeur spécifiée par la propriété <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> .</span><span class="sxs-lookup"><span data-stu-id="88511-248">The palette is a fixed, equally spaced grayscale with a depth specified by the <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> property.</span></span> <span data-ttu-id="88511-249"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> doit avoir la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="88511-249"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-250">WIA_DATA_RAW_BGR</span><span class="sxs-lookup"><span data-stu-id="88511-250">WIA_DATA_RAW_BGR</span></span></td>
<td><span data-ttu-id="88511-251">Les données d’analyse sont dans le BGR (bleu-vert-rouge) colorspace.</span><span class="sxs-lookup"><span data-stu-id="88511-251">Scan data is in the BGR (blue-green-red) colorspace.</span></span> <span data-ttu-id="88511-252">Le format de couleur complet est décrit à l’aide de followingWIAproperties : <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a></span><span class="sxs-lookup"><span data-stu-id="88511-252">The full color format is described using the followingWIAproperties: <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a></span></span><br/> <span data-ttu-id="88511-253"><a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a></span><span class="sxs-lookup"><span data-stu-id="88511-253"><a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a></span></span><br/> <span data-ttu-id="88511-254"><a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a></span><span class="sxs-lookup"><span data-stu-id="88511-254"><a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a></span></span><br/> <span data-ttu-id="88511-255"><a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a></span><span class="sxs-lookup"><span data-stu-id="88511-255"><a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a></span></span><br/> <span data-ttu-id="88511-256"><a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a></span><span class="sxs-lookup"><span data-stu-id="88511-256"><a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a></span></span><br/> <span data-ttu-id="88511-257"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> doit avoir la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="88511-257"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-258">WIA_DATA_RAW_CMY</span><span class="sxs-lookup"><span data-stu-id="88511-258">WIA_DATA_RAW_CMY</span></span></td>
<td><span data-ttu-id="88511-259">Les données d’analyse se trouvent dans le colorspace cyan-magenta-jaune (CMJ).</span><span class="sxs-lookup"><span data-stu-id="88511-259">Scan data is in the cyan-magenta-yellow (CMY) colorspace.</span></span> <span data-ttu-id="88511-260">Le format de couleur complet est décrit à l’aide des mêmes propriétés WIA que dans WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="88511-260">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="88511-261"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> doit avoir la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="88511-261"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-262">WIA_DATA_RAW_CMYK</span><span class="sxs-lookup"><span data-stu-id="88511-262">WIA_DATA_RAW_CMYK</span></span></td>
<td><span data-ttu-id="88511-263">Les données d’analyse se trouvent dans le colorspace cyan-magenta-jaune-noir (CMJN).</span><span class="sxs-lookup"><span data-stu-id="88511-263">Scan data is in the cyan-magenta-yellow-black (CMYK) colorspace.</span></span> <span data-ttu-id="88511-264">Le format de couleur complet est décrit à l’aide des mêmes propriétés WIA que dans WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="88511-264">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="88511-265"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> doit avoir la valeur 4.</span><span class="sxs-lookup"><span data-stu-id="88511-265"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-266">WIA_DATA_RAW_RGB</span><span class="sxs-lookup"><span data-stu-id="88511-266">WIA_DATA_RAW_RGB</span></span></td>
<td><span data-ttu-id="88511-267">Les données d’analyse se trouvent dans le colorspace rouge-vert-bleu (RVB).</span><span class="sxs-lookup"><span data-stu-id="88511-267">Scan data is in the red-green-blue (RGB) colorspace.</span></span> <span data-ttu-id="88511-268">Le format de couleur complet est décrit à l’aide des mêmes propriétés WIA que dans WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="88511-268">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="88511-269"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> doit avoir la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="88511-269"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-270">WIA_DATA_RAW_YUV</span><span class="sxs-lookup"><span data-stu-id="88511-270">WIA_DATA_RAW_YUV</span></span></td>
<td><span data-ttu-id="88511-271">Les données d’analyse se trouvent dans la différence luminance-bleu-différence rouge (YUV) colorspace.</span><span class="sxs-lookup"><span data-stu-id="88511-271">Scan data is in the luminance-blue difference-red difference (YUV) colorspace.</span></span> <span data-ttu-id="88511-272">Le format de couleur complet est décrit à l’aide des mêmes propriétés WIA que dans WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="88511-272">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="88511-273"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> doit avoir la valeur 3.</span><span class="sxs-lookup"><span data-stu-id="88511-273"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 3.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-274">WIA_DATA_RAW_YUVK</span><span class="sxs-lookup"><span data-stu-id="88511-274">WIA_DATA_RAW_YUVK</span></span></td>
<td><span data-ttu-id="88511-275">Les données d’analyse se trouvent dans la différence luminance-bleu-différence rouge-noir (YUVK) colorspace.</span><span class="sxs-lookup"><span data-stu-id="88511-275">Scan data is in the luminance-blue difference-red difference-black (YUVK) colorspace.</span></span> <span data-ttu-id="88511-276">Le format de couleur complet est décrit à l’aide des mêmes propriétés WIA que dans WIA_DATA_RAW_BGR.</span><span class="sxs-lookup"><span data-stu-id="88511-276">The full color format is described using the same WIA properties as in WIA_DATA_RAW_BGR.</span></span> <span data-ttu-id="88511-277"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> doit avoir la valeur 4.</span><span class="sxs-lookup"><span data-stu-id="88511-277"><a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> must be set to 4.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_DEPTH"></span><span id="wia_ipa_depth"></span><dl> <span data-ttu-id="88511-278"><dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-278"><dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-279">WIA_IPA_DEPTH contient le paramètre de profondeur de bit d’une image.</span><span class="sxs-lookup"><span data-stu-id="88511-279">WIA_IPA_DEPTH Contains the bit depth setting of an image.</span></span> <span data-ttu-id="88511-280">Le minipilote crée et gère cette propriété. Une application lit cette propriété pour déterminer le paramètre de profondeur de bit de l’image.</span><span class="sxs-lookup"><span data-stu-id="88511-280">The minidriver creates and maintains this property.An application reads this property to determine the bit depth setting of the image.</span></span> <span data-ttu-id="88511-281">L’application peut également être en mesure de définir cette valeur sur la profondeur de bits souhaitée.</span><span class="sxs-lookup"><span data-stu-id="88511-281">The application might also be able to set this value to the desired bit depth.</span></span></p>
<p><span data-ttu-id="88511-282">Si l’appareil peut être défini sur une seule valeur, créez un type de <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> et placez la valeur valide dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="88511-282">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type and place the valid value in it.</span></span></p>
<p><span data-ttu-id="88511-283">Cette propriété est obligatoire pour tous les éléments WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="88511-283">This property is required for all WIA 2.0 items.</span></span> <span data-ttu-id="88511-284">Il doit être en lecture/écriture pour tous les éléments de l’acquisition WIA 2,0 et lecture uniquement pour les éléments de stockage WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="88511-284">It must be Read/Write for all WIA 2.0 acquisition enabled items and Read Only for WIA 2.0 storage items.</span></span></p>
<p><span data-ttu-id="88511-285">Type : <strong>VT_I4</strong>; Accès pour les systèmes d’exploitation antérieurs à Windows Vista : lecture/écriture ; Accès pour Windows Vista et versions ultérieures : cette propriété est en lecture seule pour les éléments WIA_CATEGORY_FOLDER et WIA_CATEGORY_FINISHED_FILE, et en lecture/écriture pour toutes les autres catégories d’éléments WIA 2,0 ; Valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="88511-285">Type: <strong>VT_I4</strong>; Access for pre-Windows Vista operating systems: Read/Write; Access for Windows Vista and later: This property is Read Only for WIA_CATEGORY_FOLDER and WIA_CATEGORY_FINISHED_FILE items, and Read/Write for all other WIA 2.0 item categories; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="88511-286">WIA_DEPTH_AUTO est défini comme 0 bits par pixel, et c’est une nouvelle valeur de propriété définie pour le WIA_IPA_DEPTH.</span><span class="sxs-lookup"><span data-stu-id="88511-286">WIA_DEPTH_AUTO is defined as 0 bits per pixel, and it is a new property value defined for the WIA_IPA_DEPTH.</span></span> <span data-ttu-id="88511-287">Cette valeur est valide pour tous les éléments de source de données d’image programmable, y compris le plateau et le chargeur.</span><span class="sxs-lookup"><span data-stu-id="88511-287">This value is valid for all programmable image data source items, including the Flatbed and Feeder.</span></span> <span data-ttu-id="88511-288">Lorsque WIA_DEPTH_AUTO est pris en charge par le mini-pilote WIA, le client d’application WIA peut définir WIA_IPA_DEPTH sur cette valeur, afin d’activer la détection automatique des couleurs au niveau de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="88511-288">When WIA_DEPTH_AUTO is supported by the WIA mini-driver, the WIA application client can set WIA_IPA_DEPTH to this value, to enable automatic color detection at the device.</span></span> <span data-ttu-id="88511-289">Lorsque WIA_DEPTH_AUTO est définie, le mini-pilote WIA doit mettre à jour WIA_IPA_DATATYPE sur le même élément à WIA_DATA_AUTO (qui doit être une valeur prise en charge, si l’appareil prend en charge la couleur automatique).</span><span class="sxs-lookup"><span data-stu-id="88511-289">When WIA_DEPTH_AUTO is set, the WIA mini-driver must update WIA_IPA_DATATYPE on the same item to WIA_DATA_AUTO (which must be a supported value, if the device supports automatic color).</span></span></p>
<p><span data-ttu-id="88511-290">WIA_DEPTH_AUTO est une valeur facultative, mais elle devient obligatoire lorsque WIA_DATA_AUTO est pris en charge pour WIA_IPA_DATATYPE.</span><span class="sxs-lookup"><span data-stu-id="88511-290">WIA_DEPTH_AUTO is an optional value, but it becomes required when WIA_DATA_AUTO is supported for WIA_IPA_DATATYPE.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FILENAME_EXTENSION"></span><span id="wia_ipa_filename_extension"></span><dl> <span data-ttu-id="88511-291"><dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-291"><dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-292">Contient l’extension de nom de fichier pour un format de fichier particulier.</span><span class="sxs-lookup"><span data-stu-id="88511-292">Contains the file name extension for a particular file format.</span></span> <span data-ttu-id="88511-293">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-293">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="88511-294">Facultatif pour tous les éléments WIA 2,0 avec transfert.</span><span class="sxs-lookup"><span data-stu-id="88511-294">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="88511-295">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-295">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="88511-296">Le pilote met à jour cette propriété pour refléter la valeur actuelle de la propriété <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> .</span><span class="sxs-lookup"><span data-stu-id="88511-296">The driver updates this property to reflect the current value of the <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> property.</span></span></p>
<p><span data-ttu-id="88511-297">Par exemple, si <strong>WIA_IPA_FORMAT</strong> est WiaImgFmt_JPEG, <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> doit être <strong>jpg</strong>.</span><span class="sxs-lookup"><span data-stu-id="88511-297">For example, if <strong>WIA_IPA_FORMAT</strong> is WiaImgFmt_JPEG, then <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> should be <strong>jpg</strong>.</span></span> <span data-ttu-id="88511-298">Si <strong>WIA_IPA_FORMAT</strong> est WiaImgFmt_BMP, WIA_IPA_FILENAME_EXTENSION doit être BMP.</span><span class="sxs-lookup"><span data-stu-id="88511-298">If <strong>WIA_IPA_FORMAT</strong> is WiaImgFmt_BMP, then WIA_IPA_FILENAME_EXTENSION should be BMP.</span></span></p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="88511-299">L’extension de nom de fichier n’inclut pas le point.</span><span class="sxs-lookup"><span data-stu-id="88511-299">The file name extension does not include the dot.</span></span>
</blockquote>
</div>
<div>
 
</div>
<p><span data-ttu-id="88511-300">Cette propriété est recommandée pour les pilotes qui prennent en charge les formats standard et est requise pour les pilotes qui implémentent des formats définis personnalisés.</span><span class="sxs-lookup"><span data-stu-id="88511-300">This property is recommended for drivers that support standard formats and is required for drivers that implement custom-defined formats.</span></span> <span data-ttu-id="88511-301">Il informe l’application de l’extension de nom de fichier correcte à utiliser pendant le transfert de fichiers au format privé.</span><span class="sxs-lookup"><span data-stu-id="88511-301">It informs the application of the correct file name extension to use during the transfer of privately formatted files.</span></span> <span data-ttu-id="88511-302">Par exemple, si A. Datum Corporation a créé un pilote WIA qui a transféré un fichier dans un nouveau format, l’entreprise peut spécifier une extension d' &quot; ADC &quot; .</span><span class="sxs-lookup"><span data-stu-id="88511-302">For example, if the A. Datum Corporation created a WIA driver that transferred a file in a new format, the company could specify an extension of &quot;adc&quot;.</span></span> <span data-ttu-id="88511-303">Cela permet aux applications de transférer des données dans ce format vers un fichier et de créer un nom de fichier tel que <em>MyFile. ADC</em>, ce qui est utile pour les personnes qui comprennent la nouvelle extension.</span><span class="sxs-lookup"><span data-stu-id="88511-303">This allows applications to transfer data in that format to a file and to create a file name such as <em>myfile.adc</em>,which is useful to others who understand the new extension.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_FORMAT"></span><span id="wia_ipa_format"></span><dl> <span data-ttu-id="88511-304"><dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-304"><dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-305">Contient le format actuel de l’image à transférer.</span><span class="sxs-lookup"><span data-stu-id="88511-305">Contains the current format of the image about to be transferred.</span></span></p>
<p><span data-ttu-id="88511-306">Une application lit cette propriété pour déterminer le format de l’image à recevoir.</span><span class="sxs-lookup"><span data-stu-id="88511-306">An application reads this property to determine the format of the image that it is about to receive.</span></span> <span data-ttu-id="88511-307">Une application écrit cette propriété pour définir le format.</span><span class="sxs-lookup"><span data-stu-id="88511-307">An application writes this property to set the format.</span></span> <span data-ttu-id="88511-308">Cette propriété dépend de la propriété <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> .</span><span class="sxs-lookup"><span data-stu-id="88511-308">This property depends on the <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> property.</span></span> <span data-ttu-id="88511-309">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-309">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="88511-310">Si l’appareil peut être défini sur une seule valeur, créez un <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type et placez la valeur valide dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="88511-310">If the device can be set to only a single value, create a <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type, and place the valid value in it.</span></span></p>
<p><span data-ttu-id="88511-311">Type : <strong>CLSID</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="88511-311">Type: <strong>CLSID</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="88511-312">Le tableau suivant répertorie les constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-312">The following table lists the constants that are valid with this property.</span></span> <span data-ttu-id="88511-313">L’astérisque (\*) indique que la constante n’est pas prise en charge dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="88511-313">The asterisk \* indicates that the constant is not supported in Windows Vista.</span></span> <span data-ttu-id="88511-314">(Disponible uniquement par le biais de l’interface <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> .) Le double astérisque \* \* indique que la constante n’est pas prise en charge dans Windows Server 2003 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="88511-314">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.) The double asterisk \*\* indicates that the constant is not supported in either Windows Server 2003 or Windows Vista.</span></span> <span data-ttu-id="88511-315">Le symbole <strong>V</strong> indique que la constante est prise en charge uniquement dans Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="88511-315">The <strong>V</strong> symbol indicates that the constant is supported only in Windows Vista and later.</span></span> <span data-ttu-id="88511-316">(Disponible uniquement par le biais de l’interface <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .)</span><span class="sxs-lookup"><span data-stu-id="88511-316">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="88511-317">Format</span><span class="sxs-lookup"><span data-stu-id="88511-317">Format</span></span></th>
<th><span data-ttu-id="88511-318">Description</span><span class="sxs-lookup"><span data-stu-id="88511-318">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88511-319">WiaAudFmt_AIFF</span><span class="sxs-lookup"><span data-stu-id="88511-319">WiaAudFmt_AIFF</span></span></td>
<td><span data-ttu-id="88511-320">Format audio AIFF</span><span class="sxs-lookup"><span data-stu-id="88511-320">AIFF audio format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-321">WiaAudFmt_MP3</span><span class="sxs-lookup"><span data-stu-id="88511-321">WiaAudFmt_MP3</span></span></td>
<td><span data-ttu-id="88511-322">Format audio MP3</span><span class="sxs-lookup"><span data-stu-id="88511-322">MP3 audio format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-323">WiaAudFmt_WAV</span><span class="sxs-lookup"><span data-stu-id="88511-323">WiaAudFmt_WAV</span></span></td>
<td><span data-ttu-id="88511-324">Format audio WAV</span><span class="sxs-lookup"><span data-stu-id="88511-324">WAV audio format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-325">WiaAudFmt_WMA</span><span class="sxs-lookup"><span data-stu-id="88511-325">WiaAudFmt_WMA</span></span></td>
<td><span data-ttu-id="88511-326">Format audio WMA</span><span class="sxs-lookup"><span data-stu-id="88511-326">WMA audio format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-327">WiaImgFmt_ASF \* \*</span><span class="sxs-lookup"><span data-stu-id="88511-327">WiaImgFmt_ASF\*\*</span></span></td>
<td><span data-ttu-id="88511-328">Format vidéo ASF</span><span class="sxs-lookup"><span data-stu-id="88511-328">ASF video format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-329">WiaImgFmt_AVI \* \*</span><span class="sxs-lookup"><span data-stu-id="88511-329">WiaImgFmt_AVI\*\*</span></span></td>
<td><span data-ttu-id="88511-330">Format vidéo AVI</span><span class="sxs-lookup"><span data-stu-id="88511-330">AVI video format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-331">WiaImgFmt_BMP</span><span class="sxs-lookup"><span data-stu-id="88511-331">WiaImgFmt_BMP</span></span></td>
<td><span data-ttu-id="88511-332">Bitmap Windows avec un fichier d’en-tête</span><span class="sxs-lookup"><span data-stu-id="88511-332">Windows bitmap with a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-333">WiaImgFmt_CIFF \*</span><span class="sxs-lookup"><span data-stu-id="88511-333">WiaImgFmt_CIFF\*</span></span></td>
<td><span data-ttu-id="88511-334">Format du fichier image de l’appareil photo</span><span class="sxs-lookup"><span data-stu-id="88511-334">Camera Image File format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-335">WiaImgFmt_DPOF</span><span class="sxs-lookup"><span data-stu-id="88511-335">WiaImgFmt_DPOF</span></span></td>
<td><span data-ttu-id="88511-336">Format d’impression DPOF</span><span class="sxs-lookup"><span data-stu-id="88511-336">DPOF printing format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-337">WiaImgFmt_EMF</span><span class="sxs-lookup"><span data-stu-id="88511-337">WiaImgFmt_EMF</span></span></td>
<td><span data-ttu-id="88511-338">Métafichier Windows étendu</span><span class="sxs-lookup"><span data-stu-id="88511-338">Extended Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-339">WiaImgFmt_EXEC</span><span class="sxs-lookup"><span data-stu-id="88511-339">WiaImgFmt_EXEC</span></span></td>
<td><span data-ttu-id="88511-340">Fichier exécutable</span><span class="sxs-lookup"><span data-stu-id="88511-340">Executable file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-341">WiaImgFmt_EXIF</span><span class="sxs-lookup"><span data-stu-id="88511-341">WiaImgFmt_EXIF</span></span></td>
<td><span data-ttu-id="88511-342">Format de fichier Exchanger</span><span class="sxs-lookup"><span data-stu-id="88511-342">Exchangeable File Format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-343">WiaImgFmt_FLASHPIX</span><span class="sxs-lookup"><span data-stu-id="88511-343">WiaImgFmt_FLASHPIX</span></span></td>
<td><span data-ttu-id="88511-344">Format FlashPix</span><span class="sxs-lookup"><span data-stu-id="88511-344">FlashPix format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-345">WiaImgFmt_GIF</span><span class="sxs-lookup"><span data-stu-id="88511-345">WiaImgFmt_GIF</span></span></td>
<td><span data-ttu-id="88511-346">Format d’image GIF</span><span class="sxs-lookup"><span data-stu-id="88511-346">GIF image format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-347">WiaImgFmt_HTML</span><span class="sxs-lookup"><span data-stu-id="88511-347">WiaImgFmt_HTML</span></span></td>
<td><span data-ttu-id="88511-348">Format HTML</span><span class="sxs-lookup"><span data-stu-id="88511-348">HTML format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-349">WiaImgFmt_ICO</span><span class="sxs-lookup"><span data-stu-id="88511-349">WiaImgFmt_ICO</span></span></td>
<td><span data-ttu-id="88511-350">Format de fichier des icônes Windows</span><span class="sxs-lookup"><span data-stu-id="88511-350">Windows icon file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-351">WiaImgFmt_JBIG<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="88511-351">WiaImgFmt_JBIG<strong>V</strong></span></span></td>
<td><span data-ttu-id="88511-352">Le format JBIG (collaboration image experts Group).</span><span class="sxs-lookup"><span data-stu-id="88511-352">The Joint Bi-level Image Experts Group (JBIG) format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-353">WiaImgFmt_JPEG</span><span class="sxs-lookup"><span data-stu-id="88511-353">WiaImgFmt_JPEG</span></span></td>
<td><span data-ttu-id="88511-354">Format compressé JPEG</span><span class="sxs-lookup"><span data-stu-id="88511-354">JPEG compressed format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-355">WiaImgFmt_JPEG2K</span><span class="sxs-lookup"><span data-stu-id="88511-355">WiaImgFmt_JPEG2K</span></span></td>
<td><span data-ttu-id="88511-356">Format compressé JPEG 2000</span><span class="sxs-lookup"><span data-stu-id="88511-356">JPEG 2000 compressed format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-357">WiaImgFmt_JPEG2KX</span><span class="sxs-lookup"><span data-stu-id="88511-357">WiaImgFmt_JPEG2KX</span></span></td>
<td><span data-ttu-id="88511-358">Format compressé JPEG 2000</span><span class="sxs-lookup"><span data-stu-id="88511-358">JPEG 2000 compressed format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-359">WiaImgFmt_MEMORYBMP</span><span class="sxs-lookup"><span data-stu-id="88511-359">WiaImgFmt_MEMORYBMP</span></span></td>
<td><span data-ttu-id="88511-360">Bitmap Windows sans fichier d’en-tête</span><span class="sxs-lookup"><span data-stu-id="88511-360">Windows bitmap without a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-361">WiaImgFmt_PDFA<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="88511-361">WiaImgFmt_PDFA<strong>V</strong></span></span></td>
<td><span data-ttu-id="88511-362">Format PDF/A (ISO/CD 19005-1).</span><span class="sxs-lookup"><span data-stu-id="88511-362">The PDF/A (ISO/CD 19005-1) format.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-363">WiaImgFmt_MPG \* \*</span><span class="sxs-lookup"><span data-stu-id="88511-363">WiaImgFmt_MPG\*\*</span></span></td>
<td><span data-ttu-id="88511-364">Format vidéo MPEG</span><span class="sxs-lookup"><span data-stu-id="88511-364">MPEG video format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-365">WiaImgFmt_PHOTOCD</span><span class="sxs-lookup"><span data-stu-id="88511-365">WiaImgFmt_PHOTOCD</span></span></td>
<td><span data-ttu-id="88511-366">Format de fichier Eastman Kodak</span><span class="sxs-lookup"><span data-stu-id="88511-366">Eastman Kodak file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-367">WiaImgFmt_PICT</span><span class="sxs-lookup"><span data-stu-id="88511-367">WiaImgFmt_PICT</span></span></td>
<td><span data-ttu-id="88511-368">Format de fichier Apple</span><span class="sxs-lookup"><span data-stu-id="88511-368">Apple file format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-369">WiaImgFmt_PNG</span><span class="sxs-lookup"><span data-stu-id="88511-369">WiaImgFmt_PNG</span></span></td>
<td><span data-ttu-id="88511-370">Format PNG W3C</span><span class="sxs-lookup"><span data-stu-id="88511-370">W3C PNG format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-371">WiaImgFmt_RAW</span><span class="sxs-lookup"><span data-stu-id="88511-371">WiaImgFmt_RAW</span></span></td>
<td><span data-ttu-id="88511-372">Format brut pour les transferts de données uniquement</span><span class="sxs-lookup"><span data-stu-id="88511-372">Raw format for data transfers only</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-373">WiaImgFmt_RAWRGB</span><span class="sxs-lookup"><span data-stu-id="88511-373">WiaImgFmt_RAWRGB</span></span></td>
<td><span data-ttu-id="88511-374">Format RVB brut</span><span class="sxs-lookup"><span data-stu-id="88511-374">Raw RGB format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-375">WiaImgFmt_RTF</span><span class="sxs-lookup"><span data-stu-id="88511-375">WiaImgFmt_RTF</span></span></td>
<td><span data-ttu-id="88511-376">Format de fichier texte enrichi</span><span class="sxs-lookup"><span data-stu-id="88511-376">Rich Text File format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-377">WiaImgFmt_SCRIPT</span><span class="sxs-lookup"><span data-stu-id="88511-377">WiaImgFmt_SCRIPT</span></span></td>
<td><span data-ttu-id="88511-378">Fichier de script</span><span class="sxs-lookup"><span data-stu-id="88511-378">Script file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-379">WiaImgFmt_TIFF</span><span class="sxs-lookup"><span data-stu-id="88511-379">WiaImgFmt_TIFF</span></span></td>
<td><span data-ttu-id="88511-380">Tag Image File Format (TIFF)</span><span class="sxs-lookup"><span data-stu-id="88511-380">Tag Image File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-381">WiaImgFmt_TXT</span><span class="sxs-lookup"><span data-stu-id="88511-381">WiaImgFmt_TXT</span></span></td>
<td><span data-ttu-id="88511-382">Fichier texte</span><span class="sxs-lookup"><span data-stu-id="88511-382">Text file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-383">WiaImgFmt_UNICODE16</span><span class="sxs-lookup"><span data-stu-id="88511-383">WiaImgFmt_UNICODE16</span></span></td>
<td><span data-ttu-id="88511-384">Encodage UNICODE 16 bits</span><span class="sxs-lookup"><span data-stu-id="88511-384">UNICODE 16-bit encoding</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-385">WiaImgFmt_WMF</span><span class="sxs-lookup"><span data-stu-id="88511-385">WiaImgFmt_WMF</span></span></td>
<td><span data-ttu-id="88511-386">Métafichier Windows</span><span class="sxs-lookup"><span data-stu-id="88511-386">Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-387">WiaImgFmt_XML</span><span class="sxs-lookup"><span data-stu-id="88511-387">WiaImgFmt_XML</span></span></td>
<td><span data-ttu-id="88511-388">Fichier XML</span><span class="sxs-lookup"><span data-stu-id="88511-388">XML file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-389">WiaImgFmt_XPS<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="88511-389">WiaImgFmt_XPS<strong>V</strong></span></span></td>
<td><span data-ttu-id="88511-390">Format de package XPS</span><span class="sxs-lookup"><span data-stu-id="88511-390">XPS Package format</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="88511-391">Lorsque cette propriété a la valeur WiaImgFmt_PDFA ou WiaImgFmt_XPS, et WIA_IPA_COMPRESSION est WIA_COMPRESSION_NONE ; la dernière valeur signifie que le mode de compression n’est pas défini et que le scanneur doit décider d’un mode.</span><span class="sxs-lookup"><span data-stu-id="88511-391">When this property is either WiaImgFmt_PDFA or WiaImgFmt_XPS, and WIA_IPA_COMPRESSION is WIA_COMPRESSION_NONE; then the latter value means that the compression mode is undefined and the scanner must decide on a mode.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FULL_ITEM_NAME"></span><span id="wia_ipa_full_item_name"></span><dl> <span data-ttu-id="88511-392"><dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-392"><dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-393">Contient le nom complet de l’élément (nom de l’élément, ainsi que les informations relatives au chemin d’accès).</span><span class="sxs-lookup"><span data-stu-id="88511-393">Contains the full item name (the item name together with path information).</span></span> <span data-ttu-id="88511-394">Le nom complet de l’élément est le même que le paramètre <em>bstrFullItemName</em> de la fonction de l’utilitaire de service <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> .</span><span class="sxs-lookup"><span data-stu-id="88511-394">The full item name is the same as the <em>bstrFullItemName</em> parameter of the <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> service utility function.</span></span> <span data-ttu-id="88511-395">Une application lit cette propriété pour déterminer l’élément utilisé actuellement et l’emplacement où se trouve cet élément dans l’arborescence des éléments.</span><span class="sxs-lookup"><span data-stu-id="88511-395">An application reads this property to determine which item it is currently using and where that item is located in the item tree.</span></span> <span data-ttu-id="88511-396">Chaque élément doit avoir un nom unique.</span><span class="sxs-lookup"><span data-stu-id="88511-396">Each item should have a unique name.</span></span> <span data-ttu-id="88511-397">Les applications utilisent généralement le nom complet de l’élément pour rechercher des éléments dans l’arborescence des éléments.</span><span class="sxs-lookup"><span data-stu-id="88511-397">Applications commonly use the full item name to search for items in the item tree.</span></span> <span data-ttu-id="88511-398">Le service WIA crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-398">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="88511-399">Obligatoire pour tous les éléments WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="88511-399">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="88511-400">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-400">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_GAMMA_CURVES"></span><span id="wia_ipa_gamma_curves"></span><dl> <span data-ttu-id="88511-401"><dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-401"><dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-402">Cette propriété est réservée à une utilisation future et n’est pas implémentée pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="88511-402">This property is reserved for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="88511-403">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-403">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ICM_PROFILE_NAME"></span><span id="wia_ipa_icm_profile_name"></span><dl> <span data-ttu-id="88511-404"><dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-404"><dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-405">Contient le nom du profil ICM requis pour décoder correctement l’image.</span><span class="sxs-lookup"><span data-stu-id="88511-405">Contains the ICM profile name that is needed to properly decode the image.</span></span> <span data-ttu-id="88511-406">Une application lit cette propriété pour déterminer le profil ICM à utiliser lors du traitement de l’image.</span><span class="sxs-lookup"><span data-stu-id="88511-406">An application reads this property to determine the ICM profile to use when processing the image.</span></span> <span data-ttu-id="88511-407">Le service WIA crée et gère cette propriété en fonction de l’entrée ICMProfiles dans le fichier d’installation du pilote.</span><span class="sxs-lookup"><span data-stu-id="88511-407">The WIA service creates and maintains this property based on the ICMProfiles entry in the driver installation file.</span></span></p>
<p><span data-ttu-id="88511-408">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-408">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_CATEGORY"></span><span id="wia_ipa_item_category"></span><dl> <span data-ttu-id="88511-409"><dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-409"><dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-410">Pris en charge uniquement dans Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="88511-410">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="88511-411">Les éléments WIA 2,0 sont regroupés en catégories qui définissent la façon dont un <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> doit être traité ou utilisé.</span><span class="sxs-lookup"><span data-stu-id="88511-411">WIA 2.0 items are grouped into categories that define how a <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> is to be treated or used.</span></span> <span data-ttu-id="88511-412">Par exemple, si l’élément représente un flux, l’application doit s’attendre à ce qu’il contienne les propriétés du chargeur de documents requis et fonctionne comme un chargeur de documents.</span><span class="sxs-lookup"><span data-stu-id="88511-412">For example, If the item represents a feeder, then the application should expect it to contain the required document feeder properties and operate like a document feeder.</span></span> <span data-ttu-id="88511-413">Si l’élément représente un fichier fini, une application WIA 2,0 doit la traiter ainsi, en supposant que les données sont statiques et situées sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="88511-413">If the item represents a finished file, then a WIA 2.0 application should treat it that way, assuming that the data is static and located on the device.</span></span> <span data-ttu-id="88511-414">(Les règles pour chaque élément sont définies dans leurs documents de spécification individuels.)</span><span class="sxs-lookup"><span data-stu-id="88511-414">(The rules for each item will be defined in their individual specification documents.)</span></span></p>
<p><span data-ttu-id="88511-415">Obligatoire pour tous les éléments WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="88511-415">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="88511-416">Type : <strong>VT_CLSID</strong>, Access : lecture seule, valeurs valides : <a href="-wia-wia2-itemcategoryguids.md"><strong>GUID de catégorie d’élément</strong></a></span><span class="sxs-lookup"><span data-stu-id="88511-416">Type: <strong>VT_CLSID</strong>, Access: Read Only, Valid values: <a href="-wia-wia2-itemcategoryguids.md"><strong>Item Category GUIDs</strong></a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_FLAGS"></span><span id="wia_ipa_item_flags"></span><dl> <span data-ttu-id="88511-417"><dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-417"><dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-418">Contient les indicateurs descriptifs pour un élément WIA.</span><span class="sxs-lookup"><span data-stu-id="88511-418">Contains the descriptive flags for a WIA item.</span></span> <span data-ttu-id="88511-419">Les indicateurs d’élément sont les mêmes que ceux du paramètre <em>lObjectFlags</em> de la fonction de l’utilitaire de service <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> .</span><span class="sxs-lookup"><span data-stu-id="88511-419">The item flags are the same as those in the <em>lObjectFlags</em> parameter of the <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> service utility function.</span></span> <span data-ttu-id="88511-420">Le service WIA crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-420">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="88511-421">Une application lit cette propriété pour déterminer les valeurs d’indicateur descriptives de l’élément.</span><span class="sxs-lookup"><span data-stu-id="88511-421">An application reads this property to determine the item's descriptive flag values.</span></span></p>
<p><span data-ttu-id="88511-422">Type : <strong>VT_I4</strong> accès : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-422">Type: <strong>VT_I4</strong> Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="88511-423">Le tableau suivant contient les indicateurs qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-423">The following table has the flags that are valid with this property.</span></span> <span data-ttu-id="88511-424">Un astérisque \* indique que l’indicateur n’est pas pris en charge dans Windows Vista ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="88511-424">An asterisk \* indicates that the flag is not supported in Windows Vista or later.</span></span> <span data-ttu-id="88511-425">(Disponible uniquement par le biais de l’interface <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> .) Un double astérisque \* \* indique que l’indicateur n’est pas pris en charge dans Windows Server 2003 ou Windows Vista ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="88511-425">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.) An double asterisk \*\* indicates that the flag is not supported in either Windows Server 2003 or Windows Vista or later.</span></span> <span data-ttu-id="88511-426">Le symbole <strong>V</strong> indique que l’indicateur est pris en charge uniquement dans Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="88511-426">The <strong>V</strong> symbol indicates that the flag is supported only in Windows Vista and later.</span></span> <span data-ttu-id="88511-427">(Disponible uniquement par le biais de l’interface <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .)</span><span class="sxs-lookup"><span data-stu-id="88511-427">(It is only available through the <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="88511-428">Indicateur</span><span class="sxs-lookup"><span data-stu-id="88511-428">Flag</span></span></th>
<th><span data-ttu-id="88511-429">Définition</span><span class="sxs-lookup"><span data-stu-id="88511-429">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88511-430">WiaItemTypeAnalyze\*</span><span class="sxs-lookup"><span data-stu-id="88511-430">WiaItemTypeAnalyze\*</span></span></td>
<td><span data-ttu-id="88511-431">Cet élément prend en charge la méthode <strong>IWiaItem :: AnalyzeItem</strong> (décrite dans la documentation du kit de développement Platform SDK).</span><span class="sxs-lookup"><span data-stu-id="88511-431">This item supports the <strong>IWiaItem::AnalyzeItem</strong> method (described in the Platform SDK documentation).</span></span> <span data-ttu-id="88511-432">Cet élément prend également en charge la génération automatique d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="88511-432">This item also supports automatic child item generation.</span></span> <span data-ttu-id="88511-433">Cette fonctionnalité est utile pour la détection des régions ou la décomposition des pages.</span><span class="sxs-lookup"><span data-stu-id="88511-433">This capability is useful for region detection or page decomposition.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-434">WiaItemTypeAudio</span><span class="sxs-lookup"><span data-stu-id="88511-434">WiaItemTypeAudio</span></span></td>
<td><span data-ttu-id="88511-435">Cet élément prend en charge l’audio.</span><span class="sxs-lookup"><span data-stu-id="88511-435">This item supports audio.</span></span> <span data-ttu-id="88511-436">Cet indicateur n’est valide que pour les éléments dont l’indicateur <strong>WiaItemTypeFile</strong> est également défini.</span><span class="sxs-lookup"><span data-stu-id="88511-436">This flag is valid only for items that also have the <strong>WiaItemTypeFile</strong> flag set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-437">WiaItemTypeBurst\*</span><span class="sxs-lookup"><span data-stu-id="88511-437">WiaItemTypeBurst\*</span></span></td>
<td><span data-ttu-id="88511-438">Pour les dossiers uniquement.</span><span class="sxs-lookup"><span data-stu-id="88511-438">For folders only.</span></span> <span data-ttu-id="88511-439">Cet indicateur indique que les images de ce dossier ont été prises dans une séquence temporelle continue.</span><span class="sxs-lookup"><span data-stu-id="88511-439">This flag indicates that the images in this folder were taken in a continuous time sequence.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-440">WiaItemTypeDeleted</span><span class="sxs-lookup"><span data-stu-id="88511-440">WiaItemTypeDeleted</span></span></td>
<td><span data-ttu-id="88511-441">Cet élément est marqué pour suppression, cet élément a été supprimé, cet élément n’existe pas ou le contenu de cet élément n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="88511-441">This item is marked for deletion, this item has been deleted, this item does not exist, or the contents of this item are invalid.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-442">WiaItemTypeDocument<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="88511-442">WiaItemTypeDocument<strong>V</strong></span></span></td>
<td><span data-ttu-id="88511-443">Cet élément est un fichier de document dans l’un des formats de document que contient la propriété <strong>WIA_IPA_FORMAT</strong> .</span><span class="sxs-lookup"><span data-stu-id="88511-443">This item is a document file in one of the document formats that the <strong>WIA_IPA_FORMAT</strong> property contains.</span></span> <span data-ttu-id="88511-444">(Ces formats incluent ceux des fichiers autres que des fichiers. txt,. htm et. doc.)</span><span class="sxs-lookup"><span data-stu-id="88511-444">(These formats include those for nonimage files, such as .txt, .htm, and .doc files.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-445">WiaItemTypeDevice</span><span class="sxs-lookup"><span data-stu-id="88511-445">WiaItemTypeDevice</span></span></td>
<td><span data-ttu-id="88511-446">Cet élément représente un appareil connecté.</span><span class="sxs-lookup"><span data-stu-id="88511-446">This item represents a connected device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-447">WiaItemTypeDisconnected</span><span class="sxs-lookup"><span data-stu-id="88511-447">WiaItemTypeDisconnected</span></span></td>
<td><span data-ttu-id="88511-448">Cet élément représente un appareil déconnecté.</span><span class="sxs-lookup"><span data-stu-id="88511-448">This item represents a disconnected device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-449">WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="88511-449">WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="88511-450">L’élément prend en charge les transferts de fichiers.</span><span class="sxs-lookup"><span data-stu-id="88511-450">The item supports file transfers.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-451">WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="88511-451">WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="88511-452">L’élément est un dossier.</span><span class="sxs-lookup"><span data-stu-id="88511-452">The item is a folder.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-453">WiaItemTypeFree</span><span class="sxs-lookup"><span data-stu-id="88511-453">WiaItemTypeFree</span></span></td>
<td><span data-ttu-id="88511-454">L’élément n’est pas initialisé ou a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="88511-454">The item is uninitialized or has been deleted.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-455">WiaItemTypeGenerated</span><span class="sxs-lookup"><span data-stu-id="88511-455">WiaItemTypeGenerated</span></span></td>
<td><span data-ttu-id="88511-456">Cet élément a été généré par une application ou par le pilote.</span><span class="sxs-lookup"><span data-stu-id="88511-456">This item has been generated by an application or by the driver.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-457">WiaItemTypeHasAttachments\*</span><span class="sxs-lookup"><span data-stu-id="88511-457">WiaItemTypeHasAttachments\*</span></span></td>
<td><span data-ttu-id="88511-458">Cet élément prend en charge les pièces jointes et contient actuellement des pièces jointes.</span><span class="sxs-lookup"><span data-stu-id="88511-458">This item supports attachments and currently contains attachments.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-459">WiaItemTypeHPanorama\*</span><span class="sxs-lookup"><span data-stu-id="88511-459">WiaItemTypeHPanorama\*</span></span></td>
<td><span data-ttu-id="88511-460">Cet élément représente une image panoramique horizontale.</span><span class="sxs-lookup"><span data-stu-id="88511-460">This item represents a horizontal panoramic image.</span></span> <span data-ttu-id="88511-461">Cet indicateur n’est valide que pour les éléments dont l’indicateur <strong>WiaItemTypeFolder</strong> est également défini.</span><span class="sxs-lookup"><span data-stu-id="88511-461">This flag is valid only for items that also have the <strong>WiaItemTypeFolder</strong> flag set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-462">WiaItemTypeImage</span><span class="sxs-lookup"><span data-stu-id="88511-462">WiaItemTypeImage</span></span></td>
<td><span data-ttu-id="88511-463">L’élément est un fichier image.</span><span class="sxs-lookup"><span data-stu-id="88511-463">The item is an image file.</span></span> <span data-ttu-id="88511-464">Cet indicateur n’est valide que pour les éléments dont l’indicateur <strong>WiaItemTypeFile</strong> est également défini.</span><span class="sxs-lookup"><span data-stu-id="88511-464">This flag is valid only for items that also have the <strong>WiaItemTypeFile</strong> flag set.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-465">WiaItemTypeProgrammableDataSource<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="88511-465">WiaItemTypeProgrammableDataSource<strong>V</strong></span></span></td>
<td><span data-ttu-id="88511-466">L’élément est une source de données programmable et suit un ensemble de règles de configuration prédéfinies, qui sont basées sur <strong>WIA_IPA_ITEM_CATEGORY</strong>.</span><span class="sxs-lookup"><span data-stu-id="88511-466">The item is a programmable data source and follows a set of predefined configuration rules, which are based on <strong>WIA_IPA_ITEM_CATEGORY</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-467">WiaItemTypeRoot<strong>V</strong></span><span class="sxs-lookup"><span data-stu-id="88511-467">WiaItemTypeRoot<strong>V</strong></span></span></td>
<td><span data-ttu-id="88511-468">Cet élément est l’élément racine, qui est le parent de tous les éléments de fonctionnalité pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="88511-468">This item is the root item, which is the parent to all the feature items that the device supports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-469">WiaItemTypeStorage</span><span class="sxs-lookup"><span data-stu-id="88511-469">WiaItemTypeStorage</span></span></td>
<td><span data-ttu-id="88511-470">Cet indicateur indique un stockage supplémentaire pour les éléments de dossiers.</span><span class="sxs-lookup"><span data-stu-id="88511-470">This flag indicates additional storage for folders items.</span></span> <span data-ttu-id="88511-471">Les pilotes WIA spécifient leurs éléments en termes d’images et de dossiers.</span><span class="sxs-lookup"><span data-stu-id="88511-471">WIA drivers specify their items in terms of images and folders.</span></span> <span data-ttu-id="88511-472">Il n’existe pas de propriétés WIA qui décrivent les caractéristiques d’un élément de stockage (par exemple, l’espace de stockage restant, la vitesse d’écriture ou le type de média restant).</span><span class="sxs-lookup"><span data-stu-id="88511-472">No WIA properties exist that describe the characteristics of a storage item (such as remaining storage space, write speed, or type of media.</span></span> <span data-ttu-id="88511-473">Les propriétés spécifiques au fournisseur qui exposent ces informations peuvent être ajoutées.</span><span class="sxs-lookup"><span data-stu-id="88511-473">Vendor-specific properties that expose this information can be added.</span></span> <span data-ttu-id="88511-474">Ces propriétés sont accessibles uniquement aux applications ou extensions écrites pour les reconnaître.</span><span class="sxs-lookup"><span data-stu-id="88511-474">These properties are accessible only to applications or extensions that are written to recognize them.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-475">WiaItemTypeTransfer</span><span class="sxs-lookup"><span data-stu-id="88511-475">WiaItemTypeTransfer</span></span></td>
<td><span data-ttu-id="88511-476">Cet élément peut être utilisé pour transférer des données.</span><span class="sxs-lookup"><span data-stu-id="88511-476">This item can be used to transfer data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-477">WiaItemTypeTwainCapabilityPassThrough</span><span class="sxs-lookup"><span data-stu-id="88511-477">WiaItemTypeTwainCapabilityPassThrough</span></span></td>
<td><span data-ttu-id="88511-478">Ce type indique que l’appareil WIA est en mesure de recevoir les données de capacité TWAIN de la couche de compatibilité TWAIN.</span><span class="sxs-lookup"><span data-stu-id="88511-478">This type indicates that the WIA device is able to receive TWAIN capability data from the TWAIN compatibility layer.</span></span> <span data-ttu-id="88511-479">Si ce type est défini, toute fonctionnalité TWAIN qui n’est pas comprise par la couche de compatibilité TWAIN sera transmise au pilote theWIA.</span><span class="sxs-lookup"><span data-stu-id="88511-479">If this type is set, any TWAIN capability that is not understood by the TWAIN compatibility layer will be passed to theWIA driver.</span></span> <span data-ttu-id="88511-480">Cela est valide uniquement pour l’élément racine.</span><span class="sxs-lookup"><span data-stu-id="88511-480">This is valid only for the root item.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-481">WiaItemTypeVideo\*\*</span><span class="sxs-lookup"><span data-stu-id="88511-481">WiaItemTypeVideo\*\*</span></span></td>
<td><span data-ttu-id="88511-482">Cet élément prend en charge la vidéo en continu.</span><span class="sxs-lookup"><span data-stu-id="88511-482">This item supports streaming video.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-483">WiaItemTypeVPanorama\*</span><span class="sxs-lookup"><span data-stu-id="88511-483">WiaItemTypeVPanorama\*</span></span></td>
<td><span data-ttu-id="88511-484">Cet élément représente une image panoramique verticale.</span><span class="sxs-lookup"><span data-stu-id="88511-484">This item represents a vertical panoramic image.</span></span> <span data-ttu-id="88511-485">Cet indicateur n’est valide que pour les éléments dont l’indicateur <strong>WiaItemTypeFolder</strong> est également défini.</span><span class="sxs-lookup"><span data-stu-id="88511-485">This flag is valid only for items that also have the <strong>WiaItemTypeFolder</strong> flag set.</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="88511-486">Certains de ces indicateurs sont obligatoires ou facultatifs pour les éléments WIA 2,0, en fonction de la catégorie de l’élément, comme indiqué dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="88511-486">Some of these flags are required or optional for WIA 2.0 items, according to the category of the item, as shown in this table.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="88511-487">Catégorie d’élément</span><span class="sxs-lookup"><span data-stu-id="88511-487">Category of Item</span></span></th>
<th><span data-ttu-id="88511-488">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="88511-488">Required</span></span></th>
<th><span data-ttu-id="88511-489">Facultatif</span><span class="sxs-lookup"><span data-stu-id="88511-489">Optional</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88511-490">WIA_CATEGORY_ROOT</span><span class="sxs-lookup"><span data-stu-id="88511-490">WIA_CATEGORY_ROOT</span></span></td>
<td><span data-ttu-id="88511-491">WiaItemTypeRoot WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="88511-491">WiaItemTypeRoot WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="88511-492">WiaItemTypeDevice WiaItemTypeDisconnected</span><span class="sxs-lookup"><span data-stu-id="88511-492">WiaItemTypeDevice WiaItemTypeDisconnected</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-493">WIA_CATEGORY_FLATBED</span><span class="sxs-lookup"><span data-stu-id="88511-493">WIA_CATEGORY_FLATBED</span></span></td>
<td><span data-ttu-id="88511-494">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="88511-494">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="88511-495">WiaItemTypeFolder (si plusieurs éléments de régions d’analyse sont pris en charge, cet indicateur est facultatif uniquement pour l’élément racine WIA_CATEGORY_FLATBED.)</span><span class="sxs-lookup"><span data-stu-id="88511-495">WiaItemTypeFolder (If multiple scan regions items are supported, this flag is optional only for the WIA_CATEGORY_FLATBED root item.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-496">WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</span><span class="sxs-lookup"><span data-stu-id="88511-496">WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</span></span></td>
<td><span data-ttu-id="88511-497">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="88511-497">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="88511-498">WiaItemTypeFolder (si WIA_CATEGORY_FEEDER_FRONT et WIA_CATEGORY_FEEDER_BACK éléments sont présents, cet indicateur est facultatif uniquement pour l’élément racine WIA_CATEGORY_FEEDER).</span><span class="sxs-lookup"><span data-stu-id="88511-498">WiaItemTypeFolder (If WIA_CATEGORY_FEEDER_FRONT and WIA_CATEGORY_FEEDER_BACK items are present, then this flag is optional only for the WIA_CATEGORY_FEEDER root item.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-499">WIA_CATEGORY_FILM (racine)</span><span class="sxs-lookup"><span data-stu-id="88511-499">WIA_CATEGORY_FILM (root)</span></span></td>
<td><span data-ttu-id="88511-500">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="88511-500">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="88511-501">Aucun</span><span class="sxs-lookup"><span data-stu-id="88511-501">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-502">WIA_CATEGORY_FILM (enfants)</span><span class="sxs-lookup"><span data-stu-id="88511-502">WIA_CATEGORY_FILM (children)</span></span></td>
<td><span data-ttu-id="88511-503">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span><span class="sxs-lookup"><span data-stu-id="88511-503">WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</span></span></td>
<td><span data-ttu-id="88511-504">Aucun</span><span class="sxs-lookup"><span data-stu-id="88511-504">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-505">WIA_CATEGORY_FOLDER</span><span class="sxs-lookup"><span data-stu-id="88511-505">WIA_CATEGORY_FOLDER</span></span></td>
<td><span data-ttu-id="88511-506">WiaItemTypeStorage WiaItemTypeFolder</span><span class="sxs-lookup"><span data-stu-id="88511-506">WiaItemTypeStorage WiaItemTypeFolder</span></span></td>
<td><span data-ttu-id="88511-507">WiaItemTypeDeleted</span><span class="sxs-lookup"><span data-stu-id="88511-507">WiaItemTypeDeleted</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-508">WIA_CATEGORY_FINISHED_FILE</span><span class="sxs-lookup"><span data-stu-id="88511-508">WIA_CATEGORY_FINISHED_FILE</span></span></td>
<td><span data-ttu-id="88511-509">WiaItemTypeFile WiaItemTypeTransfer</span><span class="sxs-lookup"><span data-stu-id="88511-509">WiaItemTypeFile WiaItemTypeTransfer</span></span></td>
<td><span data-ttu-id="88511-510">WiaItemTypeImage WiaItemTypeAudio WiaItemTypeDeleted</span><span class="sxs-lookup"><span data-stu-id="88511-510">WiaItemTypeImage WiaItemTypeAudio WiaItemTypeDeleted</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_NAME"></span><span id="wia_ipa_item_name"></span><dl> <span data-ttu-id="88511-511"><dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-511"><dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-512">Contient le nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="88511-512">Contains the item name.</span></span> <span data-ttu-id="88511-513">Une application lit cette propriété pour déterminer l’élément qu’elle utilise actuellement.</span><span class="sxs-lookup"><span data-stu-id="88511-513">An application reads this property to determine which item it is currently using.</span></span> <span data-ttu-id="88511-514">Chaque élément a un nom unique.</span><span class="sxs-lookup"><span data-stu-id="88511-514">Each item has a unique name.</span></span> <span data-ttu-id="88511-515">Le service WIA crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-515">The WIA service creates and maintains this property.</span></span></p>
<p><span data-ttu-id="88511-516">Obligatoire pour tous les éléments WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="88511-516">Required for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="88511-517">Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-517">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_SIZE"></span><span id="wia_ipa_item_size"></span><dl> <span data-ttu-id="88511-518"><dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-518"><dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-519">Contient la taille actuelle, en octets, des données associées à l’élément.</span><span class="sxs-lookup"><span data-stu-id="88511-519">Contains the current size, in bytes, of the data that is associated with the item.</span></span> <span data-ttu-id="88511-520">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-520">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="88511-521">Contains correspond à la taille totale des données transférées.</span><span class="sxs-lookup"><span data-stu-id="88511-521">Contains is the total size of the data being transferred.</span></span> <span data-ttu-id="88511-522">Si cette valeur est égale à zéro, cela signifie que le minipilote n’a pas d’informations sur la taille exacte des données.</span><span class="sxs-lookup"><span data-stu-id="88511-522">If this value is zero, it means that the minidriver has no information about the exact size of the data.</span></span> <span data-ttu-id="88511-523">(Ceci est courant pour les données compressées.) Une application lit cette valeur pour déterminer la taille de l’acquisition avant qu’elle ait lieu.</span><span class="sxs-lookup"><span data-stu-id="88511-523">(This is common for compressed data.) An application reads this value to determine the size of the acquisition before it takes place.</span></span> <span data-ttu-id="88511-524">Le service WIA lit cette propriété pour aider à allouer de la mémoire pour les transferts de données.</span><span class="sxs-lookup"><span data-stu-id="88511-524">The WIA service reads this property to assist in allocating memory for data transfers.</span></span> <span data-ttu-id="88511-525">Pour plus d’informations, consultez <a href="https://msdn.microsoft.com/library/ms792198.aspx">transfert de données vers une application WIA</a> si la propriété a la valeur zéro et que TYMED est configuré pour un transfert de fichiers, le service WIA n’alloue pas de mémoire pour le minipilote WIA.</span><span class="sxs-lookup"><span data-stu-id="88511-525">For further information, see <a href="https://msdn.microsoft.com/library/ms792198.aspx">Transferring Data to a WIA Application</a> if the property is set to zero and TYMED is configured for a file transfer, the WIA service does not allocate any memory for the WIA minidriver.</span></span></p>
<p><span data-ttu-id="88511-526">Obligatoire pour tous les éléments WIA 2,0 avec transfert.</span><span class="sxs-lookup"><span data-stu-id="88511-526">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="88511-527">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-527">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_TIME"></span><span id="wia_ipa_item_time"></span><dl> <span data-ttu-id="88511-528"><dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-528"><dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-529">Contient l’heure à laquelle l’image a été capturée à l’origine.</span><span class="sxs-lookup"><span data-stu-id="88511-529">Contains the time that the image was originally captured.</span></span> <span data-ttu-id="88511-530">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-530">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="88511-531">Cette propriété doit être signalée comme un vecteur de huit valeurs de <strong>mots</strong> sous la forme d’une structure SYSTEMTIME (décrite dans la documentation du kit de développement Platform SDK).</span><span class="sxs-lookup"><span data-stu-id="88511-531">This property should be reported as a vector of eight <strong>WORD</strong> values in the form of a SYSTEMTIME structure (described in the Platform SDK documentation).</span></span></p>
<p><span data-ttu-id="88511-532">Facultatif pour tous les éléments WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="88511-532">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="88511-533">Type : <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong> accès : lecture/écriture ou lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-533">Type: <strong>VT_UI2</strong> | <strong>VT_VECTOR</strong> Access: Read/Write or Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <span data-ttu-id="88511-534"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-534"><dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-535">Pris en charge uniquement dans Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="88511-535">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="88511-536">Spécifie le nombre d’éléments stockés dans l’élément WIA_CATEGORY_FOLDER.</span><span class="sxs-lookup"><span data-stu-id="88511-536">Specifies how many items are stored in the WIA_CATEGORY_FOLDER item.</span></span></p>
<p><span data-ttu-id="88511-537">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-537">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_MIN_BUFFER_SIZE"></span><span id="wia_ipa_min_buffer_size"></span><dl> <span data-ttu-id="88511-538"><dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-538"><dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-539">Spécifie la taille de mémoire tampon minimale utilisée dans les transferts de données.</span><span class="sxs-lookup"><span data-stu-id="88511-539">Specifies the minimum buffer size that is used in data transfers.</span></span> <span data-ttu-id="88511-540">Si le transfert de données est effectué via un mécanisme de rappel, la valeur de la propriété peut être aussi petite que 64 Ko.</span><span class="sxs-lookup"><span data-stu-id="88511-540">If the data transfer is performed through a callback mechanism, the property value can be as small as 64KB.</span></span> <span data-ttu-id="88511-541">Toutefois, si le transfert est vers un fichier, la valeur de la propriété est le nombre d’octets nécessaires pour transférer une page de données à la fois.</span><span class="sxs-lookup"><span data-stu-id="88511-541">However, if the transfer is to file, the property value is the number of bytes that are needed to transfer one page of data at a time.</span></span> <span data-ttu-id="88511-542">Le minipilote crée et gère cette propriété WIA.</span><span class="sxs-lookup"><span data-stu-id="88511-542">The minidriver creates and maintains this WIA property.</span></span></p>
<p><span data-ttu-id="88511-543">Facultatif pour tous les éléments WIA 2,0 avec transfert.</span><span class="sxs-lookup"><span data-stu-id="88511-543">Optional for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="88511-544">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-544">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_NUMBER_OF_LINES"></span><span id="wia_ipa_number_of_lines"></span><dl> <span data-ttu-id="88511-545"><dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-545"><dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-546">Contient le nombre de lignes contenues dans l’image (hauteur verticale de l’image en pixels).</span><span class="sxs-lookup"><span data-stu-id="88511-546">Contains the number of lines contained in the image (the vertical height of the image in pixels).</span></span> <span data-ttu-id="88511-547">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-547">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="88511-548">Facultatif pour tous les éléments WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="88511-548">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="88511-549">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-549">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PIXELS_PER_LINE"></span><span id="wia_ipa_pixels_per_line"></span><dl> <span data-ttu-id="88511-550"><dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-550"><dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-551">Contient le nombre de pixels dans chaque ligne de l’image (la largeur de l’image en pixels).</span><span class="sxs-lookup"><span data-stu-id="88511-551">Contains the number of pixels in each line of the image (the width of the image in pixels).</span></span> <span data-ttu-id="88511-552">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-552">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="88511-553">Facultatif pour tous les éléments WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="88511-553">Optional for all WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="88511-554">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-554">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PLANAR"></span><span id="wia_ipa_planar"></span><dl> <span data-ttu-id="88511-555"><dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-555"><dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-556">Cette propriété n’est pas prise en charge dans Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="88511-556">This property is not supported in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="88511-557">Contient les options de compression des données d’image.</span><span class="sxs-lookup"><span data-stu-id="88511-557">Contains image data packing options.</span></span> <span data-ttu-id="88511-558">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-558">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="88511-559">Une application lit cette propriété pour déterminer les options de compression d’image ou définit les options de compression d’image actuelles.</span><span class="sxs-lookup"><span data-stu-id="88511-559">An application reads this property to determine the image packing options or sets the current image packing options.</span></span></p>
<p><span data-ttu-id="88511-560">Type : <strong>VT_I4</strong>; Accès : lecture/écriture ; Valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span><span class="sxs-lookup"><span data-stu-id="88511-560">Type: <strong>VT_I4</strong>; Access: Read/Write; Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>.</span></span> <span data-ttu-id="88511-561">Si l’appareil peut être défini sur une seule valeur, créez un type de WIA_PROP_LIST et placez la valeur valide dans celui-ci.</span><span class="sxs-lookup"><span data-stu-id="88511-561">If the device can be set to only a single value, create a WIA_PROP_LIST type and place the valid value in it.</span></span></p>
<p><span data-ttu-id="88511-562">Le tableau suivant contient les deux constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-562">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="88511-563">Valeur</span><span class="sxs-lookup"><span data-stu-id="88511-563">Value</span></span></th>
<th><span data-ttu-id="88511-564">Définition</span><span class="sxs-lookup"><span data-stu-id="88511-564">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88511-565">WIA_PACKED_PIXEL</span><span class="sxs-lookup"><span data-stu-id="88511-565">WIA_PACKED_PIXEL</span></span></td>
<td><span data-ttu-id="88511-566">Les données de l’image sont au format de pixel compressé.</span><span class="sxs-lookup"><span data-stu-id="88511-566">Image data is in packed-pixel format.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-567">WIA_PLANAR</span><span class="sxs-lookup"><span data-stu-id="88511-567">WIA_PLANAR</span></span></td>
<td><span data-ttu-id="88511-568">Les données de l’image sont au format Planar.</span><span class="sxs-lookup"><span data-stu-id="88511-568">Image data is in planar format.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PREFERRED_FORMAT"></span><span id="wia_ipa_preferred_format"></span><dl> <span data-ttu-id="88511-569"><dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-569"><dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-570">Contient le format préféré pour les images que ce minipilote transfère.</span><span class="sxs-lookup"><span data-stu-id="88511-570">Contains the preferred format for images that this minidriver transfers.</span></span> <span data-ttu-id="88511-571">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-571">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="88511-572">Obligatoire pour tous les éléments WIA 2,0 avec transfert.</span><span class="sxs-lookup"><span data-stu-id="88511-572">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="88511-573">Type : <strong>CLSID</strong>, accès : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-573">Type: <strong>CLSID</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PROP_STREAM_COMPAT_ID"></span><span id="wia_ipa_prop_stream_compat_id"></span><dl> <span data-ttu-id="88511-574"><dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-574"><dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-575">Spécifie un CLSID qui représente un ensemble de valeurs de propriétés de périphérique.</span><span class="sxs-lookup"><span data-stu-id="88511-575">Specifies a CLSID that represents a set of device property values.</span></span> <span data-ttu-id="88511-576">Si un pilote de périphérique implémente cette fonctionnalité, les applications utilisent cette propriété pour déterminer si l’appareil prend en charge un ensemble de valeurs.</span><span class="sxs-lookup"><span data-stu-id="88511-576">If a device driver implements this feature, applications use this property to determine if the device supports a set of values.</span></span></p>
<p><span data-ttu-id="88511-577">Type : <strong>CLSID</strong>, accès : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="88511-577">Type: <strong>CLSID</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="88511-578">Le tableau suivant contient les 12 constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-578">The following table has the 12 constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="88511-579">Valeur</span><span class="sxs-lookup"><span data-stu-id="88511-579">Value</span></span></th>
<th><span data-ttu-id="88511-580">Définition</span><span class="sxs-lookup"><span data-stu-id="88511-580">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88511-581">WiaImgFmt_BMP</span><span class="sxs-lookup"><span data-stu-id="88511-581">WiaImgFmt_BMP</span></span></td>
<td><span data-ttu-id="88511-582">Bitmap de point de passe avec un fichier d’en-tête</span><span class="sxs-lookup"><span data-stu-id="88511-582">MicrosoftWindows bitmap with a header file</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-583">WiaImgFmt_EMF</span><span class="sxs-lookup"><span data-stu-id="88511-583">WiaImgFmt_EMF</span></span></td>
<td><span data-ttu-id="88511-584">Métafichier Windows étendu</span><span class="sxs-lookup"><span data-stu-id="88511-584">Extended Windows metafile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-585">WiaImgFmt_EXIF</span><span class="sxs-lookup"><span data-stu-id="88511-585">WiaImgFmt_EXIF</span></span></td>
<td><span data-ttu-id="88511-586">Format de fichier Exchanger</span><span class="sxs-lookup"><span data-stu-id="88511-586">Exchangeable File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-587">WiaImgFmt_FLASHPIX</span><span class="sxs-lookup"><span data-stu-id="88511-587">WiaImgFmt_FLASHPIX</span></span></td>
<td><span data-ttu-id="88511-588">Format FlashPix</span><span class="sxs-lookup"><span data-stu-id="88511-588">FlashPix format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-589">WiaImgFmt_GIF</span><span class="sxs-lookup"><span data-stu-id="88511-589">WiaImgFmt_GIF</span></span></td>
<td><span data-ttu-id="88511-590">Format d’image GIF</span><span class="sxs-lookup"><span data-stu-id="88511-590">GIF image format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-591">WiaImgFmt_ICO</span><span class="sxs-lookup"><span data-stu-id="88511-591">WiaImgFmt_ICO</span></span></td>
<td><span data-ttu-id="88511-592">Format de fichier des icônes Windows</span><span class="sxs-lookup"><span data-stu-id="88511-592">Windows icon file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-593">WiaImgFmt_JPEG</span><span class="sxs-lookup"><span data-stu-id="88511-593">WiaImgFmt_JPEG</span></span></td>
<td><span data-ttu-id="88511-594">Format compressé JPEG</span><span class="sxs-lookup"><span data-stu-id="88511-594">JPEG compressed format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-595">WiaImgFmt_PHOTOCD</span><span class="sxs-lookup"><span data-stu-id="88511-595">WiaImgFmt_PHOTOCD</span></span></td>
<td><span data-ttu-id="88511-596">Format de fichier Eastman Kodak</span><span class="sxs-lookup"><span data-stu-id="88511-596">Eastman Kodak file format</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-597">WiaImgFmt_PNG</span><span class="sxs-lookup"><span data-stu-id="88511-597">WiaImgFmt_PNG</span></span></td>
<td><span data-ttu-id="88511-598">Format PNG W3C</span><span class="sxs-lookup"><span data-stu-id="88511-598">W3C PNG format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-599">WiaImgFmt_MEMORYBMP</span><span class="sxs-lookup"><span data-stu-id="88511-599">WiaImgFmt_MEMORYBMP</span></span></td>
<td><span data-ttu-id="88511-600">Bitmap Windows sans fichier d’en-tête</span><span class="sxs-lookup"><span data-stu-id="88511-600">Windows bitmap without a header file</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-601">WiaImgFmt_TIFF</span><span class="sxs-lookup"><span data-stu-id="88511-601">WiaImgFmt_TIFF</span></span></td>
<td><span data-ttu-id="88511-602">Tag Image File Format (TIFF)</span><span class="sxs-lookup"><span data-stu-id="88511-602">Tag Image File Format</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-603">WiaImgFmt_WMF</span><span class="sxs-lookup"><span data-stu-id="88511-603">WiaImgFmt_WMF</span></span></td>
<td><span data-ttu-id="88511-604">Métafichier Windows</span><span class="sxs-lookup"><span data-stu-id="88511-604">Windows metafile</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_RAW_BITS_PER_CHANNEL"></span><span id="wia_ipa_raw_bits_per_channel"></span><dl> <span data-ttu-id="88511-605"><dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-605"><dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-606">Pris en charge uniquement dans Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="88511-606">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="88511-607">Contient le nombre de bits dans chaque canal.</span><span class="sxs-lookup"><span data-stu-id="88511-607">Contains the number of bits in each channel.</span></span> <span data-ttu-id="88511-608">Cette propriété doit être signalée comme un vecteur de valeurs d’octets comme il y a de canaux, où le premier octet correspond au nombre de bits dans le premier canal, le deuxième octet au nombre de bits dans le deuxième canal, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="88511-608">This property should be reported as a vector of as many BYTE values as there are channels, where the first BYTE corresponds to the number of bits in the first channel, the second byte to the number of bits in the second channel and so on.</span></span> <span data-ttu-id="88511-609">Il doit y avoir autant d’entrées qu’il y a de canaux en fonction de WIA_IPA_CHANNELS_PER_PIXEL.</span><span class="sxs-lookup"><span data-stu-id="88511-609">There need to be as many entries as there are channels according to WIA_IPA_CHANNELS_PER_PIXEL.</span></span> <span data-ttu-id="88511-610">Le pilote définit cette propriété lorsque l’application passe à WiaImgFmt_RAW.</span><span class="sxs-lookup"><span data-stu-id="88511-610">The driver sets that property when the application switches to WiaImgFmt_RAW.</span></span> <span data-ttu-id="88511-611">Pour les sous-types connus, il y a autant d’entrées que celles répertoriées dans le tableau sous WIA_IPA_RAW_SUBTYPE.</span><span class="sxs-lookup"><span data-stu-id="88511-611">For the well-known subtypes, there are as many entries as listed in the table under WIA_IPA_RAW_SUBTYPE.</span></span></p>
<p><span data-ttu-id="88511-612">Type : <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-612">Type: <strong>VT_UI1</strong>|<strong>VT_VECTOR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_REGION_TYPE"></span><span id="wia_ipa_region_type"></span><dl> <span data-ttu-id="88511-613"><dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-613"><dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-614">Cette propriété est réservée par pour une utilisation future et n’est pas implémentée pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="88511-614">This property is reserved by for future use and is not implemented at this time.</span></span></p>
<p><span data-ttu-id="88511-615">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-615">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_SUPPRESS_PROPERTY_PAGE"></span><span id="wia_ipa_suppress_property_page"></span><dl> <span data-ttu-id="88511-616"><dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-616"><dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-617">Spécifie s’il faut supprimer les pages de propriétés générales des éléments sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="88511-617">Specifies whether to suppress the general property pages for items on the device.</span></span></p>
<p><span data-ttu-id="88511-618">Cette propriété est disponible sur Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="88511-618">This property is available on Windows XP and later.</span></span></p>
<p><span data-ttu-id="88511-619">Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-619">Type: <strong>VT_I4</strong>, Access: Read Only, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="88511-620">Le tableau suivant contient les constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-620">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="88511-621">L’astérisque (\*) indique que la constante n’est pas valide avec Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="88511-621">The asterisk \* indicates that the constant is not valid with Windows Vista and later.</span></span> <span data-ttu-id="88511-622">(Disponible uniquement par le biais de l’interface <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> .)</span><span class="sxs-lookup"><span data-stu-id="88511-622">(It is only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="88511-623">Constante</span><span class="sxs-lookup"><span data-stu-id="88511-623">Constant</span></span></th>
<th><span data-ttu-id="88511-624">Description</span><span class="sxs-lookup"><span data-stu-id="88511-624">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88511-625">WIA_PROPPAGE_CAMERA_ITEM_GENERAL \*</span><span class="sxs-lookup"><span data-stu-id="88511-625">WIA_PROPPAGE_CAMERA_ITEM_GENERAL\*</span></span></td>
<td><span data-ttu-id="88511-626">Supprimer la page de propriétés élément général d’un appareil photo.</span><span class="sxs-lookup"><span data-stu-id="88511-626">Suppress the general item property page for a camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-627">WIA_PROPPAGE_SCANNER_ITEM_GENERAL</span><span class="sxs-lookup"><span data-stu-id="88511-627">WIA_PROPPAGE_SCANNER_ITEM_GENERAL</span></span></td>
<td><span data-ttu-id="88511-628">Supprimer la page de propriétés d’élément général pour un scanneur.</span><span class="sxs-lookup"><span data-stu-id="88511-628">Suppress the general item property page for a scanner.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_TYMED"></span><span id="wia_ipa_tymed"></span><dl> <span data-ttu-id="88511-629"><dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-629"><dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-630">Cette propriété contient le paramètre de méthode de transfert.</span><span class="sxs-lookup"><span data-stu-id="88511-630">This property contains the transfer method setting.</span></span> <span data-ttu-id="88511-631">Le minipilote crée et gère cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-631">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="88511-632">Une application lit cette propriété pour déterminer la méthode de transfert de données du minipilote.</span><span class="sxs-lookup"><span data-stu-id="88511-632">An application reads this property to determine the minidriver's method of data transfer.</span></span></p>
<p><span data-ttu-id="88511-633">Obligatoire pour tous les éléments WIA 2,0 avec transfert.</span><span class="sxs-lookup"><span data-stu-id="88511-633">Required for all transfer-enabled WIA 2.0 items.</span></span></p>
<p><span data-ttu-id="88511-634">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="88511-634">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid Values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="88511-635">Le tableau suivant contient les constantes qui sont valides avec cette propriété.</span><span class="sxs-lookup"><span data-stu-id="88511-635">The following table has the constants that are valid with this property.</span></span> <span data-ttu-id="88511-636">L’astérisque \* indique des constantes qui ne sont pas valides avec Windows Vista et les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="88511-636">The asterisk \* indicates constants that are not valid with Windows Vista and later.</span></span> <span data-ttu-id="88511-637">(Ils sont uniquement disponibles par le biais de l’interface <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> .)</span><span class="sxs-lookup"><span data-stu-id="88511-637">(They are only available through the <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> interface.)</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="88511-638">Type de transfert</span><span class="sxs-lookup"><span data-stu-id="88511-638">Transfer Type</span></span></th>
<th><span data-ttu-id="88511-639">Description</span><span class="sxs-lookup"><span data-stu-id="88511-639">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88511-640">TYMED_CALLBACK \*</span><span class="sxs-lookup"><span data-stu-id="88511-640">TYMED_CALLBACK\*</span></span></td>
<td><span data-ttu-id="88511-641">Transférer une image en mémoire, en bandes.</span><span class="sxs-lookup"><span data-stu-id="88511-641">Transfer an image to memory, in bands.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-642">TYMED_MULTIPAGE_CALLBACK \*</span><span class="sxs-lookup"><span data-stu-id="88511-642">TYMED_MULTIPAGE_CALLBACK\*</span></span></td>
<td><span data-ttu-id="88511-643">Transférer plusieurs images en mémoire, en bandes.</span><span class="sxs-lookup"><span data-stu-id="88511-643">Transfer multiple images to memory, in bands.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88511-644">TYMED_FILE</span><span class="sxs-lookup"><span data-stu-id="88511-644">TYMED_FILE</span></span></td>
<td><span data-ttu-id="88511-645">Transférer une image dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="88511-645">Transfer an image to a file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88511-646">TYMED_MULTIPAGE_FILE</span><span class="sxs-lookup"><span data-stu-id="88511-646">TYMED_MULTIPAGE_FILE</span></span></td>
<td><span data-ttu-id="88511-647">Transférer une image dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="88511-647">Transfer an image to a file.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <span data-ttu-id="88511-648"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </span><span class="sxs-lookup"><span data-stu-id="88511-648"><dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="88511-649">Pris en charge uniquement dans Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="88511-649">Supported only in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="88511-650">Spécifie le nombre d’octets à télécharger pour un élément.</span><span class="sxs-lookup"><span data-stu-id="88511-650">Specifies the number of bytes to upload for an item.</span></span></p>
<p><span data-ttu-id="88511-651">Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="88511-651">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="88511-652">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88511-652">Requirements</span></span>



| <span data-ttu-id="88511-653">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88511-653">Requirement</span></span> | <span data-ttu-id="88511-654">Valeur</span><span class="sxs-lookup"><span data-stu-id="88511-654">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="88511-655">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88511-655">Minimum supported client</span></span><br/> | <span data-ttu-id="88511-656">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88511-656">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="88511-657">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88511-657">Minimum supported server</span></span><br/> | <span data-ttu-id="88511-658">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88511-658">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="88511-659">En-tête</span><span class="sxs-lookup"><span data-stu-id="88511-659">Header</span></span><br/>                   | <dl> <span data-ttu-id="88511-660"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="88511-660"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




