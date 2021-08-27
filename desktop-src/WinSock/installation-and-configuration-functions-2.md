---
description: les fonctions suivantes sont implémentées dans le \_32.dll Ws2 et sont destinées à être utilisées par les applications qui installent des fournisseurs de services d’espace de noms et de transport Windows sockets sur un ordinateur.
ms.assetid: 3289737a-77b6-45d1-9c0a-3ed05b3475c2
title: Fonctions d’installation et de configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0731eff882c614c19c20d8323d012a7656fc2d8c15072aaafef3d7c91e46e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097859"
---
# <a name="installation-and-configuration-functions"></a>Fonctions d’installation et de configuration

les fonctions suivantes sont implémentées dans le \_32.dll Ws2 et sont destinées à être utilisées par les applications qui installent des fournisseurs de services d’espace de noms et de transport Windows sockets sur un ordinateur. Ces fonctions n’affectent ni les applications en cours d’exécution, ni les modifications apportées par ces fonctions aux applications en cours d’exécution.

Pour tous les fournisseurs, un identificateur de fournisseur est un GUID généré par le développeur du fournisseur (à l’aide de l’utilitaire Uuidgen.exe) et fourni à Ws2 \_32.dll.



| Fonction                                                                      | Description                                                                                                                                              |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSCDeinstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider)                        | Supprime un fournisseur de services de transport du Registre.                                                                                                  |
| [**WSCDeinstallProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32)                      | Supprime le fournisseur de services de transport 32 bits spécifié du Registre sur une plateforme 64 bits.                                                          |
| [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)                                | Récupère des informations sur les protocoles de transport disponibles.                                                                                               |
| [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)                              | Récupère des informations sur les protocoles de transport disponibles dans le catalogue 32 bits sur les plateformes 64 bits.                                                     |
| [**WSCInstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider)                            | Inscrit un nouveau fournisseur de services de transport.                                                                                                              |
| [**WSCInstallProvider64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32)                   | Inscrit un nouveau fournisseur de services de transport dans les bases de données de configuration système 32 bits et 64 bits sur une plateforme 64 bits.                               |
| [**WSCInstallProviderAndChains**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains)            | Inscrit un nouveau fournisseur de services de transport 32 bits ainsi que ses chaînes de protocole spécifiques dans la base de données de configuration système sur une plateforme 32 bits.   |
| [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32) | Inscrit un nouveau fournisseur de transport et sa chaîne de protocole spécifique dans les bases de données de configuration système 32 bits et 64 bits sur une plateforme 64 bits. |



 

 

 



