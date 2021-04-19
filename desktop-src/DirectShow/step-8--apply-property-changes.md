---
description: 'Étape 8 :'
ms.assetid: c54745ef-beeb-40b6-9db6-6e3b5da860f8
title: 'Étape 8 : Appliquer les modifications de propriété'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46425613b8f23981a7b288121dc1a4ab0945452e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521115"
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

 

 



