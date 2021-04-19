---
title: IGatherNotify OnDataChange (déprécié), méthode
description: Cette rubrique de l’interface de recherche Windows Desktop est déconseillée et remplacée par l’API ISearchPersistentItemsChangedSink de recherche Windows dans le SDK Windows. | IGatherNotify OnDataChange (déprécié), méthode
ms.assetid: 0cbfa6b7-44f0-41f0-93a3-d5941b5822de
keywords:
- Méthode OnDataChange (déconseillée) fonctionnalités héritées de l’environnement Windows
- OnDataChange (déprécié), méthode fonctionnalités d’environnement Windows héritées, interface IGatherNotify
- Interface IGatherNotify fonctionnalités d’environnement Windows héritées, méthode OnDataChange (déconseillée)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataChange (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d41edeaa591a7f3cbc9494064906af1815597737
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106532396"
---
# <a name="igathernotifyondatachange-deprecated-method"></a>IGatherNotify :: OnDataChange (déconseillé), méthode

\[**OnDataChange** peut être modifié ou non disponible dans les versions ultérieures du système d’exploitation ou du produit.\]

Cette rubrique de l’interface de recherche Windows Desktop est déconseillée et remplacée par l’API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de recherche Windows dans le SDK Windows.

Cette méthode avertit l’indexeur des données qui ont changé. Lorsqu’il envoie la notification à l’indexeur, il comprend le type de modification, l’adresse physique et l’adresse logique.

## <a name="syntax"></a>Syntaxe


```C++
void OnDataChange (Deprecated)(
  [in] long eChangeAdvise,
  [in] BSTR bstrPhysicalAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*eChangeAdvise* \[ dans\]
</dt> <dd>

Type : **long**

Valeur énumérée qui spécifie le type de modification.

</dd> <dt>

*bstrPhysicalAddress* \[ dans\]
</dt> <dd>

Type : **BSTR**

Adresse physique de l’élément qui a changé.

</dd> <dt>

*bstrLogicalAddress* \[ dans\]
</dt> <dd>

Type : **BSTR**

Adresse logique de l’élément qui a changé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

 

 
