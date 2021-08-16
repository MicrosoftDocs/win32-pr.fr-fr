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
ms.openlocfilehash: 6cf9c102e5ba9732369604bea21876af66ca525b596736521e92e59e52ddf9e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207526"
---
# <a name="common-wia-item-property-constants"></a>Constantes de propriété d’élément WIA courantes

Les constantes de propriété d’appareil suivantes doivent être prises en charge par toutes les interfaces d’interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem), [**IWiaItem2**](-wia-iwiaitem2.md) et [IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) , sauf indication contraire dans leurs descriptions.

Le préfixe « WIA » \_ \_ indique une propriété d’élément pour tous les appareils et est la Convention d’affectation de noms utilisée dans C/C++. À des fins de script, ces constantes utilisent le préfixe « image » et font partie du type énuméré [WiaItemPropertyId](-wia-wiaitempropertyid.md) . Le nom de membre correspondant de cette énumération de script apparaît entre parenthèses à côté du nom de constante C/C++ dans la liste suivante.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante/valeur</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ACCESS_RIGHTS"></span><span id="wia_ipa_access_rights"></span><dl> <dt><strong>WIA_IPA_ACCESS_RIGHTS</strong></dt> <dt>PictureAccessRights</dt> </dl></td>
<td style="text-align: left;">Cet indicateur contrôle l’accès à l’élément et indique si l’élément est supprimé.<br/> Obligatoire pour tous les éléments WIA 2,0.<br/> Type : <strong>VT_I4</strong>; En lecture/écriture ou en lecture seule, en fonction de la capacité de l’élément à modifier ses droits d’accès ; Valeurs valides : WIA_PROP_FLAG<br/> Le tableau suivant contient les cinq indicateurs qui sont valides avec cette propriété.<br/> 
<table>
<thead>
<tr class="header">
<th>Droit d'accès</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_ITEM_READ</td>
<td>L’élément possède un accès en lecture seule.</td>
</tr>
<tr class="even">
<td>WIA_ITEM_WRITE</td>
<td>L’élément possède un accès en écriture seule.</td>
</tr>
<tr class="odd">
<td>WIA_ITEM_CAN_BE_DELETED</td>
<td>L’élément possède un accès en suppression seule.</td>
</tr>
<tr class="even">
<td>WIA_ITEM_RD</td>
<td>WIA_ITEM_READ | WIA_ITEM_CAN_BE_DELETED</td>
</tr>
<tr class="odd">
<td>WIA_ITEM_RWD</td>
<td>WIA_ITEM_READ | WIA_ITEM_WRITE | WIA_ITEM_CAN_BE_DELETED</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_APP_COLOR_MAPPING"></span><span id="wia_ipa_app_color_mapping"></span><dl> <dt><strong>WIA_IPA_APP_COLOR_MAPPING</strong></dt> <dt>PictureAppColorMapping</dt> </dl></td>
<td style="text-align: left;"><p>Cette propriété est réservée par pour une utilisation future et n’est pas implémentée pour l’instant.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BITS_PER_CHANNEL"></span><span id="wia_ipa_bits_per_channel"></span><dl> <dt><strong>WIA_IPA_BITS_PER_CHANNEL</strong></dt> <dt>PictureBitsPerChannel</dt> </dl></td>
<td style="text-align: left;"><p>Contient le nombre de bits par canal pour l’image. Le minipilote crée et gère cette propriété.</p>
<p>Obligatoire pour tous les éléments d’image stockés et compatibles avec l’acquisition WIA 2,0.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_BUFFER_SIZE"></span><span id="wia_ipa_buffer_size"></span><dl> <dt><strong>WIA_IPA_BUFFER_SIZE</strong></dt> <dt>PictureBufferSize</dt> </dl></td>
<td style="text-align: left;"><p>Contient la taille de la mémoire tampon, en octets, utilisée pendant un transfert de données. Le minipilote crée et gère cette propriété.</p>
<p>Une application peut lire cette propriété pour déterminer la taille de mémoire tampon spécifiée par le pilote pour les transferts de données. Le service WIA lit également cette propriété pour allouer de la mémoire au minipilote pendant le transfert de données.</p>
<p>Facultatif pour tous les éléments WIA 2,0 avec transfert.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<div class="alert">
<blockquote>
[!Note]<br />
La propriété <strong>WIA_IPA_BUFFER_SIZE</strong> contient la quantité minimale de données qu’une application peut demander à un moment donné. Plus la taille de la mémoire tampon est grande, plus les demandes de l’appareil sont volumineuses. Cela peut rendre l’appareil plus lent et ne pas répondre, peut ralentir les performances globales du système et consommer une quantité excessive de ressources. Les tailles de mémoire tampon trop petites peuvent ralentir les performances du transfert de données en exigeant de nombreuses requêtes plus petites. Choisissez une taille de mémoire tampon raisonnable en prenant en compte la taille standard d’une demande de données sur votre appareil et en équilibrant le nombre de demandes par rapport à la taille de ces demandes.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_BYTES_PER_LINE"></span><span id="wia_ipa_bytes_per_line"></span><dl> <dt><strong>WIA_IPA_BYTES_PER_LINE</strong></dt> <dt>PictureBytesPerLine</dt> </dl></td>
<td style="text-align: left;"><p>Contient le nombre d’octets d’une ligne d’analyse de l’image. Le minipilote crée et gère cette propriété.</p>
<p>Facultatif pour tous les éléments WIA 2,0.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_CHANNELS_PER_PIXEL"></span><span id="wia_ipa_channels_per_pixel"></span><dl> <dt><strong>WIA_IPA_CHANNELS_PER_PIXEL</strong></dt> <dt>PictureChannelsPerPixel</dt> </dl></td>
<td style="text-align: left;"><p>Contient le nombre de canaux par pixel pour l’image. Le minipilote crée et gère cette propriété.</p>
<p>Obligatoire pour tous les éléments d’image stockés et compatibles avec l’acquisition WIA 2,0.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_COLOR_PROFILE"></span><span id="wia_ipa_color_profile"></span><dl> <dt><strong>WIA_IPA_COLOR_PROFILE</strong></dt> <dt>PictureColorProfile</dt> </dl></td>
<td style="text-align: left;"><p>Cette propriété est réservée par pour une utilisation future et n’est pas implémentée pour l’instant.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_COMPRESSION"></span><span id="wia_ipa_compression"></span><dl> <dt><strong>WIA_IPA_COMPRESSION</strong></dt> <dt>PictureCompression</dt> </dl></td>
<td style="text-align: left;"><p>Contient le type de compression actuel utilisé. Le minipilote crée et gère cette propriété.</p>
<p>Une application lit cette propriété pour déterminer le type de compression d’image ou définit cette propriété pour configurer le paramètre de compression.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Le tableau suivant contient les constantes qui sont valides avec cette propriété. le symbole <strong>V</strong> indique que la constante est prise en charge uniquement dans Windows Vista et versions ultérieures. (Disponible uniquement par le biais de l’interface <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .)</p>

