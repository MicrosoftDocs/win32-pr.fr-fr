---
description: crée un catalogue personnalisé dans le Windows indexeur de recherche et retourne une référence à celui-ci.
ms.assetid: 2ADC48B8-87A2-4527-9AA8-9B0BA3A12462
title: 'ISearchManager2 :: CreateCatalog, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchManager2.CreateCatalog
api_type:
- COM
api_location:
- searchapi.h
ms.openlocfilehash: 34a4ceb37045ebbae62e04da0b5395673ed498c56189a26f2abaa376c960c511
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119597749"
---
# <a name="isearchmanager2createcatalog-method"></a>ISearchManager2 :: CreateCatalog, méthode

crée un catalogue personnalisé dans le Windows indexeur de recherche et retourne une référence à celui-ci.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateCatalog(
  [in]  LPCWSTR               pszCatalog,
  [out] ISearchCatalogManager **ppCatalogManager
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszCatalog* \[ dans\]
</dt> <dd>

Type : **[ **LPCWSTR**](../winprog/windows-data-types.md)**

Nom du catalogue à créer. Peut être n’importe quel nom sélectionné par l’appelant, ne doit contenir que des caractères alphanumériques standard et des traits de soulignement.

</dd> <dt>

*ppCatalogManager* \[ à\]
</dt> <dd>

Type : **[ **ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)\*\***

En cas de réussite, une référence au catalogue créé est retournée en tant que pointeur d’interface [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) . La mise en sortie () doit être appelée sur cette interface une fois que l’application appelante a fini de l’utiliser.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

HRESULT indiquant l’état de l’opération :



| Code de retour                                                                             | Description                                                                                 |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>    | Le catalogue n’existait pas déjà et a été créé. Référence au catalogue renvoyé.<br/> |
| <dl> <dt>**S \_ false**</dt> </dl> | Le catalogue existait précédemment, la référence au catalogue a été retournée.<br/>                       |



 

ÉCHEC de HRESULT : échec de la création du catalogue ou des arguments non valides passés.

## <a name="remarks"></a>Remarques

appelé pour créer un nouveau catalogue dans le Windows indexeur de recherche. Après la création, les méthodes sur le gestionnaire de [**ISearchCatalog**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) retourné peuvent être utilisées pour ajouter des emplacements à indexer, surveiller le processus d’indexation et construire des requêtes à envoyer à l’indexeur et obtenir des résultats. Pour plus d’informations, consultez la documentation relative à la gestion de l’index : https://msdn.microsoft.com/library/bb266516(VS.85).aspx

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>           |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISearchManager2**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager2)
</dt> </dl>

 

 
