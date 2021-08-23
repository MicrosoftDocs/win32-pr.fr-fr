---
title: Écouter, ne pas reconnaître simplement
description: Écouter, ne pas reconnaître simplement
ms.assetid: 74bb2122-98c1-4a51-b894-93e1481aa46b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b226b9172b10c70e4e699a98df49acc002dcd5add95986c9efbdf9e8f057648d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119888089"
---
# <a name="listen-dont-just-recognize"></a>Écouter, ne pas reconnaître simplement

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

La communication réussie implique plus que la reconnaissance de mots. Le processus de dialogue implique l’échange de signaux pour la prise de vue et la compréhension des signaux. Les caractères peuvent améliorer les interfaces conversationnelles en fournissant des signaux tels que les inclinaisons de l’en-tête, les nœuds ou les secousses pour indiquer quand le moteur de reconnaissance vocale est à l’état d’écoute et quand un événement est reconnu. Par exemple, Microsoft Agent lit les animations affectées à l’état d' **écoute** lorsqu’un utilisateur appuie sur la clé d’écoute Push-to-parler et les animations affectées à l’état **auditif** lorsqu’un énoncé est détecté. Lorsque vous définissez votre propre caractère, veillez à créer et assigner des animations appropriées à ces États. Pour plus d’informations sur la conception de caractères, consultez [conception de caractères pour Microsoft Agent](designing-characters-for-microsoft-agent.md).

Outre les indications non verbales, une conversation implique un contexte commun entre les parties inversées. De même, les scénarios d’entrée vocale avec des caractères sont plus susceptibles de parvenir lorsque le contexte est bien établi. L’établissement du contexte vous permet d’améliorer l’interprétation des expressions de sons similaires telles que la « vérification du courrier » et la vérification de la messagerie. Vous pouvez également permettre à l’utilisateur d’interroger le contexte en fournissant une commande, telle que « Help » ou « WHERE AM I », à laquelle vous répondez en rappelant le contexte actuel, telle que la dernière action effectuée par votre application.

Microsoft Agent fournit des interfaces qui vous permettent d’accéder à la meilleure correspondance et aux deux meilleures alternatives retournées par le moteur de reconnaissance vocale. En outre, vous pouvez accéder aux scores de confiance pour toutes les correspondances. Vous pouvez utiliser ces informations pour mieux déterminer ce qui a été parlé. Par exemple, si les scores de confiance de la meilleure correspondance et de la première alternative sont proches, cela peut indiquer que le moteur de reconnaissance vocale a des difficultés à distinguer les différences. Dans ce cas, vous pouvez demander à l’utilisateur de répéter ou de reformuler la demande afin d’améliorer les performances. Toutefois, si la meilleure correspondance et la première ou la deuxième alternative retournent la même commande, elle renforce l’indication de la reconnaissance correcte.

La nature d’une conversation ou d’une boîte de dialogue implique qu’il doit y avoir une réponse à une entrée parlée. Par conséquent, l’entrée d’un utilisateur doit toujours répondre à une rétroaction orale ou visuel qui indique qu’une action a été effectuée ou qu’un problème a été rencontré, ou fournit une réponse appropriée.

 

 




