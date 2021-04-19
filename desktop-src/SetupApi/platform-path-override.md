---
description: Remplacement du chemin d’accès de la plateforme
ms.assetid: f430fd9a-f865-4cdb-b0ea-4e6d79913308
title: Remplacement du chemin d’accès de la plateforme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9a6ae6795b444c44db91d90ecd93efd19ea9dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538204"
---
# <a name="platform-path-override"></a>Remplacement du chemin d’accès de la plateforme

La fonction [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) est utilisée pour définir un remplacement de chemin d’accès de plateforme pour un ordinateur cible lors de l’utilisation de fichiers INF à partir d’un autre ordinateur. Par conséquent, il peut faire référence à une plateforme différente de celle sur laquelle il est en cours d’exécution. Pour traiter les sources multimédias, il peut faire référence à des plateformes qui ne sont plus prises en charge, telles que alpha, MIPS et PPC. Elle supprime la substitution du chemin d’accès de la plateforme si aucune valeur n’est spécifiée.

Une fois qu’une substitution du chemin d’accès à la plateforme a été définie par un appel à [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea), toute fonction de configuration qui met en file d’attente les opérations de copie de fichiers examine le composant final du chemin source. Si le composant final correspond au nom de la plateforme de l’utilisateur, la fonction d’installation le remplace par la chaîne de remplacement définie par **SetupSetPlatformPathOverride**.

Par exemple, lors de l’installation de pilotes d’imprimante sur un serveur MIPS, vous souhaiterez peut-être installer des pilotes pour toutes les plateformes prises en charge. La mise en file d’attente des fichiers installe normalement les fichiers spécifiés dans les sections dépendant des MIPS du fichier INF, avec les chemins sources tels que les \\ \\ \\ \\ mips sources. Pour installer les fichiers pour une deuxième plateforme, vous devez appeler [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) avec *override* indiquant la plateforme de remplacement. Si l’emplacement indiqué par *override* contient la valeur de chaîne « alpha », le chemin source des opérations de copie de fichiers envoyées à la file d’attente avec un chemin source de \\ \\ \\ mips source est \\ remplacé par la \\ \\ \\ source racine \\ alpha. Vous devez répéter ce processus pour chaque plateforme qui vous intéresse.

 

 



