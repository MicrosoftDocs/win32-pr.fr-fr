---
title: Interface IMsTscNonScriptable
description: contient des propriétés et des méthodes qui sont liées à l’application d’un mot de passe au contrôle Bureau à distance ActiveX.
ms.assetid: b4a68e02-cce6-4fbe-98b4-0627c10f3f37
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsTscNonScriptable
- Services Bureau à distance de l’interface IMsTscNonScriptable, Description
topic_type:
- apiref
api_name:
- IMsTscNonScriptable
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92372f7ea9479f7fcdd632546a0bd7dd2f0b465e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217449"
---
# <a name="imstscnonscriptable-interface"></a>Interface IMsTscNonScriptable

contient des propriétés et des méthodes qui sont liées à l’application d’un mot de passe au contrôle Bureau à distance ActiveX.

la principale utilisation de l’interface **IMsTscNonScriptable** consiste à configurer l’accès à la connexion automatique par mot de passe aux serveurs Bureau à distance hôte de session (hôte de session bureau à distance) dans les scénarios où l’Bureau à distance ActiveX contrôle est hébergé dans un conteneur écrit personnalisé. lorsque l’ouverture de session automatique est configurée, l’utilisateur ne reçoit pas la boîte de dialogue d’ouverture de session Windows au moment de la connexion.

Sur certaines plateformes, les méthodes de l’interface **IMsTscNonScriptable** peuvent être utilisées pour spécifier des mots de passe dans l’un des trois formats pris en charge :

-   Plaintext
-   Encodé portable
-   Encodé binaire (à ne pas porter)

Notez qu’un mot de passe dans un format encodé se compose de deux parties :

-   Partie du mot de passe encodé.
-   Partie de valeur salt.

Les deux parties sont requises pour définir un mot de passe encodé. Ni la partie de mot de passe encodée ni la valeur Salt ne doivent être considérées comme étant chiffrées de manière sécurisée.

L’accès scriptable aux mots de passe en texte en clair est disponible via la propriété [**ClearTextPassword**](imsrdpclientadvancedsettings-cleartextpassword.md) de l’interface scriptable [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md).

L’interface **IMsTscNonScriptable** est accessible uniquement via la vtable.

## <a name="members"></a>Membres

L’interface **IMsTscNonScriptable** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsTscNonScriptable** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IMsTscNonScriptable** possède ces méthodes.



| Méthode                                                     | Description                                           |
|:-----------------------------------------------------------|:------------------------------------------------------|
| [**ResetPassword**](imstscnonscriptable-resetpassword.md) | Réinitialise tous les États de mot de passe dans le contrôle.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **IMsTscNonScriptable** possède les propriétés suivantes.



| Propriété                                                                      | Type d’accès           | Description                                                                  |
|:------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------|
| [**BinaryPassword**](imstscnonscriptable-binarypassword.md)<br/>       | Lecture/écriture<br/> | Cette propriété n'est pas prise en charge.<br/>                                   |
| [**BinarySalt**](imstscnonscriptable-binarysalt.md)<br/>               | Lecture/écriture<br/> | Cette propriété n'est pas prise en charge.<br/>                                   |
| [**ClearTextPassword**](imstscnonscriptable-cleartextpassword.md)<br/> | Écriture seule<br/> | Bureau à distance ActiveX mot de passe de contrôle, au format texte en clair.<br/> |
| [**PortablePassword**](imstscnonscriptable-portablepassword.md)<br/>   | Lecture/écriture<br/> | Cette propriété n'est pas prise en charge.<br/>                                   |
| [**PortableSalt**](imstscnonscriptable-portablesalt.md)<br/>           | Lecture/écriture<br/> | Cette propriété n'est pas prise en charge.<br/>                                   |



 

## <a name="remarks"></a>Notes

l’ajout d’un mot de passe au contrôle Bureau à distance ActiveX est facultatif. si vous fournissez un mot de passe au contrôle, vous devez appliquer un seul des trois formats précédents au contrôle avant d’initialiser la connexion avec un appel à la méthode [**Connecter**](imstscax-connect.md) .

