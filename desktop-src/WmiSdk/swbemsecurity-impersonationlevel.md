---
description: La propriété ImpersonationLevel est un entier qui définit le niveau d’emprunt d’identité COM affecté à cet objet.
ms.assetid: cf57620b-7827-4552-a969-d25e5eb13a89
ms.tgt_platform: multiple
title: SWbemSecurity. ImpersonationLevel, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.ImpersonationLevel
- ISWbemSecurity.ImpersonationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cde6bca09198d6e05f1ae0143ee07d1aedd465df68258303f1d6ca2b4b7699f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639579"
---
# <a name="swbemsecurityimpersonationlevel-property"></a>SWbemSecurity. ImpersonationLevel, propriété

La propriété **ImpersonationLevel** est un entier qui définit le niveau d’emprunt d’identité com affecté à cet objet. ce paramètre détermine si les processus appartenant à Windows Management Instrumentation (WMI) peuvent détecter ou utiliser vos informations d’identification de sécurité lorsque vous effectuez des appels à d’autres processus. Pour plus d’informations sur les niveaux d’emprunt d’identité, consultez Définition de la [ \_ sécurité des \_ processus de l’application cliente](setting-client-application-process-security.md).

Si vous ne définissez pas spécifiquement le niveau d’emprunt d’identité dans un moniker, ou en définissant la propriété **SWBemSecurity. ImpersonationLevel** sur un objet sécurisable, WMI définit le niveau d’emprunt d’identité par défaut sur la valeur spécifiée dans la [clé de Registre niveau d’emprunt d’identité par défaut](setting-the-default-process-security-level-using-vbscript.md). Si ce paramètre n’est pas suffisant, le fournisseur ne prend pas en service votre demande et l’appel à l’API WMI peut échouer avec un code d’erreur **wbemErrAccessDenied** (2147749891/0x80041003).

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
SWbemSecurity.ImpersonationLevel As Integer
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Remarques

En tant que niveau d’emprunt d’identité DCOM, cette propriété peut être définie sur l’une des valeurs suivantes :



| Valeur           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Anonyme**   | Masque les informations d'identification de l'appelant. WMI ne prend pas en charge ce niveau d’emprunt d’identité. Si un script spécifie impersonationLevel = Anonymous, WMI met à niveau silencieusement le niveau d’emprunt d’identité pour identifier. Il s’agit d’un exercice non significatif, toutefois, car les scripts utilisant le niveau d’identification risquent d’échouer.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Repérer**    | Permet aux objets d’interroger les informations d’identification de l’appelant. Les scripts utilisant ce niveau d’emprunt d’identité risquent d’échouer ; le niveau d’identification ne vous permet généralement pas de vérifier les listes de contrôle d’accès. Vous ne pouvez pas exécuter de scripts sur des ordinateurs distants à l’aide de l’identification.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| **Impersonate** | Permet aux objets d’utiliser les informations d’identification de l’appelant. Il est recommandé d’utiliser ce niveau d’emprunt d’identité avec les scripts WMI. Dans ce cas, le script WMI utilise les informations d’identification de l’utilisateur. par conséquent, il sera en mesure d’effectuer toutes les tâches que vous êtes en mesure d’effectuer.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **Délégué**    | Permet aux objets d’autoriser d’autres objets à utiliser les informations d’identification de l’appelant. La délégation permet à un script d’utiliser vos informations d’identification sur un ordinateur distant, puis permet à cet ordinateur distant d’utiliser vos informations d’identification sur un autre ordinateur distant. Bien que vous puissiez utiliser ce niveau d’emprunt d’identité dans les scripts WMI, vous devez le faire uniquement si nécessaire, car cela peut poser un risque pour la sécurité.<br/> Vous ne pouvez pas utiliser le niveau d’emprunt d’identité de délégué, sauf si tous les comptes d’utilisateur et les comptes d’ordinateur impliqués dans la transaction ont tous été marqués comme approuvés pour la délégation dans Active Directory. Cela permet de réduire les risques de sécurité. Bien qu’un ordinateur distant puisse utiliser vos informations d’identification, il ne peut le faire que si celui-ci et les autres ordinateurs impliqués dans la transaction sont approuvés pour la délégation.<br/> |



 

Comme indiqué précédemment, l’emprunt d’identité anonyme masque vos informations d’identification et identifie l’autorisation d’un objet distant à interroger vos informations d’identification, mais l’objet distant ne peut pas emprunter l’identité de votre contexte de sécurité. (En d’autres termes, bien que l’objet distant sache qui vous êtes, il ne peut pas être « prétend ».) Les scripts WMI qui accèdent à des ordinateurs distants en utilisant l’un de ces deux paramètres échouent généralement. En fait, la plupart des scripts exécutés sur l’ordinateur local à l’aide de l’un de ces deux paramètres échouent également.

Impersonate permet au service WMI distant d’utiliser votre contexte de sécurité pour effectuer l’opération demandée. Une demande WMI distante qui utilise le paramètre Impersonate fonctionne généralement, à condition que vos informations d’identification aient des privilèges suffisants pour effectuer l’opération prévue. En d’autres termes, vous ne pouvez pas utiliser WMI pour effectuer une action (à distance ou autre) que vous n’avez pas l’autorisation d’effectuer en dehors de WMI.

La définition de impersonationLevel à déléguer permet au service WMI distant de transmettre vos informations d’identification à d’autres objets et est généralement considéré comme un risque pour la sécurité.

Vous pouvez définir le niveau d’emprunt d’identité d’un objet [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)et [**SwbemLocator**](swbemlocator.md) en affectant à la propriété **ImpersonationLevel** la valeur souhaitée. L’exemple suivant montre comment définir le niveau d’emprunt d’identité pour un objet **SWbemObject** :


```VB
objinstance.Security_.ImpersonationLevel = _
    wbemImpersonationLevelImpersonate
```



Vous pouvez également spécifier des niveaux d’emprunt d’identité dans le cadre d’un moniker. L’exemple suivant définit le niveau d’authentification et le niveau d’emprunt d’identité, et récupère une instance [**du \_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service).


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,"& _
                         "authenticationLevel=pktPrivacy}"& _
                         "!root/cimv2:Win32_service='ALERTER'")
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemSecurity<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemSecurity<br/>                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Définition de la sécurité des processus d' \_ application cliente \_](setting-client-application-process-security.md)
</dt> <dt>

[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> </dl>

 

