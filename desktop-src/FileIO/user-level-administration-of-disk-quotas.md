---
description: Comment obtenir davantage d’espace disque disponible après avoir dépassé le quota alloué.
ms.assetid: a73b6a11-36f1-4437-a83d-e89918b1b0ae
title: Administration au niveau de l’utilisateur des quotas de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc130cf925899ccf0a86af20ff6772689ecdfbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521914"
---
# <a name="user-level-administration-of-disk-quotas"></a>Administration au niveau de l’utilisateur des quotas de disque

Les quotas de disque sont transparents pour l’utilisateur. Lorsqu’un utilisateur demande la quantité d’espace libre sur un disque, le système signale uniquement l’allocation de quota disponible que l’utilisateur a disponible. Si l’utilisateur dépasse cette limite, le système renvoie une erreur de **\_ \_ saturation du disque** , tout comme pour indiquer que le disque est plein.

Pour obtenir plus d’espace disque disponible après avoir dépassé le quota alloué, l’utilisateur doit effectuer l’une des opérations suivantes :

-   Supprimez certains fichiers.
-   Demandez à un autre utilisateur de réclamer la propriété de certains fichiers.
-   Demander à l’administrateur d’augmenter le quota alloué.

Les programmes qui doivent récupérer la quantité réelle d’espace disque libre peuvent appeler la fonction [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) et examiner le paramètre *TotalNumberOfFreeBytes* .

 

 



