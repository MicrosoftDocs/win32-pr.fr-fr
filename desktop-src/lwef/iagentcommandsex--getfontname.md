---
title: IAgentCommandsEx GetFontName
description: IAgentCommandsEx GetFontName
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 757b2d7554f1efcee27a519b9df61b4601a237b557c3aa26b6575864144a2850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105235"
---
# <a name="iagentcommandsexgetfontname"></a>IAgentCommandsEx::GetFontName

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in character's pop-up menu
```

Récupère la valeur de la police affichée dans le menu contextuel du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*
</dt> <dd>

Adresse d’un BSTR qui reçoit le nom de la police affiché dans le menu contextuel du caractère.

</dd> </dl>

Le nom de police retourné correspond à la police utilisée pour afficher le texte dans le menu contextuel du caractère lorsque votre application cliente est en entrée active. La valeur par défaut du paramètre de police est basée sur le paramètre de police de menu pour le paramètre ID de langue du caractère ou, si elle n’est pas définie, sur le paramètre ID de langue par défaut de l’utilisateur.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

## <a name="see-also"></a>Voir aussi

[**IAgentCommandsEx :: SetFontName**](iagentcommandsex--setfontname.md), [ **IAgentCommandsEx :: SetFontSize**](iagentcommandsex--setfontsize.md)


 

 




