---
title: IDXCoreAdapterFactory::RegisterEventNotification
description: S’inscrit pour recevoir des notifications de conditions spécifiques à partir d’un adaptateur DXCore ou d’une liste d’adaptateurs.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3643fbb01fc955049c297a577f18d4d276e73f46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463507"
---
# <a name="idxcoreadapterfactoryregistereventnotification-method"></a>IDXCoreAdapterFactory :: RegisterEventNotification, méthode

S’inscrit pour recevoir des notifications de conditions spécifiques à partir d’un adaptateur DXCore ou d’une liste d’adaptateurs. Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Syntaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE RegisterEventNotification(
  _In_ IUnknown *dxCoreObject,
  DXCoreNotificationType notificationType,
  _In_ PFN_DXCORE_NOTIFICATION_CALLBACK callbackFunction,
  _In_opt_ void *callbackContext,
  _Out_ uint32_t *eventCookie) = 0;
```

## <a name="parameters"></a>Paramètres

### <a name="dxcoreobject-in"></a>dxCoreObject [in]

Type : **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Objet DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) ou [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)) dont vous êtes abonné aux notifications.

### <a name="notificationtype"></a>notificationType

Type : **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

Type de notification pour laquelle vous effectuez l’inscription. Consultez le tableau dans [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) pour plus d’informations sur les types qui sont valides avec les genres d’objets.

### <a name="callbackfunction-in"></a>callbackFunction [in]

Type : **[PFN_DXCORE_NOTIFICATION_CALLBACK](./nc-dxcore_interface-pfn_dxcore_notification_callback.md)**

Pointeur vers une fonction de rappel (implémentée par votre application), qui est appelée par l’objet DXCore pour les événements de notification. Pour obtenir la signature de la fonction, consultez [PFN_DXCORE_NOTIFICATION_CALLBACK](./nc-dxcore_interface-pfn_dxcore_notification_callback.md).

### <a name="callbackcontext-in"></a>callbackContext [in]

Type : **void \***

Pointeur facultatif vers un objet contenant des informations de contexte. Cet objet est passé à votre fonction de rappel lorsque la notification est déclenchée.

### <a name="eventcookie-out"></a>eventCookie [out]

Type : **uint32_t \***

Pointeur vers une valeur **uint32_t** . En cas de réussite, la fonction déréférence le pointeur et définit la valeur sur une valeur de cookie différente de zéro représentant cette inscription. Utilisez cette valeur de cookie pour annuler l’inscription de la notification en appelant [IDXCoreAdapterFactory :: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md). Consultez la **section Notes**.

En cas d’échec, la fonction déréférence le pointeur et définit la valeur sur zéro, ce qui représente une valeur de cookie non valide.

## <a name="returns"></a>Retours

Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.

|Valeur retournée|Description|
|-|-|
|DXGI_ERROR_INVALID_CALL|*NotificationType* n’est pas pris en charge par le système d’exploitation (OS).|
|E_INVALIDARG|`nullptr` a été fourni pour *dxCoreObject* ou si une combinaison *NotificationType* et *dxCoreObject* non valide a été fournie.|
|E_POINTER|`nullptr` a été fourni pour *callbackFunction* ou *eventCookie*.|

## <a name="remarks"></a>Notes

Vous utilisez **RegisterEventNotification** pour vous inscrire aux événements déclenchés par les interfaces [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) et [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) . Ces types de notifications sont pris en charge.

|[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)|*DxCoreObject* pris en charge|Notes|
|-|-|-|
|AdapterListStale|**IDXCoreAdapterList**|Indique que la liste des adaptateurs répondant à vos critères de filtre a changé. Si la liste des adaptateurs est périmée au moment de l’inscription, votre rappel est immédiatement appelé. Ce rappel se produit au plus une fois par inscription.|
|AdapterNoLongerValid|**IDXCoreAdapter**|Indique que l’adaptateur n’est plus valide. Si l’adaptateur n’est pas valide au moment de l’inscription, votre rappel est immédiatement appelé.|
|AdapterBudgetChange|**IDXCoreAdapter**|Indique qu’un événement de budgétisation de mémoire s’est produit et que vous devez appeler [IDXCoreAdapter :: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) (avec [DXCoreAdapterState :: AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md)) pour évaluer l’état actuel du budget de la mémoire. Lors de l’inscription, un rappel initial se produira toujours pour vous permettre d’interroger l’état initial.|
|AdapterHardwareContentProtectionTeardown|**IDXCoreAdapter**|Indique que vous devez réévaluer l’état actuel de la session de chiffrement. par exemple, en appelant [ID3D11VideoContext1 :: CheckCryptoSessionStatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) pour déterminer l’impact de la démontage du matériel pour une interface [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) spécifique. Lors de l’inscription, un rappel initial se produira toujours pour vous permettre d’interroger l’état initial.|

Un appel à la fonction que vous fournissez dans *callbackFunction* est effectué de façon asynchrone sur un thread d’arrière-plan par dxcore lorsque l’événement détecté se produit. Aucune garantie n’est établie en ce qui concerne le classement ou le minutage des rappels &mdash; . plusieurs rappels peuvent se produire dans n’importe quel ordre, voire simultanément. Il est même possible d’appeler votre rappel avant la fin de **RegisterEventNotification** . Dans ce cas, DXCore garantit que votre *eventCookie* est défini avant l’appel de votre rappel. Plusieurs rappels pour une inscription spécifique sont sérialisés dans l’ordre.

Les rappels peuvent se produire à tout moment jusqu’à ce que vous appeliez [UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)et qu’il se termine. Les rappels se produisent sur leurs propres threads, et vous pouvez effectuer des appels dans l’API DXCore sur ces threads, y compris **UnregisterEventNotification**. Toutefois, vous ne devez pas libérer la dernière référence à *dxCoreObject* sur ce thread.

> [!IMPORTANT]
> Avant de détruire l’objet DXCore représenté par l’argument *dxCoreObject* passé à **RegisterEventNotification**, vous devez utiliser la valeur cookie pour annuler l’inscription de cet objet dans les notifications en appelant [IDXCoreAdapterFactory :: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md). Si vous ne le faites pas, une exception irrécupérable est générée lorsque la situation est détectée.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory :: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), [DXCore Reference](../dxcore-reference.md), [à l’aide de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)