---
title: MrmCreateResourceIndexerFromPreviousPriFile, fonction (MrmResourceIndexer. h)
description: Crée un indexeur de ressource à partir d’un fichier PRI créé à l’aide d’un appel précédent à MrmCreateResourceFile. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez API PRI (package Resource Indexing) et systèmes de génération personnalisés.
ms.assetid: 8B3743EF-1A27-4B70-9577-8549B91DBC1E
keywords:
- Menus de fonction MrmCreateResourceIndexerFromPreviousPriFile et autres ressources
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be08170dc8ae25db34492273e7c612352d5e0530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510329"
---
# <a name="mrmcreateresourceindexerfrompreviousprifile-function"></a>MrmCreateResourceIndexerFromPreviousPriFile fonction)

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Crée un indexeur de ressource à partir d’un fichier PRI créé à l’aide d’un appel précédent à [**MrmCreateResourceFile**](mrmcreateresourcefile.md). Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousPriFile(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     PCWSTR                   priFile,
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

*priFile* \[ dans\]
</dt> <dd>

Type : **PCWSTR**

Chemin d’accès complet à un fichier PRI.

</dd> <dt>

*indexeur* \[ in, out\]
</dt> <dd>

Tapez : **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _

Pointeur vers un handle d’indexeur de ressource.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

\_OK si la fonction a réussi, sinon une autre valeur. Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1803 \[ uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de \[ Bureau Windows Server uniquement\]<br/>                                                 |
| En-tête<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Mrmsupport. lib</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[API d’indexation de ressources de package (IRP) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

