---
title: Type simple processTokenSidType
description: Définit les valeurs possibles pour l’élément ProcessTokenSidType (principalType).
ms.assetid: 9db3e113-c525-4cbf-88c2-be256d641e92
keywords:
- Planificateur de tâches de type simple processTokenSidType
topic_type:
- apiref
api_name:
- processTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13cf70534510e1aed8def9005d0c2d1eafab2a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384355"
---
# <a name="processtokensidtype-simple-type"></a>Type simple processTokenSidType

Définit les valeurs possibles pour l’élément [**ProcessTokenSidType (principalType)**](taskschedulerschema-processtokensidtype-principaltype-element.md) .

``` syntax
<xs:simpleType name="processTokenSidType">
    <xs:restriction
        base="string"
    >
        <xs:enumeration
            value="None"
         />
        <xs:enumeration
            value="Unrestricted"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="enumeration-values"></a>Valeurs d’énumération

Le type simple **processTokenSidType** définit les valeurs suivantes.



| Valeur        | Description                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| Aucune         | Les tâches sont exécutées dans un processus qui ne contient pas de SID de jeton de processus (aucune modification n’est apportée à la liste des groupes de jetons de processus).<br/> |
| Non restreint | Un SID de tâche est dérivé du chemin d’accès complet à la tâche et est ajouté à la liste des groupes de jetons de processus.<br/>                           |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



 

 





