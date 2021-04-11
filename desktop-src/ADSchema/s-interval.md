---
title: Syntaxe d’intervalle
description: Représente une valeur d’intervalle de temps.
ms.assetid: e41b71da-cd05-4a4a-8b97-9210dbe314de
ms.tgt_platform: multiple
keywords:
- Schéma Active Directory de syntaxe d’intervalle
topic_type:
- apiref
api_name:
- Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b92961deecde7faa879dbbda6bfd24560ad705
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104385319"
---
# <a name="interval-syntax"></a>Syntaxe d’intervalle

Représente une valeur d’intervalle de temps. Les unités de temps réelles dépendent de l’attribut qui utilise cette syntaxe. Cette syntaxe est identique à la syntaxe [**LargeInteger**](s-largeinteger.md) , sauf que les valeurs haute et basse sont des entiers non signés.



| Entrée | Valeur |
|--------------|------------------------------------------------------------------------------------|
| Nom         | Intervalle                                                                           |
| ID de syntaxe    | 2.5.5.16                                                                           |
| ID OM        | 65                                                                                 |
| Type MAPI    | \-                                                                                 |
| Type ADS     | \_entier long \_ ADSTYPE                                                            |
| Type de variante | \_distribution vt                                                                       |
| SDS, type     | Objet COM pouvant être casté en [**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger). |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IADsLargeInteger**](/windows/desktop/api/iads/nn-iads-iadslargeinteger)
</dt> <dt>

[**LargeInteger**](s-largeinteger.md)
</dt> </dl>

 

 
