---
description: La propriété d’espace de noms de l’objet SWbemObjectPath contient le nom de l’espace de noms qui fait partie du chemin d’accès de l’objet.
ms.assetid: be88670d-6f0d-4b9d-886f-3e70bf4758ed
ms.tgt_platform: multiple
title: Propriété SWbemObjectPath. Namespace (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Namespace
- ISWbemObjectPath.Namespace
- ISWbemObjectPath.get_Namespace
- ISWbemObjectPath.put_Namespace
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f9daa9b74918c16d58546f6830bb474e40e449a8c596f61f7e27f03342c47b4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503759"
---
# <a name="swbemobjectpathnamespace-property"></a>Propriété SWbemObjectPath. Namespace

La propriété d' **espace de noms** de l’objet [**SWbemObjectPath**](swbemobjectpath.md) contient le nom de l’espace de noms qui fait partie du chemin d’accès de l’objet. Par exemple, le chemin d’accès suivant montre la propriété d’espace de noms qui retourne \\ cimv2 racine :

``` syntax
\\computer\root\cimv2:win32_logicaldisk="a:"
```

Pour plus d’explications sur la syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
SWbemObjectPath.Namespace As String
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="examples"></a>Exemples

L’exemple suivant montre comment obtenir le nom de l’espace de noms à partir d’instances de disques [**\_ logiques Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) qui sont des disques durs. Le script se connecte à l’espace de noms par défaut.


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer)

Set colDisks = objWMIService.ExecQuery _
    ("Select * from Win32_LogicalDisk " _
    & "Where DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
    Set objpath = objDisk.path_
    Wscript.Echo "Path of Win32_Logical disk instance " _
    & objDisk.DeviceID & " = " & objpath.Namespace   
Next
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



 

