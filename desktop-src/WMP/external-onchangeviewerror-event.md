---
title: External. OnChangeViewError, événement
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. OnChangeViewError, événement
ms.assetid: d6370629-5f50-434d-8eb5-5b43d1b2f7fe
keywords:
- Événement External. OnChangeViewError lecteur Windows Media
topic_type:
- apiref
api_name:
- External.OnChangeViewError Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91bcbb71e1c5324a9907d735492364561be49a60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533173"
---
# <a name="externalonchangeviewerror-event"></a>External. OnChangeViewError, événement

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’événement **OnChangeViewError** se produit lorsqu’un appel à la méthode [External. changeView](external-changeview.md) génère une erreur.

``` syntax
window.external.OnChangeViewError = FunctionName
```

## <a name="possible-values"></a>Valeurs possibles

Il s’agit d’une propriété en écriture seule qui spécifie le nom de la fonction dans le script que le lecteur Windows Media appelle lorsque l’événement se produit.

## <a name="parameters"></a>Paramètres

La fonction qui gère cet événement a les paramètres suivants.

<dl> <dt>

<span id="hr"></span><span id="HR"></span>*h*
</dt> <dd>

Code d’erreur **HRESULT** indiquant la raison de l’échec.

</dd> <dt>

<span id="LibraryLocationType"></span><span id="librarylocationtype"></span><span id="LIBRARYLOCATIONTYPE"></span>*LibraryLocationType*
</dt> <dd>

La même chaîne qui a été passée dans le paramètre **LibraryLocationType** de **changeView**.

</dd> <dt>

<span id="LibraryLocationID"></span><span id="librarylocationid"></span><span id="LIBRARYLOCATIONID"></span>*LibraryLocationID*
</dt> <dd>

La même chaîne thatwas transmise dans le paramètre **LibraryLocationID** de **changeView**.

</dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>*Filtres*
</dt> <dd>

La même chaîne qui a été passée dans le paramètre de **filtre** de **changeView**.

</dd> <dt>

<span id="ViewParams"></span><span id="viewparams"></span><span id="VIEWPARAMS"></span>*ViewParams*
</dt> <dd>

La même chaîne qui a été passée dans le paramètre **ViewParams** de **changeView**.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ExternalObject pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





