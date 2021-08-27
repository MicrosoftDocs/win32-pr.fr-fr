---
title: Méthode IGatherNotify paramètre addscope (déconseillée)
description: cette rubrique Windows Desktop search interface est déconseillée et remplacée par l’API ISearchPersistentItemsChangedSink de recherche Windows dans le SDK Windows. | Méthode IGatherNotify paramètre addscope (déconseillée)
ms.assetid: 3b250818-1876-40b2-9a85-91f2bf6f52ec
keywords:
- paramètre addscope (déprécié) méthode héritée des fonctionnalités d’environnement Windows
- paramètre addscope (déprécié) méthode héritée Windows fonctionnalités d’environnement, interface IGatherNotify
- fonctionnalités d’environnement Windows héritées de l’interface IGatherNotify, méthode paramètre addscope (déconseillée)
topic_type:
- apiref
api_name:
- IGatherNotify.AddScope (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a49c0cf652b0cfde59167fa98498a978d3c2c41d3a886ee092b8f4a28d35f61b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118755590"
---
# <a name="igathernotifyaddscope-deprecated-method"></a>IGatherNotify :: paramètre addscope (méthode déconseillée)

\[Les **paramètre addscope** peuvent être modifiés ou non disponibles dans les versions ultérieures du système d’exploitation ou du produit.\]

cette rubrique Windows Desktop search interface est déconseillée et remplacée par l’API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de recherche Windows dans le SDK Windows.

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

## <a name="remarks"></a>Remarques

L’appel de cette méthode démarre une analyse incrémentielle lorsqu’elle est connectée au magasin. Par la suite, il est supposé que toutes les modifications d’URL sont effectuées par notification après la mise à jour initiale.

 

 
