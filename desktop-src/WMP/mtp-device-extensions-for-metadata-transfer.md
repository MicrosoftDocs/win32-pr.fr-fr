---
title: Extensions d’appareil MTP pour le transfert de métadonnées
description: Extensions d’appareil MTP pour le transfert de métadonnées
ms.assetid: 9cf68373-e84f-4568-a9da-16ddee0fc4e9
keywords:
- Lecteur Windows Media, extensions d’appareil MTP
- Lecteur Windows Media, extensions de périphérique
- Lecteur Windows Media, extensions
- Lecteur Windows Media, métadonnées
- Lecteur Windows Media, MTP (Media Transfer Protocol)
- Protocole MTP (Media Transfer Protocol)
- MTP (Media Transfer Protocol)
- métadonnées, extensions d’appareils MTP
- métadonnées, extensions de périphérique
- métadonnées, extensions
- extensions d’appareils, transfert de métadonnées
- extensions, transfert de métadonnées
- Extensions d’appareil MTP pour le transfert de métadonnées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64ff16fd97f135d7f8c902af823b967079408fb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292566"
---
# <a name="mtp-device-extensions-for-metadata-transfer"></a>Extensions d’appareil MTP pour le transfert de métadonnées

Le protocole MTP (Media Transfer Protocol) est un protocole conçu pour les appareils multimédias portables. L’objectif principal de ce protocole est de fournir un protocole commun pour l’échange de données entre un ordinateur et un périphérique multimédia portable. Cela comprend la réception et l’envoi d’objets multimédias et l’énumération du contenu et des fonctionnalités de l’appareil.

MTP utilise des identificateurs d’objets uniques persistants (PUOIDs) pour identifier de manière unique les éléments multimédias numériques (et d’autres objets) stockés sur un appareil. quand vous échangez des informations sur les modifications qui se sont produites sur un appareil qui prend en charge MTP, l’appareil et Lecteur Windows Media utilisent PUOIDs pour identifier les objets qui ont été modifiés.

le fichier d’en-tête nommé wmpdevices. h, qui est installé dans le cadre du kit de développement logiciel (SDK) Lecteur Windows Media, définit les structures et les constantes nécessaires à la prise en charge des extensions d’appareils Lecteur Windows Media.

pour qu’un appareil soit reconnu comme prenant en charge le transfert de métadonnées via l’ensemble d’extensions de périphérique MTP Lecteur Windows Media, il doit inclure les informations suivantes dans le jeu de données DeviceInfo. (Pour plus d’informations sur ce jeu de données, consultez la section 4.6.1 de la spécification MTP.)



| Champ de DataSet          | Ordre des champs | Type de données  | Valeur                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **Chaîne** | « microsoft.com/WMPPD : 10,0 » |



 

Le tableau suivant fournit des détails sur l’opération MTP pour le transfert de métadonnées accéléré.



| Élément                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Code d’opération        | 0x9201                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Paramètre d’opération 1 | L’ID de transaction fourni par l’appareil lors de la session précédente. Cette valeur est égale à zéro pour la première session.                                                                                                                                                                                                                                                                                                                                                                                       |
| Paramètre d’opération 2 | Index de départ. Cette valeur est toujours égale à zéro lors du premier appel d’une session. Lors des appels suivants au sein de la même session de synchronisation, cette valeur augmente de la somme du nombre d’éléments modifiés et supprimés des données de la réponse précédente.                                                                                                                                                                                                                                             |
| Paramètre d’opération 3 | 0x10000. Cette constante, définie dans wmpdevices. h, est le nombre maximal de PUOIDs qui peuvent être retournés dans la réponse. Notez que la valeur de cette constante peut être révisée dans les versions ultérieures de ce fichier d’en-tête.                                                                                                                                                                                                                                                                                     |
| Paramètre d’opération 4 | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Paramètre d’opération 5 | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Données                  | L’appareil retourne deux tableaux MTP contigus contenant PUOIDs. Chaque tableau MTP commence par une valeur **DWORD** indiquant le nombre d’éléments dans le tableau, suivi du tableau d’éléments. Le premier tableau MTP contient la liste des PUOIDs qui ont été ajoutés ou modifiés. Le deuxième tableau MTP contient la liste des PUOIDs qui ont été supprimés du périphérique portable. Notez que la somme du nombre de PUOID dans les deux tableaux ne doit pas dépasser la valeur passée dans le paramètre d’opération 3.<br/> |
| Direction des données        | R->I                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Options de code de réponse | **MTP \_ RÉPONSE \_ OK** (0x2001) ou code de réponse d’erreur valide.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Paramètre de réponse 1  | ID de la transaction actuelle de l’appareil.                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Paramètre de réponse 2  | Nombre de PUOIDs qui restent à récupérer par des demandes ultérieures.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Paramètre de réponse 3  | **Valeur DWORD** contenant les informations d’État. L’État est indiqué par une opération au niveau du bit. Pour plus d’informations sur les indicateurs à utiliser, consultez la section Notes.                                                                                                                                                                                                                                                                                                                                                                     |
| Paramètre de réponse 4  | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Paramètre de réponse 5  | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Notes

L’État est indiqué par le biais du paramètre de réponse 3 dans un mode de bits à l’aide des indicateurs suivants.



| Indicateur                                             | Valeur | Description                                                                                                                                                                                                                          |
|--------------------------------------------------|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_indicateurs MDRT \_ WMP \_ désignalés par des \_ \_ éléments supprimés** | 0x1   | Les éléments ont été supprimés avant le premier nom de chemin d’accès à l’objet signalé. Cela indique souvent que l’appareil a été reformaté.                                                                                                           |
| **indicateurs MDRT WMP signalés comme étant \_ \_ \_ \_ ajoutés \_**   | 0x2   | L’appareil contient des éléments ajoutés qui ne peuvent pas être retournés dans la liste des PUOIDS. Notez que cet indicateur n’est pas redondant avec le paramètre de réponse 2. Définissez cet indicateur uniquement lorsqu’il y a des éléments demandés que l’appareil ne peut pas retourner. |



 

Les bits 2 à 31 sont réservés à une utilisation ultérieure. Ces bits doivent être définis sur zéro.

Lecteur Windows Media envoie la commande MTP à un appareil au démarrage d’une session de synchronisation avant le transfert des fichiers multimédias. L’appareil doit renvoyer sa réponse le plus rapidement possible pour éviter des retards dans l’opération de synchronisation.

Lecteur Windows Media demande des valeurs pour les attributs figurant dans [à propos des métadonnées](about-the-metadata.md) de chaque POUID modifié renvoyé dans la réponse. Lecteur Windows Media pouvez envoyer des valeurs mises à jour pour ces attributs à l’appareil dans les commandes suivantes.

Les fichiers signalés comme ayant été supprimés de l’appareil peuvent être copiés à nouveau sur l’appareil si les paramètres de l’utilisateur l’exigent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Extensions d’appareil pour le transfert de métadonnées accéléré**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 





