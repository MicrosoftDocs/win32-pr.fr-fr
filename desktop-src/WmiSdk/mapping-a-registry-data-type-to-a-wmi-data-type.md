---
description: L’application doit créer les propriétés avec un type de données mappé au type de données de registre.
ms.assetid: aa86565c-47eb-40d3-a533-03464cd1c6cd
ms.tgt_platform: multiple
title: Mappage d’un type de données de Registre à un type de données WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e620d51eee52592df946e822165d8ed1833214c6f75519d4274b0d7fe3f5550c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050687"
---
# <a name="mapping-a-registry-data-type-to-a-wmi-data-type"></a>Mappage d’un type de données de Registre à un type de données WMI

L’application doit créer les propriétés avec un type de données mappé au type de données de registre. Vous n’avez pas besoin de spécifier le type de données de Registre dans les méthodes qui créent, obtiennent ou définissent des valeurs de registre. Toutefois, le paramètre d’entrée qui contient la valeur doit être dans le type de données WMI correct. Par exemple, si une application reçoit des données **reg \_ DWORD** du Registre, la classe qui reçoit les données doit inclure une propriété **UInt32** .

Le tableau suivant répertorie le mappage entre les types de données de Registre et WMI utilisés dans les méthodes [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) .



| Type de données de Registre      | Type de données WMI                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_fichier binaire reg**         | tableau **UInt8**<br/> Tableau de valeurs qui ne dépassent pas 255 ou Hex FF. par exemple, le code de Script Visual Basic suivant crée un tableau qui correspond à ce type de données.<br/> `BinArray = Array(&H01, &Ha2)`<br/> La méthode de la classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov) requiert le type de données **\_ Binary reg** .<br/>                                                                                          |
| **\_valeur DWORD reg**          | **uint32**, **sint32** ou Visual Basic **entier**<br/> Valeur 32 bits unique. Les méthodes de la classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**GetDWORDValue**](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov) et [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov) requièrent le type de données **reg \_ DWORD** .<br/>                                                                                                                                                                  |
| **SZ de REG \_**             | **string**<br/> La méthode de la classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) requiert le type de données **reg \_ SZ** .<br/>                                                                                                                                                                                                                                                                                                            |
| **\_q QWord**          | **UInt64**.<br/> Valeur 64 bits unique. Les méthodes de la classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**GetQWORDValue**](/previous-versions/windows/desktop/regprov/getqwordvalue-method-in-class-stdregprov) et [**SetQWORDValue**](/previous-versions/windows/desktop/regprov/setqwordvalue-method-in-class-stdregprov) requièrent le type de données **reg \_ QWord** .<br/>                                                                                                                                                                                                         |
| **REG \_ développer \_ SZ**     | **string**<br/> Les chaînes développées sont des chaînes spéciales qui représentent des variables d’environnement système. Par exemple, le code VBScript suivant crée une chaîne qui représente la variable d’environnement de l' **\_ \_ utilisateur local HKEY** Temp.<br/> `TEMP = "%USERPROFILE\LocalSettings\Temp%"`<br/> La méthode de la classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) requiert le type de données **reg \_ expand \_ SZ** .<br/> |
| **REG \_ multiple \_ SZ**      | Tableau de **chaînes**<br/> Le type de données multichaîne contient plusieurs chaînes. Par exemple, le code VBScript suivant crée un tableau qui correspond à ce type de données.<br/> `MultiValue = Array("first", "second", "third")`<br/> La méthode de la classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) requiert le type de données **reg \_ multiple \_ SZ** .<br/>                                                                     |
| **\_liste des ressources reg \_** | Selon le cas Pour plus d’informations, consultez [Description d’une ressource pour le registre](describing-a-resource-for-the-registry.md).<br/>                                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition des classes pour le fournisseur de Registre système](defining-classes-for-the-system-registry-provider.md)
</dt> </dl>

 

