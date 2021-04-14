---
title: Points de terminaison
description: Configure une application COM pour utiliser un numéro de port TCP spécifié pour les communications DCOM.
ms.assetid: 2a286a13-24b8-418a-b29b-5543a1c56c45
keywords:
- Valeur de registre des points de terminaison COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0addcd6c09b409629bb4a7157241d57476cafe3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379785"
---
# <a name="endpoints"></a><span data-ttu-id="1b4f6-104">Points de terminaison</span><span class="sxs-lookup"><span data-stu-id="1b4f6-104">Endpoints</span></span>

<span data-ttu-id="1b4f6-105">Configure une application COM pour utiliser un numéro de port TCP spécifié pour les communications DCOM.</span><span class="sxs-lookup"><span data-stu-id="1b4f6-105">Configures a COM application to use a specified TCP port number for DCOM communications.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="1b4f6-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="1b4f6-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      Endpoints = ncacn_ip_tcp,0,port
```

## <a name="remarks"></a><span data-ttu-id="1b4f6-107">Notes</span><span class="sxs-lookup"><span data-stu-id="1b4f6-107">Remarks</span></span>

<span data-ttu-id="1b4f6-108">Il s’agit d’une valeur **reg \_ multiple \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="1b4f6-108">This is a **REG\_MULTI\_SZ** value.</span></span>

<span data-ttu-id="1b4f6-109">La valeur de *port* est un nombre compris entre 1024 et 65535, qui spécifie le numéro de port TCP que votre application com utilisera pour les communications DCOM.</span><span class="sxs-lookup"><span data-stu-id="1b4f6-109">The *port* value is a number between 1024 and 65535 that specifies the TCP port number that your COM application will use for DCOM communications.</span></span> <span data-ttu-id="1b4f6-110">Si vous ne spécifiez pas cette clé de Registre, les numéros de port des communications DCOM sont attribués de manière dynamique.</span><span class="sxs-lookup"><span data-stu-id="1b4f6-110">If you do not specify this registry key, port numbers for DCOM communications are dynamically assigned.</span></span> <span data-ttu-id="1b4f6-111">Dans la plupart des scénarios, vous préférerez peut-être laisser cette clé de Registre non définie et autoriser DCOM à affecter dynamiquement des numéros de port.</span><span class="sxs-lookup"><span data-stu-id="1b4f6-111">In most scenarios, you might prefer to leave this registry key undefined and allow DCOM to dynamically assign port numbers.</span></span>

 

 




