---
title: Diffusion
description: L’attribut Broadcast est un attribut de niveau fichier qui indique si le contenu peut être diffusé. Il est supposé que tout contenu pour lequel aucun copyright n’a été attribué peut être légalement diffusé.
ms.assetid: da2adf16-a9b5-4678-896e-2be8f5ca27e4
keywords:
- Diffuser le format Windows Media
topic_type:
- apiref
api_name:
- Broadcast
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b233a74deb71efe041ab5ad2f5e4ffa421d048a70c5b97e8f7ac38499bd18df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086162"
---
# <a name="broadcast"></a>Diffusion

L’attribut **Broadcast** est un attribut de niveau fichier qui indique si le contenu peut être diffusé. Il est supposé que tout contenu pour lequel aucun copyright n’a été attribué peut être légalement diffusé.

## <a name="global-constant"></a>Constante globale

\_wszWMBroadcast g

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Remarques

Il s’agit d’un attribut codé.

Cet attribut ne peut pas être dupliqué au niveau du fichier. si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) de Format multimédia Windows.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




