---
title: Interface IMsRdpClientNonScriptable4
description: Fournit l’accès aux propriétés non scriptables de la session à distance d’un client sur le contrôle ActiveX Bureau à distance. Dérive de l’interface IMsRdpClientNonScriptable3.
ms.assetid: 570a5722-94b9-4195-846a-10233d56002d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, Description
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aedea56733a2a98db4b966bd91d9337e38e61d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942886"
---
# <a name="imsrdpclientnonscriptable4-interface"></a>Interface IMsRdpClientNonScriptable4

Fournit l’accès aux propriétés non scriptables de la session à distance d’un client sur le contrôle ActiveX Bureau à distance. Dérive de l’interface [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md) . Les méthodes de cette interface sont accessibles uniquement par le biais de la vtable ; ils ne peuvent pas être utilisés pour des clients scriptables.

## <a name="members"></a>Membres

L’interface **IMsRdpClientNonScriptable4** hérite de [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md). **IMsRdpClientNonScriptable4** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IMsRdpClientNonScriptable4** possède les propriétés suivantes.



| Propriété                                                                                                         | Type d’accès           | Description                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowCredentialSaving**](imsrdpclientnonscriptable4-allowcredentialsaving.md)<br/>                     | Lecture/écriture<br/> | Spécifie si la boîte de dialogue informations d’identification affiche une case à cocher pour activer l’enregistrement des informations d’identification.<br/>                                                                                        |
| [**LaunchedViaClientShellInterface**](imsrdpclientnonscriptable4-launchedviaclientshellinterface.md)<br/> | Lecture/écriture<br/> | Spécifie si l’utilisateur a lancé le contrôle client à l’aide de l’interface de Accès web des services Bureau à distance.<br/>                                                                                                  |
| [**MarkRdpSettingsSecure**](imsrdpclientnonscriptable4-markrdpsettingssecure.md)<br/>                     | Lecture/écriture<br/> | Spécifie si les paramètres RDP sont marqués comme sécurisés.<br/>                                                                                                                                          |
| [**PromptForCredsOnClient**](imsrdpclientnonscriptable4-promptforcredsonclient.md)<br/>                   | Lecture/écriture<br/> | Spécifie si le contrôle client affiche une boîte de dialogue qui vous invite à entrer des informations d’identification.<br/>                                                                                                      |
| [**PublisherCertificateChain**](imsrdpclientnonscriptable4-publishercertificatechain.md)<br/>             | Lecture/écriture<br/> | Spécifie la chaîne du certificat de l’éditeur. La chaîne est stockée dans un variant de type VT \_ ByRef qui contient un pointeur vers une structure de [**contexte de \_ chaîne \_ du certificat**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .<br/> |
| [**RedirectionWarningType**](imsrdpclientnonscriptable4-redirectionwarningtype.md)<br/>                   | Lecture/écriture<br/> | Contrôle la présence et l’apparence de la boîte de dialogue de redirection.<br/>                                                                                                                           |
| [**TrustedZoneSite**](imsrdpclientnonscriptable4-trustedzonesite.md)<br/>                                 | Lecture/écriture<br/> | Spécifie si le site Web à partir duquel l’utilisateur a lancé la connexion se trouve dans la liste des sites de confiance de l’ordinateur client.<br/>                                                                |
| [**WarnAboutPrinterRedirection**](imsrdpclientnonscriptable4-warnaboutprinterredirection.md)<br/>         | Lecture/écriture<br/> | Spécifie si la boîte de dialogue de redirection affiche un message sur la redirection de l’imprimante avant de démarrer une session.<br/>                                                                          |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| CLSID<br/>                    | Le CLSID \_ MsRdpClient10 est défini en tant que C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> Le CLSID \_ MsRdpClient10NotSafeForScripting est défini en tant que A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> Le CLSID \_ MsRdpClient6 est défini en tant que 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> Le CLSID \_ MsRdpClient6NotSafeForScripting est défini en tant que D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> Le CLSID \_ MsRdpClient7 est défini en tant que A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> Le CLSID \_ MsRdpClient7NotSafeForScripting est défini en tant que 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> Le CLSID \_ MsRdpClient8 est défini en tant que 5F681803-2900-4C43-A1CC-CF405404A676<br/> Le CLSID \_ MsRdpClient8NotSafeForScripting est défini en tant que A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> Le CLSID \_ MsRdpClient9 est défini en tant que 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> Le CLSID \_ MsRdpClient9NotSafeForScripting est défini en tant que 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable4 est défini en tant que f50fa8aa-1c7d-4f59-B15C-a90cacae1fcb<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence Connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

