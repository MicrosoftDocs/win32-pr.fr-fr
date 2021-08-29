---
description: La configuration par application redirige la dépendance d’une application particulière d’une version d’un assembly côte à côte vers une autre version de l’assembly.
ms.assetid: b7988385-c87e-443c-8ec3-84ab3c172eab
title: Configuration par application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccecdd184ec9c23d3b06a698abeba01b266e558c72851cefb283d3a98adffaae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142022"
---
# <a name="per-application-configuration"></a>Configuration par application

La configuration par application redirige la dépendance d’une application particulière d’une version d’un assembly côte à côte vers une autre version de l’assembly. Une configuration par application peut devenir nécessaire si le bon fonctionnement d’une application particulière requiert une version d’assembly différente de la version normalement spécifiée comme configuration [par défaut](default-configuration.md) ou configuration du serveur de [publication](publisher-configuration.md). Par exemple, une mise à jour globale de la version de l’assembly par le serveur de publication peut corriger l’assembly, mais rompre cette application particulière. Dans ce cas, la configuration par application peut être utilisée pour permettre à l’application de continuer à s’exécuter avec la version d’assembly précédente.

à compter de Windows Server 2003, la configuration par application remplace toujours la [configuration par défaut](default-configuration.md) pour chaque application. La configuration par application remplace la configuration de l' [éditeur](publisher-configuration.md) pour chaque application uniquement si le fichier de [configuration](application-configuration-files.md) de l’application spécifie *apply = "no"* dans **publisherPolicy** et qu’une entrée correspondante est présente dans la base de données de compatibilité des applications.

> [!Note]  
> sur Windows XP, la configuration par application remplace la configuration [par défaut](default-configuration.md) et la [configuration](publisher-configuration.md) du serveur de publication par application. pour plus d’informations, consultez [Configuration par application sur Windows XP](per-application-configuration-on-windows-xp.md).

 

à compter de Windows Server 2003, une configuration par application remplacera une [configuration d’éditeur](publisher-configuration.md) si le [fichier de configuration d’application](application-configuration-files.md) spécifie *apply = « yes »* dans **publisherPolicy** et que l’indicateur EnableAppConfig est défini pour l’application dans la base de données de compatibilité des applications. Cette fonctionnalité permettant de remplacer une configuration de serveur de publication à l’aide d’une configuration par application permet à l’application d’être exécutée en mode sans échec. pour plus d’informations sur la base de données de compatibilité des applications et la Safemode, consultez la Windows Shared Computer Toolkit de compatibilité des applications. vous pouvez obtenir le Windows Shared Computer Toolkit de compatibilité des applications à partir de [https://www.microsoft.com/downloads](https://www.microsoft.com/Downloads/) .

> [!Note]  
> Si vous expédiez des composants avec un [fichier de configuration d’application](application-configuration-files.md) (fichier .config) qui spécifie *apply = "no"* dans **publisherPolicy**, cela entraîne l’échec de la génération du contexte d’activation. La configuration par application sera ignorée si vous expédiez des composants avec un fichier .config spécifiant *apply = "Yes"* dans **publisherPolicy**.

 

Les administrateurs d’applications peuvent implémenter une configuration par application en créant et en installant des fichiers de configuration d’application et en mettant à jour la base de données de compatibilité des applications. Le fichier de configuration de l’application doit ensuite être déployé et installé dans le même dossier que le fichier exécutable de l’application. Pour obtenir la liste du schéma de fichier, consultez [schéma du fichier de configuration](application-configuration-file-schema.md)de l’application. la base de données de compatibilité des applications doit être distribuée comme décrit dans le Shared Computer Toolkit de compatibilité des applications.

> [!Note]  
> Si votre application s’exécute en mode safemode, elle ne recevra pas de correctifs de sécurité ou de correctifs de bogues importants. l’éditeur de l’assembly peut être émis comme des fichiers de configuration d’éditeur. Une application qui utilise une configuration par application peut donc rester non sécurisée ou continuer à fonctionner de manière incorrecte même après l’application d’un nouvel assembly avec ces correctifs au système. Pour cette raison, les développeurs d’applications ne doivent jamais livrer une application avec une configuration par application. La configuration par application doit être utilisée uniquement par les administrateurs d’entreprise comme un correctif temporaire lorsque l’application est interrompue par une configuration de serveur de publication. Dans ce cas, la solution permanente est que les développeurs de l’assembly et les développeurs de l’application doivent travailler ensemble pour s’assurer que les assemblys avec la configuration du serveur de publication sont entièrement compatibles avec le niveau de compatibilité descendante.

 

Voici un exemple de fichier de configuration de l’application. Pour plus d’informations, consultez fichiers de configuration de l’application.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<configuration>
 <windows>
  <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
   <assemblyIdentity  processorArchitecture="X86" name="Microsoft.Windows.mysampleApp" type="win32" version="1.0.0.0"/>
   <publisherPolicy apply="no"/>                     
   <dependentAssembly>
    <assemblyIdentity type="win32" processorArchitecture="x86" name="Microsoft.Windows.SampleAssembly" publicKeyToken="0000000000000000"/>
    <bindingRedirect oldVersion="2.0.0.0" newVersion="2.0.1.0"/>
   </dependentAssembly>
  </assemblyBinding>
 </windows>
</configuration>
```

L’administrateur de l’application doit ajouter les entrées requises à la base de données de compatibilité des applications. téléchargez et installez le Windows Application compatibility Shared Computer Toolkit 2,6 à partir de [https://www.microsoft.com/downloads](https://www.microsoft.com/Downloads/) . Créez un nouveau personnalisé ou mettez à jour votre base de données existante à l’aide de l’administrateur de compatibilité, comme indiqué dans la boîte à outils. Le correctif de compatibilité que vous souhaitez choisir pour la couche de compatibilité pour votre application est EnableAppConfig. Vous devez toujours tester les applications avant d’installer une nouvelle base de données de compatibilité.

 

 



