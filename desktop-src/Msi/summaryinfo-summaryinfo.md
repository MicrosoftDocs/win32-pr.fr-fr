---
description: La propriété Property de l’objet SummaryInfo définit ou obtient la valeur de la propriété spécifiée dans le flux d’informations de résumé.
ms.assetid: 8e8f0987-c92b-43f3-a61a-35099188c629
title: Propriété SummaryInfo. Property
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3b8635d081b44adfad3b3e869cb7fab96ee3d81107a8d962153f1caa5a14ac72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624090"
---
# <a name="summaryinfoproperty-property"></a>Propriété SummaryInfo. Property

La propriété **Property** de l’objet [**SummaryInfo**](summaryinfo-object.md) définit ou obtient la valeur de la propriété spécifiée dans le flux d’informations de résumé. Les propriétés sont lues lorsque l’objet [**SummaryInfo**](summaryinfo-object.md) est créé, mais elles ne sont pas écrites tant que la méthode [**Persist**](summaryinfo-persist.md) n’est pas appelée. La définition d’une propriété sur Empty entraîne sa suppression ; de même, la demande d’une propriété inexistante retourne une valeur vide. Sinon, les valeurs peuvent être transférées comme des chaînes, des entiers ou des types date (date/heure).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = SummaryInfo.Property
```



## <a name="property-value"></a>Valeur de la propriété

ID de propriété requis de l’une des propriétés de résumé.

## <a name="remarks"></a>Remarques

**ID de propriété de résumé standard**

(pas une énumération)



| Nom du paramètre     | Valeur | Description                                       |
|--------------------|-------|---------------------------------------------------|
| \_dictionnaire PID    | 0     | Format spécial, non pris en charge par l’objet SummaryInfo |
| \_page de codes PID      | 1     | VT \_ I2                                            |
| \_titre PID         | 2     | VT- \_ LPSTR                                         |
| \_objet PID       | 3     | VT- \_ LPSTR                                         |
| \_auteur PID        | 4     | VT- \_ LPSTR                                         |
| \_Mots clés PID      | 5     | VT- \_ LPSTR                                         |
| \_Commentaires PID      | 6     | VT- \_ LPSTR                                         |
| \_modèle PID      | 7     | VT- \_ LPSTR                                         |
| PID \_ LASTAUTHOR    | 8     | VT- \_ LPSTR                                         |
| PID \_ REVNUMBER     | 9     | VT- \_ LPSTR                                         |
| PID \_ edittime      | 10    | de VT \_ fileTime                                      |
| PID \_ LASTPRINTED   | 11    | de VT \_ fileTime                                      |
| PID \_ créer \_ DTM   | 12    | de VT \_ fileTime                                      |
| PID \_ LASTSAVE \_ DTM | 13    | de VT \_ fileTime                                      |
| PID \_ PageCount     | 14    | VT \_                                            |
| PID \_ WORDCOUNT     | 15    | VT \_                                            |
| ID de la PID \_     | 16    | VT \_                                            |
| \_miniature PID     | 17    | VT \_ CF (non pris en charge)                            |
| PID \_ appname       | 18    | VT- \_ LPSTR                                         |
| \_sécurité PID      | 19    | VT \_                                            |



 

**Types de données de propriété**

(pas une énumération)



| Nom du paramètre | Valeur | Description                                                                              |
|----------------|-------|------------------------------------------------------------------------------------------|
| VT \_ I2         | 2     | Entier de 16 bits                                                                           |
| VT \_         | 3     | Entier de 32 bits                                                                           |
| VT- \_ LPSTR      | 30    | String                                                                                   |
| de VT \_ fileTime   | 64    | Date et heure (FILETIME, converties en heure variant)                                          |
| \_CF VT         | 71    | Format du presse-papiers + données, non géré par l’objet [**SummaryInfo**](summaryinfo-object.md) |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo est défini en tant que 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)
</dt> <dt>

[**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)
</dt> </dl>

 

 