<table>
<thead>
<tr class="header">
<th>Type de compression</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_COMPRESSION_NONE</td>
<td>Aucune compression. Pour plus d’informations, consultez <strong>Remarque</strong> .</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_AUTO</td>
<td>Mode de compression automatique. Pour plus d’informations, consultez <strong>Remarque</strong> .</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_BI_RLE4</td>
<td>Compression RLE4</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_BI_RLE8</td>
<td>Compression RLE8</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_G3</td>
<td>Compression de groupe 3</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_G4</td>
<td>Compression de groupe 4</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_JPEG</td>
<td>Compression JPEG.</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_JBIG<strong>V</strong></td>
<td>Compression JBIG.</td>
</tr>
<tr class="odd">
<td>WIA_COMPRESSION_JPEG2K<strong>V</strong></td>
<td>Compression JPEG 2000.</td>
</tr>
<tr class="even">
<td>WIA_COMPRESSION_PNG<strong>V</strong></td>
<td>Compression PNG.</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
<p>[!Note]</p>
<p>Lorsque cette propriété est WIA_COMPRESSION_NONE, et WIA_IPA_FORMAT est soit WiaImgFmt_PDFA, soit WiaImgFmt_XPS ; WIA_COMPRESSION_NONE signifie alors que le mode de compression n’est pas défini et que le scanneur doit décider d’un mode.</p>
<p>WIA_COMPRESSION_AUTO est une nouvelle valeur de propriété définie pour la propriété WIA_IPA_COMPRESSION. Cette valeur est valide pour tous les éléments de source de données d’image programmable, y compris le plateau et le chargeur. Lorsque cette valeur est prise en charge par le mini-pilote WIA, le client d’application WIA peut définir WIA_IPA_COMPRESSION afin d’activer la détection automatique du mode de compression au niveau de l’appareil. WIA_COMPRESSION_AUTO pouvez travailler avec et sans une couleur automatique complète prise en charge ou activée (WIA_DATA_AUTO et WIA_DEPTH_AUTO).</p>
<p>WIA_COMPRESSION_AUTO est très utile avec les formats de fichier de transfert qui prennent en charge plusieurs types de données et des profondeurs de bits, comme WiaImgFmt_RAW. Pour plus d’informations sur les formats de fichier de transfert, consultez WIA_IPA_FORMAT dans ce tableau.</p>
<p>La WIA_COMPRESSION_AUTO pour le mini-pilote WIA est opitonal. Lorsqu’il est pris en charge, le mini-pilote WIA ne doit jamais le définir comme valeur par défaut pour WIA_IPA_COMPRESSION ; seule l’application WIA peut définir cette valeur.</p>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_DATATYPE"></span><span id="wia_ipa_datatype"></span><dl> <dt><strong>WIA_IPA_DATATYPE</strong></dt> <dt>PictureDatatype</dt> </dl></td>
<td style="text-align: left;"><p>Contient le paramètre de type de données actuel pour l’appareil. Le minipilote crée et gère cette propriété.</p>
<p>Une application lit cette propriété pour déterminer le type de données de l’image. Une application écrit cette propriété pour définir le type de données actuel de l’image à transférer.</p>
<p>Cette propriété est obligatoire pour tous les éléments WIA 2,0. Il doit être en lecture/écriture pour tous les éléments de l’acquisition WIA 2,0 et lecture uniquement pour les éléments de stockage WIA 2,0.</p>
<p>Type : <strong>VT_I4</strong>; accès pour les systèmes d’exploitation antérieurs à Windows Vista : cette propriété est en lecture seule pour les appareils photo et en lecture/écriture pour les scanneurs ; accès pour Windows Vista et versions ultérieures : cette propriété est en lecture seule pour les éléments WIA_CATEGORY_FOLDER et WIA_CATEGORY_FINISHED_FILE, et en lecture/écriture pour toutes les autres catégories d’éléments WIA 2,0 ; Valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Le tableau suivant contient les six constantes qui sont valides avec lorsque <strong>WIA_IPA_FORMAT</strong> n’est pas défini sur WiaImgFmt_RAW.</p>

