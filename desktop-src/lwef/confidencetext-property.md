---
title: Propriété ConfidenceText
description: Propriété ConfidenceText
ms.assetid: ff856af7-c5ad-4970-8778-b59a76c5e276
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6612d4ade657748674fb4dd7391f447849691dcd756f2320f590c00ac33430
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963149"
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

*agent ***. Caractères («**_CharacterID_*_»). Commandes («_*_Name_*_»)_*.  \[ ConfidenceText  =  *chaîne*\]



| Partie     | Description                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------|
| *string* | Expression de chaîne qui prend la valeur du texte de **ConfidenceText** pour la [**commande**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Lorsque la valeur de confiance renvoyée pour la meilleure correspondance (UserInput. Confidence) ne dépasse pas le paramètre de [**confiance**](confidence-property.md) , le serveur affiche le texte fourni dans **ConfidenceText** dans le Conseil d’écoute.

 

 