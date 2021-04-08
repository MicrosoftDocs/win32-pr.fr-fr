---
description: 'En savoir plus sur : colonnes définies par l’utilisateur'
title: Colonnes définies par l’utilisateur
TOCTitle: User Defined Columns
ms:assetid: cccfc97c-acde-4328-a87f-ee7dcc54203c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294091(v=EXCHG.10)
ms:contentKeyID: 32765706
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 624a916ee2048d9069c7695c79824e3357b511f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034237"
---
# <a name="user-defined-columns"></a>Colonnes définies par l’utilisateur


_**S’applique à :** Windows | Serveur Windows_

## <a name="user-defined-columns"></a>Colonnes définies par l’utilisateur

Les colonnes définies par l’utilisateur sont des colonnes dont les valeurs par défaut sont fournies par une fonction de rappel. Ces colonnes sont toujours marquées et définies sur la valeur calculée par la fonction de rappel. Cette valeur doit être stable pour chaque ligne de la table. La fonction de rappel est utilisée uniquement lorsque l’application ou le moteur de base de données lui-même doit lire la valeur de la colonne pour une ligne donnée. L’application a la possibilité de remplacer la valeur par défaut et de définir une valeur spécifique dans la colonne. Lorsque la valeur par défaut est remplacée dans les colonnes, elle utilise de l’espace dans la ligne ; sinon, les colonnes par défaut définies par l’utilisateur n’utilisent pas d’espace dans l’enregistrement.

L’option valeurs par défaut définies par l’utilisateur est définie dans le membre **Grbit** de la structure [JET_COLUMNDEF](./jet-columndef-structure.md) dans l’appel à [JetAddColumn](./jetaddcolumn-function.md). Le paramètre *pvDefault* de la fonction [JetAddColumn](./jetaddcolumn-function.md) pointe vers une structure [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) , qui contient le nom de la fonction de rappel dans le membre **szCallback** et les données qui sont passées au rappel dans le membre **pbUserData** .
