---
description: Décrivez l’instruction SELECT pour une requête de données.
ms.assetid: 9c1a164e-4728-4fbe-8a49-b571005a46ec
ms.tgt_platform: multiple
title: Instruction SELECT pour les requêtes de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44fec0526c5e5d47a74d6e165726222f9e521bd7102072e5a4b79e960f8dae19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315947"
---
# <a name="select-statement-for-data-queries"></a>Instruction SELECT pour les requêtes de données

Vous pouvez utiliser diverses instructions SELECT pour demander des informations. Les instructions peuvent être des instructions de base ou elles peuvent être plus restrictives pour limiter le jeu de résultats retourné par la requête.

L’exemple suivant est une instruction SELECT de base utilisée pour interroger des données.


```sql
SELECT * FROM Class
```



Cette instruction retourne les instances de la classe spécifiée et l’une de ses sous-classes. Toutes les propriétés système et définies par l’utilisateur pour les classes sont incluses. Si une propriété système n’est pas pertinente pour une requête particulière, elle contient la **valeur null**.

Vous pouvez utiliser plusieurs techniques pour réduire la bande passante nécessaire à la récupération du jeu de résultats, si l’exécution de la requête entraîne une surcharge excessive et que l’utilisateur est uniquement intéressé par un sous-ensemble des propriétés. Tout d’abord, les requêtes peuvent remplacer l’astérisque par les propriétés souhaitées.

L’exemple suivant montre comment interroger des propriétés spécifiques.


```sql
SELECT property_1, property_2, property_3 FROM class
```



Le jeu de résultats comprend toutes les propriétés système et les propriétés non système spécifiées.

Une autre technique pour limiter l’étendue du jeu de résultats d’une requête consiste à utiliser la propriété système de [**\_ \_ classe**](wmi-system-properties.md) . Par défaut, les requêtes retournent toutes les instances de la classe spécifiée et de ses sous-classes. Vous pouvez utiliser la propriété système de **\_ \_ classe** pour demander uniquement des instances de la classe spécifiée, à l’exclusion de ses sous-classes.

L’exemple suivant montre comment utiliser la propriété système de [**\_ \_ classe**](wmi-system-properties.md) dans une clause WHERE.


```sql
SELECT * FROM Device WHERE __CLASS = "Device"
```



Vous pouvez également utiliser la propriété système de [**\_ \_ classe**](wmi-system-properties.md) pour limiter le jeu de résultats aux instances de sous-classes particulières.

L’exemple suivant montre comment limiter le jeu de résultats aux instances de sous-classes particulières.


```sql
SELECT * FROM Device WHERE __CLASS = "Modem" OR __CLASS = "Keyboard"
```



> [!Note]  
> Si vous construisez une requête avec un chemin d’accès non valide pour un objet incorporé, votre requête ne retourne pas d’erreur ou de résultats.

 

L’exemple suivant retourne une instance de **MainClass**, en supposant qu’il existe une instance de **MainClass** contenant l’objet incorporé **EmbedObj** avec une propriété **P \_ UInt32** égale à « 70011 ».


```sql
SELECT * FROM MainClass WHERE EmbedObj.P_Uint32 = 70011
```



L’exemple suivant ne retourne aucun résultat et ne retourne pas d’erreur, en supposant que l’objet incorporé **EmbedObj** dans l’instance de **MainClass** n’a pas de propriété **non valide**.


```sql
SELECT * FROM MainClass WHERE StrongEmbedObj.INVALID = 70011
```



 

 



