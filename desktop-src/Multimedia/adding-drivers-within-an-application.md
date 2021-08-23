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
ms.openlocfilehash: 9c4cce1310a487e772ac6f65680221f065335951d7d1d6c6dd22c4178c0d985f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692329"
---
# <a name="adding-drivers-within-an-application"></a>Ajout de pilotes dans une application

Si vous avez besoin que votre application implémente ses propres routines de compression en interne, l’application peut ajouter des pilotes à l’ACM en appelant la fonction [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd) . L’application implémente le pilote en fournissant une fonction conforme au prototype [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc) . Une fois que l’application a ajouté le pilote, l’application peut utiliser le pilote à l’aide de l’ACM comme tout autre pilote.

L’ACM traite les pilotes comme des pilotes globaux ou locaux. Une application spécifie si un pilote doit être ajouté comme global ou local lorsqu’il appelle **acmDriverAdd**. Il existe deux différences entre les pilotes globaux et les pilotes locaux :

-   Les pilotes ajoutés en tant que pilotes globaux ne sont pas partagés avec d’autres applications.
-   Une application peut modifier directement la priorité d’un pilote global (mais pas un pilote local) en appelant la fonction [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority) . L’ACM effectue une recherche prioritaire lors de la recherche d’un pilote approprié pour fournir une implémentation d’un appel de fonction. L’ACM donne toujours aux pilotes locaux une priorité plus élevée que les pilotes globaux. Le pilote local le plus récemment ajouté a la priorité la plus élevée.

 

 




