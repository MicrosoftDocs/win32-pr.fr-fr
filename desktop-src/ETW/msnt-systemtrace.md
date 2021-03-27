---
description: Classe parente à partir de laquelle toutes les classes de trace d’événements système sont dérivées. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 27979d9c-eca7-426f-8f8e-99443e5a0188
title: Classe MSNT_SystemTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSNT_SystemTrace
- MSNT_SystemTrace.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2eb0044029761a93a353a08a955d39d76c267f9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972282"
---
# <a name="msnt_systemtrace-class"></a>MSNT \_ SystemTrace, classe

Classe parente à partir de laquelle toutes les classes de trace d’événements système sont dérivées.

La syntaxe suivante est simplifiée à partir du code MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Guid("{9e814aad-3204-11d2-9a82-006008a86939}")]
class MSNT_SystemTrace : EventTrace
{
  uint32 Flags;
};
```

## <a name="members"></a>Membres

La classe **MSNT \_ SystemTrace** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSNT \_ SystemTrace** possède les propriétés suivantes.

<dl> <dt>

**Indicateurs**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **DefineValues {"processus de l’indicateur de trace d’événements", "thread de l’indicateur de trace d’événements", "chargement de l’image de l’indicateur de trace d’événements", "compteurs de processus de l’indicateur de trace d’événements", "indicateur de trace d’événements \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ CSWITCH", "indicateur de trace d’événements \_ \_ \_ DPC", "indicateur de trace d’événements indicateur de trace d’événements \_ \_ \_ \_ \_ \_ SYSTEMCALL", "indicateur de trace d’événements \_ \_ \_ Disk \_ IO", "Event \_ trace \_ Flag Disk \_ \_ file \_ IO", "Event \_ trace \_ Flag \_ Disk \_ IO \_ init", "EVENT trace Flag répartiteur", "EVENT trace Flag Network tcpips", "Event Trace Flag \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ Memory \_ \_ Faults", "Event \_ trace Flag virtuel Alloc", "Event Trace Flag \_ \_ \_ \_ \_ \_ Network \_ tcpip", "Event \_ trace Flag \_ \_ Registry», « Event Trace Flag \_ \_ \_ ALPC », « Event \_ trace \_ Flag \_ Split \_ IO », « Event \_ trace \_ Flag \_ Driver », « Event Trace Flag \_ \_ \_ Profile », « Event \_ trace \_ Flag \_ file \_ IO », «Event \_ trace \_ Flag \_ file \_ IO \_ init"}**, **ValueMap {"0x00000001", "0x00000002", "0x00000004", "0x00000008", "0x00000010", "0x00000020", "0x00000040", "0x00000080", "0x00000100" , « 0x00000200 », « 0x00000400 », « 0x00000800 », « 0x00001000 », « 0x00002000 », « 0x00004000** », « 0x00010000 », « 0x00020000 », « 0x00100000 », « 0x00200000 », « 0x00800000 », « 0x01000000 », « 0x02000000 », « 0x04000000 »}
</dt> </dl>

Activez l’indicateur qui indique les fournisseurs de noyau activés.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



 

 




