---
description: Le tableau suivant répertorie les objets COM et les interfaces associés aux contrôles de conférence Rendezvous.
ms.assetid: d9634586-8315-46d3-9ffc-bfa9a4d7738e
title: Interfaces COM Rendezvous
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05978b3536b2bb6d3cb384372c00f9052c2d602b51fb52e79f88d6f8eff2ca32
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080479"
---
# <a name="rendezvous-com-interfaces"></a>Interfaces COM Rendezvous

\[les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne sont pas disponibles pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation. L’API cliente RTC offre des fonctionnalités similaires.\]

Le tableau suivant répertorie les objets COM et les interfaces associés aux contrôles de conférence Rendezvous.

Pour plus d’informations sur le modèle COM (Component Object Model), consultez les sections correspondantes dans le kit de développement logiciel (SDK) de la plateforme.



| Interfaces                                                         | Description                                                                                                               |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**IEnumDialableAddrs**](/windows/desktop/api/Rend/nn-rend-ienumdialableaddrs)                   | Énumère les adresses numérotables disponibles dans le répertoire actif.                                                     |
| [**IEnumDirectory**](/windows/desktop/api/Rend/nn-rend-ienumdirectory)                           | Énumère les objets [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) .                                                                    |
| [**IEnumDirectoryObject**](/windows/desktop/api/Rend/nn-rend-ienumdirectoryobject)               | Énumère les objets [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) .                                                        |
| [**IEnumMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)                         | Énumère les objets [**IMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope) .                                                                    |
| [**IEnumMedia**](ienummedia.md)                                   | Énumère les objets [**ITMedia**](itmedia.md) .                                                                            |
| [**IEnumTime**](ienumtime.md)                                     | Énumère les objets [**ITTime**](ittime.md) .                                                                              |
| [**IMcastAddressAllocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)         | Interface principale pour le wrapper COM de l’allocation d’adresses de multidiffusion.                                                           |
| [**IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)                         | Fournit des méthodes pour récupérer et définir des informations de bail d’adresse.                                                           |
| [**IMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)                                 | Encapsule toutes les propriétés d’une étendue de multidiffusion et fournit des méthodes pour obtenir des informations sur la portée.             |
| [**ITAttributeList**](itattributelist.md)                         | Permet d’obtenir et de définir des attributs non interprétés.                                                                   |
| [**ITConferenceBlob**](itconferenceblob.md)                       | Fournit l’accès aux informations de conférence spécifiques au fournisseur.                                                              |
| [**ITConnection**](itconnection.md)                               | Fournit des méthodes pour manipuler des facteurs de connexion tels que l’adresse de la Conférence, la portée et la bande passante.                       |
| [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory)                                 | Obtient et définit les informations de répertoire, et fournit l’accès à un objet d’annuaire particulier.                                |
| [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)                     | Obtient et définit des informations génériques pour une conférence ou un utilisateur dans un répertoire.                                            |
| [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) | Obtient et définit des informations génériques spécifiques à une conférence, telles que les heures de démarrage et d’arrêt.                                 |
| [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser)             | Obtient et définit des informations génériques spécifiques à un utilisateur, telles que le nom d’un ordinateur qui est le téléphone IP principal de l’utilisateur. |
| [**ITILSConfig**](/windows/desktop/api/Rend/nn-rend-itilsconfig)                                 | Obtient et définit des informations spécifiques au serveur d’un répertoire ILS donné.                                                |
| [**ITMedia**](itmedia.md)                                         | Obtient et définit les propriétés de média de base, telles que le nom du média et le protocole de transport.                                       |
| [**ITMediaCollection**](itmediacollection.md)                     | Autorise l’accès aux médias par index. Permet la création et la suppression de médias.                                                     |
| [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous)                               | Interface principale pour le contrôle Rendezvous.                                                                                |
| [**ITSdp**](itsdp.md)                                             | Manipule l’objet BLOB SDP (session Description Protocol). Référence : RFC 2327.                                             |
| [**ITTime**](ittime.md)                                           | Donne accès à un ensemble de délais d’activation pour la session.                                                             |
| [**ITTimeCollection**](ittimecollection.md)                       | Autorise l’accès au composant heure par index. Permet la création et la suppression de composants de temps.                                  |



 

 

 



