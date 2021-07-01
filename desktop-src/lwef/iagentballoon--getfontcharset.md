---
title: IAgentBalloon GetFontCharSet
description: IAgentBalloon GetFontCharSet
ms.assetid: 1ab5767a-31e3-449c-b242-f20b11336ca0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f809fbd83e44259c96184c9f364a85151ec9ddde
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120404"
---
# <a name="iagentballoongetfontcharset"></a>IAgentBalloon::GetFontCharSet

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetFontCharSet(
   short * psFontCharSet  // character set displayed in word balloon
); 
```

Indique le jeu de caractères de la police affichée dans une bulle de mot.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="psFontCharSet"></span><span id="psfontcharset"></span><span id="PSFONTCHARSET"></span>*psFontCharSet*
</dt> <dd>

Adresse d’une valeur qui reçoit le jeu de caractères de la police. Voici quelques paramètres courants pour la valeur :



| Value    | Jeu de caractères                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| 0   | Caractères Windows standard (ANSI).                                                    |
| 1   | Jeu de caractères par défaut.                                                                 |
| 2   | Jeu de caractères de symbole.                                                              |
| 128 | Jeu de caractères codés sur deux octets (DBCS) propre à la version japonaise de Windows.            |
| 129 | Jeu de caractères codés sur deux octets (DBCS) propre à la version coréenne de Windows.              |
| 134 | Jeu de caractères codés sur deux octets (DBCS) propre à la version de Windows en chinois simplifié.  |
| 136 | Jeu de caractères codés sur deux octets (DBCS) propre à la version de Windows en chinois traditionnel. |
| 255 | Les caractères étendus sont généralement affichés par les applications MS-DOS.                          |



 

</dd> </dl>

Pour les autres valeurs de jeu de caractères, consultez la documentation du kit de développement Platform SDK.

Le jeu de caractères par défaut utilisé dans la bulle de texte d’un caractère est défini dans l’éditeur de caractères Microsoft Agent. Vous pouvez le modifier à l’aide de [**IAgentBalloon :: SetFontCharSet**](iagentballoon--setfontcharset.md). Toutefois, l’utilisateur peut remplacer le paramètre de jeu de caractères pour tous les caractères à l’aide de la feuille de propriétés de l’agent Microsoft.

## <a name="see-also"></a>Voir aussi

[**IAgentBalloon::SetFontCharSet**](iagentballoon--setfontcharset.md)


 

 




