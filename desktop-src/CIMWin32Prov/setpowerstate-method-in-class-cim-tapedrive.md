---
description: La méthode SetPowerState de la classe CIM CIM \_ définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État.
ms.assetid: 73f98d08-49da-4b21-91c4-cbe420c648e4
ms.tgt_platform: multiple
title: Méthode SetPowerState de la classe CIM_TapeDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a6efcfe08dfddca3477081f65fac35780f713005
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524151"
---
# <a name="setpowerstate-method-of-the-cim_tapedrive-class"></a>Méthode SetPowerState de la classe CIM CIM \_

La méthode **SetPowerState** de la classe CIM CIM \_ définit l’état d’alimentation souhaité pour un périphérique logique et lorsqu’un appareil doit être placé dans cet État. Dans une sous-classe, l’ensemble des codes de retour possibles doit être spécifié à l’aide d’un qualificateur **ValueMap** sur la méthode. Les chaînes dans lesquelles le contenu **ValueMap** est traduit doivent également être spécifiées dans la sous-classe en tant que qualificateur de tableau de **valeurs** . Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PowerState* \[ dans\]
</dt> <dd>

Valeur **ValueMap** qui spécifie l’état d’alimentation souhaité pour cet appareil logique.

<dt>

1
</dt> <dd>

Toute la puissance.

</dd> <dt>

2
</dt> <dd>

Économie d’énergie en mode faible consommation d’énergie.

</dd> <dt>

3
</dt> <dd>

Économie d’énergie en veille.

</dd> <dt>

4
</dt> <dd>

Économie d’énergie.

</dd> <dt>

5
</dt> <dd>

Cycle d’alimentation.

</dd> <dt>

6
</dt> <dd>

Mise hors tension.

</dd> </dl> </dd> <dt>

*Heure* \[ dans\]
</dt> <dd>

Spécifie quand l’état d’alimentation doit être défini comme une valeur de date et d’heure régulière ou comme une valeur d’intervalle (où l’intervalle commence lorsque l’appel de la méthode est reçu). Lorsque le paramètre *PowerState* est égal à 5 (« Power cycle »), le paramètre *Time* indique quand l’appareil doit se rallumer. La mise hors tension est immédiate.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 (zéro) en cas de réussite, 1 (un) si la demande *PowerState* et *Time* spécifiée n’est pas prise en charge, et une autre valeur si une autre erreur s’est produite.

## <a name="remarks"></a>Notes

Actuellement, cette méthode n’est pas implémentée par WMI. Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.

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

[CIM \_ CIM](setpowerstate-method-in-class-cim-tapedrive.md)
</dt> <dt>

[**CIM \_ CIM**](cim-tapedrive.md)
</dt> </dl>

 

 




