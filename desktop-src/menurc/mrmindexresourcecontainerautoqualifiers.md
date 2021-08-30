---
title: MrmIndexResourceContainerAutoQualifiers, fonction (MrmResourceIndexer. h)
description: Indexe les ressources de type chaîne contenues dans un fichier de ressources (. resw/. resjson), ou. priinfo ou. prifile, appartenant à une application UWP.
ms.assetid: 7FCAA2B5-FF45-4961-84BA-B444B550C91D
keywords:
- Menus de fonction MrmIndexResourceContainerAutoQualifiers et autres ressources
topic_type:
- apiref
api_name:
- MrmIndexResourceContainerAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a05e05b9bbc6919d56760bec82e40989fac3a31bc57ad43712ccfddda3024e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952353"
---
# <a name="mrmindexresourcecontainerautoqualifiers-function"></a>MrmIndexResourceContainerAutoQualifiers fonction)

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

Indexe les ressources de type chaîne contenues dans un fichier de ressources (. resw/. resjson), ou. priinfo ou. prifile, appartenant à une application UWP. Déduit une liste de qualificateurs de ressources à partir du paramètre *containerPath* . Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT HRESULT MrmIndexResourceContainerAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   containerPath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*indexeur* \[ dans\]
</dt> <dd>

Type : **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Handle identifiant l’indexeur de ressource qui indexera les ressources de type chaîne.

</dd> <dt>

*containerPath* \[ dans\]
</dt> <dd>

Type : **PCWSTR**

Chemin d’accès relatif à un. resw,. resjson,. priinfo ou. prifile contenant les ressources de type chaîne que vous souhaitez indexer. Ce chemin d’accès est relatif à la racine du projet de l’application UWP pour laquelle vous générez des fichiers PRI. La racine du projet est la valeur de *projectRoot* que vous avez passée à [**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

\_OK si la fonction a réussi, sinon une autre valeur. Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.

## <a name="remarks"></a>Remarques

Les qualificateurs de ressources sont déduits à partir de *containerPath*. Par exemple, la valeur L "en-US \\ \\ Resources. resw" ajoute des ressources de type chaîne avec le qualificateur "language-fr-US".

Le nom du fichier de ressources sera utilisé comme nom de sous-arborescence de mappage des ressources pour ces ressources lorsque vous générerez ultérieurement un fichier PRI à partir de cet indexeur de ressource.

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

 

