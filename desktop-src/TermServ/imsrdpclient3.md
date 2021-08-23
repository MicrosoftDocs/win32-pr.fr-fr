---
title: Interface IMsRdpClient3
description: Fournit les méthodes et les propriétés nécessaires à la configuration et à l’utilisation du contrôle client. Dérive de l’interface IMsRdpClient2.
ms.assetid: 31e52de1-1fb0-47ef-aad5-fd06621f2b3c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, Description
topic_type:
- apiref
api_name:
- IMsRdpClient3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 444f022c2f4db57c1c62f1405b30625bf7fed291674255ed6287026c9451e825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059007"
---
# <a name="imsrdpclient3-interface"></a>Interface IMsRdpClient3

Fournit les méthodes et les propriétés nécessaires à la configuration et à l’utilisation du contrôle client. Dérive de l’interface [**IMsRdpClient2**](imsrdpclient2.md) .

## <a name="members"></a>Membres

L’interface **IMsRdpClient3** hérite de [**IMsRdpClient2**](imsrdpclient2.md). **IMsRdpClient3** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IMsRdpClient3** possède les propriétés suivantes.



| Propriété                                                                | Type d’accès          | Description                                                                                                                                                       |
|:------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/> | Lecture seule<br/> | Pointeur vers l’interface [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) , utilisé pour définir des paramètres avancés pour le contrôle client.<br/> |



 

## <a name="remarks"></a>Remarques

L’interface **IMsRdpClient3** a été étendue par les interfaces suivantes, chaque nouvelle interface héritant de toutes les méthodes et propriétés des interfaces précédentes :

-   [**IMsRdpClient4**](imsrdpclient4.md)
-   [**IMsRdpClient5**](imsrdpclient5.md)
-   [**IMsRdpClient6**](imsrdpclient6.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| CLSID<br/>                    | Le CLSID \_ MsRdpClient10 est défini en tant que C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> Le CLSID \_ MsRdpClient10NotSafeForScripting est défini en tant que A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> Le CLSID \_ MsRdpClient3 est défini en tant que 7584C670-2274-4efb-B00B-D6AABA6D3850<br/> Le CLSID \_ MsRdpClient3a est défini en tant que 6A6F4B83-45C5-4CA9-BDD9-0D81C12295E4<br/> Le CLSID \_ MsRdpClient3NotSafeForScripting est défini en tant que ACE575FD-1FCF-4074-9401-EBAB990FA9DE<br/> Le CLSID \_ MsRdpClient4 est défini en tant que 4EDCB26C-D24C-4E72-af07-B576699AC0DE<br/> Le CLSID \_ MsRdpClient4a est défini en tant que 54CE37E0-9834-41AE-9896-4DAB69DC022B<br/> Le CLSID \_ MsRdpClient4NotSafeForScripting est défini en tant que 6AE29350-321B-42BE-BBE5-12FB5270C0DE<br/> Le CLSID \_ MsRdpClient5 est défini en tant que 4EB89FF4-7f78-4A0F-8B8D-2BF02E94E4B2<br/> Le CLSID \_ MsRdpClient5NotSafeForScripting est défini en tant que 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> Le CLSID \_ MsRdpClient6 est défini en tant que 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> Le CLSID \_ MsRdpClient6NotSafeForScripting est défini en tant que D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> Le CLSID \_ MsRdpClient7 est défini en tant que A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> Le CLSID \_ MsRdpClient7NotSafeForScripting est défini en tant que 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> Le CLSID \_ MsRdpClient8 est défini en tant que 5F681803-2900-4C43-A1CC-CF405404A676<br/> Le CLSID \_ MsRdpClient8NotSafeForScripting est défini en tant que A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> Le CLSID \_ MsRdpClient9 est défini en tant que 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> Le CLSID \_ MsRdpClient9NotSafeForScripting est défini en tant que 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClient3 est défini en tant que 91b7cbc5-a72e-4FA0-9300-d647d7e897ff<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[Référence Connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