<table>
<thead>
<tr class="header">
<th>Type de données</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DATA_AUTO</td>
<td>Valide pour tous les éléments de source de données d’image programmable, y compris le plateau et le chargeur. Lorsque cette valeur est prise en charge par le mini-pilote WIA, le client d’application WIA peut définir WIA_IPA_DATATYPE afin d’activer la détection automatique des couleurs au niveau de l’appareil. Lorsque WIA_DATA_AUTO est définie, le mini-pilote WIA doit mettre à jour WIA_IPA_DEPTH sur le même élément à WIA_DEPTH_AUTO (qui doit être une valeur prise en charge si l’appareil prend en charge la couleur automatique).<br/> Il s’agit d’une valeur facultative, mais elle est requise lorsque WIA_DEPTH_AUTO est pris en charge pour WIA_IPA_DEPTH.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_COLOR</td>
<td>Les données d’analyse sont de couleur rouge, verte, bleue (RVB). Le format de couleur complet est décrit à l’aide des propriétés WIA suivantes : <strong>WIA_IPA_CHANNELS_PER_PIXEL</strong><br/> <strong>WIA_IPA_BITS_PER_CHANNEL</strong><br/> <strong>WIA_IPA_PLANAR</strong><br/> <strong>WIA_IPA_PIXELS_PER_LINE</strong><br/> <strong>WIA_IPA_BYTES_PER_LINE</strong><br/> <strong>WIA_IPA_NUMBER_OF_LINES</strong><br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_COLOR_DITHER</td>
<td>Identique à WIA_DATA_COLOR à la différence que les données sont tramées à l’aide du modèle de trame actuellement sélectionné.</td>
</tr>
<tr class="even">
<td>WIA_DATA_COLOR_THRESHOLD</td>
<td>Identique à WIA_DATA_COLOR sauf que la valeur de seuil est utilisée lors de l’analyse des données. Les valeurs de couleur sur la valeur de <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> sont converties en luminosité complète. les couleurs sous cette valeur sont converties en noir.</td>
</tr>
<tr class="odd">
<td>WIA_DATA_DITHER</td>
<td>Les données d’analyse sont tramées à l’aide du modèle de trame actuellement sélectionné.</td>
</tr>
<tr class="even">
<td>WIA_DATA_GRAYSCALE</td>
<td>Les données d’analyse représentent l’intensité. La palette est une échelle grise fixe et à espacement identique avec une profondeur spécifiée par <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> propriété.</td>
</tr>
<tr class="odd">
<td>WIA_DATA_THRESHOLD</td>
<td>Le seuil est un bit par pixel de données en noir et blanc. Les données sur la valeur actuelle de <a href="https://msdn.microsoft.com/library/ms796233.aspx">WIA_IPS_THRESHOLD</a> sont converties en blanc ; les données de cette valeur sont converties en noir.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>La propriété <strong>WIA_IPA_DATATYPE</strong> est également utilisée pour décrire le type de transfert de données brutes à utiliser lorsque l’application définit WiaImgFmt_RAW. Le pilote doit définir la propriété <strong>WIA_IPA_DATATYPE</strong> sur une liste de valeurs autorisées à partir desquelles l’application peut en choisir une.</p>
<p>Si l’appareil peut être défini sur une seule valeur, créez un <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type et placez la valeur valide dans celui-ci.</p>
<p>Vérifiez la propriété <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> pour déterminer la profondeur de bit. Cette propriété contient généralement une valeur unique pour les appareils photo.</p>
<p>Le tableau suivant répertorie les constantes qui sont valides avec <strong>WIA_IPA_DATATYPE</strong> lorsque <strong>WIA_IPA_FORMAT</strong> a la valeur WiaImgFmt_RAW.</p>

<table>
<thead>
<tr class="header">
<th>Type de données</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DATA_GRAYSCALE</td>
<td>Les données d’analyse représentent l’intensité. La palette est un niveau de nuances de gris fixe et uniformément espacé avec une profondeur spécifiée par la propriété <a href="https://msdn.microsoft.com/library/ms795935.aspx">WIA_IPA_DEPTH</a> . <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> doit avoir la valeur 1.</td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_BGR</td>
<td>Les données d’analyse sont dans le BGR (bleu-vert-rouge) colorspace. Le format de couleur complet est décrit à l’aide de followingWIAproperties : <a href="https://msdn.microsoft.com/library/ms796163.aspx">WIA_IPA_CHANNELS_PER_PIXEL</a><br/> <a href="https://msdn.microsoft.com/library/ms795997.aspx">WIA_IPA_BITS_PER_CHANNEL</a><br/> <a href="https://msdn.microsoft.com/library/ms796567.aspx">WIA_IPA_PIXELS_PER_LINE</a><br/> <a href="https://msdn.microsoft.com/library/ms796404.aspx">WIA_IPA_BYTES_PER_LINE</a><br/> <a href="https://msdn.microsoft.com/library/ms795916.aspx">WIA_IPA_NUMBER_OF_LINES</a><br/> <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> doit avoir la valeur 3.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_CMY</td>
<td>Les données d’analyse se trouvent dans le colorspace cyan-magenta-jaune (CMJ). Le format de couleur complet est décrit à l’aide des mêmes propriétés WIA que dans WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> doit avoir la valeur 3.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_CMYK</td>
<td>Les données d’analyse se trouvent dans le colorspace cyan-magenta-jaune-noir (CMJN). Le format de couleur complet est décrit à l’aide des mêmes propriétés WIA que dans WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> doit avoir la valeur 4.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_RGB</td>
<td>Les données d’analyse se trouvent dans le colorspace rouge-vert-bleu (RVB). Le format de couleur complet est décrit à l’aide des mêmes propriétés WIA que dans WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> doit avoir la valeur 3.<br/></td>
</tr>
<tr class="even">
<td>WIA_DATA_RAW_YUV</td>
<td>Les données d’analyse se trouvent dans la différence luminance-bleu-différence rouge (YUV) colorspace. Le format de couleur complet est décrit à l’aide des mêmes propriétés WIA que dans WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> doit avoir la valeur 3.<br/></td>
</tr>
<tr class="odd">
<td>WIA_DATA_RAW_YUVK</td>
<td>Les données d’analyse se trouvent dans la différence luminance-bleu-différence rouge-noir (YUVK) colorspace. Le format de couleur complet est décrit à l’aide des mêmes propriétés WIA que dans WIA_DATA_RAW_BGR. <a href="https://msdn.microsoft.com/library/ms795495.aspx">WIA_IPA_RAW_BITS_PER_CHANNEL</a> doit avoir la valeur 4.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_DEPTH"></span><span id="wia_ipa_depth"></span><dl> <dt><strong>WIA_IPA_DEPTH</strong></dt> <dt>PictureDepth</dt> </dl></td>
<td style="text-align: left;"><p>WIA_IPA_DEPTH contient le paramètre de profondeur de bit d’une image. Le minipilote crée et gère cette propriété. Une application lit cette propriété pour déterminer le paramètre de profondeur de bit de l’image. L’application peut également être en mesure de définir cette valeur sur la profondeur de bits souhaitée.</p>
<p>Si l’appareil peut être défini sur une seule valeur, créez un type de <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> et placez la valeur valide dans celui-ci.</p>
<p>Cette propriété est obligatoire pour tous les éléments WIA 2,0. Il doit être en lecture/écriture pour tous les éléments de l’acquisition WIA 2,0 et lecture uniquement pour les éléments de stockage WIA 2,0.</p>
<p>Type : <strong>VT_I4</strong>; accès pour les systèmes d’exploitation antérieurs à Windows Vista : lecture/écriture ; accès pour Windows Vista et versions ultérieures : cette propriété est en lecture seule pour les éléments WIA_CATEGORY_FOLDER et WIA_CATEGORY_FINISHED_FILE, et en lecture/écriture pour toutes les autres catégories d’éléments WIA 2,0 ; Valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>WIA_DEPTH_AUTO est défini comme 0 bits par pixel, et c’est une nouvelle valeur de propriété définie pour le WIA_IPA_DEPTH. Cette valeur est valide pour tous les éléments de source de données d’image programmable, y compris le plateau et le chargeur. Lorsque WIA_DEPTH_AUTO est pris en charge par le mini-pilote WIA, le client d’application WIA peut définir WIA_IPA_DEPTH sur cette valeur, afin d’activer la détection automatique des couleurs au niveau de l’appareil. Lorsque WIA_DEPTH_AUTO est définie, le mini-pilote WIA doit mettre à jour WIA_IPA_DATATYPE sur le même élément à WIA_DATA_AUTO (qui doit être une valeur prise en charge, si l’appareil prend en charge la couleur automatique).</p>
<p>WIA_DEPTH_AUTO est une valeur facultative, mais elle devient obligatoire lorsque WIA_DATA_AUTO est pris en charge pour WIA_IPA_DATATYPE.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FILENAME_EXTENSION"></span><span id="wia_ipa_filename_extension"></span><dl> <dt><strong>WIA_IPA_FILENAME_EXTENSION</strong></dt> <dt>PictureFilenameExtension</dt> </dl></td>
<td style="text-align: left;"><p>Contient l’extension de nom de fichier pour un format de fichier particulier. Le minipilote crée et gère cette propriété.</p>
<p>Facultatif pour tous les éléments WIA 2,0 avec transfert.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Le pilote met à jour cette propriété pour refléter la valeur actuelle de la propriété <a href="https://msdn.microsoft.com/library/ms796440.aspx">WIA_IPA_FORMAT</a> .</p>
<p>Par exemple, si <strong>WIA_IPA_FORMAT</strong> est WiaImgFmt_JPEG, <a href="-wia-property-attributes.md">WIA_IPA_FILENAME_EXTENSION</a> doit être <strong>jpg</strong>. Si <strong>WIA_IPA_FORMAT</strong> est WiaImgFmt_BMP, WIA_IPA_FILENAME_EXTENSION doit être BMP.</p>
<div class="alert">
<blockquote>
[!Note]<br />
L’extension de nom de fichier n’inclut pas le point.
</blockquote>
</div>
<div>
 
