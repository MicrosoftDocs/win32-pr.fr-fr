---
description: Utilisez l’opérateur ISA dans la clause WHERE d’une requête de données pour demander des objets incorporés dans une hiérarchie de classes.
ms.assetid: a4eb4c34-2ed0-4e85-84c6-6b8f17c8b07d
ms.tgt_platform: multiple
title: Opérateur ISA pour les requêtes de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b33c0bc4b78101a4b1e6a38997518fec543b9eb49e42b28cbb2500c321f56ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318301"
---
# <a name="isa-operator-for-data-queries"></a>Opérateur ISA pour les requêtes de données

Utilisez l’opérateur ISA dans la clause WHERE d’une requête de données pour demander des objets incorporés dans une hiérarchie de classes.

L’exemple suivant illustre la syntaxe permettant de demander des objets incorporés dans une hiérarchie de classes.


```sql
SELECT * FROM Class WHERE EmbeddedProp ISA "ParentClass"
```



Le résultat comprend des instances de **classe** qui ont des objets incorporés dérivés de **ParentClass** dans la propriété **EmbeddedProp** . Les instances de l’objet de **classe** ne sont pas toutes dérivées de **ParentClass**, mais le résultat retourne les objets incorporés dérivés de **ParentClass**.

Par exemple, dans la requête suivante, **classa** comprend la propriété **EmbeddedObj** faiblement typée. La classe **classa** comporte dix instances. Cinq de ces instances ont des objets incorporés avec un type dérivé de **ClassZ**. Les cinq autres ont des objets incorporés d’autres types.

L’exemple suivant montre la requête qui retourne les cinq instances, qui incluent les objets dérivés de **ClassZ**.


```sql
SELECT * FROM ClassA WHERE EmbeddedObj ISA "ClassZ"
```



 

 



