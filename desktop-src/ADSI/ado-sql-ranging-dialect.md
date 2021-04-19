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
# <a name="ado-sql-ranging-dialect"></a><span data-ttu-id="adefd-104">Dialecte SQL ADO</span><span class="sxs-lookup"><span data-stu-id="adefd-104">ADO SQL Ranging Dialect</span></span>

<span data-ttu-id="adefd-105">Lorsque vous utilisez les objets d’annuaire ActiveX (ADO) à l’aide du dialecte SQL, vous devez utiliser des guillemets simples (') autour du spécificateur d’attribut et de plage.</span><span class="sxs-lookup"><span data-stu-id="adefd-105">When using the ActiveX Directory Objects (ADO), using the SQL dialect, single quotation marks (') must be used around the attribute and range specifier.</span></span> <span data-ttu-id="adefd-106">Voici un exemple de dialecte SQL ADO.</span><span class="sxs-lookup"><span data-stu-id="adefd-106">The following is an example of the ADO SQL dialect.</span></span>


```sql
Command.CommandText = "select Name, 'member;Range=0-50' from 'LDAP://CN=Group1,DC=Fabrikam,DC=Com' where objectCategory='group'"
```



 

 