</div>
<p>Cette propriété est recommandée pour les pilotes qui prennent en charge les formats standard et est requise pour les pilotes qui implémentent des formats définis personnalisés. Il informe l’application de l’extension de nom de fichier correcte à utiliser pendant le transfert de fichiers au format privé. Par exemple, si A. Datum Corporation a créé un pilote WIA qui a transféré un fichier dans un nouveau format, l’entreprise peut spécifier une extension d' &quot; ADC &quot; . Cela permet aux applications de transférer des données dans ce format vers un fichier et de créer un nom de fichier tel que <em>MyFile. ADC</em>, ce qui est utile pour les personnes qui comprennent la nouvelle extension.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_FORMAT"></span><span id="wia_ipa_format"></span><dl> <dt><strong>WIA_IPA_FORMAT</strong></dt> <dt>PictureFormat</dt> </dl></td>
<td style="text-align: left;"><p>Contient le format actuel de l’image à transférer.</p>
<p>Une application lit cette propriété pour déterminer le format de l’image à recevoir. Une application écrit cette propriété pour définir le format. Cette propriété dépend de la propriété <a href="https://msdn.microsoft.com/library/ms795488.aspx">WIA_IPA_TYMED</a> . Le minipilote crée et gère cette propriété.</p>
<p>Si l’appareil peut être défini sur une seule valeur, créez un <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> type et placez la valeur valide dans celui-ci.</p>
<p>Type : <strong>CLSID</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Le tableau suivant répertorie les constantes qui sont valides avec cette propriété. l’astérisque (*) indique que la constante n’est pas prise en charge dans Windows Vista. (Disponible uniquement par le biais de l’interface <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> .) le double astérisque * * indique que la constante n’est pas prise en charge dans Windows Server 2003 ou Windows Vista. le symbole <strong>V</strong> indique que la constante est prise en charge uniquement dans Windows Vista et versions ultérieures. (Disponible uniquement par le biais de l’interface <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .)</p>

