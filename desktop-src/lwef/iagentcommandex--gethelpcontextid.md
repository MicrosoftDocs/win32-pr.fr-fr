---
title: IAgentCommandEx GetHelpContextID
description: IAgentCommandEx GetHelpContextID
ms.assetid: 97b390f3-ab24-4c09-aa87-d76076eba995
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f330e8ae8cd8bdaff5e27ccd00352b41b07be2b6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381933"
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

Si vous avez créé un fichier d’aide Windows pour votre application et défini la propriété [**HelpFile**](helpfile-property.md) de votre caractère sur ce fichier, Microsoft agent appelle automatiquement l’aide lorsque [**HelpModeOn**](helpmodeon-property.md) a la valeur **true** et que l’utilisateur sélectionne la commande. S’il existe un numéro de contexte dans le [**HelpContextID**](helpcontextid-property-com.md), l’agent appelle l’aide et recherche la rubrique identifiée par le numéro de contexte actuel. Le nombre de contextes actuels est la valeur de **HelpContextID** pour la commande.

> [!Note]  
> La génération d’un fichier d’aide requiert le compilateur d’aide Microsoft Windows.

 

## <a name="see-also"></a>Voir aussi

[**IAgentCommandEx :: SetHelpContextID**](iagentcommandex--sethelpcontextid.md), [**IAgentCharacterEx :: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx :: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)


 

 