---
title: Méthode ISearchDesktop ExecuteSQLQuery
description: prend un pointeur vers une chaîne qui contient une requête langage SQL (SQL) et ses attributs et retourne un pointeur vers le jeu retourné.
ms.assetid: df3f473b-0bee-4035-abf8-dbe5249ef0ed
keywords:
- fonctionnalités d’environnement Windows héritées de la méthode ExecuteSQLQuery
- méthode ExecuteSQLQuery héritage Windows fonctionnalités d’environnement, interface ISearchDesktop
- fonctionnalités d’environnement Windows héritées de l’interface ISearchDesktop, méthode ExecuteSQLQuery
topic_type:
- apiref
api_name:
- ISearchDesktop.ExecuteSQLQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec436a427958988e7605673b12b3fd8dc6fd3e1a54ab61cc5f542f0494c34923
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014289"
---
# <a name="isearchdesktopexecutesqlquery-method"></a>ISearchDesktop :: ExecuteSQLQuery, méthode

> [!NOTE]
> Windows Desktop Search 2. x est une technologie obsolète qui était à l’origine disponible en tant que complément pour Windows XP et Windows Server 2003. dans les versions ultérieures, utilisez plutôt l' [API de recherche Windows](../search/-search-reference-entry-page.md) . 

prend un pointeur vers une chaîne qui contient une requête langage SQL (SQL) et ses attributs et retourne un pointeur vers le jeu retourné.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
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

chaîne qui contient la requête SQL.

</dd> <dt>

*ppidUrl* \[ à\]
</dt> <dd>

Type : **ppidUrl \***

Lorsque cette méthode est retournée avec succès, contient un pointeur vers le Recordset retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

 

 




