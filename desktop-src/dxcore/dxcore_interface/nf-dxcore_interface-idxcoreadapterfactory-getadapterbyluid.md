---
title: IDXCoreAdapterFactory::GetAdapterByLuid
description: Récupère l’objet d’adaptateur DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) pour un LUID spécifié, s’il est disponible.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: d8f72aba23b9a1f57094b39e5afba3740f8749348c6a2da6a8753f72a7a0e6ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787050"
---
# <a name="idxcoreadapterfactorygetadapterbyluid-method"></a>IDXCoreAdapterFactory :: GetAdapterByLuid, méthode

Récupère l’objet d’adaptateur DXCore ([IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)) pour un LUID spécifié, s’il est disponible. Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Syntaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
   REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapterByLuid( 
  const LUID &adapterLUID,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a>Paramètres

### <a name="adapterluid"></a>adapterLUID

Type : **[LUID](/windows/win32/api/winnt/ns-winnt-luid) const\&**

Valeur locale unique qui identifie l’instance de l’adaptateur.

### <a name="riid-in"></a>riid [in]

Type : **REFIID**

Référence à l’identificateur global unique (GUID) de l’interface que vous souhaitez retourner dans *ppvAdapter*. Il doit s’agir de l’identificateur d’interface (IID) de [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md).

### <a name="ppvadapter-out"></a>ppvAdapter [out]

Type : **void \* \***

Adresse d’un pointeur vers une interface avec l’IID spécifié dans le paramètre *riid* . Une fois le retour réussi, *\* ppvAdapter* (l’adresse déréférencée) contient un pointeur vers l’adaptateur dxcore créé.

## <a name="returns"></a>Retours

Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.

|Valeur retournée|Description|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|Le LUID d’adaptateur transmis dans *adapterLUID* est reconnu, mais l’état de l’adaptateur n’est plus valide.|
|E_INVALIDARG|Aucun LUID d’adaptateur de ce type, car la valeur transmise dans *adapterLUID* est disponible via dxcore.|
|E_NOINTERFACE|Une valeur non valide a été fournie pour *riid*.|
|E_POINTER|`nullptr` a été fourni pour *ppvAdapter*.|

## <a name="remarks"></a>Remarques

Plusieurs appels passant le même [LUID](/windows/win32/api/winnt/ns-winnt-luid) retournent des pointeurs d’interface identiques. Par conséquent, il est possible de comparer des pointeurs d’interface pour déterminer si plusieurs pointeurs font référence au même objet d’adaptateur.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)