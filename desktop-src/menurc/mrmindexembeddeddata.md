---
title: MrmIndexEmbeddedData, fonction (MrmResourceIndexer. h)
description: Indexe une ressource données incorporée unique appartenant à une application UWP.
ms.assetid: 4DA37CF9-43B6-44EE-8A10-DBD4510D7885
keywords:
- Menus de fonction MrmIndexEmbeddedData et autres ressources
topic_type:
- apiref
api_name:
- MrmIndexEmbeddedData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 308d08e0e125e7919ad3eb32e6cba2184356fce5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513762"
---
# <a name="mrmindexembeddeddata-function"></a>MrmIndexEmbeddedData fonction)

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Indexe une ressource **données incorporée** unique appartenant à une application UWP. Prend une liste explicite (mais facultative) des qualificateurs de ressources. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT HRESULT MrmIndexEmbeddedData(
  _In_           MrmResourceIndexerHandle indexer,
  _In_           PCWSTR                   resourceUri,
  _In_     const BYTE                     *embeddedData,
  _In_           ULONG                    embeddedDataSize,
  _In_opt_       PCWSTR                   qualifiers
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*indexeur* \[ dans\]
</dt> <dd>

Type : **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Handle identifiant l’indexeur de ressource qui indexe le fichier de ressources.

</dd> <dt>

*resourceuri* \[ dans\]
</dt> <dd>

Type : **PCWSTR**

URI de ressource à assigner à la ressource. Le chemin d’accès sera utilisé comme nom de sous-arborescence de mappage des ressources pour cette ressource lorsque vous générerez ultérieurement un fichier PRI à partir de cet indexeur de ressource.

</dd> <dt>

*données incorporée* \[ dans\]
</dt> <dd>

Type : **const Byte \** _

Pointeur vers les données de la ressource que vous souhaitez indexer.

</dd> <dt>

_embeddedDataSize * \[ dans\]
</dt> <dd>

Type : **ULong**

Taille des données vers lesquelles pointe *données incorporée*.

</dd> <dt>

*qualificateurs* \[ dans, facultatif\]
</dt> <dd>

Type : **PCWSTR**

Liste facultative de qualificateurs de ressources, par exemple L « language-en-US \_ Scale-100 \_ Contrast-standard ». Une chaîne vide ou **nullptr** indique une ressource neutre. Les qualificateurs de ressources ne sont *pas* déduits de *resourceuri*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

\_OK si la fonction a réussi, sinon une autre valeur. Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.

## <a name="remarks"></a>Notes

Si vous souhaitez spécifier des qualificateurs de ressources, transmettez-les dans le paramètre *Qualifiers* . Les qualificateurs de ressources ne sont *pas* déduits de *resourceuri*.

Le segment de nom de fichier de *resourceuri* est utilisé comme nom de ressource.

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

 

