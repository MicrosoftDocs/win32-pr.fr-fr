---
description: Vous pouvez utiliser la méthode AddAsString de l’objet SWbemPrivilegeSet pour ajouter un privilège à une collection SWbemPrivilegeSet à l’aide d’une chaîne de privilèges.
ms.assetid: 729ed4e3-2c5c-4bb4-acc6-cf9ad0d5eaf1
ms.tgt_platform: multiple
title: Méthode SWbemPrivilegeSet. AddAsString (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
- ISWbemPrivilegeSet.AddAsString
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b3a740141b14766080a09d01b36b5c0202351eda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543745"
---
# <a name="swbemprivilegesetaddasstring-method"></a>Méthode SWbemPrivilegeSet. AddAsString

Vous pouvez utiliser la méthode **AddAsString** de l’objet [**SWbemPrivilegeSet**](swbemprivilegeset.md) pour ajouter un privilège à une collection **SWbemPrivilegeSet** à l’aide d’une chaîne de privilèges. Utilisez cette méthode pour ajouter un privilège ou pour activer un privilège pour les objets [**SWbemSecurity**](swbemsecurity.md) . Consultez [exécution d’opérations privilégiées à l’aide de VBScript](executing-privileged-operations-using-vbscript.md).

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objPrivilege = .AddAsString( _
  ByVal strPrivilege, _
  [ ByVal bIsEnabled ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*strPrivilege* 
</dt> <dd>

Obligatoire. Une des chaînes de privilège. Pour obtenir la liste complète de ces chaînes et des constantes WMI associées, consultez [**constantes de privilège**](privilege-constants.md). Chaque chaîne de privilège représente un privilège spécifique. Par exemple, pour ajouter le privilège qui utilise pour arrêter un système informatique, utilisez la chaîne **SeShutdownPrivilege** .

</dd> <dt>

*bIsEnabled* \[ facultatif\]
</dt> <dd>

Valeur booléenne qui active ou désactive ce privilège. La valeur par défaut est **True**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cette méthode retourne un objet [**SWbemPrivilege**](swbemprivilege.md) qui représente le nouveau privilège. Dans le cas contraire, un objet null est retourné.

## <a name="error-codes"></a>Codes d’erreur

À la fin de la méthode **AddAsString** , l’objet **Err** peut contenir le code d’erreur figurant dans la liste suivante.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erreur non spécifiée.

</dd> </dl>

## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant crée un nouveau port pour un serveur d’impression à l’aide de [**Win32 \_ TCPIPPrinterPort**](/windows/desktop/CIMWin32Prov/win32-tcpipprinterport). **SeLoadDriverPrivilege** est requis pour cette opération. Consultez [exécution d’opérations privilégiées](executing-privileged-operations.md).


```VB
Set objWMIService = GetObject("Winmgmts:")
objWMIService.Security_.Privileges. _
    AddAsString "SeLoadDriverPrivilege", True
Set objNewPort = objWMIService.Get _
    ("Win32_TCPIPPrinterPort").SpawnInstance_
objNewPort.Name = "IP_111.222.111.11"
objNewPort.Protocol = 1
objNewPort.HostAddress = "111.222.111.11"
objNewPort.PortNumber = "9999"
objNewPort.SNMPEnabled = False
objNewPort.Put_
```



Un exemple de code qui utilise cette méthode est également décrit dans la rubrique [**SWbemPrivilegeSet**](swbemprivilegeset.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemPrivilegeSet<br/>                                                     |
| IID<br/>                      | IID \_ ISWbemPrivilegeSet<br/>                                                      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> <dt>

[**SWbemPrivilegeSet. Add**](swbemprivilegeset-add.md)
</dt> <dt>

[**SWbemPrivilegeSet. Remove**](swbemprivilegeset-remove.md)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Constantes de privilège**](privilege-constants.md)
</dt> <dt>

[Exécution des opérations privilégiées](executing-privileged-operations.md)
</dt> <dt>

[Exécution d’opérations privilégiées à l’aide de VBScript](executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

