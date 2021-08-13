---
description: pour aider à maintenir un environnement sécurisé lors de l’installation des logiciels, respectez ces instructions lors de la création du package Windows Installer.
ms.assetid: 04d91a9b-0528-4acb-8e11-fc817009db1f
title: Instructions pour la création d’installations sécurisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f796594fe665875f63751d0da4cac5bd7cde621e04b4d1d35585c74755dd719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635797"
---
# <a name="guidelines-for-authoring-secure-installations"></a>Instructions pour la création d’installations sécurisées

le respect des indications suivantes lors de la création d’un package de Windows Installer aide à maintenir un environnement sécurisé pendant l’installation :

-   Les administrateurs doivent installer des applications gérées dans un dossier d’installation cible pour lequel les utilisateurs non-administrateurs n’ont pas de privilèges de modification ou de modification.
-   Rendez toute propriété définie par l’utilisateur une propriété publique. Les propriétés privées ne peuvent pas être modifiées par l’utilisateur qui interagit avec l’interface utilisateur. Pour plus d’informations, consultez [à propos des propriétés](about-properties.md).
-   N’utilisez pas de propriétés pour les mots de passe ou d’autres informations qui doivent rester sécurisées. Le programme d’installation peut écrire la valeur d’une propriété créée dans la [table de propriétés](property-table.md)ou créée au moment de l’exécution dans un journal ou dans le registre système. Pour plus d’informations, consultez [la page empêcher l’écriture d’informations confidentielles dans le fichier journal](preventing-confidential-information-from-being-written-into-the-log-file.md).
-   Lorsque l’installation requiert que le programme d’installation utilise des privilèges [*élevés*](e-gly.md) , utilisez des [propriétés publiques restreintes](restricted-public-properties.md) pour restreindre les propriétés publiques qu’un utilisateur peut modifier. Certaines restrictions sont généralement nécessaires pour maintenir un environnement sécurisé lorsque l’installation requiert que le programme d’installation utilise des privilèges *élevés* .
-   Évitez d’installer des services qui empruntent l’identité des privilèges d’un utilisateur particulier, car cela peut écrire des données de sécurité dans un journal ou dans le registre système. Cela crée un risque pour un problème de sécurité, un conflit de mot de passe ou la perte de données de configuration lors du redémarrage du système. Pour plus d’informations, consultez la [table ServiceInstall](serviceinstall-table.md).
-   Utilisez la table [LockPermissions](lockpermissions-table.md) et la [table MsiLockPermissionsEx](msilockpermissionsex-table.md) pour sécuriser les services, les fichiers, les clés de Registre et les dossiers créés dans un environnement verrouillé.
-   Ajoutez des signatures numériques à l’installation pour garantir l’intégrité des fichiers. pour plus d’informations, consultez [Signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md) et [création d’une Installation signée entièrement vérifiée](authoring-a-fully-verified-signed-installation.md).
-   créez votre Windows Installer package de sorte que si l’accès aux ressources est refusé à l’utilisateur, le programme d’installation échoue de manière à maintenir un environnement sécurisé. Vérifiez les privilèges d’accès de l’utilisateur et déterminez si l’espace disque est suffisant avant le début de l’installation. En règle générale, le programme d’installation ne doit afficher une boîte de dialogue de navigation que si l’utilisateur actuel est un administrateur ou si l’installation ne requiert pas de privilèges [*élevés*](e-gly.md) . Pour plus d’informations, consultez [résilience source](source-resiliency.md).
-   Utilisez des [transformations sécurisées](secured-transforms.md) pour stocker des transformations dans un système de fichiers sécurisé localement sur l’ordinateur de l’utilisateur. Cela empêche l’utilisateur d’avoir un accès en écriture à la transformation.
-   Pour plus d’informations sur la sécurisation des sources multimédias des applications gérées, consultez [résilience source](source-resiliency.md).
-   Utilisez la propriété [**Résumé de sécurité**](security-summary.md) pour indiquer si le package doit être ouvert en lecture seule. Cette propriété doit être définie sur lecture seule recommandée pour une base de données d’installation et à appliquer en lecture seule pour une transformation ou un correctif.
-   Le programme d’installation exécute des actions personnalisées avec des privilèges d’utilisateur par défaut afin de limiter l’accès des actions personnalisées au système. Le programme d’installation peut exécuter des actions personnalisées avec des privilèges [*élevés*](e-gly.md) si une application managée est en cours d’installation ou si la stratégie système a été spécifiée pour des privilèges élevés. Pour plus d’informations, consultez [sécurité des actions personnalisées](custom-action-security.md).
-   Utilisez la stratégie [DisablePatch](disablepatch.md) pour assurer la sécurité dans les environnements où les correctifs doivent être limités.
-   Utilisez la [table AppID](appid-table.md) pour enregistrer les paramètres de configuration et de sécurité courants pour les objets DCOM.
-   Pour obtenir des informations connexes, consultez [instructions pour la sécurisation des actions personnalisées](guidelines-for-securing-custom-actions.md).
-   Pour obtenir des informations connexes, consultez [instructions pour la sécurisation des packages sur les ordinateurs verrouillés](guidelines-for-securing-packages-on-locked-down-computers.md).
-   à compter de Windows Installer 3,0, la mise à [jour corrective du contrôle de compte d’utilisateur](user-account-control--uac--patching.md) permet aux utilisateurs non-administrateurs d’appliquer des correctifs aux applications installées dans le contexte par ordinateur. La mise à jour corrective du contrôle de compte d’utilisateur est activée en fournissant un certificat de signataire dans la table [MsiPatchCertificate](msipatchcertificate-table.md) et en signant les correctifs avec le même certificat.
-   la capacité du Windows Installer 5,0 à définir des autorisations d’accès sur les services, les fichiers, les dossiers créés et les entrées de registre peut aider à renforcer la sécurité des applications d’installation. Pour plus d’informations, consultez [sécurisation des ressources](securing-resources-.md).

 

 



