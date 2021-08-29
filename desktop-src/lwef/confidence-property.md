---
title: Propriété confidence
description: Propriété confidence
ms.assetid: 28a57970-4649-4a9a-9fb2-bf3f0b2f54ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f446136ce9711d17adf133dd205741c7812ef1360526a0a2c1c6c86442f13aac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716519"
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

*agent ***. Caractères («**_CharacterID_*_»). Commandes («_*_Name_*_»)_*. * ** *  \[  =  *numéro* de confiance\]



| Partie     | Description                                                                                                                        |
|----------|------------------------------------------------------------------------------------------------------------------------------------|
| *Nombre* | Expression numérique qui prend la valeur d’un entier long qui identifie la valeur de confiance de la [**commande**](/windows/desktop/lwef/the-command-object). |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Si la valeur de confiance renvoyée pour la meilleure correspondance (UserInput. Confidence) ne dépasse pas la valeur que vous définissez pour la propriété **confidence** , le texte fourni dans [**ConfidenceText**](confidencetext-property.md) est affiché dans le Conseil d’écoute.

 

 