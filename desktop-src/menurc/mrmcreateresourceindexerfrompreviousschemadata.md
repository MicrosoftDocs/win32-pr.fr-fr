---
title: MrmCreateResourceIndexerFromPreviousSchemaData, fonction (MrmResourceIndexer. h)
description: Crée un indexeur de ressource à partir de données de schéma en mémoire créées à l’aide d’un appel précédent à MrmDumpPriFileInMemory ou MrmDumpPriDataInMemory.
ms.assetid: D9C90C12-CEFE-4794-9553-8BFBE9E43D99
keywords:
- Menus de fonction MrmCreateResourceIndexerFromPreviousSchemaData et autres ressources
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 621500f8f35714daad0e259e6a718c25129987dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465599"
---
# <a name="mrmcreateresourceindexerfrompreviousschemadata-function"></a>MrmCreateResourceIndexerFromPreviousSchemaData fonction)

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Crée un indexeur de ressource à partir de données de schéma en mémoire créées à l’aide d’un appel précédent à [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) ou [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md). Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaData(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *schemaXmlData,
  _In_     ULONG                    schemaXmlSize,
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

*schemaXmlData* \[ dans\]
</dt> <dd>

Type : **Byte \** _

Pointeur vers les données de schéma créées par un appel précédent à [_ *MrmDumpPriFileInMemory* *](mrmdumpprifileinmemory.md) ou [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md). Ne libérez pas *schemaXmlData* tant que vous n’avez pas fini d’utiliser l’indexeur de ressource créé par cette fonction.

</dd> <dt>

*schemaXmlSize* \[ dans\]
</dt> <dd>

Type : **ULong**

Taille des données vers lesquelles pointe *schemaXmlData*.

</dd> <dt>

*indexeur* \[ in, out\]
</dt> <dd>

Tapez : **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _

Pointeur vers un handle d’indexeur de ressource.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

\_OK si la fonction a réussi, sinon une autre valeur. Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.

## <a name="remarks"></a>Notes

Ne libérez pas *schemaXmlData* tant que vous n’avez pas fini d’utiliser l’indexeur de ressource créé par cette fonction.

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

 

