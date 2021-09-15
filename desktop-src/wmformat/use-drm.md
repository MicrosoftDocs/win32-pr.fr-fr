---
title: Use_DRM
description: L’attribut utiliser la \_ gestion des droits numériques (DRM) demande à l’objet enregistreur d’appliquer la protection DRM version 1 au fichier actuel.
ms.assetid: ad959e4a-faf7-4b61-9988-6878afcf3a90
keywords:
- Format Windows Media Use_DRM
topic_type:
- apiref
api_name:
- Use_DRM
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fcb010855ac4660792a7c579556001d5d7c4c96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521040"
---
# <a name="use_drm"></a>Utiliser \_ DRM

L’attribut utiliser la gestion des **\_ droits numériques (DRM** ) demande à l’objet enregistreur d’appliquer la protection DRM version 1 au fichier actuel.

## <a name="global-constant"></a>Constante globale

g \_ wszWMUse \_ DRM

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Notes

Utilisez [**IWMHeaderInfo :: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) pour affecter à cette propriété la **valeur true** lors de la création du contenu DRM version 1. Cette propriété n’est pas accessible à partir de l’objet lecteur.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> </dl>

 

 




