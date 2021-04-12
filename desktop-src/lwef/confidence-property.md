---
title: Propriété confidence
description: Propriété confidence
ms.assetid: 28a57970-4649-4a9a-9fb2-bf3f0b2f54ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa004e5690c534b7467c293d26cdf60f327dcfb
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104381817"
---
# <a name="confidence-property"></a>Propriété confidence

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit une valeur indiquant si la **confiance** du client s’affiche dans l’info-bulle d’écoute.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («*** CharacterID ***»). Commandes («*** name ***»)**. * ** *  \[  =  *numéro* de confiance\]



| Partie     | Description                                                                                                                        |
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| *Nombre* | Expression numérique qui prend la valeur d’un entier long qui identifie la valeur de confiance de la [**commande**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Si la valeur de confiance renvoyée pour la meilleure correspondance (UserInput. Confidence) ne dépasse pas la valeur que vous définissez pour la propriété **confidence** , le texte fourni dans [**ConfidenceText**](confidencetext-property.md) est affiché dans le Conseil d’écoute.

 

 