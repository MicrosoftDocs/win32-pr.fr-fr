---
description: Classe Process_TypeGroup1-cette classe est la classe de type d’événement pour les événements de processus. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 4f06e1af-3f9a-4346-aa50-50f3ee82cd98
title: Classe Process_TypeGroup1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_TypeGroup1
- Process_TypeGroup1.UniqueProcessKey
- Process_TypeGroup1.ProcessId
- Process_TypeGroup1.ParentId
- Process_TypeGroup1.SessionId
- Process_TypeGroup1.ExitStatus
- Process_TypeGroup1.DirectoryTableBase
- Process_TypeGroup1.UserSID
- Process_TypeGroup1.ImageFileName
- Process_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: b1a172b7c3c09ca5735e9e58da2003fcb3790f584cda5809e393ae721393e6a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070029"
---
# <a name="process_typegroup1-class"></a>Traiter la \_ classe TypeGroup1

Cette classe est la classe de type d’événement pour les événements de processus.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_TypeGroup1 : Process
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  uint32 DirectoryTableBase;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a>Membres

La classe **process \_ TypeGroup1** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **process \_ TypeGroup1** a ces propriétés.

<dl> <dt>

CommandLine
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (9), StringTermination ("NullTerminated"), format ("w")
</dt> </dl>

Ligne de commande complète du processus.

</dd> <dt>

DirectoryTableBase
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (6), pointeur
</dt> </dl>

Adresse physique de la table de pages du processus.

</dd> <dt>

ExitStatus
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (5)
</dt> </dl>

État de sortie du processus arrêté.

</dd> <dt>

ImageFileName
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (8), StringTermination ("NullTerminated")
</dt> </dl>

Chemin d’accès au fichier exécutable du processus.

</dd> <dt>

ParentId
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3), format ("x")
</dt> </dl>

Identificateur unique du processus qui crée ce processus. Les numéros d’identificateur de processus sont réutilisés, donc ils identifient uniquement un processus pendant la durée de vie de ce processus. Il est possible que le processus identifié par ParentProcessId soit terminé, de sorte que ParentProcessId ne peut pas faire référence à un processus en cours d’exécution. Il est également possible que ParentProcessId fasse incorrectement référence à un processus qui réutilise un identificateur de processus.

</dd> <dt>

ProcessId
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2), format ("x")
</dt> </dl>

Identificateur de processus global que vous pouvez utiliser pour identifier un processus. La valeur est valide à partir du moment où un processus est créé jusqu’à ce qu’il soit terminé.

</dd> <dt>

SessionId
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (4)
</dt> </dl>

Identificateur unique généré par un système d’exploitation lors de la création d’une nouvelle session. Une session s’étend sur une période allant de l’ouverture de session jusqu’à la fermeture d’une session à partir d’un système spécifique.

</dd> <dt>

UniqueProcessKey
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), pointeur
</dt> </dl>

Adresse de l’objet processus dans le noyau.

</dd> <dt>

UserSID
</dt> <dd> <dl> <dt>

Type de données : **objet**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (7), extension (« SID »)
</dt> </dl>

Identificateur de sécurité (SID) du contexte de l’utilisateur sous lequel l’événement se produit.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les types d’événements DCStart et DCEnd énumèrent le processus en cours d’exécution, y compris le processus système et inactif au moment où la session du noyau démarre et se termine, respectivement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Processus**](process.md)
</dt> </dl>

 

 




