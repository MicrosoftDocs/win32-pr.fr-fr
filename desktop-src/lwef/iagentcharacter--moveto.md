---
title: IAgentCharacter MoveTo
description: IAgentCharacter MoveTo
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86d1ba423dc637895216ff03e2adec2862bbf27d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031115"
---
# <a name="iagentcharactermoveto"></a>IAgentCharacter :: MoveTo

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT MoveTo(
   short x,         // x-coordinate of new location
   short y,         // y-coordinate of new location
   long lSpeed,     // speed to move the character
   long * pdwReqID  // address of request ID
);
```

Lit l’animation d’état **mobile** associée et déplace le cadre de caractère vers l’emplacement spécifié.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi. Lorsque la fonction retourne, cette variable contient l’ID de la demande.

<dl> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Coordonnée x de la nouvelle position, en pixels, par rapport à l’origine de l’écran (en haut à gauche). L’emplacement d’un caractère est basé sur l’angle supérieur gauche de son cadre d’animation.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordonnée y de la nouvelle position, en pixels, par rapport à l’origine de l’écran (en haut à gauche). L’emplacement d’un caractère est basé sur l’angle supérieur gauche de son cadre d’animation.

</dd> <dt>

<span id="lSpeed"></span><span id="lspeed"></span><span id="LSPEED"></span>*lSpeed*
</dt> <dd>

Paramètre spécifiant, en millisecondes, la vitesse de déplacement du cadre du caractère. La valeur recommandée est 1000. Si vous spécifiez zéro (0), le frame est déplacé sans qu’une animation ne soit lue.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Adresse d’une variable qui reçoit l’ID de requête [**MoveTo**](https://www.bing.com/search?q=**MoveTo**) .

</dd> </dl>

Lorsque vous utilisez le protocole HTTP pour accéder aux données de caractères et d’animation, utilisez la méthode [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) pour garantir la disponibilité des animations d’état **mobile** avant d’appeler cette méthode. Même si l’animation n’est pas chargée, le serveur déplace toujours le frame.

## <a name="see-also"></a>Voir aussi

[**IAgentCharacter :: SetPosition**](iagentcharacter--setposition.md)


 

 