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
ms.openlocfilehash: 8c0648cc82faae7a0bab9614761caef98c316fd73b5eb90550d14754386282f7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109929"
---
# <a name="wmpicture"></a>WM/image

L’attribut **WM/Picture** contient une image associée au contenu.

## <a name="global-constant"></a>Constante globale

\_wszWMPicture g

## <a name="data-type"></a>Type de données

[**WM \_ IMAGE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**\_ type de type WMT \_ binaire**)

## <a name="remarks"></a>Remarques

Cet attribut est compatible avec le frame ID3, APIC. La spécification ID3 du frame APIC stipule que, bien qu’il puisse y avoir un nombre quelconque d’images APIC associées à un fichier, une seule peut être de type 1 et une seule peut être de type 2. La spécification stipule également que la description de l’image ne peut pas dépasser 64 caractères, mais peut être vide.

les attributs WM/Picture ajoutés avec les objets du kit de développement logiciel (SDK) Windows Media Format ne sont pas validés automatiquement pour être conformes aux spécifications ID3. Vous devez ajouter du code dans votre application pour effectuer les validations si vous souhaitez assurer une compatibilité complète avec ID3.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> <dt>

[**\_image WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)
</dt> </dl>

 

 




