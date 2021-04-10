---
title: Gestion des exceptions sous WOW64
description: WOW64 utilise des exceptions natives x64, ia64 ou ARM64 comme un transport pour les exceptions x86. Par conséquent, dans une application 32 bits s’exécutant sous WOW64, les exceptions non interceptées se comportent comme des exceptions 64 bits natives.
ms.assetid: 2EE1A1F3-A691-4ee6-9587-7FF7C4F9DD98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb57e56b85be4769d452a5772ff7b0024724641
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031720"
---
# <a name="exception-handling-under-wow64"></a>Gestion des exceptions sous WOW64

WOW64 utilise des exceptions natives x64, ia64 ou ARM64 comme un transport pour les exceptions x86. Par conséquent, dans une application 32 bits s’exécutant sous WOW64, les exceptions non interceptées se comportent comme des exceptions 64 bits natives.

Dans une application qui s’exécute sur une version 32 bits de Windows, les exceptions non interceptées sont transmises aux gestionnaires d’exceptions de niveau supérieur de l’application, le cas échéant. Dans la même application 32 bits qui s’exécute sous WOW64, le système peut supprimer les exceptions non interceptées.

**Windows Vista, Windows Server 2003 et Windows XP :** Dans la même application 32 bits qui s’exécute sous WOW64, le système appelle les filtres d’exception, mais peut supprimer les exceptions non interceptées sans appeler les gestionnaires associés. Ce comportement a été modifié à partir de Windows Vista avec Service Pack 1 (SP1).

Pour plus d’informations sur les exceptions non interceptées dans les procédures de fenêtre, consultez la fonction [WindowProc](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

 

 