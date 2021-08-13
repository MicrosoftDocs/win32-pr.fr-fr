---
description: Utilisé pour contrôler la collection de mesures pour un ou des éléments managés.
ms.assetid: 3DC043ED-A790-4322-BF80-55961E9946C2
title: Méthode ControlMetrics de la classe Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 051a08f261432c817bc0e56cab323c56cd11935c1541c40357b6b151a14f4074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118645845"
---
# <a name="controlmetrics-method-of-the-msvm_metricservice-class"></a>Méthode ControlMetrics de la \_ classe MetricService MSVM

Utilisé pour contrôler la collection de mesures pour un ou des éléments managés.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Objet* \[ dans\]
</dt> <dd>

Instance [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) qui identifie les éléments managés pour lesquels des mesures seront collectées. Si ce paramètre a la **valeur null**, les métriques de tous les éléments managés associés au paramètre de *définition* seront collectées.

</dd> <dt>

*Définition* \[ de dans\]
</dt> <dd>

Instance [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) qui spécifie les métriques qui seront collectées. Si ce paramètre a la **valeur null**, les métriques de toutes les définitions associées à l’élément géré identifié par le paramètre *Subject* sont collectées.

</dd> <dt>

*MetricCollectionEnabled* \[ dans\]
</dt> <dd>

Spécifie l’opération à effectuer sur la collection de mesures. Il doit s’agir de l’une des valeurs suivantes.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Activer** (2)


</dt> <dd>

Activez la collecte des métriques.

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Désactiver** (3)


</dt> <dd>

Désactivez la collecte des métriques.

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Réinitialiser** (4)


</dt> <dd>

Réinitialiser les valeurs des métriques.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF réservé** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fournisseur réservé** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.

<dl> <dt>

**Opération réussie** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> <dt>

**Échec** (2)
</dt> <dt>

**Méthode réservée** (..)
</dt> <dt>

**Spécifique au fournisseur** (32768.. 65535)
</dt> </dl>

## <a name="remarks"></a>Remarques

Cette méthode échouera dans les cas suivants :

-   Les paramètres *Subject* et *definition* ont tous deux la **valeur null**.
-   Les paramètres *Subject* et *definition* sont tous deux non **null** et il n’y a pas d’instance de [**MSVM \_ MetricDefForME**](msvm-metricdefforme.md) qui associe les deux instances.
-   Le paramètre de *définition* est une référence à une instance de [**MSVM \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) qui n’est pas associée [**au \_ MetricService MSVM**](msvm-metricservice.md) via [**MSVM \_ ServiceAffectsElement**](msvm-serviceaffectselement.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

