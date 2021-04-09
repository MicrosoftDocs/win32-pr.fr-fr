---
description: L’interface IInstallationResult définit les propriétés suivantes.
ms.assetid: bd6cd5ae-2e43-4ac3-8ce7-ac80b7fc5cb8
title: Propriétés IInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78783b6758ab30d6a77c07cd71111486f3a7343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034042"
---
# <a name="iinstallationresult-properties"></a>Propriétés IInstallationResult

L’interface [**IInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) définit les propriétés suivantes.



| Propriété                                                     | Description                                                                                                                            |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**HResult**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_hresult)               | Obtient le **HRESULT** de l’exception, le cas échéant, qui est déclenché pendant l’installation.                                                 |
| [**RebootRequired**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_rebootrequired) | Obtient une valeur booléenne qui indique si vous devez redémarrer l’ordinateur pour terminer l’installation ou la désinstallation d’une mise à jour. |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_resultcode)         | Obtient une valeur [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) qui spécifie le résultat d’une opération sur une mise à jour.               |



 

 

 



