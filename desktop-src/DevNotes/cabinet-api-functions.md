---
description: 'En savoir plus sur : fonctions de l’API cab'
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: Fonctions de l’API Cabinet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b08234a47c84a604c78275632d88be2bcdeef68e47fd092bbf50e4d97dcf925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668353"
---
# <a name="cabinet-api-functions"></a>Fonctions de l’API Cabinet

Cette section décrit les fonctions suivantes de l’API CAB :

## <a name="fci-functions"></a>FCI, fonctions

La bibliothèque FCI (file compression interface) offre la possibilité de créer des armoires (également appelées « fichiers CAB »). En outre, la bibliothèque fournit la compression pour réduire la taille des données de fichier stockées dans les armoires.



| Fonction                                   | Description                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | Ajoute un fichier au fichier CAB actuellement construit.<br/>                                           |
| [**FCICreate**](/windows/desktop/api/Fci/nf-fci-fcicreate)             | Crée un contexte FCI.<br/>                                                                          |
| [**FCIDestroy**](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | Supprime un contexte FCI ouvert, libérant de la mémoire et des fichiers temporaires associés au contexte.<br/> |
| [**FCIFlushCabinet**](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | Termine le fichier CAB actuel.<br/>                                                                   |
| [**FCIFlushFolder**](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | Force l’exécution immédiate du dossier actif en cours de construction.<br/>                        |



 

## <a name="fdi-functions"></a>Fonctions FDI

La bibliothèque FDI (file Decompression interface) offre la possibilité d’extraire des fichiers des armoires.



| Fonction                                         | Description                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**FDICopy**](/windows/desktop/api/Fdi/nf-fdi-fdicopy)                       | Extrait des fichiers des armoires.<br/>                                                          |
| [**FDICreate**](/windows/desktop/api/Fdi/nf-fdi-fdicreate)                   | Crée un contexte FDI.<br/>                                                                |
| [**FDIDestroy**](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)                 | Supprime un contexte FDI ouvert.<br/>                                                           |
| [**FDIIsCabinet**](/windows/desktop/api/Fdi/nf-fdi-fdiiscabinet)             | Détermine si un fichier est un fichier CAB et, si c’est le cas, retourne des informations descriptives.<br/> |
| [**FDITruncateCabinet**](/windows/desktop/api/Fdi/nf-fdi-fditruncatecabinet) | Tronque un fichier CAB en commençant au numéro de dossier spécifié.<br/>                      |



 

## <a name="deprecated-functions"></a>Fonctions dépréciées

-   [**DeleteExtractedFiles**](deleteextractedfiles.md)
-   [**DllGetVersion**](dllgetversion.md)
-   [**Extract**](extract.md)
-   [**GetDllVersion**](getdllversion.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de l’API cab](cabinet-api-reference.md)
</dt> <dt>

[Utilisation de l’API Cabinet](using-the-cabinet-api.md)
</dt> </dl>

 

 




