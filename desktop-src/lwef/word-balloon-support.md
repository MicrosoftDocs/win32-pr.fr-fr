---
title: Prise en charge des bulles Word
description: Prise en charge des bulles Word
ms.assetid: deac032f-0480-4a0d-bc69-e26f12666bbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78316c509ece6fc8f9b0cefd50b1564a50697a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196537"
---
# <a name="word-balloon-support"></a>Prise en charge des bulles Word

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

La sortie orale peut également apparaître sous forme de texte sous la forme d’une bulle de texte animé. Cela peut être utilisé pour compléter la sortie orale d’un caractère ou comme une alternative à la sortie audio lorsque vous utilisez la méthode [**Speak**](speak-method.md) .

![Oui, bulle d’un mot principal](images/f3ballon.gif)

Vous pouvez également utiliser une bulle de mot pour communiquer ce qu’un caractère est en « pensant » à l’aide de la méthode de [**réflexion**](think-method.md) . Cela affiche le texte que vous fournissez dans une bulle toujours « pensée ». La méthode de **réflexion** diffère également de la méthode [**Speak**](speak-method.md) en ce qu’elle ne produit pas de sortie audio.

Les bulles de mots ne prennent en charge que les communications sous-titrages à partir du caractère, et non des entrées utilisateur. Par conséquent, le mot Balloon ne prend pas en charge les contrôles d’entrée. Toutefois, vous pouvez facilement fournir une entrée d’utilisateur pour un caractère, en utilisant les interfaces de votre langage de programmation ou les autres services d’entrée fournis par Microsoft Agent, tels que le menu contextuel.

Lorsque vous définissez un caractère, vous pouvez spécifier s’il faut inclure la prise en charge des bulles de mots. Toutefois, si vous utilisez un caractère qui comprend la prise en charge des bulles de mots, vous ne pouvez pas désactiver la prise en charge.

 

 




