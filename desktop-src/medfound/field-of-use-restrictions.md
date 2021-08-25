---
description: Champ des restrictions d’utilisation
ms.assetid: 36f28e4c-2baf-4618-9935-5d4615f6bc77
title: Champ des restrictions d’utilisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ccfb5b7c0923bdea117371a3b6af2669bf903fb3af996f754be43d5665c1ee1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942667"
---
# <a name="field-of-use-restrictions"></a>Champ des restrictions d’utilisation

> [!Note]  
> cette rubrique s’applique à Windows 7 ou version ultérieure.

 

Une restriction de *champ d’utilisation* est une provision qui limite la manière dont une licence pour une technologie particulière peut être utilisée.

Media Foundation fournit un mécanisme permettant d’appliquer des restrictions de champ d’utilisation sur les transformations de Media Foundation (MFTs), en particulier les codecs. Ce mécanisme requiert que la table MFT bloque sa propre utilisation par les applications jusqu’à ce que l’application ait effectué une négociation avec la table MFT. Media Foundation ne définit pas le protocole de transfert, en général, il implique un certain type d’échange de chiffrement.

### <a name="registration-and-enumeration"></a>Inscription et énumération

Si une table MFT a des restrictions de champ d’utilisation, définissez l’indicateur FIELDOFUSE de l' **\_ \_ indicateur \_ d’énumération MFT** lors de l’inscription de la table MFT. Cet indicateur s’applique aux API d’inscription MFT suivantes :

-   [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister)
-   [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)
-   [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid)
-   [**IMFLocalMFTRegistration::RegisterMFTs**](/windows/desktop/api/mfidl/nf-mfidl-imflocalmftregistration-registermfts)

Par défaut, les MFTs inscrits avec cet indicateur sont exclus des résultats de l’énumération. Pour énumérer les MFTs avec des restrictions de champ d’utilisation, appelez [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) et spécifiez l’indicateur de FIELDOFUSE d' **\_ \_ indicateur \_ d’énumération MFT** dans le paramètre *Flags* . Le diagramme suivant illustre ce processus.

![Diagramme montrant MFT et une application envoyant des données au registre](images/mft-fou01.gif)

La fonction [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) exclut toujours les MFTS qui ont des restrictions de champ d’utilisation.

### <a name="unlocking-the-mft"></a>Déverrouillage de la MFT

Pour utiliser une table MFT avec des restrictions de champ d’utilisation, procédez comme suit :

1.  L’application implémente l’interface [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) .
2.  La méthode [**IMFFieldOfUseMFTUnlock :: Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) prend un pointeur vers l’interface **IUnknown** de la table MFT.
3.  Dans la méthode [**Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) , l’application exécute le protocole de transfert requis, en utilisant le mécanisme défini par la table MFT. Cette étape n’est pas définie par l’API Media Foundation.
4.  Si la méthode [**Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) est établie, la table MFT se déverrouille.

L’application spécifie le pointeur [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) en définissant l’attribut de [ \_ \_ déverrouillage de l' \_ attribut MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) . Il existe différentes façons de définir cet attribut, selon la façon dont votre application crée le décodeur ou le pipeline d’encodage :



| API                   | Comment déverrouiller un champ d’utilisation                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lecteur source         | Si votre application utilise le [lecteur source](source-reader.md) pour décoder un fichier multimédia, définissez l’attribut [MFT \_ FIELDOFUSE \_ Unlock \_ attribute](mft-fieldofuse-unlock-attribute.md) dans les paramètres de configuration. Consultez [attributs du lecteur source](source-reader-attributes.md).                                                                                                                                                                                                                                                                         |
| Enregistreur du récepteur           | Si votre application utilise le writer de récepteur pour encoder un fichier multimédia, définissez l’attribut [MFT \_ FIELDOFUSE \_ Unlock \_ attribute](mft-fieldofuse-unlock-attribute.md) dans les paramètres de configuration. Consultez [attributs du writer du récepteur](sink-writer-attributes.md).                                                                                                                                                                                                                                                                                                    |
| Transcodage rapide        | Si votre application utilise la fonctionnalité de transcodage rapide pour créer une topologie d’encodage, définissez l' [ \_ \_ \_ attribut MFT FIELDOFUSE Unlock](mft-fieldofuse-unlock-attribute.md) lorsque vous appelez [**IMFTranscodeProfile :: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes). Pour plus d’informations sur la fonctionnalité de transcodage rapide, consultez [API de transcodage](transcode-api.md).                                                                                                                                                                      |
| Topologie              | Si vous créez une topologie directement, définissez l' [attribut MFT \_ FIELDOFUSE \_ Unlock \_ ](mft-fieldofuse-unlock-attribute.md) en tant qu’attribut sur la topologie. Consultez [attributs de topologie](topology-attributes.md).                                                                                                                                                                                                                                                                                                                                                  |
| Objet d’activation MFT | Si votre application énumère directement les décodeurs ou les encodeurs qu’elle utilisera, définissez l' [ \_ \_ \_ attribut MFT FIELDOFUSE Unlock](mft-fieldofuse-unlock-attribute.md) sur les pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retournés par la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) . <br/> Définissez l’attribut avant d’appeler [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) pour créer la table MFT. L’objet d’activation appelle [**IMFFieldOfUseMFTUnlock :: Unlock**](/windows/desktop/api/mfidl/nf-mfidl-imffieldofusemftunlock-unlock) lorsqu’il crée la table MFT.<br/> |



 

Le diagramme suivant montre la relation entre les objets d’activation MFT et l’interface [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) .

![Diagramme montrant une application, un objet d’activation et une table MFT avec des flèches vers un objet SHA, qui a une flèche de retour à la table MFT](images/mft-fou02.gif)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transformations de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 




