---
title: IAgentBalloon SetFontCharSet
description: IAgentBalloon SetFontCharSet
ms.assetid: ce1b152d-c8af-47ec-9e6b-5768dbcf3566
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 178e2f6e2e086962456b6717dcb6866db9d607dd16136f839a127857d85cd58e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751051"
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



| Valeur    | Jeu de caractères                                                                                       |
|-----|----------------------------------------------------------------------------------------|
| 0   | caractères de Windows Standard (ANSI).                                                    |
| 1   | Jeu de caractères par défaut.                                                                 |
| 2   | Jeu de caractères de symbole.                                                              |
| 128 | Jeu de caractères codés sur deux octets (DBCS) propre à la version japonaise de Windows.            |
| 129 | Jeu de caractères codés sur deux octets (DBCS) propre à la version coréenne de Windows.              |
| 134 | Jeu de caractères codés sur deux octets (DBCS) propre à la version en chinois simplifié de Windows.  |
| 136 | Jeu de caractères codés sur deux octets (DBCS) propre à la version en chinois traditionnel de Windows. |
| 255 | Les caractères étendus sont généralement affichés par les applications MS-DOS.                          |



 

</dd> </dl>

Pour les autres valeurs de jeu de caractères, consultez la documentation du kit de développement Platform SDK.

Le jeu de caractères par défaut utilisé dans la bulle de texte d’un caractère est défini dans l’éditeur de caractères Microsoft Agent. Vous pouvez le modifier avec [**IAgentBalloon :: SetFontCharSet**](https://www.bing.com/search?q=**IAgentBalloon::SetFontCharSet**). Toutefois, l’utilisateur peut remplacer le paramètre de jeu de caractères pour tous les caractères à l’aide de la feuille de propriétés de l’agent Microsoft. Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

## <a name="see-also"></a>Voir aussi

[**IAgentBalloon::GetFontCharSet**](iagentballoon--getfontcharset.md)


 

 




