---
title: DXCoreCreateAdapterFactory
description: Crée une fabrique d’adaptateur DXCore, que vous pouvez utiliser pour générer d’autres objets DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3f5164578da87af8f4d92c3bedcecb6f3dbaa95e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941244"
---
# <a name="dxcorecreateadapterfactory-function"></a>DXCoreCreateAdapterFactory fonction)

## <a name="description"></a>Description

Crée une fabrique d’adaptateur DXCore, que vous pouvez utiliser pour générer d’autres objets DXCore. Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).

## <a name="parameters"></a>Paramètres

### <a name="riid"></a>riid

Type : **REFIID**

Référence à l’identificateur global unique (GUID) de l’interface que vous souhaitez retourner dans *ppvFactory*. Il doit s’agir de l’identificateur d’interface (IID) de [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md).

### <a name="ppvfactory-out"></a>ppvFactory [out]

Type : **void \* \***

Adresse d’un pointeur vers une interface avec l’IID spécifié dans le paramètre *riid* . Une fois le retour réussi, *\* ppvFactory* (l’adresse déréférencée) contient un pointeur vers la fabrique dxcore créée.

## <a name="returns"></a>Retours

Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.

|Valeur retournée|Description|
|-|-|
|E_NOINTERFACE|Une valeur non valide a été fournie pour *riid*.|
|E_POINTER|`nullptr` a été fourni pour *ppvFactory*.|

## <a name="remarks"></a>Notes

Pour la durée pendant laquelle une référence existe sur une interface [IDXCoreAdapterFactory](../dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) , une interface [IDXCoreAdapterList](../dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) ou une interface [IDXCoreAdapter](../dxcore_interface/nn-dxcore_interface-idxcoreadapter.md) , les appels supplémentaires à **DXCoreCreateAdapterFactory**, [IDXCoreAdapterList :: GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getfactory.md)ou [IDXCoreAdapter :: GetFactory](../dxcore_interface/nf-dxcore_interface-idxcoreadapter-getfactory.md) retournent des pointeurs vers le même objet, ce qui permet d’accroître le nombre de références de l’interface **IDXCoreAdapterFactory** .

## <a name="see-also"></a>Voir aussi

[Référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)