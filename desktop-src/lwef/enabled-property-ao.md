---
title: Propriété Enabled (objet AudioOutput)
description: Propriété activée
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dff9153a1aa7a6bf5346d46f43f80bf48809c9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032258"
---
# <a name="enabled-property-audiooutput-object"></a>Propriété Enabled (objet AudioOutput)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne une valeur booléenne indiquant si la sortie audio (parlée) est activée.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent * * *. AudioOutput. Enabled**



| Valeur     | Description                               |
|-----------|-------------------------------------------|
| **True**  | Valeurs La sortie audio parlée est activée. |
| **False** | La sortie audio parlée est désactivée.          |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Cette propriété reflète l’option lire l’audio en sortie dans la page sortie de la feuille de propriétés de l’agent (options des caractères avancés). Lorsque la propriété [**Enabled**](enabled-property.md) retourne la **valeur true**, la méthode [**Speak**](speak-method.md) produit une sortie audio si un moteur TTS compatible est installé ou si vous utilisez des fichiers son pour la sortie parlée. Quand elle retourne **false**, cela signifie que la sortie vocale n’est pas installée ou a été désactivée par l’utilisateur. Le paramètre de propriété s’applique à tous les caractères de l’agent et est en lecture seule ; seul l’utilisateur peut définir cette valeur de propriété.

## <a name="see-also"></a>Voir aussi

[Événement AgentPropertyChange](agentpropertychange-event.md)


 

 




