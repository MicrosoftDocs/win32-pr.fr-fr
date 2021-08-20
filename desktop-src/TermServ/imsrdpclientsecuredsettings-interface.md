---
title: Interface IMsRdpClientSecuredSettings
description: comprend des méthodes permettant de récupérer et de définir les propriétés du contrôle Bureau à distance ActiveX qui sont limitées à des zones de sécurité URL Internet Explorer spécifiques. | Interface IMsRdpClientSecuredSettings
ms.assetid: 56d3193d-a0fb-468a-9fb3-c080db5500b7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientSecuredSettings
- Services Bureau à distance de l’interface IMsRdpClientSecuredSettings, Description
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a1b834d42c957998ad2a8eda5cd3790dd16f40dfd82a8e463bc34e510cd742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129789"
---
# <a name="imsrdpclientsecuredsettings-interface"></a>Interface IMsRdpClientSecuredSettings

comprend des méthodes permettant de récupérer et de définir les propriétés du contrôle Bureau à distance ActiveX qui sont limitées à des zones de sécurité URL Internet Explorer spécifiques.

## <a name="members"></a>Membres

L’interface **IMsRdpClientSecuredSettings** hérite de [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md). **IMsRdpClientSecuredSettings** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IMsRdpClientSecuredSettings** possède les propriétés suivantes.



| Propriété                                                                                   | Type d’accès           | Description                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [**AudioRedirectionMode**](imsrdpclientsecuredsettings-autoredirectionmode.md)<br/> | Lecture/écriture<br/> | Paramètres de redirection audio.<br/>    |
| [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md)<br/>        | Lecture/écriture<br/> | Paramètres de redirection du clavier.<br/> |



 

## <a name="remarks"></a>Remarques

Ces propriétés ne peuvent pas être définies lorsque le contrôle est connecté.

Pour plus d’informations sur les méthodes de cette interface, consultez la rubrique [fourniture de la sécurité du client RDP](providing-for-rdp-client-security.md) .

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                 |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings est défini en tant que 605befcf-39c1-45cc-A811-068fb7be346d<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> <dt>

[Référence Connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





