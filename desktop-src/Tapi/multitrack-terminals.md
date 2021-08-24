---
description: TAPI 3,1 introduit la notion de terminal multipiste, un terminal qui, par essence, est une collection de &\# 0034 ; track&\# 0034 ; terminaux.
ms.assetid: 8dd6f792-a29e-40fd-9f5b-ee5525028c2e
title: Terminaux multipiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9e5f9c6d614308370b3d9211f578d5fcb2650bd3c5ba7f8a81dbc981ad2687
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575519"
---
# <a name="multitrack-terminals"></a>Terminaux multipiste

TAPI 3,1 introduit la notion de terminal multipiste, un terminal qui, par essence, est un ensemble de terminaux de « suivi ». Les terminaux multipiste facilitent la charge du programmeur dans les situations où plusieurs flux multimédias sont impliqués dans une session de communication.

Le [terminal d’enregistrement de fichier](file-playback-terminal-and-file-recording-terminal.md) est un exemple de terminal multipiste. Il se compose de « pistes », où chaque « piste » est un terminal correspondant à un flux dans le fichier enregistré.

Un [terminal de suivi](track-terminals.md) peut être un autre terminal multipiste ou un seul terminal. Un terminal à un seul rail est un terminal qui n’a pas de terminaux de suivi. Un terminal simple-Track est un terminal dans le sens TAPI 3 du mot.

Pour plus d’informations sur les terminaux multipiste, consultez les rubriques suivantes :

-   [À propos des terminaux multipiste](about-multitrack-terminals.md)
-   [Mécanisme de sélection par défaut des terminaux](default-terminal-selection-mechanism.md)
-   [Sélection manuelle des terminaux](manual-terminal-selection.md)
-   [Utilisation des terminaux multipiste et du mécanisme de sélection par défaut](using-multitrack-terminals-and-the-default-selection-mechanism.md)

 

 



