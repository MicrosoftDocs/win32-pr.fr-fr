---
title: IDXCoreAdapterList::Sort
description: Trie un objet de liste d’adaptateurs DXCore en fonction d’un tableau d’entrée fourni de critères de tri.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 6260e700053a99b531a66a5c19e15d4a32f07e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102196"
---
# <a name="idxcoreadapterlistsort-method"></a>IDXCoreAdapterList :: sort, méthode

## <a name="description"></a>Description

Trie un objet de liste d’adaptateurs DXCore en fonction d’un tableau d’entrée de critères de tri fourni, où les éléments de tableau précédents dans le tableau de critères reçoivent une pondération plus élevée. Le **Tri** vous permet de trouver plus facilement votre adaptateur idéal dans une liste d’adaptateurs.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT Sort(
  uint32_t numPreferences,
  _In_reads_(numPreferences) const DXCoreAdapterPreference* preferences
);
```

## <a name="parameters"></a>Paramètres

### <a name="numpreferences"></a>numPreferences

Type : **uint32_t**

Nombre d’éléments dans le tableau vers lequel pointe le paramètre *Preferences* .

### <a name="preferences-in"></a>préférences [in]

Type : **const [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) \***

Pointeur vers un tableau de constantes de valeurs [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) représentant des critères de tri.

## <a name="returns"></a>Retours

Type : **[HRESULT](../../com/structure-of-com-error-codes.md)**

Si la fonction est réussie, elle retourne **S_OK**. Sinon, elle retourne un [](../../com/structure-of-com-error-codes.md) [code d’erreur](../../com/com-error-codes-10.md)HRESULT.

|Valeur retournée|Description|
|-|-|
|E_INVALIDARG|L’argument *numPreferences* est égal à zéro ou l’argument *Preferences* a la valeur `nullptr` .|

## <a name="remarks"></a>Notes

Dans les cas où une valeur [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) fournie n’est pas reconnue par le système d’exploitation, elle est ignorée et ne provoque pas l’échec de l’API. Dans ce cas, les valeurs **DXCoreAdapterPreference** connues seront toujours prises en compte. Pour déterminer si un type de tri est compris par l’API, appelez [IDXCoreAdapterList :: IsAdapterPreferenceSupported](./nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).

Les valeurs de **DXCoreAdapterPreference** qui se produisent plus tôt dans le tableau de *Préférences* fourni sont traitées avec une priorité plus élevée. 

Pour plus d’informations sur la logique appliquée à chaque type, reportez-vous à la documentation sur l’énumération **DXCoreAdapterPreference** . La logique interne d’un type peut se développer au fur et à mesure du développement du système d’exploitation.

Lorsque **sort** retourne, les éléments de la liste de l’adaptateur dxcore sont triés de la plus préférable à la moins préférable. Ainsi, l’appel de [IDXCoreAdapterList :: GetAdapter](./nf-dxcore_interface-idxcoreadapterlist-getadapter.md) avec l’index 0 récupère l’adaptateur qui correspond le mieux aux types de préférences de tri demandés ; l’index 1 est la meilleure correspondance la plus proche, et ainsi de suite.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)