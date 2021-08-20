---
title: Dialecte LDAP ADO
description: lors de l’utilisation d’objets ActiveX Directory (ADO) avec le dialecte LDAP, les spécificateurs d’attribut et de plage ne requièrent pas de guillemets.
ms.assetid: adda9cf7-6588-48ee-85e2-fddbaf28807b
ms.tgt_platform: multiple
keywords:
- Interface ADSI de dialecte LDAP ADO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15dba9b7a701b792321ef327d7b5f9893ef3daa0a5eaad80ea151c2b2c90cad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023987"
---
# <a name="ado-ldap-ranging-dialect"></a>Dialecte LDAP ADO

lors de l’utilisation d’objets ActiveX Directory (ADO) avec le dialecte LDAP, les spécificateurs d’attribut et de plage ne requièrent pas de guillemets.

Voici un exemple de dialecte LDAP ADO.


```C++
Command.Text = "<LDAP://CN=NewGroup,DC=Fabrikam,DC=Com>;(objectCategory=group);name,member;Range=51-*;base"
```



 

 




