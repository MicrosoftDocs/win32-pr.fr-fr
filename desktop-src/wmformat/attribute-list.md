---
title: Liste d’attributs
description: Liste d’attributs
ms.assetid: 81fc356e-ee7a-4630-841f-6c1543e022d3
keywords:
- Windows Media Format SDK, attributs
- ASF (Advanced Systems Format), attributs
- ASF (format des systèmes avancés), attributs
- attributs, liste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793c0a860f6f9e40257bb6aec610dc7680b34538
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507922"
---
# <a name="attribute-list"></a>Liste d’attributs

Les attributs prédéfinis inclus dans ce kit de développement logiciel (SDK) sont présentés par ordre alphabétique dans le tableau suivant. Chaque attribut a un nom, un identificateur global et un type de données tel que défini par le membre approprié de l’énumération de [**\_ \_ DataTypes WMT attr**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_attr_datatype) . Certains attributs n’utilisent pas un type de données simple ou sont mis en forme selon une structure. Les entrées de ces attributs répertorient un nom de structure dans la colonne de type de données avec le type de données utilisé pour définir la valeur entre parenthèses.

> [!Note]  
> Consultez la liste des attributs [DRM](drm-attribute-list.md) pour obtenir une table de tous les attributs DRM.

 

Lorsque vous programmez avec ces attributs, vous devez utiliser l’identificateur global au lieu d’utiliser le nom comme littéral de chaîne. À l’aide de l’identificateur global, les erreurs typographiques génèrent une erreur au moment de la compilation.



