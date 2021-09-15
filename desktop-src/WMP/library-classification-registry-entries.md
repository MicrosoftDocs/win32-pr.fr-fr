---
title: Entrées de registre de classification de bibliothèque
description: Entrées de registre de classification de bibliothèque
ms.assetid: 3ef7d384-503f-4b8f-9f4b-e0ef3c56616b
keywords:
- Lecteur Windows Media, bibliothèque
- Lecteur Windows Media, entrées de registre de classification
- Lecteur Windows Media, extensions de nom de fichier
- Lecteur Windows Media, registre
- Registre, extensions de noms de fichiers
- Registre, entrées de classification de bibliothèque
- registre, paramètres pour Lecteur Windows Media
- paramètres de registre de l’extension de nom de fichier
- bibliothèque, entrées de registre de classification
- bibliothèque, registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48ea1aacdd1e4c553a7e83bfdd711ff331c0878
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295126"
---
# <a name="library-classification-registry-entries"></a>Entrées de registre de classification de bibliothèque

lorsque Lecteur Windows Media rencontre un fichier multimédia qui a une extension de nom de fichier personnalisée, il ne sait pas si le fichier doit être classé comme audio, vidéo ou tout autre type. par défaut, Lecteur Windows Media place ces fichiers dans l’autre partie média de la bibliothèque.

si vos fichiers multimédias numériques ont un format personnalisé, vous pouvez fournir à Lecteur Windows Media des informations sur l’emplacement où vos fichiers doivent apparaître dans la bibliothèque du lecteur en plaçant deux entrées dans le registre sur l’ordinateur de l’utilisateur.

Une entrée est insérée dans la sous-clé suivante.

**HKEY \_ local \_ machine \\ Software \\ Microsoft \\ MediaPlayer \\ MLS \\ Extensions**

L’entrée de registre a le format suivant.



| Nom                                                  | Type de données   | Valeur                                      |
|-------------------------------------------------------|-------------|--------------------------------------------|
| L’extension de nom de fichier sans séparateur de points (.) | **SZ de REG \_** | Chaîne qui spécifie un emplacement de bibliothèque |



 

L’autre entrée de Registre est insérée dans la sous-clé suivante que vous créez.

**HKEY \_ CLASSES \_ racine \\** *customExtension*

où *customExtension* est l’extension de nom de fichier, y compris le séparateur de points (.).

L’entrée de registre a le format suivant.



| Nom          | Type de données   | Valeur                                      |
|---------------|-------------|--------------------------------------------|
| PerceivedType | **SZ de REG \_** | Chaîne qui spécifie un emplacement de bibliothèque |



 

Les deux entrées de Registre doivent avoir la même valeur. Les valeurs possibles sont indiquées dans le tableau suivant.



| Valeur | Description                                                                      |
|-------|----------------------------------------------------------------------------------|
| audio | Les fichiers qui ont l’extension personnalisée s’affichent dans la partie musique de la bibliothèque. |
| video | Les fichiers qui ont l’extension personnalisée s’affichent dans la partie vidéo de la bibliothèque. |



 

Par exemple, les entrées de Registre suivantes spécifient que les fichiers portant l’extension de nom de fichier. xyz s’afficheront dans la partie musique de la bibliothèque :


```C++

HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\MLS\Extensions
    xyz     REG_SZ     audio

HKEY_CLASSES_ROOT\.xyz
    PerceivedType     REG_SZ     audio

```



Notez que tout code qui tente d’écrire dans le registre sur l’ordinateur de l’utilisateur peut écrire dans la sous-arborescence de l' \_ ordinateur local HKEY \_ uniquement si l’utilisateur actuel dispose de privilèges d’administrateur.

les entrées de registre de classification de bibliothèque sont prises en charge par les versions suivantes de Lecteur Windows Media.

-   Lecteur Windows Media série 9 avec le correctif 823275
-   Lecteur Windows Media 10 et versions ultérieures

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Paramètres de registre de l’Extension de nom de fichier**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




