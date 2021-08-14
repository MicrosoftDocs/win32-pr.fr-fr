---
description: Chaque fichier ASF contient un ou plusieurs flux. L’objet profil ASF représente une collection de flux ASF. Pour l’encodage ASF, vous devez créer et configurer les flux que vous souhaitez Encoder.
ms.assetid: cc89e8bc-58ff-48e2-9668-0dcd6cfd25e1
title: Création et configuration d’Flux ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c780de3fa0abb5db29e3e5e5ed049b78aca7898966e8f7e8595b504804da91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743237"
---
# <a name="creating-and-configuring-asf-streams"></a>Création et configuration d’Flux ASF

Chaque fichier ASF contient un ou plusieurs flux. L’objet [Profil ASF](asf-profile.md) représente une collection de flux ASF. Pour l’encodage ASF, vous devez créer et configurer les flux que vous souhaitez Encoder.

Une application peut effectuer les tâches suivantes avec l’objet profil ASF :

-   Ajoutez ou supprimez un flux.
-   Obtenir les paramètres de configuration d’un flux.
-   Configurez les extensions de charge utile.
-   Ajoutez, supprimez ou modifiez un objet d’exclusion mutuelle ASF.

Cette rubrique contient les sections suivantes.

-   [Création d’un nouveau flux](#creating-a-new-stream)
-   [Affectation de numéros de flux](#assigning-stream-numbers)
-   [Définition des valeurs des compartiments fuites](#setting-leaky-bucket-values)
-   [Extensions de charge utile](#payload-extensions)
-   [Ajout d’un flux au profil](#adding-a-stream-to-the-profile)
-   [Rubriques connexes](#related-topics)

## <a name="creating-a-new-stream"></a>Création d’un nouveau flux

Un objet de profil ASF doit contenir des paramètres de configuration pour au moins un flux ASF. Chaque flux est représenté par un objet de *configuration de flux* qui expose l’interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) . Les informations de l’objet de configuration de flux correspondent à l’objet de propriétés de flux et aux objets de propriétés de flux étendus dans l’en-tête de fichier ASF. (Voir [structure de fichiers ASF](asf-file-structure.md).)

Pour ajouter un flux à un profil ASF, procédez comme suit :

1.  Créez un objet de configuration de flux de flux vide.
2.  Configurez le flux en fonction des exigences de l’application.
3.  Ajoutez le flux au profil.

Pour créer un flux pour le profil, appelez [**IMFASFProfile :: CreateStream,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) pour créer un objet de configuration de flux vide et recevoir le pointeur dans le paramètre *ppIStream* . **CreateStream,** doit connaître le type du flux à créer. Les types de flux les plus courants utilisés dans les fichiers ASF sont des flux audio et vidéo. Dans Media Foundation, les types de flux sont dénotés par l’objet de type de média qui expose l’interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) . Le type principal du type de média définit la catégorie du flux multimédia numérique, tel que audio ou vidéo. Le sous-type définit le format du type principal. Le type de média initial défini par **CreateStream,** peut être modifié à l’aide de l’objet de configuration de vapeur. Pour récupérer le type de média pour le flux, appelez [**IMFASFStreamConfig :: GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) ou pour récupérer l’appel de type principal [**IMFASFStreamConfig :: GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype). Le type de média initial d’un flux peut être remplacé par un nouveau type de média configuré en appelant [**IMFASFStreamConfig :: SetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setmediatype).

Si une application crée un profil à partir d’un descripteur de présentation valide en appelant [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor). La fonction définit automatiquement les objets de configuration de flux pour chacun des flux et les définit sur le profil. Les types de médias de diffusion en continu sont définis en fonction des descripteurs de flux associés au descripteur de présentation.

## <a name="assigning-stream-numbers"></a>Affectation de numéros de flux

un numéro de flux doit être assigné à Flux de tous les types. Les numéros de flux n’ont pas besoin d’être séquentiels, mais doivent être dans la plage comprise entre 1 et 127. Pour assigner des numéros de flux, appelez [**IMFASFStreamConfig :: SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber). Pour récupérer le numéro de flux, appelez [**IMFASFStreamConfig :: GetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamnumber).

> [!Note]  
> Un numéro de flux est différent d’un index de flux, que vous utilisez pour obtenir des flux dans un profil à l’aide de [**IMFASFProfile :: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream). L’index de flux est un nombre affecté au flux par l’objet de profil. Les index de flux sont compris entre 0 et un de moins que le nombre de flux récupérés par [**IMFASFProfile :: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount). Vous pouvez également obtenir un flux à partir du profil par numéro de flux en appelant [**IMFASFProfile :: GetStreamByNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber).

 

## <a name="setting-leaky-bucket-values"></a>Définition des valeurs des compartiments fuites

Chaque objet de configuration de flux qui représente un flux doit avoir des paramètres de compartiment fuite associés, une vitesse de transmission et des valeurs de fenêtre de mémoire tampon.

Ces valeurs sont disponibles pour l’application par le biais de l’attribut [**\_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) et de l’attribut [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) . Pour l’encodage de fichier, les valeurs réelles dépendent du type d’encodage et sont choisies par l’encodeur. Si vous disposez déjà d’un encodeur configuré et que le type de sortie est défini sur l’encodeur, l’application doit interroger l’encodeur pour les paramètres de compartiment avec fuite et définir les valeurs de ces attributs.

Si vous utilisez les composants de la couche de pipeline et que vous configurez les flux pour le récepteur de média ASF, vous n’avez probablement pas d’encodeur configuré. Dans ce cas, vous devez interroger les négociations de types postérieurs au support de l’encodeur et définir la valeur mise à jour dans la propriété [**\_ LEAKYBUCKET MFPKEY ASFSTREAMSINK \_ corrigée \_**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) de la Banque de propriétés du récepteur de média ASF. Le magasin de propriétés d’encodage est récupéré via le de l’objet ContentInfo associé au profil. Les valeurs mises à jour sont répercutées automatiquement dans les valeurs d’attribut de compartiment avec fuites du flux. Pour obtenir des informations générales sur les compartiments de fuites et sur l’obtention de la valeur de compartiment perdue à partir de l’encodeur, consultez le [modèle de tampon de compartiment avec fuite](the-leaky-bucket-buffer-model.md).

## <a name="payload-extensions"></a>Extensions de charge utile

Les données multimédias pour les flux sont ajoutées à l’objet de données ASF en tant qu' [exemples de supports](media-samples.md) par le [multiplexeur ASF](asf-multiplexer.md). Ces exemples de supports peuvent contenir des données d’extension de charge utile : les données de code temporel SMPTE, les proportions de pixels non carrés, la durée de l’échantillon et, si l’exemple le contient, une image clé vidéo. Pour obtenir la liste des types d’extension de charge utile pris en charge, consultez [GUID d’extension de charge utile ASF](asf-payload-extension-guids.md).

Un flux doit être configuré pour accepter l’extension de charge utile. ainsi, pendant la génération de l’échantillon, le multiplexeur peut ajouter les données supplémentaires à chaque échantillon pour ce flux.

Pour récupérer le nombre total d’extensions de charge utile définies sur le flux, appelez [**IMFASFStreamConfig :: GetPayloadExtensionCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextensioncount) , puis Énumérez la liste en appelant [**IMFASFStreamConfig :: GetPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getpayloadextension). Pour ajouter l’extension de charge utile pour le flux, appelez [**IMFASFStreamConfig :: AddPayloadExtension**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-addpayloadextension). Cela permet d’ajouter des données supplémentaires aux échantillons de supports individuels générés pour le flux.

Pour supprimer les extensions de charge utile existantes associées au flux, appelez [**IMFASFStreamConfig :: RemoveAllPayloadExtensions**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-removeallpayloadextensions).

## <a name="adding-a-stream-to-the-profile"></a>Ajout d’un flux au profil

Après la configuration d’un flux, appelez [**IMFASFProfile :: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) pour ajouter le flux au profil.

Pour supprimer un flux existant dans le profil, appelez [**IMFASFProfile :: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream).

Le profil configuré doit être défini sur l’objet ContentInfo en appelant [**IMFASFContentInfo :: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile). Si vous apportez des modifications à un flux existant, vous devez l’ajouter à nouveau au profil et définir le profil sur l’objet ContentInfo.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Profil ASF](asf-profile.md)
</dt> <dt>

[Prise en charge ASF dans Media Foundation](asf-support-in-media-foundation.md)
</dt> <dt>

[Composants WMContainer ASF](wmcontainer-asf-components.md)
</dt> </dl>

 

 



