---
title: IAgentCharacter MoveTo
description: IAgentCharacter MoveTo
ms.assetid: 4e24d2f8-1df2-47ca-a1e9-b9d29708207d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00ea5a0e288e4b7d9782f1b463fdbcccf01b0da9314894be1a60c556392e25e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848539"
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


 

 