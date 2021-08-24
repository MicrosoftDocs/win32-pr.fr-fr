---
title: Propriété Enabled (objet Command)
description: En savoir plus sur la propriété de l’objet de commande activé. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a3d8b77833da20c4a0b4254d4ce3432ff20d2f9b18a1da877adc9664bbff6c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726059"
---
# <a name="enabled-property-command-object"></a>Propriété Enabled (objet Command)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit une valeur indiquant si la **commande** est activée dans le menu contextuel du caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»). Commandes («_*_nom_*_»)._ *  \[  =  *Valeur booléenne* activée\]



| Partie      | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expression booléenne spécifiant si la **commande** est activée.<br/> <dl> <dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**Vrai**</dt> <dd> La **commande** est activée.<br/> </dd> <dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**Faux**</dt> <dd> La **commande** est désactivée.<br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Si la propriété [**Enabled**](enabled-property.md) a la valeur **true**, la légende de l’objet de [**commande**](/windows/desktop/lwef/the-command-object) apparaît comme texte normal dans le menu contextuel du caractère lorsque l’application cliente est en entrée-active. Si la propriété **Enabled** a la **valeur false**, la légende apparaît comme texte non disponible (désactivé). Une **commande** désactivée n’est pas non plus accessible pour une entrée vocale.

 

