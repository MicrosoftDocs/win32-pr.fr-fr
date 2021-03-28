---
description: Cette section décrit les indicateurs utilisés par les méthodes de l’interface IActiveDesktop.
title: Indicateurs IActiveDesktop (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6d1a2f69-0730-4805-8b50-071332ff7070
api_name:
- AD_APPLY_ALL
- AD_APPLY_BUFFERED_REFRESH
- AD_APPLY_DYNAMICREFRESH
- AD_APPLY_FORCE
- AD_APPLY_HTMLGEN
- AD_APPLY_REFRESH
- AD_APPLY_SAVE
- COMP_ELEM_ALL
- COMP_ELEM_CHECKED
- COMP_ELEM_CURITEMSTATE
- COMP_ELEM_FRIENDLYNAME
- COMP_ELEM_NOSCROLL
- COMP_ELEM_ORIGINAL_CSI
- COMP_ELEM_POS_LEFT
- COMP_ELEM_POS_TOP
- COMP_ELEM_POS_ZINDEX
- COMP_ELEM_RESTORED_CSI
- COMP_ELEM_SIZE_HEIGHT
- COMP_ELEM_SIZE_WIDTH
- COMP_ELEM_SOURCE
- COMP_ELEM_TYPE
- COMP_TYPE_CFHTML
- COMP_TYPE_CONTROL
- COMP_TYPE_HTMLDOC
- COMP_TYPE_MAX
- COMP_TYPE_PICTURE
- COMP_TYPE_WEBSITE
- COMPONENT_TOP
- WPSTYLE_CENTER
- WPSTYLE_MAX
- WPSTYLE_STRETCH
- WPSTYLE_TILE
- WPSTYLE_SPAN
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dae164c696ae54963f802a6ddd5cb1f6862b2f14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982930"
---
# <a name="iactivedesktop-flags"></a>Indicateurs IActiveDesktop

Cette section décrit les indicateurs utilisés par les méthodes de l’interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .

<dl> <dt>

<span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**AD \_ appliquer \_ tout**
</dt> <dd> <dl> <dt>



Agrégat des valeurs * * * * AD \_ apply \_ Save * * * *, * * * * Active Directory Apply \_ \_ HTMLGEN * * * * et * * * * ad \_ apply \_ Refresh * * * *.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**actualisation de la \_ \_ mise en mémoire tampon appliquée par Active Directory \_**
</dt> <dd> <dl> <dt>



Démarre un minuteur et regroupe toutes les demandes d’actualisation effectuées avec cet indicateur au cours de cet intervalle de temps en une seule actualisation. Cet intervalle est défini sur cinq secondes. À la fin de l’intervalle, ou si une actualisation est demandée au cours de l’intervalle sans un indicateur * * * * AD \_ apply- \_ buffer \_ Refresh * * * *, l’actualisation est effectuée et le minuteur est arrêté. Cet indicateur doit être combiné avec l’indicateur * * * * AD \_ apply \_ Refresh * * * *.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**application active AD \_ \_ DYNAMICREFRESH**
</dt> <dd> <dl> <dt>



[Version 5,0](versions.md). Utilisez le HTML dynamique pour actualiser uniquement les éléments qui ont été modifiés depuis la dernière actualisation, et non l’intégralité du bureau.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**\_application \_ FORCÉe ad**
</dt> <dd> <dl> <dt>



Forcer une modification active sur le bureau.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**application active AD \_ \_ HTMLGEN**
</dt> <dd> <dl> <dt>



Régénérez le fichier HTML du bureau.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**actualisation de l' \_ application ad \_**
</dt> <dd> <dl> <dt>



Actualisez l’élément du bureau.


</dt> </dl> </dd> <dt>

<span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**AD \_ appliquer \_ Enregistrer**
</dt> <dd> <dl> <dt>



Enregistrez l’élément du bureau.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**COMP \_ elem \_ tout**
</dt> <dd> <dl> <dt>



Agrégat des valeurs de COMP \_ elem \_ \* .


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**COMP \_ elem \_ activé**
</dt> <dd> <dl> <dt>



L’élément a été activé.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**COMP \_ elem \_ CURITEMSTATE**
</dt> <dd> <dl> <dt>



État actuel de l’élément de bureau.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMP \_ elem \_ FRIENDLYNAME**
</dt> <dd> <dl> <dt>



Nom convivial de l’élément.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**COMP \_ elem- \_ Scroll elem**
</dt> <dd> <dl> <dt>



L’élément ne peut pas faire l’objet d’un défilement.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**COMP \_ . \_ CSI d’origine elem \_**
</dt> <dd> <dl> <dt>



Informations d’état de l’élément de bureau d’origine.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**COMP \_ elem \_ CDE à \_ gauche**
</dt> <dd> <dl> <dt>



Position horizontale de l’élément.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**COMP \_ elem \_ CDE POS \_ Top**
</dt> <dd> <dl> <dt>



Position verticale de l’élément.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**COMP \_ elem \_ CDE \_ ZINDEX**
</dt> <dd> <dl> <dt>



Index z de l’élément.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**COMP \_ elem \_ - \_ CSI restauré**
</dt> <dd> <dl> <dt>



Informations d’état de l’élément de bureau restaurées.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**RESPECTER \_ la \_ hauteur de taille elem \_**
</dt> <dd> <dl> <dt>



Hauteur de l'élément.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**RESPECTER la largeur de la \_ \_ taille elem \_**
</dt> <dd> <dl> <dt>



Largeur de l'élément.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**COMP \_ elem \_ source**
</dt> <dd> <dl> <dt>



Source d’origine de l’élément.


</dt> </dl> </dd> <dt>

<span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**COMP \_ elem ( \_ type)**
</dt> <dd> <dl> <dt>



Type d'élément.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**COMP \_ type \_ CFHTML**
</dt> <dd> <dl> <dt>



Format HTML compressé.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**COMP ( \_ contrôle de type) \_**
</dt> <dd> <dl> <dt>



L’élément est un contrôle.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**COMP \_ type \_ htmldoc**
</dt> <dd> <dl> <dt>



L’élément est un document HTML. Cet indicateur doit être utilisé uniquement lorsque cela est absolument nécessaire. Cela entraîne l’insertion textuelle d’un document HTML dans le fichier Desktop. htt utilisé pour contrôler la disposition du bureau. Dans la plupart des cas, vous devez utiliser l’indicateur * * * * COMP \_ type \_ Web * * * * pour ajouter des éléments au bureau.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**TYPE de COMP \_ \_ Max.**
</dt> <dd> <dl> <dt>



Valeur maximale d’un indicateur de \_ type COMP \_ \* .


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**\_image de type de comp \_**
</dt> <dd> <dl> <dt>



L’élément est une image.


</dt> </dl> </dd> <dt>

<span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**\_site Web type de comp \_**
</dt> <dd> <dl> <dt>



L’élément est un site Web.


</dt> </dl> </dd> <dt>

<span id="COMPONENT_TOP"></span><span id="component_top"></span>**COMPOSANT en \_ haut**
</dt> <dd> <dl> <dt>



Valeur d’ordre de plan qui signifie que l’élément est en haut.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**\_Centre WPSTYLE**
</dt> <dd> <dl> <dt>



Le papier peint est centré.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**WPSTYLE \_ Max**
</dt> <dd> <dl> <dt>



Valeur maximale d’un indicateur WPSTYLE \_ \* .


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**WPSTYLE \_ Stretch**
</dt> <dd> <dl> <dt>



Le papier peint est étiré pour s’ajuster à la totalité de l’écran.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**\_vignette WPSTYLE**
</dt> <dd> <dl> <dt>



Le papier peint est disposé en mosaïque.


</dt> </dl> </dd> <dt>

<span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**\_étendue WPSTYLE**
</dt> <dd> <dl> <dt>



**Windows 8 et versions ultérieures**: le papier peint s’étend sur plusieurs moniteurs.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
