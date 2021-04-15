---
description: Simule une version de clé.
ms.assetid: EAE84BD5-ECEA-44E7-A7AB-CD18299DF2FE
title: Méthode ReleaseKey de la classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.ReleaseKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2193a4b78128ff3f65e98b4425528a51f6cf5916
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530100"
---
# <a name="releasekey-method-of-the-msvm_keyboard-class"></a>Méthode ReleaseKey de la \_ classe de clavier MSVM

Simule une version de clé. En cas de réussite, la clé sera à l’État up.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ReleaseKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*keyCode* \[ dans\]
</dt> <dd>

Type : **UInt32**

Code de la clé virtuelle à libérer. Pour obtenir la liste des codes de touche virtuelle, consultez la page [**codes de clé virtuelle**](../inputdev/virtual-key-codes.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Une valeur de retour de zéro indique une réussite. Une valeur différente de zéro indique un échec de modification de l’état de la clé.

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
</dt> </dl>

## <a name="remarks"></a>Notes

La méthode **ReleaseKey** mappe les références au **\_ menu VK** (18), **au \_ contrôle VK** (17) et à **VK \_ Shift** (16) **à VK \_ LMENU** (164), **VK \_ LCONTROL** (162) et **VK \_ LSHIFT** (160), respectivement, car le **\_ menu VK**, le **\_ contrôle VK** et les codes de touches virtuelles **VK \_ Shift** ne représentent pas des clés réelles sur un clavier.

L’accès à la classe de [**\_ clavier MSVM**](msvm-keyboard.md) peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_Clavier MSVM**](msvm-keyboard.md)
</dt> <dt>

[**Codes de clé virtuelle**](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

