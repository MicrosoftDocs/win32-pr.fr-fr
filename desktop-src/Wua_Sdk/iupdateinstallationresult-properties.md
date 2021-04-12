---
description: L’interface IUpdateInstallationResult définit les propriétés suivantes.
ms.assetid: 7e8f7125-f89b-416f-bcc5-422eecabe0c4
title: Propriétés IUpdateInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b2e2792215d8d927d6e6157c82e37193e74d2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201568"
---
# <a name="iupdateinstallationresult-properties"></a>Propriétés IUpdateInstallationResult

L’interface [**IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) définit les propriétés suivantes.



| Propriété                                                           | Description                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**HResult**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_hresult)               | Obtient la valeur de l’exception **HRESULT** levée pendant l’opération sur une mise à jour.                                            |
| [**RebootRequired**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_rebootrequired) | Obtient une valeur booléenne qui indique si un redémarrage système est requis sur un ordinateur pour terminer l’installation d’une mise à jour. |
| [**ResultCode**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_resultcode)         | Obtient une valeur [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) qui spécifie le résultat d’une opération sur une mise à jour.          |



 

 

 



