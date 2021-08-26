---
title: Propriété Enabled (objet AudioOutput)
description: En savoir plus sur la propriété d’objet AudioOutput activée. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: 6526f249-be13-4732-b79e-a9952489461f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 515b7148acf65d98b0ec8b5a5f324e5bfd9dccd10c874e165adfa2d0de9442ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963039"
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

## <a name="remarks"></a>Remarques

Cette propriété reflète l’option lire l’audio en sortie dans la page sortie de la feuille de propriétés de l’agent (options des caractères avancés). Lorsque la propriété [**Enabled**](enabled-property.md) retourne la **valeur true**, la méthode [**Speak**](speak-method.md) produit une sortie audio si un moteur TTS compatible est installé ou si vous utilisez des fichiers son pour la sortie parlée. Quand elle retourne **false**, cela signifie que la sortie vocale n’est pas installée ou a été désactivée par l’utilisateur. Le paramètre de propriété s’applique à tous les caractères de l’agent et est en lecture seule ; seul l’utilisateur peut définir cette valeur de propriété.

## <a name="see-also"></a>Voir aussi

[Événement AgentPropertyChange](agentpropertychange-event.md)


 

 