<table>
<thead>
<tr class="header">
<th>Format</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaAudFmt_AIFF</td>
<td>Format audio AIFF</td>
</tr>
<tr class="even">
<td>WiaAudFmt_MP3</td>
<td>Format audio MP3</td>
</tr>
<tr class="odd">
<td>WiaAudFmt_WAV</td>
<td>Format audio WAV</td>
</tr>
<tr class="even">
<td>WiaAudFmt_WMA</td>
<td>Format audio WMA</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_ASF * *</td>
<td>Format vidéo ASF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_AVI * *</td>
<td>Format vidéo AVI</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_BMP</td>
<td>Windows bitmap avec un fichier d’en-tête</td>
</tr>
<tr class="even">
<td>WiaImgFmt_CIFF *</td>
<td>Format du fichier image de l’appareil photo</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_DPOF</td>
<td>Format d’impression DPOF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EMF</td>
<td>métafichier de Windows étendu</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_EXEC</td>
<td>Fichier exécutable</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EXIF</td>
<td>Format de fichier Exchanger</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_FLASHPIX</td>
<td>Format FlashPix</td>
</tr>
<tr class="even">
<td>WiaImgFmt_GIF</td>
<td>Format d’image GIF</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_HTML</td>
<td>Format HTML</td>
</tr>
<tr class="even">
<td>WiaImgFmt_ICO</td>
<td>format du fichier d’icône Windows</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JBIG<strong>V</strong></td>
<td>Le format JBIG (collaboration image experts Group).</td>
</tr>
<tr class="even">
<td>WiaImgFmt_JPEG</td>
<td>Format compressé JPEG</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JPEG2K</td>
<td>Format compressé JPEG 2000</td>
</tr>
<tr class="even">
<td>WiaImgFmt_JPEG2KX</td>
<td>Format compressé JPEG 2000</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_MEMORYBMP</td>
<td>bitmap Windows sans fichier d’en-tête</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PDFA<strong>V</strong></td>
<td>Format PDF/A (ISO/CD 19005-1).</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_MPG * *</td>
<td>Format vidéo MPEG</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PHOTOCD</td>
<td>Format de fichier Eastman Kodak</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_PICT</td>
<td>Format de fichier Apple</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PNG</td>
<td>Format PNG W3C</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_RAW</td>
<td>Format brut pour les transferts de données uniquement</td>
</tr>
<tr class="even">
<td>WiaImgFmt_RAWRGB</td>
<td>Format RVB brut</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_RTF</td>
<td>Format de fichier texte enrichi</td>
</tr>
<tr class="even">
<td>WiaImgFmt_SCRIPT</td>
<td>Fichier de script</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_TIFF</td>
<td>Tag Image File Format (TIFF)</td>
</tr>
<tr class="even">
<td>WiaImgFmt_TXT</td>
<td>Fichier texte</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_UNICODE16</td>
<td>Encodage UNICODE 16 bits</td>
</tr>
<tr class="even">
<td>WiaImgFmt_WMF</td>
<td>métafichier Windows</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_XML</td>
<td>Fichier XML</td>
</tr>
<tr class="even">
<td>WiaImgFmt_XPS<strong>V</strong></td>
<td>Format de package XPS</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
Lorsque cette propriété a la valeur WiaImgFmt_PDFA ou WiaImgFmt_XPS, et WIA_IPA_COMPRESSION est WIA_COMPRESSION_NONE ; la dernière valeur signifie que le mode de compression n’est pas défini et que le scanneur doit décider d’un mode.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_FULL_ITEM_NAME"></span><span id="wia_ipa_full_item_name"></span><dl> <dt><strong>WIA_IPA_FULL_ITEM_NAME</strong></dt> <dt>PictureFullItemName</dt> </dl></td>
<td style="text-align: left;"><p>Contient le nom complet de l’élément (nom de l’élément, ainsi que les informations relatives au chemin d’accès). Le nom complet de l’élément est le même que le paramètre <em>bstrFullItemName</em> de la fonction de l’utilitaire de service <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> . Une application lit cette propriété pour déterminer l’élément utilisé actuellement et l’emplacement où se trouve cet élément dans l’arborescence des éléments. Chaque élément doit avoir un nom unique. Les applications utilisent généralement le nom complet de l’élément pour rechercher des éléments dans l’arborescence des éléments. Le service WIA crée et gère cette propriété.</p>
<p>Obligatoire pour tous les éléments WIA 2,0.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_GAMMA_CURVES"></span><span id="wia_ipa_gamma_curves"></span><dl> <dt><strong>WIA_IPA_GAMMA_CURVES</strong></dt> <dt>PictureGammaCurves</dt> </dl></td>
<td style="text-align: left;"><p>Cette propriété est réservée à une utilisation future et n’est pas implémentée pour l’instant.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ICM_PROFILE_NAME"></span><span id="wia_ipa_icm_profile_name"></span><dl> <dt><strong>WIA_IPA_ICM_PROFILE_NAME</strong></dt> <dt>PictureIcmProfileName</dt> </dl></td>
<td style="text-align: left;"><p>contient le nom de profil ICM nécessaire pour décoder correctement l’image. une application lit cette propriété pour déterminer le profil ICM à utiliser lors du traitement de l’image. Le service WIA crée et gère cette propriété en fonction de l’entrée ICMProfiles dans le fichier d’installation du pilote.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_CATEGORY"></span><span id="wia_ipa_item_category"></span><dl> <dt><strong>WIA_IPA_ITEM_CATEGORY</strong></dt> <dt>PictureItemCategory</dt> </dl></td>
<td style="text-align: left;"><p>pris en charge uniquement dans Windows Vista et versions ultérieures.</p>
<p>Les éléments WIA 2,0 sont regroupés en catégories qui définissent la façon dont un <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> doit être traité ou utilisé. Par exemple, si l’élément représente un flux, l’application doit s’attendre à ce qu’il contienne les propriétés du chargeur de documents requis et fonctionne comme un chargeur de documents. Si l’élément représente un fichier fini, une application WIA 2,0 doit la traiter ainsi, en supposant que les données sont statiques et situées sur l’appareil. (Les règles pour chaque élément sont définies dans leurs documents de spécification individuels.)</p>
<p>Obligatoire pour tous les éléments WIA 2,0.</p>
<p>Type : <strong>VT_CLSID</strong>, Access : lecture seule, valeurs valides : <a href="-wia-wia2-itemcategoryguids.md"><strong>GUID de catégorie d’élément</strong></a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_FLAGS"></span><span id="wia_ipa_item_flags"></span><dl> <dt><strong>WIA_IPA_ITEM_FLAGS</strong></dt> <dt>PictureItemFlags</dt> </dl></td>
<td style="text-align: left;"><p>Contient les indicateurs descriptifs pour un élément WIA. Les indicateurs d’élément sont les mêmes que ceux du paramètre <em>lObjectFlags</em> de la fonction de l’utilitaire de service <a href="https://msdn.microsoft.com/library/ms794649.aspx">wiasCreateDrvItem</a> . Le service WIA crée et gère cette propriété.</p>
<p>Une application lit cette propriété pour déterminer les valeurs d’indicateur descriptives de l’élément.</p>
<p>Type : <strong>VT_I4</strong> accès : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Le tableau suivant contient les indicateurs qui sont valides avec cette propriété. un astérisque * indique que l’indicateur n’est pas pris en charge dans Windows Vista ou version ultérieure. (Disponible uniquement par le biais de l’interface <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> .) un double astérisque * * indique que l’indicateur n’est pas pris en charge dans Windows Server 2003 ou Windows Vista ou version ultérieure. le symbole <strong>V</strong> indique que l’indicateur est pris en charge uniquement dans Windows Vista et versions ultérieures. (Disponible uniquement par le biais de l’interface <a href="-wia-iwiaitem2.md"><strong>IWiaItem2</strong></a> .)</p>

