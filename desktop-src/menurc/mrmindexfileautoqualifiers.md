---
title: MrmIndexFileAutoQualifiers, fonction (MrmResourceIndexer. h)
description: Indexe un fichier de ressources appartenant à une application UWP. Déduit une liste de qualificateurs de ressources à partir du paramètre filePath. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: CEA4D845-987C-48D6-B80E-9F055363FFE0
keywords:
- Menus de fonction MrmIndexFileAutoQualifiers et autres ressources
topic_type:
- apiref
api_name:
- MrmIndexFileAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a10dbdb564f7e2d830d1edea59be6ca6f11b72d2650a937f96b6d305b6c7f61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886729"
---
# <a name="mrmindexfileautoqualifiers-function"></a>MrmIndexFileAutoQualifiers fonction)

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

Indexe un fichier de ressources appartenant à une application UWP. Déduit une liste de qualificateurs de ressources à partir du paramètre *filePath* . Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT HRESULT MrmIndexFileAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   filePath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*indexeur* \[ dans\]
</dt> <dd>

Type : **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Handle identifiant l’indexeur de ressource qui indexe le fichier de ressources.

</dd> <dt>

*filePath* \[ dans\]
</dt> <dd>

Type : **PCWSTR**

Chemin d’accès relatif à un fichier contenant une ressource que vous souhaitez indexer. Ce chemin d’accès est relatif à la racine du projet de l’application UWP pour laquelle vous générez des fichiers PRI. La racine du projet est la valeur de *projectRoot* que vous avez passée à [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

\_OK si la fonction a réussi, sinon une autre valeur. Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.

## <a name="remarks"></a>Remarques

Le segment de nom de fichier de *filePath* est utilisé comme nom de ressource ; les qualificateurs de ressources et sont dérivés de son chemin d’accès. Par exemple, si vous transmettez L "images \\ de-- \\ scale-100 \\background.png" vers *filePath* , l’indexeur de ressource ajoute une ressource nommée "background.png" avec des qualificateurs de ressources "Language-out" et "Scale-100".

L "fichiers" sera utilisé comme nom de sous-arborescence de mappage des ressources pour cette ressource lorsque vous générerez ultérieurement un fichier PRI à partir de cet indexeur de ressource.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1803 \[ uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows \[Applications de bureau serveur uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Mrmsupport. lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

