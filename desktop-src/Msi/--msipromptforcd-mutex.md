---
description: Le \_ \_ mutex MsiPromptForCD existe quand le programme d’installation invite l’utilisateur à insérer un CD-ROM.
ms.assetid: f6319cda-48ac-4351-8eb5-f326490e3aff
title: Mutex __MsiPromptForCD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba2c829cb0102192b4c2bc2670892f8849000a6ed9cad2a88e7f3e3e557b259
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764289"
---
# <a name="__msipromptforcd-mutex"></a>\_\_Mutex MsiPromptForCD

Le \_ \_ mutex MsiPromptForCD existe quand le programme d’installation invite l’utilisateur à insérer un CD-ROM. Les programmes de lecture automatique doivent vérifier que le \_ \_ mutex MsiPromptForCD n’est pas actuellement défini avant le démarrage. Notez qu’il est possible qu’une invite de CD-ROM se produise avant que la clé en cours ou le \_ mutex MSIExecute existe.

 

 



