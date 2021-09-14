---
title: Interface IMsRdpClient
description: Fournit les méthodes et les propriétés nécessaires à la configuration et à l’utilisation du contrôle client. Dérive de l’interface IMsTscAx.
ms.assetid: 6698c1d7-94d2-453c-96db-366113b95dd4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, Description
topic_type:
- apiref
api_name:
- IMsRdpClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc6d3a1de6a6cd18004ff957ea0f8c4d7c23b14d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856942"
---
# <a name="imsrdpclient-interface"></a>Interface IMsRdpClient

Fournit les méthodes et les propriétés nécessaires à la configuration et à l’utilisation du contrôle client. Dérive de l’interface [**IMsTscAx**](imstscax-interface.md) .

## <a name="members"></a>Membres

L’interface **IMsRdpClient** hérite de [**IMsTscAx**](imstscax-interface.md). **IMsRdpClient** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IMsRdpClient** possède ces méthodes.



| Méthode                                                                    | Description                                                         |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md) | Récupère les options définies pour un canal virtuel.<br/>         |
| [**RequestClose**](imsrdpclient-requestclose.md)                         | Demande un arrêt approprié du contrôle client.<br/>      |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md) | Définit les options de canal virtuel pour le contrôle client.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IMsRdpClient** possède les propriétés suivantes.



| Propriété                                                                             | Type d’accès           | Description                                                                                                                                                               |
|:-------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Lecture seule<br/>  | Pointeur vers l’interface [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) , utilisé pour définir des paramètres avancés pour le contrôle client.<br/> |
| [**La**](imsrdpclient-colordepth.md)<br/>                             | Lecture/écriture<br/> | Profondeur de couleur du contrôle actuel.<br/>                                                                                                                            |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | Lecture seule<br/>  | Informations étendues sur la raison de la déconnexion du contrôle client.<br/>                                                                                      |
| [**Large**](imsrdpclient-fullscreen.md)<br/>                             | Lecture/écriture<br/> | Indique si le contrôle est en mode plein écran.<br/>                                                                                                          |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Lecture seule<br/>  | Pointeur vers l’interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) , utilisé pour définir des paramètres sécurisés pour le contrôle client.<br/>    |



 

## <a name="remarks"></a>Notes

L’interface **IMsRdpClient** a été étendue par les interfaces suivantes, chaque nouvelle interface héritant de toutes les méthodes et propriétés des interfaces précédentes :

-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**IMsRdpClient3**](imsrdpclient3.md)
-   [**IMsRdpClient4**](imsrdpclient4.md)
-   [**IMsRdpClient5**](imsrdpclient5.md)
-   [**IMsRdpClient6**](imsrdpclient6.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | Le CLSID \_ MsRdpClient est défini en tant que 791fa017-2de3-492e-Acc5-53c67a2b94d0<br/> Le CLSID \_ MsRdpClient10 est défini en tant que C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> Le CLSID \_ MsRdpClient10NotSafeForScripting est défini en tant que A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> Le CLSID \_ MsRdpClient2 est défini en tant que 9059F30F-4eb1-4BD2-9FDC-36F43A218F4A<br/> Le CLSID \_ MsRdpClient2a est défini en tant que 971127BB-259F-48C2-BD75-5F97A3331551<br/> Le CLSID \_ MsRdpClient2NotSafeForScripting est défini en tant que 3523C2FB-4031-44E4-9A3B-F1E94986EE7F<br/> Le CLSID \_ MsRdpClient3 est défini en tant que 7584C670-2274-4efb-B00B-D6AABA6D3850<br/> Le CLSID \_ MsRdpClient3a est défini en tant que 6A6F4B83-45C5-4CA9-BDD9-0D81C12295E4<br/> Le CLSID \_ MsRdpClient3NotSafeForScripting est défini en tant que ACE575FD-1FCF-4074-9401-EBAB990FA9DE<br/> Le CLSID \_ MsRdpClient4 est défini en tant que 4EDCB26C-D24C-4E72-af07-B576699AC0DE<br/> Le CLSID \_ MsRdpClient4a est défini en tant que 54CE37E0-9834-41AE-9896-4DAB69DC022B<br/> Le CLSID \_ MsRdpClient4NotSafeForScripting est défini en tant que 6AE29350-321B-42BE-BBE5-12FB5270C0DE<br/> Le CLSID \_ MsRdpClient5 est défini en tant que 4EB89FF4-7f78-4A0F-8B8D-2BF02E94E4B2<br/> Le CLSID \_ MsRdpClient5NotSafeForScripting est défini en tant que 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> Le CLSID \_ MsRdpClient6 est défini en tant que 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> Le CLSID \_ MsRdpClient6NotSafeForScripting est défini en tant que D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> Le CLSID \_ MsRdpClient7 est défini en tant que A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> Le CLSID \_ MsRdpClient7NotSafeForScripting est défini en tant que 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> Le CLSID \_ MsRdpClient8 est défini en tant que 5F681803-2900-4C43-A1CC-CF405404A676<br/> Le CLSID \_ MsRdpClient8NotSafeForScripting est défini en tant que A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> Le CLSID \_ MsRdpClient9 est défini en tant que 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> Le CLSID \_ MsRdpClient9NotSafeForScripting est défini en tant que 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> Le CLSID \_ MsRdpClientNotSafeForScripting est défini en tant que 7CACBD7B-0D99-468F-AC33-22E495C0AFE5<br/> Le CLSID \_ MsTscAx est défini en tant que 1FB464C8-09BB-4017-A2F5-EB742F04392F<br/> Le CLSID \_ MsTscAxNotSafeForScripting est défini en tant que A41A4187-5A86-4E26-B40A-856F9035D9CB<br/> |
| IID<br/>                      | IID \_ IMsRdpClient est défini en tant que 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[Référence Connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





