---
description: Fournit l’accès au contexte d’un objet de magasin CAPICOM. Ce contexte permet d’utiliser le magasin de certificats CAPICOM dans d’autres dérivations de CryptoAPI.
ms.assetid: dc108e2d-d6ec-4972-9c8e-e6e738c25756
title: Interface ICertStore
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a48913b4bfb1fc28b612437a8f3b6934941c19b22683913f68d59f3f11d9e1c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005577"
---
# <a name="icertstore-interface"></a>Interface ICertStore

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP.\]

L’interface **ICertStore** fournit l’accès au contexte d’un objet de [**magasin**](store.md) CAPICOM. Ce contexte permet d’utiliser le magasin de certificats CAPICOM dans d’autres dérivations de CryptoAPI.

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez cette interface lorsque vous devez utiliser un objet de [**magasin**](store.md) CAPICOM dans une autre dérivation de CryptoAPI.

## <a name="members"></a>Membres

L’interface **ICertStore** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **ICertStore** possède ces méthodes.



| Méthode                                        | Description                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**CloseHandle**](icertstore-closehandle.md) | Ferme un handle HCERTSTORE acquis par le biais de la propriété [**StoreHandle**](icertstore-storehandle.md) .<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **ICertStore** possède les propriétés suivantes.



| Propriété                                                     | Type d’accès           | Description                                                                                                         |
|:-------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**StoreHandle**](icertstore-storehandle.md)<br/>     | Lecture/écriture<br/> | Définit ou récupère le handle HCERTSTORE d’un magasin de certificats.<br/>                                          |
| [**StoreLocation**](icertstore-storelocation.md)<br/> | Lecture/écriture<br/> | Définit ou récupère l' [**\_ \_ emplacement du magasin CAPICOM**](capicom-store-location.md) d’un magasin de certificats.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 




