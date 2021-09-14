---
title: DRM_Level
description: '\_le niveau DRM est un attribut de licence défini par le kit de développement logiciel (SDK) de Format de média Windows lors de la création d’une licence locale pour les fichiers protégés avec la version 1 de DRM.'
ms.assetid: 05357378-4d73-48df-a3b5-bdb2c543ec66
keywords:
- Format Windows Media DRM_Level
topic_type:
- apiref
api_name:
- DRM_Level
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3177197b9c149c2fca2c7678a8fe03c6b412e2d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293863"
---
# <a name="drm_level"></a>\_Niveau DRM

**DRM \_ Level** est un attribut de licence que le kit de développement logiciel (SDK) de Format multimédia Windows définit lorsqu’il crée une licence locale pour les fichiers protégés par la version 1 de DRM. Il contient le niveau de sécurité que l’application appelante doit avoir pour accéder au contenu du fichier. La valeur par défaut est 150.

## <a name="global-constant"></a>Constante globale

\_niveau de wszWMDRM g \_

## <a name="data-type"></a>Type de données

**\_valeur DWORD de type WMT \_**

## <a name="remarks"></a>Notes

Le niveau de sécurité DRM d’une application est déterminé par la bibliothèque wmstubdrm particulière à laquelle il est lié au moment de la compilation. Pour plus d’informations sur ces niveaux de sécurité, consultez [obtention de la bibliothèque DRM requise](obtaining-the-required-drm-library.md). Utilisez [**IWMHeaderInfo :: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) pour définir cette propriété lors de la protection des fichiers ASF avec la version 1 de DRM.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés DRM**](drm-properties.md)
</dt> </dl>

 

 




