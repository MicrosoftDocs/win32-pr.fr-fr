---
title: STYLE (instruction)
description: Définit le style de la fenêtre de la boîte de dialogue. Le style de fenêtre spécifie si la zone est une fenêtre contextuelle ou une fenêtre enfant.
ms.assetid: 5ede57ad-5fa5-414c-9823-e66994826027
keywords:
- Menus de l’instruction de STYLE et autres ressources
topic_type:
- apiref
api_name:
- STYLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88d74ced35b6b5a2f6c04004fbd2e161df7ba16ff5111577835b93363291c114
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886763"
---
# <a name="style-statement"></a>STYLE (instruction)

Définit le style de la fenêtre de la boîte de dialogue. Le style de fenêtre spécifie si la zone est une fenêtre contextuelle ou une fenêtre enfant.

``` syntax
STYLE style
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*style*
</dt> <dd>

Style de fenêtre. Ce paramètre peut être une valeur entière ou une combinaison de valeurs de style de fenêtre (par exemple, **WS \_ Caption** et **WS \_ SYSMENU**) et des valeurs de style de boîte de dialogue (par exemple, **DS \_ Center**).

</dd> </dl>

Pour obtenir la liste des styles de fenêtre, consultez [styles de fenêtre](/windows/desktop/winmsg/window-styles). Pour obtenir la liste des styles de boîte de dialogue, consultez [styles de modèle](../dlgbox/about-dialog-boxes.md)de boîte de dialogue. si vous utilisez les valeurs de style de la fenêtre ou de la boîte de dialogue, vous devez inclure Windows. h.

 

 