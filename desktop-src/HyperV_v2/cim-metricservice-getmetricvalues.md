---
description: Offre la possibilité de retourner une liste filtrée d' \_ instances BASEMETRICVALUE CIM.
ms.assetid: c207a0ef-11f1-42c4-af77-3dcf3fbff8a7
title: Méthode GetMetricValues de la classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d010128bdef9bec4ce7df5fb3b1021a80a6ac99bdfbaf797958a76b27a812479
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694999"
---
# <a name="getmetricvalues-method-of-the-cim_metricservice-class"></a>Méthode GetMetricValues de la \_ classe CIM MetricService

Offre la possibilité de retourner une liste filtrée d' [**instances \_ BaseMetricValue CIM**](cim-basemetricvalue.md) .

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Définition* \[ de dans\]
</dt> <dd>

Identifie un [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) pour lequel les métriques seront retournées.

</dd> <dt>

*Plage* \[ dans\]
</dt> <dd>

Identifie la manière dont les instances sont sélectionnées. L’algorithme de classement des instances de valeur est spécifique à la définition de métrique.

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

**Minimum** (2)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

**Maximum** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Spécifique au fournisseur** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> <dt>

*Nombre* \[ dans\]
</dt> <dd>

Identifie le nombre maximal d’instances qui doivent être retournées par la méthode.

</dd> <dt>

*Valeurs* \[ à\]
</dt> <dd>

Une fois la méthode terminée, contient des références à des instances [**de \_ BaseMetricValue CIM**](cim-basemetricvalue.md), filtrées en fonction des valeurs des paramètres d’entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite ; Sinon, retourne une erreur.

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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_METRICSERVICE CIM**](cim-metricservice.md)
</dt> </dl>

 

 




