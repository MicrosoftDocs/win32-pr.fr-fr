---
title: Types de données NAP (NapTypes. h)
description: 'Remarque : la plateforme de protection d’accès réseau n’est pas disponible à partir de Windows 10. les types de données pour l’API de protection d’accès réseau (NAP) sont les suivants.'
ms.assetid: 54f2866b-4333-4fc8-bb25-b7d4ae72b7dc
keywords:
- ProbationTime
- ProtocolMaxSize
- NapComponentId
- SystemHealthEntityId
- EnforcementEntityId
- SystemHealthEntityCount
- EnforcementEntityCount
- StringCorrelationId
- ConnectionId
- Pourcentage
- MessageId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5780d73701354a12b244c5e5ea6167c2cfba70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942626"
---
# <a name="nap-datatypes"></a>Types de données NAP

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

Les types de données de l’API de protection d’accès réseau (NAP) sont les suivants.


```C++
typedef FILETIME ProbationTime;
typedef UINT32 ProtocolMaxSize;
typedef UINT32 NapComponentId;
typedef NapComponentId SystemHealthEntityId;
typedef NapComponentId EnforcementEntityId;
typedef UINT16 SystemHealthEntityCount;
typedef UINT16 EnforcementEntityCount;
typedef CountedString StringCorrelationId;
typedef GUID ConnectionId;
typedef UINT8 Percentage;
typedef UINT32 MessageId;
```



<dl> <dt>

**ProbationTime**
</dt> <dd>

Structure [fileTime](/windows/win32/api/minwinbase/ns-minwinbase-filetime) qui contient une heure relative à la période d’essai d’une machine cliente.

</dd> <dt>

**ProtocolMaxSize**
</dt> <dd>

Valeur qui spécifie la plage de valeurs possibles pour la taille maximale, en octets, d’un paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) tel que défini par Range ([**minProtocolMaxSize, maxProtocolMaxSize**](nap-type-constants.md)).

</dd> <dt>

**NapComponentId**
</dt> <dd>

Identificateur à 4 octets unique utilisé par les clients de l’SHA, des validateurs d’intégrité du système et de l’application pour s’identifier eux-mêmes. Les trois premiers octets sont le code SMI affecté par l’IETF du fournisseur et le dernier octet identifie le composant lui-même.

</dd> <dt>

**SystemHealthEntityId**
</dt> <dd>

Valeur **NapComponentId** utilisée pour identifier les paires SHA/SHV.

</dd> <dt>

**EnforcementEntityId**
</dt> <dd>

Valeur **NapComponentId** utilisée pour identifier les clients de contrainte.

</dd> <dt>

**SystemHealthEntityCount**
</dt> <dd>

Valeur qui spécifie le nombre de Sha inscrits dans le système NAP dans la plage 0 (zéro) à [**maxSystemHealthEntityCount**](nap-type-constants.md).

</dd> <dt>

**EnforcementEntityCount**
</dt> <dd>

Valeur qui spécifie le nombre de clients de mise en œuvre dans le système NAP dans la plage 0 (zéro) à [**maxEnforcerCount**](nap-type-constants.md).

</dd> <dt>

**StringCorrelationId**
</dt> <dd>

Version [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) d’une structure [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) utilisée pour coupler [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh) à **SoHResponses**.

</dd> <dt>

**ID**
</dt> <dd>

Identificateur global unique (GUID) unique utilisé pour identifier les connexions NAP gérées par les clients de contrainte.

</dd> <dt>

**Percentage**
</dt> <dd>

Valeur qui contient le pourcentage compris entre 0 (zéro) et 100 de correction terminée.

</dd> <dt>

**MessageId**
</dt> <dd>

Valeur unique utilisée pour identifier les messages du système NAP.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                                                                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                                                                                |
| En-tête<br/>                   | <dl> <dt>NapTypes. h ; </dt> <dt>NapEnforcementClient. h</dt> </dl> |



 

