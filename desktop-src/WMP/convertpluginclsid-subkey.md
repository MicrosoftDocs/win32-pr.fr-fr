---
title: Sous-clé ConvertPluginCLSID
description: Sous-clé ConvertPluginCLSID
ms.assetid: 2bf5b6ad-31e9-40c2-a682-c7ad813e8f7a
keywords:
- Lecteur Windows Media, sous-clé ConvertPluginCLSID
- Lecteur Windows Media, extensions de nom de fichier
- Lecteur Windows Media, registre
- Registre, extensions de noms de fichiers
- Registre, sous-clé ConvertPluginCLSID
- registre, paramètres pour Lecteur Windows Media
- paramètres de registre de l’extension de nom de fichier
- Sous-clé ConvertPluginCLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5deeda3e7eb0b5fe465152aa7711717d086c94a06ebed4f9549dc9f6a9b62dd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341663"
---
# <a name="convertpluginclsid-subkey"></a>Sous-clé ConvertPluginCLSID

lorsque Lecteur Windows Media 11 rencontre une extension de nom de fichier personnalisée, il recherche une sous-clé de registre qui correspond à l’extension. la sous-clé est décrite dans la [Paramètres du registre](file-name-extension-registry-settings.md)de l’Extension de nom de fichier. Dans certains cas, la sous-clé de l’extension a une sous-clé nommée **ConvertPluginCLSID**.

par exemple, supposons que vous avez créé un format de fichier personnalisé (avec l’extension de nom de fichier. xyz) et un plug-in de conversion qui convertit les fichiers dans un format pris en charge par Lecteur Windows Media vous stockiez l’ID de classe du plug-in dans l’une ou les deux sous-clés suivantes.

**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Multimedia \\ wmplayer \\ extensions \\ . xyz \\ ConvertPluginCLSID**

**HKEY \_ Current \_ User \\ Software \\ \\ extensions Microsoft \\ MediaPlayer \\ Player \\ . xyz \\ ConvertPluginCLSID**

la sous-clé **ConvertPluginCLSID** spécifie les id de classe des plug-ins que Lecteur Windows Media pouvez utiliser pour convertir un fichier multimédia à partir de son format personnalisé vers un format pris en charge par le lecteur.

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



 

Notez que le plug-in de conversion par défaut est représenté par deux entrées de Registre : l’entrée par défaut et une entrée nommée. Lecteur Windows Media utilise l’entrée par défaut pour déterminer quel plug-in est le plug-in de conversion par défaut (principal). Lecteur Windows Media utilise les entrées nommées pour obtenir des noms conviviaux pour tous les plug-ins de conversion, y compris le plug-in par défaut.

Le nom convivial d’un plug-in de conversion est déterminé par la société qui crée le plug-in. Lecteur Windows Media pouvez afficher le nom convivial dans son interface utilisateur.

lorsque Lecteur Windows Media tente de convertir un fichier d’un format personnalisé vers un format standard, il commence par charger le plug-in par défaut. Si le plug-in par défaut ne parvient pas à convertir le fichier et retourne le plug-in de conversion du plug-in NS \_ E \_ WMP \_ \_ \_ \_ \_ , le lecteur charge chaque plug-in jusqu’à ce qu’une conversion réussisse ou qu’il n’y ait plus de plug-ins à essayer. Le lecteur n’affiche pas de message d’avertissement si aucun plug-in de conversion n’est trouvé pour l’extension de nom de fichier.

l’entrée de registre **ConvertPluginCLSID** est prise en charge par Lecteur Windows Media 11.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Paramètres de registre de l’Extension de nom de fichier**](file-name-extension-registry-settings.md)
</dt> <dt>

[**Lecteur Windows Media Plug-ins de conversion**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




