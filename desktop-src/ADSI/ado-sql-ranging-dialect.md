---
title: dialecte SQL ADO
description: lorsque vous utilisez les objets ActiveX Directory (ADO) à l’aide du dialecte SQL, des guillemets simples (') doivent être utilisés autour du spécificateur d’attribut et de plage.
ms.assetid: 0453aa9e-ed35-45ff-a728-e854bf0bb353
ms.tgt_platform: multiple
keywords:
- interface ADSI de dialecte SQL ADO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7ad714a514bb926239ebb521391d40d097e7f4ee6ccf50208aaed4bba54d8af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181142"
---
# <a name="ado-sql-ranging-dialect"></a>dialecte SQL ADO

lorsque vous utilisez les objets ActiveX Directory (ADO) à l’aide du dialecte SQL, des guillemets simples (') doivent être utilisés autour du spécificateur d’attribut et de plage. voici un exemple de dialecte de SQL ADO.


```sql
Command.CommandText = "select Name, 'member;Range=0-50' from 'LDAP://CN=Group1,DC=Fabrikam,DC=Com' where objectCategory='group'"
```



 

 




