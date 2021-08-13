---
title: IAgentCommandEx SetHelpContextID
description: IAgentCommandEx SetHelpContextID
ms.assetid: 861d55dc-f584-495c-a148-016af8f7a3e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6b876276d42ff07081b60194e90beff3ad9ef19fec383c50d70a551e1c9a5e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750188"
---
# <a name="iagentcommandexsethelpcontextid"></a>IAgentCommandEx::SetHelpContextID

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT SetHelpContextID(
   long ulID  //  ID for help topic
);
```

Définit la [**HelpContextID**](helpcontextid-property-com.md) pour un objet [**Command**](/windows/desktop/lwef/the-command-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*
</dt> <dd>

Numéro de contexte de la rubrique d’aide associée à l’objet de [**commande**](/windows/desktop/lwef/the-command-object) . utilisé pour fournir une aide contextuelle pour la commande.

</dd> </dl>

si vous avez créé un fichier d’aide Windows pour votre application et que vous l’avez défini dans la propriété [**HelpFile**](helpfile-property.md) du caractère. Microsoft agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **true** et que l’utilisateur sélectionne la commande. S’il existe un numéro de contexte dans le [**HelpContextID**](helpcontextid-property-com.md), l’agent appelle l’aide et recherche la rubrique identifiée par le numéro de contexte actuel. Le nombre de contextes actuels est la valeur de **HelpContextID** pour la commande.

> [!Note]  
> la génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.

 

## <a name="see-also"></a>Voir aussi

[**IAgentCommandEx :: GetHelpContextID**](iagentcommandex--gethelpcontextid.md), [**IAgentCharacterEx :: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx :: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 