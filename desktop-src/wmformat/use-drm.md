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
ms.openlocfilehash: b802a7bef777fab4ed835aa3a1770169deaa6eeea9a7eddeb802fb2e4b0a9dd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845300"
---
# <a name="use_drm"></a>Utiliser \_ DRM

L’attribut utiliser la gestion des **\_ droits numériques (DRM** ) demande à l’objet enregistreur d’appliquer la protection DRM version 1 au fichier actuel.

## <a name="global-constant"></a>Constante globale

g \_ wszWMUse \_ DRM

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Remarques

Utilisez [**IWMHeaderInfo :: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) pour affecter à cette propriété la **valeur true** lors de la création du contenu DRM version 1. Cette propriété n’est pas accessible à partir de l’objet lecteur.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> </dl>

 

 




