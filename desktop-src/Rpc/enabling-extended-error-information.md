---
title: Activation des informations d’erreur étendues
description: Activation des informations d’erreur étendues pour l’appel de procédure distante (RPC).
ms.assetid: 73b72d0a-8533-40ac-8b41-8af4d60f9631
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0813e770a6b1490ddd3e8e90b050f575ee76d01cf8e4e5d59b4d9e0eff74ce2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021669"
---
# <a name="enabling-extended-error-information"></a>Activation des informations d’erreur étendues

Pour activer les informations d’erreur étendues, procédez comme suit :

Ouvrez la stratégie de l’ordinateur local à l’aide de l’interface gpedit. msc.

Accédez à la stratégie située à la page Configuration ordinateur/Modèles d’administration/système/appel de procédure distante/prise en charge des dépannages RPC/propagation des informations d’erreur étendues.

Activez la stratégie et définissez la **propagation des informations d’erreurs étendues** sur « on ».

Ce processus active la propagation des informations d’erreur étendues pour tous les processus sur l’ordinateur.

Pour activer les informations d’erreur étendues uniquement pour certains processus sur un ordinateur, ou pour les désactiver uniquement pour certains processus sur l’ordinateur, utilisez l’option **désactivé avec les exceptions** ou **avec les exceptions** . Les deux options utilisent le champ **exceptions d’informations d’erreur étendues** pour spécifier les processus qui ont le paramètre par défaut et les processus qui ont le contraire du paramètre par défaut. Les **exceptions d’informations d’erreur étendues** contiennent une liste de noms de processus.

Si la ligne de commande d’un processus commence par une chaîne qui se trouve dans les **exceptions d’informations d’erreur étendues**, le processus reçoit l’inverse du paramètre par défaut. Par exemple, si vous souhaitez que tous les processus sur votre ordinateur propagent les informations d’erreur étendues, à l’exception de LSASS et du processus appelé **serveur sécurisé**, définissez la **propagation des informations d’erreur étendues** **sur activé avec des exceptions** et spécifiez dans le champ **exceptions d’informations d’erreur étendues** la chaîne suivante : LSASS « serveur sécurisé ».

Les chaînes peuvent être placées entre guillemets doubles, mais cela est facultatif s’il n’y a pas d’espaces dans la chaîne. En outre, le début de la ligne de commande du processus peut être spécifié. Par exemple, si la valeur **off avec exceptions** est spécifiée dans le champ **propagation des informations d’erreur étendues** , et dans le champ **exceptions d’informations d’erreur étendues** , les éléments suivants sont spécifiés : Win.

Chaque processus qui commence par « Win » propage les informations d’erreur étendues. Sur de nombreux ordinateurs, par exemple, ces processus sont winlogon.exe et WINWORD.EXE.

 

 




