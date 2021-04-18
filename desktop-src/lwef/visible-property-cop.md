---
title: Visible, propriété (objet Command)
description: Propriété visible
ms.assetid: 80137e16-4646-4251-b1c0-bca39ff7a233
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feaa6603812bf0938e6639021eb0f8660382af37
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106511917"
---
# <a name="visible-property-command-object"></a>Visible, propriété (objet Command)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit une valeur indiquant si la [**commande**](/windows/desktop/lwef/the-command-object) est visible dans le menu contextuel du caractère.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Stockéesyntaxe** 
</dt> <dd>

*agent ***. Caractères (**«* CharacterID *»**). Commandes (**«* name *» * *).* *  \[  =  *Valeur booléenne* visible\]



| Partie      | Description                                                                                                                                                                                                                                      |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expression booléenne spécifiant si la légende de la [**commande**](/windows/desktop/lwef/the-command-object)s’affiche dans le menu contextuel du caractère.<br/> **True** (valeur par défaut) la légende s’affiche.<br/> **Valeur false** La légende n’apparaît pas.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Affectez à cette propriété la **valeur false** lorsque vous souhaitez inclure une entrée vocale pour vos propres interfaces sans les faire apparaître dans le menu contextuel du caractère. Si vous définissez la propriété [**Caption**](caption-property.md) d’un objet [**Command**](/windows/desktop/lwef/the-command-object) sur la chaîne vide (""), le texte de légende n’apparaît pas dans le menu contextuel (par exemple, une ligne vide), quel que soit son paramètre de propriété [**visible**](visible-property.md) .

Le paramètre de propriété [**visible**](visible-property.md) de la collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) parent d’un objet de [**commande**](/windows/desktop/lwef/the-command-object) n’affecte pas le paramètre de propriété **visible** de la **commande**.

 

