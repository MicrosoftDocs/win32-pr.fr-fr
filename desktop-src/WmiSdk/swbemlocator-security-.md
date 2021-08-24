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
ms.openlocfilehash: 6c5fa2ba102de1135c0019e2dcfb291f55672cabb00cea1c59d8a655f21c882e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955169"
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

## <a name="remarks"></a>Remarques

Les propriétés d’un objet **SWbemLocator. \_ Security** n’ont pas de valeurs par défaut. Si vous tentez d’obtenir la valeur de [**SWbemSecurity. AuthenticationLevel**](swbemsecurity-authenticationlevel.md) ou de [**SWbemSecurity. ImpersonationLevel**](swbemsecurity-impersonationlevel.md) sur un objet [**SWbemLocator**](swbemlocator.md) avant de le définir, une erreur [wbemErrFailed](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum) se produit.

## <a name="requirements"></a>Configuration requise



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

 

 




