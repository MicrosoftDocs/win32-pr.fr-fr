---
description: Cette classe est la classe de type d’événement pour les événements de processus. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: fcf2897d-32b4-42b9-892c-f0106687d3c2
title: Classe Process_V0_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V0_TypeGroup1
- Process_V0_TypeGroup1.ProcessId
- Process_V0_TypeGroup1.ParentId
- Process_V0_TypeGroup1.UserSID
- Process_V0_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2889feb05bfc396f2c2018ca59d2cf46fba8ec13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972223"
---
# <a name="process_v0_typegroup1-class"></a>Traiter \_ la \_ classe TypeGroup1 v0

Cette classe est la classe de type d’événement pour les événements de processus.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V0_TypeGroup1 : Process_V0
{
  uint32 ProcessId;
  uint32 ParentId;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a>Membres

La classe **process \_ v0 \_ TypeGroup1** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **process \_ v0 \_ TypeGroup1** possède les propriétés suivantes.

<dl> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4), StringTermination ("NullTerminated")
</dt> </dl>

Chemin d’accès au fichier exécutable du processus.

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2), pointeur
</dt> </dl>

Identificateur unique du processus qui crée un processus. Les numéros d’identificateur de processus sont réutilisés, donc ils identifient uniquement un processus pendant la durée de vie de ce processus. Il est possible que le processus identifié par ParentProcessId soit terminé, de sorte que ParentProcessId ne peut pas faire référence à un processus en cours d’exécution. Il est également possible que ParentProcessId fasse incorrectement référence à un processus qui réutilise un identificateur de processus.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), pointeur
</dt> </dl>

Identificateur de processus global que vous pouvez utiliser pour identifier un processus. La valeur est valide à partir du moment où un processus est créé jusqu’à ce qu’il soit terminé.

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3), extension (« SID »)
</dt> </dl>

Identificateur de sécurité (SID) du contexte de l’utilisateur sous lequel l’événement se produit.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Processus \_ v0**](process-v0.md)
</dt> </dl>

 

 




