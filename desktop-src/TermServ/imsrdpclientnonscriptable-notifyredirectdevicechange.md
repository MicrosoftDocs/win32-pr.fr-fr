---
title: Méthode IMsRdpClientNonScriptable NotifyRedirectDeviceChange
description: notifie le module de redirection de l’appareil du contrôle de Bureau à distance ActiveX qu’une modification de l’appareil s’est produite sur le système. Cette méthode passe \_ les notifications WM DEVICECHANGE au contrôle.
ms.assetid: 36323831-06e0-4e47-8a6c-06367119298f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode NotifyRedirectDeviceChange
- Méthode NotifyRedirectDeviceChange Services Bureau à distance, interface IMsRdpClientNonScriptable
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable, méthode NotifyRedirectDeviceChange
- Méthode NotifyRedirectDeviceChange Services Bureau à distance, interface IMsRdpClientNonScriptable2
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable2, méthode NotifyRedirectDeviceChange
- Méthode NotifyRedirectDeviceChange Services Bureau à distance, interface IMsRdpClientNonScriptable3
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable3, méthode NotifyRedirectDeviceChange
- Méthode NotifyRedirectDeviceChange Services Bureau à distance, interface IMsRdpClientNonScriptable4
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable4, méthode NotifyRedirectDeviceChange
- Méthode NotifyRedirectDeviceChange Services Bureau à distance, interface IMsRdpClientNonScriptable5
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable5, méthode NotifyRedirectDeviceChange
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable2.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable3.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable4.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable5.NotifyRedirectDeviceChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37986a218f672f5ace6d81b6496b958547e70a95f8ddea91bf6a130eb05b1ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130076"
---
# <a name="imsrdpclientnonscriptablenotifyredirectdevicechange-method"></a>IMsRdpClientNonScriptable :: NotifyRedirectDeviceChange, méthode

notifie le module de redirection de l’appareil du contrôle de Bureau à distance ActiveX qu’une modification de l’appareil s’est produite sur le système. Cette méthode passe les notifications [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) au contrôle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT NotifyRedirectDeviceChange(
  [in] WPARAM wParam,
  [in] LPARAM lParam
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Spécifie l’événement d’appareil. Ce paramètre peut prendre les valeurs suivantes.

<dt>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT \_ CONFIGCHANGECANCELED**


</dt> <dd>

Une demande de modification de la configuration actuelle (ancrer ou détacher) a été annulée.

</dd> <dt>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT \_ CONFIGCHANGED**


</dt> <dd>

La configuration actuelle a été modifiée en raison d’une station d’accueil ou d’une déconnexion.

</dd> <dt>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT \_ CUSTOMEVENT**


</dt> <dd>

Un événement personnalisé s’est produit.

</dd> <dt>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT \_ DEVICEARRIVAL**


</dt> <dd>

Un appareil a été inséré et est maintenant disponible.

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT \_ DEVICEQUERYREMOVE**


</dt> <dd>

Une autorisation est requise pour supprimer un appareil. Toute application peut refuser cette demande et annuler la suppression.

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT \_ DEVICEQUERYREMOVEFAILED**


</dt> <dd>

Une demande de suppression d’un appareil a été annulée.

</dd> <dt>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT \_ DEVICEREMOVECOMPLETE**


</dt> <dd>

Un appareil a été supprimé.

</dd> <dt>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT \_ DEVICEREMOVEPENDING**


</dt> <dd>

Un appareil va être supprimé. La suppression ne peut pas être refusée.

</dd> <dt>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT \_ DEVICETYPESPECIFIC**


</dt> <dd>

Un événement spécifique à l’appareil s’est produit.

</dd> <dt>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT \_ DEVNODES \_ modifié**


</dt> <dd>

Un appareil a été ajouté ou supprimé du système.

</dd> <dt>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT \_ QUERYCHANGECONFIG**


</dt> <dd>

Une autorisation est requise pour modifier la configuration actuelle (ancrer ou détacher).

</dd> <dt>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT \_ USERDEFINED**


</dt> <dd>

La signification de ce message est définie par l’utilisateur.

</dd> </dl> </dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Pointeur vers une structure qui contient des données spécifiques à l’événement. Son format dépend de la valeur du paramètre *wParam* . Pour plus d’informations, reportez-vous à la documentation de chaque événement. Pour plus d’informations, consultez [types d’événements d’appareil](/windows/desktop/DevIO/device-event-types).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Remarques

Une application conteneur qui permet l’ajout ou la suppression dynamique d’appareils doit traiter le message [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) dans sa fenêtre de niveau supérieur et transférer le message au contrôle à l’aide de la méthode **NotifyRedirectDeviceChange** . Par exemple, un changement de périphérique dynamique se fait lorsqu’un lecteur de disque Redirigé est ajouté ou supprimé pendant que le système est en cours d’exécution.

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                               |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable est défini en tant que 2f079c4c-87B2-4AFD-97ab-20cdb43038ae<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> </dl>

 

