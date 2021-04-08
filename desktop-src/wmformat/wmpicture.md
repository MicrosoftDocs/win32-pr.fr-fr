---
title: WM/image
description: L’attribut WM/Picture contient une image associée au contenu.
ms.assetid: ec82dfdf-7755-4758-9771-096aac114f78
keywords:
- Format Windows Media WM/Picture
topic_type:
- apiref
api_name:
- WM/Picture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ba3f74378112c8e3f58958db8b22c970e8e099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103940442"
---
# <a name="wmpicture"></a>WM/image

L’attribut **WM/Picture** contient une image associée au contenu.

## <a name="global-constant"></a>Constante globale

\_wszWMPicture g

## <a name="data-type"></a>Type de données

[**WM \_ IMAGE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**\_ type de type WMT \_ binaire**)

## <a name="remarks"></a>Notes

Cet attribut est compatible avec le frame ID3, APIC. La spécification ID3 du frame APIC stipule que, bien qu’il puisse y avoir un nombre quelconque d’images APIC associées à un fichier, une seule peut être de type 1 et une seule peut être de type 2. La spécification stipule également que la description de l’image ne peut pas dépasser 64 caractères, mais peut être vide.

Les attributs WM/Picture ajoutés avec les objets du kit de développement logiciel (SDK) du format Windows Media ne sont pas validés automatiquement pour être conformes aux spécifications ID3. Vous devez ajouter du code dans votre application pour effectuer les validations si vous souhaitez assurer une compatibilité complète avec ID3.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> <dt>

[**\_image WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)
</dt> </dl>

 

 




