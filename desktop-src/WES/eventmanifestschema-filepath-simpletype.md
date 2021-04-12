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
ms.openlocfilehash: 492580634c1a48c88df6f50de2582c215ec7ecb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464570"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



 

 





