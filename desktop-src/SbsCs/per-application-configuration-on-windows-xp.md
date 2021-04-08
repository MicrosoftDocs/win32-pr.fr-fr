---
description: Sur Windows XP, la configuration par application remplace la configuration par défaut et la configuration du serveur de publication par application.
ms.assetid: 5b55d12d-8805-4820-91af-5ef583de3463
title: Configuration par application sur Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea6fa2e14e24e48be84247a23feecddf2784fbc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867894"
---
# <a name="per-application-configuration-on-windows-xp"></a>Configuration par application sur Windows XP

Sur Windows XP, la configuration par application remplace la configuration [par défaut](default-configuration.md) et la [configuration](publisher-configuration.md) du serveur de publication par application. Cela redirige la dépendance d’une application spécifique d’une version d’un assembly côte à côte vers une autre version spécifiée de l’assembly.

> [!Note]  
> À compter de Windows Server 2003, la configuration par application remplace la [configuration](publisher-configuration.md) de l’éditeur pour chaque application uniquement si le [fichier de configuration](application-configuration-files.md) de l’application spécifie *apply = "no"* dans **publisherPolicy** et qu’une entrée correspondante est présente dans la base de données de compatibilité des applications. La configuration par application remplace toujours la [configuration par défaut](default-configuration.md). Pour plus d’informations, consultez [configuration par application](per-application-configuration.md).

 

Une configuration par application peut devenir nécessaire si le bon fonctionnement d’une application particulière requiert une version d’assembly différente de la version normalement spécifiée comme configuration par défaut ou de serveur de publication. Par exemple, une mise à jour globale de la version de l’assembly par le serveur de publication peut corriger l’assembly, mais rompre cette application particulière. Dans ce cas, la configuration par application peut être utilisée pour permettre à l’application de continuer à s’exécuter avec la version d’assembly précédente. Un autre exemple, une installation Service Pack contenant une mise à jour d’assembly peut utiliser la configuration de l' [éditeur](publisher-configuration.md) pour rediriger les dépendances de l’ensemble des applications et des assemblys du système de la version 1.0.0.0 vers 1.0.1.0. Si une application nécessite que la version 1.0.0.0 fonctionne correctement, elle peut être redirigée vers la version 1.0.0.0 à l’aide d’une configuration par application.

Les administrateurs d’applications peuvent implémenter une configuration par application en créant et en installant des [fichiers de configuration d’application](application-configuration-files.md). Ces redirections d’une application spécifique de dépendent d’une version d’un assembly côte à côte pour dépendre d’une autre version. Les fichiers de configuration de l' [*application*](/windows/desktop/Msi/a-gly) peuvent remplacer les [fichiers de configuration](publisher-configuration-files.md) de l’éditeur et la configuration par défaut spécifiée par les manifestes d' [application](application-manifests.md) et les [manifestes d’assembly](assembly-manifests.md). Le fichier de configuration de l’application contient les informations utilisées par le chargeur lorsque [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) est appelé.

Pour configurer une application afin qu’elle remplace à la fois le manifeste de l’application et la configuration du serveur de publication, un développeur doit créer un fichier de configuration d’application. Le fichier de configuration de l’application est ensuite déployé et installé dans le même dossier que le fichier exécutable de l’application. Pour obtenir la liste du schéma de fichier, consultez [schéma du fichier de configuration](application-configuration-file-schema.md)de l’application.

Notez que si votre application utilise une configuration par application, elle ne recevra pas de correctifs de sécurité importants ou de correctifs de bogues que l’éditeur de l’assembly peut émettre comme fichiers de configuration d’éditeur. Une application qui utilise une configuration par application peut donc rester non sécurisée ou continuer à fonctionner de manière incorrecte même après l’application d’un nouvel assembly avec ces correctifs au système. Pour cette raison, les développeurs d’applications ne doivent jamais livrer une application avec une configuration par application. La configuration par application doit être utilisée uniquement par les administrateurs d’entreprise comme un correctif temporaire lorsque l’application est interrompue par une configuration de serveur de publication. Dans ce cas, la solution permanente est que les développeurs de l’assembly et les développeurs de l’application doivent travailler ensemble pour s’assurer que les assemblys avec la configuration du serveur de publication sont entièrement compatibles avec le niveau de compatibilité descendante.

Voici un exemple de fichier de configuration de l’application. Pour plus d’informations, consultez [fichiers de configuration](application-configuration-files.md)de l’application.

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<configuration>
  <windows>
    <assemblyBinding xmlns="urn:schemas-microsoft-com:asm.v1">
      <assemblyIdentity 
          name="Microsoft.Windows.mysampleApp" 
          processorArchitecture="x86" 
          version="1.0.0.0" type="win32"/>
        <dependentAssembly>
          <assemblyIdentity type="win32" 
              name="Microsoft.Windows.SampleAssembly" 
              processorArchitecture="x86" 
              publicKeyToken="0000000000000000"/>
          <bindingRedirect 
              oldVersion="2.0.0.0" 
              newVersion="2.0.1.0"/>
        </dependentAssembly>
    </assemblyBinding>
   </windows>
</configuration>
```

 

 
