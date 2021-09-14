---
title: Méthode IMsRdpClient RequestClose
description: demande un arrêt approprié du contrôle de Bureau à distance ActiveX.
ms.assetid: 0b930a00-f134-4da2-a752-8fd131a22043
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RequestClose
- Méthode RequestClose Services Bureau à distance, interface IMsRdpClient
- Services Bureau à distance de l’interface IMsRdpClient, méthode RequestClose
- Méthode RequestClose Services Bureau à distance, interface IMsRdpClient2
- Services Bureau à distance de l’interface IMsRdpClient2, méthode RequestClose
- Méthode RequestClose Services Bureau à distance, interface IMsRdpClient3
- Services Bureau à distance de l’interface IMsRdpClient3, méthode RequestClose
- Méthode RequestClose Services Bureau à distance, interface IMsRdpClient4
- Services Bureau à distance de l’interface IMsRdpClient4, méthode RequestClose
- Méthode RequestClose Services Bureau à distance, interface IMsRdpClient5
- Services Bureau à distance de l’interface IMsRdpClient5, méthode RequestClose
- Méthode RequestClose Services Bureau à distance, interface IMsRdpClient6
- Services Bureau à distance de l’interface IMsRdpClient6, méthode RequestClose
- Méthode RequestClose Services Bureau à distance, interface IMsRdpClient7
- Services Bureau à distance de l’interface IMsRdpClient7, méthode RequestClose
- Méthode RequestClose Services Bureau à distance, interface IMsRdpClient8
- Services Bureau à distance de l’interface IMsRdpClient8, méthode RequestClose
- Méthode RequestClose Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode RequestClose
- Méthode RequestClose Services Bureau à distance, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, méthode RequestClose
topic_type:
- apiref
api_name:
- IMsRdpClient.RequestClose
- IMsRdpClient2.RequestClose
- IMsRdpClient3.RequestClose
- IMsRdpClient4.RequestClose
- IMsRdpClient5.RequestClose
- IMsRdpClient6.RequestClose
- IMsRdpClient7.RequestClose
- IMsRdpClient8.RequestClose
- IMsRdpClient9.RequestClose
- IMsRdpClient10.RequestClose
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1679b08680b962cdbff57e9bbbd1c392607d8709
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126856936"
---
# <a name="imsrdpclientrequestclose-method"></a>IMsRdpClient :: RequestClose, méthode

demande un arrêt approprié du contrôle de Bureau à distance ActiveX. Un arrêt approprié peut inclure la fin de la session de Services Bureau à distance de l’utilisateur, mais il n’arrête pas le serveur hôte de session Bureau à distance (hôte de session Bureau à distance).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RequestClose(
  [out] ControlCloseStatus *pCloseStatus
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pCloseStatus* \[ à\]
</dt> <dd>

Valeur de l’énumération [**ControlCloseStatus**](controlclosestatus.md) qui indique si l’application peut fermer le contrôle immédiatement. Voici une liste de valeurs possibles.

<dt>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>

<span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed** (0x0000)


</dt> <dd>

L’application conteneur peut continuer à fermer le contrôle immédiatement. Cette valeur peut également indiquer que la connexion a déjà été arrêtée.

</dd> <dt>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>

<span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents** (0x0001)


</dt> <dd>

L’application conteneur ne doit pas fermer le contrôle immédiatement ; l’application doit attendre que l’un des événements décrits dans la section Notes suivante se produise avant la fermeture.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Notes

Si le paramètre *pCloseStatus* est égal à **controlCloseWaitForEvents**, l’application doit attendre que l’un des événements suivants se produise avant que l’application ne ferme le contrôle :

-   [**IMsTscAxEvents :: OnDisconnected**](imstscaxevents-ondisconnected.md). Si l’utilisateur n’est pas connecté à la session Services Bureau à distance, l’application peut appeler la fonction [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) pour détruire toutes les fenêtres, puis fermer le contrôle.
-   [**IMsTscAxEvents :: OnConfirmClose**](imstscaxevents-onconfirmclose.md). Si l’utilisateur est connecté à la session Services Bureau à distance, le contrôle déclenche un événement **OnConfirmClose** . Cet événement permet à l’application de demander à l’utilisateur s’il faut fermer la connexion. Si l’utilisateur répond oui à l’invite, l’application conteneur peut appeler [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) pour détruire toutes les fenêtres et fermer le contrôle.

**RequestClose** permet à une application de conteneur de demander à l’utilisateur s’il faut fermer une connexion. Pour plus d’informations, consultez [**IMsTscAxEvents :: OnConfirmClose**](imstscaxevents-onconfirmclose.md).

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient est défini en tant que 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

