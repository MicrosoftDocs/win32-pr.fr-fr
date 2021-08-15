---
description: Récupère l’état de clé d’une clé.
ms.assetid: 4AEB732D-274E-42BB-AA97-9E4D30B81338
title: Méthode IsKeyPressed de la classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.IsKeyPressed
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bb8b4e2da0a6f1cd3c30e3d65404ecf308c71e88483e322193497216586b20b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392442"
---
# <a name="iskeypressed-method-of-the-msvm_keyboard-class"></a>Méthode IsKeyPressed de la \_ classe de clavier MSVM

Récupère l’état de clé d’une clé.

## <a name="syntax"></a>Syntaxe


```mof
uint32 IsKeyPressed(
  [in]  uint32  keyCode,
  [out] boolean keyState
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*keyCode* \[ dans\]
</dt> <dd>

Type : **UInt32**

Code de la clé virtuelle de la clé à interroger. Pour obtenir la liste des codes de touche virtuelle, consultez la page [**codes de clé virtuelle**](../inputdev/virtual-key-codes.md).

</dd> <dt>

*KeyState* \[ à\]
</dt> <dd>

Type : **booléen**

État actuel de la partie inférieure de la clé. Une valeur **true** signifie que la touche est enfoncée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Une valeur de retour de zéro indique une réussite. Une valeur différente de zéro indique un échec d’interrogation de l’état de la clé.

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

## <a name="remarks"></a>Remarques

La méthode **IsKeyPressed** retourne toujours la **valeur false** pour le **\_ menu VK** (18), le **\_ contrôle VK** (17) et **VK \_ Shift** (16), car il ne s’agit pas de clés réelles sur un clavier. Ces codes de touches virtuelles sont toujours mappés à **VK \_ LMENU** (164), **VK \_ LCONTROL** (162) et **VK \_ LSHIFT** (160), respectivement, par les méthodes [**PressKey**](presskey-msvm-keyboard.md) et [**ReleaseKey**](releasekey-msvm-keyboard.md) .

L’accès à la classe de [**\_ clavier MSVM**](msvm-keyboard.md) peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_Clavier MSVM**](msvm-keyboard.md)
</dt> <dt>

[**Codes de clé virtuelle**](../inputdev/virtual-key-codes.md)
</dt> </dl>

 

