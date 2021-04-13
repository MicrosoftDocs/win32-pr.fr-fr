---
description: La propriété Privileges est un objet SWbemPrivilegeSet. Cette propriété est utilisée pour activer ou désactiver des privilèges Windows spécifiques. Vous devrez peut-être définir l’un de ces privilèges pour effectuer des tâches spécifiques à l’aide de l’API Windows Management Instrumentation (WMI).
ms.assetid: 6e4cae22-23d6-4981-b38c-d298654e59ab
ms.tgt_platform: multiple
title: SWbemSecurity. Privileges, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.Privileges
- ISWbemSecurity.Privileges
- ISWbemSecurity.get_Privileges
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6fd8e1c0f9b6667b49d0956bcea5ac9e187443d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202147"
---
# <a name="swbemsecurityprivileges-property"></a>SWbemSecurity. Privileges, propriété

La propriété **Privileges** est un objet [**SWbemPrivilegeSet**](swbemprivilegeset.md) . Cette propriété est utilisée pour activer ou désactiver des privilèges Windows spécifiques. Vous devrez peut-être définir l’un de ces privilèges pour effectuer des tâches spécifiques à l’aide de l’API Windows Management Instrumentation (WMI).

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
SWbemSecurity.Privileges As Object
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Notes

Ce paramètre vous permet d’accorder ou de révoquer des privilèges dans le cadre d’une chaîne de moniker WMI. Pour obtenir la liste complète des valeurs applicables, consultez [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) et [**constantes de privilège**](privilege-constants.md).

Vous pouvez modifier les privilèges définis pour les objets [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)et [**SwbemLocator**](swbemlocator.md) en ajoutant des objets [**SWbemPrivilege**](swbemprivilege.md) à la propriété **Privileges** .

Il existe des différences fondamentales dans la façon dont les différentes versions de Windows gèrent les modifications des privilèges. Si vous développez une application qui est utilisée uniquement sur des plateformes Windows, vous pouvez définir ou révoquer des privilèges à tout moment.

L’exemple suivant définit **SeDebugPrivilege** sur la connexion initiale du moniker pour obtenir un objet [**SWbemServices**](swbemservices.md) .


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



Pour plus d’informations sur la façon de mettre en forme la chaîne de sécurité pour une connexion de moniker, consultez [**constantes de privilège**](privilege-constants.md).

L’exemple suivant effectue la même tâche, mais définit le privilège après la connexion initiale à WMI.


```VB
Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate}")
Service.Security_.Privileges.AddAsString "SeDebugPrivilege", True
```



Notez que pour les appels à [**SwbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md), vous devez utiliser le nom complet du privilège de sécurité, par exemple, « SeDebugPrivilege » au lieu de « Debug ».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSecurity<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemSecurity<br/>                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Exécution des opérations privilégiées](executing-privileged-operations.md)
</dt> <dt>

[**SWbemPrivilegeSet**](swbemprivilegeset.md)
</dt> </dl>

 

 




