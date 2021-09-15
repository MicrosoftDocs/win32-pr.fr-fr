---
description: Indique si un flux de données contient du contenu protégé.
ms.assetid: 1c1a201c-4b55-4b86-a08f-d06c1a7db29d
title: Attribut MF_SD_PROTECTED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c97320d15353b8e23a43fa4efac2e5883a7366f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523657"
---
# <a name="mf_sd_protected-attribute"></a>\_ \_ Attribut protégé SD MF

Indique si un flux de données contient du contenu protégé.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Notes

Cet attribut s’applique aux descripteurs de flux. Si la valeur de l’attribut est **true**, le flux de données contient du contenu protégé. Si la valeur est **false** ou si l’attribut n’est pas défini, le flux contient du contenu clair.

Au lieu de vérifier chaque flux pour cet attribut, vous pouvez passer un descripteur de présentation à la fonction [**MFRequireProtectedEnvironment**](/windows/desktop/api/mfidl/nf-mfidl-mfrequireprotectedenvironment) . Cette fonction vérifie si le descripteur de présentation contient des flux protégés.

Une source de média doit définir cet attribut sur le descripteur de flux si le contenu requiert le chemin d’accès de média protégé (PMP).

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="examples"></a>Exemples


```
// This function returns TRUE if the stream contains protected 
// content. You can also call the MFRequireProtectedEnvironment 
// function to test whether a presentation contains any streams
// with protected content.

BOOL StreamHasProtectedContent(IMFStreamDescriptor *pSD)
{
    return MFGetAttributeUINT32(pSD, MF_SD_PROTECTED, FALSE);
}
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Attributs du descripteur de flux](stream-descriptor-attributes.md)
</dt> </dl>

 

 




