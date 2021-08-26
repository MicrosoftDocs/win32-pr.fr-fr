---
description: Le jeu de propriétés protection de copie de DVD permet d’authentifier les informations de protection contre la copie à partir de déchiffreurs matériels ou logiciels. Utilisez cette propriété pour empêcher toute copie non autorisée à partir d’un DVD-vidéo préenregistré.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: Jeu de propriétés de protection de copie de DVD (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76034c0ac9b310d446f142d31b96ea2edbe6b725
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477346"
---
# <a name="dvd-copy-protection-property-set"></a>Jeu de propriétés protection de copie de DVD

Le jeu de propriétés protection de copie de DVD permet d’authentifier les informations de protection contre la copie à partir de déchiffreurs matériels ou logiciels. Utilisez cette propriété pour empêcher toute copie non autorisée à partir d’un DVD-vidéo préenregistré.

Microsoft fournit des logiciels qui facilitent le processus d’authentification requis par le schéma de chiffrement, ce qui permet à un lecteur de DVD-ROM d’authentifier et de transférer des clés avec un DVD Decrypter. Microsoft n’a pas de plan actuel pour envoyer un DVD Decrypter et, à la place, il fournit un code de système d’exploitation qui servira d’agent pour permettre l’authentification de déchiffreurs matériels ou logiciels.

Le navigateur DVD lance et contrôle le processus d’échange de clés. Le minipilote de DVD n’a besoin que d’implémenter les propriétés suivantes. Les autres composants gèrent le reste.

Chaque flux d’entrée DVD recevra les propriétés de protection de copie. Cela est vrai même si le même matériel contrôle tous les flux de DVD.

Les informations suivantes présentent les constantes et types de données nécessaires à utiliser pour ce jeu de propriétés dans les appels aux méthodes [**IKsPropertySet**](ikspropertyset.md) . Il fournit des valeurs pour les paramètres **GUID** (*GUIDPROPSET*), ID de propriété (*dwPropID*) et type de données de propriété (*pPropData*).



| Étiquette | Valeur |
|-------------------|---------------------------|
| GUID de jeu de propriétés | AM \_ KSPROPSETID \_ CopyProt |



 




| ID de propriété | Description | 
|-------------|-------------|
| <a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a> | Recherche si la sortie vidéo est une vidéo de composant analogique de définition standard. | 
| AM_PROPERTY_COPY_MACROVISION | Il s’agit d’une propriété définie uniquement. Cette propriété définit le niveau de protection de copie analogique pour l’encodeur NTSC à l’extrémité de sortie du code confidentiel de réception. Utilise <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>. | 
| AM_PROPERTY_DVDCOPY_CHLG_KEY | Les opérations d’extraction et de définition sont prises en charge sur cette propriété. Une opération d’extraction demande au décodeur de fournir sa clé de Challenge de bus. Une opération ensembliste fournit le décodeur avec la clé de Challenge du bus à partir du lecteur de DVD. Les données passées dans cette propriété seront une structure de type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>. | 
| AM_PROPERTY_DVDCOPY_DEC_KEY2 | Il s’agit d’une propriété de récupération uniquement. Cette propriété demande que la clé de bus du décodeur 2 soit transférée vers le lecteur de DVD. Les données passées sont une structure de type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>. | 
| AM_PROPERTY_DVDCOPY_DISC_KEY | Propriété Set-only. Cela fournit une clé de disque. La clé est une structure de type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>. | 
| AM_PROPERTY_DVDCOPY_DVD_KEY1 | Il s’agit d’une propriété définie uniquement. Cette propriété fournit la clé de bus de lecteur de DVD 1 au décodeur. Les données passées sont une structure de type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>. | 
| AM_PROPERTY_DVDCOPY_REGION | Code de région demande la définition de région que le décodeur est autorisé à lire comme défini par le consortium de DVD. Cette région est définie en tant que structure de <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> . | 
| AM_PROPERTY_DVDCOPY_SET_COPY_STATE | Les options d’extraction et de définition sont prises en charge sur cette propriété. La méthode est appelée en premier pour déterminer si l’authentification est requise. Les propriétés définies sont des indications relatives à la phase de la négociation de la protection contre la copie que le filtre entre. Les données passées sont une structure de type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>. | 
| AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT | Si cette propriété a la <strong>valeur true</strong>, le navigateur DVD n’envoie pas d’échantillons <strong>AM_UseNewCSSKey</strong> avant de négocier la clé de disque. Consultez <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.<br /> Lecture seule. Les données de propriété sont une valeur <strong>bool</strong> .<br /><blockquote>[!Note]<br />s’applique à Windows 7.</blockquote><br /> | 
| AM_PROPERTY_DVDCOPY_TITLE_KEY | Il s’agit d’une propriété définie uniquement. Cela fournit une clé de titre à partir du contenu actuel. La clé est une structure de type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>. | 




 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Jeux de propriétés](property-sets.md)
</dt> </dl>

 

 




