---
title: IMsTscAdvancedSettings propriété ContainerHandledFullScreen
description: Spécifie si le mode plein écran géré par le conteneur est activé.
ms.assetid: 67679323-4a74-4d91-abd0-607415295f3d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ContainerHandledFullScreen
- Services Bureau à distance de la propriété ContainerHandledFullScreen, interface IMsTscAdvancedSettings
- Services Bureau à distance de l’interface IMsTscAdvancedSettings, propriété ContainerHandledFullScreen
- Services Bureau à distance de la propriété ContainerHandledFullScreen, interface IMsRdpClientAdvancedSettings
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings, propriété ContainerHandledFullScreen
- Services Bureau à distance de la propriété ContainerHandledFullScreen, interface IMsRdpClientAdvancedSettings2
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings2, propriété ContainerHandledFullScreen
- Services Bureau à distance de la propriété ContainerHandledFullScreen, interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, propriété ContainerHandledFullScreen
- Services Bureau à distance de la propriété ContainerHandledFullScreen, interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, propriété ContainerHandledFullScreen
- Services Bureau à distance de la propriété ContainerHandledFullScreen, interface IMsRdpClientAdvancedSettings5
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings5, propriété ContainerHandledFullScreen
- Services Bureau à distance de la propriété ContainerHandledFullScreen, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété ContainerHandledFullScreen
- Services Bureau à distance de la propriété ContainerHandledFullScreen, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété ContainerHandledFullScreen
- Services Bureau à distance de la propriété ContainerHandledFullScreen, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété ContainerHandledFullScreen
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.ContainerHandledFullScreen
- IMsTscAdvancedSettings.get_ContainerHandledFullScreen
- IMsTscAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.put_ContainerHandledFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 975581aaca4aad2511396e8ec426a7bf2a4720ff54202d42fbe932c0c2e9464d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513119"
---
# <a name="imstscadvancedsettingscontainerhandledfullscreen-property"></a>IMsTscAdvancedSettings :: ContainerHandledFullScreen, propriété

Spécifie si le mode plein écran géré par le conteneur est activé.

> [!Note]  
> la valeur de la propriété **ContainerHandledFullScreen** n’a aucun effet lorsque l’Bureau à distance ActiveX contrôle est sécurisé pour l’écriture de scripts, et renvoie la valeur **\_ false** en cas de tentative de modification de la valeur.

 

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_ContainerHandledFullScreen(
  [in]  BOOL ContainerHandledFullScreen
);

HRESULT get_ContainerHandledFullScreen(
  [out] BOOL *pContainerHandledFullScreen
);
```



## <a name="property-value"></a>Valeur de la propriété

Définissez ce paramètre sur **true** pour activer le mode ou une autre valeur pour désactiver le mode.

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite. Retourne **S \_ false** s’il n’est pas pris en charge.

## <a name="remarks"></a>Remarques

Quand ce mode est activé, le conteneur actuel traite le commutateur dans et hors du mode plein écran. Cette méthode doit être utilisée uniquement si le conteneur actuel a besoin d’un contrôle étendu sur le comportement du mode plein écran. Quand cette propriété est définie, le contrôle n’entre pas en mode plein écran en réponse à la combinaison de touches de raccourci du mode plein écran (CTRL + ALT + ATTN); au lieu de cela, les événements [**IMsTscAxEvents :: OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md) et [**IMsTscAxEvents :: OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md) sont appelés. Pour plus d’informations sur ces événements, consultez [**IMsTscAxEvents**](imstscaxevents-interface.md) .

La plupart des applications de conteneur n’ont pas besoin d’utiliser le mode plein écran géré par le conteneur.

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                            |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings est défini en tant que 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





