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
ms.openlocfilehash: a3e255c91c5779eb44da8e587601fdfd9264f10888a46a7f216ae2af619ff9f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118198275"
---
# <a name="is_trusted"></a>Est \_ approuvé

L’attribut **is \_ Trusted** est un attribut de niveau fichier qui spécifie si l’URL d’acquisition de licence dans le fichier est approuvée.

## <a name="global-constant"></a>Constante globale

\_wszWMTrusted g

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Remarques

Il s’agit d’un attribut codé.

Avant de naviguer vers une URL d’acquisition de licence contenue dans un fichier protégé par DRM, une application doit d’abord vérifier que cette propriété a la valeur true. Si la valeur est false, l’application doit avertir l’utilisateur que l’URL a peut-être été falsifiée.

Cet attribut ne peut pas être dupliqué au niveau du fichier. si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) de Format multimédia Windows.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




