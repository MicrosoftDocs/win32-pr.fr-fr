---
description: L’interface de programmation d’applications (API) d’installation fournit un ensemble de fonctions que votre application d’installation peut appeler pour effectuer des opérations d’installation. Ces fonctions d’installation fonctionnent avec les fichiers INF Windows pour fournir les fonctionnalités d’installation suivantes.
ms.assetid: 58201596-cb8c-480a-abef-896c1f9ef098
title: Vue d’ensemble
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32b99c6079fdb61fd6bfd0033ffccb9ebb7b922
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536676"
---
# <a name="overview"></a>Vue d’ensemble

L’interface de programmation d’applications (API) d’installation fournit un ensemble de fonctions que votre application d’installation peut appeler pour effectuer des opérations d’installation. Ces fonctions d’installation fonctionnent avec les fichiers INF Windows pour fournir les fonctionnalités d’installation suivantes.



| Pour obtenir des informations sur                       | Consultez                                                                                                                                                                         |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Mise en file d’attente des fichiers                               | [Files d’attente de fichiers](file-queues.md)                                                                                                                                              |
| Installation des fichiers                            | [Files d’attente de fichiers](file-queues.md)<br/> [Configurer des applications](setup-applications.md)<br/> [Création d’applications d’installation](creating-setup-applications.md)<br/> |
| Gestion des erreurs et demande de support     | [Demande de disque et gestion des erreurs](disk-prompting-and-error-handling.md)                                                                                                  |
| Mise à jour des entrées de Registre                   | [Configurer des applications](setup-applications.md)                                                                                                                                |
| Journalisation des fichiers installés                     | [Journal des fichiers](file-log.md)                                                                                                                                                    |
| Stockage des chemins sources les plus récemment utilisés | [Liste de sources MRU](mru-source-list.md)                                                                                                                                      |



 

Les versions Unicode et ANSI sont disponibles pour la plupart des fonctions de configuration. Les fichiers texte Unicode doivent contenir la marque d’ordre d’octet de 0xFEFF standard pour permettre aux fonctions de configuration d’identifier le fichier en tant que texte Unicode.

Bien que l’API d’installation prenne en charge l’invite de commandes pour les boîtes de dialogue nouveau média et gestion des erreurs de base, les fonctions d’installation ne fournissent pas de fonctionnalités d’Assistant ni d’interface utilisateur générique.

Les développeurs doivent déterminer s’ils peuvent utiliser [Windows Installer](/windows/desktop/Msi/windows-installer-portal) pour installer leurs applications plutôt que l’API d’installation. Windows Installer réduit le coût total de possession (TCO) de vos clients en leur permettant d’installer et de configurer efficacement vos produits et applications. Le programme d’installation peut également fournir à votre produit de nouvelles fonctionnalités permettant de publier des fonctionnalités sans les installer, d’installer des produits à la demande et d’ajouter des personnalisations utilisateur.

 

