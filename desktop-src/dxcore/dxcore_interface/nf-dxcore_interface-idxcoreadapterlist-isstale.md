---
title: IDXCoreAdapterList::IsStale
description: Détermine si les modifications apportées à ce système ont entraîné la mise à jour de cet objet de liste d’adaptateurs DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: a40a590a76773592d5442993c75149b2349880f7681d625e777d363062f5c4be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118502570"
---
# <a name="idxcoreadapterlistisstale-method"></a>IDXCoreAdapterList :: IsStale, méthode

Détermine si les modifications apportées à ce système ont entraîné la mise à jour de cet objet de liste d’adaptateurs DXCore. Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Syntaxe

```cpp
virtual bool STDMETHODCALLTYPE IsStale() = 0;
```

## <a name="returns"></a>Retours

Type : **bool**

Retourne `true` si, depuis la génération de la liste, des modifications ont été apportées aux conditions du système, ce qui entraînerait l’obsolescence de cette liste d’adaptateurs. Sinon, retourne `false`.

## <a name="remarks"></a>Remarques

Vous pouvez interroger **IsStale** pour déterminer si la modification des conditions système a entraîné la mise à jour de cette liste. Si **IsStale** retourne `true` une seule fois, il retourne `true` pour la durée de vie restante de l’objet de liste d’adaptateurs dxcore. Un objet de liste périmé est toujours considéré comme obsolète même si les conditions système retournent à un état correspondant à la liste (les mêmes conditions s’obtiennent maintenant que lors de la première génération de la liste).

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)