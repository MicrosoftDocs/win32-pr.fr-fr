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
ms.openlocfilehash: c083f7a2336a374e8009af2ba8094d57d9826197e16b7577aaf3b00a4c035173
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829619"
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

Qualificateurs : **DefineValues {"processus de l’indicateur de trace d’événements", "thread de l’indicateur de trace d’événements", "chargement de l’image de l’indicateur de trace d’événements", "compteurs de processus de l’indicateur de trace d’événements", "indicateur de trace d’événements SYSTEMCALL", "indicateur de trace d’événements \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ de l' \_ \_ \_ \_ \_ \_ \_ \_ \_ e/s du disque", "indicateur de suivi d’événements \_ \_ \_ \_ \_ e/s de fichier disque « », «indicateur de suivi d’événement \_ \_ \_ Disk \_ IO \_ Init », « Event \_ trace \_ Flag \_ répartiteur », « Event Trace Flag Memory Faults », « Event Trace Flag Memory incorrecte », « Event Trace Flag \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ Network Alloc », « Event \_ trace Flag \_ \_ Network \_ tcpip », « Event Trace Flag \_ \_ \_ Registry », \_ \_ \_ \_Indicateur de trace d’événements \_ \_ Split \_ IO ", \_ " \_ pilote de l’indicateur de trace d’événements \_ "," \_ \_ profil de l’indicateur de trace d’événements \_ "," \_ e/s du fichier d’indicateur de trace d’événements \_ \_ \_ "," Event \_ trace \_ Flag \_ file \_ IO \_ init "}**, **ValueMap {" 0x00000001 "," 0x00000002 0x00000010», « 0x00000020 », « 0x00000040 », « 0x00000080 », « 0x00000100 », « 0x00000200 », « 0x00000400** », « 0x00000800 », « 0x00001000 », « 0x00002000 », « 0x00004000 », « 0x00010000 », « 0x00020000 », « 0x00100000 », « 0x00200000 », « 0x00800000 », « 0x01000000 », « 0x02000000 », « 0x04000000 », «»}
</dt> </dl>

Activez l’indicateur qui indique les fournisseurs de noyau activés.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



 

 




