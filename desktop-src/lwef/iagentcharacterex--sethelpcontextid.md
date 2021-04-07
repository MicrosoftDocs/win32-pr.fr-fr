---
title: IAgentCharacterEx SetHelpContextID
description: IAgentCharacterEx SetHelpContextID
ms.assetid: 218e970e-825e-441d-8947-30ec6a2845bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 500187bf04babbecf7577ff933dd0adcc53609f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672174"
---
# <a name="iagentcharacterexsethelpcontextid"></a>IAgentCharacterEx::SetHelpContextID

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

Définit la [**HelpContextID**](helpcontextid-property.md) pour le caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

Le numéro de contexte de la rubrique d’aide associée à un caractère ; utilisé pour fournir une aide contextuelle pour le caractère.

</dd> </dl>

Si vous avez créé un fichier d’aide Windows pour votre application et que vous l’avez défini dans la propriété [**HelpFile**](helpfile-property.md) du caractère, Microsoft agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **true** et que l’utilisateur sélectionne le caractère. S’il existe un numéro de contexte dans le [**HelpContextID**](helpcontextid-property.md), l’agent appelle l’aide et recherche la rubrique identifiée par le numéro de contexte actuel. Le nombre de contextes actuels est la valeur de **HelpContextID** pour le caractère. S’il existe un numéro de contexte dans la propriété **HelpContextID** , help affiche une rubrique correspondant au contexte d’aide actuel ; Sinon, elle affiche « aucune rubrique d’aide associée à cet élément ».

Ce paramètre s’applique uniquement lorsque votre application cliente est le client actif du premier caractère. Elle n’affecte pas les autres clients du caractère ou d’autres caractères que votre application cliente utilise.

> [!Note]  
> La génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.

 

## <a name="see-also"></a>Voir aussi

[**IAgentCharacterEx :: GetHelpContextID**](iagentcharacterex--gethelpcontextid.md), [**IAgentCharacterEx :: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx :: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 




