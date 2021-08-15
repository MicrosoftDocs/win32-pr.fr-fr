---
description: Inscription de votre gestionnaire de feuille de propriétés
ms.assetid: 6621529c-717b-4f36-8d9e-769d6b720b8a
title: Inscription de votre gestionnaire de feuille de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91f1642c03a068a24b37cd5647bcdef63222ed2dbe5d78832daeea31e8abd67d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083533"
---
# <a name="registering-your-property-sheet-handler"></a>Inscription de votre gestionnaire de feuille de propriétés

pour que votre gestionnaire de feuille de propriétés soit reconnu par l’espace de noms WPD, vous devez l’inscrire correctement dans le registre Windows. Les entrées d’inscription pour un gestionnaire de feuille de propriétés WPD sont similaires à celles de l’interpréteur de commandes, mais elles sont inscrites en tant que types de fichier spéciaux. Les gestionnaires de la feuille de propriétés WPD sont inscrits en fonction du type de contenu qu’ils représentent. Voici un exemple d’arborescence d’inscription pour un gestionnaire de menu contextuel WPD :


```C++
HKEY_CLASSES_ROOT
 \-- WPDPropSheet.Image
      \-- shellex
           \-- PropertySheetHandlers
                \-- MyHandler (Default)  REG_SZ {0000000-0000-0000-0000-000000000000}

```



L’exemple ci-dessus inscrit un gestionnaire personnalisé avec l’espace de noms WPD. quand un utilisateur clique avec le bouton droit sur un fichier image sur un appareil via l’interpréteur de Windows et sélectionne des **propriétés**, il appelle ce gestionnaire de feuille de propriétés. L’espace de noms WPD utilise \_ le \_ type de contenu wpd pour déterminer les gestionnaires de feuille de propriétés à charger. Si le type de contenu ne fournit pas de classification utile, l’espace de noms chargera les gestionnaires de feuille de propriétés sous la clé de **Registre WPDPropSheet. Generic** . Le tableau suivant répertorie toutes les classes de fichiers disponibles pour un gestionnaire de menu contextuel, ainsi que les types de contenu et les extensions de fichier qu’ils représentent.



| Clé de Registre                   | Type de contenu WPD                                                                                                               |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| **WPDContextMenu. appareil**      | L’inscription sous cette clé active votre gestionnaire de menu contextuel au niveau de l’appareil. (Cliquez avec le bouton droit sur un appareil).                   |
| **WPDContextMenu. Stockage**     | L’inscription sous cette clé active votre gestionnaire de menu contextuel au niveau du stockage. (Cliquez avec le bouton droit sur un stockage.)                 |
| **WPDContextMenu. dossier**      | \_dossier de \_ type de contenu wpd \_                                                                                                     |
| **WPDContextMenu. image**       | \_image de \_ type de contenu wpd \_                                                                                                      |
| **WPDContextMenu. audio**       | \_type de contenu wpd \_ \_ audio                                                                                                      |
| **WPDContextMenu. vidéo**       | vidéo sur le \_ type de contenu wpd \_ \_                                                                                                      |
| **WPDContextMenu. playlist**    | \_playlist de \_ type de contenu wpd \_                                                                                                   |
| **WPDContextMenu.Document**    | \_document de \_ type de contenu wpd \_                                                                                                   |
| **WPDContextMenu. contact**     | \_contact de \_ type de contenu wpd \_                                                                                                    |
| **WPDContextMenu.Email**       | \_e-mail de \_ type de contenu wpd \_                                                                                                      |
| **WPDContextMenu. rendez-vous** | \_ \_ rendez-vous de type de contenu wpd \_                                                                                                |
| **WPDContextMenu. tâche**        | \_tâche de \_ type de contenu wpd \_                                                                                                       |
| **WPDContextMenu. MEMO**        | \_mémo de \_ type de contenu wpd \_                                                                                                       |
| **WPDContextMenu.ImageAlbum**  | \_album d' \_ images de type de contenu wpd \_ \_                                                                                               |
| **WPDContextMenu.AudioAlbum**  | TYPE de contenu WPD- \_ \_ \_ \_ album audio                                                                                               |
| **WPDContextMenu.VideoAlbum**  | \_ \_ album vidéo de type de contenu wpd \_ \_                                                                                               |
| **WPDContextMenu.MixedAlbum**  | TYPE de contenu WPD- \_ \_ \_ album de \_ contenu mixte \_                                                                                      |
| **WPDContextMenu. Generic**     | \_type de contenu wpd \_ \_ non spécifié<br/> \_ \_ fichier générique du type de contenu wpd \_ \_<br/> \_programme de \_ type de contenu wpd \_<br/> |



 

 

 




