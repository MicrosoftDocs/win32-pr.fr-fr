---
title: IAgentCharacterEx GetHelpContextID
description: IAgentCharacterEx GetHelpContextID
ms.assetid: 9dec5b0c-4758-4859-9aa6-6db3ef0d6b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3a64de0f4373bcaa890156ec88595d066aae9ae84b5b242fe62ffae10479d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750794"
---
# <a name="iagentcharacterexgethelpcontextid"></a>IAgentCharacterEx::GetHelpContextID

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of character's help topic ID
);
```

Récupère le [**HelpContextID**](helpcontextid-property.md) pour le caractère.

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*
</dt> <dd>

Adresse d’une variable qui reçoit le numéro de contexte de la rubrique d’aide pour le caractère.

</dd> </dl>

si vous avez créé un fichier d’aide Windows pour votre application et défini la propriété [**HelpFile**](helpfile-property.md) du caractère, Microsoft Agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **True** et que l’utilisateur sélectionne le caractère. S’il existe un numéro de contexte dans le [**HelpContextID**](helpcontextid-property.md), l’agent appelle l’aide et recherche la rubrique identifiée par le numéro de contexte actuel. Le nombre de contextes actuels est la valeur de **HelpContextID** pour le caractère.

**IAgentCharacterEx :: GetHelpContextID** retourne le [**HelpContextID**](helpcontextid-property.md) que vous définissez pour le caractère. Elle ne retourne pas la valeur **HelpContextID** définie par d’autres clients.

> [!Note]  
> la génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.

 

## <a name="see-also"></a>Voir aussi

[**IAgentCharacterEx :: SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCharacterEx :: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx :: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 




