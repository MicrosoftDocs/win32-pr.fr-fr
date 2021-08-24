---
description: Crée un nouveau pilote d’imprimante.
ms.assetid: 23d9ec50-235a-4bf8-ab6b-be3509c3869f
ms.tgt_platform: multiple
title: Méthode AddPrinterDriver de la classe Win32_PrinterDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriver.AddPrinterDriver
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 14681c381f8c8b9abbc5b28ec763b959854e2303b9a0b87af762238f4e5a8d27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752799"
---
# <a name="addprinterdriver-method-of-the-win32_printerdriver-class"></a>Méthode AddPrinterDriver de la \_ classe Win32 PrinterDriver

La méthode de la classe **AddPrinterDriver** crée un nouveau pilote d’imprimante.

Cette rubrique utilise la syntaxe format MOF (MOF). Pour plus d’informations sur l’utilisation de cette méthode, consultez [appel d’une méthode](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Syntaxe


```mof
uint32 AddPrinterDriver(
  [in] Win32_PrinterDriver DriverInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DriverInfo* \[ dans\]
</dt> <dd>

Instance de la classe [**\_ PrinterDriver Win32**](win32-printerdriver.md) qui représente le pilote d’imprimante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’une des valeurs répertoriées dans la liste suivante ou toute autre valeur pour indiquer une erreur. Pour obtenir des valeurs différentes de celles répertoriées dans la liste suivante, consultez [**constantes d’erreur WMI**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

**0**
</dt> <dd>

Réussite.

</dd> <dt>

**5**
</dt> <dd>

Accès refusé.

</dd> <dt>

**87**
</dt> <dd>

Le paramètre est incorrect. Peut se produire lorsque l’objet n’est pas correctement rempli ou lorsque le pilote ne peut pas être trouvé dans le système. L’attribut Name peut également être différent du modèle spécifié dans le fichier. inf. Ou il se peut qu’il y ait une barre oblique inverse (« \\ ») manquante sur un attribut PathFile.

</dd> <dt>

**1797**
</dt> <dd>

Le pilote d’imprimante est inconnu.

</dd> </dl>

## <a name="remarks"></a>Remarques

> [!Note]  
> Lorsque vous utilisez la méthode **AddPrinterDriver** , vous devez utiliser **SeLoadDriverPrivilege** pour charger ou décharger un pilote de périphérique.

 

## <a name="examples"></a>Exemples

L’exemple de code de l'[installation d’un pilote d’imprimante introuvable dans les pilotes CAB](https://Gallery.TechNet.Microsoft.Com/1aac6333-a794-48d3-b7da-46d87df56ee1) en VBScript installe une imprimante hypothétique à l’aide d’un pilote d’impression introuvable dans Drivers.cab.

L’exemple VBScript suivant installe le pilote d’imprimante pour une imprimante Apple LaserWriter 8500.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
objWMIService.Security_.Privileges.AddAsString "SeLoadDriverPrivilege", True 
 
Set objDriver = objWMIService.Get("Win32_PrinterDriver") 
 
objDriver.Name = "NewPrinter Model 2900" 
objDriver.SupportedPlatform = "Windows NT x86" 
objDriver.Version = "3" 
objDriver.DriverPath = "C:\Scripts\NewPrinter.dll" 
objDriver.Infname = "C:\Scripts\NewPrinter.inf" 
intResult = objDriver.AddPrinterDriver(objDriver) 
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                      |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes matérielles du système informatique](computer-system-hardware-classes.md)
</dt> <dt>

[**\_PrinterDriver Win32**](win32-printerdriver.md)
</dt> </dl>

 

