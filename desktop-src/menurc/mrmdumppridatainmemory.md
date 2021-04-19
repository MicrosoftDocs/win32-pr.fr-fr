---
title: MrmDumpPriDataInMemory, fonction (MrmResourceIndexer. h)
description: Vide les informations PRI (en tant qu’objet BLOB en mémoire, créées par un appel précédent à MrmCreateResourceFileInMemory) dans son équivalent XML (en tant que données en mémoire), afin de le rendre plus facile à lire.
ms.assetid: 6E563B43-4E0A-465D-A8EA-7DE61738DE06
keywords:
- Menus de fonction MrmDumpPriDataInMemory et autres ressources
topic_type:
- apiref
api_name:
- MrmDumpPriDataInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072309dcf9ebda1ba4a5669034019582b99105f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510773"
---
# <a name="mrmdumppridatainmemory-function"></a>MrmDumpPriDataInMemory fonction)

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Vide les informations PRI (en tant qu’objet BLOB en mémoire, créées par un appel précédent à [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)) dans son équivalent XML (en tant que données en mémoire), afin de le rendre plus facile à lire. La fonction alloue de la mémoire et retourne un pointeur vers cette mémoire dans *outputXmlData*. Appelez [**MrmFreeMemory**](mrmfreememory.md) avec le même pointeur pour libérer de la mémoire. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT HRESULT MrmDumpPriDataInMemory(
  _In_     BYTE        *inputPriData,
  _In_     ULONG       inputPriSize,
  _In_opt_ BYTE        *schemaPriData,
  _In_     ULONG       schemaPriSize,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*inputPriData* \[ dans\]
</dt> <dd>

Type : **Byte \** _

Pointeur vers les données PRI créées par un appel précédent à [_ *MrmCreateResourceFileInMemory* *](mrmcreateresourcefileinmemory.md).

</dd> <dt>

*inputPriSize* \[ dans\]
</dt> <dd>

Type : **ULong**

Taille des données vers lesquelles pointe *inputPriData*.

</dd> <dt>

*schemaPriData* \[ dans, facultatif\]
</dt> <dd>

Type : **Byte \** _

Pointeur facultatif vers les informations PRI (en tant qu’objet BLOB en mémoire) représentant les données de schéma créées par un appel précédent à [_ *MrmCreateResourceFileInMemory* *](mrmcreateresourcefileinmemory.md). Ne libérez pas *schemaPriData* tant que vous n’avez pas fini d’utiliser l’indexeur de ressources. Consultez également la section Notes.

</dd> <dt>

*schemaPriSize* \[ dans\]
</dt> <dd>

Type : **ULong**

Taille des données vers lesquelles pointe *schemaPriData*.

</dd> <dt>

*dumpType* \[ dans\]
</dt> <dd>

Type : **[ **MrmDumpType**](mrmdumptype.md)**

Spécifie le degré de détail de la sauvegarde XML, ou si un schéma doit être vidé.

</dd> <dt>

*outputXmlData* \[ à\]
</dt> <dd>

Type : **Byte \* \***

Adresse d’un pointeur vers l’octet. La fonction alloue de la mémoire et retourne un pointeur vers cette mémoire dans *outputXmlData*. Appelez [**MrmFreeMemory**](mrmfreememory.md) avec votre pointeur vers Byte pour libérer cette mémoire.

</dd> <dt>

*outputXmlSize* \[ à\]
</dt> <dd>

Type : **ULong \** _

Adresse d’un ULONG. Dans _outputXmlSize *, la fonction retourne la taille de la mémoire allouée appelée par *outputXmlData*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

\_OK si la fonction a réussi, sinon une autre valeur. Utilisez les macros SUCCEEDED () ou FAILed () (définies dans Winerror. h) pour déterminer la réussite ou l’échec.

## <a name="remarks"></a>Notes

Un pack de ressources sans schéma est un pack créé avec l’argument [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) passé à [**MrmCreateResourceFile**](mrmcreateresourcefile.md) ou [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (ou avec le commutateur *omitSchemaFromResourcePacks* dans le fichier de configuration PRI). Pour vider un pack de ressources sans schéma, transmettez le chemin d’accès à vos données PRI de package principal en tant qu’argument pour le paramètre *schemaPriData* .

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

 

