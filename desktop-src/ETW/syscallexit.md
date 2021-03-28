---
description: Cette classe est la classe de type d’événement pour les événements de sortie d’appel système. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: bb9a2770-f37b-4055-8811-59ba117adf82
title: SysCallExit, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallExit
- SysCallExit.SysCallNtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: af46f374d4532efc15185a4716526beabfe5ced1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973410"
---
# <a name="syscallexit-class"></a>SysCallExit, classe

Cette classe est la classe de type d’événement pour les événements de sortie d’appel système.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{52}, EventTypeName{"SysClExit"}]
class SysCallExit : PerfInfo
{
  uint32 SysCallNtStatus;
};
```

## <a name="members"></a>Membres

La classe **SysCallExit** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **SysCallExit** possède les propriétés suivantes.

<dl> <dt>

**SysCallNtStatus**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), format ("x")
</dt> </dl>

Code d’état retourné par l’appel système NT.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 




