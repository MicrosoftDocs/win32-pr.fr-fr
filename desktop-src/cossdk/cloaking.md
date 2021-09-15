---
description: Il existe deux ingrédients pour déterminer le comportement d’emprunt d’identité de l’autorité que le client accorde explicitement au serveur via un niveau d’emprunt d’identité et la capacité des serveurs à masquer sa propre identité lors des appels au nom des clients.
ms.assetid: b34264ff-eb6a-4b99-8c0e-ab6b969a7fb1
title: Masquage (services de composants)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e5cba98d229c7f2132a2a1c345e65900b634afe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518905"
---
# <a name="cloaking-component-services"></a>Masquage (services de composants)

Il existe deux ingrédients pour déterminer le comportement de l’emprunt d’identité : l’autorité que le client accorde explicitement au serveur via un niveau d’emprunt d’identité et la capacité du serveur à masquer sa propre identité lors des appels au nom du client. Cette dernière fonctionnalité est connue sous le nom de *masquage*. Le masquage porte sur l’identité de sécurité sous laquelle le serveur effectue des appels.

Lorsque le serveur emprunte l’identité du client, il dispose d’un accès direct aux informations d’identification de sécurité du client. Dans un sens très local, le thread serveur prend l’identité du client. Toutefois, lorsque le serveur effectue des appels en dehors de son processus, l’identité du client ne sera pas nécessairement projetée en tant qu’identité sous laquelle l’appel est effectué.

Lorsque le masquage est activé, les appels effectués par le serveur qui emprunte l’identité du client peuvent être effectués sous l’identité du client. Lorsque le masquage est désactivé, les appels par le serveur sont effectués sous l’identité du serveur.

En outre, il existe deux formes de masquage, le masquage *statique* et le *masquage dynamique*, qui peuvent être décrits comme suit :

-   Emprunt d’identité avec masquage statique. L’identité du client d’origine (réalisée en tant que jeton de thread du serveur) peut être présentée une seule fois à un serveur en aval sur un appel à l’aide de [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), en définissant l’identité du client d’origine une seule fois sur le proxy, et ce jeton de thread sera utilisé lors des appels de méthode suivants.
-   Emprunt d’identité avec masquage dynamique. L’identité du client d’origine est découverte en tant que jeton de thread du serveur sur chaque appel de méthode au serveur en aval. En effet, l’identité présentée peut être déterminée dynamiquement. La surcharge requise pour effectuer cette opération peut être considérablement plus coûteuse.

Pour les applications COM+, la configuration par défaut est pour la fonctionnalité de voilage dynamique. Cela peut être modifié par programme et administrativement. Bien que le masquage dynamique puisse avoir une surcharge des performances, il offre la flexibilité qui est généralement requise dans les circonstances qui nécessitent l’utilisation de l’emprunt d’identité en premier lieu.

Pour plus d’informations sur le masquage et les descriptions précises des comportements possibles, consultez [masquage](/windows/desktop/com/cloaking) dans la documentation com.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Emprunt d’identité et délégation du client](client-impersonation-and-delegation.md)
</dt> <dt>

[Exigences côté client pour l’emprunt d’identité](client-side-requirements-for-impersonation.md)
</dt> <dt>

[Exigences côté serveur pour l’emprunt d’identité](server-side-requirements-for-impersonation.md)
</dt> </dl>

 

 
