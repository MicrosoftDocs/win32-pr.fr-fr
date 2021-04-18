---
description: Association entre un système virtuel et les données de paramètre de l’instantané qui est le parent du système virtuel.
ms.assetid: d11e00e0-a163-49ea-b8ef-e3909a7dc83f
ms.tgt_platform: multiple
title: Classe CIM_PreviousSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PreviousSettingData
- Root\CIMV2.CIM_PreviousSettingData.Target
- Root\CIMV2.CIM_PreviousSettingData.PreviousObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 4422d590714b82120b610dc4eeb9377a385519d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533027"
---
# <a name="cim_previoussettingdata-class"></a>\_Classe CIM PreviousSettingData

Association entre un système virtuel et les données de paramètre de l’instantané qui est le parent du système virtuel.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
class CIM_PreviousSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF PreviousObject;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ PreviousSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ PreviousSettingData** possède les propriétés suivantes.

<dl> <dt>

**PreviousObject**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ propriété ManagedElement**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Données du paramètre d’instantané qui est le parent de ce système informatique.

</dd> <dt>

**Cible**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ propriété ManagedElement**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Système informatique qui était la cible de l’application.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------|------------------------|
| Espace de noms<br/> | \\Cimv2 racine<br/> |



 

 




