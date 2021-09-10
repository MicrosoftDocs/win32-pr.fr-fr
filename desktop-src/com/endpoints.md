---
title: Points de terminaison
description: Configure une application COM pour utiliser un numéro de port TCP spécifié pour les communications DCOM.
ms.assetid: 2a286a13-24b8-418a-b29b-5543a1c56c45
keywords:
- Valeur de registre des points de terminaison COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0addcd6c09b409629bb4a7157241d57476cafe3
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363584"
---
# <a name="endpoints"></a>Points de terminaison

Configure une application COM pour utiliser un numéro de port TCP spécifié pour les communications DCOM.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      Endpoints = ncacn_ip_tcp,0,port
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur **reg \_ multiple \_ SZ** .

La valeur de *port* est un nombre compris entre 1024 et 65535, qui spécifie le numéro de port TCP que votre application com utilisera pour les communications DCOM. Si vous ne spécifiez pas cette clé de Registre, les numéros de port des communications DCOM sont attribués de manière dynamique. Dans la plupart des scénarios, vous préférerez peut-être laisser cette clé de Registre non définie et autoriser DCOM à affecter dynamiquement des numéros de port.

 

 




