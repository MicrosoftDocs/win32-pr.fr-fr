---
title: Extensions d’appareil pour la création de rapports sur le contenu acquis
description: Extensions d’appareil pour la création de rapports sur le contenu acquis
ms.assetid: 597d872e-9105-4edb-afa3-9f4407de0f73
keywords:
- Lecteur Windows Media, extensions de périphérique
- Lecteur Windows Media, extensions
- Lecteur Windows Media, création de rapports sur le contenu acquis
- extensions d’appareils, création de rapports sur le contenu acquis
- extensions, création de rapports sur le contenu acquis
- création de rapports sur le contenu acquis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3389f5b35cedc853d66e6f450836195497628972ea6ae15642d75155d8b83b6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902059"
---
# <a name="device-extensions-for-reporting-acquired-content"></a>Extensions d’appareil pour la création de rapports sur le contenu acquis

Lecteur Windows Media 11 introduit une nouvelle fonctionnalité qui permet aux appareils portables de notifier le lecteur du contenu ajouté à l’appareil depuis la dernière synchronisation. Lecteur Windows Media 11 peut utiliser ces informations pour copier le contenu nouvellement acquis de l’appareil sur l’ordinateur de l’utilisateur. Les fabricants de périphériques doivent noter les exigences suivantes pour la prise en charge de cette fonctionnalité :

-   Cette fonctionnalité est prise en charge uniquement pour les appareils compatibles MTP.
-   cette fonctionnalité ne fonctionne qu’avec des appareils qui ont un partenariat avec Lecteur Windows Media.
-   Les appareils doivent signaler uniquement le contenu que l’appareil a créé ou téléchargé. Cela comprend les photos prises par l’appareil ; enregistrements vocaux créés par l’appareil ; enregistrements de la messagerie vocale ; téléchargements à partir d’une carte de stockage ; et téléchargements à partir d’Internet. Le contenu qui a été stocké sur le périphérique suite à une synchronisation avec un autre appareil ou un autre partenariat ne doit pas être signalé.

le fichier d’en-tête nommé wmpdevices. h, qui est installé dans le cadre du kit de développement logiciel (SDK) Lecteur Windows Media, définit les structures et les constantes nécessaires à la prise en charge des extensions d’appareils Lecteur Windows Media.

pour qu’un appareil soit reconnu comme prenant en charge la création de rapports de contenu acquis via le jeu d’extensions de périphérique MTP Lecteur Windows Media, il doit inclure les informations suivantes dans le jeu de données DeviceInfo. (Pour plus d’informations sur ce jeu de données, consultez la section 4.6.1 de la spécification MTP.)



| Champ de DataSet          | Ordre des champs | Type de données  | Valeur                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **Chaîne** | « microsoft.com/WMPPD : 11,0 » |



 

Le tableau suivant fournit des détails sur l’opération MTP pour la création de rapports sur le contenu acquis.



| Élément                  | Description                                                                                                                                                                                                                     |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Code d'opération        | 0x9202                                                                                                                                                                                                                          |
| Paramètre d’opération 1 | L’ID de transaction fourni par l’appareil lors de la session précédente. Cette valeur est égale à zéro pour la première session.                                                                                                                |
| Paramètre d’opération 2 | Index de départ. Cette valeur est toujours égale à zéro lors du premier appel d’une session. Lors des appels suivants au sein de la même session de synchronisation, cette valeur augmente en fonction du nombre d’éléments renvoyés par les données de la réponse précédente. |
| Paramètre d’opération 3 | 0x10000. Cette constante, définie dans wmpdevices. h, est le nombre maximal de PUOIDs qui peuvent être retournés dans la réponse. Notez que la valeur de cette constante peut être révisée dans les versions ultérieures de ce fichier d’en-tête.              |
| Paramètre d’opération 4 | 0                                                                                                                                                                                                                               |
| Paramètre d’opération 5 | 0                                                                                                                                                                                                                               |
| Données                  | L’appareil retourne un tableau MTP contenant des PUOIDs acquis. Le tableau commence par une valeur **DWORD** indiquant le nombre d’éléments dans le tableau, suivi du tableau d’éléments.                               |
| Direction des données        | R->I                                                                                                                                                                                                                         |
| Options de code de réponse | **MTP \_ RÉPONSE \_ OK** (0x2001) ou code de réponse d’erreur valide.                                                                                                                                                                    |
| Paramètre de réponse 1  | ID de la transaction actuelle.                                                                                                                                                                                                     |
| Paramètre de réponse 2  | Nombre de PUOIDs qui restent à récupérer par des demandes ultérieures.                                                                                                                                                            |
| Paramètre de réponse 3  | **Valeur DWORD** contenant les informations d’État. L’État est indiqué par une opération au niveau du bit. Pour plus d’informations sur les indicateurs à utiliser, consultez la section Notes.                                                                                              |
| Paramètre de réponse 4  | 0                                                                                                                                                                                                                               |
| Paramètre de réponse 5  | 0                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Remarques

L’État est indiqué par le paramètre de réponse 3 dans un mode de bits à l’aide de l’indicateur suivant.



| Indicateur                                              | Valeur | Description                                                                                                                                                                                                                             |
|---------------------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **indicateurs MDRT WMP qui ne sont pas \_ \_ \_ signalés comme étant \_ acquis \_** | 0x1   | L’appareil contient des éléments acquis qui ne peuvent pas être retournés dans la liste des PUOIDS. Notez que cet indicateur n’est pas redondant avec le paramètre de réponse 2. Définissez cet indicateur uniquement lorsqu’il y a des éléments demandés que l’appareil ne peut pas retourner. |



 

Les bits 1 à 31 sont réservés à une utilisation ultérieure. Ces bits doivent être définis sur zéro.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecteur Windows Media**](windows-media-player.md)
</dt> </dl>

 

 




