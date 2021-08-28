---
title: DXCoreNotificationType
description: Définit des constantes qui spécifient les types de notifications déclenchés par les objets [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) ou [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) .
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 230b6c103f83e72dfe0ba7803cde4b4695a32de724ce44c1aaccf5131d077bad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726009"
---
# <a name="dxcorenotificationtype-enum"></a>Énumération DXCoreNotificationType

Définit des constantes qui spécifient les types de notifications déclenchés par les objets [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) ou [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) .

Vous pouvez enregistrer et annuler l’inscription de ces notifications en appelant [IDXCoreAdapterFactory :: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) et [IDXCoreAdapterFactory :: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), respectivement.

## <a name="syntax"></a>Syntaxe

```cpp
enum class DXCoreNotificationType : uint32_t
{
  AdapterListStale = 0,
  AdapterNoLongerValid = 1,
  AdapterBudgetChange = 2,
  AdapterHardwareContentProtectionTeardown = 3
};
```

## <a name="constants"></a>Constantes

### <a name="adapterliststale"></a>AdapterListStale

Cette notification est déclenchée par un objet <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist">IDXCoreAdapterList</a> lorsque la liste des adaptateurs devient obsolète. La transition actualisée est unidirectionnelle et ponctuelle. par conséquent, cette notification est déclenchée au plus une fois.

### <a name="adapternolongervalid"></a>AdapterNoLongerValid

Cette notification est déclenchée par un objet <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> lorsque l’adaptateur n’est plus valide. La transition valide-à-non valide est unidirectionnelle et ponctuelle. par conséquent, cette notification est déclenchée au plus une fois.

### <a name="adapterbudgetchange"></a>AdapterBudgetChange

Cette notification est déclenchée par un objet <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> lorsqu’une modification de budget d’adaptateur se produit. Cette notification peut se produire plusieurs fois. L’utilisation de cette notification est fonctionnellement similaire à <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent">IDXGIAdapter3 :: RegisterVideoMemoryBudgetChangeNotificationEvent</a>. En réponse à cet événement, vous devez appeler [IDXCoreAdapter :: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) (avec [DXCoreAdapterState :: AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md)) pour évaluer l’état actuel du budget de la mémoire.

### <a name="adapterhardwarecontentprotectionteardown"></a>AdapterHardwareContentProtectionTeardown

Cette notification est déclenchée par un objet <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> pour notifier le démontage de la protection du contenu matériel d’un adaptateur. Cette notification peut se produire plusieurs fois. Elle est fonctionnellement similaire à <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registerhardwarecontentprotectionteardownstatusevent">IDXGIAdapter3 :: RegisterHardwareContentProtectionTeardownStatusEvent</a>. En réponse à cet événement, vous devez réévaluer l’état actuel de la session de chiffrement. par exemple, en appelant [ID3D11VideoContext1 :: CheckCryptoSessionStatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) pour déterminer l’impact de la démontage du matériel pour une interface [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) spécifique.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapterFactory :: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [IDXCoreAdapterFactory :: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)