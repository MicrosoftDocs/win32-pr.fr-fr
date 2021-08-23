---
title: External. accountType
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La propriété accountType récupère le type de compte de l’utilisateur actuel.
ms.assetid: 4fb6de90-a32d-4483-bbae-b23cbff93bd5
keywords:
- External. accountType Lecteur Windows Media
topic_type:
- apiref
api_name:
- External.accountType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bd19413d891f5a8008b162f6795af29a9d15e75a80d35bb82ff13f8e013da9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650039"
---
# <a name="externalaccounttype"></a>External. accountType

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La propriété **AccountType** récupère le type de compte de l’utilisateur actuel.

``` syntax
window.external.accountType
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule qui représente le type de compte. Les chaînes qui représentent différents types de compte sont définies par le magasin en ligne.

## <a name="remarks"></a>Remarques

Cette propriété récupère le type de compte en appelant la méthode [IWMPContentPartner :: GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) , qui est implémentée par le plug-in du magasin en ligne. si l’utilisateur actuel est connecté au magasin en ligne ou si le plug-in a mis en cache les informations d’identification de l’utilisateur, la méthode **getContentPartnerInfo** peut déterminer le type de compte de l’utilisateur et le renvoyer à Lecteur Windows Media. le type de compte est une chaîne que Lecteur Windows Media n’interprète pas. au lieu de cela, Lecteur Windows Media transmet la chaîne du plug-in du magasin en ligne au script sur la page de découverte du magasin en ligne.

Si l’utilisateur actuel n’est pas connecté au magasin en ligne et que le plug-in de la boutique en ligne ne dispose pas d’informations d’identification mises en cache pour l’utilisateur, cette propriété récupère toute chaîne renvoyée par la méthode **getContentPartnerInfo** dans cette situation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. userLoggedIn**](external-userloggedin.md)
</dt> </dl>

 

 





