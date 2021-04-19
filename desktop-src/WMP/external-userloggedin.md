---
title: External. userLoggedIn
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. userLoggedIn
ms.assetid: d02d9486-c692-4f46-bc29-f0aaa45cad0f
keywords:
- External. userLoggedIn Windows Media Player
topic_type:
- apiref
api_name:
- External.userLoggedIn
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5454dd9d2fa2d771005448a4157c33b5634a30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532645"
---
# <a name="externaluserloggedin"></a>External. userLoggedIn

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La propriété **userLoggedIn** récupère une valeur indiquant si l’utilisateur est connecté au magasin en ligne.

## <a name="syntax"></a>Syntaxe

``` syntax
window.external.userLoggedIn
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **valeur booléenne** en lecture seule. La **valeur true** indique que l’utilisateur est connecté, et **false** indique que l’utilisateur a ouvert une session.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. attemptLogin**](external-attemptlogin.md)
</dt> <dt>

[**External. OnLoginChange, événement**](external-onloginchange-event.md)
</dt> </dl>

 

 





