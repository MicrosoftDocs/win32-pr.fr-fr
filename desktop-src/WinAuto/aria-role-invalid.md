---
title: Erreur de rôle ARIA
description: Erreur de rôle ARIA
ms.assetid: FEEB4F28-4A71-4417-A2F9-ABCB86B44F0F
keywords:
- AriaRoleErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c0fcef639a54bcd805bcb3f239e8d42cfeda8c5111d128c5f54157db75d7ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134012"
---
# <a name="aria-role-error"></a>Erreur de rôle ARIA

## <a name="text"></a>Texte

L’élément a un rôle WAI-ARIA non valide.

## <a name="type"></a>Type

Erreur

## <a name="description"></a>Description

Cette erreur s’applique à tous les éléments qui ont l’attribut [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) . Elle indique que l’attribut de **rôle** n’est pas une initiative d’accessibilité Web valide-valeur de rôle WAI-ARIA (Rich Internet applications) accessible comme défini par la spécification WAI-ARIA. La définition d’un rôle valide permet de s’assurer que l’élément est correctement interprété par les lecteurs d’écran et d’autres outils de technologie d’assistance.

Pour corriger cette erreur, affectez à l’attribut [**role**](https://developer.mozilla.org/docs/Web/HTML/Reference) une valeur de rôle WAI-ARIA valide. Notez que les rôles en WAI-ARIA abstraits ne sont pas valides.

## <a name="example"></a>Exemple


```HTML
<!—The invalid role will not expose this element as a button. -->
<div role="backbutton" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >

<!—Setting the correct role will expose this as a button that can be clicked. -->
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Erreur de rôle de conteneur ARIA](aria-container-role.md)
</dt> </dl>

 

 




