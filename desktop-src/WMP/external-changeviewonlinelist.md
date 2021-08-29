---
title: External. changeViewOnlineList, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. changeViewOnlineList, méthode
ms.assetid: d7a45ced-431f-4d35-8c9c-c6eeba6fcbf3
keywords:
- Lecteur Windows Media de la méthode changeViewOnlineList
- méthode changeViewOnlineList Lecteur Windows Media, classe externe
- Lecteur Windows Media de classe externe, méthode changeViewOnlineList
topic_type:
- apiref
api_name:
- External.changeViewOnlineList
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bfd5601dc1eaa1ad325a39e1a340537c3863eee48f26510acefbc57ecd0cdbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649259"
---
# <a name="externalchangeviewonlinelist-method"></a>External. changeViewOnlineList, méthode

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

la méthode **changeViewOnlineList** modifie la vue dans Lecteur Windows Media pour afficher une liste générée dynamiquement par le magasin en ligne.

## <a name="syntax"></a>Syntaxe


```JScript
External.changeViewOnlineList(
  LibraryLocationType,
  LibraryLocationID,
  Params,
  FriendlyName,
  ListType,
  ViewMode
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

**Chaîne** contenant l’ID de l’élément spécifique à afficher dans la nouvelle vue. Par exemple, si *LibraryLocationType* est CPGenreID, ce paramètre spécifie l’ID du genre à afficher dans la nouvelle vue. Cette chaîne peut être vide.

</dd> <dt>

*Paramètres* \[ dans\]
</dt> <dd>

**chaîne** contenant des paramètres qui Lecteur Windows Media transmis au plug-in du magasin en ligne en appelant [IWMPContentPartner :: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate). ces paramètres ne sont pas interprétés par Lecteur Windows Media. Ils sont créés par le magasin en ligne et ont une signification uniquement pour le magasin en ligne. Cette chaîne peut être vide

</dd> <dt>

*FriendlyName* \[ dans\]
</dt> <dd>

**chaîne** contenant un nom convivial, à afficher par Lecteur Windows Media, pour la liste dynamique.

</dd> <dt>

*ListType* \[ dans\]
</dt> <dd>

Constante d’emplacement de bibliothèque qui spécifie le type des éléments de la liste générée dynamiquement. Par exemple, si la valeur de ce paramètre est CPTrackID, la liste dynamique contient des pistes.

</dd> <dt>

*ViewMode* \[ dans\]
</dt> <dd>

**chaîne** qui spécifie le mode utilisé par Lecteur Windows Media pour afficher la liste dynamique. L’appelant doit définir ce paramètre sur l’une des valeurs suivantes, qui sont définies dans contentpartner. h :

ViewModeReport

ViewModeDetails

ViewModeIcon

ViewModeTile

ViewModeOrderedList

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

lorsque le script sur une page de découverte appelle **changeViewOnlineList**, Lecteur Windows Media passe certains des paramètres aux méthodes [IWMPContentPartner :: GetListContents](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents) et [IWMPContentPartner :: GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) , qui sont implémentées par le plug-in du magasin en ligne. Le tableau suivant montre la correspondance entre les paramètres des trois méthodes.



| paramètre changeViewOnlineList | Paramètre GetListContents | Paramètre GetTemplate |
|--------------------------------|---------------------------|-----------------------|
| *LocationType (*                 | *location*                | *location*            |
| *LocationID*                   | *pContext*                | *pContext*            |
| *Params*                       | *bstrParams*              | *bstrViewParams*      |
| *Type*                     | *bstrListType*            | Non applicable        |



 

Étant donné que les trois méthodes indiquées dans le tableau précédent sont implémentées par le magasin en ligne, vous disposez d’une certaine flexibilité dans la façon dont vous utilisez les paramètres. L’idée est que vous fournissez suffisamment d’informations pour que **GetListContents** détermine la liste qu’il doit récupérer et pour **GetTemplate** déterminer la page de découverte à afficher ensuite. Les exemples suivants illustrent deux possibilités.

**Exemple 1 : liste dynamique figurant dans le catalogue du magasin en ligne**

Supposons que vous souhaitiez que le plug-in récupère le contenu de la liste dynamique dont l’ID est 6 dans le catalogue du magasin en ligne. Supposons que la liste 6 est une liste de pistes. Vous pouvez fournir le plug-in avec suffisamment d’informations en effectuant l’appel suivant.


```C++
external.changeViewOnlineList(
   "CPListID", 6, "", 
   "Songs for Today", "CPTrackID", "ViewModeDetails");
```



Notez que le paramètre *params* est vide. le plug-in a suffisamment d’informations dans les autres paramètres.

**Exemple 2 : liste dynamique qui ne figure pas dans le catalogue du magasin en ligne**

Supposons que vous souhaitiez que le plug-in récupère le contenu d’une liste dynamique qui ne figure pas dans le catalogue du magasin en ligne. Peut-être avez-vous décidé d’avoir une liste dynamique qui comprend des chansons sélectionnées par un artiste particulier. Supposons que l’artiste a un ID de 2 dans le catalogue du magasin en ligne. Vous pouvez effectuer l’appel suivant.


```C++
external.changeViewOnlineList(
   "CPArtistID", 2, "songs picked by Sally", 
   "Sally Picks", "CPTrackID", "ViewModeDetails");
```



Notez que les paramètres *LocationType (* et *LocationID* ne spécifient pas la liste. Au lieu de cela, le paramètre *params* spécifie la liste. Les paramètres *LocationType (* et *LocationID* sont passés à **IWMPContentPartner :: GetListContents**, mais dans ce cas, **GetListContents** peut les ignorer. Les paramètres *LocationType (* et *LocationID* sont également passés à **IWMPContentPartner :: GetTemplate**, qui peuvent les utiliser pour déterminer quelle page de découverte doit être affichée avec la liste dynamique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**IWMPContentPartner::GetListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getlistcontents)
</dt> <dt>

[**IWMPContentPartnerCallback::AddListContents**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-addlistcontents)
</dt> <dt>

[**IWMPContentPartner::GetTemplate**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate)
</dt> <dt>

[**Emplacement et élément sélectionné**](location-and-selected-item.md)
</dt> </dl>

 

 





