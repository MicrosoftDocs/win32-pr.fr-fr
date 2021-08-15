---
description: inscrit une application en cours d’exécution pour la notification d’événement 2,0 de l’Acquisition d’images (WIA) de Windows.
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
ms.openlocfilehash: e2658654254257c707d12f4e676aee3371f0ad491dfedeb0637508ca3f33a057
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965638"
---
# <a name="iwiadevmgr2registereventcallbackinterface-method"></a>IWiaDevMgr2 :: RegisterEventCallbackInterface, méthode

inscrit une application en cours d’exécution pour la notification d’événement 2,0 de l’Acquisition d’images (WIA) de Windows.

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

Type : **const GUID \***

Spécifie un pointeur vers l’identificateur d’événement pour lequel l’application est inscrite. Consultez [identificateurs d’événements WIA](-wia-wia-event-identifiers.md) pour les identificateurs d’événements standard.

</dd> <dt>

*pIWiaEventCallback* \[ dans\]
</dt> <dd>

Type : **[ **IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback)\***

Spécifie un pointeur vers l’interface [**IWiaEventCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaeventcallback) que l’WIA 2,0 utilise pour envoyer une notification d’événement.

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



 

## <a name="remarks"></a>Remarques

> [!WARNING]
> L’utilisation des méthodes [**IWiaDevMgr :: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface), **IWiaDevMgr2 :: RegisterEventCallbackInterface** et [**devicemanager. RegisterEvent**](/previous-versions/windows/desktop/wiaaut/-wiaaut-idevicemanager-registerevent) à partir du même processus après le redémarrage du service image continue peut entraîner une violation d’accès, si les fonctions ont été utilisées avant l’arrêt du service.

 

Lorsque les applications WIA 2,0 commencent à s’exécuter, elles utilisent cette méthode pour s’inscrire afin de recevoir des événements de périphérique matériel. Cela empêche l’application d’être redémarrée lorsqu’un autre événement pour lequel elle est inscrite se produit. Une fois qu’une application appelle **IWiaDevMgr2 :: RegisterEventCallbackInterface** pour s’inscrire pour recevoir les événements WIA 2,0 d’un appareil, les événements inscrits sont acheminés vers le programme par WIA 2,0.

Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *pEventObject* .

> [!Note]  
> Dans une application multithread, le rappel de notification d’événements peut se trouver sur un thread différent de celui qui a inscrit le rappel.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
