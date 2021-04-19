---
description: Chaque propriété d’une classe d’affichage doit avoir un qualificateur de tableau de chaînes appelé PropertySources.
ms.assetid: df89680b-8ea7-4f38-81ba-c4132b944f37
ms.tgt_platform: multiple
title: Qualificateur PropertySources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertySources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3809977282a2bdf82d0b51ef8f566541b74fe28a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524936"
---
# <a name="propertysources-qualifier"></a>Qualificateur PropertySources

Chaque propriété d’une classe d’affichage doit avoir un qualificateur de tableau de chaînes appelé **PropertySources**. Le qualificateur **PropertySources** contient le nom de la ou des propriétés de classe source à partir desquelles cette propriété de la classe de vue obtient des données. L’ordre des valeurs de ce tableau correspond à l’ordre des classes sources définies pour le [qualificateur ViewSources](viewsources-qualifier.md). L’exemple suivant montre comment définir une propriété pour une classe d’affichage d’Union qui est l’Union de la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) à partir de deux ordinateurs différents :


```mof
[PropertySources{"DeviceID", "DeviceID"},key] String Devname;
```



La première propriété **DeviceID** correspond à la propriété **DeviceID** de la classe dans la première requête source. La deuxième propriété **DeviceID** est la propriété **DeviceID** de la classe dans la deuxième requête source.

Lors de la définition des propriétés des classes de vue de jointure, vous devez définir une propriété de vue distincte pour chacune des propriétés de la classe source, sauf si les propriétés de la classe source sont la base de la classe de vue de jointure. L’exemple suivant crée des propriétés dans une classe de vue de jointure sur des propriétés similaires de la classe source [**Win32 \_ Printer**](/windows/desktop/CIMWin32Prov/win32-printer) et de la classe source [**Win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) :


```mof
[PropertySources{"VerticalResolution", ""}] Uint32 Vres;
[PropertySources{"", "YResolution"}] Uint32 Yres;
```



Si les deux classes sources sont jointes par une propriété commune, vous ne pouvez définir qu’une seule propriété de classe d’affichage, car la valeur des deux propriétés de la classe source est toujours la même. L’exemple suivant montre comment joindre la classe [**Win32 \_ Printer**](/windows/desktop/CIMWin32Prov/win32-printer) et [**Win32 \_ PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) par une valeur de propriété commune :


```mof
[PropertySources{"DeviceId", "DeviceName "}] String Name;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Qualificateurs spécifiques au fournisseur de vues**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

