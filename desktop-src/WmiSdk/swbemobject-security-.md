---
description: La \_ propriété Security de l’objet SWbemObject est utilisée pour lire ou définir les paramètres de sécurité d’un objet SWbemObject.
ms.assetid: add77267-d62f-4ee4-a0ff-8ca06a6bf7cd
ms.tgt_platform: multiple
title: SWbemObject.Security_, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Security_
- ISWbemObject.Security_
- ISWbemObject.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f4d4b9aec7b6d800fa27609abd5d0cb1f3a435a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320665"
---
# <a name="swbemobjectsecurity_-property"></a>SWbemObject. Security, \_ propriété

La **propriété \_ Security** de l’objet [**SWbemObject**](swbemobject.md) est utilisée pour lire ou définir les paramètres de sécurité d’un objet **SWbemObject** . Cette propriété est un objet [**SWbemSecurity**](swbemsecurity.md) . Les paramètres de sécurité de cet objet n’indiquent pas les paramètres d’authentification, d’emprunt d’identité ou de privilège effectués sur une connexion à Windows Management Instrumentation (WMI), ou la sécurité en vigueur pour le proxy lorsqu’un objet est remis à un récepteur dans un appel asynchrone. Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md).

> [!Note]  
> Le paramétrage de la propriété de **\_ sécurité** d’un objet [**SWbemObject**](swbemobject.md) sur **null** accorde un accès illimité à tout le monde en permanence. Pour plus d’informations, consultez [**SWbemSecurity**](swbemsecurity.md).

 

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
SWbemObject.Security_ As Object
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**M**](swbemobject.md)
</dt> <dt>

[Création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Définition de la sécurité des processus d' \_ application cliente \_](setting-client-application-process-security.md)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[**Constantes de privilège**](privilege-constants.md)
</dt> </dl>

 

 




