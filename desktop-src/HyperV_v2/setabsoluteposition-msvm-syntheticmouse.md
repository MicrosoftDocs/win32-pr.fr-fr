---
description: Définit la position horizontale et verticale du curseur de la souris.
ms.assetid: 7845E10A-7F61-4134-BF81-AED5483F36AD
title: Méthode SetAbsolutePosition de la classe Msvm_SyntheticMouse (Dbdao. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetAbsolutePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4b8ffb3a4d415f76dedf30acba5869b4cc585eb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864889"
---
# <a name="setabsoluteposition-method-of-the-msvm_syntheticmouse-class"></a>Méthode SetAbsolutePosition de la \_ classe SyntheticMouse MSVM

Définit la position horizontale et verticale du curseur de la souris.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetAbsolutePosition(
  [in] sint32 horizontalPosition,
  [in] sint32 verticalPosition
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*horizontalPosition* \[ dans\]
</dt> <dd>

Type : **sint32**

Nouvelle position horizontale du curseur de la souris, en pixels.

</dd> <dt>

*verticalPosition* \[ dans\]
</dt> <dd>

Type : **sint32**

Nouvelle position verticale du curseur de la souris, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Une valeur de retour de zéro indique une réussite. Une valeur différente de zéro indique un échec de modification de la position de défilement.

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

L’accès à la classe [**MSVM \_ SyntheticMouse**](msvm-syntheticmouse.md) peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| En-tête<br/>                   | <dl> <dt>Dbdao. h</dt> </dl>                      |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ SyntheticMouse**](msvm-syntheticmouse.md)
</dt> </dl>

 

