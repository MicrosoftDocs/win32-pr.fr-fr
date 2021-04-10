---
title: Ajout de pilotes dans une application
description: Ajout de pilotes dans une application
ms.assetid: cd9bd0a8-652b-440b-a197-81e20a9d71f1
keywords:
- Audio Compression Manager (ACM), ajout de pilotes
- ACM (gestionnaire de compression audio), ajout de pilotes
- Exemples ACM, ajout de pilotes
- ajout de pilotes
- acmDriverAdd fonction)
- pilotes globaux
- pilotes locaux
- Audio Compression Manager (ACM), pilotes globaux
- ACM (gestionnaire de compression audio), pilotes globaux
- Audio Compression Manager (ACM), pilotes locaux
- ACM (gestionnaire de compression audio), pilotes locaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 000bf7bded89b778f271599d5ce0f8d7f7bd5f72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029226"
---
# <a name="adding-drivers-within-an-application"></a>Ajout de pilotes dans une application

Si vous avez besoin que votre application implémente ses propres routines de compression en interne, l’application peut ajouter des pilotes à l’ACM en appelant la fonction [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) . L’application implémente le pilote en fournissant une fonction conforme au prototype [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) . Une fois que l’application a ajouté le pilote, l’application peut utiliser le pilote à l’aide de l’ACM comme tout autre pilote.

L’ACM traite les pilotes comme des pilotes globaux ou locaux. Une application spécifie si un pilote doit être ajouté comme global ou local lorsqu’il appelle **acmDriverAdd**. Il existe deux différences entre les pilotes globaux et les pilotes locaux :

-   Les pilotes ajoutés en tant que pilotes globaux ne sont pas partagés avec d’autres applications.
-   Une application peut modifier directement la priorité d’un pilote global (mais pas un pilote local) en appelant la fonction [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) . L’ACM effectue une recherche prioritaire lors de la recherche d’un pilote approprié pour fournir une implémentation d’un appel de fonction. L’ACM donne toujours aux pilotes locaux une priorité plus élevée que les pilotes globaux. Le pilote local le plus récemment ajouté a la priorité la plus élevée.

 

 