<table>
<thead>
<tr class="header">
<th>Indicateur</th>
<th>Définition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaItemTypeAnalyze*</td>
<td>Cet élément prend en charge la méthode <strong>IWiaItem :: AnalyzeItem</strong> (décrite dans la documentation du kit de développement Platform SDK). Cet élément prend également en charge la génération automatique d’éléments enfants. Cette fonctionnalité est utile pour la détection des régions ou la décomposition des pages.</td>
</tr>
<tr class="even">
<td>WiaItemTypeAudio</td>
<td>Cet élément prend en charge l’audio. Cet indicateur n’est valide que pour les éléments dont l’indicateur <strong>WiaItemTypeFile</strong> est également défini.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeBurst*</td>
<td>Pour les dossiers uniquement. Cet indicateur indique que les images de ce dossier ont été prises dans une séquence temporelle continue.</td>
</tr>
<tr class="even">
<td>WiaItemTypeDeleted</td>
<td>Cet élément est marqué pour suppression, cet élément a été supprimé, cet élément n’existe pas ou le contenu de cet élément n’est pas valide.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeDocument<strong>V</strong></td>
<td>Cet élément est un fichier de document dans l’un des formats de document que contient la propriété <strong>WIA_IPA_FORMAT</strong> . (Ces formats incluent ceux des fichiers qui ne sont pas des images, tels que les fichiers .txt, .htm et .doc.)</td>
</tr>
<tr class="even">
<td>WiaItemTypeDevice</td>
<td>Cet élément représente un appareil connecté.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeDisconnected</td>
<td>Cet élément représente un appareil déconnecté.</td>
</tr>
<tr class="even">
<td>WiaItemTypeFile</td>
<td>L’élément prend en charge les transferts de fichiers.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeFolder</td>
<td>L’élément est un dossier.</td>
</tr>
<tr class="even">
<td>WiaItemTypeFree</td>
<td>L’élément n’est pas initialisé ou a été supprimé.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeGenerated</td>
<td>Cet élément a été généré par une application ou par le pilote.</td>
</tr>
<tr class="even">
<td>WiaItemTypeHasAttachments*</td>
<td>Cet élément prend en charge les pièces jointes et contient actuellement des pièces jointes.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeHPanorama*</td>
<td>Cet élément représente une image panoramique horizontale. Cet indicateur n’est valide que pour les éléments dont l’indicateur <strong>WiaItemTypeFolder</strong> est également défini.</td>
</tr>
<tr class="even">
<td>WiaItemTypeImage</td>
<td>L’élément est un fichier image. Cet indicateur n’est valide que pour les éléments dont l’indicateur <strong>WiaItemTypeFile</strong> est également défini.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeProgrammableDataSource<strong>V</strong></td>
<td>L’élément est une source de données programmable et suit un ensemble de règles de configuration prédéfinies, qui sont basées sur <strong>WIA_IPA_ITEM_CATEGORY</strong>.</td>
</tr>
<tr class="even">
<td>WiaItemTypeRoot<strong>V</strong></td>
<td>Cet élément est l’élément racine, qui est le parent de tous les éléments de fonctionnalité pris en charge par l’appareil.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeStorage</td>
<td>Cet indicateur indique un stockage supplémentaire pour les éléments de dossiers. Les pilotes WIA spécifient leurs éléments en termes d’images et de dossiers. Il n’existe pas de propriétés WIA qui décrivent les caractéristiques d’un élément de stockage (par exemple, l’espace de stockage restant, la vitesse d’écriture ou le type de média restant). Les propriétés spécifiques au fournisseur qui exposent ces informations peuvent être ajoutées. Ces propriétés sont accessibles uniquement aux applications ou extensions écrites pour les reconnaître.</td>
</tr>
<tr class="even">
<td>WiaItemTypeTransfer</td>
<td>Cet élément peut être utilisé pour transférer des données.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeTwainCapabilityPassThrough</td>
<td>Ce type indique que l’appareil WIA est en mesure de recevoir les données de capacité TWAIN de la couche de compatibilité TWAIN. Si ce type est défini, toute fonctionnalité TWAIN qui n’est pas comprise par la couche de compatibilité TWAIN sera transmise au pilote theWIA. Cela est valide uniquement pour l’élément racine.</td>
</tr>
<tr class="even">
<td>WiaItemTypeVideo**</td>
<td>Cet élément prend en charge la vidéo en continu.</td>
</tr>
<tr class="odd">
<td>WiaItemTypeVPanorama*</td>
<td>Cet élément représente une image panoramique verticale. Cet indicateur n’est valide que pour les éléments dont l’indicateur <strong>WiaItemTypeFolder</strong> est également défini.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Certains de ces indicateurs sont obligatoires ou facultatifs pour les éléments WIA 2,0, en fonction de la catégorie de l’élément, comme indiqué dans ce tableau.</p>

