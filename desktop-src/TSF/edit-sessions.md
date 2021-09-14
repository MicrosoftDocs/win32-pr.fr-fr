---
title: Sessions de modification
description: Lorsqu’un service de texte doit obtenir, modifier ou définir du texte dans un contexte, il doit demander une session d’édition.
ms.assetid: e4115227-1036-4892-986d-dc4cef5b178e
keywords:
- Text Services Framework (TSF), modifier la session
- TSF (Text Services Framework), modifier la session
- services de texte, modifier la session
- session d'édition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81897c3c63539626776b693a22be9096f973d02e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193532"
---
# <a name="edit-sessions"></a>Sessions de modification

Lorsqu’un service de texte doit obtenir, modifier ou définir du texte dans un contexte, il doit demander une *session d’édition*. Lorsqu’une session d’édition est demandée, le gestionnaire TSF négocie avec le propriétaire du contexte cible pour un verrou de document du type demandé. Lorsque le verrou de document est accordé, le gestionnaire de TSF permet au service de texte de lire et/ou d’écrire du texte dans le contexte.

 

 




