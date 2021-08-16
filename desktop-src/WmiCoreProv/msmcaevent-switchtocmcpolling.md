---
description: Représente la gestion de la vérification de l’ordinateur (CMC) corrigée pour passer du pilote d’interruption à l’interrogation. cette classe est disponible uniquement dans les systèmes Windowss 64 bits.
ms.assetid: c5e99e13-0f65-40bc-8863-b2ca7ea221df
title: Classe MSMCAEvent_SwitchToCMCPolling
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SwitchToCMCPolling
- MSMCAEvent_SwitchToCMCPolling.Active
- MSMCAEvent_SwitchToCMCPolling.InstanceName
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: a8192dc83a50063b2aaabba2bf708053fadb8e094bfa1cab82b11b084f722a76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640939"
---
# <a name="msmcaevent_switchtocmcpolling-class"></a>MSMCAEvent \_ SwitchToCMCPolling, classe

La classe **MSMCAEvent \_ SwitchToCMCPolling** représente la gestion des machines (CMC) corrigée pour passer du pilote d’interruption à l’interrogation. Dans certains cas, le noyau interroge la couche d’abstraction système (SAL) pour toute erreur CMC ou une erreur de plateforme corrigée (CPE) qui s’est produite au cours de l’intervalle d’interrogation précédent. cette classe est disponible uniquement dans les systèmes Windowss 64 bits.

La syntaxe suivante est simplifiée du code format MOF (MOF) et comprend toutes ses propriétés héritées. Les propriétés et les méthodes sont classées par ordre alphabétique, et non par ordre MOF.

## <a name="syntax"></a>Syntaxe

``` syntax
class MSMCAEvent_SwitchToCMCPolling : WMIEvent
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Membres

La classe **MSMCAEvent \_ SwitchToCMCPolling** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSMCAEvent \_ SwitchToCMCPolling** possède les propriétés suivantes.

<dl> <dt>

**Actif**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**True** si cette instance de la classe est active ; Sinon, **false**.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Identificateur unique de cette instance de la classe.

</dd> </dl>

## <a name="remarks"></a>Remarques

La classe **MSMCAEvent \_ SwitchToCMCPolling** est dérivée de [**WmiEvent**](wmievent.md).

La couche d’abstraction système (SAL) est du code gravé sur la ROM que le système d’exploitation appelle pour effectuer des opérations dépendantes de la plateforme. Il est similaire au BIOS sur une plateforme x86. Dans les cas où la plateforme ne prend pas en charge les interruptions pour l’interrogation CMC ou CPE, le système d’exploitation interroge toutes les minutes, en vérifiant si une erreur s’est produite précédemment. Si la plateforme prend en charge les interruptions et que le système d’exploitation reçoit une quantité définie par l’utilisateur d’interrogations CMC ou CPE pendant une minute, elle désactive l’interruption et l’interrogation. Si l’utilisateur ne définit pas le nombre d’interrogations au bout d’une minute, le système définit une valeur par défaut de 10 interrogations par minute.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2003<br/>                                                         |
| Espace de noms<br/>                | \\WMI racine<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes MSMCA](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

