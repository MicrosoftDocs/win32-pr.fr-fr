---
description: les constantes suivantes spécifient le type d’élément d’Acquisition d’Image Windows (WIA).
ms.assetid: 7961f692-088a-4f3b-84e9-5fabb0373c3c
title: Indicateurs de type d’élément WIA (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaItemTypeAnalyze
- WiaItemTypeAudio
- WiaItemTypeBurst
- WiaItemTypeDeleted
- WiaItemTypeDevice
- WiaItemTypeDisconnected
- WiaItemTypeDocument
- WiaItemTypeFile
- WiaItemTypeFolder
- WiaItemTypeFree
- WiaItemTypeGenerated
- WiaItemTypeHasAttachments
- WiaItemTypeHPanorama
- WiaItemTypeImage
- WiaItemTypeProgrammableDataSource
- WiaItemTypeRemoved
- WiaItemTypeRoot
- WiaItemTypeStorage
- WiaItemTypeTransfer
- WiaItemTypeTwainCapabilityPassThrough
- WiaItemTypeVideo
- WiaItemTypeVPanorama
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 5a1a76792a79321ba909607ec7f514a40dac4da92fbbfc4623f87eb99881aaa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965528"
---
# <a name="wia-item-type-flags"></a>Indicateurs de type d’élément WIA

les constantes suivantes spécifient le type d’élément d’Acquisition d’Image Windows (WIA).



| Constante                                                                                                                                                                                                                                                                                     | Description                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WiaItemTypeAnalyze"></span><span id="wiaitemtypeanalyze"></span><span id="WIAITEMTYPEANALYZE"></span><dl> <dt>**WiaItemTypeAnalyze**</dt> </dl>                                                                             | Cet élément prend en charge la méthode [**IWiaItem :: AnalyzeItem**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem) . *cette constante n’est pas prise en charge par* Windows Vista *et versions ultérieures.*<br/>                                                                                                                               |
| <span id="WiaItemTypeAudio"></span><span id="wiaitemtypeaudio"></span><span id="WIAITEMTYPEAUDIO"></span><dl> <dt>**WiaItemTypeAudio**</dt> </dl>                                                                                     | L’élément est un fichier audio. Valide uniquement pour les éléments qui ont également l’attribut **WiaItemTypeFile** . <br/>                                                                                                                                                                                     |
| <span id="WiaItemTypeBurst"></span><span id="wiaitemtypeburst"></span><span id="WIAITEMTYPEBURST"></span><dl> <dt>**WiaItemTypeBurst**</dt> </dl>                                                                                     | Pour les dossiers uniquement. Les images de ce dossier ont été effectuées dans un ordre chronologique continu. *cette constante n’est pas prise en charge par* Windows Vista *et versions ultérieures.*<br/>                                                                                                                                       |
| <span id="WiaItemTypeDeleted"></span><span id="wiaitemtypedeleted"></span><span id="WIAITEMTYPEDELETED"></span><dl> <dt>**WiaItemTypeDeleted**</dt> </dl>                                                                             | L’élément est marqué comme supprimé de l’arborescence. <br/>                                                                                                                                                                                                                                          |
| <span id="WiaItemTypeDevice"></span><span id="wiaitemtypedevice"></span><span id="WIAITEMTYPEDEVICE"></span><dl> <dt>**WiaItemTypeDevice**</dt> </dl>                                                                                 | L’élément représente un appareil connecté. <br/>                                                                                                                                                                                                                                               |
| <span id="WiaItemTypeDisconnected"></span><span id="wiaitemtypedisconnected"></span><span id="WIAITEMTYPEDISCONNECTED"></span><dl> <dt>**WiaItemTypeDisconnected**</dt> </dl>                                                         | L’élément représente un appareil déconnecté. <br/>                                                                                                                                                                                                                                            |
| <span id="WiaItemTypeDocument"></span><span id="wiaitemtypedocument"></span><span id="WIAITEMTYPEDOCUMENT"></span><dl> <dt>**WiaItemTypeDocument**</dt> </dl>                                                                         | L’élément représente un document. *cette constante est prise en charge uniquement par* Windows Vista *et versions ultérieures.*<br/>                                                                                                                                                                                        |
| <span id="WiaItemTypeFile"></span><span id="wiaitemtypefile"></span><span id="WIAITEMTYPEFILE"></span><dl> <dt>**WiaItemTypeFile**</dt> </dl>                                                                                         | L’élément est un fichier. <br/>                                                                                                                                                                                                                                                                   |
| <span id="WiaItemTypeFolder"></span><span id="wiaitemtypefolder"></span><span id="WIAITEMTYPEFOLDER"></span><dl> <dt>**WiaItemTypeFolder**</dt> </dl>                                                                                 | L’élément est un dossier. <br/>                                                                                                                                                                                                                                                                 |
| <span id="WiaItemTypeFree"></span><span id="wiaitemtypefree"></span><span id="WIAITEMTYPEFREE"></span><dl> <dt>**WiaItemTypeFree**</dt> </dl>                                                                                         | L’élément n’est pas initialisé ou a été supprimé. <br/>                                                                                                                                                                                                                                        |
| <span id="WiaItemTypeGenerated"></span><span id="wiaitemtypegenerated"></span><span id="WIAITEMTYPEGENERATED"></span><dl> <dt>**WiaItemTypeGenerated**</dt> </dl>                                                                     | Cet élément a été créé par l’application ou le pilote, et n’a pas d’élément correspondant dans l’arborescence des éléments du pilote. <br/>                                                                                                                                                               |
| <span id="WiaItemTypeHasAttachments"></span><span id="wiaitemtypehasattachments"></span><span id="WIAITEMTYPEHASATTACHMENTS"></span><dl> <dt>**WiaItemTypeHasAttachments**</dt> </dl>                                                 | L’élément contient des pièces jointes. *cette constante n’est pas prise en charge par* Windows Vista *et versions ultérieures.*<br/>                                                                                                                                                                                          |
| <span id="WiaItemTypeHPanorama"></span><span id="wiaitemtypehpanorama"></span><span id="WIAITEMTYPEHPANORAMA"></span><dl> <dt>**WiaItemTypeHPanorama**</dt> </dl>                                                                     | L’élément représente une image panoramique horizontale. *cette constante n’est pas prise en charge par* Windows Vista *et versions ultérieures.*<br/>                                                                                                                                                                       |
| <span id="WiaItemTypeImage"></span><span id="wiaitemtypeimage"></span><span id="WIAITEMTYPEIMAGE"></span><dl> <dt>**WiaItemTypeImage**</dt> </dl>                                                                                     | L’élément est un fichier image. Valide uniquement pour les éléments qui ont également l’attribut **WiaItemTypeFile** . <br/>                                                                                                                                                                                     |
| <span id="WiaItemTypeProgrammableDataSource"></span><span id="wiaitemtypeprogrammabledatasource"></span><span id="WIAITEMTYPEPROGRAMMABLEDATASOURCE"></span><dl> <dt>**WiaItemTypeProgrammableDataSource**</dt> </dl>                 | L’élément représente une source de données programmable. *cette constante est prise en charge uniquement par* Windows Vista *et versions ultérieures.*<br/>                                                                                                                                                                        |
| <span id="WiaItemTypeRemoved"></span><span id="wiaitemtyperemoved"></span><span id="WIAITEMTYPEREMOVED"></span><dl> <dt>**WiaItemTypeRemoved**</dt> </dl>                                                                             | L’élément a été supprimé de l’appareil. <br/>                                                                                                                                                                                                                                            |
| <span id="WiaItemTypeRoot"></span><span id="wiaitemtyperoot"></span><span id="WIAITEMTYPEROOT"></span><dl> <dt>**WiaItemTypeRoot**</dt> </dl>                                                                                         | Identifie l’élément racine dans l’arborescence d’objets d’élément de l’appareil. *cette constante est prise en charge uniquement par* Windows Vista *et versions ultérieures.*<br/>                                                                                                                                                         |
| <span id="WiaItemTypeStorage"></span><span id="wiaitemtypestorage"></span><span id="WIAITEMTYPESTORAGE"></span><dl> <dt>**WiaItemTypeStorage**</dt> </dl>                                                                             | L’élément représente un support de stockage. <br/>                                                                                                                                                                                                                                                 |
| <span id="WiaItemTypeTransfer"></span><span id="wiaitemtypetransfer"></span><span id="WIAITEMTYPETRANSFER"></span><dl> <dt>**WiaItemTypeTransfer**</dt> </dl>                                                                         | L’élément peut être transféré. <br/>                                                                                                                                                                                                                                                          |
| <span id="WiaItemTypeTwainCapabilityPassThrough"></span><span id="wiaitemtypetwaincapabilitypassthrough"></span><span id="WIAITEMTYPETWAINCAPABILITYPASSTHROUGH"></span><dl> <dt>**WiaItemTypeTwainCapabilityPassThrough**</dt> </dl> | Ce type indique que l’appareil WIA est capable de recevoir des données de fonctionnalité TWAIN de la couche de compatibilité TWAIN. Si ce type est défini, toutes les fonctionnalités TWAIN qui ne sont pas comprises par la couche de compatibilité TWAIN, pendant une session TWAIN, sont transmises au pilote WIA. <br/> |
| <span id="WiaItemTypeVideo"></span><span id="wiaitemtypevideo"></span><span id="WIAITEMTYPEVIDEO"></span><dl> <dt>**WiaItemTypeVideo**</dt> </dl>                                                                                     | L’élément représente la diffusion vidéo en continu. *cette constante n’est pas prise en charge par* Windows Server 2003 *,* Windows Vista *ou version ultérieure.*<br/>                                                                                                                                                      |
| <span id="WiaItemTypeVPanorama"></span><span id="wiaitemtypevpanorama"></span><span id="WIAITEMTYPEVPANORAMA"></span><dl> <dt>**WiaItemTypeVPanorama**</dt> </dl>                                                                     | L’élément représente une image panoramique verticale. *cette constante n’est pas prise en charge par* Windows Vista *et versions ultérieures.*<br/>                                                                                                                                                                         |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




