---
title: MrmCreateResourceFileInMemory, fonction (MrmResourceIndexer. h)
description: Crée des informations PRI en tant qu’objet BLOB en mémoire, et non en tant que fichier sur le disque.
ms.assetid: 68BDAD27-545A-4DC6-B909-4242A0863690
keywords:
- Menus de fonction MrmCreateResourceFileInMemory et autres ressources
topic_type:
- apiref
api_name:
- MrmCreateResourceFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17bbe36a55b5be18f9f4005b4e0ae24d3d610bd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466598"
---
# <a name="mrmcreateresourcefileinmemory-function"></a>MrmCreateResourceFileInMemory fonction)

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Crée des informations PRI en tant qu’objet BLOB en mémoire, et non en tant que fichier sur le disque. La fonction alloue de la mémoire et retourne un pointeur vers cette mémoire dans *outputPriData*. Appelez [**MrmFreeMemory**](mrmfreememory.md) avec le même pointeur pour libérer de la mémoire. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT HRESULT MrmCreateResourceFileInMemory(
  _In_  MrmResourceIndexerHandle indexer,
  _In_  MrmPackagingMode         packagingMode,
  _In_  MrmPackagingOptions      packagingOptions,
  _Out_ BYTE                     **outputPriData,
  _Out_ ULONG                    *outputPriSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*indexeur* \[ dans\]
</dt> <dd>

Type : **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Handle identifiant l’indexeur de ressource à partir duquel créer les informations PRI.

</dd> <dt>

*packagingMode* \[ dans\]
</dt> <dd>

Type : **[ **MrmPackagingMode**](mrmpackagingmode.md)**

Spécifie si les informations PRI doivent être autonomes ou être un pack de ressources. **MrmPackagingModeAutoSplit** n’est pas pris en charge.

</dd> <dt>

*packagingOptions* \[ dans\]
</dt> <dd>

Type : **[ **MrmPackagingOptions**](mrmpackagingoptions.md)**

Spécifie des options supplémentaires sur les informations PRI.

</dd> <dt>

*outputPriData* \[ à\]
</dt> <dd>

Type : **Byte \* \***

Adresse d’un pointeur vers l’octet. La fonction alloue de la mémoire et retourne un pointeur vers cette mémoire dans *outputPriData*. Appelez [**MrmFreeMemory**](mrmfreememory.md) avec votre pointeur vers Byte pour libérer cette mémoire.

</dd> <dt>

*outputPriSize* \[ à\]
</dt> <dd>

Type : **ULong \** _

Adresse d’un ULONG. Dans _outputPriSize *, la fonction retourne la taille de la mémoire allouée appelée par *outputPriData*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

\_OK si la fonction a réussi, sinon une autre valeur. Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.

## <a name="remarks"></a>Notes

Si vous transmettez *outputPriData* à [**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md), ne libérez pas la mémoire tant que vous n’avez pas fini d’utiliser l’indexeur de ressource.

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

 

