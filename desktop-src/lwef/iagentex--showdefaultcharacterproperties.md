---
title: IAgentEx ShowDefaultCharacterProperties
description: IAgentEx ShowDefaultCharacterProperties
ms.assetid: 4817b52a-7168-4008-9cda-0b8d598daea0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 362cffa8d4b34d70111505a60fd5eadc68a220cd45c3beb519e5e39ba62f1a81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749813"
---
# <a name="iagentexshowdefaultcharacterproperties"></a>IAgentEx::ShowDefaultCharacterProperties

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT ShowDefaultCharacterProperties(
   short x,          // x-coordinate of window
   short y,          // y-coordinate of window
   long bUseDefault  // default position flag
);
```

Affiche la fenêtre Propriétés des caractères par défaut.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Coordonnée x de la fenêtre, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordonnée y de la fenêtre, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> <dt>

<span id="bUseDefault"></span><span id="busedefault"></span><span id="BUSEDEFAULT"></span>*bUseDefault*
</dt> <dd>

Indicateur de position par défaut. Si ce paramètre a la **valeur true**, Microsoft Agent affiche la fenêtre de la feuille de propriétés pour le caractère par défaut au dernier emplacement.

> [!Note]  
> pour Windows 2000, il peut être nécessaire d’appeler la nouvelle API [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) pour vous assurer que cette fenêtre devient la fenêtre de premier plan. pour plus d’informations sur la définition de la fenêtre de premier plan sous Windows 2000, consultez la documentation du kit de développement platform SDK.

 

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentNotifySinkEx ::D efaultCharacterChange**](iagentnotifysinkex--defaultcharacterchange.md)


 

 