---
title: MrmCreateResourceIndexerFromPreviousPriData, fonction (MrmResourceIndexer. h)
description: Crée un indexeur de ressource à partir de données PRI créées par un appel précédent à MrmCreateResourceFileInMemory. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: 945ED98C-8D73-404F-ACE3-7DD314FB405A
keywords:
- Menus de fonction MrmCreateResourceIndexerFromPreviousPriData et autres ressources
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousPriData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d178532a77e01bc724276b40881685e0ec44d5364617fd856ffc55acfd99cf98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952351"
---
# <a name="mrmcreateresourceindexerfrompreviouspridata-function"></a>MrmCreateResourceIndexerFromPreviousPriData fonction)

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

Crée un indexeur de ressource à partir de données PRI créées par un appel précédent à [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md). Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousPriData (
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *priData,
  _In_     ULONG                    priSize,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*projectRoot* \[ dans\]
</dt> <dd>

Type : **PCWSTR**

Racine du projet de l’application UWP pour laquelle vous allez générer des fichiers PRI. En d’autres termes, le chemin d’accès aux fichiers de ressources de cette application. Vous le spécifiez afin que vous puissiez ensuite spécifier des chemins relatifs à cette racine dans les appels d’API suivants vers le même indexeur de ressource.

</dd> <dt>

*platformVersion* \[ dans\]
</dt> <dd>

Type : **[ **MrmPlatformVersion**](mrmplatformversion.md)**

Version de la plateforme cible pour l’indexeur de ressource.

</dd> <dt>

*defaultQualifiers* \[ dans, facultatif\]
</dt> <dd>

Type : **PCWSTR**

Liste des qualificateurs de ressources par défaut. Par exemple, L « language-en-US \_ Scale-100 \_ Contrast-standard »

</dd> <dt>

*priData* \[ dans\]
</dt> <dd>

Type : **Byte \***

Pointeur vers les données PRI créées par un appel précédent à [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md). Ne libérez pas *priData* tant que vous n’avez pas fini d’utiliser l’indexeur de ressource créé par cette fonction.

</dd> <dt>

Pris en  \[ dans\]
</dt> <dd>

Type : **ULong**

Taille des données vers lesquelles pointe *priData*.

</dd> <dt>

*indexeur* \[ in, out\]
</dt> <dd>

Type : **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\***

Pointeur vers un handle d’indexeur de ressource.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

\_OK si la fonction a réussi, sinon une autre valeur. Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.

## <a name="remarks"></a>Remarques

Ne libérez pas *priData* tant que vous n’avez pas fini d’utiliser l’indexeur de ressource créé par cette fonction.

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

 