> [!Note]  
> Vous pouvez également activer l’ouverture de session automatique sur le serveur avec l’outil de configuration Services Bureau à distance (TSCC. msc). un administrateur peut utiliser cet outil pour attribuer un mot de passe spécifique à une connexion dans une situation où une ouverture de session automatisée est nécessaire.

 

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

L’interface **IMsTscNonScriptable** a été étendue par les interfaces suivantes, chaque nouvelle interface héritant de toutes les méthodes et propriétés des interfaces précédentes :

-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
-   [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
-   [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
-   [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | Le CLSID \_ MsRdpClient est défini en tant que 791fa017-2de3-492e-Acc5-53c67a2b94d0<br/> Le CLSID \_ MsRdpClient10 est défini en tant que C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> Le CLSID \_ MsRdpClient10NotSafeForScripting est défini en tant que A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> Le CLSID \_ MsRdpClient2 est défini en tant que 9059F30F-4eb1-4BD2-9FDC-36F43A218F4A<br/> Le CLSID \_ MsRdpClient2a est défini en tant que 971127BB-259F-48C2-BD75-5F97A3331551<br/> Le CLSID \_ MsRdpClient2NotSafeForScripting est défini en tant que 3523C2FB-4031-44E4-9A3B-F1E94986EE7F<br/> Le CLSID \_ MsRdpClient3 est défini en tant que 7584C670-2274-4efb-B00B-D6AABA6D3850<br/> Le CLSID \_ MsRdpClient3a est défini en tant que 6A6F4B83-45C5-4CA9-BDD9-0D81C12295E4<br/> Le CLSID \_ MsRdpClient3NotSafeForScripting est défini en tant que ACE575FD-1FCF-4074-9401-EBAB990FA9DE<br/> Le CLSID \_ MsRdpClient4 est défini en tant que 4EDCB26C-D24C-4E72-af07-B576699AC0DE<br/> Le CLSID \_ MsRdpClient4a est défini en tant que 54CE37E0-9834-41AE-9896-4DAB69DC022B<br/> Le CLSID \_ MsRdpClient4NotSafeForScripting est défini en tant que 6AE29350-321B-42BE-BBE5-12FB5270C0DE<br/> Le CLSID \_ MsRdpClient5 est défini en tant que 4EB89FF4-7f78-4A0F-8B8D-2BF02E94E4B2<br/> Le CLSID \_ MsRdpClient5NotSafeForScripting est défini en tant que 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> Le CLSID \_ MsRdpClient6 est défini en tant que 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> Le CLSID \_ MsRdpClient6NotSafeForScripting est défini en tant que D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> Le CLSID \_ MsRdpClient7 est défini en tant que A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> Le CLSID \_ MsRdpClient7NotSafeForScripting est défini en tant que 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> Le CLSID \_ MsRdpClient8 est défini en tant que 5F681803-2900-4C43-A1CC-CF405404A676<br/> Le CLSID \_ MsRdpClient8NotSafeForScripting est défini en tant que A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> Le CLSID \_ MsRdpClient9 est défini en tant que 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> Le CLSID \_ MsRdpClient9NotSafeForScripting est défini en tant que 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> Le CLSID \_ MsRdpClientNotSafeForScripting est défini en tant que 7CACBD7B-0D99-468F-AC33-22E495C0AFE5<br/> Le CLSID \_ MsTscAx est défini en tant que 1FB464C8-09BB-4017-A2F5-EB742F04392F<br/> Le CLSID \_ MsTscAxNotSafeForScripting est défini en tant que A41A4187-5A86-4E26-B40A-856F9035D9CB<br/> |
| IID<br/>                      | IID \_ IMsTscNonScriptable est défini en tant que C1E6743A-41C1-4A74-832A-0DD06C1C7A0E<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence Connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsTscAx :: Connecter**](imstscax-connect.md)
</dt> </dl>

 

