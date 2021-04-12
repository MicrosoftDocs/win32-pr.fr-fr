---
title: À propos des versions de modèle objet
description: À propos des versions de modèle objet
ms.assetid: 20bb1681-9079-4f8c-bb5e-5c98e3bdc76a
keywords:
- Windows Media Player, versions
- Windows Media Player Object Model (version)
- modèle objet, versions
- Contrôle ActiveX du lecteur Windows Media, versions pour le modèle objet
- Contrôle ActiveX, versions pour le modèle objet
- Windows Media Player Mobile contrôle ActiveX, versions pour le modèle objet
- Windows Media Player Mobile, versions pour le modèle objet
- versions du lecteur Windows Media, modèle objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59886f5750b6fc42112f73d6bb6e05e8d013ffdc
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104381682"
---
# <a name="about-the-object-model-versions"></a>À propos des versions de modèle objet

Le lecteur Windows Media 7,0 a introduit un nouveau modèle d’objet. Ce modèle objet a été étendu avec le lecteur Windows Media 7,1, le lecteur Windows Media pour Windows XP, le lecteur Windows Media série 9, le lecteur Windows Media 10, le lecteur Windows Media 11 et le lecteur Windows Media 12. Chaque rubrique de la référence de modèle objet comprend une section spécifications qui détaille la configuration minimale requise pour la propriété, la méthode ou l’événement individuel. Les listes suivantes détaillent les nouveaux objets, méthodes, propriétés et événements qui ont été ajoutés pour chaque version depuis la version 7,0. Ces listes incluent également de nouvelles interfaces, méthodes et événements C++.

Lorsqu’une interface nouvelle ou mise à jour est également exposée en tant qu’objet, seul l’objet est répertorié. Pour localiser l’interface, reportez-vous à la [Référence du modèle objet pour C++](object-model-reference-for-c.md). En règle générale, vous devez simplement ajouter le préfixe IWMP au nom de l’objet. Si une nouvelle interface étend une interface existante, vous devrez peut-être Rechercher le numéro de version le plus récent. Par exemple, le lecteur Windows Media série 9 a introduit de nouvelles propriétés et méthodes disponibles à partir de l’objet [**Settings**](settings-object.md) . En C++, ces derniers sont disponibles via l’interface [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) , qui étend [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).

## <a name="added-for-windows-media-player-71"></a>Ajouté pour le lecteur Windows Media 7,1

-   [**Propriété Player. stretchToFit**](player-stretchtofit.md)

## <a name="added-for-windows-media-player-for-windows-xp"></a>Ajouté pour le lecteur Windows Media pour Windows XP

-   [**Controls. Step, méthode**](controls-step.md)
-   [**Objet DVD**](dvd-object.md)
-   [**Propriété Media. Error**](media-error.md)
-   [**Événement Player. DomainChange**](player-player-domainchange.md)
-   [**Événement Player. MediaError**](player-player-mediaerror.md)
-   [**Événement Player. OpenPlaylistSwitch**](player-player-openplaylistswitch.md)
-   [**Propriété Player. windowlessVideo**](player-windowlessvideo.md)

## <a name="added-for-windows-media-player-9-series"></a>Ajouté pour le lecteur Windows Media 9

