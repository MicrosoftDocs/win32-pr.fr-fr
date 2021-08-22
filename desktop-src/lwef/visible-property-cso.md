---
title: Visible, propriété (objet Commands)
description: En savoir plus sur la propriété visible de l’objet Commands, qui détermine si la légende de la collection Commands s’affiche dans le menu contextuel du caractère.
ms.assetid: 0178a789-141b-4d4c-ba7c-05c7995f13bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c742733d06f0a4c7ae2d10c7fb97a20e735b59370c61efa5f7204003f1cd81bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975469"
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

## <a name="remarks"></a>Remarques

Pour que la légende apparaisse dans le menu contextuel du caractère lorsque votre application n’est pas le client d’entrée-actif, cette propriété doit avoir la valeur **true** et la propriété [**Caption**](caption-property.md) définie pour votre collection de commandes. De plus, cette propriété doit avoir la valeur **true** pour que les commandes de votre collection s’affichent dans le menu contextuel lorsque votre application est en entrée active.

 

