---
title: Objet WSMan (WSManDisp. h)
description: Fournit des méthodes et des propriétés utilisées pour créer une session, représentée par un objet de session.
ms.assetid: 45895a4e-b7de-4469-ae78-6d1d3f9d6145
ms.tgt_platform: multiple
keywords:
- objet WSMan Windows Remote Management
- objet WSMan Windows Remote Management, description
topic_type:
- apiref
api_name:
- WSMan
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dac26be22118a320848ea227643f9c4d3857dc01
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475965"
---
# <a name="wsman-object"></a>Objet WSMan

Fournit des méthodes et des propriétés utilisées pour créer une session, représentée par un objet de [**session**](session.md) . toute opération de Windows Remote Management nécessite la création d’une [**Session**](session.md) qui se connecte à un ordinateur distant, à un [*contrôleur de gestion de base*](windows-remote-management-glossary.md) (BMC) ou à l’ordinateur local. Les opérations incluent l’obtention, l’écriture, l’énumération de données ou l’appel de méthodes.

## <a name="members"></a>Membres

L’objet **WSMan** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **WSMan** possède ces méthodes.




| Méthode | Description | 
|--------|-------------|
| <a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a> | Crée un objet <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> qui spécifie le nom d’utilisateur et le mot de passe utilisés lors de la création d’une session à distance.<br /> | 
| <a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a> | Crée un objet <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> qui peut spécifier les éléments suivants :<br /><ul><li>Le chemin d’accès complet à une <a href="windows-remote-management-glossary.md"><em>ressource</em></a> ou à un élément de données unique.</li><li><a href="windows-remote-management-glossary.md"><em>Sélecteur</em></a> pour une instance spécifique d’une ressource.</li><li><a href="windows-remote-management-glossary.md"><em>Option</em></a> qui fournit des données supplémentaires au fournisseur de ressources.</li></ul> | 
| <a href="wsman-createsession.md"><strong>CreateSession</strong></a> | Crée un objet de <a href="session.md"><strong>session</strong></a> qui peut ensuite être utilisé pour les opérations réseau ultérieures.<br /> | 
| <a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan. EnumerationFlagHierarchyDeep</strong></a> | Retourne la valeur de l’indicateur d’énumération <strong>EnumerationFlagHierarchyDeep</strong> à utiliser dans le paramètre <em>Flags</em> de <a href="session-enumerate.md"><strong>session. Enumerate</strong></a>.<br /> | 
| <a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan. EnumerationFlagHierarchyDeepBasePropsOnly</strong></a> | Retourne la valeur de l’indicateur d’énumération <strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong> à utiliser dans le paramètre <em>Flags</em> de <a href="session-enumerate.md"><strong>session. Enumerate</strong></a>.<br /> | 
| <a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan. EnumerationFlagHierarchyShallow</strong></a> | Retourne la valeur de l’indicateur d’énumération <strong>EnumerationFlagHierarchyShallow</strong> à utiliser dans le paramètre <em>Flags</em> de <a href="session-enumerate.md"><strong>session. Enumerate</strong></a>.<br /> | 
| <a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan. EnumerationFlagNonXmlText</strong></a> | Retourne la valeur de la constante d’énumération <strong>WSManFlagNonXmlText</strong> à utiliser dans le paramètre <em>Flags</em> de la méthode <a href="session-enumerate.md"><strong>session. Enumerate</strong></a> .<br /> | 
| <a href="wsman-enumerationflagreturnepr.md"><strong>WSMan. EnumerationFlagReturnEPR</strong></a> | Retourne la valeur de l’indicateur d’énumération <strong>EnumerationFlagReturnEPR</strong> à utiliser dans le paramètre <em>Flags</em> de <a href="session-enumerate.md"><strong>session. Enumerate</strong></a>.<br /> | 
| <a href="wsman-enumerationflagreturnobject.md"><strong>WSMan. EnumerationFlagReturnObject</strong></a> | Retourne la valeur de l’indicateur d’énumération <strong>EnumerationFlagReturnObject</strong> à utiliser dans le paramètre <em>Flags</em> de <a href="session-enumerate.md"><strong>session. Enumerate</strong></a>.<br /> | 
| <a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan. EnumerationFlagReturnObjectAndEPR</strong></a> | Retourne la valeur de l’indicateur d’énumération <strong>EnumerationFlagReturnObjectAndEPR</strong> à utiliser dans le paramètre <em>Flags</em> de <a href="session-enumerate.md"><strong>session. Enumerate</strong></a>.<br /> | 
| <a href="wsman-geterrormessage.md"><strong>WSMan. GetErrorMessage</strong></a> | Retourne une chaîne mise en forme contenant le texte d’un numéro d’erreur.<br /> | 
| <a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan. SessionFlagCredUsernamePassword</strong></a> | Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagCredUsernamePassword</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan. SessionFlagEnableSPNServerPort</strong></a> | Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagEnableSPNServerPort</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagnoencryption.md"><strong>WSMan. SessionFlagNoEncryption</strong></a> | Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagNoEncryption</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagskipcacheck.md"><strong>WSMan. SessionFlagSkipCACheck</strong></a> | Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagSkipCACheck</strong> à utiliser dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagskipcncheck.md"><strong>WSMan. SessionFlagSkipCNCheck</strong></a> | Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagSkipCNCheck</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagusebasic.md"><strong>WSMan. SessionFlagUseBasic</strong></a> | Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagUseBasic</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagusedigest.md"><strong>WSMan. SessionFlagUseDigest</strong></a> | Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagUseDigest</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagusekerberos.md"><strong>WSMan. SessionFlagUseKerberos</strong></a> | Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagUseKerberos</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagusenegotiate.md"><strong>WSMan. SessionFlagUseNegotiate</strong></a> | Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagUseNegotiate</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan. SessionFlagUseNoAuthentication</strong></a> | Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagUseNoAuthentication</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagutf8.md"><strong>WSMan. SessionFlagUTF8</strong></a> | Retourne la valeur de l’indicateur d’authentification <strong>WSManFlagUTF8</strong> pour une utilisation dans le paramètre <em>Flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br /> | 




 

### <a name="properties"></a>Propriétés

L’objet **WSMan** possède ces propriétés.



| Propriété                                            | Type d’accès          | Description                                                                   |
|:----------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [**CommandLine**](wsman-commandline.md)<br/> | Lecture seule<br/> | Obtient la ligne de commande non traités pour le processus d’hébergement actuel.<br/> |
| [**Erreurs**](wsman-error.md)<br/>             | Lecture seule<br/> | Obtient les informations d’erreur.<br/>                                            |



 

## <a name="remarks"></a>Remarques

L’objet **WSMan** correspond aux interfaces [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) et [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) . **WSMan** est le seul objet qui peut être créé directement à l’aide de [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).

## <a name="examples"></a>Exemples

L’exemple de code suivant montre comment instancier un objet **WSMan** .


```VB
Dim objWsman
Dim Session, Resource 
Set objWsman = CreateObject( "WSMAN.Automation" )
Set Session = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/Root/CIMv2/Win32_OperatingSystem"
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[API de script WinRM](winrm-scripting-api.md)
</dt> <dt>

[à propos de Windows Remote Management](about-windows-remote-management.md)
</dt> <dt>

[utilisation de Windows Remote Management](using-windows-remote-management.md)
</dt> <dt>

[scripts dans Windows Remote Management](scripting-in-windows-remote-management.md)
</dt> <dt>

[Obtention de données à partir de l’ordinateur local](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Obtention de données à partir d’un ordinateur distant](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

