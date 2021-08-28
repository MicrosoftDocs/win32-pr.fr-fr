---
description: les constantes suivantes spécifient le jeu de propriétés d’élément de scanneur WIA (Windows Image Acquisition) valides.
ms.assetid: c7c5b10b-81e8-4a30-b20a-ea187724ddd4
title: Constantes de propriété d’élément WIA du scanneur (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_IPS_AUTO_DESKEW
- WIA_IPS_BRIGHTNESS
- WIA_IPS_CONTRAST
- WIA_IPS_CUR_INTENT
- WIA_IPS_DESKEW_X
- WIA_IPS_DESKEW_Y
- WIA_IPS_DOCUMENT_HANDLING_SELECT
- WIA_IPS_FILM_NODE_NAME
- WIA_IPS_FILM_SCAN_MODE
- WIA_IPS_INVERT
- WIA_IPA_ITEMS_STORED
- WIA_IPS_LAMP
- WIA_IPS_LAMP_AUTO_OFF
- WIA_IPS_MAX_HORIZONTAL_SIZE
- WIA_IPS_MAX_VERTICAL_SIZE
- WIA_IPS_MIN_HORIZONTAL_SIZE
- WIA_IPS_MIN_VERTICAL_SIZE
- WIA_IPS_MIRROR
- WIA_IPS_OPTICAL_XRES
- WIA_IPS_OPTICAL_YRES
- WIA_IPS_ORIENTATION
- WIA_IPS_PAGE_SIZE
- WIA_IPS_PAGE_HEIGHT
- WIA_IPS_PAGE_WIDTH
- WIA_IPS_PAGES
- WIA_IPS_PHOTOMETRIC_INTERP
- WIA_IPS_PREVIEW
- WIA_IPS_PREVIEW_TYPE
- WIA_IPS_ROTATION
- WIA_IPS_SEGMENTATION
- WIA_IPS_SHEET_FEEDER_REGISTRATION
- WIA_IPS_SHOW_PREVIEW_CONTROL
- WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION
- WIA_IPS_THRESHOLD
- WIA_IPS_TRANSFER_CAPABILITIES
- WIA_IPA_UPLOAD_ITEM_SIZE
- WIA_IPS_WARM_UP_TIME
- WIA_IPS_XEXTENT
- WIA_IPS_XPOS
- WIA_IPS_XRES
- WIA_IPS_XSCALING
- WIA_IPS_YEXTENT
- WIA_IPS_YPOS
- WIA_IPS_YRES
- WIA_IPS_YSCALING
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 008a806ccaebd595fe7a67ff8f98e6a9385b0bf2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882706"
---
# <a name="scanner-wia-item-property-constants"></a>Constantes de propriété d’élément WIA du scanneur

les constantes suivantes spécifient le jeu de propriétés d’élément de scanneur WIA (Windows Image Acquisition) valides.

Le préfixe « WIA \_ IPS \_ » indique une propriété d’élément pour les périphériques de scanneur et est la Convention d’affectation de noms utilisée dans C/C++. À des fins de script, ces constantes utilisent le préfixe « ScannerPicture » et font partie du type énuméré [WiaItemPropertyId](-wia-wiaitempropertyid.md) . Le nom de membre correspondant de cette énumération de script apparaît entre parenthèses à côté du nom de constante C/C++ dans la liste suivante.



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
<td ><span id="WIA_IPS_AUTO_DESKEW"></span><span id="wia_ips_auto_deskew"></span><dl> <dt><strong>WIA_IPS_AUTO_DESKEW</strong></dt> <dt>ScannerPictureAutoDeskew</dt> </dl></td>
<td ><blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
<br/> Active ou désactive la réalignement automatique.<br/> Facultatif pour WIA_CATEGORY_FEEDER uniquement.<br/> Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a><br/> Le tableau suivant contient les constantes qui sont valides avec cette propriété. 
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_AUTO_DESKEW_ON</td>
<td>Activez la réalignement automatique.</td>
</tr>
<tr class="even">
<td>WIA_AUTO_DESKEW_OFF</td>
<td>Désactivez la réalignement automatique.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_BRIGHTNESS"></span><span id="wia_ips_brightness"></span><dl> <dt><strong>WIA_IPS_BRIGHTNESS</strong></dt> <dt>ScannerPictureBrightness</dt> </dl></td>
<td ><p>Valeurs de luminosité de l’image disponibles dans le scanneur.</p>
<p>Contient le paramètre de luminosité matérielle actuel de l’appareil. Une application définit cette propriété sur la valeur de luminosité du matériel. Le minipilote crée et gère cette propriété.</p>
<p>Les valeurs doivent être mappées dans une plage comprise entre-1000 et 1000, où 1000 correspond à la luminosité maximale, 0 correspond à la luminosité normale et-1000 correspond à la luminosité minimale.</p>
<p>Obligatoire pour tous les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM. Facultatif, mais recommandé, pour les éléments de WIA_CATEGORY_FINISHED_FILE prenant en charge les aperçus.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_CONTRAST"></span><span id="wia_ips_contrast"></span><dl> <dt><strong>WIA_IPS_CONTRAST</strong></dt> <dt>ScannerPictureContrast</dt> </dl></td>
<td ><p>Contient le paramètre de contraste matériel actuel pour un appareil. Une application définit cette propriété sur la valeur de contraste du matériel. Le minipilote crée et gère cette propriété.</p>
<p>Les valeurs doivent être mappées dans une plage comprise entre-1000 et 1000, où-1000 correspond au contraste minimal, 0 correspond au contraste normal et 1000 correspond au contraste maximal.</p>
<p>Obligatoire pour tous les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM. Facultatif, mais recommandé, pour les éléments de WIA_CATEGORY_FINISHED_FILE prenant en charge les aperçus.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_CUR_INTENT"></span><span id="wia_ips_cur_intent"></span><dl> <dt><strong>WIA_IPS_CUR_INTENT</strong></dt> <dt>ScannerPictureCurIntent</dt> </dl></td>
<td ><p>Contient les paramètres d’intention actuels. Le minipilote crée et gère cette propriété.</p>
<p>Obligatoire pour tous les éléments activés pour l’acquisition ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM. Elle n’est pas prise en charge pour les éléments WIA_CATEGORY_FINISHED_FILE ou WIA_CATEGORY_FOLDER.</p>
<p>Type : <strong>VT_I4</strong> accès : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_FLAGS</a></p>
<p>Le pilote les utilise pour prédéfinir les propriétés d’élément en fonction de l’utilisation prévue de l’image par une application. Cela peut inclure, par exemple, la qualité maximale, la taille minimale, etc.</p>
<p>Le pilote choisit la profondeur de bit, en points par pouce, et d’autres paramètres qu’il détermine sont appropriés pour l’intention sélectionnée. Il revient à l’application de lire les paramètres actuels pour déterminer les propriétés qui ont été modifiées. Une application définit cette propriété pour définir automatiquement les propriétés WIA pour une intention d’acquisition spécifique. Cette propriété est obligatoire pour tous les scanneurs.</p>
<p>Une application définit cette propriété pour définir automatiquement les propriétés WIA pour une intention d’acquisition spécifique</p>
<div class="alert">
<blockquote>
[!Note]<br />
Les indicateurs peuvent être combinés avec <strong>un opérateur or</strong> au niveau du bit, mais une image ne peut pas être à la fois des nuances de gris et des couleurs.
</blockquote>
</div>
<div>
 
</div>
<p>Cette propriété est obligatoire pour tous les scanneurs.</p>
<p>Le tableau suivant contient les indicateurs de type image et leurs définitions. Ces indicateurs permettent de définir le type d’image prévu : couleur, nuances de gris, et ainsi de suite.</p>
<p></p>
<table>
<thead>
<tr class="header">
<th>Indicateurs de type d’image prévu</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_INTENT_NONE</td>
<td>Valeur par défaut. Aucun objectif n’est spécifié.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_IMAGE_TYPE_COLOR</td>
<td>L’application envisage de préparer l’appareil pour une analyse des couleurs.</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_IMAGE_TYPE_GRAYSCALE</td>
<td>L’application envisage de préparer l’appareil pour une analyse en nuances de gris.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_IMAGE_TYPE_TEXT</td>
<td>L’application envisage de préparer l’appareil pour l’analyse du texte.</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_IMAGE_TYPE_MASK</td>
<td>Masque pour tous les indicateurs de type image.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Le tableau suivant contient les indicateurs de qualité et de taille et leurs définitions. Ces indicateurs sont utilisés pour définir le niveau de qualité souhaité.</p>

<table>
<thead>
<tr class="header">
<th>Indicateurs de qualité/taille d’image prévus</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_INTENT_MINIMIZE_SIZE</td>
<td>L’application envisage de préparer l’appareil pour l’analyse d’une image qui résulte dans une analyse de petite taille.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_MAXIMIZE_QUALITY</td>
<td>L’application envisage de préparer l’appareil pour l’analyse d’une image de haute qualité.</td>
</tr>
<tr class="odd">
<td>WIA_INTENT_SIZE_MASK</td>
<td>Cet indicateur est un masque pour tous les indicateurs de taille/qualité.</td>
</tr>
<tr class="even">
<td>WIA_INTENT_BEST_PREVIEW</td>
<td>L’application envisage de préparer l’appareil pour l’analyse d’une version préliminaire.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_DESKEW_X"></span><span id="wia_ips_deskew_x"></span><dl> <dt><strong>WIA_IPS_DESKEW_X</strong></dt> <dt>ScannerPictureDeskewX</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Contient le nombre de pixels de l’axe x à partir WIA_IPS_XPOS jusqu’à la coordonnée x du coin supérieur de l’image à décroiser. Par conséquent, il décrit, conjointement avec WIA_IPS_DESKEW_Y, où les deux coins supérieurs de l’image inclinée se trouvent dans le rectangle englobant défini par WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT et WIA_IPS_YEXTENT. sa propriété est implémentée par le pilote du scanneur si elle prend en charge la réalignement.</p>
<p>Les valeurs valides pour WIA_IPS_DESKEW_X doivent être comprises entre 0 et (WIA_IPS_XEXTENT-1). La valeur 0 signifie qu’il n’est pas possible d’effectuer une détorsion.</p>
<p>Cette propriété est facultative pour les éléments des catégories WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER et WIA_CATEGORY_FILM ; elle n’est pas disponible pour les éléments WIA_CATEGORY_FINISHED_FILE ou WIA_CATEGORY_FOLDER.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : WIA_PROP_RANGE</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_DESKEW_Y"></span><span id="wia_ips_deskew_y"></span><dl> <dt><strong>WIA_IPS_DESKEW_Y</strong></dt> <dt>ScannerPictureDeskewY</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Contient le nombre de pixels de l’axe y de WIA_IPS_YPOS à la coordonnée y du coin le plus à gauche de l’image à décroiser. Par conséquent, il décrit, conjointement avec WIA_IPS_DESKEW_X, où les deux coins supérieurs de l’image inclinée se trouvent dans le rectangle englobant défini par WIA_IPS_XPOS, WIA_IPS_YPOS, WIA_IPS_XEXTENT et WIA_IPS_YEXTENT. Cette propriété est implémentée par le pilote du scanneur si elle prend en charge la réalignement.</p>
<p>Les valeurs valides pour WIA_IPS_DESKEW_Y doivent être comprises entre 0 et (WIA_IPS_YEXTENT-1). La valeur 0 signifie qu’il n’est pas possible d’effectuer une détorsion.</p>
<p>Cette propriété est facultative pour les éléments des catégories WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER et WIA_CATEGORY_FILM ; elle n’est pas disponible pour les éléments WIA_CATEGORY_FINISHED_FILE ou WIA_CATEGORY_FOLDER.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : WIA_PROP_RANGE</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_DOCUMENT_HANDLING_SELECT"></span><span id="wia_ips_document_handling_select"></span><dl> <dt><strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong></dt> <dt>ScannerPictureDocumentHandlingSelect</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Contient la source et le mode d’acquisition du scanneur en cours. Le minipilote crée et gère cette propriété.</p>
<p>Une application lit cette propriété pour déterminer la source d’acquisition actuelle du scanneur ou pour écrire cette propriété afin de définir la source et le mode du scanneur. En outre, les applications utilisent cette propriété pour activer et désactiver les fonctionnalités duplex.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>Le tableau suivant contient les constantes qui sont valides avec cette propriété. </p>
<table>
<thead>
<tr class="header">
<th>Indicateurs</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>DUPLEX</td>
<td>Analyse à l’aide d’opérations duplex. Analyser les deux côtés du document à l’aide des paramètres communs configurés pour l’élément du chargeur (WIA_CATEGORY_FEEDER). Les modes DUPLEX et ADVANCE_DUPLEX ne peuvent pas être définis.</td>
</tr>
<tr class="even">
<td>ADVANCED_DUPLEX</td>
<td>Analyse en utilisant des paramètres individuels configurés pour chaque élément du chargeur d’enfants (WIA_CATEGORY_FEEDER_FRONT et WIA_CATEGORY_FEEDER_BACK). Les modes DUPLEX et ADVANCE_DUPLEX ne peuvent pas être définis.</td>
</tr>
<tr class="odd">
<td>FRONT_FIRST</td>
<td>Commencez par analyser le recto du document. Cette valeur est valide lorsque DUPLEX ou ADVANCED_DUPLEX est défini.</td>
</tr>
<tr class="even">
<td>BACK_FIRST</td>
<td>Commencez par analyser le verso du document. Cette valeur est valide lorsque DUPLEX ou ADVANCED_DUPLEX est défini.</td>
</tr>
<tr class="odd">
<td>FRONT_ONLY</td>
<td>Analysez l’avant uniquement.</td>
</tr>
<tr class="even">
<td>BACK_ONLY</td>
<td>Analyser l’arrière uniquement. Cette valeur est valide lorsque DUPLEX ou ADVANCED_DUPLEX est défini.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_FILM_NODE_NAME"></span><span id="wia_ips_film_node_name"></span><dl> <dt><strong>WIA_IPS_FILM_NODE_NAME</strong></dt> <dt>ScannerPictureFilmNodeName</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Permet la spécification d’une pièce jointe d’analyse de film particulière lorsqu’il en existe plusieurs.</p>
<p>Cette propriété est requise pour les éléments de WIA_CATEGORY_FILM lorsqu’il y a plusieurs éléments de numérisation de film. Si l’appareil ne prend en charge qu’un seul élément de film de scanneur racine, cette propriété est facultative.</p>
<p>Type : <strong>VT_BSTR</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Valeurs autorisées : le BSTR doit se présenter sous la forme de @ResourceBinary ,- &lt; ResourceId &gt; pour permettre la localisation, car cette chaîne est exposée à l’utilisateur via l’interface utilisateur de numérisation de film.</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_FILM_SCAN_MODE"></span><span id="wia_ips_film_scan_mode"></span><dl> <dt><strong>WIA_IPS_FILM_SCAN_MODE</strong></dt> <dt>ScannerPictureFilmScanMode</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Active la configuration de l’analyse de pellicule actuelle.</p>
<p>Cette propriété est obligatoire pour l’élément WIA_CATEGORY_FILM.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Le tableau suivant contient les constantes qui sont valides avec cette propriété. </p>
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_FILM_COLOR_SLIDE</td>
<td>Recherchez une diapositive de couleur.</td>
</tr>
<tr class="even">
<td>WIA_FILM_COLOR_NEGATIVE</td>
<td>Rechercher une couleur négative.</td>
</tr>
<tr class="odd">
<td>WIA_FILM_BW_NEGATIVE</td>
<td>Recherche un négatif noir et blanc.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_INVERT"></span><span id="wia_ips_invert"></span><dl> <dt><strong>WIA_IPS_INVERT</strong></dt> <dt>ScannerPictureInvert</dt> </dl></td>
<td ><p>Réservé à une utilisation future et n’est pas mis en œuvre pour l’instant.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPA_ITEMS_STORED"></span><span id="wia_ipa_items_stored"></span><dl> <dt><strong>WIA_IPA_ITEMS_STORED</strong></dt> <dt>ScannerPictureInvert</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Spécifie le nombre d’éléments stockés dans l’élément WIA_CATEGORY_FOLDER.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_LAMP"></span><span id="wia_ips_lamp"></span><dl> <dt><strong>WIA_IPS_LAMP</strong></dt> <dt>ScannerPictureLamp</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Active ou désactive la lampe du scanneur.</p>
<p>Facultatif pour les éléments WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER et WIA_CATEGORY_FILM et recommandé pour WIA_CATEGORY_FILM.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Le tableau suivant contient les constantes qui sont valides avec cette propriété. </p>
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_LAMP_ON</td>
<td>Activez la lampe.</td>
</tr>
<tr class="even">
<td>WIA_LAMP_OFF</td>
<td>Désactivez la lampe.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_LAMP_AUTO_OFF"></span><span id="wia_ips_lamp_auto_off"></span><dl> <dt><strong>WIA_IPS_LAMP_AUTO_OFF</strong></dt> <dt>ScannerPictureLampAutoOff</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Définit la durée maximale de conservation de la lampe lorsque le scanneur n’est pas utilisé.</p>
<p>Facultatif pour les éléments WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER et WIA_CATEGORY_FILM et recommandé pour WIA_CATEGORY_FILM.</p>
<p>Type : <strong>VT_UI4</strong>, Access : lecture/écriture, valeurs valides : 0-0xFFF secondes</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_MAX_HORIZONTAL_SIZE"></span><span id="wia_ips_max_horizontal_size"></span><dl> <dt><strong>WIA_IPS_MAX_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMaxHorizontalSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Spécifie la largeur maximale, en millièmes de pouce, qui est numérisée sur l’axe horizontal (X) à la résolution actuelle. Il peut s’agir de la largeur du chargeur de feuille ou de la vitre de numérisation, en fonction du type d’élément.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_MAX_VERTICAL_SIZE"></span><span id="wia_ips_max_vertical_size"></span><dl> <dt><strong>WIA_IPS_MAX_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMaxVerticalSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Spécifie la hauteur maximale, en millièmes de pouce, qui est analysée sur l’axe vertical (Y) à la résolution actuelle. Il peut s’agir de la hauteur du chargeur de feuille ou de la vitre de numérisation, en fonction du type d’élément.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_MIN_HORIZONTAL_SIZE"></span><span id="wia_ips_min_horizontal_size"></span><dl> <dt><strong>WIA_IPS_MIN_HORIZONTAL_SIZE</strong></dt> <dt>ScannerPictureMinHorizontalSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Spécifie la largeur minimale, en millièmes de pouce, qui est numérisée sur l’axe horizontal (X) à la résolution actuelle.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_MIN_VERTICAL_SIZE"></span><span id="wia_ips_min_vertical_size"></span><dl> <dt><strong>WIA_IPS_MIN_VERTICAL_SIZE</strong></dt> <dt>ScannerPictureMinVerticalSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Spécifie la hauteur minimale, en millièmes de pouce, qui est analysée sur l’axe vertical (Y) à la résolution actuelle.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_MIRROR"></span><span id="wia_ips_mirror"></span><dl> <dt><strong>WIA_IPS_MIRROR</strong></dt> <dt>ScannerPictureMirror</dt> </dl></td>
<td ><p>Réservé à une utilisation future et n’est pas mis en œuvre pour l’instant.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_OPTICAL_XRES"></span><span id="wia_ips_optical_xres"></span><dl> <dt><strong>WIA_IPS_OPTICAL_XRES</strong></dt> <dt>ScannerPictureOpticalXres</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Résolution optique horizontale. Résolution optique horizontale la plus élevée prise en charge en PPP. Cette propriété est une valeur unique. Il ne s’agit pas d’une liste de toutes les résolutions qui peuvent être générées par l’appareil. Au lieu de cela, il s’agit de la résolution des optiques de l’appareil. Le minipilote crée et gère cette propriété. Cette propriété est obligatoire pour tous les éléments.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_OPTICAL_YRES"></span><span id="wia_ips_optical_yres"></span><dl> <dt><strong>WIA_IPS_OPTICAL_YRES</strong></dt> <dt>ScannerPictureOpticalYres</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Résolution optique verticale. Résolution optique verticale la plus élevée prise en charge en PPP. Cette propriété est une valeur unique. Il ne s’agit pas d’une liste de toutes les résolutions générées par l’appareil. Au lieu de cela, il s’agit de la résolution des optiques de l’appareil. Le minipilote crée et gère cette propriété. Cette propriété est obligatoire pour tous les éléments.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_ORIENTATION"></span><span id="wia_ips_orientation"></span><dl> <dt><strong>WIA_IPS_ORIENTATION</strong></dt> <dt>ScannerPictureOrientation</dt> </dl></td>
<td ><p>Spécifie l’orientation actuelle des documents à analyser. Le minipilote crée et gère cette propriété.</p>
<p>Une application définit cette propriété pour définir l’orientation d’origine d’une page ou d’une image à acquérir. Pour plus d’informations sur l’utilisation de WIA_IPS_ORIENTATION, consultez <strong>WIA_IPS_PAGE_SIZE</strong>.</p>
<div class="alert">
<blockquote>
[!Note]<br />
WIA_IPS_ORIENTATION fait référence à la position du document à analyser sur la vitre ou le chargeur du scanneur. Il s’agit de l’orientation du document par rapport à la direction de l’analyse. WIA_IPS_ROTATION fait référence à la rotation appliquée à l’image après son analyse, juste avant que l’image ne soit transférée à l’application.
</blockquote>
</div>
<div>
 
</div>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Le tableau suivant contient les quatre constantes qui sont valides avec cette propriété.</p>

<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Définition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Aperçu</td>
<td>0 degré.</td>
</tr>
<tr class="even">
<td>JARDIN</td>
<td>rotation de 90 degrés-sens des aiguilles d’une montre, par rapport à l’orientation PORTRAIT.</td>
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

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_PAGE_SIZE"></span><span id="wia_ips_page_size"></span><dl> <dt><strong>WIA_IPS_PAGE_SIZE</strong></dt> <dt>ScannerPicturePageSize</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Contient la taille de la page qui est actuellement configurée pour être analysée. Une application définit cette propriété pour sélectionner les dimensions de la page à analyser. Le minipilote crée et gère cette propriété.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Pour connaître les constantes qui peuvent être utilisées avec cette propriété, consultez <a href="-wia-wia2-pagesizeconstants.md"><strong>constantes de taille de page WIA 2,0</strong></a>. Notez ces tailles non fixes, en particulier : </p>
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Définition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_PAGE_CUSTOM</td>
<td>Défini par les valeurs des propriétés <strong>WIA_IPS_PAGE_HEIGHT</strong> et <strong>WIA_IPS_PAGE_WIDTH</strong> .</td>
</tr>
<tr class="even">
<td>WIA_PAGE_AUTO</td>
<td>La taille de la page est automatiquement déterminée par l’appareil.</td>
</tr>
<tr class="odd">
<td>WIA_PAGE_CUSTOM_BASE</td>
<td>Taille de page personnalisée dont les dimensions sont déjà connues de l’application et du pilote de périphérique.</td>
</tr>
</tbody>
</table>

<p> </p>
<p>La valeur de la propriété <strong>WIA_IPS_ORIENTATION</strong> détermine l’orientation de la page actuellement sélectionnée. Les propriétés <strong>WIA_IPS_PAGE_WIDTH</strong> et <strong>WIA_IPS_PAGE_HEIGHT</strong> signalent les dimensions de la page, en millièmes de pouce. Ces propriétés doivent être accordées avec <strong>WIA_IPS_XEXTENT</strong> et <strong>WIA_IPS_YEXTENT</strong>, qui contiennent les dimensions de la page en pixels.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Les valeurs valides de type WIA_PROP_LIST dépendent des paramètres valides de la propriété <strong>WIA_IPS_ORIENTATION</strong> . Si, par exemple, l’appareil ne peut pas analyser les documents orientés paysage avec un paramètre WIA_PAGE_A4, WIA_PAGE_A4 n’est pas une valeur valide pour la propriété <strong>WIA_IPS_PAGE_SIZE</strong> lorsque <strong>WIA_IPS_ORIENTATION</strong> est défini sur paysage.
</blockquote>
</div>
<div>
 
</div>
<p>Si une application définit <strong>WIA_IPS_PAGE_SIZE</strong> sur une valeur autre que les trois dans le tableau ci-dessus, le minipilote doit ajuster les valeurs de <strong>WIA_IPS_PAGE_WIDTH</strong> et <strong>WIA_IPS_PAGE_HEIGHT</strong> aux dimensions de la page, en millièmes de pouce. Elle doit également ajuster les valeurs de <strong>WIA_IPS_XEXTENT</strong> et <strong>WIA_IPS_YEXTENT</strong> sur les dimensions de la page en pixels.</p>
<p>Si un paramètre d’extension (<strong>WIA_IPS_XEXTENT</strong> ou <strong>WIA_IPS_YEXTENT</strong>) est remplacé par une valeur qui ne correspond pas au paramètre de taille de page actuel, le minipilote doit remplacer la valeur de la propriété <strong>WIA_IPS_PAGE_SIZE</strong> par WIA_PAGE_CUSTOM. Le minipilote doit également modifier <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_WIDTH</strong></a> ou <strong>WIA_IPS_PAGE_HEIGHT</strong> conformément au nouveau paramètre d’extension.</p>
<p>Si <strong>WIA_IPS_ORIENTATION</strong> est défini sur paysage, les paramètres d’étendue sont échangés par rapport à leurs valeurs habituelles. Par exemple, si une application définit <strong>WIA_IPS_PAGE_SIZE</strong> sur WIA_PAGE_A4, le minipilote définit <strong>WIA_IPS_PAGE_WIDTH</strong> sur 11692 et <strong>WIA_IPS_PAGE_HEIGHT</strong> sur 8267. (Le minipilote doit également ajuster <strong>WIA_IPS_XEXTENT</strong> et <strong>WIA_IPS_YEXTENT</strong> en conséquence.)</p>
<div class="alert">
<blockquote>
[!Note]<br />
Si <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_IPS_PAGE_SIZE</strong></a> est défini sur WIA_PAGE_CUSTOM, le paramètre d’orientation n’est pas utilisé pour déterminer les dimensions d’étendue de la page à analyser.
</blockquote>
</div>
<div>
 
</div>
<p>Le minipilote est chargé de s’assurer que la propriété <strong>WIA_IPS_ORIENTATION</strong> est en accord avec la zone de sélection actuelle. Si une application remplace la valeur de <strong>WIA_IPS_ORIENTATION</strong> par une valeur non valide pour la taille de page actuellement sélectionnée, le minipilote doit changer la valeur de <strong>WIA_IPS_PAGE_SIZE</strong> en une taille de page prise en charge par la nouvelle valeur d’orientation.</p>
<p>Si une application définit la propriété <strong>WIA_IPS_PAGE_SIZE</strong> sur WIA_PAGE_CUSTOM, la zone de sélection actuelle n’est pas affectée. Le minipilote WIA doit obtenir la disposition actuelle de l’image, en commençant par les paramètres actuels des propriétés <strong>WIA_IPS_XPOS</strong> et <strong>WIA_IPS_YPOS</strong> . Si le paramètre taille de la page se trouve dans une zone de sélection située en dehors de la vitre du scanneur, le minipilote doit automatiquement ajuster les valeurs des propriétés <strong>WIA_IPS_XPOS</strong> et <strong>WIA_IPS_YPOS</strong> aux paramètres valides. Si les propriétés <strong>WIA_IPS_PAGE_SIZE</strong> et <strong>WIA_IPS_ORIENTATION</strong> sont définies en même temps et qu’elles ne sont pas valides lorsqu’elles sont appliquées en combinaison, le minipilote doit faire échouer les paramètres de l’application en renvoyant une erreur dans le <a href="https://msdn.microsoft.com/library/ms794145.aspx">IWiaMiniDrv ::d rvvalidateitemproperties</a>.</p>
<p>Les quatre exemples suivants illustrent différents scénarios de <strong>WIA_IPS_PAGE_SIZE</strong> .</p>
<ol>
<li>Le pilote signale les paramètres.</li>
<li>Une application définit la propriété <strong>WIA_IPS_PAGE_SIZE</strong> sur WIA_PAGE_LETTER.</li>
<li>Une application définit la propriété <strong>WIA_IPS_ORIENTATION</strong> sur paysage.</li>
<li>Une application remplace la propriété <strong>WIA_IPS_XEXTENT</strong> par une valeur inférieure.</li>
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
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_WIDTH = 11500
WIA_IPS_PAGE_HEIGHT = 14000
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
<p><strong>Exemple 2 : une application définit la</strong> <strong></strong><strong>propriété WIA_IPS_PAGE_SIZE sur WIA_PAGE_LETTER</strong>  </p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_PAGE_HEIGHT = 11000
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
<p><strong>Exemple 3 : une application définit la</strong> <strong></strong><strong>propriété WIA_IPS_ORIENTATION sur paysage</strong>  </p>
<p>Le lit physique doit pouvoir acquérir une page qui était à l’origine en orientation paysage.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_LETTER
WIA_IPS_PAGE_HEIGHT = 11000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
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
<p><strong>Exemple 4 : une application remplace la</strong> <strong></strong> <strong>propriété WIA_IPS_XEXTENT par une valeur inférieure</strong></p>
<p>Dans l’exemple suivant, une application remplace la valeur de la propriété <strong>WIA_IPS_XEXTENT</strong> par 1000. Le minipilote doit supposer que la nouvelle valeur contenue dans <strong>WIA_IPS_XEXTENT</strong> n’est plus valide pour la propriété <strong>WIA_IPS_PAGE_SIZE</strong> et doit donc remplacer <strong>WIA_IPS_PAGE_SIZE</strong> par WIA_PAGE_CUSTOM. Le minipilote doit également ajuster <strong>WIA_IPS_PAGE_WIDTH</strong>.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>WIA_IPS_PAGE_SIZE = WIA_PAGE_CUSTOM
WIA_IPS_PAGE_HEIGHT = 10000
WIA_IPS_PAGE_WIDTH = 8500
WIA_IPS_ORIENTATION = LANDSCAPE
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
<td ><span id="WIA_IPS_PAGE_HEIGHT"></span><span id="wia_ips_page_height"></span><dl> <dt><strong>WIA_IPS_PAGE_HEIGHT</strong></dt> <dt>ScannerPicturePageHeight</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Contient la hauteur, en millièmes de pouce, de la page actuellement sélectionnée. Le minipilote crée et gère la propriété <strong>WIA_IPS_PAGE_HEIGHT</strong> . Une application lit cette propriété pour déterminer les dimensions physiques de la page en cours d’analyse. Si les paramètres d’étendue sont différents des tailles de page connues, cette propriété signale la hauteur de la page dont la propriété <strong>WIA_IPS_PAGE_SIZE</strong> est définie sur WIA_PAGE_CUSTOM (qui est une valeur de la propriété <strong>WIA_IPS_PAGE_SIZE</strong> ). <strong>WIA_IPS_PAGE_HEIGHT</strong> doit être synchronisé avec <strong>WIA_IPS_XEXTENT</strong>, qui indique la hauteur, en pixels, de la page à analyser.</p>
<p>Cette propriété est requise pour les éléments de WIA_CATEGORY_FEEDER.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_PAGE_WIDTH"></span><span id="wia_ips_page_width"></span><dl> <dt><strong>WIA_IPS_PAGE_WIDTH</strong></dt> <dt>ScannerPicturePageWidth</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Contient la largeur de la page actuelle sélectionnée, en millièmes de pouce. Une application lit cette propriété pour déterminer les dimensions physiques de la page en cours d’analyse. Si les paramètres d’étendue sont différents des tailles de page connues, cette propriété signale la largeur de la page dont la propriété <strong>WIA_IPS_PAGE_SIZE</strong> est définie sur WIA_PAGE_CUSTOM. <strong>WIA_IPS_PAGE_WIDTH</strong> doit être synchronisée avec la valeur de <strong>WIA_IPS_XEXTENT</strong>, qui indique la largeur, en pixels, de la page à analyser. Le minipilote crée et gère cette propriété.</p>
<p>Cette propriété est requise pour les éléments de WIA_CATEGORY_FEEDER.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_PAGES"></span><span id="wia_ips_pages"></span><dl> <dt><strong>WIA_IPS_PAGES</strong></dt> <dt>ScannerPicturePages</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Contient le nombre actuel de pages à acquérir à partir d’un chargeur automatique de documents. Le minipilote crée et gère cette propriété.</p>
<p>Type : <strong>VT_I4</strong>; Accès : lecture/écriture ; Valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> il s’agit de zéro dans le nombre maximal de pages que le scanneur peut analyser. La valeur est ALL_PAGES (= 0) si le scanneur peut effectuer une analyse continue.</p>
<p>Une application lit cette propriété pour déterminer la capacité de page du chargeur de documents. L’application définit également cette propriété sur le nombre de pages qu’elle va analyser.</p>
<div class="alert">
<blockquote>
[!Note]<br />
Si le mode duplex est activé (<strong>WIA_IPS_DOCUMENT_HANDLING_SELECT</strong> est défini sur alimentation | DUPLEX | ADVANCED_DUPLEX), <strong>WIA_IPS_PAGES</strong> est toujours égal au nombre de pages à analyser.
</blockquote>
</div>
<div>
 
</div>
<p>Une feuille de papier contient automatiquement deux pages si le DUPLEX est activé, même si le côté arrière de la page est vide.</p>
<p>Si vous affectez la valeur 1 à <strong>WIA_IPS_PAGES</strong> , un scanneur traite un côté de la page. Si un scanneur ne parvient pas à analyser un seul côté d’une page en mode duplex, il est recommandé de remplacer la valeur <strong>WIA_IPS_PAGES</strong> pour le membre Inc du membre de la plage de la structure WIA_PROPERTY_INFO par 2. Cette valeur signale à l’application qu’elle doit demander des pages par multiples de deux. La valeur ALL_PAGES (= 0) signifie que <em>toutes les</em> pages qui sont actuellement chargées dans le chargeur de documents doivent être analysées.</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_PHOTOMETRIC_INTERP"></span><span id="wia_ips_photometric_interp"></span><dl> <dt><strong>WIA_IPS_PHOTOMETRIC_INTERP</strong></dt> <dt>ScannerPicturePhotometricInterp</dt> </dl></td>
<td ><p>Contient la valeur actuelle pour les pixels blancs et noirs. Le minipilote crée et gère cette propriété.</p>
<p>Une application lit cette valeur pour déterminer la valeur du blanc ou du noir (en fonction de ce que l’application fait).</p>
<p>Obligatoire pour toutes les acquisitions activées ou éléments stockés ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE et WIA_CATEGORY_FILM. Elle n’est pas prise en charge pour les éléments de WIA_CATEGORY_FOLDER.</p>
<p>Type : <strong>VT_I4</strong>; Accès : lecture/écriture ; Valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a>. Si l’appareil peut être défini sur une seule valeur, créez un WIA_PROP_LIST type et placez la valeur valide dans celui-ci.</p>
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
<td>WIA_PHOTO_WHITE_0</td>
<td>Le blanc est 0 et le noir est 1.</td>
</tr>
<tr class="even">
<td>WIA_PHOTO_WHITE_1</td>
<td>Le blanc est 1 et le noir est 0.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_PREVIEW"></span><span id="wia_ips_preview"></span><dl> <dt><strong>WIA_IPS_PREVIEW</strong></dt> <dt>ScannerPicturePreview</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Indique le mode d’aperçu pour un appareil. Une application définit cette propriété pour placer l’appareil dans un mode aperçu.</p>
<p>Cette propriété est requise pour les éléments WIA_CATEGORY_FLATBED et WIA_CATEGORY_FILM, facultatifs pour l’élément WIA_CATEGORY_FEEDER.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Le tableau suivant contient les constantes qui sont valides avec cette propriété. </p>
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
<tr class="even">
<td ><span id="WIA_IPS_PREVIEW_TYPE"></span><span id="wia_ips_preview_type"></span><dl> <dt><strong>WIA_IPS_PREVIEW_TYPE</strong></dt> <dt>ScannerPicturePreviewType</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Spécifie si l’image d’aperçu existante peut être mise à jour au cours d’une préversion d’image (en réponse à une modification dans les propriétés de WIA_IPA_DATATYPE ou de WIA_IPA_DEPTH).</p>
<p>Cette propriété est facultative pour tous les éléments activés pour l’acquisition qui prennent en charge les analyses d’aperçu. autrement dit, WIA_IPS_PREVIEW est pris en charge avec WIA_PREVIEW_SCAN. Cela comprend les éléments de type WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Le tableau suivant contient les constantes qui sont valides avec cette propriété. </p>
<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_ADVANCED_PREVIEW</td>
<td>La mise à jour de l’image existante est possible.</td>
</tr>
<tr class="even">
<td>WIA_BASIC_PREVIEW</td>
<td>Une autre analyse préliminaire doit être exécutée, car la mise à jour de l’image existante n’est pas possible.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_ROTATION"></span><span id="wia_ips_rotation"></span><dl> <dt><strong>WIA_IPS_ROTATION</strong></dt> <dt>ScannerPictureRotation</dt> </dl></td>
<td ><p>Contient le paramètre de rotation actuel, s’il est implémenté. Le minipilote crée et gère cette propriété.</p>
<p>Une application définit cette propriété pour informer le pilote de la quantité (le cas) de rotation de l’image avant que le pilote le renvoie à l’application.</p>
<div class="alert">
<blockquote>
[!Note]<br />
WIA_IPS_ORIENTATION fait référence à la position du document à analyser sur la vitre ou le chargeur du scanneur. Il s’agit de l’orientation du document par rapport à la direction de l’analyse. WIA_IPS_ROTATION fait référence à la rotation appliquée à l’image après son analyse, juste avant que l’image ne soit transférée à l’application.
</blockquote>
</div>
<div>
 
</div>
<p>Le minipilote WIA est chargé de faire pivoter les données de l’image avant de les renvoyer à l’application. L’application est chargée de vérifier les en-têtes d’image pour voir les valeurs qui viennent d’être pivotées.</p>
<p>Il existe une certaine confusion quant à la résolution de l’effet de la rotation sur la zone de sélection de l’image actuelle (qui est définie par les propriétés <strong>WIA_IPS_XPOS</strong>, <strong>WIA_IPS_YPOS</strong>, <strong>WIA_IPS_XEXTENT</strong> et <strong>WIA_IPS_YEXTENT</strong> ).</p>
<p>La <em>zone de sélection</em> fait référence à la zone sélectionnée sur la vitre du scanneur physique à partir de laquelle une image est acquise. <strong>WIA_IPS_ROTATION</strong> ne modifie pas la zone de sélection. Le pilote applique une rotation dans le sens inverse des aiguilles d’une passe en fonction de <strong>WIA_IPS_ROTATION</strong> uniquement après que le pilote a acquis la zone de sélection appropriée. <strong>WIA_IPS_ROTATION</strong> affecte les dimensions de l’image de sortie, ces dimensions doivent donc être reflétées dans l’en-tête de données de l’image résultante.</p>
<p>Facultatif pour tous les éléments activés pour l’acquisition ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></p>
<p>Les constantes de rotation suivantes sont définies.</p>

<table>
<thead>
<tr class="header">
<th>Constante</th>
<th>Définition</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Aperçu</td>
<td>Le pilote ne fait pas pivoter l’image.</td>
</tr>
<tr class="even">
<td>JARDIN</td>
<td>Le pilote fait pivoter l’image de 90 degrés dans le sens inverse des aiguilles d’une passe.</td>
</tr>
<tr class="odd">
<td>ROT180</td>
<td>Le pilote fait pivoter l’image de 180 degrés dans le sens inverse des aiguilles d’une passe.</td>
</tr>
<tr class="even">
<td>ROT270</td>
<td>Le pilote fait pivoter l’image de 270 degrés dans le sens inverse des aiguilles d’une passe.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_SEGMENTATION"></span><span id="wia_ips_segmentation"></span><dl> <dt><strong>WIA_IPS_SEGMENTATION</strong></dt> <dt>ScannerPictureSegmentation</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Spécifie si l’application doit utiliser le filtre de segmentation du pilote pour l’analyse sur plusieurs régions. WIA_IPS_SEGMENTATION doit être implémenté pour les éléments WIA_CATEGORY_FLATBED et WIA_CATEGORY_FILM s’ils prennent en charge la création d’éléments enfants avec un filtre de segmentation ou si le pilote lui-même crée des éléments enfants pour les frames fixes.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
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
<td>WIA_USE_SEGMENTATION_FILTER</td>
<td>L’application doit utiliser le filtre de segmentation pour l’analyse sur plusieurs régions.</td>
</tr>
<tr class="even">
<td>WIA_DONT_USE_SEGMENTATION_FILTER</td>
<td>Le pilote crée les éléments enfants lui-même pour l’analyse sur plusieurs régions. C’est généralement le cas si le scanneur utilise des frames fixes à cet effet.</td>
</tr>
</tbody>
</table>

<p> </p>
<div class="alert">
<blockquote>
[!Note]<br />
Il est possible qu’un pilote soit fourni avec un filtre de segmentation, mais qu’il ait toujours WIA_IPS_SEGMENTATION défini sur WIA_DONT_USE_SEGMENTATION_FILTER pour l’un de ses éléments (par exemple, l’élément WIA_CATEGORY_FILM). Cela peut être le cas si le scanneur utilise des images fixes pour l’analyse des films, mais pas pour une analyse régulière à partir des éléments de WIA_CATEGORY_FLATBED.
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_SHEET_FEEDER_REGISTRATION"></span><span id="wia_ips_sheet_feeder_registration"></span><dl> <dt><strong>WIA_IPS_SHEET_FEEDER_REGISTRATION</strong></dt> <dt>ScannerPictureSheetFeederRegistration</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
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
<tr class="even">
<td ><span id="WIA_IPS_SHOW_PREVIEW_CONTROL"></span><span id="wia_ips_show_preview_control"></span><dl> <dt><strong>WIA_IPS_SHOW_PREVIEW_CONTROL</strong></dt> <dt>ScannerPictureShowPreviewControl</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Indique si un élément a besoin d’un contrôle d’aperçu affiché pour l’utilisateur. Le minipilote crée et gère cette propriété.</p>
<p>Facultatif pour tous les éléments activés pour le transfert. Il s’agit généralement simplement d’éléments des catégories WIA_ITEM_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM et WIA_CATEGORY_FINISHED_FILE.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Le tableau suivant contient les constantes qui sont valides avec cette propriété. </p>
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
<tr class="odd">
<td ><span id="WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION"></span><span id="wia_ips_supports_child_item_creation"></span><dl> <dt><strong>WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION</strong></dt> <dt>ScannerPictureSupportsChildItemCreation</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Spécifie si l’application (ou les filtres) peut créer des éléments enfants sous l’élément actuel.</p>
<p>Facultatif pour toutes les catégories d’éléments activées pour le transfert : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FILM et même WIA_CATEGORY_FOLDER. (Si le stockage ne prend pas en charge le chargement de nouveaux éléments, cette propriété doit être non prise en charge ou prise en charge avec la valeur <strong>false</strong> .)</p>
<p>Les éléments qui prennent en charge WIA_IPS_SEGMENTATION et WIA_USE_SEGMENTATION_FILTER doivent également prendre en charge WIA_IPS_SUPPORTS_CHILD_ITEM_CREATION et avoir la valeur <strong>true</strong>.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <strong>true</strong> et <strong>false</strong></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_THRESHOLD"></span><span id="wia_ips_threshold"></span><dl> <dt><strong>WIA_IPS_THRESHOLD</strong></dt> <dt>ScannerPictureThreshold</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Spécifie la valeur de nuances de gris qui détermine si un pixel est converti en blanc ou noir quand une image est convertie en monochromatique. Les pixels situés au-dessus du seuil deviennent blancs. Les pixels situés en dessous du seuil deviennent blancs.</p>
<p>Cette propriété est requise pour les éléments d’acquisition qui prennent en charge les analyses 1-BPP et dont la propriété WIA_IPA_DATATYPE est définie sur WIA_DATA_THRESHOLD.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_TRANSFER_CAPABILITIES"></span><span id="wia_ips_transfer_capabilities"></span><dl> <dt><strong>WIA_IPS_TRANSFER_CAPABILITIES</strong></dt> <dt>ScannerPictureTransferCapabilities</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Spécifie si le pilote peut transférer plusieurs éléments enfants dans un appel de transfert unique.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_FLAG</a></p>
<p>La seule valeur possible pour cette propriété est WIA_TRANSFER_CHILDREN_SINGLE_SCAN. Si cet indicateur est défini, le pilote est en charge du transfert de plusieurs éléments enfants dans un appel de transfert unique. Si l’indicateur n’est pas défini, le service WIA parcourt les éléments enfants de manière récursive, puis transfère chacun de ces éléments.</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPA_UPLOAD_ITEM_SIZE"></span><span id="wia_ipa_upload_item_size"></span><dl> <dt><strong>WIA_IPA_UPLOAD_ITEM_SIZE</strong></dt> <dt>ScannerPictureInvert</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Spécifie le nombre d’octets à charger pour l’élément.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_WARM_UP_TIME"></span><span id="wia_ips_warm_up_time"></span><dl> <dt><strong>WIA_IPS_WARM_UP_TIME</strong></dt> <dt>ScannerPictureWarmUpTime</dt> </dl></td>
<td ><p>Spécifie la durée de préchauffage maximale, en millisecondes, nécessaire à l’appareil avant de démarrer l’opération d’analyse. Le minipilote crée et gère cette propriété.</p>
<p>Une application peut lire cette propriété pour déterminer le temps de préchauffage maximal pour cet appareil. Il peut alors présenter une &quot; boîte de dialogue en attente de préchauffage de l’appareil pour &quot; permettre à l’utilisateur de savoir qu’une attente ou une pause peut se produire avant tout problème.</p>
<p>Cette propriété est obligatoire pour tous les éléments d’acquisition activés ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_XEXTENT"></span><span id="wia_ips_xextent"></span><dl> <dt><strong>WIA_IPS_XEXTENT</strong></dt> <dt>ScannerPictureXextent</dt> </dl></td>
<td ><p>Contient la largeur actuelle, en pixels, de l’image sélectionnée à acquérir. Une application définit cette propriété pour marquer la largeur d’une zone de sélection à acquérir. Cette propriété doit accepter la propriété <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> . Le minipilote crée et gère cette propriété.</p>
<p>Obligatoire pour tous les éléments activés pour l’acquisition ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_XPOS"></span><span id="wia_ips_xpos"></span><dl> <dt><strong>WIA_IPS_XPOS</strong></dt> <dt>ScannerPictureXpos</dt> </dl></td>
<td ><p>Contient la coordonnée x, en pixels, de l’angle supérieur gauche de l’image sélectionnée. Une application définit cette propriété pour marquer l’angle supérieur gauche de la zone de sélection. Le minipilote crée et gère cette propriété.</p>
<p>Obligatoire pour tous les éléments activés pour l’acquisition ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE et WIA_CATEGORY_FILM. Elle n’est pas prise en charge pour les éléments de WIA_CATEGORY_FOLDER.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_XRES"></span><span id="wia_ips_xres"></span><dl> <dt><strong>WIA_IPS_XRES</strong></dt> <dt>ScannerPictureXres</dt> </dl></td>
<td ><p>Contient la résolution horizontale actuelle, en pixels par pouce, pour l’appareil. Une application définit cette propriété pour définir la résolution horizontale. Le minipilote crée et gère cette propriété.</p>
<p>Si l’appareil peut être défini sur une seule valeur, créez un type de <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> et placez la valeur valide dans celui-ci. C’est également le cas lorsque l’un des paramètres de résolution dépend d’une autre résolution. (La résolution verticale peut dépendre de la résolution horizontale.)</p>
<p>Obligatoire pour tous les éléments activés pour l’acquisition ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE et WIA_CATEGORY_FILM. Elle n’est pas prise en charge pour les éléments de WIA_CATEGORY_FOLDER.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture ou lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> ou WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_XSCALING"></span><span id="wia_ips_xscaling"></span><dl> <dt><strong>WIA_IPS_XSCALING</strong></dt> <dt>ScannerPictureXscaling</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Définit la mise à l’échelle horizontale, sous la forme d’un pourcentage, qui peut être appliquée aux images numérisées au sein du périphérique du scanneur ou de son pilote.</p>
<p>Cette propriété est facultative pour tous les éléments d’acquisition activés ; autrement dit, les éléments de type WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture ou lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE.</p>
<p>Les valeurs peuvent être comprises entre 1 et maximum VT_I4 (0xFFFF). Par exemple, 100 signifie aucune mise à l’échelle, 050 signifie la mise à l’échelle jusqu’à 50% de la taille de la replacer, et 200 signifie la mise à l’échelle jusqu’à 200% de la taille d’origine.</p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_YEXTENT"></span><span id="wia_ips_yextent"></span><dl> <dt><strong>WIA_IPS_YEXTENT</strong></dt> <dt>ScannerPictureYextent</dt> </dl></td>
<td ><p>Contient la hauteur actuelle, en pixels, de l’image sélectionnée à acquérir. Une application définit cette propriété pour marquer la hauteur d’une zone de sélection. Cette propriété doit être conforme à la valeur de la propriété <a href="-wia-wiaitempropcommonitem.md"><strong>WIA_IPA_PIXELS_PER_LINE</strong></a> . Le minipilote crée et gère cette propriété.</p>
<p>Obligatoire pour tous les éléments activés pour l’acquisition ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_YPOS"></span><span id="wia_ips_ypos"></span><dl> <dt><strong>WIA_IPS_YPOS</strong></dt> <dt>ScannerPictureYpos</dt> </dl></td>
<td ><p>Coordonnée y actuelle, en pixels, de l’angle supérieur gauche de l’image sélectionnée. Une application définit cette propriété pour marquer l’angle supérieur gauche de la zone de sélection. Le minipilote crée et gère cette propriété.</p>
<p>Obligatoire pour tous les éléments activés pour l’acquisition ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE et WIA_CATEGORY_FILM. Elle n’est pas prise en charge pour les éléments de WIA_CATEGORY_FOLDER.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a></p></td>
</tr>
<tr class="even">
<td ><span id="WIA_IPS_YRES"></span><span id="wia_ips_yres"></span><dl> <dt><strong>WIA_IPS_YRES</strong></dt> <dt>ScannerPictureYres</dt> </dl></td>
<td ><p>Contient la résolution verticale actuelle, en pixels par pouce, pour l’appareil. Une application définit cette propriété pour définir la résolution verticale. Le minipilote crée et gère cette propriété.</p>
<p>Si l’appareil peut être défini sur une seule valeur, créez un type de <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> et placez la valeur valide dans celui-ci. C’est également le cas lorsque l’un des paramètres de résolution dépend d’une autre résolution. (La résolution horizontale peut dépendre de la résolution verticale.)</p>
<p>Obligatoire pour tous les éléments activés pour l’acquisition ; autrement dit, les éléments des catégories : WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK, WIA_CATEGORY_FINISHED_FILE et WIA_CATEGORY_FILM. Elle n’est pas prise en charge pour les éléments de WIA_CATEGORY_FOLDER.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture ou lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> ou WIA_PROP_LIST</p></td>
</tr>
<tr class="odd">
<td ><span id="WIA_IPS_YSCALING"></span><span id="wia_ips_yscaling"></span><dl> <dt><strong>WIA_IPS_YSCALING</strong></dt> <dt>ScannerPictureYscaling</dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
cette propriété est prise en charge uniquement par Windows Vista et versions ultérieures.
</blockquote>
</div>
<div>
 
</div>
<p>Définit la mise à l’échelle verticale, sous la forme d’un pourcentage, qui peut être appliquée aux images numérisées au sein du périphérique du scanneur ou de son pilote.</p>
<p>Cette propriété est facultative pour tous les éléments d’acquisition activés ; autrement dit, les éléments de type WIA_CATEGORY_FLATBED, WIA_CATEGORY_FEEDER, WIA_CATEGORY_FEEDER_FRONT, WIA_CATEGORY_FEEDER_BACK et WIA_CATEGORY_FILM.</p>
<p>Type : <strong>VT_I4</strong>, Access : lecture/écriture ou lecture seule, valeurs valides : <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> ou WIA_PROP_RANGE.</p>
<p>Les valeurs peuvent être comprises entre 1 et maximum VT_I4 (0xFFFF). Par exemple, 100 signifie aucune mise à l’échelle, 050 signifie la mise à l’échelle jusqu’à 50% de la taille de la replacer, et 200 signifie la mise à l’échelle jusqu’à 200% de la taille d’origine.</p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




