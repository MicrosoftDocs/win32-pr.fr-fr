---
title: IAgentCommandsEx SetHelpContextID
description: IAgentCommandsEx SetHelpContextID
ms.assetid: b49d8184-f8dd-4359-9d45-3f038af18da5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14ed692185adbd60a73085b367b30b14fb646ab6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725924"
---
# <a name="iagentcommandsexsethelpcontextid"></a>IAgentCommandsEx::SetHelpContextID

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

Définit la [**HelpContextID**](helpcontextid-property.md) pour un objet [**Command**](/windows/desktop/lwef/the-command-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*
</dt> <dd>

Numéro de contexte de la rubrique d’aide associée à l’objet de [**commande**](/windows/desktop/lwef/the-command-object) . utilisé pour fournir une aide contextuelle pour la commande.

</dd> </dl>

Si vous avez créé un fichier d’aide Windows pour votre application et que vous l’avez défini dans la propriété [**HelpFile**](helpfile-property.md) du caractère. L’agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **true** et que l’utilisateur sélectionne la commande. S’il existe un numéro de contexte dans le [**HelpContextID**](helpcontextid-property.md), l’agent appelle l’aide et recherche la rubrique identifiée par le numéro de contexte actuel. Le nombre de contextes actuels est la valeur de **HelpContextID** pour la commande. S’il existe un numéro de contexte dans la propriété **HelpContextID** de la commande sélectionnée, help affiche une rubrique correspondant au contexte d’aide actuel. Sinon, elle affiche « aucune rubrique d’aide associée à cet élément ».

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

> [!Note]  
> La génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.

 

## <a name="see-also"></a>Voir aussi

[**IAgentCommandsEx :: GetHelpContextID**](iagentcommandsex--gethelpcontextid.md), [**IAgentCharacterEx :: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx :: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 