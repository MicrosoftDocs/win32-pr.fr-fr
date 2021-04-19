---
title: IAgentPropertySheet
description: IAgentPropertySheet
ms.assetid: 09bac150-ad68-40b2-9c2c-760f6bc919e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd5e185a6e8d55d87e561f727c8dc9df8a8cfd63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510612"
---
# <a name="iagentpropertysheetgetsize"></a>IAgentPropertySheet :: est à obtenir

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetSize(
   long * plWidth,  // address of variable for property sheet width
   long * plHeight  // address of variable for property sheet height
);
```

Récupère la taille de la fenêtre de la feuille de propriétés de l’agent Microsoft.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="plWidth"></span><span id="plwidth"></span><span id="PLWIDTH"></span>*plWidth*
</dt> <dd>

Adresse d’une variable qui reçoit la largeur de la feuille de propriétés, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> <dt>

<span id="plHeight"></span><span id="plheight"></span><span id="PLHEIGHT"></span>*plHeight*
</dt> <dd>

Adresse d’une variable qui reçoit la hauteur de la feuille de propriétés, en pixels, par rapport à l’origine de l’écran (en haut à gauche).

</dd> </dl>

## <a name="see-also"></a>Voir aussi

[**IAgentPropertySheet :: GetPosition**](iagentpropertysheet--getposition.md)


 

 




