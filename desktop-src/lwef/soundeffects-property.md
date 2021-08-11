---
title: Propriété SoundEffects
description: Propriété SoundEffects
ms.assetid: 39e48e5f-b24e-48ce-b5a3-85467ac252e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3894782ec3a038831f7bab7d6d5fe0701936baf1c1add136ad5c2c3446f78867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246255"
---
# <a name="soundeffects-property"></a>Propriété SoundEffects

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne une valeur booléenne indiquant si les effets sonores (. WAV) configurés dans le cadre des actions d’un caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent * * *. AudioOutput.SoundEffects**



| Valeur     | Description                          |
|-----------|--------------------------------------|
| **True**  | Les effets sonores des caractères sont activés. |
| **False** | L’effet sonore des caractères est désactivé. |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Cette propriété reflète l’option lire les effets sonores des caractères sur la page sortie de la feuille de propriétés de l’agent (options des caractères avancés). Lorsque la propriété **SoundEffects** retourne la **valeur true**, les effets sonores inclus dans la définition d’un caractère sont joués. Lorsque la **valeur est false**, les effets sonores ne sont pas joués. Le paramètre de propriété affecte tous les caractères et est en lecture seule ; seul l’utilisateur peut définir cette valeur de propriété.

## <a name="see-also"></a>Voir aussi

[**Événement AgentPropertyChange**](agentpropertychange-event.md)


 

 




