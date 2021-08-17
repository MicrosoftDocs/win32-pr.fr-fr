---
title: Interface IMsRdpClientAdvancedSettings3
description: Gère les paramètres client avancés. Dérive de l’interface IMsRdpClientAdvancedSettings2.
ms.assetid: bfa9cf74-5943-45ca-9259-3ef0cc9ab2ab
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, Description
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df13ccfb0d955714984af82daaf693522ee7d61af9c608107c53dc9f5464b591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001377"
---
# <a name="imsrdpclientadvancedsettings3-interface"></a>Interface IMsRdpClientAdvancedSettings3

Gère les paramètres client avancés. Dérive de l’interface [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) . cette interface comprend des méthodes pour récupérer et définir des propriétés avancées (facultatives) pour le contrôle ActiveX Bureau à distance.

Pour obtenir une instance de cette interface, utilisez la propriété [**IMsTscAx :: AdvancedSettings**](imstscax-advancedsettings.md) pour obtenir un pointeur d’interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) . Appelez ensuite [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le pointeur **IMsTscAdvancedSettings** et transmettez **IID \_ IMsRdpClientAdvancedSettings3** à **QueryInterface**.

## <a name="members"></a>Membres

L’interface **IMsRdpClientAdvancedSettings3** hérite de [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md). **IMsRdpClientAdvancedSettings3** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IMsRdpClientAdvancedSettings3** possède les propriétés suivantes.



| Propriété                                                                                                            | Type d’accès           | Description                                                                            |
|:--------------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------|
| [**ConnectionBarShowMinimizeButton**](imsrdpclientadvancedsettings3-connectionbarshowminimizebutton.md)<br/> | Lecture/écriture<br/> | Spécifie s’il faut afficher le bouton **réduire** sur la barre de connexion.<br/> |
| [**ConnectionBarShowRestoreButton**](imsrdpclientadvancedsettings3-connectionbarshowrestorebutton.md)<br/>   | Lecture/écriture<br/> | Spécifie s’il faut afficher le bouton **restaurer** sur la barre de connexion.<br/>  |



 

## <a name="remarks"></a>Remarques

Cette interface a été étendue par les interfaces suivantes, chaque nouvelle interface héritant de toutes les méthodes et propriétés des interfaces précédentes :

-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
-   [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                   |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings3 est défini en tant que 19cd856b-c542-4c53-acee-f127e3be1a59<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Référence Connexion Bureau à distance par le Web](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

