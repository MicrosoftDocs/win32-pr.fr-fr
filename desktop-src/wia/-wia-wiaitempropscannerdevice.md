---
description: Windows les périphériques matériels d’Acquisition d’images (WIA) ont des valeurs de propriété qui sont stockées dans le registre Windows.
ms.assetid: 78caa3af-927b-4143-9e88-4b5c918d00a4
title: Constantes de propriété de périphérique de scanneur (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPS_DEVICE_ID
- WIA_DPS_DITHER_PATTERN_DATA
- WIA_DPS_DITHER_SELECT
- WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES
- WIA_DPS_DOCUMENT_HANDLING_SELECT
- WIA_DPS_DOCUMENT_HANDLING_STATUS
- WIA_DPS_ENDORSER_CHARACTERS
- WIA_DPS_ENDORSER_STRING
- WIA_DPS_FILTER_SELECT
- WIA_DPS_GLOBAL_IDENTITY
- WIA_DPS_HORIZONTAL_BED_REGISTRATION
- WIA_DPS_HORIZONTAL_BED_SIZE
- WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MAX_SCAN_TIME
- WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE
- WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE
- WIA_DPS_OPTICAL_XRES
- WIA_DPS_OPTICAL_YRES
- WIA_DPS_ORIENTATION
- WIA_DPS_PAD_COLOR
- WIA_DPS_PAGE_HEIGHT
- WIA_DPS_PAGE_SIZE
- WIA_DPS_PAGE_WIDTH
- WIA_DPS_PAGES
- WIA_DPS_PLATEN_COLOR
- WIA_DPS_PREVIEW
- WIA_DPS_SCAN_AHEAD_PAGES
- WIA_DPS_SCAN_AVAILABLE_ITEM
- WIA_DPS_SERVICE_ID
- WIA_DPS_SHEET_FEEDER_REGISTRATION
- WIA_DPS_SHOW_PREVIEW_CONTROL
- WIA_DPS_USER_NAME
- WIA_DPS_VERTICAL_BED_REGISTRATION
- WIA_DPS_VERTICAL_BED_SIZE
- WIA_DPS_VERTICAL_SHEET_FEED_SIZE
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: d9e7afee9b5b639c21e52dc797e7ad42a6ee0dd0
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627185"
---
# <a name="scanner-device-property-constants"></a>Constantes de propriété de périphérique de scanneur

Windows les périphériques matériels d’Acquisition d’images (WIA) ont des valeurs de propriété qui sont stockées dans le registre Windows. Pour plus d’informations, consultez [**constantes de propriété d’appareil courantes**](-wia-wiaitempropcommondevice.md). Les constantes de propriété d’appareil suivantes, avec leurs chaînes associées, sont spécifiques aux scanneurs d’images numériques.

Le préfixe « WIA \_ DPS \_ » indique une propriété d’appareil pour les périphériques de scanneur et est la Convention d’affectation de noms utilisée dans C/C++. À des fins de script, ces constantes utilisent le préfixe « ScannerDevice » et font partie du type énuméré [WiaItemPropertyId](-wia-wiaitempropertyid.md) . Le nom de membre correspondant de cette énumération de script apparaît entre parenthèses à côté du nom de constante C/C++ dans la liste suivante.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Constante/valeur</th>
<th >Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><span id="WIA_DPS_DEVICE_ID"></span><span id="wia_dps_device_id"></span><dl> <dt><strong>WIA_DPS_DEVICE_ID</strong></dt> <dt>ScannerDeviceDeviceId</dt> </dl></td>
<td ><blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement sur Windows Vista et versions ultérieures.
</blockquote>
<br/> Contient un identificateur d’instance de fonction unique pour un périphérique de scanneur de services Web. Cet identificateur représente le service Web sur le périphérique de scanneur avec lequel le mini-pilote WIA communique. Aucune hypothèse relative à la forme de cet identificateur ne doit être faite. Le mini-pilote WIA crée et gère cette propriété. <br/> Les applications WIA peuvent utiliser la valeur de WIA_DPS_DEVICE_ID pour trouver, à l’aide de l’API de détection de fonction, l’objet d’instance de fonction représentant le périphérique Web services scanner utilisé dans la session WIA 2,0 actuelle.<br/> Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_DITHER_PATTERN_DATA"></span><span id="wia_dps_dither_pattern_data"></span><dl> <dt><strong>WIA_DPS_DITHER_PATTERN_DATA</strong></dt> </dl></td>
<td >Réservé, n’utilisez pas.<br/> Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_DITHER_SELECT"></span><span id="wia_dps_dither_select"></span><dl> <dt><strong>WIA_DPS_DITHER_SELECT</strong></dt> </dl></td>
<td >Réservé, n’utilisez pas.<br/> Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES"></span><span id="wia_dps_document_handling_capabilities"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></dt> <dt>ScannerDeviceDocumentHandlingCapabilities</dt> </dl></td>
<td >Contient les fonctionnalités du scanneur. Le minipilote crée et gère cette propriété. <br/> Une application lit cette propriété pour déterminer si le scanneur a un plateau, un chargeur de documents ou un duplexeur installé. Cette propriété est également utilisée pour définir plus précisément les fonctionnalités installées.<br/> Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> le tableau suivant décrit les constantes qui sont valides avec Windows 7 uniquement.<br/> 
<table>
<thead>
<tr class="header">
<th>Indicateurs</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AUTO_SOURCE</td>
<td>Un gestionnaire de documents automatique est installé sur le scanneur.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>le tableau suivant décrit les constantes qui sont valides avec Windows 7 et Windows Vista uniquement.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Indicateurs</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ADVANCED_DUP</td>
<td>L’appareil prend en charge la configuration avancée de l’analyse duplex. Utilisez WIA_IPS_DUPLEX_SETTINGS pour basculer entre l’utilisation de configurations duplex de base et avancées.</td>
</tr>
<tr class="even">
<td>DETECT_FILM_TPA</td>
<td>Le scanneur peut détecter lorsque la carte de transparence/film est prête à être analysée.</td>
</tr>
<tr class="odd">
<td>DETECT_STOR</td>
<td>Le scanneur peut détecter les documents dans le stockage interne.</td>
</tr>
<tr class="even">
<td>FILM_TPA</td>
<td>Le scanneur est équipé d’un adaptateur d’analyse de transparence/film.</td>
</tr>
<tr class="odd">
<td>STOR</td>
<td>Le scanneur est équipé d’un dispositif de stockage d’images interne.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>le tableau suivant décrit les constantes qui sont valides avec Windows XP ou version ultérieure.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Indicateurs</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DETECT_FEED</td>
<td>Le scanneur peut détecter un document dans le chargeur.</td>
</tr>
<tr class="even">
<td>DETECT_FLAT</td>
<td>Le scanneur peut détecter un document sur le plateau à plat.</td>
</tr>
<tr class="odd">
<td>DETECT_SCAN</td>
<td>Le scanneur peut détecter un document dans le chargeur uniquement en analysant.</td>
</tr>
<tr class="even">
<td>DUP</td>
<td>Le scanneur a un duplex.</td>
</tr>
<tr class="odd">
<td>ALIMENTAIRE</td>
<td>Un gestionnaire de documents automatique est installé sur le scanneur.</td>
</tr>
<tr class="even">
<td>PLATE</td>
<td>Le scanneur a un plateau à plateau.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>le tableau suivant décrit les constantes qui sont valides avec Windows XP uniquement. ces valeurs ont été dépréciées pour Windows 7 et Windows Vista et ne doivent pas être utilisées.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Indicateurs</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DETECT_DUP</td>
<td>Le scanneur peut détecter une demande d’analyse duplex de la part de l’utilisateur.</td>
</tr>
<tr class="even">
<td>DETECT_DUP_AVAIL</td>
<td>Le scanneur peut déterminer à quel moment le duplexeur est installé.</td>
</tr>
<tr class="odd">
<td>DETECT_FEED_AVAIL</td>
<td>Le scanneur peut déterminer quand le chargeur automatique de documents est installé.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_dps_document_handling_select"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerDeviceDocumentHandlingSelect</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété n’est pas prise en charge dans Windows Vista et versions ultérieures. Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contient la source et le mode d’acquisition du scanneur en cours. Le minipilote crée et gère cette propriété.</p>
<p>Une application lit cette propriété pour déterminer la source d’acquisition actuelle du scanneur ou pour écrire cette propriété afin de définir la source et le mode du scanneur. En outre, les applications utilisent cette propriété pour activer et désactiver les fonctionnalités duplex.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>Le tableau suivant contient les dix constantes qui sont valides avec cette propriété. </p>
<table>
<thead>
<tr class="header">
<th>Indicateurs</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FEEDER</td>
<td>Analyse à l’aide du chargeur de documents.</td>
</tr>
<tr class="even">
<td>Scanner</td>
<td>Numérisez à l’aide du plateau.</td>
</tr>
<tr class="odd">
<td>DUPLEX</td>
<td>Analyse à l’aide d’opérations duplex.</td>
</tr>
<tr class="even">
<td>AUTO_ADVANCE</td>
<td>Active l’alimentation automatique du document suivant après une analyse.</td>
</tr>
<tr class="odd">
<td>FRONT_FIRST</td>
<td>Commencez par analyser le recto du document. Cette valeur est valide lorsque DUPLEX est défini.</td>
</tr>
<tr class="even">
<td>BACK_FIRST</td>
<td>Commencez par analyser le verso du document. Cette valeur est valide lorsque DUPLEX est défini.</td>
</tr>
<tr class="odd">
<td>FRONT_ONLY</td>
<td>Analysez l’avant uniquement. Cette valeur est valide lorsque DUPLEX est défini.</td>
</tr>
<tr class="even">
<td>BACK_ONLY</td>
<td>Analyser l’arrière uniquement. Cette valeur est valide lorsque DUPLEX est défini.</td>
</tr>
<tr class="odd">
<td>NEXT_PAGE</td>
<td>Analyse la page suivante du document.</td>
</tr>
<tr class="even">
<td>Préalimentation</td>
<td>Activez le mode de pré-flux. Prépositionner le document suivant lors de l’analyse.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_DOCUMENT_HANDLING_STATUS"></span><span id="wia_dps_document_handling_status"></span><dl> <dt><strong>WIA_DPS_DOCUMENT_HANDLING_STATUS</strong></dt> <dt>ScannerDeviceDocumentHandlingStatus</dt> </dl></td>
<td ><p>Contient l’état actuel du plateau installé du scanneur, du chargeur de documents ou du duplexeur. Le minipilote crée et gère cette propriété.</p>
<p>Une application lit cette propriété pour déterminer si le périphérique du scanneur est prêt à être utilisé. Il s’agit d’une façon idéale de vérifier si le papier est dans le chargeur avant d’acquérir une image.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Le tableau suivant contient les constantes qui sont valides avec cette propriété. un astérisque * indique que l’indicateur n’est pas pris en charge dans Windows Vista ou version ultérieure. le symbole <strong>V</strong> indique que l’indicateur est pris en charge uniquement dans Windows Vista et versions ultérieures. </p>
<table>
<thead>
<tr class="header">
<th>Indicateurs</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FEED_READY</td>
<td>Le plateau est prêt à l’emploi.</td>
</tr>
<tr class="even">
<td>FLAT_READY</td>
<td>Le scanneur a un document sur le plateau à plat.</td>
</tr>
<tr class="odd">
<td>DUP_READY</td>
<td>Le duplexeur est activé et prêt à être utilisé.</td>
</tr>
<tr class="even">
<td>FLAT_COVER_UP</td>
<td>Le cache plat est en place.</td>
</tr>
<tr class="odd">
<td>PATH_COVER_UP</td>
<td>Le chemin d’accès au papier est couvert et empêche le bon fonctionnement.</td>
</tr>
<tr class="even">
<td>PAPER_JAM</td>
<td>Un document est coincé dans le chargeur de documents.</td>
</tr>
<tr class="odd">
<td>FILM_TPA_READY<strong>V</strong></td>
<td>L’adaptateur de transparence est installé et prêt à l’emploi.</td>
</tr>
<tr class="even">
<td>STORAGE_READY<strong>V</strong></td>
<td>Le dispositif de stockage interne est prêt.</td>
</tr>
<tr class="odd">
<td>STORAGE_FULL<strong>V</strong></td>
<td>Le stockage est plein, aucune opération de chargement n’est possible.</td>
</tr>
<tr class="even">
<td>MULTIPLE_FEED<strong>V</strong></td>
<td>Une condition de flux multiples s’est produite (généralement avec un PAPER_JAM).</td>
</tr>
<tr class="odd">
<td>DEVICE_ATTENTION<strong>V</strong></td>
<td>Une erreur nécessite une intervention de l’utilisateur sur l’appareil.</td>
</tr>
<tr class="even">
<td>LAMP_ERR<strong>V</strong></td>
<td>Le scanneur n’est pas prêt en raison d’un problème de lampe.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_ENDORSER_CHARACTERS"></span><span id="wia_dps_endorser_characters"></span><dl> <dt><strong>WIA_DPS_ENDORSER_CHARACTERS</strong></dt> <dt>ScannerDeviceEndorserCharacters</dt> </dl></td>
<td ><p>Contient tous les caractères valides qu’une application peut utiliser pour créer des chaînes d’endosseur valides. Un endosseur est une imprimante installée sur un scanneur qui imprime un message texte sur chaque page analysée. Le minipilote doit valider la valeur de la propriété <strong>WIA_DPS_ENDORSER_STRING</strong> par rapport au jeu de caractères valide dans cette propriété. Le minipilote crée et gère cette propriété.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_ENDORSER_STRING"></span><span id="wia_dps_endorser_string"></span><dl> <dt><strong>WIA_DPS_ENDORSER_STRING</strong></dt> <dt>ScannerDeviceEndorserString</dt> </dl></td>
<td ><p>Contient une chaîne qui doit être approuvée (en d’autres termes, imprimée) sur chaque page analysée par le minipilote. Une application définit cette propriété à l’aide du jeu de caractères valide signalé dans la propriété <strong>WIA_DPS_ENDORSER_CHARACTERS</strong> . Le minipilote doit approuver les documents uniquement si une chaîne est définie dans cette propriété. Une chaîne vide signifie que la fonctionnalité de l’endosseur est désactivée.</p>
<p>Étant donné que le pilote est responsable de l’interprétation de la chaîne d’endossement, votre pilote peut utiliser des caractères spéciaux dans <strong>WIA_DPS_ENDORSER_STRING</strong>. Toutefois, seules vos applications comprendront ces caractères.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Un pilote qui prend en charge la propriété <strong>WIA_DPS_ENDORSER_STRING</strong> doit prendre en charge la liste de jetons suivante. </p>
<table>
<thead>
<tr class="header">
<th>par jeton</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>$DATE $</td>
<td>Date au format AAAA/MM/JJ.</td>
</tr>
<tr class="even">
<td>$DAY $</td>
<td>Jour au format jj.</td>
</tr>
<tr class="odd">
<td>$MONTH $</td>
<td>Mois de l’année au format MM.</td>
</tr>
<tr class="even">
<td>$PAGE _COUNT $</td>
<td>Nombre de pages transférées.</td>
</tr>
<tr class="odd">
<td>$TIME $</td>
<td>Heure de la journée au format HH : MM : SS.</td>
</tr>
<tr class="even">
<td>$YEAR $</td>
<td>Année au format YYYY.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_FILTER_SELECT"></span><span id="wia_dps_filter_select"></span><dl> <dt><strong>WIA_DPS_FILTER_SELECT</strong></dt> </dl></td>
<td ><p>Réservé, n’utilisez pas.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_GLOBAL_IDENTITY"></span><span id="wia_dps_global_identity"></span><dl> <dt><strong>WIA_DPS_GLOBAL_IDENTITY</strong></dt> <dt>ScannerDeviceGlobalIdentity</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement sur Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Contient l’adresse SOAP d’un périphérique de scanneur de services Web. Le mini-pilote WIA 2,0 crée et gère cette propriété.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_HORIZONTAL_BED_REGISTRATION"></span><span id="wia_dps_horizontal_bed_registration"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceHorizontalBedRegistration</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété n’est pas prise en charge avec Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Contient l’enregistrement ou l’alignement horizontal pour les documents placés sur le plateau. Le minipilote crée et gère cette propriété.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Le tableau suivant contient les trois constantes qui sont valides avec cette propriété.</p>

<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LEFT_JUSTIFIED</td>
<td>Le papier est justifié à gauche.</td>
</tr>
<tr class="even">
<td>PARTANT</td>
<td>Le papier est centré.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>Le papier est justifié à droite.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Voir aussi</strong></p>
<p><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_HORIZONTAL_BED_SIZE"></span><span id="wia_dps_horizontal_bed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_BED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalBedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété n’est pas prise en charge avec Windows Vista et versions ultérieures. Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Spécifie la largeur maximale, en millièmes de pouce, qui est numérisée sur l’axe horizontal (X) à partir du plateau d’un scanneur à plat dans la résolution actuelle. Cette propriété s’applique également aux alimentations automatiques de documents qui déplacent des feuilles vers le plateau d’un scanneur à plat pour l’analyse. Cette propriété est obligatoire pour les scanneurs qui ont un plateau. À la place, les autres types de scanneurs implémentent la propriété <strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong> .</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceHorizontalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété n’est pas prise en charge avec Windows Vista et versions ultérieures. Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Spécifie la largeur maximale, en millièmes de pouce, qui est numérisée sur l’axe horizontal (X) à partir d’un scanneur de papier portable ou de feuille à la résolution actuelle. Cette propriété s’applique également aux alimentations automatiques de documents qui analysent sans déplacer les feuilles vers le plateau d’un scanneur à plat. Cette propriété est obligatoire pour les scanneurs de feuilles, le défilement et les scanneurs.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_MAX_SCAN_TIME"></span><span id="wia_dps_max_scan_time"></span><dl> <dt><strong>WIA_DPS_MAX_SCAN_TIME</strong></dt> <dt>ScannerDeviceMaxScanTime</dt> </dl></td>
<td ><p>Contient la durée maximale d’analyse d’une page unique avec les paramètres de propriété actuels, en millisecondes. Une application lit cette propriété pour estimer le temps nécessaire à l’analyse d’une page. Cela est utile lorsque vous déterminez les conditions d’un appareil qui a cessé de répondre. Le minipilote crée et gère cette propriété. Cette propriété est obligatoire pour tous les scanneurs.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_horizontal_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinHorizontalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété n’est pas prise en charge avec Windows Vista et versions ultérieures. Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contient les dimensions horizontales physiques de la plus petite page que le chargeur de documents du scanneur peut analyser, en millièmes de pouce. Le minipilote crée et gère cette propriété.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>Voir aussi</strong></p>
<p><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_min_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_MIN_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceMinVerticalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété n’est pas prise en charge avec Windows Vista et versions ultérieures. Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contient les dimensions verticales physiques de la plus petite page que le chargeur de documents du scanneur peut analyser, en millièmes de pouce. Le minipilote crée et gère cette propriété.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p><strong>Voir aussi</strong></p>
<p><strong>WIA_DPS_MIN_HORIZONTAL_SHEET_FEED_SIZE</strong></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_OPTICAL_XRES"></span><span id="wia_dps_optical_xres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_XRES</strong></dt> <dt>ScannerDeviceOpticalXres</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété n’est pas prise en charge par Windows Vista. Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_XRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Résolution optique horizontale. Résolution optique horizontale la plus élevée prise en charge en PPP. Cette propriété est une valeur unique. Il ne s’agit pas d’une liste de toutes les résolutions qui peuvent être générées par l’appareil. Au lieu de cela, il s’agit de la résolution des optiques de l’appareil. Le minipilote crée et gère cette propriété. Cette propriété est obligatoire pour tous les scanneurs.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_OPTICAL_YRES"></span><span id="wia_dps_optical_yres"></span><dl> <dt><strong>WIA_DPS_OPTICAL_YRES</strong></dt> <dt>ScannerDeviceOpticalYres</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété n’est pas prise en charge par Windows Vista. Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_OPTICAL_YRES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Résolution optique verticale. Résolution optique verticale la plus élevée prise en charge en PPP. Cette propriété est une valeur unique. Il ne s’agit pas d’une liste de toutes les résolutions générées par l’appareil. Au lieu de cela, il s’agit de la résolution des optiques de l’appareil. Le minipilote crée et gère cette propriété. Cette propriété est obligatoire pour tous les scanneurs.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_ORIENTATION"></span><span id="wia_dps_orientation"></span><dl> <dt><strong>WIA_DPS_ORIENTATION</strong></dt> <dt>ScannerDeviceOrientation</dt> </dl></td>
<td ><p>Contient le paramètre d’orientation actuel. Le minipilote crée et gère cette propriété.</p>
<p>Une application définit la propriété <strong>WIA_DPS_ORIENTATION</strong> pour définir l’orientation d’origine d’une page ou d’une image à acquérir. Pour plus d’informations sur l’utilisation de WIA_DPS_ORIENTATION, consultez <strong>WIA_DPS_PAGE_SIZE</strong></p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Le tableau suivant contient les quatre constantes qui sont valides avec cette propriété.</p>

<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Définitment</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>JARDIN</td>
<td>rotation de 90 degrés-sens des aiguilles d’une montre, par rapport à l’orientation PORTRAIT.</td>
</tr>
<tr class="even">
<td>Aperçu</td>
<td>0 degré.</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>rotation de 180 degrés-sens des aiguilles d’une montre, par rapport à l’orientation PORTRAIT.</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>rotation de 270 degrés-sens des aiguilles d’une montre, par rapport à l’orientation PORTRAIT.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Voir aussi</strong></p>
<p><a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ROTATION</strong></a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PAD_COLOR"></span><span id="wia_dps_pad_color"></span><dl> <dt><strong>WIA_DPS_PAD_COLOR</strong></dt> <dt>ScannerDevicePadColor</dt> </dl></td>
<td ><p>Couleur utilisée pour remplir le bloc lorsqu’il n’y a pas assez de données image pour remplir une mémoire tampon demandée. Cette propriété est implémentée pour les scanneurs qui complètent la mémoire tampon. Cette propriété est facultative pour tous les scanneurs. Le minipilote crée et gère cette propriété.</p>
<p>Type : <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Le format des informations de couleur est <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_PAGE_HEIGHT"></span><span id="wia_dps_page_height"></span><dl> <dt><strong>WIA_DPS_PAGE_HEIGHT</strong></dt> <dt>ScannerDevicePageHeight</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété n’est pas prise en charge par Windows Vista. Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_HEIGHT</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contient la hauteur, en millièmes de pouce, de la page actuellement sélectionnée. Le minipilote crée et gère la propriété <strong>WIA_DPS_PAGE_HEIGHT</strong> . Une application lit cette propriété pour déterminer les dimensions physiques de la page en cours d’analyse. Si les paramètres d’étendue sont différents des tailles de page connues, cette propriété signale la hauteur de la page dont la propriété <strong>WIA_DPS_PAGE_SIZE</strong> est définie sur WIA_PAGE_CUSTOM (qui est une valeur de la propriété <strong>WIA_DPS_PAGE_SIZE</strong> ). <strong>WIA_DPS_PAGE_HEIGHT</strong> doit être synchronisé avec <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, qui indique la hauteur, en pixels, de la page à analyser.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PAGE_SIZE"></span><span id="wia_dps_page_size"></span><dl> <dt><strong>WIA_DPS_PAGE_SIZE</strong></dt> <dt>ScannerDevicePageSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété n’est pas prise en charge par Windows Vista. Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contient la taille de la page actuellement sélectionnée pour être analysée. Pour sélectionner les dimensions de la page à analyser, une application définit cette propriété. Le minipilote crée et gère cette propriété.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Le tableau suivant contient les trois constantes qui sont valides avec cette propriété. </p>
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Définition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PAGE_A4</td>
<td>8267 X 11692 (orientation PORTRAIT)</td>
</tr>
<tr class="even">
<td>WIA_PAGE_CUSTOM</td>
<td>Défini par les valeurs des propriétés <strong>WIA_DPS_PAGE_HEIGHT</strong> et <strong>WIA_DPS_PAGE_WIDTH</strong></td>
</tr>
<tr class="odd">
<td>WIA_PAGE_LETTER</td>
<td>8500 X 11000 (orientation PORTRAIT)</td>
</tr>
</tbody>
</table>

<p> </p>
<p>La valeur de la propriété <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> détermine l’orientation de la page actuellement sélectionnée. Les propriétés <strong>WIA_DPS_PAGE_WIDTH</strong> et <strong>WIA_DPS_PAGE_HEIGHT</strong> signalent les dimensions de la page, en millièmes de pouce. Notez que ces propriétés doivent être accordées avec <strong>WIA_IPS_XEXTENT</strong> et <strong>WIA_IPS_YEXTENT</strong>, qui contiennent les dimensions de la page en pixels. Les valeurs valides de type WIA_PROP_LIST doivent dépendre des paramètres valides de la propriété <strong>WIA_IPS_ORIENTATION</strong> . Si l’appareil ne peut pas analyser les documents orientés paysage avec un paramètre WIA_PAGE_A4, WIA_PAGE_A4 ne doit pas apparaître dans la liste des valeurs valides pour la propriété <strong>WIA_DPS_PAGE_SIZE</strong> lorsque <strong>WIA_IPS_ORIENTATION</strong> a la valeur Lanscape.</p>
<p>Si une application définit <strong>WIA_DPS_PAGE_SIZE</strong> sur une valeur autre que WIA_PAGE_CUSTOM, le minipilote doit ajuster les valeurs de <strong>WIA_DPS_PAGE_WIDTH</strong> et <strong>WIA_DPS_PAGE_HEIGHT</strong> aux dimensions de la page, en millièmes de pouce. Elle doit également ajuster les valeurs de <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> et <strong>WIA_IPS_YEXTENT</strong> sur les dimensions de la page en pixels.</p>
<p>Si un paramètre d’extension (<a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> ou <strong>WIA_IPS_YEXTENT</strong>) est changé en une valeur qui ne correspond pas au paramètre de taille de page actuel, le minipilote doit changer la valeur de la propriété <strong>WIA_DPS_PAGE_SIZE</strong> en WIA_PAGE_CUSTOM. Le minipilote doit également modifier <strong>WIA_DPS_PAGE_WIDTH</strong> ou <strong>WIA_DPS_PAGE_HEIGHT</strong> conformément au nouveau paramètre d’extension.</p>
<p>Si <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> a la valeur Lanscape, les paramètres d’étendue sont &quot; retournés. &quot; Par exemple, si une application définit <strong>WIA_DPS_PAGE_SIZE</strong> sur WIA_PAGE_A4, le minipilote doit définir <strong>WIA_DPS_PAGE_WIDTH</strong> sur 11692 et <strong>WIA_DPS_PAGE_HEIGHT</strong> sur 8267. (Le minipilote doit également définir <strong>WIA_IPS_XEXTENT</strong> et <strong>WIA_IPS_YEXTENT</strong> en conséquence). Notez que si <strong>WIA_DPS_PAGE_SIZE</strong> est défini sur WIA_PAGE_CUSTOM, le paramètre d’orientation n’est pas utilisé pour déterminer les dimensions d’étendue de la page à analyser.</p>
<p>Le minipilote est chargé de s’assurer que la propriété <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> est en accord avec la zone de sélection actuelle. Si une application remplace la valeur de <strong>WIA_IPS_ORIENTATION</strong> par une valeur non valide pour la taille de page actuellement sélectionnée, le minipilote doit changer la valeur de <strong>WIA_DPS_PAGE_SIZE</strong> en une taille de page prise en charge par la nouvelle valeur d’orientation.</p>
<p>Si une application définit la propriété <strong>WIA_DPS_PAGE_SIZE</strong> sur WIA_PAGE_CUSTOM, la zone de sélection actuelle n’est pas affectée. Le minipilote WIA doit obtenir la disposition actuelle de l’image, en commençant par les paramètres actuels des propriétés <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XPOS</strong></a> et <strong>WIA_IPS_YPOS</strong> . Si le paramètre de taille de page produit une zone de sélection située en dehors de la vitre du scanneur, le minipilote doit automatiquement ajuster les valeurs des propriétés <strong>WIA_IPS_XPOS</strong> et <strong>WIA_IPS_YPOS</strong> aux paramètres valides. Si les propriétés <strong>WIA_DPS_PAGE_SIZE</strong> et <strong>WIA_IPS_ORIENTATION</strong> sont définies en même temps et qu’elles ne sont pas valides lorsqu’elles sont appliquées en combinaison, le minipilote doit faire échouer les paramètres de l’application en renvoyant une erreur dans le <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv ::d rvvalidateitemproperties</a>. .</p>
<p>Les quatre exemples suivants illustrent différents scénarios de <strong>WIA_DPS_PAGE_SIZE</strong> .</p>
<ol>
<li>Le pilote signale les paramètres.</li>
<li>Une application définit la propriété <strong>WIA_DPS_PAGE_SIZE</strong> sur WIA_PAGE_LETTER.</li>
<li>Une application définit la propriété <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_ORIENTATION</strong></a> sur Lanscape.</li>
<li>Une application remplace la propriété <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> par une valeur inférieure.</li>
</ol>
<p><strong>Exemple 1 : le minipilote signale les paramètres</strong></p>
<p>Dans l’exemple suivant, le minipilote définit une zone de sélection personnalisée avant qu’une application définisse des propriétés WIA. Dans ce cas, la zone de sélection représente l’ensemble du plateau.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_WIDTH = 11500
WIA_DPS_PAGE_HEIGHT = 14000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1150
WIA_IPS_YEXTENT = 1400
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><strong>Exemple 2 : une application définit la</strong> <strong></strong><strong>propriété WIA_DPS_PAGE_SIZE sur WIA_PAGE_LETTER</strong>  </p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_WIDTH = 8500
WIA_DPS_PAGE_HEIGHT = 11000
WIA_IPS_ORIENTATION = PORTRAIT
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 850
WIA_IPS_YEXTENT = 1100
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><strong>Exemple 3 : une application définit la</strong> <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a><strong>propriété WIA_IPS_ORIENTATION sur Lanscape</strong>  </p>
<p>Le lit physique doit pouvoir acquérir une page qui était à l’origine en orientation paysage.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_DPS_PAGE_HEIGHT = 11000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1100
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p><strong>Exemple 4 : une application remplace la</strong> <a href="-wia-wiaitempropscanneritem.md"><strong></strong></a><strong>propriété WIA_IPS_XEXTENT par une valeur inférieure</strong>  </p>
<p>Dans l’exemple suivant, une application remplace la valeur de la propriété <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a> par 1000. Le minipilote doit supposer que la nouvelle valeur contenue dans <strong>WIA_IPS_XEXTENT</strong> n’est plus valide pour la propriété <strong>WIA_DPS_PAGE_SIZE</strong> et doit donc remplacer <strong>WIA_DPS_PAGE_SIZE</strong> par WIA_PAGE_CUSTOM. Le minipilote doit également ajuster <strong>WIA_DPS_PAGE_WIDTH</strong>.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_DPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_DPS_PAGE_HEIGHT = 10000
WIA_DPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANSCAPE
WIA_IPS_XPOS = 0
WIA_IPS_YPOS = 0
WIA_IPS_XEXTENT = 1000
WIA_IPS_YEXTENT = 850
WIA_IPS_XRES = 100
WIA_IPS_YRES = 100</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_PAGE_WIDTH"></span><span id="wia_dps_page_width"></span><dl> <dt><strong>WIA_DPS_PAGE_WIDTH</strong></dt> <dt>ScannerDevicePageWidth</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété n’est pas prise en charge par Windows Vista. Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contient la largeur de la page actuelle sélectionnée, en millièmes de pouce. Une application lit cette propriété pour déterminer les dimensions physiques de la page en cours d’analyse. Si les paramètres d’étendue sont différents des tailles de page connues, cette propriété signale la largeur de la page dont la propriété <strong>WIA_DPS_PAGE_SIZE</strong> est définie sur WIA_PAGE_CUSTOM. <strong>WIA_DPS_PAGE_WIDTH</strong> doit être synchronisée avec la valeur de <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_XEXTENT</strong></a>, qui indique la largeur, en pixels, de la page à analyser. Le minipilote crée et gère cette propriété.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PAGES"></span><span id="wia_dps_pages"></span><dl> <dt><strong>WIA_DPS_PAGES</strong></dt> <dt>ScannerDevicePages</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété n’est pas prise en charge par Windows Vista. Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PAGES</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contient le nombre actuel de pages à acquérir à partir d’un chargeur automatique de documents. Le minipilote crée et gère cette propriété.</p>
<p>Type : <strong>VT_I4</strong>; Accès : lecture/écriture ; Valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> (zéro jusqu’au nombre maximal de pages que le chargeur de documents peut contenir)</p>
<p>Une application lit cette propriété pour déterminer la capacité de page du chargeur de documents. L’application définit également cette propriété sur le nombre de pages qu’elle va analyser.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Si le mode duplex est activé (<strong>WIA_DPS_DOCUMENT_HANDLING_SELECT</strong> est défini sur alimentation | DUPLEX), <strong>WIA_DPS_PAGES</strong> est toujours égal au nombre de pages à analyser.
</blockquote>
</div>
<div>
 
</div>
<p>Une feuille de papier contient automatiquement deux pages si le DUPLEX est activé, même si le côté arrière de la page est vide.</p>
<p>Si vous affectez la valeur 1 à <strong>WIA_DPS_PAGES</strong> , un scanneur traite l’un des côtés de la page. Si un scanneur ne parvient pas à analyser un seul côté d’une page alors qu’il est en mode duplex, le <strong>WIA_DPS_PAGES</strong> valeur valide pour le membre Inc de la structure WIA_PROPERTY_INFO doit être changée en 2. Cette valeur signale à l’application qu’elle doit demander des pages par multiples de deux. La valeur zéro signifie que <em>toutes les</em> pages qui sont actuellement chargées dans le chargeur de documents doivent être analysées.</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_PLATEN_COLOR"></span><span id="wia_dps_platen_color"></span><dl> <dt><strong>WIA_DPS_PLATEN_COLOR</strong></dt> <dt>ScannerDevicePlatenColor</dt> </dl></td>
<td ><p>Spécifie la couleur du plateau dans l’arrière de la feuille à analyser. Cette propriété est facultative pour les scanneurs qui ont un plateau. Le minipilote crée et gère cette propriété.</p>
<p>Type : <strong>VT_UI1</strong>  |  <strong>VT_VECTOR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Le format des informations de couleur est <a href="/windows/win32/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a>.</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_PREVIEW"></span><span id="wia_dps_preview"></span><dl> <dt><strong>WIA_DPS_PREVIEW</strong></dt> <dt>ScannerDevicePreview</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété n’est pas prise en charge par Windows Vista. Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_PREVIEW</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Indique le mode d’aperçu pour un appareil. Une application définit cette propriété pour placer l’appareil dans un mode aperçu.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Le tableau suivant contient les deux constantes qui sont valides avec cette propriété. </p>
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Définition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_FINAL_SCAN</td>
<td>L’application effectue une analyse finale.</td>
</tr>
<tr class="even">
<td>WIA_PREVIEW_SCAN</td>
<td>L’application effectue une analyse de l’aperçu.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_SCAN_AHEAD_PAGES"></span><span id="wia_dps_scan_ahead_pages"></span><dl> <dt><strong>WIA_DPS_SCAN_AHEAD_PAGES</strong></dt> <dt>ScannerDeviceScanAheadPages</dt> </dl></td>
<td ><p>Contient une valeur qui indique si le scanneur met en cache des pages dans une mémoire tampon de scanneur avant de les envoyer à l’application.</p>
<p>Une valeur de zéro désactive l’analyse à l’avance et aucune page n’est analysée. Les transferts de données normaux sur l’élément d’analyse mis en mémoire tampon récupèrent les pages mises en mémoire tampon. Les propriétés WIA ne peuvent pas être modifiées lors d’une opération d’analyse anticipée. Cette propriété est facultative.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> de zéro au nombre maximal de pages que le chargeur de documents peut contenir.</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_SCAN_AVAILABLE_ITEM"></span><span id="wia_dps_scan_available_item"></span><dl> <dt><strong>WIA_DPS_SCAN_AVAILABLE_ITEM</strong></dt> <dt>ScannerDeviceScanAvailableItem</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows 7 et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Indique la source d’entrée à partir de laquelle effectuer l’analyse, ou l’emplacement de stockage à partir duquel les données sont transférées.</p>
<p>Un événement d’analyse informe l’application que l’utilisateur a lancé une analyse, mais l’événement ne fournit pas le nom de l’élément WIA qui représente la source d’entrée. Le gestionnaire d’événements de l’application peut interroger la propriété de WIA_DPS_SCAN_AVAILABLE_ITEM de l’élément racine pour obtenir le nom de l’élément source d’entrée.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> de zéro au nombre maximal de pages que le chargeur de documents peut contenir.</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_SERVICE_ID"></span><span id="wia_dps_service_id"></span><dl> <dt><strong>WIA_DPS_SERVICE_ID</strong></dt> <dt>ScannerDeviceServiceId</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Contient l’ID de service d’un périphérique de scanneur de services Web. Le mini-pilote WIA 2,0 crée et gère cette propriété.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_dps_sheet_feeder_registration"></span><dl> <dt><strong>WIA_DPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerDeviceSheetFeederRegistration</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété n’est pas prise en charge avec Windows Vista et versions ultérieures. Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Contient les détections d’alignement, d’alignement et de bord pour les documents placés sur le plateau. Le minipilote crée et gère cette propriété. Cette propriété indique comment la feuille est positionnée horizontalement sur la tête de numérisation d’un lecteur de poche ou d’un scanneur à feuille. La propriété permet de prédire où un document est placé sur l’en-tête d’analyse.</p>
<p>Pour les scanneurs qui prennent en charge plusieurs têtes d’analyse, cette propriété est relative à la tête d’analyse la plus haut. Cette propriété est obligatoire pour les scanneurs de feuille, d’alimentation et de défilement.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Le tableau suivant contient les trois constantes qui sont valides avec cette propriété.</p>

<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>LEFT_JUSTIFIED</td>
<td>La feuille est positionnée à gauche par rapport à la tête de numérisation.</td>
</tr>
<tr class="even">
<td>PARTANT</td>
<td>La feuille est centrée sur la tête de numérisation.</td>
</tr>
<tr class="odd">
<td>RIGHT_JUSTIFIED</td>
<td>La feuille est positionnée à droite par rapport à la tête de numérisation.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_dps_show_preview_control"></span><dl> <dt><strong>WIA_DPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerDeviceShowPreviewControl</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété n’est pas prise en charge par Windows Vista. Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Indique si un élément a besoin d’un contrôle d’aperçu affiché pour l’utilisateur. Le minipilote crée et gère cette propriété.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Le tableau suivant contient les deux constantes qui sont valides avec cette propriété. </p>
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_SHOW_PREVIEW_CONTROL</td>
<td>Affichez un contrôle d’aperçu pour l’utilisateur, car ce dernier peut effectuer une préversion.</td>
</tr>
<tr class="even">
<td>WIA_DONT_SHOW_PREVIEW_CONTROL</td>
<td>N’affiche pas un contrôle d’aperçu pour l’utilisateur, car cet appareil ne peut pas effectuer d’aperçu.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_USER_NAME"></span><span id="wia_dps_user_name"></span><dl> <dt><strong>WIA_DPS_USER_NAME</strong></dt> <dt>ScannerDeviceUserName</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Utilisé par le service WIA pour informer le mini-pilote du nom du compte d’utilisateur (y compris le nom de domaine réseau, le cas échéant) de la session dans laquelle l’application WIA en cours est en cours d’exécution.</p>
<p>Il s’agit d’une propriété d’élément racine, gérée par le service WIA.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_VERTICAL_BED_REGISTRATION"></span><span id="wia_dps_vertical_bed_registration"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_REGISTRATION</strong></dt> <dt>ScannerDeviceVerticalBedRegistration</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété n’est pas prise en charge avec Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Contient l’inscription, ou l’alignement vertical et la détection des bords, pour les documents placés sur le plateau. Le minipilote crée et gère cette propriété.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Le tableau suivant contient les trois constantes qui sont valides avec cette propriété. </p>
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>TOP_JUSTIFIED</td>
<td>Le papier est aligné en haut.</td>
</tr>
<tr class="even">
<td>PARTANT</td>
<td>Le papier est centré.</td>
</tr>
<tr class="odd">
<td>BOTTOM_JUSTIFIED</td>
<td>Le papier est justifié en bas.</td>
</tr>
</tbody>
</table>

<p> </p>
<p><strong>Voir aussi</strong>.</p>
<p><strong>WIA_DPS_HORIZONTAL_BED_REGISTRATION</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_DPS_VERTICAL_BED_SIZE"></span><span id="wia_dps_vertical_bed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_BED_SIZE</strong></dt> <dt>ScannerDeviceVerticalBedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété n’est pas prise en charge avec Windows Vista et versions ultérieures. Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Spécifie la hauteur maximale, en millièmes de pouce, qui est analysée sur l’axe vertical (Y) à partir du plateau d’un scanneur à plat dans la résolution actuelle. Cette propriété s’applique également aux alimentations automatiques de documents, qui déplacent les feuilles vers le plateau d’un scanneur à plat à des fins de numérisation. Cette propriété est obligatoire pour les scanneurs qui ont un plateau. À la place, les autres types de scanneurs implémentent la propriété <strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong> .</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_DPS_VERTICAL_SHEET_FEED_SIZE"></span><span id="wia_dps_vertical_sheet_feed_size"></span><dl> <dt><strong>WIA_DPS_VERTICAL_SHEET_FEED_SIZE</strong></dt> <dt>ScannerDeviceVerticalSheetFeedSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété n’est pas prise en charge avec Windows Vista et versions ultérieures. Utilisez <a href="-wia-wiaitempropscanneritem.md"><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></a>.
</blockquote>
</div>
<div>
 
</div>
<p>Spécifie la hauteur maximale, en millièmes de pouce, qui est numérisée sur l’axe vertical (Y) à partir d’un scanneur de papier portable ou de feuille à la résolution actuelle. Cette propriété s’applique également aux alimentations automatiques de documents qui analysent sans déplacer les feuilles vers le plateau d’un scanneur à plat. Cette propriété est obligatoire pour les scanneurs feuille à alimentation. Les scanneurs à défilement et les scanneurs de la main ne doivent pas implémenter cette propriété.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
