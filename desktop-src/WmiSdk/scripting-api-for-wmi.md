---
description: La référence de script WMI contient des définitions pour l’API de script WMI.
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: API de script pour WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c43587fd8f40c2524bcabd79fe80e3d00d74b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863798"
---
# <a name="scripting-api-for-wmi"></a>API de script pour WMI

La référence de script WMI contient des définitions pour l’API de script WMI. Utilisez cette API si vous écrivez des applications avec Microsoft Visual Basic, Visual Basic pour Applications, Visual Basic Scripting Edition (VBScript) ou tout autre langage de script prenant en charge les technologies Active Scripting.

> [!Note]  
> PowerShell est également disponible pour l’écriture de scripts avec WMI. L’applet de commande obtient-WMI et les trois accélérateurs de type ( \[ WMI \] , \[ WMIClass \] et \[ WmiSearcher \] ) permettent un accès administratif de base à WMI. Pour plus d’informations, consultez [écriture de scripts avec Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).

 

Les objets de script WMI, à l’exception de [**SWbemDateTime**](swbemdatetime.md) , ne sont pas marqués comme sécurisés pour l’écriture de scripts pour les scripts exécutés sur des pages HTML dans Internet Explorer. Par conséquent, à moins que le niveau de sécurité dans Internet Explorer ne soit abaissé, le script échoue. **SWbemDateTime** est marqué comme sécurisé pour l’initialisation et l’écriture de scripts. Toutefois, utilisez tous les objets de script WMI dans les appels **GetObject** et **CreateObject** sur le code côté serveur dans les pages de Active Server (ASP).

-   [Modèle objet de l’API de script](scripting-api-object-model.md)
-   [Conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md)
-   [Scripts d’objets d’API](scripting-api-objects.md)
-   [Constantes d’API de script](scripting-api-constants.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence WMI](wmi-reference.md)
</dt> <dt>

[Codes de retour WMI](wmi-return-codes.md)
</dt> </dl>

 

 



