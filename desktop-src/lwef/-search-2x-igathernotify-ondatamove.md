---
title: Méthode IGatherNotify OnDataMove (déconseillée)
description: cette rubrique Windows Desktop search interface est déconseillée et remplacée par l’API ISearchPersistentItemsChangedSink de recherche Windows dans le SDK Windows. | Méthode IGatherNotify OnDataMove (déconseillée)
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- OnDataMove (déprécié) méthode héritée des fonctionnalités d’environnement Windows
- OnDataMove (déprécié) méthode héritée Windows fonctionnalités d’environnement, interface IGatherNotify
- fonctionnalités d’environnement Windows héritées de l’interface IGatherNotify, méthode OnDataMove (déconseillée)
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f3d4f7d91bc9e9741f227812997a820ab4180ccf438d52ae8cfea93f67dc0bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665869"
---
# <a name="igathernotifyondatamove-deprecated-method"></a>IGatherNotify :: OnDataMove (méthode déconseillée)

\[Les **OnDataMove** peuvent être modifiés ou non disponibles dans les versions ultérieures du système d’exploitation ou du produit.\]

cette rubrique Windows Desktop search interface est déconseillée et remplacée par l’API [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) de recherche Windows dans le SDK Windows.

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

 

 
