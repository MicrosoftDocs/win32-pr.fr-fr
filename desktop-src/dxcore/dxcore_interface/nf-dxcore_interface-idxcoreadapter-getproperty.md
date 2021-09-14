---
title: IDXCoreAdapter::GetProperty
description: Récupère la valeur de la propriété de l’adaptateur spécifiée.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: c8a7f7b36fdb0128b4047335051823da07a074c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918047"
---
# <a name="idxcoreadaptergetproperty-method"></a>IDXCoreAdapter :: GetProperty, méthode

Récupère la valeur de la propriété de l’adaptateur spécifiée. Avant d’appeler **GetProperty** pour un type de propriété, appelez [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) pour confirmer que le type de propriété est disponible pour cet adaptateur et le système d’exploitation. De même, avant d’appeler **GetProperty**, appelez [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) pour déterminer la taille nécessaire de la mémoire tampon dans laquelle la valeur de propriété doit être reçue.

## <a name="syntax"></a>Syntaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE GetProperty(
  DXCoreAdapterProperty property,
  size_t bufferSize,
  _Out_writes_bytes_(bufferSize) void *propertyData) = 0;

template <class T>
HRESULT GetProperty( 
  DXCoreAdapterProperty property,
  _Out_writes_bytes_(sizeof(T)) T *propertyData);
```

## <a name="parameters"></a>Paramètres

### <a name="property"></a>propriété

Type : **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Type de la propriété dont vous souhaitez récupérer la valeur. Consultez le tableau dans [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) pour plus d’informations sur chaque propriété de l’adaptateur.

### <a name="buffersize"></a>Tampon

Type : **size_t**

Taille, en octets, de la mémoire tampon de sortie que vous allouez et fournissez dans *PropertyData*.

### <a name="propertydata-out"></a>propertyData [out]

Type : **void \***

Pointeur vers une mémoire tampon de sortie que vous allouez dans votre application, et que la fonction remplit. Appelez [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) pour déterminer la taille de la mémoire tampon *PropertyData* pour une propriété d’adaptateur donnée.

## <a name="returns"></a>Retours

Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.

|Valeur de retour|Description|
|-|-|
|DXGI_ERROR_INVALID_CALL|Le type de propriété spécifié dans la *propriété* n’est pas reconnu par ce système d’exploitation. Appelez [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) pour confirmer que le type de propriété est disponible pour cet adaptateur et le système d’exploitation.|
|DXGI_ERROR_UNSUPPORTED|Le type de propriété spécifié dans la *propriété* n’est pas pris en charge par l’adaptateur. Appelez [IsPropertySupported](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) pour confirmer que le type de propriété est disponible pour cet adaptateur et le système d’exploitation.|
|E_INVALIDARG|Une taille de mémoire tampon insuffisante est fournie dans *PropertyData*. Appelez [GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) pour déterminer la taille de la mémoire tampon *PropertyData* pour une propriété d’adaptateur donnée.|
|E_POINTER|`nullptr` a été fourni pour *PropertyData*.|

## <a name="remarks"></a>Notes

Vous pouvez appeler **GetProperty** sur un adaptateur qui n’est plus valide &mdash; . la fonction n’échouera pas à la suite de cela. Cette fonction met à zéro la mémoire tampon *PropertyData* avant de la remplir.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)