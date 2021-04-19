---
title: External. OnChangeViewOnlineListError, événement
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. OnChangeViewOnlineListError, événement
ms.assetid: f53dfc80-a7d7-42b1-b390-e90aa108145f
keywords:
- Événement External. OnChangeViewOnlineListError lecteur Windows Media
topic_type:
- apiref
api_name:
- External.OnChangeViewOnlineListError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09e9ff854893268a00cb7b5f2fb35409be2e70e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529950"
---
# <a name="externalonchangeviewonlinelisterror-event"></a>External. OnChangeViewOnlineListError, événement

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’événement **OnChangeViewOnlineListError** se produit lorsqu’un appel à la méthode [External. changeViewOnlineList](external-changeviewonlinelist.md) génère une erreur.

``` syntax
window.external.OnChangeViewOnlineListError = functionname
```

## <a name="possible-values"></a>Valeurs possibles

Il s’agit d’une propriété en écriture seule qui spécifie le nom de la fonction dans le script que le lecteur Windows Media appelle lorsque l’événement se produit.

## <a name="parameters"></a>Paramètres

La fonction qui gère cette erreur a les paramètres suivants.

<dl> <dt>

<span id="hr"></span><span id="HR"></span>*h*
</dt> <dd>

Code d’erreur **HRESULT** indiquant la raison de l’échec.

</dd> <dt>

<span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*
</dt> <dd>

La même chaîne qui a été passée dans le paramètre **LibraryLocationType** de **changeViewOnlineList**.

</dd> <dt>

<span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*
</dt> <dd>

La même chaîne qui a été passée dans le paramètre **LibraryLocationID** de **changeViewOnlineList**.

</dd> <dt>

<span id="Params"></span><span id="params"></span><span id="PARAMS"></span>*Params*
</dt> <dd>

La même chaîne qui a été passée dans le paramètre **params** de **changeViewOnlineList**.

</dd> <dt>

<span id="FriendlyName"></span><span id="friendlyname"></span><span id="FRIENDLYNAME"></span>*Convivial*
</dt> <dd>

La même chaîne qui a été passée dans le paramètre **FriendlyName** de **changeViewOnlineList**.

</dd> <dt>

<span id="ListType"></span><span id="listtype"></span><span id="LISTTYPE"></span>*Type*
</dt> <dd>

La même chaîne qui a été passée dans le paramètre **ListType** de **changeViewOnlineList**.

</dd> <dt>

<span id="ViewMode"></span><span id="viewmode"></span><span id="VIEWMODE"></span>*ViewMode*
</dt> <dd>

La même chaîne qui a été passée dans le paramètre **ViewMode** de **changeViewOnlineList**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





