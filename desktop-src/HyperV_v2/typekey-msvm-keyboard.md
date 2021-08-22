---
description: Simule une séquence de touches d’appui sur la touche.
ms.assetid: 4166BA71-315D-41BD-857C-48AFB702911E
title: Méthode TypeKey de la classe Msvm_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.TypeKey
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d387e1b0d0d939d997589c90195b4a50427f1973eaf46520a0fa70caf62c610b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068349"
---
# <a name="typekey-method-of-the-msvm_keyboard-class"></a>Méthode TypeKey de la \_ classe de clavier MSVM

Simule une séquence de touches d’appui sur la touche. Cela équivaut à appeler [**PressKey**](presskey-msvm-keyboard.md) suivi de [**ReleaseKey**](releasekey-msvm-keyboard.md).

## <a name="syntax"></a>Syntaxe


```mof
uint32 TypeKey(
  [in] uint32 keyCode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*keyCode* \[ dans\]
</dt> <dd>

Type : **UInt32**

Code de la touche virtuelle de la touche sur laquelle appuyer. Pour obtenir la liste des codes de touche virtuelle, consultez la page [**codes de clé virtuelle**](../inputdev/virtual-key-codes.md).

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

## <a name="remarks"></a>Remarques

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

 

