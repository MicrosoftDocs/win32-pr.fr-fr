---
title: Interface IMsRdpClientNonScriptable5
description: fournit l’accès aux propriétés qui ne sont pas scriptables de la session à distance d’un client sur le contrôle Bureau à distance ActiveX. Dérive de l’interface IMsRdpClientNonScriptable4.
ms.assetid: 41b8c624-0451-4a7e-bc80-d0bf269e33c6
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, Description
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ec338dbe07c4733bf80207298f23f388bf8f77c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919944"
---
# <a name="imsrdpclientnonscriptable5-interface"></a>Interface IMsRdpClientNonScriptable5

fournit l’accès aux propriétés qui ne sont pas scriptables de la session à distance d’un client sur le contrôle Bureau à distance ActiveX. Dérive de l’interface [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md) . Les méthodes de cette interface sont accessibles uniquement par le biais de la vtable ; ils ne peuvent pas être utilisés pour des clients scriptables.

Une instance de cette interface est obtenue en appelant [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’objet [**IMsTscAx**](imstscax-interface.md) , en passant **IID \_ IMsRdpClientNonScriptable5**.

## <a name="members"></a>Membres

L’interface **IMsRdpClientNonScriptable5** hérite de [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md). **IMsRdpClientNonScriptable5** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IMsRdpClientNonScriptable5** possède les propriétés suivantes.



| Propriété                                                                                                         | Type d’accès           | Description                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**AllowPromptingForCredentials**](imsrdpclientnonscriptable5-allowpromptingforcredentials.md)<br/>       | Lecture/écriture<br/> | spécifie si le contrôle de ActiveX Bureau à distance peut inviter l’utilisateur à fournir des informations d’identification.<br/>                    |
| [**DisableConnectionBar**](imsrdpclientnonscriptable5-disableconnectionbar.md)<br/>                       | Écriture seule<br/> | spécifie si le contrôle de ActiveX Bureau à distance doit désactiver la barre de connexion.<br/>                      |
| [**DisableRemoteAppCapsCheck**](imsrdpclientnonscriptable5-disableremoteappcapscheck.md)<br/>             | Lecture/écriture<br/> | spécifie si le contrôle de ActiveX Bureau à distance ne doit pas vérifier les fonctionnalités RemoteApp du serveur.<br/> |
| [**GetRemoteMonitorsBoundingBox**](imsrdpclientnonscriptable5-getremotemonitorsboundingbox.md)<br/>       | Lecture seule<br/>  | Spécifie le rectangle englobant du moniteur distant.<br/>                                                      |
| [**RemoteMonitorCount**](imsrdpclientnonscriptable5-remotemonitorcount.md)<br/>                           | Lecture seule<br/>  | Spécifie le nombre de moniteurs à distance.<br/>                                                                     |
| [**RemoteMonitorLayoutMatchesLocal**](imsrdpclientnonscriptable5-remotemonitorlayoutmatcheslocal.md)<br/> | Lecture seule<br/>  | Spécifie si la disposition du moniteur distant est identique à la disposition du moniteur local.<br/>                             |
| [**UseMultimon**](imsrdpclientnonscriptable5-usemultimon.md)<br/>                                         | Lecture/écriture<br/> | spécifie si le contrôle de ActiveX Bureau à distance doit utiliser plusieurs analyses.<br/>                           |
| [**WarnAboutDirectXRedirection**](imsrdpclientnonscriptable5-warnaboutdirectxredirection.md)<br/>         | Lecture/écriture<br/> | Cette propriété n'est pas utilisée.<br/>                                                                                   |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID<br/>                    | Le CLSID \_ MsRdpClient10 est défini en tant que C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> Le CLSID \_ MsRdpClient10NotSafeForScripting est défini en tant que A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> Le CLSID \_ MsRdpClient7 est défini en tant que A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> Le CLSID \_ MsRdpClient7NotSafeForScripting est défini en tant que 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> Le CLSID \_ MsRdpClient8 est défini en tant que 5F681803-2900-4C43-A1CC-CF405404A676<br/> Le CLSID \_ MsRdpClient8NotSafeForScripting est défini en tant que A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> Le CLSID \_ MsRdpClient9 est défini en tant que 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> Le CLSID \_ MsRdpClient9NotSafeForScripting est défini en tant que 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 est défini en tant que 4f6996d5-d7b1-412c-b0ff-063718566907<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

