---
title: IAgentCommandsEx GetFontSize
description: IAgentCommandsEx GetFontSize
ms.assetid: 8173e026-d28f-43d8-a8b4-96d1d97a8b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92f2ce1908ea5f37d24fb8a085204917440f61ae30feb1e596639d0240c353d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976269"
---
# <a name="iagentcommandsexgetfontsize"></a>IAgentCommandsEx::GetFontSize

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in character's pop-up menu
```

Récupère la valeur de la taille de la police affichée dans le menu contextuel du caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*
</dt> <dd>

Adresse d’une valeur qui reçoit la taille de la police.

</dd> </dl>

La taille en points de la police retournée correspond à la taille définie pour afficher le texte dans le menu contextuel du caractère lorsque votre client est en entrée-actif. La valeur par défaut du paramètre de police est basée sur le paramètre de police de menu pour le paramètre ID de langue du caractère ou, si elle n’est pas définie, sur le paramètre de langue par défaut de l’utilisateur.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

## <a name="see-also"></a>Voir aussi

[**IAgentCommandsEx :: SetFontSize**](iagentcommandsex--setfontsize.md), [ **IAgentCommandsEx :: SetFontName**](iagentcommandsex--setfontname.md)


 

 




