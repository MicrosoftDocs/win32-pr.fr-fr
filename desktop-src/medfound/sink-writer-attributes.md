---
description: Attributs du writer du récepteur
ms.assetid: f27b9beb-f35f-400e-a337-50d9de21e91e
title: Attributs du writer du récepteur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23dbca06c3ff1a4ac80b8e68413fdd0816d71a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525613"
---
# <a name="sink-writer-attributes"></a>Attributs du writer du récepteur

Les attributs suivants peuvent être utilisés pour initialiser le writer du récepteur.



| Attribut                                                                                  | Description                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_latence faible \_ MF](mf-low-latency.md)                                                     | Active le traitement à faible latence.                                                                                                                                                                                                    |
| [\_ \_ convertisseurs de désactivation MF ReadWrite \_](mf-readwrite-disable-converters.md)                  | Active ou désactive les conversions de format par le writer du récepteur.                                                                                                                                                                         |
| [MF \_ ReadWrite \_ activer \_ les \_ transformations matérielles](mf-readwrite-enable-hardware-transforms.md) | Permet au writer de récepteur d’utiliser des transformations de Media Foundation basées sur le matériel (MFTs).                                                                                                                                                  |
| [\_ \_ rappel asynchrone du writer de récepteur MF \_ \_](mf-sink-writer-async-callback.md)                     | Contient un pointeur vers l’interface de rappel de l’application pour le writer du récepteur.                                                                                                                                                    |
| [\_limitation de \_ \_ désactivation de l’enregistreur de récepteur MF \_](mf-sink-writer-disable-throttling.md)             | Spécifie si l’enregistreur du récepteur limite le taux des données entrantes.                                                                                                                                                                |
| [\_CONTAINERTYPE de transcodage MF \_](mf-transcode-containertype.md)                             | Spécifie le type de conteneur du fichier de sortie.                                                                                                                                                                                   |
| [\_Attribut de \_ déverrouillage MFT FIELDOFUSE \_](mft-fieldofuse-unlock-attribute.md)                  | Contient un pointeur [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , utilisé pour déverrouiller une table MFT avec des restrictions de champ d’utilisation. Pour plus d’informations, consultez [restrictions relatives au champ d’utilisation](field-of-use-restrictions.md). |
| [\_ \_ \_ Gestionnaire D3D de l’enregistreur du récepteur MF \_](mf-sink-writer-d3d-manager.md)                           | Utilisez cet attribut pour fournir un appareil Direct3D pour tous les encodeurs vidéo ou récepteurs multimédias chargés par le writer du récepteur.                                                                                                                   |



 

Utilisez ces attributs avec les méthodes et fonctions suivantes :

-   [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**IMFReadWriteClassFactory::CreateInstanceFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

Pour utiliser l’un de ces attributs, appelez d’abord [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) pour créer un nouveau magasin d’attributs. Utilisez ensuite l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pour définir les attributs souhaités sur le magasin d’attributs. Transmettez le pointeur **IMFAttributes** au paramètre *pAttributes* de l’une des méthodes ou fonctions indiquées précédemment.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IMFSinkWriter**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



