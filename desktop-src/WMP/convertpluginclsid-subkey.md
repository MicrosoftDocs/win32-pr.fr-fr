---
title: Sous-clé ConvertPluginCLSID
description: Sous-clé ConvertPluginCLSID
ms.assetid: 2bf5b6ad-31e9-40c2-a682-c7ad813e8f7a
keywords:
- Lecteur Windows Media, sous-clé ConvertPluginCLSID
- Windows Media Player, extensions de nom de fichier
- Lecteur Windows Media, registre
- Registre, extensions de noms de fichiers
- Registre, sous-clé ConvertPluginCLSID
- Registre, paramètres pour le lecteur Windows Media
- paramètres de registre de l’extension de nom de fichier
- Sous-clé ConvertPluginCLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4229617c3999708d89fac976e94b2747b5a69145
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029303"
---
# <a name="convertpluginclsid-subkey"></a>Sous-clé ConvertPluginCLSID

Lorsque le lecteur Windows Media 11 rencontre une extension de nom de fichier personnalisée, il recherche une sous-clé de Registre qui correspond à l’extension. La sous-clé est décrite dans les paramètres de registre de l' [extension de nom de fichier](file-name-extension-registry-settings.md). Dans certains cas, la sous-clé de l’extension a une sous-clé nommée **ConvertPluginCLSID**.

Par exemple, supposons que vous avez créé un format de fichier personnalisé (avec l’extension de nom de fichier. xyz) et un plug-in de conversion qui convertit les fichiers dans un format pris en charge par le lecteur Windows Media, puis vous stockiez l’ID de classe du plug-in dans l’une ou les deux sous-clés suivantes.

**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Multimedia \\ wmplayer \\ extensions \\ . xyz \\ ConvertPluginCLSID**

**HKEY \_ Current \_ User \\ Software \\ \\ extensions Microsoft \\ MediaPlayer \\ Player \\ . xyz \\ ConvertPluginCLSID**

La sous-clé **ConvertPluginCLSID** spécifie les ID de classe des plug-ins que le lecteur Windows Media peut utiliser pour convertir un fichier multimédia à partir de son format personnalisé vers un format pris en charge par le lecteur.

La sous-clé **ConvertPluginCLSID** contient les entrées suivantes.

-   Entrée par défaut qui représente le plug-in de conversion par défaut.
-   Entrée nommée qui représente le plug-in de conversion par défaut.
-   Entrées nommées supplémentaires qui représentent d’autres plug-ins de conversion.

Par exemple, supposons qu’un format de fichier personnalisé possède un plug-in de conversion par défaut et deux autres plug-ins de conversion. Les entrées de Registre sous la sous-clé **ConvertPluginCLSID** se présentent sous la forme suivante.



| Nom                                                                          | Type        | Valeur                                                                |
|-------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------|
| Default                                                                       | **SZ de REG \_** | ID de classe, au format de Registre, du plug-in de conversion par défaut. |
| ID de classe, au format de Registre, du plug-in de conversion par défaut.          | **SZ de REG \_** | Nom convivial du plug-in de conversion par défaut.                 |
| ID de classe, au format de Registre, du premier plug-in de conversion.  | **SZ de REG \_** | Nom convivial du premier plug-in de conversion.         |
| ID de classe, au format de Registre, du deuxième plug-in de conversion. | **SZ de REG \_** | Nom convivial du deuxième plug-in de conversion.        |



 

Notez que le plug-in de conversion par défaut est représenté par deux entrées de Registre : l’entrée par défaut et une entrée nommée. Le lecteur Windows Media utilise l’entrée par défaut pour déterminer quel plug-in est le plug-in de conversion par défaut (principal). Le lecteur Windows Media utilise les entrées nommées pour obtenir des noms conviviaux pour tous les plug-ins de conversion, y compris le plug-in par défaut.

Le nom convivial d’un plug-in de conversion est déterminé par la société qui crée le plug-in. Le lecteur Windows Media peut afficher le nom convivial dans son interface utilisateur.

Lorsque le lecteur Windows Media tente de convertir un fichier d’un format personnalisé vers un format standard, il commence par charger le plug-in par défaut. Si le plug-in par défaut ne parvient pas à convertir le fichier et retourne le plug-in de conversion du plug-in NS \_ E \_ WMP \_ \_ \_ \_ \_ , le lecteur charge chaque plug-in jusqu’à ce qu’une conversion réussisse ou qu’il n’y ait plus de plug-ins à essayer. Le lecteur n’affiche pas de message d’avertissement si aucun plug-in de conversion n’est trouvé pour l’extension de nom de fichier.

L’entrée de Registre **ConvertPluginCLSID** est prise en charge par le lecteur Windows Media 11.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Paramètres de registre de l’extension de nom de fichier**](file-name-extension-registry-settings.md)
</dt> <dt>

[**Plug-ins de conversion du lecteur Windows Media**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




