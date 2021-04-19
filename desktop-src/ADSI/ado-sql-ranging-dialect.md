---
title: Dialecte SQL ADO
description: Lorsque vous utilisez les objets d’annuaire ActiveX (ADO) à l’aide du dialecte SQL, vous devez utiliser des guillemets simples (') autour du spécificateur d’attribut et de plage.
ms.assetid: 0453aa9e-ed35-45ff-a728-e854bf0bb353
ms.tgt_platform: multiple
keywords:
- Interface ADSI de dialecte SQL ADO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f7b846cd3517613dd8ea914f53a7b31c30f8651
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106531184"
---
# <a name="ado-sql-ranging-dialect"></a>Dialecte SQL ADO

Lorsque vous utilisez les objets d’annuaire ActiveX (ADO) à l’aide du dialecte SQL, vous devez utiliser des guillemets simples (') autour du spécificateur d’attribut et de plage. Voici un exemple de dialecte SQL ADO.


```sql
Command.CommandText = "select Name, 'member;Range=0-50' from 'LDAP://CN=Group1,DC=Fabrikam,DC=Com' where objectCategory='group'"
```



 

 




