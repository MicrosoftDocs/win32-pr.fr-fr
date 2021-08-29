---
description: Lors de la création d’un fichier ASF, l’objet ContentInfo doit connaître les caractéristiques du contenu multimédia afin que les différents objets d’en-tête soient renseignés avec les valeurs correctes.
ms.assetid: 30e3c10b-1310-4194-8b83-221dfe73b03c
title: Définition des propriétés dans l’objet ContentInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c17d82a05540512be34ba0d327ce006aa6215774da86a14ebfcf4339c85ab361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101799"
---
# <a name="setting-properties-in-the-contentinfo-object"></a>Définition des propriétés dans l’objet ContentInfo

Lors de la création d’un fichier ASF, l’objet ContentInfo doit connaître les caractéristiques du contenu multimédia afin que les différents objets d’en-tête soient renseignés avec les valeurs correctes.

-   [Paramètres relative au contenu dans l’objet ContentInfo](#content-related-settings-in-the-contentinfo-object)
-   [configuration de l’objet ContentInfo avec l’encodeur Paramètres](#configuring-the-contentinfo-object-with-encoder-settings)
-   [Rubriques connexes](#related-topics)

## <a name="content-related-settings-in-the-contentinfo-object"></a>Paramètres relative au contenu dans l’objet ContentInfo

Les paramètres de configuration du contenu sont des paramètres de flux, qui sont contenus dans le profil et spécifient l’identificateur de flux, le type de média et les paramètres de compartiment avec fuite pour le récepteur multimédia. Une fois le profil défini sur l’objet ContentInfo en appelant [**IMFASFContentInfo :: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile), ces valeurs sont reflétées dans l’objet d’en-tête ASF qui a été généré. Pour plus d’informations sur ces paramètres, consultez [création et configuration d’flux ASF](creating-and-configuring-asf-streams.md).

## <a name="configuring-the-contentinfo-object-with-encoder-settings"></a>configuration de l’objet ContentInfo avec l’encodeur Paramètres

Les données audio ou vidéo multimédia numériques sont complexes et occupent de grandes quantités de mémoire. Dans la plupart des cas, l’audio et la vidéo sont compressés à l’aide d’encodeurs avant d’être ajoutés à un fichier ASF. Dans Media Foundation, les encodeurs sont implémentés en tant que [Media Foundation transformations](media-foundation-transforms.md) (MFTS) avec une entrée et une sortie. Vous devez sélectionner le type de média de sortie en fonction du type de média du flux d’entrée et du type d’encodage que vous choisissez pour compresser le flux.

Avant la session d’encodage, l’encodeur doit être configuré en définissant les propriétés appropriées en fonction du type d’encodage.

Après la configuration de l’encodeur, vous devez configurer l’objet ContentInfo avec les valeurs de l’encodeur, car le [multiplexeur ASF](asf-multiplexer.md) et le récepteur multimédia ASF, qui sont initialisés avec l’objet ContentInfo rempli, utilisent des paramètres tels que les valeurs de compartiments avec fuites pour générer des paquets de données ASF. Les valeurs ne sont pas enregistrées dans l’objet d’en-tête ASF final. Les paramètres d’encodage sont exposés en tant que propriétés. Pour configurer l’objet ContentInfo avec les propriétés de l’encodeur, procédez comme suit :

1.  Obtenir un pointeur vers la Banque de propriétés de l’encodeur en interrogeant directement l’encodeur (interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ) pour l’interface **IPropertyStore** .
2.  Appelez [**IMFASFContentInfo :: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore). Pour définir des propriétés spécifiques au flux, spécifiez l’identificateur de flux dans le paramètre *wStreamNumber* ; pour les propriétés au niveau du fichier, passer 0. Le paramètre *ppIStore* reçoit un pointeur vers l’interface **IPropertyStore** . La Banque de propriétés reçue est vide.
3.  Appelez **IPropertyStore :: GetValue** sur l’encodeur et récupérez la valeur de la propriété en spécifiant les constantes de clé de propriété. Pour obtenir la liste complète des propriétés d’encodage, consultez la [référence de programmation de codec](/previous-versions//aa384554(v=vs.85)).
4.  Appelez **IPropertyStore :: SetValue** sur l’objet ContentInfo pour définir la propriété Required dans la Banque de propriétés.
5.  Répétez les étapes 3 et 4 pour chaque propriété que vous souhaitez définir.

Le récepteur de média ASF peut être créé à l’aide d’un objet d’activation en appelant [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate). Le nouvel objet récepteur multimédia est configuré en fonction des paramètres spécifiques au récepteur multimédia qui peuvent être définis dans la Banque de propriétés de l’objet ContentInfo. Le tableau suivant répertorie les constantes de propriété de récepteur de média ASF.



| Propriété                                                                                                     | Description                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFPKEY \_ ASFMEDIASINK \_ base \_ SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md)                   | L’heure d’envoi indique quand la charge utile dans le compartiment avec fuite est libérée. Cette valeur de propriété indique la première heure d’envoi. Le multiplexeur utilise cette valeur pour calculer les temps d’envoi suivants pour les paquets générés et s’assure que les flux de données transitent régulièrement via le compartiment avec fuite. |
| [**MFPKEY \_ ASFMEDIASINK \_ ajuster la \_ vitesse de transmission**](mfpkey-asfmediasink-autoadjust-bitrate-property.md)         | Cette valeur **bool** indique si le multiplexeur doit ajuster la vitesse de transmission automatiquement pour s’assurer que les données ne dépassent pas le compartiment avec fuite.                                                                                                                                              |
| [**MFPKEY \_ ASFMEDIASINK \_ DRMACTION**](mfpkey-asfmediasink-drmaction-property.md)                            | Cela indique l’action DRM de récepteur multimédia ASF pour la génération de fichier. Dans cette version, seul le transcodage DRM est pris en charge.                                                                                                                                                                                   |
| [**MFPKEY \_ ASFSTREAMSINK \_ corrigé \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) | Cette propriété doit être définie lorsque l’encodeur détermine la fenêtre de mémoire tampon et la vitesse de transmission à utiliser. Pour définir ces valeurs, utilisez l’interface [**IWMCodecLeakyBucket**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcodecleakybucket) . Cette valeur doit être définie pour chaque flux du fichier ASF.                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture d’un objet d’en-tête ASF pour un nouveau fichier](writing-an-asf-header-object-for-a-new-file.md)
</dt> </dl>

 

 
