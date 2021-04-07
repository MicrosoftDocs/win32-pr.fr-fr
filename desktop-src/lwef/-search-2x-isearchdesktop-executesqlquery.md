---
title: Méthode ISearchDesktop ExecuteSQLQuery
description: Prend un pointeur vers une chaîne qui contient une requête langage SQL (SQL) et ses attributs, et retourne un pointeur vers le jeu retourné.
ms.assetid: df3f473b-0bee-4035-abf8-dbe5249ef0ed
keywords:
- Méthode ExecuteSQLQuery fonctionnalités d’environnement Windows héritées
- Méthode ExecuteSQLQuery fonctionnalités d’environnement Windows héritées, interface ISearchDesktop
- Fonctionnalités d’environnement Windows héritées de l’interface ISearchDesktop, méthode ExecuteSQLQuery
topic_type:
- apiref
api_name:
- ISearchDesktop.ExecuteSQLQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0b13ff361d07f99efe1366e2201d610eac10523
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2020
ms.locfileid: "103724010"
---
# <a name="isearchdesktopexecutesqlquery-method"></a>ISearchDesktop :: ExecuteSQLQuery, méthode

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. Dans les versions ultérieures, utilisez plutôt l' [API Windows Search](../search/-search-reference-entry-page.md) . 

Prend un pointeur vers une chaîne qui contient une requête langage SQL (SQL) et ses attributs, et retourne un pointeur vers le jeu retourné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pdwAttributes* \[ dans\]
</dt> <dd>

Type : **LPCWSTR \***

Chaîne qui contient les autres attributs de la requête.

</dd> <dt>

*pwszURL* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Chaîne qui contient la requête SQL.

</dd> <dt>

*ppidUrl* \[ à\]
</dt> <dd>

Type : **ppidUrl \***

Lorsque cette méthode est retournée avec succès, contient un pointeur vers le Recordset retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

 

 




