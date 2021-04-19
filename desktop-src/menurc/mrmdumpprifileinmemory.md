---
title: MrmDumpPriFileInMemory, fonction (MrmResourceIndexer. h)
description: Fait un dump d’un fichier PRI (binaire) dans son équivalent XML (en tant que données en mémoire), afin de le rendre plus facile à lire.
ms.assetid: 04FD048F-1473-47B1-9CAB-03FEF98A9B48
keywords:
- Menus de fonction MrmDumpPriFileInMemory et autres ressources
topic_type:
- apiref
api_name:
- MrmDumpPriFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 253db38bf1e272f21ff66210bdbd07d5a33f4c60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510303"
---
# <a name="mrmdumpprifileinmemory-function"></a>MrmDumpPriFileInMemory fonction)

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Fait un dump d’un fichier PRI (binaire) dans son équivalent XML (en tant que données en mémoire), afin de le rendre plus facile à lire. La fonction alloue de la mémoire et retourne un pointeur vers cette mémoire dans *outputXmlData*. Appelez [**MrmFreeMemory**](mrmfreememory.md) avec le même pointeur pour libérer de la mémoire. Pour plus d’informations et pour obtenir des procédures pas à pas sur l’utilisation de ces API, consultez [API PRI (package Resource Indexing) et systèmes de génération personnalisés](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT HRESULT MrmDumpPriFileInMemory(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*indexFileName* \[ dans\]
</dt> <dd>

Type : **PCWSTR**

Chemin d’accès complet à un fichier PRI. Il s’agit du fichier PRI qui sera vidé au format XML.

</dd> <dt>

*schemaPriFile* \[ dans, facultatif\]
</dt> <dd>

Type : **PCWSTR**

Chemin de fichier complet facultatif d’un fichier de schéma (ou d’un fichier PRI représentant un schéma ; consultez la section Notes).

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

Un pack de ressources sans schéma est un pack créé avec l’argument [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) passé à [**MrmCreateResourceFile**](mrmcreateresourcefile.md) ou [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (ou avec le commutateur *omitSchemaFromResourcePacks* dans le fichier de configuration PRI). Pour vider un pack de ressources sans schéma, transmettez le chemin d’accès à vos données PRI de package principal en tant qu’argument pour le paramètre *schemaPriFile* .

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

 

