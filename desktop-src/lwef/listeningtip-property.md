---
title: Propriété ListeningTip
description: Propriété ListeningTip
ms.assetid: 02a678bb-5eb6-495f-b339-35170a44b15e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402fd970bf902f034fd6ffb713029e3a27095c8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106543040"
---
# <a name="listeningtip-property"></a>Propriété ListeningTip

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne une valeur booléenne indiquant le paramètre de l’utilisateur actuel pour l’info-bulle d’écoute.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Stockéesyntaxe** 
</dt> <dd>

*agent * * *. SpeechInput.ListeningTip**



| Valeur     | Description                    |
|-----------|--------------------------------|
| **True**  | L’info-bulle d’écoute est activée.  |
| **False** | L’info-bulle d’écoute est désactivée. |



 

</dd> </dl>

## <a name="remarks"></a>Notes

La propriété **ListeningTip** indique si l’option Afficher l’info-bulle d’écoute dans la feuille de propriétés de l’agent Microsoft (options de caractères avancés) est activée. Quand **ListeningTip** retourne la **valeur true** et que l’entrée vocale est activée, le serveur affiche la fenêtre d’info-bulle lorsque l’utilisateur appuie sur la touche d’écoute.

## <a name="see-also"></a>Voir aussi

[**Événement AgentPropertyChange**](agentpropertychange-event.md)


 

 




