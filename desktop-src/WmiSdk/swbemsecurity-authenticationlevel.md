---
description: La propriété AuthenticationLevel est un entier qui définit le niveau d’authentification COM affecté à cet objet.
ms.assetid: 96c2e6a5-a91f-469d-bdd1-eaa20b176158
ms.tgt_platform: multiple
title: SWbemSecurity. AuthenticationLevel, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.AuthenticationLevel
- ISWbemSecurity.AuthenticationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 63ae9e529de010e0a0ca7b8bc1da7dc8dc4891b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403475"
---
# <a name="swbemsecurityauthenticationlevel-property"></a>SWbemSecurity. AuthenticationLevel, propriété

La propriété **AuthenticationLevel** est un entier qui définit le niveau d’authentification com affecté à cet objet. Ce paramètre détermine la façon dont vous protégez les informations envoyées à partir de WMI. Pour plus d’informations sur les niveaux d’authentification, consultez Définition de la [ \_ sécurité des \_ processus de l’application cliente](setting-client-application-process-security.md). En général, il n’est pas nécessaire de définir le niveau d’authentification lors de l’exécution d’appels d’API WMI. Si vous ne définissez pas cette propriété, le niveau d’authentification COM par défaut de votre système est utilisé.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
SWbemSecurity.AuthenticationLevel As Integer
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Notes

Le paramètre authenticationLevel vous permet de demander le niveau d’authentification et de confidentialité DCOM à utiliser au cours d’une connexion. Paramètres allant de l’authentification sans authentification à l’authentification chiffrée par paquet.



| Valeur        | Description                                                                                                                                                                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| None         | N’utilise pas d’authentification. Tous les paramètres de sécurité sont ignorés.<br/>                                                                                                                                                                                                                                         |
| Valeur par défaut      | Utilise une négociation de sécurité standard pour sélectionner un niveau d’authentification. Il s’agit du paramètre recommandé, car le client impliqué dans la transaction sera négocié au niveau d’authentification spécifié par le serveur.<br/> DCOM ne sélectionne pas la valeur aucun au cours d’une session de négociation.<br/> |
| Se connecter      | Authentifie les informations d’identification du client uniquement lorsque le client tente de se connecter au serveur. Une fois la connexion établie, aucune vérification d’authentification supplémentaire n’a lieu.<br/>                                                                                                                          |
| Appeler         | Authentifie les informations d’identification du client uniquement au début de chaque appel, lorsque le serveur reçoit la demande. Les en-têtes de paquets sont signés, mais les paquets de données échangés entre le client et le serveur ne sont ni signés ni chiffrés.<br/>                                                     |
| PKT          | Authentifie que tous les paquets de données sont reçus du client attendu. Semblable à Call ; les en-têtes de paquets sont signés, mais pas chiffrés. Les paquets eux-mêmes ne sont ni signés ni chiffrés.<br/>                                                                                                               |
| PktIntegrity | Authentifie et vérifie qu’aucun des paquets de données transférés entre le client et le serveur n’a été modifié. Chaque paquet de données est signé, ce qui garantit que les paquets n’ont pas été modifiés pendant le transit. Aucun des paquets de données n’est chiffré.<br/>                                            |
| PktPrivacy   | Authentifie tous les niveaux et signes d’emprunt d’identité précédents et chiffre chaque paquet de données. Cela garantit que toutes les communications entre le client et le serveur sont confidentielles.<br/>                                                                                                                             |



 

Vous pouvez définir le niveau d’authentification des objets [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md)et [**SwbemLocator**](swbemlocator.md) en affectant à la propriété **AuthenticationLevel** la valeur souhaitée.

L’exemple suivant montre comment définir le niveau d’authentification pour un objet **SwbemObject** .


```VB
objinstance.Security_.AuthenticationLevel = wbemAuthenticationLevelPkt
```



Vous pouvez également spécifier des niveaux d’authentification dans le cadre d’un moniker. L’exemple suivant définit le niveau d’authentification et le niveau d’emprunt d’identité, et récupère une instance [**de \_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!root/cimv2:Win32_LogicalDisk='c:'")
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

[Définition de la sécurité des processus d' \_ application cliente \_](setting-client-application-process-security.md)
</dt> <dt>

[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[**SWbemSecurity**](swbemsecurity.md)
</dt> </dl>

 

