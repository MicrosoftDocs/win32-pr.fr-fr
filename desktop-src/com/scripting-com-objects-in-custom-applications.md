---
title: Écriture de scripts d’objets COM dans des applications personnalisées
description: Écriture de scripts d’objets COM dans des applications personnalisées
ms.assetid: 14e8cd53-e2b2-4393-8961-32efdf269f76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31d16938747755dfb0c08907430837de5a1106ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196663"
---
# <a name="scripting-com-objects-in-custom-applications"></a>Écriture de scripts d’objets COM dans des applications personnalisées

Microsoft fournit plusieurs environnements pour l’écriture de scripts d’objets COM : Active Server pages, Windows Script Host, etc. Les éditeurs de logiciels indépendants (ISV) peuvent également accorder des licences aux moteurs de script Microsoft pour les utiliser dans leurs applications. Par exemple, un ISV qui crée un traitement de texte peut vouloir ajouter un langage de macro à l’application afin que les utilisateurs puissent automatiser des tâches simples. En accordant une licence à un moteur de script, l’ISV peut utiliser un langage tel que VBScript ou JScript comme langage de macro de l’application.

Outre les moteurs de script VBScript et JScript, les éditeurs de logiciels indépendants peuvent écrire leurs propres moteurs de script ActiveX. Ces moteurs de script peuvent ensuite être connectés à n’importe quel environnement hôte qui prend en charge le moteur de script ActiveX standard. Par exemple, un éditeur de logiciels peut écrire un moteur de script PerlScript et l’installer sur un serveur ASP, ce qui permet au serveur ASP de traiter les scripts PerlScript.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture de scripts avec des objets COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




