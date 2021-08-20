---
description: Un fichier partiellement alloué affecte les quotas de l’utilisateur par la taille nominale du fichier, et non par la quantité réelle d’espace disque allouée.
ms.assetid: 7dbe1133-f5cb-4925-9448-5d40f1c553ff
title: Fichiers partiellement alloués et quotas de disque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e78e9d35e557585f17df6c4672a04b2997792f95b0fca63d2e6a2345a7a8b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015077"
---
# <a name="sparse-files-and-disk-quotas"></a>Fichiers partiellement alloués et quotas de disque

Un fichier partiellement alloué affecte les quotas de l’utilisateur par la taille nominale du fichier, et non par la quantité réelle d’espace disque allouée. Autrement dit, la création d’un fichier de 50 Mo avec zéro octet consomme 50 Mo du quota de cet utilisateur. Cela signifie que lorsque l’utilisateur écrit des données dans le fichier partiellement alloué, il n’a pas besoin de se soucier du dépassement de sa limite de quota, car il a déjà été facturé pour l’espace. Les administrateurs système ne doivent pas compter sur la taille d’un fichier partiellement alloué restant. Par conséquent, ils ne doivent pas accorder à leurs utilisateurs des limites de quota en dur qui dépassent l’espace physique disponible, malgré l’utilisation de fichiers partiellement alloués.

 

 



