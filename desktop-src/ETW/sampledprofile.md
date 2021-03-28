---
description: Cette classe est la classe de type d’événement pour les événements de profil échantillonnés. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 75ea1e5e-2554-40bb-aa9d-c6d4942c5801
title: SampledProfile, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SampledProfile
- SampledProfile.InstructionPointer
- SampledProfile.ThreadId
- SampledProfile.Count
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3d7a69eef1a2a7988569ffcd930b73a559e18d90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973650"
---
# <a name="sampledprofile-class"></a>SampledProfile, classe

Cette classe est la classe de type d’événement pour les événements de profil échantillonnés.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[EventType{46}, EventTypeName{"SampleProfile"}]
class SampledProfile : PerfInfo
{
  uint32 InstructionPointer;
  uint32 ThreadId;
  uint32 Count;
};
```

## <a name="members"></a>Membres

La classe **SampledProfile** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **SampledProfile** possède les propriétés suivantes.

<dl> <dt>

**Count**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (3)
</dt> </dl>

Non utilisé.

</dd> <dt>

**InstructionPointer**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (1), pointeur
</dt> </dl>

Adresse de l’image qui était en cours d’exécution au moment où le processeur a été échantillonné.

</dd> <dt>

**ThreadId**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : WmiDataId (2)
</dt> </dl>

Identificateur du thread qui s’exécutait au moment où le processeur a été échantillonné.

</dd> </dl>

## <a name="remarks"></a>Notes

Ces événements fournissent un profil d’exécution échantillonné. L’événement enregistre ce qui a été exécuté sur le processeur. Vous pouvez utiliser les événements d’image pour identifier le module binaire contenant cette instruction. Vous pouvez ensuite utiliser ces informations pour créer un profil d’exécution pendant la durée de la trace.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 




