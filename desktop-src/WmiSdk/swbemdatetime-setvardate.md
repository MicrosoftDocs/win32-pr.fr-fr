---
description: Convertit une date au \_ format de date VT au format DateTime CIM.
ms.assetid: 24c39d44-22ac-44ac-9e05-72a5b666ab19
ms.tgt_platform: multiple
title: Méthode SWbemDateTime. SetVarDate (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetVarDate
- ISWbemDateTime.SetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 56d193bd2faffd51507ec4a913c7ee068b055dcf45ca756e801431659768c47d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050097"
---
# <a name="swbemdatetimesetvardate-method"></a>Méthode SWbemDateTime. SetVarDate

La méthode **SetVarDate** de l’objet [**SWbemDateTime**](swbemdatetime.md) convertit une date au format de **\_ Date VT** au format [DateTime CIM](date-and-time-format.md) .

une valeur de **\_ DATE VT** est une valeur datetime variant qui Visual Basic et ActiveX utiliser.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemDateTime.SetVarDate( _
  ByVal vdate, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Vdate* \[ dans\]
</dt> <dd>

Valeur de date de la variante pour définir l’objet. Ce paramètre doit être au format **de \_ Date VT** .

</dd> <dt>

*bIsLocal* \[ dans, facultatif\]
</dt> <dd>

Si la **valeur est true**, *Vdate* est interprété comme une heure locale et la propriété de temps universel coordonné (UTC, Universal Time Coordinated) contient l’heure locale convertie en décalage UTC correct. Quand *bIsLocal* a la valeur **false**, *Vdate* est converti directement en valeur UTC avec un décalage de zéro (0).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **SetVarDate** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir le code d’erreur figurant dans la liste suivante.

<dl> <dt>

**wbemErrInvalidSyntax** -2147749921 (0x80041021)
</dt> <dd>

Le format de *Vdate* n’est pas valide.

</dd> </dl>

## <a name="remarks"></a>Remarques

Après un appel réussi à **SetVarDate**, la valeur [**DateTime**](datetime.md) est interprétée comme une valeur DateTime absolue au lieu d’un intervalle, et la propriété [**IsInterval**](swbemdatetime-isinterval.md) a la valeur **false**.

la fonction intrinsèque Visual Basic ou VBScript function [CDate](/previous-versions//2dt118h2(v=vs.85)) fournit une valeur [**datetime**](datetime.md) au format de **\_ DATE VT** pour l’entrée dans **SetVarDate**.

## <a name="examples"></a>Exemples

Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md). Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).

L’exemple de code VBScript [date to WMI Date-Time format](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) VBScript de la Galerie TechNet utilise SetVarDate pour convertir une valeur date-heure normale au format date-heure UTC.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemDateTime<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemDateTime<br/>                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemDateTime.SetFileTime**](swbemdatetime-setfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Date/heure**](datetime.md)
</dt> </dl>

 

