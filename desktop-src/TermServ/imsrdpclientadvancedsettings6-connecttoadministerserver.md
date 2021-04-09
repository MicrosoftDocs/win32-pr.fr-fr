---
title: IMsRdpClientAdvancedSettings6 propriété ConnectToAdministerServer
description: Récupère ou spécifie si le contrôle ActiveX doit tenter de se connecter au serveur à des fins d’administration.
ms.assetid: b98f9b9b-a3e7-4a3c-a7e3-e388ce53c5c9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ConnectToAdministerServer
- Services Bureau à distance de la propriété ConnectToAdministerServer, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété ConnectToAdministerServer
- Services Bureau à distance de la propriété ConnectToAdministerServer, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété ConnectToAdministerServer
- Services Bureau à distance de la propriété ConnectToAdministerServer, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété ConnectToAdministerServer
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.put_ConnectToAdministerServer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9cad8d50e2e0a4c1ec18fbd33733dc394101a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032866"
---
# <a name="imsrdpclientadvancedsettings6connecttoadministerserver-property"></a>IMsRdpClientAdvancedSettings6 :: ConnectToAdministerServer, propriété

Récupère ou spécifie si le contrôle ActiveX doit tenter de se connecter au serveur à des fins d’administration.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_ConnectToAdministerServer(
  [in]  VARIANT_BOOL connectToAdministerServer
);

HRESULT get_ConnectToAdministerServer(
  [out] VARIANT_BOOL *pConnectToAdministerServer
);
```



## <a name="property-value"></a>Valeur de la propriété

**Variante \_ TRUE** pour obliger le contrôle ActiveX à tenter de se connecter au serveur à des fins d’administration. Sinon, **Variant \_ false**. La valeur par défaut **est \_ false**.

## <a name="remarks"></a>Notes

Pour utiliser **ConnectToAdministerServer**, vous devez exécuter le client Connexion Bureau À distance (RDC) version 6,1 ou ultérieure.

> [!Note]  
> RDC version 6,1 (6.0.6001) prend en charge protocole RDP (Remote Desktop Protocol) 6,1. RDC 6,1 est inclus avec Windows Server 2008 et Windows Vista avec Service Pack 1 (SP1).

 

**ConnectToAdministerServer** vous connecte à une session utilisée à des fins administratives sur le serveur distant. Si le service de rôle hôte de session Bureau à distance (hôte de session Bureau à distance) est installé sur le serveur distant, **ConnectToAdministerServer** effectue les opérations suivantes :

-   Désactive Services Bureau à distance licence d’accès client pour la session.
-   Désactive la redirection de fuseau horaire pour la session.
-   Désactive Connexion Bureau à distance redirection du Service Broker pour les connexions Bureau à distance pour la session.
-   Désactive Plug-and-Play redirection de périphérique pour la session.
-   Modifie le thème de session à distance en Windows Classic pour la session.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                   |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings6 est défini en tant que 222c4b5d-45d9-4DF0-a7c6-60cf9089d285<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





