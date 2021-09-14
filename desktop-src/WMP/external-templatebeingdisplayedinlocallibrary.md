---
title: External. templateBeingDisplayedInLocalLibrary
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. templateBeingDisplayedInLocalLibrary
ms.assetid: a1399c20-804b-4413-be9d-bcf160d75d29
keywords:
- External. templateBeingDisplayedInLocalLibrary Lecteur Windows Media
topic_type:
- apiref
api_name:
- External.templateBeingDisplayedInLocalLibrary
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f1d9a93d870882a34014ea2d0d35f29b91f54d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192303"
---
# <a name="externaltemplatebeingdisplayedinlocallibrary"></a>External. templateBeingDisplayedInLocalLibrary

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La propriété **templateBeingDisplayedInLocalLibrary** indique si le flux représenté par la page de découverte active s’affiche dans le contrôle d’arborescence de la bibliothèque locale.

## <a name="syntax"></a>Syntaxe

``` syntax
window.external.templateBeingDisplayedInLocalLibrary
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **valeur booléenne** en lecture seule. **True** indique que le flux est affiché dans le contrôle Tree-View de la bibliothèque locale.

## <a name="remarks"></a>Notes

Une page de découverte qui représente un flux pour une sélection dynamique peut afficher un bouton qui permet à l’utilisateur d’enregistrer le flux dans sa bibliothèque locale. L’enregistrement du flux, dans ce contexte, signifie que certaines métadonnées sont enregistrées sur l’ordinateur de l’utilisateur et que le flux est listé sous le nœud **sélections** dans le contrôle arborescence de la bibliothèque locale. Script sur la page détection peut inspecter la propriété **templateBeingDisplayedInLocalLibrary** pour déterminer si l’utilisateur a déjà enregistré le flux dans la bibliothèque locale. Si l’utilisateur a déjà enregistré le flux, la page détection ne doit pas afficher le bouton enregistrer.

Une page de découverte qui représente un flux radio doit inspecter la propriété **templateBeingDisplayedInLocalLibrary** pour la même raison.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





