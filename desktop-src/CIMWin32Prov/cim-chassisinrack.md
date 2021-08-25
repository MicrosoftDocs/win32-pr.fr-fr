---
description: L' \_ Association CIM ChassisInRack représente le &\# 0034 ; contenant&\# 0034 ; relation entre un rack et un châssis qu’il contient.
ms.assetid: 1c8a5058-58fe-42e0-b337-7e1a05120789
ms.tgt_platform: multiple
title: Classe CIM_ChassisInRack
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ChassisInRack
- CIM_ChassisInRack.LocationWithinContainer
- CIM_ChassisInRack.PartComponent
- CIM_ChassisInRack.GroupComponent
- CIM_ChassisInRack.BottomU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 765b5e36fcb5f2cfe400d9dec9ba86d37cd29af8c756ae8416f7aece803f9052
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065209"
---
# <a name="cim_chassisinrack-class"></a>\_Classe CIM ChassisInRack

L’Association **CIM \_ ChassisInRack** représente la relation « contenant » entre un rack et un châssis qu’il contient.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{FAF76B73-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ChassisInRack : CIM_Container
{
  string          LocationWithinContainer;
  CIM_Chassis REF PartComponent;
  CIM_Rack    REF GroupComponent;
  uint16          BottomU;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ChassisInRack** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ChassisInRack** possède les propriétés suivantes.

<dl> <dt>

**Inférieur**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("US")
</dt> </dl>

Entier qui indique le « U » inférieur ou inférieur dans lequel le châssis est monté. Un « U » est une unité de mesure standard pour la hauteur d’un rack, ou un composant montable en rack et est égal à 1,75 pouces ou 4,445 centimètres.

</dd> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ rack CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Un [**\_ rack CIM**](cim-rack.md) qui décrit le rack qui contient le châssis.

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Chaîne de forme libre qui représente le positionnement de l’élément physique dans le package physique. Les informations relatives aux éléments stationnaires dans le conteneur (par exemple, « deuxième baie de lecteur à partir du haut »), des angles, des altitudes et d’autres données peuvent être enregistrées dans cette propriété. Cette chaîne peut compléter ou être utilisée à la place de l’instanciation de l’objet d' [**\_ emplacement CIM**](cim-location.md) .

Cette propriété est héritée [**du \_ conteneur CIM**](cim-container.md).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Type de données **: \_ châssis CIM**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

[**\_ Châssis CIM**](cim-chassis.md) qui décrit le châssis monté dans le rack.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **CIM \_ ChassisInRack** est dérivée [**du \_ conteneur CIM**](cim-container.md).

WMI n’implémente pas cette classe.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Conteneur CIM**](cim-container.md)
</dt> </dl>

 

