---
description: Lorsque l’application traite des mots entiers, les positions valides pour le signe insertion sont marquées par la valeur du membre fWordStop de la \_ structure script LOGATTR. Cette valeur est récupérée en effectuant un appel à ScriptBreak.
ms.assetid: c9bbfb51-727a-45ff-8450-774bc106f9f7
title: Utilisation des points d’arrêt de mot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9cf68d5c90b6e93a6e6f15706ec357c7a33b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210932"
---
# <a name="using-word-break-points"></a>Utilisation des points d’arrêt de mot

Lorsque l’application traite des mots entiers, les positions valides pour le signe insertion sont marquées par la valeur du membre **fWordStop** de la structure [**script \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) . Cette valeur est récupérée en effectuant un appel à [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).

Les positions valides pour les sauts de ligne entre les mots sont marquées par la valeur **fSoftBreak** récupérée par [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



