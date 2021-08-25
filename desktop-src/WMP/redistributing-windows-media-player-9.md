---
title: redistribution de Lecteur Windows Media série 9
description: redistribution de Lecteur Windows Media série 9
ms.assetid: 812e3fc7-e23d-489c-a486-62c7602cf46e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418a780836c0a64a1b31b0d3c01a69841b695803f5db61b049915ec0d981f9c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861679"
---
# <a name="redistributing-windows-media-player-9-series"></a>redistribution de Lecteur Windows Media série 9

vous pouvez installer Lecteur Windows Media série 9 sur Windows XP à l’aide de l’un des programmes d’installation suivants.

-   MPSetupXP.exe
-   MPSetup.exe

> [!Note]  
> MPSetup.exe est un sur-ensemble du programme d’installation de MPSetupXP.exe. il contient les fichiers nécessaires aux systèmes d’exploitation commercialisés avant Windows XP. MPSetup.exe est fonctionnellement équivalente à MPSetupXP.exe lorsqu’il est exécuté sur Windows xp, mais la taille du fichier du programme d’installation est plus importante car elle n’a pas été optimisée pour l’installation sur les systèmes d’exploitation Windows XP.

 

vous pouvez installer Lecteur Windows Media série 9 sur Windows 98 deuxième édition, Windows Millennium edition ou Windows 2000 à l’aide du programme d’installation suivant.

-   MPSetup.exe

Voici un exemple de ligne de commande pour l’installation sans interface utilisateur et sans invite de redémarrage ou de redémarrage.


```
MPSetup.exe /q:A /c:"setup_wm.exe /Q /R:N /P:#e"
```



> [!Note]  
> le paramètre/p : \# e spécifie que le package d’installation Lecteur Windows Media doit être mis en cache lors de l’installation de Lecteur Windows Media. Cette commande est utilisée pour gérer les futures mises à niveau du système d’exploitation. Cette commande ne doit être omise que par les administrateurs informatiques de l’entreprise. Le seul cas où/P : \# e ne doit pas être inclus sur la ligne de commande est lorsque vous êtes propriétaire du système cible et que vous savez que le système cible ne sera jamais mis à niveau vers un système d’exploitation ultérieur. par exemple, si vous installez Lecteur Windows Media série 9 sur Windows 2000 et que l’ordinateur a peut-être été mis à niveau vers Windows XP, vous devez utiliser/p : \# e sur la ligne de commande. dans le cas contraire, après l’installation de Windows XP, les fichiers Lecteur Windows Media seront remplacés par les fichiers de Lecteur Windows Media pour Windows XP.

 

le tableau suivant présente des paramètres supplémentaires que vous pouvez utiliser avec le programme d’installation de la série Lecteur Windows Media 9.



| Paramètre              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Empêcher la migration de la bibliothèque.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Créez un point de restauration système imbriqué. utilisez cette valeur si votre application crée un point de restauration système pour imbriquer le point de restauration Lecteur Windows Media dans le point de restauration de votre application.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | Interdire la création d’un point de restauration système. Cet indicateur désactive la création d’un point de restauration système. Dans la plupart des cas, cet indicateur ne doit pas être utilisé pour la redistribution de logiciels générale. elle doit être utilisée uniquement lorsque vous pouvez faire un choix explicite au nom de l’utilisateur final pour ne pas prendre en charge la restauration des fichiers de Lecteur Windows Media vers une version antérieure du lecteur. Cet indicateur doit être utilisé uniquement pour le déploiement d’entreprise ou l’installation OEM (Original Equipment Manufacturer). |



 

## <a name="notes"></a>Remarques

-   Les paramètres de ligne de commande respectent la casse.
-   Lorsque vous supprimez l’invite de redémarrage, vous devez vérifier la clé de Registre InstallResult et gérer la notification de redémarrage dans l’application d’installation appelante.
-   Lecteur Windows Media série 9 installe également le Windows media format runtime. il n’est donc pas nécessaire d’inclure à la fois le package de distribution Lecteur Windows Media et le package de distribution du runtime Windows media format dans le même package de redistribution de logiciels. Par conséquent, si vous incluez des MPSetup.exe ou des MPSetupXP.exe dans votre installation, vous n’avez pas besoin d’inclure de WMFdist.exe.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**redistribution du logiciel Lecteur Windows Media**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




