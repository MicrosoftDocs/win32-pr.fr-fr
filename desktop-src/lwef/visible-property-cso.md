---
title: Visible, propriété (objet Commands)
description: Propriété visible
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eaba059a375c23569195ddaea82e6d03cb943ec
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383739"
---
# <a name="visible-property-commands-object"></a>Visible, propriété (objet Commands)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit une valeur qui détermine si la légende de la collection de [**commandes**](/windows/desktop/lwef/the-commands-collection-object) s’affiche dans le menu contextuel du caractère.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Stockéesyntaxe** 
</dt> <dd>

*agent ***. Caractères (**"* CharacterID *" * *). Commands.* *  \[  =  *valeur booléenne* visible\]



| Partie      | Description                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expression booléenne spécifiant si votre objet [**Commands**](/windows/desktop/lwef/the-commands-collection-object) s’affiche dans le menu contextuel du caractère. <br/> **True** La légende s’affiche.<br/> **Valeur false** La légende n’apparaît pas.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Pour que la légende apparaisse dans le menu contextuel du caractère lorsque votre application n’est pas le client d’entrée-actif, cette propriété doit avoir la valeur **true** et la propriété [**Caption**](caption-property.md) définie pour votre collection de commandes. De plus, cette propriété doit avoir la valeur **true** pour que les commandes de votre collection s’affichent dans le menu contextuel lorsque votre application est en entrée active.

 

