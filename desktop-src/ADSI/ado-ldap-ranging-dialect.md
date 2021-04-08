---
title: Dialecte LDAP ADO
description: Lors de l’utilisation d’objets d’annuaire ActiveX (ADO) avec le dialecte LDAP, les spécificateurs d’attribut et de plage ne requièrent pas de guillemets.
ms.assetid: adda9cf7-6588-48ee-85e2-fddbaf28807b
ms.tgt_platform: multiple
keywords:
- Interface ADSI de dialecte LDAP ADO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78dc2c7ff2dbfc81a76ff582145b7cf12916439
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839253"
---
# <a name="ado-ldap-ranging-dialect"></a><span data-ttu-id="1e20a-104">Dialecte LDAP ADO</span><span class="sxs-lookup"><span data-stu-id="1e20a-104">ADO LDAP Ranging Dialect</span></span>

<span data-ttu-id="1e20a-105">Lors de l’utilisation d’objets d’annuaire ActiveX (ADO) avec le dialecte LDAP, les spécificateurs d’attribut et de plage ne requièrent pas de guillemets.</span><span class="sxs-lookup"><span data-stu-id="1e20a-105">When using ActiveX Directory Objects (ADO) with the LDAP dialect, the attribute and range specifier do not require quotation marks.</span></span>

<span data-ttu-id="1e20a-106">Voici un exemple de dialecte LDAP ADO.</span><span class="sxs-lookup"><span data-stu-id="1e20a-106">The following is an example of the ADO LDAP dialect.</span></span>


```C++
Command.Text = "<LDAP://CN=NewGroup,DC=Fabrikam,DC=Com>;(objectCategory=group);name,member;Range=51-*;base"
```



 

 