-   [**Méthode ClosedCaption. getSAMILangID**](closedcaption-getsamilangid.md)
-   [**Méthode ClosedCaption. getSAMILangName**](closedcaption-getsamilangname.md)
-   [**Méthode ClosedCaption. getSAMIStyleName**](closedcaption-getsamistylename.md)
-   [**ClosedCaption. SAMILangCount, propriété**](closedcaption-samilangcount.md)
-   [**ClosedCaption. SAMIStyleCount, propriété**](closedcaption-samistylecount.md)
-   [**Controls. audioLanguageCount, propriété**](controls-audiolanguagecount.md)
-   [**Controls. currentAudioLanguage, propriété**](controls-currentaudiolanguage.md)
-   [**Controls. currentAudioLanguageIndex, propriété**](controls-currentaudiolanguageindex.md)
-   [**Controls. currentPositionTimecode, propriété**](controls-currentpositiontimecode.md)
-   [**Controls. getAudioLanguageDescription, méthode**](controls-getaudiolanguagedescription.md)
-   [**Controls. getAudioLanguageID, méthode**](controls-getaudiolanguageid.md)
-   [**Controls. getLanguageName, méthode**](controls-getlanguagename.md)
-   [**ErrorItem. condition, propriété**](erroritem-condition.md)
-   [**External. appColorLight, propriété**](external-appcolorlight.md)
-   [**External. OnColorChange, événement**](external-oncolorchange-event.md)
-   [**External. version, propriété**](external-version.md)
-   [**IWMPEvents ::P événement layerDockedStateChange**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange)
-   [**IWMPEvents ::P événement layerReconnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect)
-   [**Événement IWMPEvents :: SwitchedToControl**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol)
-   [**Événement IWMPEvents :: SwitchedToPlayerApplication**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication)
-   [**Interface IWMPPlayerServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
-   [**Interface IWMPRemoteMediaServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
-   [**Interface IWMPSkinManager**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)
-   [**Méthode Media. getAttributeCountByType**](media-getattributecountbytype.md)
-   [**Méthode Media. getItemInfoByType**](media-getiteminfobytype.md)
-   [**Objet MetadataPicture**](metadatapicture-object.md)
-   [**Objet MetadataText**](metadatatext-object.md)
-   [**Événement Player. AudioLanguageChange**](player-player-audiolanguagechange.md)
-   [**Propriété Player. isRemote**](player-isremote.md)
-   [**Événement Player. MediaCollectionAttributeStringChanged**](player-player-mediacollectionattributestringchanged.md)
-   [**Player. newMedia, méthode**](player-newmedia.md)
-   [**Player. newPlaylist, méthode**](player-newplaylist.md)
-   [**Player. openPlayer, méthode**](player-openplayer.md)
-   [**Propriété Player. playerApplication**](player-playerapplication.md)
-   [**Événement Player. StatusChange**](player-player-statuschange.md)
-   [**Objet PlayerApplication**](playerapplication-object.md)
-   [**Propriété Settings. defaultAudioLanguage**](settings-defaultaudiolanguage.md)
-   [**Propriété Settings. mediaAccessRights**](settings-mediaaccessrights.md)
-   [**Settings. requestMediaAccessRights, méthode**](settings-requestmediaaccessrights.md)

## <a name="added-for-windows-media-player-10"></a>Ajouté pour le lecteur Windows Media 10

-   [**Interface IWMPGraphCreation**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)
-   [**Interface IWMPPlayerServices2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)
-   [**Interface IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
-   [**Interface IWMPSyncServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
-   [**Énumération WMPDeviceStatus**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus)
-   [**Énumération WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)

## <a name="added-for-windows-media-player-11"></a>Ajouté pour le lecteur Windows Media 11

-   [**Interface IWMPCdromBurn**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [**Interface IWMPCdromBurn (VB et C#)**](iwmpcdromburn--vb-and-c.md)
-   [**Interface IWMPCdromRip**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [**Interface IWMPCdromRip (VB et C#)**](iwmpcdromrip--vb-and-c.md)
-   [**Interface IWMPEvents3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
-   [**Interface IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [**Interface IWMPLibrary**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [**Interface IWMPLibrary (VB et C#)**](iwmplibrary--vb-and-c.md)
-   [**Interface IWMPLibraryServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [**Interface IWMPLibraryServices (VB et C#)**](iwmplibraryservices--vb-and-c.md)
-   [**Interface IWMPLibrarySharingServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [**Interface IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [**Interface IWMPMediaCollection2 (VB et C#)**](iwmpmediacollection2--vb-and-c.md)
-   [**Interface IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [**Interface IWMPQuery (VB et C#)**](iwmpquery--vb-and-c.md)
-   [**Interface IWMPRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)
-   [**Interface IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [**Interface IWMPStringCollection2 (VB et C#)**](iwmpstringcollection2--vb-and-c.md)
-   [**Interface IWMPSyncDevice2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [**Interface IWMPVideoRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [**Objet Query**](query-object.md)
-   [**Énumération WMPBurnFormat**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
-   [**Énumération WMPBurnState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
-   [**Énumération WMPLibraryType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
-   [**Énumération WMPRipState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)

## <a name="added-for-windows-media-player-12"></a>Ajouté pour le lecteur Windows Media 12

-   [**Interface IWMPAudioRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**Interface IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**Interface IWMPLibrary2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**Interface IWMPSyncDevice3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos du modèle objet Player**](about-the-player-object-model.md)
</dt> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




