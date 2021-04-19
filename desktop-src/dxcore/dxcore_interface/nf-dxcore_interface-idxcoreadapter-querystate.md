---
title: IDXCoreAdapter::QueryState
description: Récupère l’état actuel de l’élément spécifié sur l’adaptateur.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 61fc5c601904011de8f343777a95385a16ec3d7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511091"
---
# <a name="idxcoreadapterquerystate-method"></a>IDXCoreAdapter :: QueryState, méthode

Récupère l’état actuel de l’élément spécifié sur l’adaptateur. Avant d’appeler **QueryState** pour un type de propriété, appelez [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) pour confirmer que l’interrogation du genre d’État est disponible pour cet adaptateur et le système d’exploitation.

## <a name="syntax"></a>Syntaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE QueryState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t outputBufferSize,
  _Out_writes_bytes_(outputBufferSize) void *outputBuffer) = 0;

template <class T1, class T2>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _In_reads_bytes_opt_(sizeof(T1)) const T1 *inputStateDetails,
  _Out_writes_bytes_(sizeof(T2)) T2 *outputBuffer);

template <class T>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _Out_writes_bytes_(sizeof(T)) T *outputBuffer);
```

## <a name="parameters"></a>Paramètres

### <a name="state"></a>state

Type : **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

Type d’élément d’État sur l’adaptateur dont vous souhaitez récupérer l’État. Consultez le tableau dans [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) pour plus d’informations sur chaque type d’état de l’adaptateur.

### <a name="inputstatedetailssize"></a>inputStateDetailsSize

Type : **size_t**

Taille, en octets, de la mémoire tampon des détails de l’état d’entrée que vous pouvez également allouer et fournir dans *inputStateDetails*.

### <a name="inputstatedetails-in"></a>inputStateDetails [in]

Type : **void const \***

Pointeur facultatif vers une mémoire tampon de détails d’état d’entrée constante que vous allouez dans votre application, contenant toutes les informations relatives à votre demande requises pour le genre d’État que vous spécifiez dans *État*. Consultez le tableau dans [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) pour plus d’informations sur les exigences en matière de mémoire tampon d’entrée pour un type d’État donné.

### <a name="outputbuffersize"></a>outputBufferSize

Type : **size_t**

Taille, en octets, de la mémoire tampon de sortie que vous allouez et fournissez dans *OUTPUTBUFFER*.

### <a name="outputbuffer-out"></a>outputBuffer [out]

Type : **void \***

Pointeur vers une mémoire tampon de sortie que vous allouez dans votre application, et que la fonction remplit. Consultez le tableau dans [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) pour plus d’informations sur la spécification de la mémoire tampon de sortie pour un type d’État donné.

## <a name="returns"></a>Retours

Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.

|Valeur retournée|Description|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|L’état de l’adaptateur n’est plus valide.|
|DXGI_ERROR_INVALID_CALL|Le genre d’état spécifié dans l' *État* n’est pas reconnu par ce système d’exploitation. Appelez [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) pour confirmer que l’interrogation du genre d’État est disponible pour cet adaptateur et le système d’exploitation.|
|DXGI_ERROR_UNSUPPORTED|Le genre d’état spécifié dans l' *État* n’est pas pris en charge par l’adaptateur. Appelez [IsQueryStateSupported](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) pour confirmer que l’interrogation du genre d’État est disponible pour cet adaptateur et le système d’exploitation.|
|E_INVALIDARG|Une taille de mémoire tampon insuffisante est fournie pour *OUTPUTBUFFER* (ou pour *inputStateDetails* où un tampon de détails d’état d’entrée est nécessaire).|
|E_POINTER|`nullptr` a été fourni pour *OUTPUTBUFFER* (ou pour *inputStateDetails* où un tampon de détails d’état d’entrée est nécessaire).|

## <a name="remarks"></a>Notes

Pour plus d’informations sur chaque type d’état de l’adaptateur et sur les entrées et les sorties utilisées, consultez [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) . Cette fonction met à zéro la mémoire tampon *OUTPUTBUFFER* avant de la remplir.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)