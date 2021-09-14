---
title: Interface IMsTscSecuredSettings
description: comprend des méthodes permettant de récupérer et de définir les propriétés du contrôle Bureau à distance ActiveX qui sont limitées à des zones de sécurité URL Internet Explorer spécifiques. | Interface IMsTscSecuredSettings
ms.assetid: 1136dbc5-abe6-40e0-b44f-700a1460fbd2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsTscSecuredSettings
- Services Bureau à distance de l’interface IMsTscSecuredSettings, Description
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2037393147bd5a2e35d6eb803951890c9b5e7de5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118662"
---
# <a name="imstscsecuredsettings-interface"></a>Interface IMsTscSecuredSettings

comprend des méthodes permettant de récupérer et de définir les propriétés du contrôle Bureau à distance ActiveX qui sont limitées à des zones de sécurité URL Internet Explorer spécifiques. Les propriétés incluent celles qui spécifient le mode du contrôle client (mode plein écran ou mode fenêtre) et le programme à démarrer lors de la connexion au serveur hôte de session Bureau à distance (hôte de session Bureau à distance). Ces méthodes sont également disponibles via l’interface [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) .

## <a name="members"></a>Membres

L’interface **IMsTscSecuredSettings** hérite de l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IMsTscSecuredSettings** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IMsTscSecuredSettings** possède les propriétés suivantes.



| Propriété                                                              | Type d’accès           | Description                                                                |
|:----------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------|
| [**Large**](imstscsecuredsettings-fullscreen.md)<br/>     | Lecture/écriture<br/> | État plein écran du contrôle client.<br/>                    |
| [**StartProgram**](imstscsecuredsettings-startprogram.md)<br/> | Lecture/écriture<br/> | Programme à démarrer sur le serveur distant lors de la connexion.<br/> |
| [**WorkDir**](imstscsecuredsettings-workdir.md)<br/>           | Lecture/écriture<br/> | Répertoire de travail du programme de démarrage.<br/>                     |



 

## <a name="remarks"></a>Notes

Pour plus d’informations sur les méthodes de cette interface, consultez la rubrique [fourniture de la sécurité du client RDP](providing-for-rdp-client-security.md) .

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Référence Connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

