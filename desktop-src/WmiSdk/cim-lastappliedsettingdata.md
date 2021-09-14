---
description: Association entre un objet et un autre objet qui lui a été appliqué.
ms.assetid: ee6b17b7-4f01-4731-8d6b-a3421621a75a
ms.tgt_platform: multiple
title: Classe CIM_LastAppliedSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LastAppliedSettingData
- Root\CIMV2.CIM_LastAppliedSettingData.Target
- Root\CIMV2.CIM_LastAppliedSettingData.AppliedObject
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: fbad71cd88992673af5dd60c04b92dd3c833e5b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915812"
---
# <a name="cim_lastappliedsettingdata-class"></a>\_Classe CIM LastAppliedSettingData

Association entre un objet et un autre objet qui lui a été appliqué.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
class CIM_LastAppliedSettingData
{
  CIM_ManagedElement REF Target;
  CIM_ManagedElement REF AppliedObject;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ LastAppliedSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ LastAppliedSettingData** possède les propriétés suivantes.

<dl> <dt>

**AppliedObject**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ propriété ManagedElement**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Objet qui a été appliqué à l’objet cible.

</dd> <dt>

**Cible**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ propriété ManagedElement**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Objet qui était la cible de l’application de l’objet.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------|------------------------|
| Espace de noms<br/> | \\Cimv2 racine<br/> |



 

 




