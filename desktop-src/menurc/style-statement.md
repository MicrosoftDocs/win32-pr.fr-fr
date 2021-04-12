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
ms.openlocfilehash: 67cd8f6af4a6baa2f36b66855cbe9faa2b0e5120
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381895"
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

Pour obtenir la liste des styles de fenêtre, consultez [styles de fenêtre](/windows/desktop/winmsg/window-styles). Pour obtenir la liste des styles de boîte de dialogue, consultez [styles de modèle](../dlgbox/about-dialog-boxes.md)de boîte de dialogue. Si vous utilisez les valeurs de style de la fenêtre ou de la boîte de dialogue, vous devez inclure Windows. h.

 

 