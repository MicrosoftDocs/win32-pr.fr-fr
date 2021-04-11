---
description: Inscrit une application en cours d’exécution pour la notification d’événements WIA (Windows Image Acquisition) 2,0.
ms.assetid: 978dcd41-d63b-421d-b7e1-8e9368b36180
title: 'IWiaDevMgr2 :: RegisterEventCallbackInterface, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.RegisterEventCallbackInterface
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 7cd3a7e00cff56bc5d91bfc843ab79fe71aa1123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202887"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a>IWiaDevMgr2 :: RegisterEventCallbackInterface, méthode

Inscrit une application en cours d’exécution pour la notification d’événements WIA (Windows Image Acquisition) 2,0.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RegisterEventCallbackInterface(
  [in]        LONG              lFlags,
  [in]        BSTR              bstrDeviceID,
  [in]  const GUID              *pEventGUID,
  [in]        IWiaEventCallback *pIWiaEventCallback,
  [out]       IUnknown          **pEventObject
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lFlags* \[ dans\]
</dt> <dd>

Type : **long**

Actuellement inutilisé. Doit être défini sur zéro (0).

</dd> <dt>

*bstrDeviceID* \[ dans\]
</dt> <dd>

Type : **BSTR**

Spécifie l’identificateur unique d’un appareil WIA 2,0. Affectez la valeur **null** à ce paramètre pour vous inscrire à l’événement sur tous les appareils WIA 2,0.

</dd> <dt>

*pEventGUID* \[ dans\]
</dt> <dd>

Type : * #*const \* GUID* _

Spécifie un pointeur vers l’identificateur d’événement pour lequel l’application est inscrite. Consultez [identificateurs d’événements WIA](-wia-wia-event-identifiers.md) pour les identificateurs d’événements standard.

</dd> <dt>

_pIWiaEventCallback * \[ dans\]
</dt> <dd>

Tapez : **[**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) \** _

Spécifie un pointeur vers l’interface [_ *IWiaEventCallback* *](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) que l’WIA 2,0 utilise pour envoyer une notification d’événement.

</dd> <dt>

*pEventObject* \[ à\]
</dt> <dd>

Type : **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***

Reçoit l’adresse d’un pointeur vers l’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Retourne les codes d’erreur COM standard ou les éléments suivants.



| Code de retour                                                                               | Description                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**\_NOTIMPL E**</dt> </dl> | L’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) ne peut pas être retournée. <br/> |



 

## <a name="remarks"></a>Notes

> [!WARNING]
> L’utilisation des méthodes [**IWiaDevMgr :: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2 :: RegisterEventCallbackInterface** et [**devicemanager. RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) à partir du même processus après le redémarrage du service image continue peut entraîner une violation d’accès, si les fonctions ont été utilisées avant l’arrêt du service.

 

Lorsque les applications WIA 2,0 commencent à s’exécuter, elles utilisent cette méthode pour s’inscrire afin de recevoir des événements de périphérique matériel. Cela empêche l’application d’être redémarrée lorsqu’un autre événement pour lequel elle est inscrite se produit. Une fois qu’une application appelle **IWiaDevMgr2 :: RegisterEventCallbackInterface** pour s’inscrire pour recevoir les événements WIA 2,0 d’un appareil, les événements inscrits sont acheminés vers le programme par WIA 2,0.

Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *pEventObject* .

> [!Note]  
> Dans une application multithread, le rappel de notification d’événements peut se trouver sur un thread différent de celui qui a inscrit le rappel.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
