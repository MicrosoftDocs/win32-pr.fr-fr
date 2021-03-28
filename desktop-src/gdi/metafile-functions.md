---
description: Les fonctions suivantes sont utilisées avec les sous-fichiers de format amélioré.
ms.assetid: 93a17a8c-308b-4442-933e-fedc8b9a84b0
title: Fonctions de métafichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd137095fe0659871291ec4e8670054cc2899d10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528317"
---
# <a name="metafile-functions"></a>Fonctions de métafichier

Les fonctions suivantes sont utilisées avec les sous-fichiers de format amélioré.



| Fonction                                                             | Description                                                                                                            |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**CloseEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-closeenhmetafile)                         | Ferme un contexte de périphérique de métafichier amélioré.                                                                            |
| [**CopyEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-copyenhmetafilea)                           | Copie le contenu d’un métafichier de format amélioré dans un fichier spécifié.                                                |
| [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea)                       | Crée un contexte de périphérique pour un métafichier de format amélioré.                                                              |
| [**DeleteEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-deleteenhmetafile)                       | Supprime un métafichier de format amélioré ou un handle de métafichier de format amélioré.                                             |
| [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc)                           | Fonction de rappel définie par l’application utilisée avec la fonction EnumEnhMetaFile.                                       |
| [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile)                           | Énumère les enregistrements dans un métafichier de format amélioré.                                                             |
| [**GdiComment**](/windows/desktop/api/Wingdi/nf-wingdi-gdicomment)                                     | Copie un commentaire d’une mémoire tampon dans un métafichier de format amélioré spécifié.                                              |
| [**GetEnhMetaFile**](/windows/desktop/api/WinGdi/nf-wingdi-getenhmetafilea)                             | Crée un handle qui identifie le métafichier de format amélioré stocké dans le fichier spécifié.                            |
| [**GetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilebits)                     | Récupère le contenu du métafichier de format amélioré spécifié et le copie dans une mémoire tampon.                        |
| [**GetEnhMetaFileDescription**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafiledescriptiona)       | Récupère une description de texte facultative à partir d’un métafichier de format amélioré et copie la chaîne dans la mémoire tampon spécifiée. |
| [**GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader)                 | Récupère l’enregistrement contenant l’en-tête pour le métafichier de format amélioré spécifié.                                 |
| [**GetEnhMetaFilePaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilepaletteentries) | Récupère les entrées de palette facultatives du métafichier amélioré spécifié.                                               |
| [**GetMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-getmetafilea)                                   | GetMetaFile n’est plus disponible pour une utilisation à partir de Windows 2000. Utilisez plutôt [**GetEnhMetaFile**](/windows/desktop/api/WinGdi/nf-wingdi-getenhmetafilea).  |
| [**GetWinMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-getwinmetafilebits)                     | Convertit les enregistrements de format amélioré d’un métafichier en enregistrements de format Windows.                                      |
| [**PlayEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile)                           | Affiche l’image stockée dans le métafichier de format amélioré spécifié.                                                 |
| [**PlayEnhMetaFileRecord**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafilerecord)               | Lit un enregistrement de métafichier amélioré en exécutant les fonctions GDI (Graphics Device Interface) identifiées par l’enregistrement. |
| [**SetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-setenhmetafilebits)                     | Crée un métafichier de format amélioré basé sur la mémoire à partir des données spécifiées.                                               |
| [**SetWinMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-setwinmetafilebits)                     | Convertit un métafichier de l’ancien format Windows au nouveau format amélioré.                                          |



 

## <a name="obsolete-functions"></a>Fonctions obsolètes

Les fonctions suivantes sont obsolètes. Le sont fournis pour la compatibilité avec les fichiers de format Windows.

-   [**CloseMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-closemetafile)
-   [**CopyMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-copymetafilea)
-   [**CreateMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createmetafilea)
-   [**DeleteMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-deletemetafile)
-   [**EnumMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enummetafile)
-   [**EnumMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-mfenumproc)
-   [**GetMetaFileBitsEx**](/windows/desktop/api/Wingdi/nf-wingdi-getmetafilebitsex)
-   [**PlayMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playmetafile)
-   [**PlayMetaFileRecord**](/windows/desktop/api/Wingdi/nf-wingdi-playmetafilerecord)
-   [**SetMetaFileBitsEx**](/windows/desktop/api/Wingdi/nf-wingdi-setmetafilebitsex)

 

 
