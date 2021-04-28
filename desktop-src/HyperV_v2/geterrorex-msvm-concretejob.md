---
description: 'Méthode GetErrorEx de la classe Msvm_ConcreteJob : récupère les objets d’erreur pour le travail, le cas échéant.'
ms.assetid: B4B4F60C-9221-4125-8D42-F0F1D32C3E79
title: Méthode GetErrorEx de la classe Msvm_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 67abbd06fdaae9c23cca53f5516586f45216f20d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119347"
---
# <a name="geterrorex-method-of-the-msvm_concretejob-class"></a>Méthode GetErrorEx de la \_ classe ConcreteJob MSVM

Récupère les objets d’erreur pour le travail, le cas échéant. Lorsque le travail est en cours d’exécution ou s’est terminé sans erreur, cette méthode ne retourne aucune instance d' [**\_ erreur MSVM**](msvm-error.md) . Toutefois, si la tâche a échoué en raison d’un problème interne ou parce que la tâche a été arrêtée par un client, une ou plusieurs instances d' **\_ erreur MSVM** sont retournées.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Erreurs* \[ à\]
</dt> <dd>

Type : **chaîne \[ \]**

Si l’état opérationnel du travail n’est pas 2 (OK), cette méthode retourne une ou plusieurs instances incorporées de la classe d' [**\_ erreur MSVM**](msvm-error.md) , au format CIM-XML, qui représentent les erreurs rencontrées dans le travail. Si l’état opérationnel du travail est 2 (OK), la **valeur null** est retournée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **UInt32**

Cette méthode retourne l’une des valeurs suivantes.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Échec** (32768)
</dt> <dt>

**Accès refusé** (32769)
</dt> <dt>

**Non pris en charge** (32770)
</dt> <dt>

**État inconnu** (32771)
</dt> <dt>

**Délai d’expiration** (32772)
</dt> <dt>

**Paramètre non valide** (32773)
</dt> <dt>

Le **système est en cours d’utilisation** (32774)
</dt> <dt>

**État non valide pour cette opération** (32775)
</dt> <dt>

**Type de données incorrect** (32776)
</dt> <dt>

Le **système n’est pas disponible** (32777)
</dt> <dt>

**Mémoire insuffisante** (32778)
</dt> </dl>

## <a name="remarks"></a>Notes 

L’accès à la classe [**MSVM \_ ConcreteJob**](msvm-concretejob.md) peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ ConcreteJob**](msvm-concretejob.md)
</dt> </dl>

 

