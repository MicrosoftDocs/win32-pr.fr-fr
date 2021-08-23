---
title: Propriété ListeningTip
description: Propriété ListeningTip
ms.assetid: 02a678bb-5eb6-495f-b339-35170a44b15e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d6a743eb26d1e2b57d106e72d77c3774938ffe7e56ca4ba4147001d74bb99f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665439"
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

## <a name="remarks"></a>Remarques

La propriété **ListeningTip** indique si l’option Afficher l’info-bulle d’écoute dans la feuille de propriétés de l’agent Microsoft (options de caractères avancés) est activée. Quand **ListeningTip** retourne la **valeur true** et que l’entrée vocale est activée, le serveur affiche la fenêtre d’info-bulle lorsque l’utilisateur appuie sur la touche d’écoute.

## <a name="see-also"></a>Voir aussi

[**Événement AgentPropertyChange**](agentpropertychange-event.md)


 

 




