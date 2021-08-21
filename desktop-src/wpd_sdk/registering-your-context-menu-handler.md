---
description: Inscription de votre gestionnaire de menu contextuel
ms.assetid: 0023004b-b6b3-486a-8b8c-8e63c5731206
title: Inscription de votre gestionnaire de menu contextuel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 027e01d4b3bc58727579b77345d3f1b8eed668e5b858e49eb4859a40db9ad2d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083543"
---
# <a name="registering-your-context-menu-handler"></a>Inscription de votre gestionnaire de menu contextuel

pour que votre gestionnaire de menu contextuel soit reconnu par l’espace de noms WPD, vous devez l’inscrire correctement dans le registre Windows. Les entrées d’inscription pour un gestionnaire de menu contextuel WPD sont similaires à celles de l’interpréteur de commandes, mais elles sont inscrites en tant que types de fichier spéciaux. Les gestionnaires de menus contextuels WPD sont inscrits en fonction du type de contenu qu’ils représentent. Voici un exemple d’arborescence d’inscription pour un gestionnaire de menu contextuel WPD :


```C++
HKEY_CLASSES_ROOT
 \-- WPDContextMenu.Image
      \-- shellex
           \-- ContextMenuHandlers
                \-- ShImageViewer (Default)  REG_SZ {E847DA7C-1D6A-45F6-B725-CB260C236066}

```



L’exemple ci-dessus inscrit la visionneuse d’images de Shell avec l’espace de noms WPD. quand un utilisateur clique avec le bouton droit ou double-clique sur du contenu sur un appareil via l’interpréteur de commandes Windows Vista, il appelle ce gestionnaire de menu contextuel. L’espace de noms WPD utilise le \_ \_ type de contenu wpd pour déterminer les gestionnaires de menus contextuels à charger. Si le type de contenu wpd \_ \_ est égal au \_ type de contenu wpd \_ \_ non spécifié, le type de contenu wpd \_ ou le \_ \_ \_ \_ programme de type de contenu wpd \_ \_ , l’espace de noms wpd tente de trouver la meilleure correspondance en fonction de l’extension du fichier sélectionné. Si ni l’extension de fichier ni le type de contenu n’offrent une classification utile, l’espace de noms WPD chargera les gestionnaires de menus contextuels sous la clé de Registre **WPDContextMenu. Generic** . Le tableau suivant répertorie toutes les classes de fichiers disponibles pour un gestionnaire de menu contextuel, ainsi que les types de contenu et les extensions de fichier qu’ils représentent :



| Clé de Registre                           | Type de contenu WPD                                                                                               | Extension de fichier                                                                                           |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| **WPDContextMenu. appareil**              | L’inscription sous cette clé active votre gestionnaire de menu contextuel au niveau de l’appareil. (Cliquez avec le bouton droit sur un appareil).   | (N/A)                                                                                                    |
| **WPDContextMenu. Stockage**             | L’inscription sous cette clé active votre gestionnaire de menu contextuel au niveau du stockage. (Cliquez avec le bouton droit sur un stockage.) | (N/A)                                                                                                    |
| **WPDContextMenu. dossier**              | \_dossier de \_ type de contenu wpd \_                                                                                     | (N/A)                                                                                                    |
| **WPDContextMenu. image**               | \_image de \_ type de contenu wpd \_                                                                                      | .bmp <br/> .gif <br/> .png <br/> .jpg <br/> .jpe <br/> .jpeg <br/>   |
| **WPDContextMenu. audio**               | \_type de contenu wpd \_ \_ audio                                                                                      | .aiff <br/> .mp3 <br/> .wav <br/> .wma <br/>                                     |
| **WPDContextMenu. vidéo**               | vidéo sur le \_ type de contenu wpd \_ \_                                                                                      | .asf<br/> .avi <br/> . DVR-MS <br/> .mpeg <br/> .mpg <br/> .wmv <br/> |
| **WPDContextMenu. playlist**<br/> | \_playlist de \_ type de contenu wpd \_                                                                                   | . wpl <br/> .m3u <br/> .mpl <br/> .asx <br/> . Patientez <br/>                     |
| **WPDContextMenu.Document**            | \_document de \_ type de contenu wpd \_                                                                                   | .doc <br/> .txt <br/> .rtf <br/> .xls <br/> .ppt <br/>                     |
| **WPDContextMenu. contact**<br/>  | \_contact de \_ type de contenu wpd \_                                                                                    | Aucun                                                                                                     |
| **WPDContextMenu.Email**               | \_e-mail de \_ type de contenu wpd \_                                                                                      | Aucun                                                                                                     |
| **WPDContextMenu. rendez-vous**         | \_ \_ rendez-vous de type de contenu wpd \_                                                                                | Aucun                                                                                                     |
| **WPDContextMenu. tâche**                | \_tâche de \_ type de contenu wpd \_                                                                                       | Aucun                                                                                                     |
| **WPDContextMenu. MEMO**                | \_mémo de \_ type de contenu wpd \_                                                                                       | Aucun                                                                                                     |
| **WPDContextMenu.ImageAlbum**          | \_album d' \_ images de type de contenu wpd \_ \_                                                                               | Aucun                                                                                                     |
| **WPDContextMenu.AudioAlbum**          | TYPE de contenu WPD- \_ \_ \_ \_ album audio                                                                               | Aucun                                                                                                     |
| **WPDContextMenu.VideoAlbum**          | \_ \_ album vidéo de type de contenu wpd \_ \_                                                                               | Aucun                                                                                                     |
| **WPDContextMenu.MixedAlbum**          | TYPE de contenu WPD- \_ \_ \_ album de \_ contenu mixte \_                                                                      | Aucun                                                                                                     |
| **WPDContextMenu. Generic**             | \_type de contenu wpd \_ \_ non spécifié                                                                                | Toutes les autres extensions de fichier                                                                                |



 

 

 




