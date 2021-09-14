---
description: La \_ propriété de sécurité de l’objet SWbemLocator est utilisée pour lire ou définir les paramètres de sécurité d’un objet SWbemLocator. Cette propriété est un objet SWbemSecurity.
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.tgt_platform: multiple
title: SWbemLocator.Security_, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.Security_
- ISWbemLocator.Security_
- ISWbemLocator.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c2aa61ebc3ef48c82405d960d5de42ab8f23dc53
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292802"
---
# <a name="swbemlocatorsecurity_-property"></a>SWbemLocator. Security, \_ propriété

La propriété de **\_ sécurité** de l’objet [**SWbemLocator**](swbemlocator.md) est utilisée pour lire ou définir les paramètres de sécurité d’un objet **SWbemLocator** . Cette propriété est un objet [**SWbemSecurity**](swbemsecurity.md) .

> [!Note]  
> La définition de la propriété de **sécurité \_** d’un objet [**SWbemLocator**](swbemlocator.md) sur la **valeur null** accorde à tout moment un accès illimité à tous les utilisateurs. Pour plus d’informations, consultez [**SWbemSecurity**](swbemsecurity.md).

 

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
SWbemLocator.Security_ As Object
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Notes

Les propriétés d’un objet **SWbemLocator. \_ Security** n’ont pas de valeurs par défaut. Si vous tentez d’obtenir la valeur de [**SWbemSecurity. AuthenticationLevel**](swbemsecurity-authenticationlevel.md) ou de [**SWbemSecurity. ImpersonationLevel**](swbemsecurity-impersonationlevel.md) sur un objet [**SWbemLocator**](swbemlocator.md) avant de le définir, une erreur [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) se produit.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLocator<br/>                                                          |
| IID<br/>                      | IID \_ ISWbemLocator<br/>                                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemLocator**](swbemlocator.md)
</dt> <dt>

[Création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Exécution d’opérations privilégiées à l’aide de VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[Définition de la sécurité des processus d' \_ application cliente \_](setting-client-application-process-security.md)
</dt> <dt>

[**Objet SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Sécurisation d’une connexion WMI à distance](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 




