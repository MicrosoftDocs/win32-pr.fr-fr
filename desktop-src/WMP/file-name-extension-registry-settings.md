---
title: Paramètres de registre de l’Extension de nom de fichier
description: Paramètres de registre de l’Extension de nom de fichier
ms.assetid: a5c31cf7-e1e1-4f1a-8e94-ed08f99ad973
keywords:
- Lecteur Windows Media, registre
- Lecteur Windows Media, extensions de nom de fichier
- Registre, extensions de noms de fichiers
- registre, paramètres pour Lecteur Windows Media
- paramètres de registre de l’extension de nom de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c526e38ae1b2b76b942e0646df6f8aaa3b8e3417
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192276"
---
# <a name="file-name-extension-registry-settings"></a>Paramètres de registre de l’Extension de nom de fichier

si vos fichiers multimédias numériques ont un format personnalisé, vous pouvez fournir Lecteur Windows Media avec des informations sur votre format personnalisé en plaçant des entrées dans le registre sur l’ordinateur de l’utilisateur. Lecteur Windows Media inspecte vos entrées de registre pour déterminer comment il doit gérer vos fichiers. La liste suivante présente plusieurs des opérations que vous pouvez effectuer en créant des entrées de Registre relatives à votre format de fichier multimédia personnalisé.

-   Accordez l’autorisation au lecteur de lire, copier ou transcoder vos fichiers.
-   Spécifiez la technologie sous-jacente que le lecteur doit utiliser pour lire vos fichiers.
-   Spécifiez l’emplacement où le joueur doit afficher vos fichiers dans sa vue bibliothèque.
-   Spécifiez un plug-in que le lecteur doit utiliser pour convertir vos fichiers dans un format standard.
-   Spécifiez un code de format MTP (Media Transport Protocol) que le joueur peut utiliser pour déterminer si un périphérique portable particulier prend en charge votre format de fichier.

La plupart des entrées que vous fournissez se trouvent sous une sous-clé associée à votre extension de nom de fichier personnalisée. Vous pouvez créer cette sous-arborescence dans la sous-arborescence de l' \_ ordinateur local HKEY \_ et dans la sous-arborescence de l' \_ utilisateur actuel HKEY \_ . Lecteur Windows Media recherche d’abord dans la sous-arborescence de la \_ MACHINE locale HKEY \_ . S’il ne trouve pas ce dont il a besoin, il regarde dans la sous-arborescence de la sous-arborescence de l' \_ \_ utilisateur actuel. Notez que tout code qui tente d’écrire dans le registre sur l’ordinateur de l’utilisateur peut écrire dans la sous-arborescence de l' \_ ordinateur local HKEY \_ uniquement si l’utilisateur actuel dispose de privilèges d’administrateur.

Pour écrire des informations sur votre format de fichier personnalisé dans \_ la \_ sous-arborescence de l’ordinateur local HKEY, créez la sous-clé suivante.

**HKEY \_ Logiciel de l' \_ ordinateur local \\ \\ Microsoft \\ Multimedia \\ wmplayer \\ \\ Extensions** *customExtension*

où *customExtension* est l’extension de nom de fichier, y compris le séparateur de points (.). Par exemple, si l’extension de votre format de fichier personnalisé est. xyz, créez la sous-clé suivante.

**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Multimedia \\ wmplayer \\ extensions \\ . xyz**

Pour écrire des informations sur votre format de fichier personnalisé dans \_ la \_ sous-arborescence de l’utilisateur actuel HKEY, créez la sous-clé suivante.

**HKEY \_ \_Logiciel utilisateur \\ actuel \\ \\ \\ \\ extensions \\ de lecteur Microsoft MediaPlayer** 

Vous pouvez écrire une ou plusieurs des entrées suivantes dans votre sous-clé *customExtension* .

-   **autorisations**
-   **Runtime**
-   **FormatCode**

Pour spécifier des plug-ins de conversion pour votre format de fichier multimédia personnalisé, créez une sous-clé **ConvertPluginCLSID** dans votre sous-clé *customExtension* .

pour spécifier l’emplacement où les Lecteur Windows Media doivent afficher vos fichiers dans la vue bibliothèque, écrivez une entrée qui représente votre format de fichier personnalisé dans la sous-clé suivante.

**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ MediaPlayer \\ MLS \\ Extensions**

les rubriques suivantes décrivent les sous-clés et les entrées de registre qui fournissent des Lecteur Windows Media avec des informations sur les formats de fichiers multimédias personnalisés.

-   [Entrée de registre des autorisations](permissions-registry-entry.md)
-   [Entrée du Registre du Runtime](runtime-registry-entry.md)
-   [Entrée de Registre FormatCode](formatcode-registry-entry.md)
-   [Entrées de registre de classification de bibliothèque](library-classification-registry-entries.md)
-   [Sous-clé ConvertPluginCLSID](convertpluginclsid-subkey.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Paramètres du Registre**](registry-settings.md)
</dt> <dt>

[**Lecteur Windows Media Plug-ins de conversion**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




