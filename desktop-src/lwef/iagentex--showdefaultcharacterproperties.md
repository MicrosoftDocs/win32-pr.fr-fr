---
title: IAgentEx ShowDefaultCharacterProperties
description: IAgentEx ShowDefaultCharacterProperties
ms.assetid: 4817b52a-7168-4008-9cda-0b8d598daea0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65436135d9763f1cb75db6fb92b9e5f0672e17a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104463115"
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
> Pour Windows 2000, il peut être nécessaire d’appeler la nouvelle API [**AllowSetForegroundWindow**](/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow) pour vous assurer que cette fenêtre devient la fenêtre de premier plan. Pour plus d’informations sur la définition de la fenêtre de premier plan sous Windows 2000, consultez la documentation du kit de développement Platform SDK.

 

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentNotifySinkEx ::D efaultCharacterChange**](iagentnotifysinkex--defaultcharacterchange.md)


 

 