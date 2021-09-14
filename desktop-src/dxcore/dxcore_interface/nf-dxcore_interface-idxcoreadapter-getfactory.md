---
title: IDXCoreAdapter::GetFactory
description: Récupère un pointeur d’interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) vers l’objet de fabrique d’adaptateur dxcore. | IDXCoreAdapter::GetFactory
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 1ac3e7fccd39b9b03ecb7016494a610519d26afa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918040"
---
# <a name="idxcoreadaptergetfactory-method"></a>IDXCoreAdapter :: GetFactory, méthode

Récupère un pointeur d’interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) vers l’objet de fabrique d’adaptateur dxcore. Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Syntaxe

```cpp
virtual HRESULT STDMETHODCALLTYPE GetFactory(
  REFIID riid,
  _COM_Outptr_ void** ppvFactory
) = 0;

template <class T>
HRESULT GetFactory(_COM_Outptr_ T** ppvFactory);
```

## <a name="parameters"></a>Paramètres

### <a name="riid"></a>riid

Type : **REFIID**

Référence à l’identificateur global unique (GUID) de l’interface que vous souhaitez retourner dans *ppvFactory*. Il doit s’agir de l’identificateur d’interface (IID) de [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md).

### <a name="ppvfactory-out"></a>ppvFactory [out]

Type : **void \* \***

Adresse d’un pointeur vers une interface avec l’IID spécifié dans le paramètre *riid* . Une fois le retour réussi, *\* ppvFactory* (l’adresse déréférencée) contient un pointeur vers l’objet de fabrique d’adaptateur dxcore existant. Avant de retourner, la fonction incrémente le décompte de références sur l’interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) de l’objet de fabrique.

## <a name="returns"></a>Retours

Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.

|Valeur de retour|Description|
|-|-|
|E_NOINTERFACE|Une valeur non valide a été fournie pour *riid*.|
|E_POINTER|`nullptr` a été fourni pour *ppvFactory*.|

## <a name="remarks"></a>Notes

Pour la durée pendant laquelle une référence existe sur une interface [IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md) , une interface [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) ou une interface [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) , les appels supplémentaires à [DXCoreCreateAdapterFactory](../dxcore/nf-dxcore-dxcorecreateadapterfactory.md), [IDXCoreAdapterList :: GetFactory](./nf-dxcore_interface-idxcoreadapterlist-getfactory.md)ou [IDXCoreAdapter :: GetFactory]() retournent des pointeurs vers le même objet, ce qui permet d’accroître le nombre de références de l’interface **IDXCoreAdapterFactory** .

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)
