---
title: ServiceParameters
description: Spécifie les paramètres de ligne de commande à passer à un objet installé pour une utilisation par COM via la valeur de Registre LocalService.
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- Valeur de Registre ServiceParameters COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 103b55269b700beaf5c85e3408e3597e63fb9140e4dc79fe4bb895ff6767bfc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129961"
---
# <a name="serviceparameters"></a>ServiceParameters

Spécifie les paramètres de ligne de commande à passer à un objet installé pour une utilisation par COM via la valeur de Registre [**LocalService**](localservice.md) .

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ServiceParameters = parameter
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **reg \_ SZ** . Cette chaîne est transmise au service sous la forme d’un argument de ligne de commande lors de son lancement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**LocalService**](localservice.md)
</dt> <dt>

[Inscription des serveurs COM](registering-com-servers.md)
</dt> </dl>

 

 




