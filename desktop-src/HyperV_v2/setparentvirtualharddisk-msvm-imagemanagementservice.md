---
description: Met à jour le parent pour les fichiers de disque dur virtuel enfants et de feuille spécifiés.
ms.assetid: 5ad41218-bcfd-449a-a66e-2096a1d96bf5
title: Méthode SetParentVirtualHardDisk de la classe Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetParentVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 47be9f3f383da237a3679633ac1d663bbc81ef078a7529662b8f21d10246761f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050539"
---
# <a name="setparentvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Méthode SetParentVirtualHardDisk de la \_ classe ImageManagementService MSVM

Met à jour le parent pour les fichiers de disque dur virtuel enfants et de feuille spécifiés. Consultez la section Notes pour connaître les restrictions d’utilisation de cette méthode.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetParentVirtualHardDisk(
  [in]  string              ChildPath,
  [in]  string              ParentPath,
  [in]  string              LeafPath,
  [in]  boolean             IgnoreIDMismatch,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Childpath* \[ dans\]
</dt> <dd>

Chemin qualifié complet qui spécifie l’emplacement du fichier de disque dur virtuel enfant.

</dd> <dt>

*ParentPath* \[ dans\]
</dt> <dd>

Chemin qualifié complet qui spécifie l’emplacement du fichier de disque dur virtuel parent.

</dd> <dt>

*LeafPath* \[ dans\]
</dt> <dd>

Chemin qualifié complet qui spécifie l’emplacement du fichier de disque dur virtuel feuille. Le paramètre peut avoir la **valeur null** si le disque dur virtuel est hors connexion, mais doit être spécifié si le disque dur virtuel est en cours d’utilisation.

</dd> <dt>

*IgnoreIDMismatch* \[ dans\]
</dt> <dd>

Indique si le parent doit être défini de force lorsque les identificateurs de disque virtuel ne correspondent pas. Ce paramètre doit être utilisé avec précaution, car si le nouveau disque dur virtuel parent n’est pas identique au parent d’origine, des données peuvent être endommagées.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.

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
</dt> </dl>

## <a name="remarks"></a>Remarques

Seuls les types de disques durs virtuels suivants peuvent être utilisés avec cette méthode :

-   Disque dur virtuel de différenciation
-   VHDX de différenciation

L’accès à la classe [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

