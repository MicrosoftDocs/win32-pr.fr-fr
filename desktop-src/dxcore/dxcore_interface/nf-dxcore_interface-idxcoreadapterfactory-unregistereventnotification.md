---
title: IDXCoreAdapterFactory::UnregisterEventNotification
description: Annule l’inscription d’une notification que vous avez inscrite précédemment pour.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6bb12126769a914680ea17ac9e6060346001c795
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382447"
---
# <a name="idxcoreadapterfactoryunregistereventnotification-method"></a>IDXCoreAdapterFactory :: UnregisterEventNotification, méthode

Annule l’inscription d’une notification que vous avez inscrite précédemment pour. Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Syntaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE UnregisterEventNotification(
  uint32_t eventCookie) = 0;
```

## <a name="parameters"></a>Paramètres

### <a name="eventcookie"></a>eventCookie

Type : **uint32_t**

Valeur de cookie (retournée quand vous avez appelé [IDXCoreAdapterFactory :: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)) qui représente une inscription antérieure pour laquelle vous souhaitez annuler l’inscription.

## <a name="returns"></a>Retours

Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.

|Valeur retournée|Description|
|-|-|
|E_INVALIDARG|La valeur de *eventCookie* n’est pas un cookie valide représentant une inscription antérieure.|

## <a name="remarks"></a>Notes

**UnregisterEventNotification** retourne uniquement une fois que tous les rappels en attente/en cours pour cette inscription sont terminés. DXCore garantit qu’aucun nouveau rappel ne se produira pour cette inscription après que **UnregisterEventNotification** a retourné. Toutefois, pour éviter un blocage, si vous appelez **UnregisterEventNotification** à partir de votre rappel, **UnregisterEventNotification** n’attend pas que le rappel actif se termine.

> [!IMPORTANT]
> Avant de détruire l’objet DXCore représenté par l’argument *dxCoreObject* passé à [IDXCoreAdapterFactory :: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), vous devez utiliser la valeur cookie pour annuler l’inscription de cet objet dans les notifications en appelant **UnregisterEventNotification**. Si vous ne le faites pas, une exception irrécupérable est générée lorsque la situation est détectée.

Une fois que vous annulez l’inscription d’une valeur de cookie, cette valeur peut ensuite être retournée par une inscription suivante

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [IDXCoreAdapterFactory :: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [DXCore Reference](../dxcore-reference.md), [à l’aide de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)