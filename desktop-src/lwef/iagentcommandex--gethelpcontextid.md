---
title: IAgentCommandEx GetHelpContextID
description: IAgentCommandEx GetHelpContextID
ms.assetid: 97b390f3-ab24-4c09-aa87-d76076eba995
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d80f259b10adbdd1460f319b6fda4e5097c11136a5bf7ffde00a11d40a99656a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750185"
---
# <a name="iagentcommandexgethelpcontextid"></a>IAgentCommandEx::GetHelpContextID

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetHelpContextID(
   long * pulID  //  address of command's help topic ID
);
```

Récupère le [**HelpContextID**](helpcontextid-property-com.md) pour un objet [**Command**](/windows/desktop/lwef/the-command-object) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pulID"></span><span id="pulid"></span><span id="PULID"></span>*pulID*
</dt> <dd>

Adresse d’une variable qui reçoit le numéro de contexte de la rubrique d’aide associée à l’objet de [**commande**](/windows/desktop/lwef/the-command-object) .

</dd> </dl>

si vous avez créé un fichier d’aide Windows pour votre application et défini la propriété [**HelpFile**](helpfile-property.md) de votre caractère sur ce fichier, Microsoft Agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **True** et que l’utilisateur sélectionne la commande. S’il existe un numéro de contexte dans le [**HelpContextID**](helpcontextid-property-com.md), l’agent appelle l’aide et recherche la rubrique identifiée par le numéro de contexte actuel. Le nombre de contextes actuels est la valeur de **HelpContextID** pour la commande.

> [!Note]  
> la génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.

 

## <a name="see-also"></a>Voir aussi

[**IAgentCommandEx :: SetHelpContextID**](iagentcommandex--sethelpcontextid.md), [**IAgentCharacterEx :: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx :: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 