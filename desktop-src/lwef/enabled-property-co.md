---
title: Propriété Enabled (objet Command)
description: Propriété activée
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5999e396f61fbcc820bc1cec7deb0c603eb948e4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106509490"
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

## <a name="remarks"></a>Notes

Si la propriété [**Enabled**](enabled-property.md) a la valeur **true**, la légende de l’objet de [**commande**](/windows/desktop/lwef/the-command-object) apparaît comme texte normal dans le menu contextuel du caractère lorsque l’application cliente est en entrée-active. Si la propriété **Enabled** a la **valeur false**, la légende apparaît comme texte non disponible (désactivé). Une **commande** désactivée n’est pas non plus accessible pour une entrée vocale.

 

