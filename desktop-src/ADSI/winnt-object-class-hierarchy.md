---
title: Hiérarchie de classes d’objets Winnt
description: La hiérarchie de classes d’objets Winnt démarre à partir de l’objet Namespace.
ms.assetid: 01dfdfec-cfdf-43ee-bf2f-c05a741bfb22
ms.tgt_platform: multiple
keywords:
- ADSI du fournisseur de services WinNT, hiérarchie des classes d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6facb31a41e3b03db8290dd6a11e56f9a56c06b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507023"
---
# <a name="winnt-object-class-hierarchy"></a>Hiérarchie de classes d’objets Winnt

La hiérarchie de classes d’objets Winnt démarre à partir de l’objet Namespace.



| classe d'objet,                   | Description                                                                       |
|--------------------------------|-----------------------------------------------------------------------------------|
| Espace de noms<br/>           | Conteneur d’objets de niveau supérieur.<br/>                                            |
| Domain<br/>              | Domaine Windows NT.<br/>                                                 |
| Utilisateur<br/>                | Compte d’utilisateur.<br/>                                                          |
| Group<br/>               | Compte de groupe pour la gestion des droits d’accès.<br/>                              |
| UserGroupCollection<br/> | Ensemble de groupes d’utilisateurs qui implémentent [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).<br/>  |
| GroupCollection<br/>     | Ensemble d’autres groupes qui implémentent [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers).<br/> |
| Computer<br/>            | Serveur ou station de travail Windows NT 4,0.<br/>                                  |
| PrintJob<br/>            | Travail d’impression dans la file d’attente à l’impression.<br/>                                          |
| PrintJobsCollection<br/> | Ensemble de travaux d’impression.<br/>                                                   |
| PrintQueue<br/>          | File d’attente à l’impression sur un spouleur d’impression.<br/>                                      |
| Service<br/>             | Application s’exécutant en tant que service.<br/>                                      |
| FileService<br/>         | Services accédant au système de fichiers.<br/>                                        |
| FileShare<br/>           | Point de partage de fichiers.<br/>                                                      |
| Ressource<br/>            | Ressource dans le service.<br/>                                             |
| session<br/>             | Connexion au service de fichiers active.<br/>                                     |
| Utilisateur<br/>                | Compte d’utilisateur local.<br/>                                                    |
| Group<br/>               | Groupe local.<br/>                                                           |
| UserCollection<br/>      | Collection d’utilisateurs locaux.<br/>                                             |
| GroupCollection<br/>     | Collection de groupes locaux.<br/>                                            |
| schéma<br/>              | Conteneur du schéma Winnt.<br/>                                                |
| Classe<br/>               | Définition de classe de schéma.<br/>                                               |
| Propriété<br/>            | Définition d’attribut de schéma.<br/>                                           |
| Syntaxe<br/>              | Syntaxe d’une propriété.<br/>                                                  |



 

 

 





