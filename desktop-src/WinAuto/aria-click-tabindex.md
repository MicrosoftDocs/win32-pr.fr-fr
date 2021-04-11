---
title: Erreur de la TabIndex ARIA
description: Erreur de la TabIndex ARIA
ms.assetid: CCBC56E8-8899-4962-8315-762538CA666C
keywords:
- AriaTabIndexErrorId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acfec56fe1f9f6074579a8b84bccc9dfdef2e1da
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104032029"
---
# <a name="aria-tabindex-error"></a>Erreur de la TabIndex ARIA

## <a name="text"></a>Texte

L’élément n’est pas désactivé et possède un gestionnaire d’événements **Click** , mais il a **TabIndex** < 0 et n’est pas dans l’ordre de tabulation par défaut.

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

Cette erreur s’applique aux éléments qui ont un gestionnaire d’événements Click et qui ne sont pas désactivés. Ces éléments doivent être dans l’ordre de tabulation. Cela garantit qu’un élément peut être atteint à l’aide de la touche Tab, ce qui indique comment les utilisateurs de lecteurs d’écran parcourent généralement l’interface utilisateur.

Pour corriger cette erreur, affectez à l’attribut [**TabIndex**](https://developer.mozilla.org/docs/Web/HTML/Global_attributes/tabindex) une valeur supérieure ou égale à 0. Vous n’avez pas besoin de définir explicitement l’attribut **TabIndex** pour les balises qui sont dans l’ordre de tabulation par défaut, par exemple un (avec attribut [**href**](https://developer.mozilla.org/docs/Web/HTML/Attributes) ), un [**bouton**](https://developer.mozilla.org/docs/Web/HTML/Element/button), une [**entrée**](https://developer.mozilla.org/docs/Web/HTML/Element/input) (à l’exclusion de « masqué »), une [**sélection**](https://developer.mozilla.org/docs/Web/HTML/Element/select), [**un**](https://developer.mozilla.org/docs/Web/HTML/Element/a) élément [**textarea**](https://developer.mozilla.org/docs/Web/HTML/Element/textarea)et une [**zone**](https://developer.mozilla.org/docs/Web/HTML/Element/area) (dans le cadre de l’image interactive).

## <a name="example"></a>Exemple


```HTML
<div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)" >
```



 

 




