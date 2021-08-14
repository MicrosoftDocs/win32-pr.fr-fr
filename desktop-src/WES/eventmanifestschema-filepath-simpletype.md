---
title: filePath (type simple)
description: Définit une chaîne qui contient un chemin d’accès qualifié complet à un fichier.
ms.assetid: a9b8f40a-fecd-4325-b068-a5aca3133134
keywords:
- filePath type simple EventLog
topic_type:
- apiref
api_name:
- filePath
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d3929db5643ef7a68f2cd33f1d194c80b4dbc1e99e2f667b7c6e43dde8652dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118343995"
---
# <a name="filepath-simple-type"></a>filePath (type simple)

Définit une chaîne qui contient un chemin d’accès qualifié complet à un fichier. Le chemin d’accès peut contenir des variables d’environnement.

``` syntax
<xs:simpleType name="filePath">
    <xs:restriction
        base="xs:string"
     />
</xs:simpleType>
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



 

 





