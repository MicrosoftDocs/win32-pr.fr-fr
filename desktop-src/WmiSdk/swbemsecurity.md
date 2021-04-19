---
description: L’objet SWbemSecurity obtient ou définit des paramètres de sécurité, tels que des privilèges, des emprunts d’identité COM et des niveaux d’authentification affectés à un objet.
ms.assetid: 794587fa-5feb-455b-be28-ecfaa25625ad
ms.tgt_platform: multiple
title: Objet SWbemSecurity (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity
- ISWbemSecurity
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: da59c3b996a80384c133336503124141f0907f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516981"
---
# <a name="swbemsecurity-object"></a>Objet SWbemSecurity

L’objet **SWbemSecurity** obtient ou définit des paramètres de sécurité, tels que des privilèges, des emprunts d’identité com et des niveaux d’authentification affectés à un objet. Les objets [**SWbemLocator**](swbemlocator.md), [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), [**SWbemLastError**](swbemlasterror.md)et [**SWbemEventSource**](swbemeventsource.md) ont une propriété **de \_ sécurité** , qui est l’objet **SWbemSecurity** . Lorsque vous récupérez une instance ou affichez le journal de sécurité WMI, vous devrez peut-être définir les propriétés de l’objet de **sécurité \_** .

L’appel de VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) ne peut pas créer l’objet de sécurité. Les paramètres de sécurité de cet objet n’identifient pas les paramètres d’authentification, d’emprunt d’identité ou de privilège sur une connexion à WMI, ou la sécurité en vigueur pour le proxy lorsqu’un objet est remis à un récepteur dans un appel asynchrone. Pour plus d’informations, consultez [maintenance de la sécurité WMI](maintaining-wmi-security.md).

## <a name="members"></a>Membres

L’objet **SWbemSecurity** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **SWbemSecurity** a ces propriétés.



| Propriété                                                                    | Type d’accès           | Description                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthenticationLevel**](swbemsecurity-authenticationlevel.md)<br/> | Lecture/écriture<br/> | Valeur numérique qui définit le niveau d’authentification COM assigné à cet objet. Ce paramètre détermine la façon dont vous protégez les informations envoyées à partir de WMI.<br/>                                                                 |
| [**ImpersonationLevel**](swbemsecurity-impersonationlevel.md)<br/>   | Lecture/écriture<br/> | Valeur numérique qui définit le niveau d’emprunt d’identité COM assigné à cet objet. Ce paramètre détermine si les processus détenus par WMI peuvent détecter ou utiliser vos informations d’identification de sécurité lorsque vous effectuez des appels à d’autres processus.<br/> |
| [**Autorisations**](swbemsecurity-privileges.md)<br/>                   | Lecture seule<br/>  | Objet [**SWbemPrivilegeSet**](swbemprivilegeset.md) qui définit des privilèges pour cet objet. Pour plus d’informations, consultez [exécution avec des privilèges spéciaux](/windows/desktop/SecBP/running-with-special-privileges).<br/>                    |



 

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

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> <dt>

[Maintenance de la sécurité WMI](maintaining-wmi-security.md)
</dt> <dt>

[Définition de la sécurité des processus d' \_ application cliente \_](setting-client-application-process-security.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> </dl>

 

