---
title: IDXCoreAdapter::GetPropertySize
description: Pour une propriété de l’adaptateur spécifiée, récupère la taille de la mémoire tampon, en octets, requise pour un appel à [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ff077d3c4c827a55f7fd9b10dfe93f1271649f72
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918032"
---
# <a name="idxcoreadaptergetpropertysize-method"></a>IDXCoreAdapter :: GetPropertySize, méthode

Pour une propriété de l’adaptateur spécifiée, récupère la taille de la mémoire tampon, en octets, requise pour un appel à [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md). Avant d’appeler **GetPropertySize** pour un type de propriété, appelez [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) pour confirmer que le type de propriété est disponible pour cet adaptateur et le système d’exploitation.

## <a name="syntax"></a>Syntaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE GetPropertySize(
  DXCoreAdapterProperty property,
  _Out_ size_t *bufferSize) = 0;
```

## <a name="parameters"></a>Paramètres

### <a name="property"></a>propriété

Type : **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Type de la propriété dont vous souhaitez récupérer la taille, en octets.

### <a name="buffersize-out"></a>bufferSize [out]

Type : **size_t \***

Pointeur vers une valeur **size_t** . La fonction déréférence le pointeur et affecte à la valeur la taille, en octets, de la mémoire tampon de sortie que vous devez allouer et passer comme argument *PropertyData* dans votre appel à [GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md).

## <a name="returns"></a>Retours

Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.

|Valeur de retour|Description|
|-|-|
|DXGI_ERROR_INVALID_CALL|Le type de propriété spécifié dans la *propriété* n’est pas reconnu par ce système d’exploitation. Appelez [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) pour confirmer que le type de propriété est disponible pour cet adaptateur et le système d’exploitation.|
|DXGI_ERROR_UNSUPPORTED|Le type de propriété spécifié dans la *propriété* n’est pas pris en charge par l’adaptateur. Appelez [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) pour confirmer que le type de propriété est disponible pour cet adaptateur et le système d’exploitation.|
|E_POINTER|`nullptr` a été fourni pour *bufferSize*.|

## <a name="remarks"></a>Notes

Vous pouvez appeler **GetPropertySize** sur un adaptateur qui n’est plus valide &mdash; . la fonction ne peut pas échouer.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)