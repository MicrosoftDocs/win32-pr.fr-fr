---
title: Interface IMsRdpClientAdvancedSettings7
description: expose des méthodes et des propriétés qui gèrent les paramètres avancés du contrôle ActiveX.
ms.assetid: 2d6848b4-2ce6-4624-b46e-65e7daf2d0f1
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, Description
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5df2990a257d8f7fa544c24e33dba6a2422d2db8bea878f2487ca131e5bd607
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866559"
---
# <a name="imsrdpclientadvancedsettings7-interface"></a>Interface IMsRdpClientAdvancedSettings7

expose des méthodes et des propriétés qui gèrent les paramètres avancés du contrôle ActiveX.

Pour obtenir une instance de cette interface, utilisez la propriété [**IMsTscAx :: AdvancedSettings**](imstscax-advancedsettings.md) pour obtenir un pointeur d’interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) . Appelez ensuite [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le pointeur **IMsTscAdvancedSettings** et transmettez **IID \_ IMsRdpClientAdvancedSettings7** à **QueryInterface**.

## <a name="members"></a>Membres

L’interface **IMsRdpClientAdvancedSettings7** hérite de **IMsRdpClientAdvancedSettings6**. **IMsRdpClientAdvancedSettings7** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **IMsRdpClientAdvancedSettings7** possède les propriétés suivantes.



| Propriété                                                                                                    | Type d’accès           | Description                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AudioCaptureRedirectionMode**](imsrdpclientadvancedsettings7-audiocaptureredirectionmode.md)<br/> | Lecture/écriture<br/> | Spécifie ou récupère une valeur qui indique si le périphérique d’entrée audio par défaut est redirigé du client vers la session à distance.<br/> |
| [**AudioQualityMode**](imsrdpclientadvancedsettings7-audioqualitymode.md)<br/>                       | Lecture/écriture<br/> | Spécifie ou récupère une valeur qui indique le paramètre de mode de qualité audio pour le son Redirigé.<br/>                                        |
| [**EnableSuperPan**](imsrdpclientadvancedsettings7-enablesuperpan.md)<br/>                           | Lecture/écriture<br/> | Spécifie ou récupère une valeur qui indique si SuperPan est activé ou désactivé.<br/>                                                    |
| [**NetworkConnectionType**](imsrdpclientadvancedsettings7-networkconnectiontype.md)<br/>             | Lecture/écriture<br/> | Spécifie ou récupère une valeur qui indique le type de connexion réseau.<br/>                                                                |
| [**RedirectDirectX**](imsrdpclientadvancedsettings7-redirectdirectx.md)<br/>                         | Lecture/écriture<br/> | Cette propriété n'est pas utilisée.<br/>                                                                                                                |
| [**SuperPanAccelerationFactor**](imsrdpclientadvancedsettings7-superpanaccelerationfactor.md)<br/>   | Lecture/écriture<br/> | Spécifie ou récupère une valeur qui indique le facteur d’accélération SuperPan.<br/>                                                           |
| [**VideoPlaybackMode**](imsrdpclientadvancedsettings7-videoplaybackmode.md)<br/>                     | Lecture/écriture<br/> | Spécifie ou récupère une valeur qui indique le mode de lecture vidéo.<br/>                                                                    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                                |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings7 est défini en tant que 26036036-4010-4578-8091-0db9a1edf9c3<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