| Nom de l’attribut                                                                       | Identificateur global                             | Type de données                                            |
|--------------------------------------------------------------------------------------|-----------------------------------------------|------------------------------------------------------|
| [**ASFLeakyBucketPairs**](asfleakybucketpairs.md)                                   | \_wszASFLeakyBucketPairs g                     | **\_binaire de type WMT \_**                                |
| [**AspectRatioX**](aspectratiox.md)                                                 | \_wszWMAspectRatioX g                          | **\_valeur DWORD de type WMT \_**                                 |
| [**AspectRatioY**](aspectratioy.md)                                                 | \_wszWMAspectRatioY g                          | **\_valeur DWORD de type WMT \_**                                 |
| [**Auteur**](author.md)                                                             | \_wszWMAuthor g                                | **\_chaîne de type WMT \_**                                |
| [**AverageLevel**](averagelevel.md)                                                 | \_wszAverageLevel g                            | **\_valeur DWORD de type WMT \_**                                 |
| [**BannerImageData**](bannerimagedata.md)                                           | \_wszWMBannerImageData g                       | **\_binaire de type WMT \_**                                |
| [**BannerImageType**](bannerimagetype.md)                                           | \_wszWMBannerImageType g                       | **\_valeur DWORD de type WMT \_**                                 |
| [**BannerImageURL**](bannerimageurl.md)                                             | \_wszWMBannerImageURL g                        | **\_chaîne de type WMT \_**                                |
| [**Bitrate**](bit-rate.md)                                                          | \_wszWMBitrate g                               | **\_valeur DWORD de type WMT \_**                                 |
| [**Diffusion**](broadcast.md)                                                       | \_wszWMBroadcast g                             | **\_type WMT \_ bool**                                  |
| [**BufferAverage**](bufferaverage.md)                                               | \_wszBufferAverage g                           | **\_valeur DWORD de type WMT \_**                                 |
| [**Peut \_ passer à l' \_ arrière**](can-skip-backward.md)                                     | \_wszWMSkipBackward g                          | **\_type WMT \_ bool**                                  |
| [**Peut \_ avancer \_**](can-skip-forward.md)                                       | \_wszWMSkipForward g                           | **\_type WMT \_ bool**                                  |
| [**copyright**](copyright.md)                                                       | \_wszWMCopyright g                             | **\_chaîne de type WMT \_**                                |
| [**CopyrightURL**](copyrighturl.md)                                                 | \_wszWMCopyrightURL g                          | **\_chaîne de type WMT \_**                                |
| [**CurrentBitrate**](currentbitrate.md)                                             | \_wszWMCurrentBitrate g                        | **\_valeur DWORD de type WMT \_**                                 |
| [**Description**](description.md)                                                   | \_wszWMDescription g                           | **\_chaîne de type WMT \_**                                |
| [**\_CONTENTID DRM**](drm-contentid.md)                                              | g \_ wszWMDRM \_ contentid                        | **\_chaîne de type WMT \_**                                |
| [**\_DRMHEADER DRM \_ ContentDistributor**](drm-drmheader-contentdistributor.md)       | g \_ wszWMDRM \_ DRMHeader \_ ContentDistributor    | **\_chaîne de type WMT \_**                                |
| [**\_DRMHEADER DRM \_ contentid**](drm-drmheader-contentid.md)                         | g \_ wszWMDRM \_ DRMHeader \_ contentid             | **\_chaîne de type WMT \_**                                |
| [**\_DRMHEADER DRM \_ IndividualizedVersion**](drm-drmheader-individualizedversion.md) | g \_ wszWMDRM \_ DRMHeader \_ IndividualizedVersion | **\_chaîne de type WMT \_**                                |
| [**\_DRMHEADER DRM \_ KeyId**](drm-drmheader-keyid.md)                                 | g \_ wszWMDRM \_ DRMHeader \_ KeyId                 | **\_chaîne de type WMT \_**                                |
| [**\_DRMHEADER DRM \_ LicenseAcqURL**](drm-drmheader-licenseacqurl.md)                 | g \_ wszWMDRM \_ DRMHeader \_ LicenseAcqURL         | **\_chaîne de type WMT \_**                                |
| [**\_DRMHEADER DRM \_ SubscriptionContentID**](drm-drmheader-subscriptioncontentid.md) | g \_ wszWMDRM \_ DRMHeader \_ SubscriptionContentID | **\_chaîne de type WMT \_**                                |
| [**\_DRMHEADER DRM**](drm-drmheader.md)                                              | g \_ wszWMDRM \_ DRMHeader                        | **\_chaîne de type WMT \_**                                |
| [**\_INDIVIDUALIZEDVERSION DRM**](drm-individualizedversion.md)                      | g \_ wszWMDRM \_ IndividualizedVersion            | **\_chaîne de type WMT \_**                                |
| [**\_KEYID DRM**](drm-keyid.md)                                                      | g \_ wszWMDRM \_ KeyId                            | **\_chaîne de type WMT \_**                                |
| [**\_LASIGNATURECERT DRM**](drm-lasignaturecert.md)                                  | g \_ wszWMDRM \_ LASignatureCert                  | **\_chaîne de type WMT \_**                                |
| [**\_LASIGNATURELICSRVCERT DRM**](drm-lasignaturelicsrvcert.md)                      | g \_ wszWMDRM \_ LASignatureLicSrvCert            | **\_chaîne de type WMT \_**                                |
| [**\_LASIGNATUREPRIVKEY DRM**](drm-lasignatureprivkey.md)                            | g \_ wszWMDRM \_ LASignaturePrivKey               | **\_chaîne de type WMT \_**                                |
| [**\_LASIGNATUREROOTCERT DRM**](drm-lasignaturerootcert.md)                          | g \_ wszWMDRM \_ LASignatureRootCert              | **\_chaîne de type WMT \_**                                |
| [**\_LICENSEACQURL DRM**](drm-licenseacqurl.md)                                      | g \_ wszWMDRM \_ LicenseAcqURL                    | **\_chaîne de type WMT \_**                                |
| [**\_LICENSEID DRM**](drm-licenseid.md)                                              | g \_ wszWMDRM \_ LicenseID                        | **\_chaîne de type WMT \_**                                |
| [**\_SOURCEID DRM**](drm-sourceid.md)                                                | \_wszWMDRM \_ SourceId                         | **\_valeur DWORD de type WMT \_**                                 |
| [**\_V1LICENSEACQURL DRM**](drm-v1licenseacqurl.md)                                  | g \_ wszWMDRM \_ V1LicenseAcqURL                  | **\_chaîne de type WMT \_**                                |
| [**Duration**](duration.md)                                                         | \_wszWMDuration g                              | **\_type WMT \_ QWord**                                 |
| [**FileSize**](filesize.md)                                                         | \_wszWMFileSize g                              | **\_type WMT \_ QWord**                                 |
| [**HasArbitraryDataStream**](hasarbitrarydatastream.md)                             | \_wszWMHasArbitraryDataStream g                | **\_type WMT \_ bool**                                  |
| [**HasAttachedImages**](hasattachedimages.md)                                       | \_wszWMHasAttachedImages g                     | **\_type WMT \_ bool**                                  |
| [**HasAudio**](hasaudio.md)                                                         | \_wszWMHasAudio g                              | **\_type WMT \_ bool**                                  |
| [**HasFileTransferStream**](hasfiletransferstream.md)                               | \_wszWMHasFileTransferStream g                 | **\_type WMT \_ bool**                                  |
| [**HasImage**](hasimage.md)                                                         | \_wszWMHasImage g                              | **\_type WMT \_ bool**                                  |
| [**HasScript**](hasscript.md)                                                       | \_wszWMHasScript g                             | **\_type WMT \_ bool**                                  |
| [**HasVideo**](hasvideo.md)                                                         | \_wszWMHasVideo g                              | **\_type WMT \_ bool**                                  |
| [**Est \_ protégé**](is-protected.md)                                                | \_wszWMProtected g                             | **\_type WMT \_ bool**                                  |
| [**Est \_ approuvé**](is-trusted.md)                                                    | \_wszWMTrusted g                               | **\_type WMT \_ bool**                                  |
| [**ISAN**](isan.md)                                                                 | \_wszISAN g                                    | **\_chaîne de type WMT \_**                                |
| [**IsVBR**](isvbr.md)                                                               | \_wszWMIsVBR g                                 | **\_type WMT \_ bool**                                  |
| [**\_Adresse NSC**](nsc-address.md)                                                  | \_wszWMNSCAddress g                            | **\_chaîne de type WMT \_**                                |
| [**Description de NSC \_**](nsc-description.md)                                          | \_wszWMNSCDescription g                        | **\_chaîne de type WMT \_**                                |
| [**\_E-mail NSC**](nsc-email.md)                                                      | \_wszWMNSCEmail g                              | **\_chaîne de type WMT \_**                                |
| [**\_Nom NSC**](nsc-name.md)                                                        | \_wszWMNSCName g                               | **\_chaîne de type WMT \_**                                |
| [**\_Téléphone NSC**](nsc-phone.md)                                                      | \_wszWMNSCPhone g                              | **\_chaîne de type WMT \_**                                |
| [**NumberOfFrames**](numberofframes.md)                                             | \_wszWMNumberOfFrames g                        | **\_type WMT \_ QWord**                                 |
| [**OptimalBitrate**](optimalbitrate.md)                                             | \_wszWMOptimalBitrate g                        | **\_valeur DWORD de type WMT \_**                                 |
| [**PeakValue**](peakvalue.md)                                                       | \_wszPeakValue g                               | **\_valeur DWORD de type WMT \_**                                 |
| [**Rating**](rating.md)                                                             | \_wszWMRating g                                | **\_chaîne de type WMT \_**                                |
| [**Identifiable**](seekable.md)                                                         | \_wszWMSeekable g                              | **\_type WMT \_ bool**                                  |
| [**Nom de la signature \_**](signature-name.md)                                            | \_nom wszWMSignature \_ g                       | **\_chaîne de type WMT \_**                                |
| [**Stridable**](stridable.md)                                                       | \_wszWMStridable g                             | **\_type WMT \_ bool**                                  |
| [**Intitulé**](title.md)                                                               | \_wszWMTitle g                                 | **\_chaîne de type WMT \_**                                |
| [**VBRPeak**](vbrpeak.md)                                                           | \_wszVBRPeak g                                 | **\_valeur DWORD de type WMT \_**                                 |
| [**WM/AlbumArtist**](wm-albumartist.md)                                             | \_wszWMAlbumArtist g                           | **\_chaîne de type WMT \_**                                |
| [**WM/AlbumCoverURL**](wm-albumcoverurl.md)                                         | \_wszWMAlbumCoverURL g                         | **\_chaîne de type WMT \_**                                |
| [**WM/AlbumTitle**](wm-albumtitle.md)                                               | \_wszWMAlbumTitle g                            | **\_chaîne de type WMT \_**                                |
| [**WM/ASFPacketCount**](wm-asfpacketcount.md)                                       | \_wszWMASFPacketCount g                        | **\_type WMT \_ QWord**                                 |
| [**WM/ASFSecurityObjectsSize**](wm-asfsecurityobjectssize.md)                       | \_wszWMASFSecurityObjectsSize g                | **\_type WMT \_ QWord**                                 |
| [**WM/AudioFileURL**](wm-audiofileurl.md)                                           | \_wszWMAudioFileURL g                          | **\_chaîne de type WMT \_**                                |
| [**WM/AudioSourceURL**](wm-audiosourceurl.md)                                       | \_wszWMAudioSourceURL g                        | **\_chaîne de type WMT \_**                                |
| [**WM/AuthorURL**](wm-authorurl.md)                                                 | \_wszWMAuthorURL g                             | **\_chaîne de type WMT \_**                                |
| [**WM/BeatsPerMinute**](wm-beatsperminute.md)                                       | \_wszWMBeatsPerMinute g                        | **\_chaîne de type WMT \_**                                |
| [**WM/Category**](wm-category.md)                                                   | \_wszWMCategory g                              | **\_chaîne de type WMT \_**                                |
| [**WM/codec**](wm-codec.md)                                                         | \_wszWMCodec g                                 | **\_chaîne de type WMT \_**                                |
| [**WM/composer**](wm-composer.md)                                                   | \_wszWMComposer g                              | **\_chaîne de type WMT \_**                                |
| [**WM/conducteur**](wm-conductor.md)                                                 | \_wszWMConductor g                             | **\_chaîne de type WMT \_**                                |
| [**WM/ContainerFormat**](wm-containerformat.md)                                     | \_wszWMContainerFormat g                       | **WMT \_ \_format de stockage** (type de stockage **WMT \_ \_ binaire**)     |
| [**WM/ContentDistributor**](wm-contentdistributor.md)                               | \_wszWMContentDistributor g                    | **\_chaîne de type WMT \_**                                |
| [**WM/ContentGroupDescription**](wm-contentgroupdescription.md)                     | \_wszWMContentGroupDescription g               | **\_chaîne de type WMT \_**                                |
| [**WM/Director**](wm-director.md)                                                   | \_wszWMDirector g                              | **\_chaîne de type WMT \_**                                |
| [**WM/DRM**](wm-drm.md)                                                             | \_wszWMDRM g                                   | **\_chaîne de type WMT \_**                                |
| [**WM/DVDID**](wm-dvdid.md)                                                         | \_wszWMDVDID g                                 | **\_chaîne de type WMT \_**                                |
| [**WM/EncodedBy**](wm-encodedby.md)                                                 | \_wszWMEncodedBy g                             | **\_chaîne de type WMT \_**                                |
| [**WM/EncodingSettings**](wm-encodingsettings.md)                                   | \_wszWMEncodingSettings g                      | **\_chaîne de type WMT \_**                                |
| [**WM/EncodingTime**](wm-encodingtime.md)                                           | \_wszWMEncodingTime g                          | **fileTime** (**\_ type WMT \_ QWord**)                  |
| [**WM/genre**](wm-genre.md)                                                         | \_wszWMGenre g                                 | **\_chaîne de type WMT \_**                                |
| [**WM/GenreID**](wm-genreid.md)                                                     | \_wszWMGenreID g                               | **\_chaîne de type WMT \_**                                |
| [**WM/InitialKey**](wm-initialkey.md)                                               | \_wszWMInitialKey g                            | **\_chaîne de type WMT \_**                                |
| [**WM/ISRC**](wm-isrc.md)                                                           | \_wszWMISRC g                                  | **\_chaîne de type WMT \_**                                |
| [**WM/langage**](wm-language.md)                                                   | \_wszWMLanguage g                              | **\_chaîne de type WMT \_**                                |
| [**WM/paroles**](wm-lyrics.md)                                                       | \_wszWMLyrics g                                | **\_chaîne de type WMT \_**                                |
| [**Synchronisation des WM et des paroles \_**](wm-lyrics-synchronised.md)                            | c \_ wszWMLyrics \_ synchronisé                  | **WM \_ \_paroles synchronisées** (**\_ type WMT \_ binaire**) |
| [**WM/MCDI**](wm-mcdi.md)                                                           | \_wszWMMCDI g                                  | **\_binaire de type WMT \_**                                |
| [**WM/MediaClassPrimaryID**](wm-mediaprimaryid.md)                                  | \_wszWMMediaClassPrimaryID g                   | **\_GUID du type WMT \_**                                  |
| [**WM/MediaClassSecondaryID**](wm-mediasecondaryid.md)                              | \_wszWMMediaClassSecondaryID g                 | **\_GUID du type WMT \_**                                  |
| [**WM/MediaCredits**](wm-mediacredits.md)                                           | \_wszWMMediaCredits g                          | **\_chaîne de type WMT \_**                                |
| [**WM/MediaIsDelay**](wm-mediaisdelay.md)                                           | \_wszWMMediaIsDelay g                          | **\_type WMT \_ bool**                                  |
| [**WM/MediaIsFinale**](wm-mediaisfinale.md)                                         | \_wszWMMediaIsFinale g                         | **\_type WMT \_ bool**                                  |
| [**WM/MediaIsLive**](wm-mediaislive.md)                                             | \_wszWMMediaIsLive g                           | **\_type WMT \_ bool**                                  |
| [**WM/MediaIsPremiere**](wm-mediaispremiere.md)                                     | \_wszWMMediaIsPremiere g                       | **\_type WMT \_ bool**                                  |
| [**WM/MediaIsRepeat**](wm-mediaisrepeat.md)                                         | \_wszWMMediaIsRepeat g                         | **\_type WMT \_ bool**                                  |
| [**WM/MediaIsSAP**](wm-mediaissap.md)                                               | \_wszWMMediaIsSAP g                            | **\_type WMT \_ bool**                                  |
| [**WM/MediaIsStereo**](wm-mediaisstereo.md)                                         | \_wszWMMediaIsStereo g                         | **\_type WMT \_ bool**                                  |
| [**WM/MediaIsSubtitled**](wm-mediaissubtitled.md)                                   | \_wszWMMediaIsSubtitled g                      | **\_type WMT \_ bool**                                  |
| [**WM/MediaIsTape**](wm-mediaistape.md)                                             | \_wszWMMediaIsTape g                           | **\_type WMT \_ bool**                                  |
| [**WM/MediaNetworkAffiliation**](wm-medianetworkaffiliation.md)                     | \_wszWMMediaNetworkAffiliation g               | **\_chaîne de type WMT \_**                                |
| [**WM/MediaOriginalBroadcastDateTime**](wm-mediaoriginalbroadcastdatetime.md)       | \_wszWMMediaOriginalBroadcastDateTime g        | **\_chaîne de type WMT \_**                                |
| [**WM/MediaOriginalChannel**](wm-mediaoriginalchannel.md)                           | \_wszWMMediaOriginalChannel g                  | **\_chaîne de type WMT \_**                                |
| [**WM/MediaStationCallSign**](wm-mediastationcallsign.md)                           | \_wszWMMediaStationCallSign g                  | **\_chaîne de type WMT \_**                                |
| [**WM/MediaStationName**](wm-mediastationname.md)                                   | \_wszWMMediaStationName g                      | **\_chaîne de type WMT \_**                                |
| [**WM/ModifiedBy**](wm-modifiedby.md)                                               | \_wszWMModifiedBy g                            | **\_chaîne de type WMT \_**                                |
| [**WM/humeur**](wm-mood.md)                                                           | \_wszWMMood g                                  | **\_chaîne de type WMT \_**                                |
| [**WM/OriginalAlbumTitle**](wm-originalalbumtitle.md)                               | \_wszWMOriginalAlbumTitle g                    | **\_chaîne de type WMT \_**                                |
| [**WM/OriginalArtist**](wm-originalartist.md)                                       | \_wszWMOriginalArtist g                        | **\_chaîne de type WMT \_**                                |
| [**WM/OriginalFilename**](wm-originalfilename.md)                                   | \_wszWMOriginalFilename g                      | **\_chaîne de type WMT \_**                                |
| [**WM/OriginalLyricist**](wm-originallyricist.md)                                   | \_wszWMOriginalLyricist g                      | **\_chaîne de type WMT \_**                                |
| [**WM/OriginalReleaseTime**](wm-originalreleasetime.md)                             | \_wszWMOriginalReleaseTime g                   | **\_chaîne de type WMT \_**                                |
| [**WM/OriginalReleaseYear**](wm-originalreleaseyear.md)                             | \_wszWMOriginalReleaseYear g                   | **\_chaîne de type WMT \_**                                |
| [**WM/ParentalRating**](wm-parentalrating.md)                                       | \_wszWMParentalRating g                        | **\_chaîne de type WMT \_**                                |
| [**WM/ParentalRatingReason**](wm-parentalratingreason.md)                           | \_wszWMParentalRatingReason g                  | **\_chaîne de type WMT \_**                                |
| [**WM/PartOfSet**](wm-partofset.md)                                                 | \_wszWMPartOfSet g                             | **\_chaîne de type WMT \_**                                |
| [**WM/PeakBitrate**](wm-peakbitrate.md)                                             | \_wszWMPeakBitrate g                           | **\_valeur DWORD de type WMT \_**                                 |
| [**WM/period**](wm-period.md)                                                       | \_wszWMPeriod g                                | **\_chaîne de type WMT \_**                                |
| [**WM/image**](/windows/desktop/wmformat/wmpicture)                                      | \_wszWMPicture g                               | **WM \_ IMAGE** (**\_ type de type WMT \_ binaire**)              |
| [**WM/PlaylistDelay**](wm-playlistdelay.md)                                         | \_wszWMPlaylistDelay g                         | **\_chaîne de type WMT \_**                                |
| [**WM/Producer**](wm-producer.md)                                                   | \_wszWMProducer g                              | **\_chaîne de type WMT \_**                                |
| [**WM/PromotionURL**](wm-promotionurl.md)                                           | \_wszWMPromotionURL g                          | **\_chaîne de type WMT \_**                                |
| [**WM/ProtectionType**](wm-protectiontype.md)                                       | \_wszWMProtectionType g                        | **\_chaîne de type WMT \_**                                |
| [**WM/Provider**](wm-provider.md)                                                   | \_wszWMProvider g                              | **\_chaîne de type WMT \_**                                |
| [**WM/ProviderCopyright**](wm-providercopyright.md)                                 | \_wszWMProviderCopyright g                     | **\_chaîne de type WMT \_**                                |
| [**WM/ProviderRating**](wm-providerrating.md)                                       | \_wszWMProviderRating g                        | **\_chaîne de type WMT \_**                                |
| [**WM/ProviderStyle**](wm-providerstyle.md)                                         | \_wszWMProviderStyle g                         | **\_chaîne de type WMT \_**                                |
| [**WM/serveur de publication**](wm-publisher.md)                                                 | \_wszWMPublisher g                             | **\_chaîne de type WMT \_**                                |
| [**WM/RadioStationName**](wm-radiostationname.md)                                   | \_wszWMRadioStationName g                      | **\_chaîne de type WMT \_**                                |
| [**WM/RadioStationOwner**](wm-radiostationowner.md)                                 | \_wszWMRadioStationOwner g                     | **\_chaîne de type WMT \_**                                |
| [**WM/SharedUserRating**](wm-shareduserrating.md)                                   | \_wszWMSharedUserRating g                      | **\_valeur DWORD de type WMT \_**                                 |
| [**WM/StreamTypeInfo**](wm-streamtypeinfo.md)                                       | \_wszWMStreamTypeInfo g                        | **WM \_ \_ \_ informations sur le type de flux** (**\_ type WMT \_ binaire**)   |
| [**WM/SubscriptionContentID**](wm-subscriptioncontentid.md)                         | \_wszWMSubscriptionContentID g                 | **\_chaîne de type WMT \_**                                |
| [**WM/sous-titre**](wm-subtitle.md)                                                   | \_wszWMSubTitle g                              | **\_chaîne de type WMT \_**                                |
| [**WM/SubTitleDescription**](wm-subtitledescription.md)                             | \_wszWMSubTitleDescription g                   | **\_chaîne de type WMT \_**                                |
| [**WM/texte**](wm-text.md)                                                           | \_wszWMText g                                  | **WM \_ \_texte** de l’utilisateur (**type de \_ type WMT \_ binaire**)           |
| [**WM/ToolName**](wm-toolname.md)                                                   | \_wszWMToolName g                              | **\_chaîne de type WMT \_**                                |
| [**WM/Toolversion la valeur**](wm-toolversion.md)                                             | \_wszWMToolVersion g                           | **\_chaîne de type WMT \_**                                |
| [**WM/Track**](wm-track.md)                                                         | \_wszWMTrack g                                 | **\_chaîne de type WMT \_**                                |
| [**WM/TrackNumber**](wm-tracknumber.md)                                             | \_wszWMTrackNumber g                           | **\_chaîne de type WMT \_**                                |
| [**WM/UniqueFileIdentifier**](wm-uniquefileidentifier.md)                           | \_wszWMUniqueFileIdentifier g                  | **\_chaîne de type WMT \_**                                |
| [**WM/UserWebURL**](wm-userweburl.md)                                               | \_wszWMUserWebURL g                            | **WM \_ \_ \_ URL Web utilisateur** (**\_ type WMT \_ binaire**)       |
| [**WM/VideoClosedCaptioning**](wm-videoclosedcaptioning.md)                         | \_wszWMVideoClosedCaptioning g                 | **\_type WMT \_ bool**                                  |
| [**WM/VideoFrameRate**](wm-videoframerate.md)                                       | \_wszWMVideoFrameRate g                        | **\_valeur DWORD de type WMT \_**                                 |
| [**WM/VideoHeight**](wm-videoheight.md)                                             | \_wszWMVideoHeight g                           | **\_valeur DWORD de type WMT \_**                                 |
| [**WM/VideoWidth**](wm-videowidth.md)                                               | \_wszWMVideoWidth g                            | **\_valeur DWORD de type WMT \_**                                 |
| [**WM/WMADRCAverageReference**](wm-wmadrcaveragereference.md)                       | \_wszWMWMADRCAverageReference g                | **\_valeur DWORD de type WMT \_**                                 |
| [**WM/WMADRCAverageTarget**](wm-wmadrcaveragetarget.md)                             | \_wszWMWMADRCAverageTarget g                   | **\_valeur DWORD de type WMT \_**                                 |
| [**WM/WMADRCPeakReference**](wm-wmadrcpeakreference.md)                             | \_wszWMWMADRCPeakReference g                   | **\_valeur DWORD de type WMT \_**                                 |
| [**WM/WMADRCPeakTarget**](wm-wmadrcpeaktarget.md)                                   | \_wszWMWMADRCPeakTarget g                      | **\_valeur DWORD de type WMT \_**                                 |
| [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md)                             | \_wszWMWMCollectionGroupID g                   | **\_GUID du type WMT \_**                                  |
| [**WM/WMCollectionID**](wm-wmcollectionid.md)                                       | \_wszWMWMCollectionID g                        | **\_GUID du type WMT \_**                                  |
| [**WM/WMContentID**](wm-wmcontentid.md)                                             | \_wszWMWMContentID g                           | **\_GUID du type WMT \_**                                  |
| [**WM/WMShadowFileSourceDRMType**](wm-wmshadowfilesourcedrmtype.md)                 | \_wszWMWMShadowFileSourceDRMType g             | **\_chaîne de type WMT \_**                                |
| [**WM/WMShadowFileSourceFileType**](wm-wmshadowfilesourcefiletype.md)               | \_wszWMWMShadowFileSourceFileType g            | **\_chaîne de type WMT \_**                                |
| [**WM/Writer**](wm-writer.md)                                                       | \_wszWMWriter g                                | **\_chaîne de type WMT \_**                                |
| [**WM/Year**](wm-year.md)                                                           | \_wszWMYear g                                  | **\_chaîne de type WMT \_**                                |



 

## <a name="remarks"></a>Notes

Les constantes suivantes sont définies avec les attributs. Chacun d’eux indique le nombre d’un type spécifique d’attribut. Vous n’avez pas besoin d’utiliser ces valeurs dans vos applications.



| Constante                 | Valeur |
|--------------------------|-------|
| \_dwWMSpecialAttributes g | 20    |
| \_dwWMContentAttributes g | 5     |
| \_dwWMNSCAttributes g     | 5     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Attributs**](attributes.md)
</dt> </dl>

 

 