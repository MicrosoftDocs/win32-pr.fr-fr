---
title: MrmCreateResourceFile, fonction (MrmResourceIndexer. h)
description: Crée un fichier PRI (nommé \ 0034 ; Resources. pri \ 0034 ;), ou des fichiers, sur le disque dans le dossier spécifié. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: B9CE0638-4650-4E1A-BE5E-4CC7C6614030
keywords:
- Menus de fonction MrmCreateResourceFile et autres ressources
topic_type:
- apiref
api_name:
- MrmCreateResourceFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f58cd2ca366e2eeb4c594df986016d29c9aafbee0fa3310beded7a0b9bb12ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687332"
---
# <a name="mrmcreateresourcefile-function"></a>MrmCreateResourceFile fonction)

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

Crée un fichier PRI (nommé « Resources. PRI ») ou des fichiers sur le disque dans le dossier spécifié. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT HRESULT MrmCreateResourceFile(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ MrmPackagingMode         packagingMode,
  _In_ MrmPackagingOptions      packagingOptions,
       PCWSTR                   outputDirectory
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*indexeur* \[ dans\]
</dt> <dd>

Type : **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Handle identifiant l’indexeur de ressource à partir duquel créer le fichier PRI.

</dd> <dt>

*packagingMode* \[ dans\]
</dt> <dd>

Type : **[ **MrmPackagingMode**](mrmpackagingmode.md)**

Spécifie si le fichier PRI doit être autonome, être fractionné automatiquement par qualificateur de ressource ou être un pack de ressources.

</dd> <dt>

*packagingOptions* \[ dans\]
</dt> <dd>

Type : **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**

Spécifie des options supplémentaires sur le fichier PRI.

</dd> <dt>

*outputDirectory* 
</dt> <dd>

Type : **PCWSTR**

Chemin d’accès à un dossier dans lequel enregistrer le fichier PRI.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

\_OK si la fonction a réussi, sinon une autre valeur. Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.

## <a name="requirements"></a>Conditions requises



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

 