<table>
<thead>
<tr class="header">
<th>Catégorie d’élément</th>
<th>Obligatoire</th>
<th>Facultatif</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_CATEGORY_ROOT</td>
<td>WiaItemTypeRoot WiaItemTypeFolder</td>
<td>WiaItemTypeDevice WiaItemTypeDisconnected</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FLATBED</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>WiaItemTypeFolder (si plusieurs éléments de régions d’analyse sont pris en charge, cet indicateur est facultatif uniquement pour l’élément racine WIA_CATEGORY_FLATBED.)</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FEEDER WIA_CATEGORY_FEEDER_FRONT WIA_CATEGORY_FEEDER_BACK</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>WiaItemTypeFolder (si WIA_CATEGORY_FEEDER_FRONT et WIA_CATEGORY_FEEDER_BACK éléments sont présents, cet indicateur est facultatif uniquement pour l’élément racine WIA_CATEGORY_FEEDER).</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FILM (racine)</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile WiaItemTypeFolder</td>
<td>Aucun</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM (enfants)</td>
<td>WiaItemTypeProgrammableDataSource WiaItemTypeTransfer WiaItemTypeImage WiaItemTypeFile</td>
<td>Aucun</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FOLDER</td>
<td>WiaItemTypeStorage WiaItemTypeFolder</td>
<td>WiaItemTypeDeleted</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FINISHED_FILE</td>
<td>WiaItemTypeFile WiaItemTypeTransfer</td>
<td>WiaItemTypeImage WiaItemTypeAudio WiaItemTypeDeleted</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_NAME"></span><span id="wia_ipa_item_name"></span><dl> <dt><strong>WIA_IPA_ITEM_NAME</strong></dt> <dt>PictureItemName</dt> </dl></td>
<td style="text-align: left;"><p>Contient le nom de l’élément. Une application lit cette propriété pour déterminer l’élément qu’elle utilise actuellement. Chaque élément a un nom unique. Le service WIA crée et gère cette propriété.</p>
<p>Obligatoire pour tous les éléments WIA 2,0.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_SIZE"></span><span id="wia_ipa_item_size"></span><dl> <dt><strong>WIA_IPA_ITEM_SIZE</strong></dt> <dt>PictureItemSize</dt> </dl></td>
<td style="text-align: left;"><p>Contient la taille actuelle, en octets, des données associées à l’élément. Le minipilote crée et gère cette propriété.</p>
<p>Contains correspond à la taille totale des données transférées. Si cette valeur est égale à zéro, cela signifie que le minipilote n’a pas d’informations sur la taille exacte des données. (Ceci est courant pour les données compressées.) Une application lit cette valeur pour déterminer la taille de l’acquisition avant qu’elle ait lieu. Le service WIA lit cette propriété pour aider à allouer de la mémoire pour les transferts de données. Pour plus d’informations, consultez <a href="https://msdn.microsoft.com/library/ms792198.aspx">transfert de données vers une application WIA</a> si la propriété a la valeur zéro et que TYMED est configuré pour un transfert de fichiers, le service WIA n’alloue pas de mémoire pour le minipilote WIA.</p>
<p>Obligatoire pour tous les éléments WIA 2,0 avec transfert.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_ITEM_TIME"></span><span id="wia_ipa_item_time"></span><dl> <dt><strong>WIA_IPA_ITEM_TIME</strong></dt> <dt>PictureItemTime</dt> </dl></td>
<td style="text-align: left;"><p>Contient l’heure à laquelle l’image a été capturée à l’origine. Le minipilote crée et gère cette propriété. Cette propriété doit être signalée comme un vecteur de huit valeurs de <strong>mots</strong> sous la forme d’une structure SYSTEMTIME (décrite dans la documentation du kit de développement Platform SDK).</p>
<p>Facultatif pour tous les éléments WIA 2,0.</p>
<p>Type : <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong> accès : lecture/écriture ou lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>PictureItemItemsStored</dt> </dl></td>
<td style="text-align: left;"><p>pris en charge uniquement dans Windows Vista et versions ultérieures.</p>
<p>Spécifie le nombre d’éléments stockés dans l’élément WIA_CATEGORY_FOLDER.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_MIN_BUFFER_SIZE"></span><span id="wia_ipa_min_buffer_size"></span><dl> <dt><strong>WIA_IPA_MIN_BUFFER_SIZE</strong></dt> <dt>PictureMinBufferSize</dt> </dl></td>
<td style="text-align: left;"><p>Spécifie la taille de mémoire tampon minimale utilisée dans les transferts de données. Si le transfert de données est effectué via un mécanisme de rappel, la valeur de la propriété peut être aussi petite que 64 Ko. Toutefois, si le transfert est vers un fichier, la valeur de la propriété est le nombre d’octets nécessaires pour transférer une page de données à la fois. Le minipilote crée et gère cette propriété WIA.</p>
<p>Facultatif pour tous les éléments WIA 2,0 avec transfert.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_NUMBER_OF_LINES"></span><span id="wia_ipa_number_of_lines"></span><dl> <dt><strong>WIA_IPA_NUMBER_OF_LINES</strong></dt> <dt>PictureNumberOfLines</dt> </dl></td>
<td style="text-align: left;"><p>Contient le nombre de lignes contenues dans l’image (hauteur verticale de l’image en pixels). Le minipilote crée et gère cette propriété.</p>
<p>Facultatif pour tous les éléments WIA 2,0.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PIXELS_PER_LINE"></span><span id="wia_ipa_pixels_per_line"></span><dl> <dt><strong>WIA_IPA_PIXELS_PER_LINE</strong></dt> <dt>PicturePixelsPerLine</dt> </dl></td>
<td style="text-align: left;"><p>Contient le nombre de pixels dans chaque ligne de l’image (la largeur de l’image en pixels). Le minipilote crée et gère cette propriété.</p>
<p>Facultatif pour tous les éléments WIA 2,0.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PLANAR"></span><span id="wia_ipa_planar"></span><dl> <dt><strong>WIA_IPA_PLANAR</strong></dt> <dt>PicturePlanar</dt> </dl></td>
<td style="text-align: left;"><p>cette propriété n’est pas prise en charge dans Windows Vista et versions ultérieures.</p>
<p>Contient les options de compression des données d’image. Le minipilote crée et gère cette propriété.</p>
<p>Une application lit cette propriété pour déterminer les options de compression d’image ou définit les options de compression d’image actuelles.</p>
<p>Type : <strong>VT_I4</strong>; Accès : lecture/écriture ; Valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>. Si l’appareil peut être défini sur une seule valeur, créez un type de WIA_PROP_LIST et placez la valeur valide dans celui-ci.</p>
<p>Le tableau suivant contient les deux constantes qui sont valides avec cette propriété.</p>

