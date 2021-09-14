---
title: MrmCreateResourceIndexer, fonction (MrmResourceIndexer. h)
description: Crée un indexeur de ressource, utilisé pour générer des fichiers PRI (package Resource index) pour une application UWP. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: 9AE3EF90-4ADC-4646-9C62-87A702333B9A
keywords:
- Menus de fonction MrmCreateResourceIndexer et autres ressources
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexer
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5240112c3fef6e358cfbc90638ef867108aabeb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235685"
---
# <a name="mrmcreateresourceindexer-function"></a>MrmCreateResourceIndexer fonction)

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

Crée un indexeur de ressource, utilisé pour générer des fichiers PRI (package Resource index) pour une application UWP. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT HRESULT MrmCreateResourceIndexer(
  _In_     PCWSTR                   packageFamilyName,
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*packageFamilyName* \[ dans\]
</dt> <dd>

Type : **PCWSTR**

Nom de la famille de packages de l’application UWP pour laquelle vous allez générer des fichiers PRI. Cette valeur sera utilisée comme nom de mappage de ressources lorsque vous générerez ultérieurement un fichier PRI à partir de cet indexeur de ressource.

</dd> <dt>

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

*indexeur* \[ in, out\]
</dt> <dd>

Type : **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\***

Pointeur vers un handle d’indexeur de ressource.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

\_OK si la fonction a réussi, sinon une autre valeur. Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.

## <a name="requirements"></a>Spécifications



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

 

