---
title: Méthode IGatherNotify paramètre addscope (déconseillée)
description: Cette rubrique de l’interface de recherche Windows Desktop est déconseillée et remplacée par l’API ISearchPersistentItemsChangedSink de recherche Windows dans le SDK Windows. | Méthode IGatherNotify paramètre addscope (déconseillée)
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- Méthode paramètre addscope (déconseillée) fonctionnalités héritées de l’environnement Windows
- Méthode paramètre addscope (déconseillée) fonctionnalités d’environnement Windows héritées, interface IGatherNotify
- Interface IGatherNotify fonctionnalités d’environnement Windows héritées, méthode paramètre addscope (déconseillée)
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 967dc4f30acee2f8d8adbcfec04f0508e53bba15
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322181"
---
# <a name="igathernotifyaddscope-deprecated-method"></a>IGatherNotify :: paramètre addscope (méthode déconseillée)

\[Les **paramètre addscope** peuvent être modifiés ou non disponibles dans les versions ultérieures du système d’exploitation ou du produit.\]

Cette rubrique de l’interface de recherche Windows Desktop est déconseillée et remplacée par l’API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de recherche Windows dans le SDK Windows.

Ajoute la page de démarrage ou l’URL que vous analysez. Cela lance une analyse incrémentielle lorsque vous vous connectez, puis suppose que toutes les autres modifications d’URL sont effectuées par notification.

## <a name="syntax"></a>Syntaxe


```C++
void AddScope (Deprecated)(
  [in] BSTR bstrScope
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrScope* \[ dans\]
</dt> <dd>

Type : **BSTR**

Chaîne qui spécifie la page de démarrage ou URLthat que vous analysez.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

L’appel de cette méthode démarre une analyse incrémentielle lorsqu’elle est connectée au magasin. Par la suite, il est supposé que toutes les modifications d’URL sont effectuées par notification après la mise à jour initiale.

 

 
