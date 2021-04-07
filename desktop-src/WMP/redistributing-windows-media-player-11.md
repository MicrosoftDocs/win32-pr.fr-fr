---
title: Redistribution du lecteur Windows Media 11
description: Redistribution du lecteur Windows Media 11
ms.assetid: 3348821f-6d72-40c2-954b-0046ce502401
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674da0298196f0749a549670bf9bd7c4095b6e7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028984"
---
# <a name="redistributing-windows-media-player-11"></a>Redistribution du lecteur Windows Media 11

Vous pouvez installer le lecteur Windows Media 11 sur Windows XP en utilisant l’un des programmes d’installation suivants, où *LocaleID* est un identificateur de paramètres régionaux.

-   WMP11-WindowsXP-x86-*LocaleID*. exe
-   WMP11-WindowsXP-x64-*LocaleID*. exe

Voici un exemple de ligne de commande pour l’installation sans interface utilisateur et sans invite de redémarrage ou de redémarrage.


```
wmp11-windowsxp-x86-enu.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



Le tableau suivant présente des paramètres supplémentaires que vous pouvez utiliser avec le programme d’installation du lecteur Windows Media 11.



| Paramètre              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Empêcher la migration de la bibliothèque.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Créez un point de restauration système imbriqué. Utilisez cette valeur si votre application crée un point de restauration système pour imbriquer le point de restauration du lecteur Windows Media au sein de votre point de restauration de l’application.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | Interdire la création d’un point de restauration système. Cet indicateur désactive la création d’un point de restauration système. Dans la plupart des cas, cet indicateur ne doit pas être utilisé pour la redistribution de logiciels générale. Elle doit être utilisée uniquement lorsque vous pouvez faire un choix explicite au nom de l’utilisateur final pour ne pas prendre en charge la restauration des fichiers du lecteur Windows Media vers une version antérieure du lecteur. Cet indicateur doit être utilisé uniquement pour le déploiement d’entreprise ou l’installation OEM (Original Equipment Manufacturer). |
| /DefaultService        | Définissez le magasin en ligne initial. Pour plus d’informations, consultez [paramètres de ligne de commande du programme d’installation pour les magasins en ligne](setup-command-line-parameters-for-online-stores.md).                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Redistribution du logiciel Windows Media Player**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




