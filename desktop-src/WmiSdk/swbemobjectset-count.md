---
description: Utilisez la propriété Count de l’objet SWbemObjectSet pour déterminer le nombre d’éléments contenus dans une collection SWbemObjectSet. Cette propriété est en lecture seule.
ms.assetid: ad3d1265-a11e-4962-b1f3-60092d2f79ef
ms.tgt_platform: multiple
title: Propriété SWbemObjectSet. Count (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Count
- ISWbemObjectSet.Count
- ISWbemObjectSet.get_Count
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c1305cc0119f002f8ac3229664227d5c21bea9d865eedb0a31fcb7eb77250424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857229"
---
# <a name="swbemobjectsetcount-property"></a>Propriété SWbemObjectSet. Count

Utilisez la propriété **Count** de l’objet [**SWbemObjectSet**](swbemobjectset.md) pour déterminer le nombre d’éléments contenus dans une collection **SWbemObjectSet** . Cette propriété est en lecture seule.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
SWbemObjectSet.Count As Integer
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

L’une des points à prendre en compte lors de l’utilisation de Count est que WMI ne continue pas à s’exécuter avec le nombre d’éléments d’une collection. Si vous demandez un nombre pour une collection, WMI ne peut pas répondre instantanément avec un chiffre ; au lieu de cela, il doit littéralement compter les éléments, en énumérant l’ensemble de la collection. Pour une collection qui a relativement peu d’éléments, tels que des services, cette énumération prend probablement moins d’une seconde. Toutefois, le nombre d’événements dans une collection de journaux des événements peut prendre beaucoup plus de temps.

Supposons que vous souhaitez afficher les valeurs de propriété pour chaque événement de la collection. Dans ce cas, WMI devra énumérer la totalité de la collection une deuxième fois.

> [!Note]  
> Si vous tentez d’obtenir cette propriété à partir d’un objet [**SWbemObjectSet**](swbemobjectset.md) qui est retourné à partir d’une méthode où les indicateurs spécifiés sont inclus dans l’indicateur wbemFlagForwardOnly, vous obtiendrez une erreur wbemErrFailed.

 

## <a name="examples"></a>Exemples

Pour l’essentiel, la seule chose que vous feriez avec une SWbemObjectSet est d’énumérer tous les objets contenus dans la collection elle-même. Toutefois, le nombre de nombres qui peut être utile dans les scripts d’administration de système. Comme son nom l’indique, count indique le nombre d’éléments dans la collection. Par exemple, ce script récupère une collection de tous les services installés sur un ordinateur, puis renvoie le nombre total de services trouvés :


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
Wscript.Echo "Services installed on target computer: " & colSWbemObjectSet.Count

```



Ce qui rend le nombre utile, c’est qu’il peut vous indiquer si une instance spécifique est disponible sur un ordinateur. Par exemple, ce script récupère une collection de tous les services sur un ordinateur portant le nom W3SVC. Si le nombre est égal à 0 (et qu’il est valide pour les collections qui n’ont pas d’instances), cela signifie que le service W3SVC n’est pas installé sur l’ordinateur.


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
    ("SELECT * FROM Win32_Service WHERE Name='w3svc'")
If colSWbemObjectSet.Count = 0 Then
    Wscript.Echo "W3SVC service is not installed on target computer."
Else
    For Each objSWbemObject In colSWbemObjectSet
        ' Perform task on World Wide Web Publishing service.
    Next
End If
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



 

 




