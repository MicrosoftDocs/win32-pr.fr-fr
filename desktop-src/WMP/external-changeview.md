---
title: External. changeView, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. la méthode changeView modifie la vue dans Lecteur Windows Media.
ms.assetid: bd9d7d4b-ee4c-4d7c-92ef-dd0b8ab46d9d
keywords:
- Lecteur Windows Media de la méthode changeView
- méthode changeView Lecteur Windows Media, classe externe
- Lecteur Windows Media de classe externe, méthode changeView
topic_type:
- apiref
api_name:
- External.changeView
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa982e87e0a25fa8ae6cc80b428524844f60e2ec76f50d246e7b2a76b3ca942a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649369"
---
# <a name="externalchangeview-method"></a>External. changeView, méthode

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

la méthode **changeView** modifie la vue dans Lecteur Windows Media.

## <a name="syntax"></a>Syntaxe


```JScript
External.changeView(
  LibraryLocationType,
  LibraryLocationID,
  Filter,
  ViewParams
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*LibraryLocationType* \[ dans\]
</dt> <dd>

[Constante d’emplacement de bibliothèque](library-location-constants.md) qui spécifie le type de la nouvelle vue. Par exemple, la constante CPGenreID spécifie que la nouvelle vue affichera un genre particulier.

</dd> <dt>

*LibraryLocationID* \[ dans\]
</dt> <dd>

**Chaîne** contenant l’ID de l’élément spécifique à afficher dans la nouvelle vue. Par exemple, si *LibraryLocationType* est CPGenreID, ce paramètre spécifie l’ID du genre à afficher dans la nouvelle vue. Cette chaîne peut être vide. Consultez la section Notes.

</dd> <dt>

*Filtre* \[ dans\]
</dt> <dd>

**Chaîne** contenant le filtre pour la nouvelle vue. La vue sera filtrée comme si l’utilisateur avait entré ce texte dans le contrôle de roulette de mot du joueur. Cette chaîne peut être vide.

</dd> <dt>

*ViewParams* \[ dans\]
</dt> <dd>

**chaîne** contenant les paramètres que Lecteur Windows Media met à la disposition de la nouvelle page de découverte qui s’affiche avec la nouvelle vue. ces paramètres ne sont pas interprétés par Lecteur Windows Media. Ils sont créés par le magasin en ligne et ont une signification uniquement pour le magasin en ligne.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Dans certains cas, il est logique de définir le paramètre *LibraryLocationID* sur une chaîne vide. Par exemple, si vous définissez le paramètre *LibraryLocationType* sur AllCPAlbumIDs, la nouvelle vue représentera tous les albums. Aucun album individuel n’est l’objectif de la nouvelle vue. il n’est donc pas nécessaire de fournir un ID d’album dans le paramètre *LibraryLocationID* .

Le paramètre *ViewParams* permet à une page de découverte de communiquer avec une autre page de découverte. lorsque le script sur une page de découverte appelle **changeView**, Lecteur Windows Media ajuste son interface utilisateur. Cet ajustement fait en sorte que le lecteur appelle la méthode [IWMPContentPartner :: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) du plug-in pour obtenir l’URL d’une nouvelle page de découverte. La chaîne que la page de découverte d’origine transmet dans le paramètre *ViewParams* n’est pas passée à **GetTemplate**. Toutefois, la nouvelle page de découverte peut récupérer la chaîne *ViewParams* en appelant [External. viewParameters](external-viewparameters.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External. libraryLocationID**](external-librarylocationid.md)
</dt> <dt>

[**External. libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**External. viewParameters**](external-viewparameters.md)
</dt> </dl>

 

 





