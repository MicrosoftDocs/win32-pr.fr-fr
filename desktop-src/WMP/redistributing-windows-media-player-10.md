---
title: redistribution Lecteur Windows Media 10
description: redistribution Lecteur Windows Media 10
ms.assetid: 58d601d4-e3d4-4a29-969c-799b2819f92c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4515317e0a6714d53c147671bbb83c06c172ef6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010930"
---
# <a name="redistributing-windows-media-player-10"></a>redistribution Lecteur Windows Media 10

vous pouvez installer Lecteur Windows Media 10 sur Windows XP à l’aide du programme d’installation suivant.

-   MP10Setup.exe

Voici un exemple de ligne de commande pour l’installation sans interface utilisateur et sans invite de redémarrage ou de redémarrage.


```
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



le tableau suivant présente des paramètres supplémentaires que vous pouvez utiliser avec le programme d’installation Lecteur Windows Media 10.



| Paramètre              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Empêcher la migration de la bibliothèque.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Créez un point de restauration système imbriqué. utilisez cette valeur si votre application crée un point de restauration système pour imbriquer le point de restauration Lecteur Windows Media dans le point de restauration de votre application.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | Interdire la création d’un point de restauration système. Cet indicateur désactive la création d’un point de restauration système. Dans la plupart des cas, cet indicateur ne doit pas être utilisé pour la redistribution de logiciels générale. elle doit être utilisée uniquement lorsque vous pouvez faire un choix explicite au nom de l’utilisateur final pour ne pas prendre en charge la restauration des fichiers de Lecteur Windows Media vers une version antérieure du lecteur. Cet indicateur doit être utilisé uniquement pour le déploiement d’entreprise ou l’installation OEM (Original Equipment Manufacturer). |
| /DefaultService        | Définissez le magasin en ligne initial. Pour plus d’informations, consultez [paramètres de ligne de commande du programme d’installation pour les magasins en ligne](setup-command-line-parameters-for-online-stores.md).                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**redistribution du logiciel Lecteur Windows Media**](redistributing-windows-media-player-software.md)
</dt> <dt>

[**Document ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




