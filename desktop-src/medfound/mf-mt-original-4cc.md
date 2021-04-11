---
description: Contient le FOURCC du codec d’origine pour un flux vidéo.
ms.assetid: 2e6ef198-5754-4ded-9fe3-61edd0742a17
title: Attribut MF_MT_ORIGINAL_4CC (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b374ba3ef74cb98925edcc5d809e1fd5e0b7fbcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952660"
---
# <a name="mf_mt_original_4cc-attribute"></a>\_ \_ Attribut 4cc d’origine MF MT \_

Contient le FOURCC du codec d’origine pour un flux vidéo.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Notes

En fonction du fichier source, la source du média AVI peut définir cet attribut sur les types de médias qu’elle propose.

Un fichier AVI contient un en-tête de flux pour chaque flux du fichier. La source de média AVI traduit l’en-tête de flux en un type de média. Pour les flux vidéo compressés, l’en-tête de flux contient un FOURCC qui identifie le codec vidéo. Dans la plupart des cas, la source de média AVI convertit ce FOURCC directement en un GUID de sous-type, comme décrit dans la rubrique GUID de sous- [type de vidéo](video-subtype-guids.md). Toutefois, dans certains cas, il mappe le FOURCC d’origine à un autre FOURCC équivalent. Si c’est le cas, la source du média stocke le FOURCC d’origine dans le type de média, à l’aide de l' \_ \_ attribut 4cc d’origine MF MT \_ .

Les mappages FOURCC sont stockés dans le Registre sous la clé suivante :

**HKEY \_ CLASSES \_ racine** \\ **MediaFoundation** \\ **MapVideo4cc**

Chaque entrée est une valeur **DWORD** . Le nom de l’entrée est la représentation hexadécimale du FOURCC, sans préfixe « 0x », et le premier caractère apparaissant en premier dans la chaîne. Par exemple, le code FOURCC « ABCD » apparaît sous la forme « 61626364 ». La valeur de l’entrée est le code FOURCC équivalent.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




