---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6202aa144d13c3c7435be03721a3f8fd4878b93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517975"
---
# <a name="iagentballoonsetfontcharset"></a>IAgentBalloon::SetFontCharSet

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetFontCharSet(
   short sFontCharSet  // character set displayed in word balloon
); 
```

Définit le jeu de caractères de la police affichée dans la bulle de mot.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="sFontCharSet"></span><span id="sfontcharset"></span><span id="SFONTCHARSET"></span>*sFontCharSet*
</dt> <dd>

Jeu de caractères de la police. Voici quelques paramètres courants pour la valeur :



|     |                                                                                        |
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

Le jeu de caractères par défaut utilisé dans la bulle de texte d’un caractère est défini dans l’éditeur de caractères Microsoft Agent. Vous pouvez le modifier avec [**IAgentBalloon :: SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**). Toutefois, l’utilisateur peut remplacer le paramètre de jeu de caractères pour tous les caractères à l’aide de la feuille de propriétés de l’agent Microsoft. Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

## <a name="see-also"></a>Voir aussi

[**IAgentBalloon::GetFontCharSet**](iagentballoon--getfontcharset.md)


 

 




