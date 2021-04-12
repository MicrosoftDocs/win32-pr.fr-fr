---
title: Propriété ConfidenceText
description: Propriété ConfidenceText
ms.assetid: ff856af7-c5ad-4970-8778-b59a76c5e276
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb30b5ac481b6011d3575ab99dbc389f426b085d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381880"
---
# <a name="confidencetext-property"></a>Propriété ConfidenceText

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit le **ConfidenceText** du client qui apparaît dans l’info-bulle d’écoute.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

* agent ***. Caractères («*** CharacterID ***»). Commandes («*** name ***»)**.  \[ ConfidenceText  =  *chaîne*\]



| Partie     | Description                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| *string* | Expression de chaîne qui prend la valeur du texte de **ConfidenceText** pour la [**commande**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Lorsque la valeur de confiance renvoyée pour la meilleure correspondance (UserInput. Confidence) ne dépasse pas le paramètre de [**confiance**](confidence-property.md) , le serveur affiche le texte fourni dans **ConfidenceText** dans le Conseil d’écoute.

 

 