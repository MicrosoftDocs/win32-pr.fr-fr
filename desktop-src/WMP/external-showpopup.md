---
title: External. showPopup, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. showPopup, méthode
ms.assetid: 17958543-dbed-45a5-9b02-4800a07cb820
keywords:
- méthode showPopup Lecteur Windows Media
- méthode showPopup Lecteur Windows Media, classe externe
- External, classe Lecteur Windows Media, méthode showPopup
topic_type:
- apiref
api_name:
- External.showPopup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a651add93e32c1c2eb82827a4089a338341f2506ba26d9fbb06061aa6d185d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648339"
---
# <a name="externalshowpopup-method"></a>External. showPopup, méthode

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

la méthode **showPopup** demande à Lecteur Windows Media d’afficher une page web contextuelle ; autrement dit, une page Web qui s’affiche dans une fenêtre distincte.

## <a name="syntax"></a>Syntaxe


```JScript
External.showPopup(
  PopupIndex,
  Parameters
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PopupIndex* \[ dans\]
</dt> <dd>

**Nombre** (**long**) qui spécifie l’index de la page Web contextuelle.

</dd> <dt>

*Paramètres* \[ dans\]
</dt> <dd>

**chaîne** qui Lecteur Windows Media ajoute à l’URL de la page web.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

l’index contextuel n’est pas interprété par Lecteur Windows Media. Les index qui identifient les pages Web contextuelles sont créés par le magasin en ligne et ont une signification uniquement pour le magasin en ligne.

les étapes suivantes montrent comment Lecteur Windows Media utilise les paramètres de la méthode **showPopup** pour créer une URL pour la fenêtre contextuelle.

1.  Un script sur une page de découverte appelle **ShowPopup**, en passant un entier dans *PopupIndex* et une chaîne dans les *paramètres*.

2.  Lecteur Windows Media passe l’index à [IWMPContentPartner :: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) pour récupérer l’URL de la page web à afficher.

3.  Lecteur Windows Media ajoute des *paramètres* à l’URL sous la forme d’une chaîne de requête. par exemple, si **GetItemInfo** retourne « https://www.Proseware.com/Pages/Popup1.htm » et que les *paramètres* sont égaux à « DlgX = 800&DlgY = 400&Greeting = Hi », Lecteur Windows Media crée l’URL suivante :

    https://www.Proseware.com/Pages/Popup1.htm?DlgX=800&DlgY=400&Greeting=Hi

Vous pouvez utiliser des *paramètres* pour spécifier la taille de la fenêtre indépendante. Par exemple, si vous définissez les *paramètres* sur « DlgX = 800&DlgY = 400 », la fenêtre contextuelle aura une taille de 800 pixels par 400 pixels.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





