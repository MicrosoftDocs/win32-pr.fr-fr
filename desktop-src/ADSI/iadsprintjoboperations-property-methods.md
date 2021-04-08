---
title: Méthodes de propriété IADsPrintJobOperations (IADs. h)
description: Les méthodes de propriété de l’interface IADsPrintJobOperations lisent et écrivent les propriétés énumérées dans le tableau suivant. Pour plus d’informations sur les méthodes de propriété, consultez Méthodes de propriété d’interface.
ms.assetid: d1710bd4-e600-4d92-892a-16b4316851d4
ms.tgt_platform: multiple
keywords:
- Méthodes de propriété IADsPrintJobOperations ADSI
topic_type:
- apiref
api_name:
- IADsPrintJobOperations Property Methods
- IADsPrintJobOperations.Status
- IADsPrintJobOperations.get_Status
- IADsPrintJobOperations.TimeElapsed
- IADsPrintJobOperations.get_TimeElapsed
- IADsPrintJobOperations.PagesPrinted
- IADsPrintJobOperations.get_PagesPrinted
- IADsPrintJobOperations.Position
- IADsPrintJobOperations.get_Position
- IADsPrintJobOperations.put_Position
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2981fcdd8043c0eb0ee8b05cfd0331fe3abfabe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844013"
---
# <a name="iadsprintjoboperations-property-methods"></a>Méthodes de propriété IADsPrintJobOperations

Les méthodes de propriété de l’interface [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) lisent et écrivent les propriétés énumérées dans le tableau suivant. Pour plus d’informations sur les méthodes de propriété, consultez [méthodes de propriété d’interface](interface-property-methods.md).

## <a name="properties"></a>Propriétés

<dl> <dt>

**PagesPrinted**
</dt> <dd> <dl>

Contient le nombre de pages imprimées.

<dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PagesPrinted(
  [out] LONG* plPagesPrinted
);
```


</dt> </dl> </dd> <dt>

**Position**
</dt> <dd> <dl>

Contient la position de ce travail d’impression dans la file d’attente à l’impression.

<dt>

Type d’accès : lecture/écriture
</dt> <dt>

Type de données de script : **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Position(
  [out] LONG* plPosition
);
HRESULT put_Position(
  [in] LONG lPosition
);
```


</dt> </dl> </dd> <dt>

**État**
</dt> <dd> <dl>

Contient l’état actuel du travail d’impression comme indiqué par l’une des valeurs des [**constantes d’État du travail d’impression ADSI**](adsi-print-job-status-constants.md) .

<dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Status(
  [out] LONG* plStatus
);
```


</dt> </dl> </dd> <dt>

**TimeElapsed**
</dt> <dd> <dl>

Contient le nombre de millisecondes écoulées depuis le début du travail d’impression.

<dt>

Type d'accès : Lecture seule
</dt> <dt>

Type de données de script : **long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_TimeElapsed(
  [out] LONG* plTimeElapsed
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment les propriétés de [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations) peuvent être utilisées.


```VB
Dim pqo As IADsPrintQueueOperations
Dim pjo As IADsPrintJobOperations

On Error GoTo Cleanup

Set pqo = GetObject("WinNT://aMachine/aPrinter")
For Each pj In pqo.PrintJobs
    Set pjo = pj
    MsgBox pjo.PagesPrinted & " pages printed for job " & pj.Name
    If (pjo.position > 1) Then
        pjo.Position = pjo.status - 1
    End If
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set pqo = Nothing
    Set pjo = Nothing
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                            |
| En-tête<br/>                   | <dl> <dt>IADs. h</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IADsPrintJobOperations est défini en tant que 32FB6780-1ED0-11CF-A988-00AA006BC149<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob)
</dt> <dt>

[**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)
</dt> <dt>

[**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)
</dt> <dt>

[**Constantes d’État du travail d’impression ADSI**](adsi-print-job-status-constants.md)
</dt> </dl>

 

 





