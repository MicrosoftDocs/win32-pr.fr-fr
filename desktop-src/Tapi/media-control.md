---
description: Le support d’une session de communication est le formulaire dans lequel les données sont transmises. Les contrôles multimédias permettent à une application de reconnaître un large éventail de types de médias et d’ajuster les aspects du flux de médias, tels que le volume de transmission vocale.
ms.assetid: b32503fe-d494-44ea-b144-e38b8ab9b3d4
title: Contrôle multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17e3ad30107a98cc5d1a312880fa29422c42dce2b2bc59cadfbf894cb032d74a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034529"
---
# <a name="media-control"></a>Contrôle multimédia

Le support d’une session de communication est le formulaire dans lequel les données sont transmises. Les contrôles multimédias permettent à une application de reconnaître un large éventail de types de médias et d’ajuster les aspects du flux de médias, tels que le volume de transmission vocale.

La disponibilité du contrôle multimédia et des informations varie considérablement en fonction du type d’application TAPI, de la prise en charge du fournisseur de services et de l’environnement de communication local. La documentation suivante fournit une description générale du contrôle de média. L’interface TAPI fournit une infrastructure flexible pour l’implémentation des contrôles. les fonctionnalités les plus intéressantes sont souvent spécifiques à un fournisseur de services donné.

Sous la téléphonie classique, une application a très peu de contrôle sur le flux multimédia une fois qu’un chemin d’accès de communication a été configuré. Les applications TAPI 2 ont accès à certaines fonctions qui leur permettent de reconnaître et de réagir à des chiffres ou des tonalités pendant un appel. elles peuvent également utiliser l’API Wave pour exercer un contrôle supplémentaire sur les supports pendant une session de communication, mais elles ne disposent pas d’un accès en flux continu. Pour une revue de ces fonctions, consultez vue d’ensemble de l' [accès aux médias](./media-access.md) TAPI 2,2 ou vue d’ensemble de l' [accès aux médias](/previous-versions/windows/desktop/legacy/ms725240(v=vs.85)) TSPI.

TAPI 3 présente les [fournisseurs de services de média](about-the-media-service-provider-msp-.md), ce qui augmente considérablement les informations et le contrôle sur le média ou une session de communication. Une application TAPI 3 peut accéder directement au [flux](stream-objects.md) multimédia d’une session. Un flux distinct est créé pour chaque type de média impliqué dans la session, comme la voix ou la vidéo. Certains MSP peuvent implémenter des contrôles de sous-flux, qui peuvent répartir davantage les flux, par exemple par participant dans le cas du MSP IPConf.



| Fonctions TAPI 2. x                                          | Description                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**lineGatherDigits**](/windows/win32/api/tapi/nf-tapi-linegatherdigits)       | Lance la collecte mise en mémoire tampon des chiffres sur l’appel spécifié.                                                          |
| [**lineGenerateDigits**](/windows/win32/api/tapi/nf-tapi-linegeneratedigits)   | Initialise la génération des chiffres spécifiés sur l’appel spécifié en tant que tons inbandes à l’aide du mode de signalisation spécifié. |
| [**lineGenerateTone**](/windows/win32/api/tapi/nf-tapi-linegeneratetone)       | Génère le ton inbande spécifié sur l’appel spécifié.                                                               |
| [**lineMonitorDigits**](/windows/win32/api/tapi/nf-tapi-linemonitordigits)     | Active et désactive la détection non mise en mémoire tampon des chiffres reçus sur l’appel.                                              |
| [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia)       | Active et désactive la détection des types de média lors de l’appel spécifié.                                                   |
| [**lineMonitorTones**](/windows/win32/api/tapi/nf-tapi-linemonitortones)       | Active et désactive la détection des tons inbandes sur l’appel.                                                            |
| [**lineSetMediaControl**](/windows/win32/api/tapi/nf-tapi-linesetmediacontrol) | Active et désactive les actions de contrôle sur le flux de média associé à la ligne, à l’adresse ou à l’appel spécifié.             |



 



| Interfaces ou méthodes TAPI 3. x                               | Description                                                                                                                                                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITLegacyCallMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol) | Prend en charge les applications héritées qui doivent communiquer directement avec un appareil.                                                                                                                             |
| [**ITLegacyWaveSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport)           | Permet à une application de détecter si un terminal créé par un TSP hérité (pré-TAPI 3) peut être contrôlé à l’aide de l’API Wave.                                                                        |
| [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)                                 | Permet à une application de récupérer des informations sur un flux de données ; pour démarrer, suspendre ou arrêter le flux ; pour sélectionner ou désélectionner des terminaux sur un flux ; et pour obtenir la liste des terminaux sélectionnés dans le flux. |
| [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)                   | Permet à une application d’énumérer, de créer ou de supprimer des flux multimédias.                                                                                                                                   |



 

 

 
