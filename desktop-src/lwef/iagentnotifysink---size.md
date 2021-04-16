---
title: Taille de IAgentNotifySink
description: Taille de IAgentNotifySink
ms.assetid: ef192234-bee6-4158-a5d8-4326b784e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 252ad15f6bb5201e8ec000292d1e89efe9368934
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507327"
---
# <a name="iagentnotifysinksize"></a>IAgentNotifySink :: Size

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Size(
   long dwCharID,  // character ID
   long lWidth,    // new width
   long lHeight,   // new height
);                          
```

Avertit une application cliente lorsque le caractère a été redimensionné.

-   Pas de valeur de retour.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Identificateur du caractère qui a été redimensionné.

</dd> <dt>

<span id="lWidth"></span><span id="lwidth"></span><span id="LWIDTH"></span>*lWidth*
</dt> <dd>

Largeur, en pixels, du cadre d’animation du caractère.

</dd> <dt>

<span id="lHeight"></span><span id="lheight"></span><span id="LHEIGHT"></span>*lHeight*
</dt> <dd>

Hauteur, en pixels, du cadre d’animation du caractère.

</dd> </dl>

Cet événement est envoyé à tous les clients du caractère.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter ::**](iagentcharacter--getsize.md) [ **deIAgentCharacter :: deinstalle**](iagentcharacter--setsize.md)


 

 




