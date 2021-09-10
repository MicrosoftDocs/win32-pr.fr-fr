---
title: ServiceParameters
description: Spécifie les paramètres de ligne de commande à passer à un objet installé pour une utilisation par COM via la valeur de Registre LocalService.
ms.assetid: da11e422-c0f2-4e44-9728-740ea6b61421
keywords:
- Valeur de Registre ServiceParameters COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235de1052df72e88e2093647928ed68ab67451cd
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363331"
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

 

 




