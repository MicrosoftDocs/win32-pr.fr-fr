---
title: Is_Trusted
description: L' \_ attribut is Trusted est un attribut de niveau fichier qui spécifie si l’URL d’acquisition de licence dans le fichier est approuvée.
ms.assetid: 7b383b45-e992-4a07-af0b-9ef220ddd9af
keywords:
- Format Windows Media Is_Trusted
topic_type:
- apiref
api_name:
- Is_Trusted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e8dd4fdd638bad0908bb1bbf50135cde5bad6c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103940512"
---
# <a name="is_trusted"></a>Est \_ approuvé

L’attribut **is \_ Trusted** est un attribut de niveau fichier qui spécifie si l’URL d’acquisition de licence dans le fichier est approuvée.

## <a name="global-constant"></a>Constante globale

\_wszWMTrusted g

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Notes

Il s’agit d’un attribut codé.

Avant de naviguer vers une URL d’acquisition de licence contenue dans un fichier protégé par DRM, une application doit d’abord vérifier que cette propriété a la valeur true. Si la valeur est false, l’application doit avertir l’utilisateur que l’URL a peut-être été falsifiée.

Cet attribut ne peut pas être dupliqué au niveau du fichier. Si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) du format Windows Media.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