<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Définition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PACKED_PIXEL</td>
<td>Les données de l’image sont au format de pixel compressé.</td>
</tr>
<tr class="even">
<td>WIA_PLANAR</td>
<td>Les données de l’image sont au format Planar.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_PREFERRED_FORMAT"></span><span id="wia_ipa_preferred_format"></span><dl> <dt><strong>WIA_IPA_PREFERRED_FORMAT</strong></dt> <dt>PicturePreferredFormat</dt> </dl></td>
<td style="text-align: left;"><p>Contient le format préféré pour les images que ce minipilote transfère. Le minipilote crée et gère cette propriété.</p>
<p>Obligatoire pour tous les éléments WIA 2,0 avec transfert.</p>
<p>Type : <strong>CLSID</strong>, accès : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_PROP_STREAM_COMPAT_ID"></span><span id="wia_ipa_prop_stream_compat_id"></span><dl> <dt><strong>WIA_IPA_PROP_STREAM_COMPAT_ID</strong></dt> <dt>PicturePropStreamCompatId</dt> </dl></td>
<td style="text-align: left;"><p>Spécifie un CLSID qui représente un ensemble de valeurs de propriétés de périphérique. Si un pilote de périphérique implémente cette fonctionnalité, les applications utilisent cette propriété pour déterminer si l’appareil prend en charge un ensemble de valeurs.</p>
<p>Type : <strong>CLSID</strong>, accès : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Le tableau suivant contient les 12 constantes qui sont valides avec cette propriété.</p>

<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Définition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WiaImgFmt_BMP</td>
<td>Bitmap de point de passe avec un fichier d’en-tête</td>
</tr>
<tr class="even">
<td>WiaImgFmt_EMF</td>
<td>métafichier de Windows étendu</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_EXIF</td>
<td>Format de fichier Exchanger</td>
</tr>
<tr class="even">
<td>WiaImgFmt_FLASHPIX</td>
<td>Format FlashPix</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_GIF</td>
<td>Format d’image GIF</td>
</tr>
<tr class="even">
<td>WiaImgFmt_ICO</td>
<td>format du fichier d’icône Windows</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_JPEG</td>
<td>Format compressé JPEG</td>
</tr>
<tr class="even">
<td>WiaImgFmt_PHOTOCD</td>
<td>Format de fichier Eastman Kodak</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_PNG</td>
<td>Format PNG W3C</td>
</tr>
<tr class="even">
<td>WiaImgFmt_MEMORYBMP</td>
<td>bitmap Windows sans fichier d’en-tête</td>
</tr>
<tr class="odd">
<td>WiaImgFmt_TIFF</td>
<td>Tag Image File Format (TIFF)</td>
</tr>
<tr class="even">
<td>WiaImgFmt_WMF</td>
<td>métafichier Windows</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_RAW_BITS_PER_CHANNEL"></span><span id="wia_ipa_raw_bits_per_channel"></span><dl> <dt><strong>WIA_IPA_RAW_BITS_PER_CHANNEL</strong></dt> <dt>PictureRawBitsPerChannel</dt> </dl></td>
<td style="text-align: left;"><p>pris en charge uniquement dans Windows Vista et versions ultérieures.</p>
<p>Contient le nombre de bits dans chaque canal. Cette propriété doit être signalée comme un vecteur de valeurs d’octets comme il y a de canaux, où le premier octet correspond au nombre de bits dans le premier canal, le deuxième octet au nombre de bits dans le deuxième canal, et ainsi de suite. Il doit y avoir autant d’entrées qu’il y a de canaux en fonction de WIA_IPA_CHANNELS_PER_PIXEL. Le pilote définit cette propriété lorsque l’application passe à WiaImgFmt_RAW. Pour les sous-types connus, il y a autant d’entrées que celles répertoriées dans le tableau sous WIA_IPA_RAW_SUBTYPE.</p>
<p>Type : <strong>VT_UI1</strong> | <strong>VT_VECTOR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_REGION_TYPE"></span><span id="wia_ipa_region_type"></span><dl> <dt><strong>WIA_IPA_REGION_TYPE</strong></dt> <dt>PictureRegionType</dt> </dl></td>
<td style="text-align: left;"><p>Cette propriété est réservée par pour une utilisation future et n’est pas implémentée pour l’instant.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_SUPPRESS_PROPERTY_PAGE"></span><span id="wia_ipa_suppress_property_page"></span><dl> <dt><strong>WIA_IPA_SUPPRESS_PROPERTY_PAGE</strong></dt> <dt>PictureSuppressPropertyPage</dt> </dl></td>
<td style="text-align: left;"><p>Spécifie s’il faut supprimer les pages de propriétés générales des éléments sur l’appareil.</p>
<p>cette propriété est disponible sur Windows XP et versions ultérieures.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Le tableau suivant contient les constantes qui sont valides avec cette propriété. l’astérisque (*) indique que la constante n’est pas valide avec Windows Vista et versions ultérieures. (Disponible uniquement par le biais de l’interface <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> .)</p>

<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PROPPAGE_CAMERA_ITEM_GENERAL *</td>
<td>Supprimer la page de propriétés élément général d’un appareil photo.</td>
</tr>
<tr class="even">
<td>WIA_PROPPAGE_SCANNER_ITEM_GENERAL</td>
<td>Supprimer la page de propriétés d’élément général pour un scanneur.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_IPA_TYMED"></span><span id="wia_ipa_tymed"></span><dl> <dt><strong>WIA_IPA_TYMED</strong></dt> <dt>PictureTymed</dt> </dl></td>
<td style="text-align: left;"><p>Cette propriété contient le paramètre de méthode de transfert. Le minipilote crée et gère cette propriété.</p>
<p>Une application lit cette propriété pour déterminer la méthode de transfert de données du minipilote.</p>
<p>Obligatoire pour tous les éléments WIA 2,0 avec transfert.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Le tableau suivant contient les constantes qui sont valides avec cette propriété. l’astérisque * indique des constantes qui ne sont pas valides avec Windows Vista et versions ultérieures. (Ils sont uniquement disponibles par le biais de l’interface <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> .)</p>

<table>
<thead>
<tr class="header">
<th>Type de transfert</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TYMED_CALLBACK *</td>
<td>Transférer une image en mémoire, en bandes.</td>
</tr>
<tr class="even">
<td>TYMED_MULTIPAGE_CALLBACK *</td>
<td>Transférer plusieurs images en mémoire, en bandes.</td>
</tr>
<tr class="odd">
<td>TYMED_FILE</td>
<td>Transférer une image dans un fichier.</td>
</tr>
<tr class="even">
<td>TYMED_MULTIPAGE_FILE</td>
<td>Transférer une image dans un fichier.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>PictureItemUploadItemSize</dt> </dl></td>
<td style="text-align: left;"><p>pris en charge uniquement dans Windows Vista et versions ultérieures.</p>
<p>Spécifie le nombre d’octets à télécharger pour un élément.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




