---
title: IAgentCommandEx GetVoiceCaption
description: IAgentCommandEx GetVoiceCaption
ms.assetid: a81accfd-c137-4347-8ead-4ed5e7148751
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d093a971331c6c5cddf467e770dae69960ae0d616ddc9b37863a46d25becb7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105417"
---
# <a name="iagentcommandexgetvoicecaption"></a>IAgentCommandEx::GetVoiceCaption

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption text
);
```

Récupère le [**VoiceCaption**](voicecaption-property.md) pour une [**commande**](/windows/desktop/lwef/the-command-object).

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*
</dt> <dd>

Adresse d’un BSTR qui reçoit la valeur du texte de [**légende**](caption-property.md) affiché pour une [**commande**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Le [**VoiceCaption**](voicecaption-property.md) est le texte qui apparaît pour un objet [**Command**](/windows/desktop/lwef/the-command-object) dans la fenêtre commandes vocales lorsque votre application cliente est en entrée active.

## <a name="see-also"></a>Voir aussi

[**IAgentCommandEx :: SetVoiceCaption**](iagentcommandex--setvoicecaption.md), [**IAgentCommand :: SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand :: setVisible**](iagentcommand--setvisible.md), [**IAgentCommand :: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx :: Addex**](iagentcommandsex--addex.md), [**IAgentCommandsEx :: InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands :: Add**](iagentcommands--add.md), [**IAgentCommands :: Insert**](iagentcommands--insert.md)


 

 