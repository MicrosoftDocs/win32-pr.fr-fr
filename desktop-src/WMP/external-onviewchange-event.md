---
title: External. OnViewChange, événement
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. L’événement OnViewChange se produit lorsque la vue change dans le lecteur Windows Media.
ms.assetid: aa1378ad-8b84-4592-85c5-5e284be05ea6
keywords:
- Événement External. OnViewChange lecteur Windows Media
topic_type:
- apiref
api_name:
- External.OnViewChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c7144e03955fb67ed90cad4a4336bf782ca1566
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106536455"
---
# <a name="externalonviewchange-event"></a>External. OnViewChange, événement

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’événement **OnViewChange** se produit lorsque la vue change dans le lecteur Windows Media.

``` syntax
window.external.OnViewChange = FunctionName
```

## <a name="possible-values"></a>Valeurs possibles

Il s’agit d’une propriété en écriture seule qui spécifie le nom de la fonction dans le script que le lecteur Windows Media appelle lorsque l’événement se produit.

## <a name="parameters"></a>Paramètres

La fonction qui gère cet événement n’accepte aucun paramètre.

## <a name="remarks"></a>Notes

La vue dans le lecteur Windows Media peut changer pour l’une des raisons suivantes :

-   L’utilisateur interagit avec l’interface utilisateur du lecteur Windows Media.
-   L’utilisateur interagit avec une page de découverte et le script sur la page de découverte appelle [External. changeView](external-changeview.md).
-   L’utilisateur interagit avec une page de découverte et le script sur la page de découverte appelle [External. changeViewOnlineList](external-changeviewonlinelist.md).

Lorsque la vue change dans le lecteur Windows Media, le lecteur appelle [IWMPContentPartner :: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) pour obtenir l’URL de la page de découverte suivante à afficher. Toutefois, avant que le lecteur n’affiche la page nouvelle détection, il déclenche l’événement **OnViewChange** . Si le gestionnaire d’événements **OnViewChange** appelle [External. CancelNavigate](external-cancelnavigate.md), le lecteur Windows Media n’affiche pas la page nouvelle détection. Au lieu de cela, il continue d’afficher la page de découverte actuelle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. changeView**](external-changeview.md)
</dt> <dt>

[**External. changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> </dl>

 

 





