---
description: La \_ classe CIM MonitorSetting associe la résolution du moniteur à l’analyseur de bureau à laquelle elle s’applique.
ms.assetid: 4bf0b2d5-b901-4294-a33b-9c8a87785af0
ms.tgt_platform: multiple
title: Classe CIM_MonitorSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MonitorSetting
- CIM_MonitorSetting.Setting
- CIM_MonitorSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 084b8bf9b1ca175f723fe7e15beaf6b79e315b318982c1a0bd505b82b58fbd2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821029"
---
# <a name="cim_monitorsetting-class"></a>\_Classe CIM MonitorSetting

La classe **CIM \_ MonitorSetting** associe la résolution du moniteur à l’analyseur de bureau à laquelle elle s’applique.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La syntaxe suivante est simplifiée à partir de code au format MOF (Managed Object Format) et inclut toutes les propriétés héritées. Les propriétés sont répertoriées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, UUID("{1008CCED-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_MonitorSetting : CIM_ElementSetting
{
  CIM_MonitorResolution REF Setting;
  CIM_DesktopMonitor    REF Element;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ MonitorSetting** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ MonitorSetting** possède les propriétés suivantes.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ desktopmonitor**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("element")
</dt> </dl>

[**\_ Desktopmonitor CIM**](cim-desktopmonitor.md) décrivant le moniteur de bureau.

</dd> <dt>

**Paramètre**
</dt> <dd> <dl> <dt>

Type de données : **CIM \_ MonitorResolution**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("paramètre")
</dt> </dl>

[**\_ MonitorResolution CIM**](cim-monitorresolution.md) décrivant la résolution de l’analyseur associée à l’analyseur de bureau.

</dd> </dl>

## <a name="remarks"></a>Remarques

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

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> </dl>

 

