---
description: Macros Assert et Breakpoint
ms.assetid: c34db182-1f65-4a2f-9534-268638c2502d
title: Macros Assert et Breakpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4771fb7e302ec9e1093fca82d7842212e0b68e2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109734"
---
# <a name="assert-and-breakpoint-macros"></a>Macros Assert et Breakpoint

Les [classes de base DirectShow](directshow-base-classes.md) fournissent plusieurs macros qui effectuent des assertions ou génèrent des points d’arrêt.



| Macro                                        | Description                                                                                                                        |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**ASSERT**](assert.md)                     | Évalue une expression et affiche un message de diagnostic si l’expression a la **valeur false**.                                         |
| [**DbgAssertAligned**](dbgassertaligned.md) | Teste si un pointeur est aligné sur une limite spécifiée.                                                                        |
| [**DbgBreak**](dbgbreak.md)                 | Affiche une boîte de message avec la chaîne spécifiée, le nom du fichier source et le numéro de ligne.                                |
| [**EXÉCUTER une \_ assertion**](execute-assert.md)    | Évalue une expression dans les builds de débogage et de vente au détail. Dans les versions Debug, affiche un message de diagnostic si l’expression a la **valeur false**. |
| [**KASSERT**](kassert.md)                   | Évalue une expression et provoque une exception de point d’arrêt si l’expression est **false**.                                         |
| [**KDbgBreak**](kdbgbreak.md)               | Provoque une exception de point d’arrêt et journalise la chaîne spécifiée.                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilitaires de débogage](debugging-utilities.md)
</dt> </dl>

 

 



