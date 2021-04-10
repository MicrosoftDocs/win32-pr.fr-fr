---
title: Redistribution du lecteur Windows Media série 9
description: Redistribution du lecteur Windows Media série 9
ms.assetid: 812e3fc7-e23d-489c-a486-62c7602cf46e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f48da20123255ae08a0993d361a95deb8ed335
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029753"
---
# <a name="redistributing-windows-media-player-9-series"></a>Redistribution du lecteur Windows Media série 9

Vous pouvez installer le lecteur Windows Media 9 sur Windows XP en utilisant l’un des programmes d’installation suivants.

-   MPSetupXP.exe
-   MPSetup.exe

> [!Note]  
> MPSetup.exe est un sur-ensemble du programme d’installation de MPSetupXP.exe. Il contient les fichiers nécessaires aux systèmes d’exploitation antérieurs à Windows XP. MPSetup.exe est fonctionnellement équivalente à MPSetupXP.exe lorsqu’il est exécuté sur Windows XP, mais la taille du fichier du programme d’installation est plus importante car elle n’a pas été optimisée pour l’installation sur les systèmes d’exploitation Windows XP.

 

Vous pouvez installer le lecteur Windows Media 9 sur Windows 98 Deuxième édition, Windows Millennium Edition ou Windows 2000 à l’aide du programme d’installation suivant.

-   MPSetup.exe

Voici un exemple de ligne de commande pour l’installation sans interface utilisateur et sans invite de redémarrage ou de redémarrage.


```
MPSetup.exe /q:A /c:"setup_wm.exe /Q /R:N /P:#e"
```



> [!Note]  
> Le paramètre/P : \# e spécifie que le package d’installation du lecteur Windows Media doit être mis en cache lors de l’installation du lecteur Windows Media. Cette commande est utilisée pour gérer les futures mises à niveau du système d’exploitation. Cette commande ne doit être omise que par les administrateurs informatiques de l’entreprise. Le seul cas où/P : \# e ne doit pas être inclus sur la ligne de commande est lorsque vous êtes propriétaire du système cible et que vous savez que le système cible ne sera jamais mis à niveau vers un système d’exploitation ultérieur. Par exemple, si vous installez le lecteur Windows Media 9 sur Windows 2000 et que l’ordinateur a peut-être été mis à niveau vers Windows XP, vous devez utiliser/P : \# e sur la ligne de commande. Dans le cas contraire, après l’installation de Windows XP, les fichiers du lecteur Windows Media seront remplacés par les fichiers du lecteur Windows Media pour Windows XP.

 

Le tableau suivant présente des paramètres supplémentaires que vous pouvez utiliser avec le programme d’installation de Windows Media Player 9 Series.



| Paramètre              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Empêcher la migration de la bibliothèque.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Créez un point de restauration système imbriqué. Utilisez cette valeur si votre application crée un point de restauration système pour imbriquer le point de restauration du lecteur Windows Media au sein de votre point de restauration de l’application.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | Interdire la création d’un point de restauration système. Cet indicateur désactive la création d’un point de restauration système. Dans la plupart des cas, cet indicateur ne doit pas être utilisé pour la redistribution de logiciels générale. Elle doit être utilisée uniquement lorsque vous pouvez faire un choix explicite au nom de l’utilisateur final pour ne pas prendre en charge la restauration des fichiers du lecteur Windows Media vers une version antérieure du lecteur. Cet indicateur doit être utilisé uniquement pour le déploiement d’entreprise ou l’installation OEM (Original Equipment Manufacturer). |



 

## <a name="notes"></a>Notes

-   Les paramètres de ligne de commande respectent la casse.
-   Lorsque vous supprimez l’invite de redémarrage, vous devez vérifier la clé de Registre InstallResult et gérer la notification de redémarrage dans l’application d’installation appelante.
-   Le lecteur Windows Media 9 installe également le runtime Windows Media format. il n’est donc pas nécessaire d’inclure à la fois le package de distribution du lecteur Windows Media et le package de distribution du format d’exécution Windows Media dans le même package de redistribution de logiciels. Par conséquent, si vous incluez des MPSetup.exe ou des MPSetupXP.exe dans votre installation, vous n’avez pas besoin d’inclure de WMFdist.exe.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Redistribution du logiciel Windows Media Player**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




