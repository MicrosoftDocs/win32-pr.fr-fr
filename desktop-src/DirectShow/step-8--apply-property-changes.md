---
description: 'Étape 8 :'
ms.assetid: c54745ef-beeb-40b6-9db6-6e3b5da860f8
title: 'Étape 8 : Appliquer les modifications de propriété'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2292d9f294711129b2edba50ef6fb623d767dfba4122295222d08eb1ad21dfb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652055"
---
# <a name="step-8-apply-property-changes"></a>Étape 8 : Appliquer les modifications de propriété

Substituez la méthode [**CBasePropertyPage :: OnApplyChanges**](cbasepropertypage-onapplychanges.md) pour valider les modifications apportées aux propriétés. Dans cet exemple, la \_ variable m lNewVal est mise à jour chaque fois que l’utilisateur fait défiler la barre du curseur. La méthode **OnApplyChanges** copie cette valeur dans la \_ variable m lVal, en remplaçant la valeur d’origine :


```C++
HRESULT CGrayProp::OnApplyChanges(void)
{
    m_lVal = m_lNewVal;
    return S_OK;
} 
```



Suivant : [étape 9. Déconnectez la page de propriétés](step-9--disconnect-the-property-page.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une page de propriétés de filtre](creating-a-filter-property-page.md)
</dt> </dl>

 

 



