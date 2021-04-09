---
description: Récupère une valeur qui décrit l’état d’application de la stratégie Device Guard pour le code dynamique .NET.
ms.assetid: 11E6C631-0FF8-4DB2-931A-1012B3CA4357
title: WldpIsDynamicCodePolicyEnabled, fonction (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsDynamicCodePolicyEnabled
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 4df0555f89e9c575a7d97b69a5252c17936eb3d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110070"
---
# <a name="wldpisdynamiccodepolicyenabled-function"></a>WldpIsDynamicCodePolicyEnabled fonction)

Récupère une valeur qui décrit l’état d’application de la stratégie Device Guard pour le code dynamique .NET.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI WldpIsDynamicCodePolicyEnabled(
  _Out_ PBOOL  isEnabled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*IsEnabled* \[ à\]
</dt> <dd>

En cas de réussite, retourne la **valeur true** si la stratégie Device Guard applique la stratégie de code dynamique .net ; Sinon, retourne **false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne **S \_ OK** en cas de réussite ou un code d’échec dans le cas contraire.

## <a name="remarks"></a>Notes

Le code dynamique fait référence au code généré dynamiquement par la liste de révocation de certificats .NET.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1803 \[ uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




