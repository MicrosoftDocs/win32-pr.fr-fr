---
title: Modification Flux
description: Modification Flux
ms.assetid: 1653ff90-e96a-43fc-b509-6d8ad4ddcd2c
keywords:
- CreateEditableStream fonction)
- EditStreamCut fonction)
- EditStreamCopy fonction)
- EditStreamPaste fonction)
- EditStreamClone fonction)
- EditStreamSetInfo fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29eb687eb36ff9dfe0b1d3477bff095bdd78a135
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239777"
---
# <a name="editing-streams"></a>Modification Flux

Vous pouvez créer un flux que vous pouvez modifier à l’aide de la fonction [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) . Cette fonction initialise l’environnement pour la modification d’un flux. Cela comprend la création d’une interface pour le nouveau flux et les tables de modification internes qui effectuent le suivi des modifications apportées au flux. **CreateEditableStream** retourne un pointeur de flux vers un flux modifiable requis par d’autres fonctions de modification de flux. Le pointeur de flux modifiable peut également être utilisé par d’autres fonctions AVIFile qui acceptent des pointeurs de flux.

Vous pouvez couper un ou plusieurs échantillons d’un flux modifiable à l’aide de la fonction [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) . Pour supprimer des exemples du flux modifiable, cette fonction ajoute une entrée à la table de modification. La fonction place ensuite une copie des exemples coupés dans un nouveau flux temporaire dont le pointeur d’interface est retourné dans une variable.

Vous pouvez copier un ou plusieurs échantillons d’un flux modifiable dans un flux temporaire à l’aide de la fonction [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) . **EditStreamCopy** place des copies des exemples dans un nouveau flux temporaire dont le pointeur d’interface est retourné dans une variable.

Vous pouvez copier un ou plusieurs échantillons à partir d’un flux et les coller dans un flux modifiable à l’aide de la fonction [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) . Pour insérer les exemples à la position spécifiée, cette fonction ajoute une entrée dans la table de modification du flux modifiable cible.

Vous pouvez dupliquer un flux modifiable à l’aide de la fonction [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) . Cette fonction retourne un pointeur vers l’interface de flux du nouveau flux. Vous pouvez copier ces flux dans le presse-papiers ou les utiliser pour conserver une trace des modifications apportées à un flux.

Vous pouvez modifier plusieurs caractéristiques d’un flux modifiable à l’aide de la fonction [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) . Cette fonction met à jour le paramètre de priorité, la langue, l’échelle et le taux, l’heure de début, le paramètre de qualité, les dimensions et les coordonnées du rectangle de destination, ainsi que la description textuelle du flux. Ces éléments sont stockés dans la structure [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) associée au flux modifiable.

Vous pouvez également modifier la description textuelle d’un flux modifiable à l’aide de la fonction [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) . Cette fonction met à jour le membre **szName** de la structure **AVISTREAMINFO** associée au flux modifiable.

Les fonctions d’édition fonctionnent sur les flux. Vous devez couper et coller chaque flux individuellement, puis utiliser la fonction [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) pour créer un nouveau pointeur de fichier.

> [!Note]  
> La modification des tables dans un flux modifiable conserve toutes les modifications apportées à un flux. Le flux source n’est jamais modifié.

 

 

 




