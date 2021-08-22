---
description: Décale la position du pointeur de la souris selon les deltas horizontaux et verticaux spécifiés.
ms.assetid: C74E4BEA-C7E1-44C7-B4FC-8926F23DF1FE
title: Méthode SetRelativePosition de la classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetRelativePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: dc3b0915795142b725ce26a2b8eac09dca613dc6094495fd3c188ba58aecbf1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147732"
---
# <a name="setrelativeposition-method-of-the-msvm_ps2mouse-class"></a>Méthode SetRelativePosition de la \_ classe Ps2Mouse MSVM

Décale la position du pointeur de la souris selon les deltas horizontaux et verticaux spécifiés.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetRelativePosition(
  [in] sint8 horizontalDelta,
  [in] sint8 verticalDelta
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*horizontalDelta* \[ dans\]
</dt> <dd>

Type : **sint8**

Modification horizontale de la position de la souris, en pixels.

</dd> <dt>

*verticalDelta* \[ dans\]
</dt> <dd>

Type : **sint8**

Modification verticale de la position de la souris, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Une valeur de retour de zéro indique une réussite. Une valeur différente de zéro indique un échec de modification de la position de la souris.

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

L’accès à la classe [**MSVM \_ Ps2Mouse**](msvm-ps2mouse.md) peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**MSVM \_ Ps2Mouse**](msvm-ps2mouse.md)
</dt> </dl>

 

