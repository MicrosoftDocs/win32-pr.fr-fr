---
description: En savoir plus sur la définition des propriétés dans le récepteur de fichiers ASF, qu’une application peut utiliser pour archiver des données de média ASF dans un fichier.
ms.assetid: a47caabd-23e3-4d22-b4b6-5fdb79d62ca1
title: Définition des propriétés dans le récepteur de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b6b000ed04c7858251f7388d3edc6a40e0b213
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525633"
---
# <a name="setting-properties-in-the-file-sink"></a>Définition des propriétés dans le récepteur de fichiers

Le récepteur de fichiers ASF est une implémentation de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fournie par Media Foundation qu’une application peut utiliser pour archiver des données de média ASF dans un fichier. Pour plus d’informations sur le modèle objet et l’utilisation générale des récepteurs de média ASF, consultez [récepteurs de média ASF](asf-media-sinks.md).

Une fois [le récepteur de fichiers ASF créé](creating-the-asf-file-sink.md), il doit être configuré avec des informations sur les flux dans le fichier de sortie. Cette procédure est décrite dans [Ajout d’informations de flux au récepteur de fichiers ASF](adding-stream-information-to-the-asf-file-sink.md). Vous pouvez définir des propriétés supplémentaires sur le récepteur de fichiers en fonction du type d’encodage. compartiments avec fuites ; Propriétés générales du fichier. Ces paramètres ne sont pas écrits dans l’objet d’en-tête ASF final. Cette rubrique décrit le processus d’ajout de ces propriétés dans la Banque de propriétés du récepteur de fichiers.

L’objet ContentInfo gère les propriétés de fichier globales et les propriétés de flux individuelles pour le récepteur de fichiers. Pour plus d’informations sur l’obtention d’une référence à l’objet ASF ContentInfo du récepteur de fichiers, consultez [création du récepteur de fichiers ASF](creating-the-asf-file-sink.md).

Pour obtenir une référence à la Banque de propriétés du récepteur de fichiers ([**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)), appelez [**IMFASFContentInfo :: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) sur la référence de l’objet ContentInfo du récepteur de fichiers.

## <a name="stream-encoding-properties"></a>Propriétés d’encodage de flux

Pour encoder le contenu correctement, le fichier doit connaître certaines informations de codage, telles que le type d’encodage et les paramètres d’encodage associés. Ces valeurs sont définies sur le récepteur de fichiers en tant que valeurs de propriété dans une banque de propriétés gérée par l’objet ASF ContentInfo. si vous configurez le récepteur de fichiers avant d’instancier les encodeurs appropriés, vous pouvez utiliser l’objet ContentInfo avec toutes les propriétés remplies pour créer les encodeurs Windows Media. Dans ce cas, les propriétés sont définies automatiquement sur les encodeurs instanciés. À l’inverse, si vous créez les encodeurs avant le récepteur, assurez-vous que les propriétés que vous définissez sur les encodeurs sont copiées dans la Banque de propriétés du récepteur de fichiers.

Pour définir les propriétés d’encodage, vous devez avoir accès à la Banque de propriétés au niveau du flux du récepteur de fichiers. Transmettez le numéro du flux dans le paramètre *wStreamNumber* de la méthode [**IMFASFContentInfo :: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) . Les numéros de flux doivent correspondre aux valeurs définies lors de la configuration de chaque flux dans le profil. Les valeurs de propriété sont définies en appelant [**IPropertyStore :: SetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore). Le tableau suivant décrit les propriétés prises en charge.

Les propriétés dépendent du type d’encodage. Pour plus d’informations sur les propriétés et les valeurs respectives que vous devez définir, consultez [propriétés d’encodage](configuring-the-encoder.md).

## <a name="leaky-bucket-property"></a>Propriété de compartiment avec fuite

Les paramètres de compartiment avec fuite déterminent la fenêtre de mémoire tampon réelle utilisée par l’encodeur pour le flux. La propriété [**\_ LEAKYBUCKET MFPKEY ASFSTREAMSINK \_ corrigée \_**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) du récepteur de fichiers contient les paramètres de compartiment avec fuite, la vitesse de transmission, la fenêtre de mémoire tampon et la saturation de la mémoire tampon initiale. Cette propriété est définie dans la Banque de propriétés de propriété au niveau du flux du récepteur de fichiers et doit être définie après la création et la configuration des encodeurs. Cette valeur est définie dans le. Pendant la négociation de type de média, l’encodeur décide la fenêtre de mémoire tampon et la vitesse de transmission à utiliser. Vous pouvez récupérer ces valeurs à l’aide de l’interface **IWMCodecLeakyBucket** , qui est définie dans wmcodecifaces. h et vous devez créer un lien vers wmcodecdspuuid. lib pour appeler ses méthodes.

Les valeurs récupérées peuvent être définies pour cette propriété pour chaque flux du récepteur de fichiers ASF.

## <a name="global-file-sink-properties"></a>Propriétés globales du récepteur de fichiers

Pour récupérer la Banque de propriétés globale du récepteur de fichiers, transmettez 0 dans le paramètre *wStreamNumber* de la méthode [**IMFASFContentInfo :: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) . Les valeurs de propriété sont définies en appelant [**IPropertyStore :: SetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore). Le tableau suivant décrit les propriétés prises en charge.

| Propriétés au niveau du fichier                                                                                | Description                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFPKEY \_ ASFMEDIASINK \_ base \_ SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md)           | L’heure d’envoi indique quand la charge utile dans le compartiment avec fuite est libérée. Cette valeur de propriété indique la première heure d’envoi. Le multiplexeur utilise cette valeur pour calculer les temps d’envoi suivants pour les paquets générés et s’assure que les flux de données transitent régulièrement via le compartiment avec fuite. |
| [**MFPKEY \_ ASFMEDIASINK \_ ajuster la \_ vitesse de transmission**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) | Cette valeur BOOL indique si le multiplexeur doit ajuster la vitesse de transmission automatiquement pour s’assurer que les données ne dépassent pas le compartiment avec fuite.                                                                                                                                                  |
| [**MFPKEY \_ ASFMEDIASINK \_ DRMACTION**](mfpkey-asfmediasink-drmaction-property.md)                    | Cela indique l’action DRM de récepteur multimédia ASF pour la génération de fichier. Dans cette version, seul le transcodage DRM est pris en charge.                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Récepteurs de média ASF](asf-media-sinks.md)
</dt> <dt>

[Composants ASF de couche de pipeline](pipeline-layer-asf-components.md)
</dt> <dt>

[Prise en charge ASF dans Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 
