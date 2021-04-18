---
title: External. viewParameters
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. viewParameters
ms.assetid: 0afabe35-2857-413a-a662-1a76d3fb75fe
keywords:
- External. viewParameters Windows Media Player
topic_type:
- apiref
api_name:
- External.viewParameters
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0adec580a68bd3f6b92beef1de814729848179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533080"
---
# <a name="externalviewparameters"></a>External. viewParameters

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La propriété **viewParameters** récupère les paramètres associés à la vue actuelle dans le lecteur Windows Media.

## <a name="syntax"></a>Syntaxe

**Window. external. viewParameters**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété retourne une **chaîne** en lecture seule.

## <a name="remarks"></a>Notes

Cette propriété récupère les paramètres qui ont été définis précédemment par le magasin en ligne. Par exemple, le magasin en ligne peut spécifier des paramètres d’affichage dans le paramètre *ViewParams* de la méthode [changeView](external-changeview.md) ou le paramètre *params* de la méthode [changeViewOnlineList](external-changeviewonlinelist.md) .

Les paramètres d’affichage ne sont pas interprétés par le lecteur Windows Media. Ils sont créés par le magasin en ligne et ont une signification uniquement pour le magasin en ligne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





