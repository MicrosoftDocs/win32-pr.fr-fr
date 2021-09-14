---
description: Convertit une date au format FILETIME de chaîne au format DateTime CIM.
ms.assetid: e375afda-5e94-46d6-b1ac-e801e0f4a620
ms.tgt_platform: multiple
title: Méthode SWbemDateTime. SetFileTime (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ca3e36a284e3700e166e86f6786218bada8f369e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013055"
---
# <a name="swbemdatetimesetfiletime-method"></a>Méthode SWbemDateTime. SetFileTime

La méthode **SetFileTime** de l’objet [**SWbemDateTime**](swbemdatetime.md) convertit une date au format **fileTime** de chaîne au format [DateTime CIM](date-and-time-format.md) .

Le format **fileTime** est une structure datetime de 64 bits qui représente le nombre d’unités de 100 nanosecondes depuis le début du 1er janvier 1601. Windows WMI (Management Instrumentation) traite les valeurs **fileTime** comme des représentations sous forme de chaîne de nombres 64 bits non signés.

Pour plus d’explications sur la syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
SWbemDateTime.SetFileTime( _
  ByVal strFileTime, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strFileTime* \[ dans\]
</dt> <dd>

Valeur **fileTime** utilisée pour définir l’objet.

</dd> <dt>

*bIsLocal* \[ dans, facultatif\]
</dt> <dd>

Si la **valeur est true**, *strFileTime* est interprété comme une heure locale. La propriété temps universel coordonné (UTC, Universal Time Coordinated) contient l’heure locale convertie en décalage UTC correct. Quand *bIsLocal* a la valeur **false**, *strFileTime* est converti directement en valeur UTC avec un décalage égal à 0 (zéro).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **SetFileTime** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir le code d’erreur figurant dans la liste suivante.

<dl> <dt>

**wbemErrInvalidSyntax** -2147749921 (0x80041021)
</dt> <dd>

Le format de *strFileTime* n’est pas valide.

</dd> </dl>

## <a name="remarks"></a>Notes

Après un appel réussi à **SetFileTime**, la valeur [**DateTime**](datetime.md) est toujours interprétée comme une valeur absolue (**DateTime**) et [**IsInterval**](swbemdatetime-isinterval.md) est défini sur **false**.

## <a name="examples"></a>Exemples

Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md). Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).

## <a name="requirements"></a>Spécifications



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

[**SWbemDateTime.SetVarDate**](swbemdatetime-setvardate.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**Date/heure**](datetime.md)
</dt> </dl>

 

