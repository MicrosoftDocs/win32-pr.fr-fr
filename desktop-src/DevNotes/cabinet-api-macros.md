---
description: En savoir plus sur les macros de l’API cab
ms.assetid: 85fade43-9fcb-4100-a734-8b36d132b2c0
title: Macros de l’API Cabinet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390fa42e0293e5d47c405e8e99986538b8f26254
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522868"
---
# <a name="cabinet-api-macros"></a>Macros de l’API Cabinet

Cette section détaille les macros utilisées par l’API CAB :

## <a name="fci-macros"></a>FCI, macros

Les macros suivantes sont utilisées par FCI :



| Macro                                              | Description                                                                                    |
|----------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**FNFCIALLOC**](/windows/desktop/api/fci/nf-fci-fnfcialloc)                   | Utilisé pour allouer de la mémoire dans un contexte FCI.<br/>                                          |
| [**FNFCICLOSE**](/windows/desktop/api/fci/nf-fci-fnfciclose)                   | Utilisé pour fermer un fichier.<br/>                                                               |
| [**FNFCIDELETE**](/windows/desktop/api/fci/nf-fci-fnfcidelete)                 | Utilisé pour supprimer un fichier.<br/>                                                              |
| [**FNFCIFILEPLACED**](/windows/desktop/api/fci/nf-fci-fnfcifileplaced)         | Utilisé pour notifier quand un fichier est placé dans le fichier CAB.<br/>                                |
| [**FNFCIFREE**](/windows/desktop/api/fci/nf-fci-fnfcifree)                     | Utilisé pour libérer de la mémoire précédemment allouée dans un contexte FCI.<br/>                         |
| [**FNFCIGETNEXTCABINET**](/windows/desktop/api/fci/nf-fci-fnfcigetnextcabinet) | Utilisé pour demander des informations pour le prochain Cabinet.<br/>                                   |
| [**FNFCIGETOPENINFO**](/windows/desktop/api/fci/nf-fci-fnfcigetopeninfo)       | Permet d’ouvrir un fichier et de récupérer la date, l’heure et les attributs d’un fichier.<br/>                   |
| [**FNFCIGETTEMPFILE**](/windows/desktop/api/fci/nf-fci-fnfcigettempfile)       | Utilisé pour obtenir un nom de fichier temporaire.<br/>                                               |
| [**FNFCIOPEN**](/windows/desktop/api/fci/nf-fci-fnfciopen)                     | Utilisé pour ouvrir un fichier dans un contexte FCI.<br/>                                              |
| [**FNFCIREAD**](/windows/desktop/api/fci/nf-fci-fnfciread)                     | Utilisé pour lire les données d’un fichier.<br/>                                                      |
| [**FNFCISEEK**](/windows/desktop/api/fci/nf-fci-fnfciseek)                     | Utilisé pour déplacer un pointeur de fichier vers un emplacement spécifié.<br/>                                |
| [**FNFCISTATUS**](/windows/desktop/api/fci/nf-fci-fnfcistatus)                 | Utilisé pour mettre à jour l’utilisateur.<br/>                                                            |
| [**FNFCIWRITE**](/windows/desktop/api/fci/nf-fci-fnfciwrite)                   | Utilisé pour écrire des données dans un fichier.<br/>                                                       |
| [**TCOMPfromLZXWindow**](/windows/desktop/api/fdi_fci_types/nf-fdi_fci_types-tcompfromlzxwindow)   | Convertit la taille Windows en valeur LXZ TCOMP pour [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile).<br/> |



 

## <a name="fdi-macros"></a>FDI, macros

Les macros suivantes sont utilisées par FDI :



| Macro                              | Description                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [**FNALLOC**](/windows/desktop/api/fdi/nf-fdi-fnalloc)         | Utilisé pour allouer de la mémoire dans un contexte FDI.<br/>                               |
| [**FNCLOSE**](/windows/desktop/api/fdi/nf-fdi-fnclose)         | Utilisé pour fermer un fichier dans un contexte FDI.<br/>                                  |
| [**FNFDINOTIFY**](/windows/desktop/api/fdi/nf-fdi-fnfdinotify) | Utilisé pour mettre à jour l’application sur l’état du décodeur.<br/>             |
| [**FNFREE**](/windows/desktop/api/fdi/nf-fdi-fnfree)           | Utilisé pour libérer de la mémoire précédemment allouée dans un contexte FDI.<br/>              |
| [**FNOPEN**](/windows/desktop/api/fdi/nf-fdi-fnopen)           | Utilisé pour ouvrir un fichier dans un contexte FDI.<br/>                                   |
| [**FNREAD**](/windows/desktop/api/fdi/nf-fdi-fnread)           | Utilisé pour lire les données d’un fichier dans un contexte FDI.<br/>                         |
| [**FNSEEK**](/windows/desktop/api/fdi/nf-fdi-fnseek)           | Utilisé pour déplacer un pointeur de fichier vers l’emplacement spécifié dans un contexte FDI.<br/> |
| [**FNWRITE**](/windows/desktop/api/fdi/nf-fdi-fnwrite)         | Utilisé pour écrire des données dans un fichier dans un contexte FDI.<br/>                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de l’API cab](cabinet-api-reference.md)
</dt> <dt>

[Utilisation de l’API Cabinet](using-the-cabinet-api.md)
</dt> </dl>

 

 




