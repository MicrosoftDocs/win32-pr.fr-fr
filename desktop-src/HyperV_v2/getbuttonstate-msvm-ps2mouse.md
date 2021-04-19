---
description: Récupère l’état actuel du bouton de périphérique spécifié.
ms.assetid: 7772A3AC-1677-44A7-9E5E-D31E90988705
title: Méthode GetButtonState de la classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8bb0df6ad49f0d260d95c6f65e0f0f481b393dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515271"
---
# <a name="getbuttonstate-method-of-the-msvm_ps2mouse-class"></a>Méthode GetButtonState de la \_ classe Ps2Mouse MSVM

Récupère l’état actuel du bouton de périphérique spécifié.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean buttonState
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*buttonIndex* \[ dans\]
</dt> <dd>

Type : **UInt32**

Index de base 1 du bouton à interroger.

</dd> <dt>

*ButtonState* \[ à\]
</dt> <dd>

Type : **booléen**

État actuel du bouton enfoncé. Une valeur **true** signifie que le bouton est enfoncé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Une valeur de retour de zéro indique une réussite. Une valeur différente de zéro indique un échec de requête.

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

L’accès à la classe [**MSVM \_ Ps2Mouse**](msvm-ps2mouse.md) peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**MSVM \_ Ps2Mouse**](msvm-ps2mouse.md)
</dt> </dl>

 

