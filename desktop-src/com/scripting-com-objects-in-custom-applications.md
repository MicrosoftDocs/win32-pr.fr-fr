---
title: Écriture de scripts d’objets COM dans des applications personnalisées
description: Écriture de scripts d’objets COM dans des applications personnalisées
ms.assetid: 14e8cd53-e2b2-4393-8961-32efdf269f76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9fb24c9e1df0cded5d648be70f8ae2582a54517b8b7eda35d1b972e44ca6c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119372889"
---
# <a name="scripting-com-objects-in-custom-applications"></a>Écriture de scripts d’objets COM dans des applications personnalisées

Microsoft fournit plusieurs environnements pour l’écriture de scripts d’objets COM : Active Server Pages, Windows l’hôte de script, etc. Les éditeurs de logiciels indépendants (ISV) peuvent également accorder des licences aux moteurs de script Microsoft pour les utiliser dans leurs applications. Par exemple, un ISV qui crée un traitement de texte peut vouloir ajouter un langage de macro à l’application afin que les utilisateurs puissent automatiser des tâches simples. en accordant une licence à un moteur de script, l’ISV peut utiliser un langage tel que VBScript ou JScript comme langage de macro de l’application.

en plus de la gestion des licences VBScript et des moteurs de script JScript, les éditeurs de logiciels indépendants peuvent écrire leurs propres moteurs de script ActiveX. ces moteurs de script peuvent ensuite être connectés à n’importe quel environnement hôte qui prend en charge le moteur de script ActiveX standard. Par exemple, un éditeur de logiciels peut écrire un moteur de script PerlScript et l’installer sur un serveur ASP, ce qui permet au serveur ASP de traiter les scripts PerlScript.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture de scripts avec des objets COM](scripting-with-com-objects.md)
</dt> </dl>

 

 




