---
description: 'Pour qu’une application Tablet PC fonctionne avec l’encre de manière efficace, cette application doit être en mesure d’effectuer les opérations suivantes :'
ms.assetid: 64a7b773-35c9-42f7-aec4-7fed34fa84d9
title: Scénarios d’interopérabilité importants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6dca3bcbf52d673131122615fa5a08317dbf10c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515981"
---
# <a name="important-interoperability-scenarios"></a>Scénarios d’interopérabilité importants

Pour qu’une application Tablet PC fonctionne avec l’encre de manière efficace, cette application doit être en mesure d’effectuer les opérations suivantes :

-   Enregistrez un document au format binaire natif de l’application sans perdre l’encre du document.
-   Enregistrez un document dans n’importe quel format que l’application prend normalement en charge (par exemple, au format HTML ou RTF) sans perdre l’encre du document.
-   Copiez l’encre d’une application vers une autre à l’aide du presse-papiers. Cela fonctionne si l’autre application reconnaît uniquement un format spécifique, tel que HTML, RTF ou bitmap (BMP). Il fonctionne également si l’application de destination reconnaît l’encre. S’il reconnaît l’encre, l’application de destination est en mesure d’interpréter l’encre qui a été copiée en tant qu’entrée manuscrite, et pas seulement comme une image.
-   Copiez l’encre, avec du texte, entre deux applications qui reconnaissent l’encre, chacune ayant plusieurs objets [**Ink**](inkdisp-class.md) . Cela requiert HTML, RTF ou un format similaire.
-   Copiez l’encre entre deux applications, chacune ayant un objet [**Ink**](inkdisp-class.md) . Le format ISF (Ink Serialized Format) est suffisant pour cela.
-   Copiez l’encre d’une application qui a plusieurs objets [**Ink**](inkdisp-class.md) vers une application qui n’a qu’un seul objet **Ink** . Dans ce cas, l’application qui possède plusieurs objets **Ink** doit pouvoir produire du format ISF (Ink Serialized Format).
-   Copiez l’encre d’une application qui a un objet [**Ink**](inkdisp-class.md) vers une application qui a plusieurs objets **Ink** . Dans ce cas, l’application qui a plusieurs objets **Ink** doit pouvoir reconnaître ISF.

 

 



