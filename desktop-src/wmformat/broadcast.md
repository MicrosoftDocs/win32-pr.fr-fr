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
ms.openlocfilehash: bbf9e7d94682f8dbf08850f87954a934fd909afe
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106511867"
---
# <a name="broadcast"></a>Diffusion

L’attribut **Broadcast** est un attribut de niveau fichier qui indique si le contenu peut être diffusé. Il est supposé que tout contenu pour lequel aucun copyright n’a été attribué peut être légalement diffusé.

## <a name="global-constant"></a>Constante globale

\_wszWMBroadcast g

## <a name="data-type"></a>Type de données

**\_type WMT \_ bool**

## <a name="remarks"></a>Notes

Il s’agit d’un attribut codé.

Cet attribut ne peut pas être dupliqué au niveau du fichier. Si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) du format Windows Media.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Liste d’attributs**](attribute-list.md)
</dt> </dl>

 

 




