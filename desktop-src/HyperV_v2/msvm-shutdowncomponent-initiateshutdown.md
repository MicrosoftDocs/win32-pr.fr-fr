---
description: Lance une opération d’arrêt du système d’exploitation sur l’ordinateur virtuel enfant associé. Si la valeur zéro (0) est retournée, l’arrêt a été lancé avec succès. Tout autre code de retour indique une condition d’erreur.
ms.assetid: 946BBC62-5479-4AE0-8870-D0A07827B902
title: Méthode InitiateShutdown de la classe Msvm_ShutdownComponent (winreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ShutdownComponent.InitiateShutdown
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f128eb2babfed0c70aca063832e579ad254ca1b02d6beaefb451c64598faa8d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950398"
---
# <a name="initiateshutdown-method-of-the-msvm_shutdowncomponent-class"></a>Méthode InitiateShutdown de la \_ classe ShutdownComponent MSVM

Lance une opération d’arrêt du système d’exploitation sur l’ordinateur virtuel enfant associé. Si la valeur zéro (0) est retournée, l’arrêt a été lancé avec succès. Tout autre code de retour indique une condition d’erreur.

## <a name="syntax"></a>Syntaxe


```mof
uint32 InitiateShutdown(
  [in] boolean Force,
  [in] string  Reason
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Force* \[ dans\]
</dt> <dd>

Type : **booléen**

Indicateur qui, si la **valeur est true**, force la fermeture des applications malgré la non-enregistrement des données.

</dd> <dt>

*Raison* \[ dans\]
</dt> <dd>

Type : **chaîne**

Raison de l’opération d’arrêt. Il s’agit d’une chaîne définie par l’utilisateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Paramètres de méthode activés-tâche démarrée** (4096)
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
</dt> <dt>

**Fichier introuvable** (32779)
</dt> <dt>

**Le système n’est pas prêt** (32780)
</dt> <dt>

**L’ordinateur est verrouillé et ne peut pas être arrêté sans l’option force** (32781)
</dt> <dt>

**Un arrêt système est en cours** (32782)
</dt> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe [**MSVM \_ ShutdownComponent**](msvm-shutdowncomponent.md) peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| En-tête<br/>                   | <dl> <dt>Winreg. h</dt> </dl>                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ ShutdownComponent**](msvm-shutdowncomponent.md)
</dt> </dl>

 

