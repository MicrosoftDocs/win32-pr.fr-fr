---
description: La méthode SetUrgency définit le niveau d’urgence souhaité pour une alarme.
ms.assetid: ac2e7fda-1317-440a-adbd-1ef0844d124c
ms.tgt_platform: multiple
title: Méthode SetUrgency de la classe CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.SetUrgency
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9557ad9e65b33e1ed8889ef1fd013b2d9f5426f8e819fe56608cb6846ea8669f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118172633"
---
# <a name="seturgency-method-of-the-cim_alarmdevice-class"></a>Méthode SetUrgency de la \_ classe CIM AlarmDevice

La méthode **SetUrgency** définit le niveau d’urgence souhaité pour une alarme.

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetUrgency(
  [in] uint16 RequestedUrgency
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*RequestedUrgency* \[ dans\]
</dt> <dd>

Fréquence relative à laquelle l’alarme clignote, vibre ou émet des tonalités audibles. Les valeurs suivantes proviennent de la propriété **urgence** dans [**CIM \_ AlarmDevice**](cim-alarmdevice.md).

<dt>

0
</dt> <dd>

Inconnu.

</dd> <dt>

1
</dt> <dd>

Autre.

</dd> <dt>

2
</dt> <dd>

Non pris en charge.

</dd> <dt>

3
</dt> <dd>

Informatif.

</dd> <dt>

4
</dt> <dd>

Non critique.

</dd> <dt>

5
</dt> <dd>

Critique.

</dd> <dt>

6
</dt> <dd>

Irrécupérable.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur 0 (zéro) en cas de réussite, 1 (un) si le niveau d’urgence demandé n’est pas pris en charge, et tout autre nombre pour indiquer une erreur.

## <a name="remarks"></a>Remarques

Actuellement, cette méthode n’est pas implémentée par WMI. Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_ALARMDEVICE CIM](seturgency-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[**\_ALARMDEVICE CIM**](cim-alarmdevice.md)
</dt> </dl>

 

