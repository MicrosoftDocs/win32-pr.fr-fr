---
title: Créer et exécuter un exemple StoServe
description: L’exemple de client et d’autres exemples associés doivent être compilés avant que vous puissiez exécuter le client.
ms.assetid: 7d8fe758-0008-495d-89ae-a814cb07ea19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46645351eb75ceb6b4f6129049b9e8f2db59dbef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512036"
---
# <a name="create-and-run-stoserve-sample"></a>Créer et exécuter un exemple StoServe

L’exemple de client et d’autres exemples associés doivent être compilés avant que vous puissiez exécuter le client. Pour plus d’informations sur la génération des exemples, consultez [Comment générer des exemples](how-to-build-samples.md). Si vous avez déjà généré les exemples appropriés, STOCLIEN.EXE est l’exécutable client à exécuter pour l’exemple **StoServe** .

## <a name="code-tour"></a>Visite guidée du code

Le tableau suivant répertorie les fichiers pertinents pour l’exemple **StoServe** .



| Fichiers        | Description                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------|
| STOSERVE.TXT | Brève description de l’exemple                                                                                                  |
| ADOPTE     | Makefile générique pour la génération de l’exemple de code STOSERVE.DLL de cette leçon.                                            |
| STOSERVE. Manutention   | Fichier include pour déclarer comme importé ou définir comme exporté les fonctions de service dans STOSERVE.DLL.                 |
| STOSERVE. COTISATIONS | Fichier d’implémentation principal pour STOSERVE.DLL. A DllMain et les fonctions du serveur COM (par exemple, DllGetClassObject). |
| STOSERVE. DEF | Fichier de définition de module. Exporte les fonctions de logement du serveur.                                                             |
| STOSERVE. Release  | Fichier de définition de ressource DLL pour l’exécutable.                                                                      |
| STOSERVE. ICO | Ressource icône pour l’exécutable.                                                                                     |
| Serveurs. Manutention     | Fichier include pour l’objet C++ de contrôle serveur.                                                                       |
| Serveurs. COTISATIONS   | Fichier d’implémentation pour l’objet C++ de contrôle serveur.                                                                |
| Fabrique. Manutention    | Fichier include pour les objets COM de la fabrique de classe du serveur.                                                              |
| Fabrique. COTISATIONS  | Fichier d’implémentation pour les fabriques de classe du serveur.                                                                 |
| Entre. Manutention    | Fichier include pour les classes énumérateur de point de connexion, point de connexion et énumérateur de connexion.                |
| Entre. COTISATIONS  | Fichier d’implémentation pour les objets énumérateur de point de connexion, point de connexion et énumérateur de connexion.         |
| Imprimé. Manutention      | Fichier include pour la classe d’objets COM du colivre.                                                                        |
| Imprimé. COTISATIONS    | Le fichier d’implémentation pour la classe d’objets COM du colivre et les points de connexion.                                       |
| STOSERVE. DSP | Microsoft Visual Studio fichier projet.                                                                                     |



 

Les principales rubriques traitées dans cette présentation du code sont les suivantes :

-   Méthodes de l’interface [**IPaper**](ipaper-methods.md) .
-   Utilisation par le biais de l’interface [**IPaperSink**](ipapersink-methods.md) pour les notifications client.
-   [**Structures**](structures---stoserve.md) dans StoServe.
-   [Considérations Unicode](unicode-considerations.md).

 

 




