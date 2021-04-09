---
description: Place le service représenté par l' \_ objet Win32 PrinterDriver dans l’état arrêté.
ms.assetid: 0e730fe6-ff9f-4866-a255-be6d372f2d7d
ms.tgt_platform: multiple
title: Méthode StopService de la classe Win32_PrinterDriver (Sdoias. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: faed7e9ed22ddcacbd8720e589463fd9a75fd87a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033693"
---
# <a name="stopservice-method-of-the-win32_printerdriver-class"></a>Méthode StopService de la \_ classe PrinterDriver Win32

La méthode de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **StopService** place le service représenté par l’objet [**Win32 \_ PrinterDriver**](win32-printerdriver.md) à l’état arrêté.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 StopService();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur. Pour obtenir des valeurs différentes de celles répertoriées dans la liste suivante, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

**0**
</dt> <dd>

Le service s’est arrêté correctement.

</dd> <dt>

**1**
</dt> <dd>

Demande non prise en charge.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                        |
| En-tête<br/>                   | <dl> <dt>Sdoias. h</dt> </dl>           |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> <dt>

[**\_PrinterDriver Win32**](win32-printerdriver.md)
</dt> </dl>

 

