---
title: IDXCoreAdapterList::GetAdapter
description: Récupère un adaptateur spécifique par index à partir d’un objet de liste d’adaptateurs DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 5ba03c9e6f2711adc5264354a6abd70ee489965f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031667"
---
# <a name="idxcoreadapterlistgetadapter-method"></a>IDXCoreAdapterList :: GetAdapter, méthode

Récupère un adaptateur spécifique par index à partir d’un objet de liste d’adaptateurs DXCore. Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Syntaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE GetAdapter(
  uint32_t index,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapter) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE GetAdapter( 
  uint32_t index,
  _COM_Outptr_ T **ppvAdapter);
```

## <a name="parameters"></a>Paramètres

### <a name="index"></a>index

Type : **uint32_t**

Index de base zéro identifiant une instance d’adaptateur dans la liste d’adaptateurs DXCore.

### <a name="riid"></a>riid

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
|DXGI_ERROR_DEVICE_REMOVED|L' *index* est valide, mais l’état de l’adaptateur n’est plus valide.|
|E_INVALIDARG|L' *index* fourni n’est pas valide.|
|E_NOINTERFACE|Une valeur non valide a été fournie pour *riid*.|
|E_POINTER|`nullptr` a été fourni pour *ppvAdapter*.|

## <a name="remarks"></a>Notes

Plusieurs appels qui passent un index qui représente le même adaptateur retournent des pointeurs d’interface identiques, y compris entre différentes listes d’adaptateurs. Par conséquent, il est possible de comparer des pointeurs d’interface pour déterminer si plusieurs pointeurs font référence au même objet d’adaptateur.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)