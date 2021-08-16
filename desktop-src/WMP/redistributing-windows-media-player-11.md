---
title: redistribution Lecteur Windows Media 11
description: redistribution Lecteur Windows Media 11
ms.assetid: 3348821f-6d72-40c2-954b-0046ce502401
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec17042165ed891370d1543fad303150c4b21d1f1db7f9da38de9f75d02876a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746558"
---
# <a name="redistributing-windows-media-player-11"></a>redistribution Lecteur Windows Media 11

vous pouvez installer Lecteur Windows Media 11 sur Windows XP à l’aide de l’un des programmes d’installation suivants, où *localeId* est un identificateur de paramètres régionaux.

-   WMP11-WindowsXP-x86-*localeId*.exe
-   WMP11-WindowsXP-x64-*localeId*.exe

Voici un exemple de ligne de commande pour l’installation sans interface utilisateur et sans invite de redémarrage ou de redémarrage.


```
wmp11-windowsxp-x86-enu.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



le tableau suivant présente des paramètres supplémentaires que vous pouvez utiliser avec le programme d’installation de Lecteur Windows Media 11.



| Paramètre              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Empêcher la migration de la bibliothèque.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Créez un point de restauration système imbriqué. utilisez cette valeur si votre application crée un point de restauration système pour imbriquer le point de restauration Lecteur Windows Media dans le point de restauration de votre application.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | Interdire la création d’un point de restauration système. Cet indicateur désactive la création d’un point de restauration système. Dans la plupart des cas, cet indicateur ne doit pas être utilisé pour la redistribution de logiciels générale. elle doit être utilisée uniquement lorsque vous pouvez faire un choix explicite au nom de l’utilisateur final pour ne pas prendre en charge la restauration des fichiers de Lecteur Windows Media vers une version antérieure du lecteur. Cet indicateur doit être utilisé uniquement pour le déploiement d’entreprise ou l’installation OEM (Original Equipment Manufacturer). |
| /DefaultService        | Définissez le magasin en ligne initial. Pour plus d’informations, consultez [paramètres de ligne de commande du programme d’installation pour les magasins en ligne](setup-command-line-parameters-for-online-stores.md).                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**redistribution du logiciel Lecteur Windows Media**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




