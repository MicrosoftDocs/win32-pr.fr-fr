---
title: Méthode IGatherNotify OnDataMove (déconseillée)
description: Cette rubrique de l’interface de recherche Windows Desktop est déconseillée et remplacée par l’API ISearchPersistentItemsChangedSink de recherche Windows dans le SDK Windows. | Méthode IGatherNotify OnDataMove (déconseillée)
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- Méthode OnDataMove (déconseillée) fonctionnalités héritées de l’environnement Windows
- Méthode OnDataMove (déconseillée) fonctionnalités d’environnement Windows héritées, interface IGatherNotify
- Interface IGatherNotify fonctionnalités d’environnement Windows héritées, méthode OnDataMove (déconseillée)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9fe38cd11e9072981334e5b724445ea3393d4361
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322178"
---
# <a name="igathernotifyondatamove-deprecated-method"></a>IGatherNotify :: OnDataMove (méthode déconseillée)

\[Les **OnDataMove** peuvent être modifiés ou non disponibles dans les versions ultérieures du système d’exploitation ou du produit.\]

Cette rubrique de l’interface de recherche Windows Desktop est déconseillée et remplacée par l’API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de recherche Windows dans le SDK Windows.

Cette méthode avertit l’indexeur des données qui ont été déplacées. Lorsqu’il envoie la notification à l’indexeur, il comprend l’ancienne adresse, la nouvelle adresse et l’adresse logique.

## <a name="syntax"></a>Syntaxe


```C++
void OnDataMove (Deprecated)(
  [in] long eChangeAdviseSemantics,
  [in] BSTR bstrOldAddress,
  [in] BSTR bstrNewAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*eChangeAdviseSemantics* \[ dans\]
</dt> <dd>

Type : **long**

Paramètre énuméré qui décrit le type de déplacement qui s’est produit.

</dd> <dt>

*bstrOldAddress* \[ dans\]
</dt> <dd>

Type : **BSTR**

Ancienne adresse de l’élément qui a été déplacé. Pour les fichiers normaux,*eChangeAdviseSematics* a la **valeur null**. Dans le cas d’un dossier ou d’un répertoire, définissez *eChangeAdviseSematics* sur le \_ répertoire sémantique d’autorité de certification GTHR \_ \_ .

</dd> <dt>

*bstrNewAddress* \[ dans\]
</dt> <dd>

Type : **BSTR**

Nouvelle adresse de l’élément qui a été déplacé.

</dd> <dt>

*bstrLogicalAddress* \[ dans\]
</dt> <dd>

Type : **BSTR**

Adresse logique de l’élément qui a été déplacé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

 

 
