---
title: ServiceParameters
description: Spécifie les paramètres de ligne de commande à passer à un objet installé pour une utilisation par COM via la valeur de Registre LocalService.
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- Valeur de Registre ServiceParameters COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235de1052df72e88e2093647928ed68ab67451cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310122"
---
# <a name="serviceparameters"></a><span data-ttu-id="3fc31-104">ServiceParameters</span><span class="sxs-lookup"><span data-stu-id="3fc31-104">ServiceParameters</span></span>

<span data-ttu-id="3fc31-105">Spécifie les paramètres de ligne de commande à passer à un objet installé pour une utilisation par COM via la valeur de Registre [**LocalService**](localservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3fc31-105">Specifies the command-line parameters to be passed to an object installed for use by COM through the [**LocalService**](localservice.md) registry value.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="3fc31-106">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="3fc31-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a><span data-ttu-id="3fc31-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3fc31-107">Remarks</span></span>

<span data-ttu-id="3fc31-108">Il s’agit d’une valeur de **reg \_ SZ** .</span><span class="sxs-lookup"><span data-stu-id="3fc31-108">This is a **REG\_SZ** value.</span></span> <span data-ttu-id="3fc31-109">Cette chaîne est transmise au service sous la forme d’un argument de ligne de commande lors de son lancement.</span><span class="sxs-lookup"><span data-stu-id="3fc31-109">This string is passed to the service as a command-line argument as it is being launched.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fc31-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3fc31-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fc31-111">**LocalService**</span><span class="sxs-lookup"><span data-stu-id="3fc31-111">**LocalService**</span></span>](localservice.md)
</dt> <dt>

[<span data-ttu-id="3fc31-112">Inscription des serveurs COM</span><span class="sxs-lookup"><span data-stu-id="3fc31-112">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 




