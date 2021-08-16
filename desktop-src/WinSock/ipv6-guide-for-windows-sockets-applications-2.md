---
description: ce guide fournit les informations dont vous avez besoin pour permettre à votre application Microsoft Windows d’utiliser la nouvelle génération de protocole Internet version 6 (IPv6).
ms.assetid: 8e862eb0-2ba9-40b0-ac73-fcb0e625965e
title: Guide IPv6 pour les Applications Windows sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c52d86dfcdfa06df80dc71a3f3313de19f9201c7421a3f27f094589a6656dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741113"
---
# <a name="ipv6-guide-for-windows-sockets-applications"></a>Guide IPv6 pour les Applications Windows sockets

ce guide fournit les informations dont vous avez besoin pour permettre à votre application Microsoft Windows d’utiliser la nouvelle génération de protocole Internet version 6 (IPv6). L’ajout de la fonctionnalité IPv6 à votre application n’est pas nécessairement un processus de Portage. Le portage d’une application suggère de modifier le code pour fonctionner sur une plateforme différente, ce qui implique de laisser la plateforme précédente en arrière-plan. Ce guide est spécifiquement structuré pour aider à ajouter des fonctionnalités IPv6 à une application tout en conservant la fonctionnalité IPv4.

Ce guide décrit les problèmes liés à l’ajout de fonctionnalités IPv6, puis cible les zones de développement les plus affectées par la transition. chaque zone reçoit une explication complète des pièges à surveiller, des stratégies suggérées pour les éviter et des conseils sur la façon de tirer le meilleur parti des nouveaux éléments de programmation de [Windows sockets 2](what-s-new-for-windows-sockets-2.md) (fonctions et structures). Pour plus d’informations sur IPv6, consultez [prise en charge d’IPv6](ipv6-support-2.md).

Ce guide fournit également des exemples de code pour vous offrir une expérience pratique et des représentations visuelles des problèmes que vous pouvez rencontrer lors de la modification de vos applications. les exemples sont tirés d’exemples fonctionnels d’une application de sockets Windows simple qui ont été modifiés pour prendre en charge à la fois IPv4 et IPv6. Le code source de ces exemples fonctionnels est inclus dans son intégralité dans deux annexes à la fin de ce document : [annexe A : le code source IPv4 uniquement](appendix-a-ipv4-only-source-code-2.md) inclut le code source d’une application avant sa modification pour prendre en charge IPv6 ; [Annexe B : le code source agnostique de la version IP](appendix-b-ip-version-agnostic-source-code-2.md) fournit le code source une fois que l’application a été activée pour IPv6.

Microsoft propose un utilitaire appelé Checkv4.exe qui vous aide à trouver du code potentiellement sensible au portage dans le code de votre application et fournit également des recommandations pour les correctifs. L’utilitaire Checkv4.exe est illustré dans ce document, à l’aide de l’exemple d’application inclus dans les annexes, avec des captures d’écran présentant la sortie générée par l’utilitaire Checkv4.exe. Pour plus d’informations, consultez [utilisation de l’utilitaire de Checkv4.exe](using-the-checkv4-exe-utility-2.md).

Les domaines de programmation traités par ce guide sont les suivants :

-   [Modification des structures de données pour IPv6 Winsock appications](changing-data-structures-2.md)
-   [Appels de fonction pour les applications Winsock IPv6](function-calls-2.md)
-   [Utilisation d’adresses IPv4 codées en dur](use-of-hardcoded-ipv4-addresses-2.md)
-   [Problèmes d’interface utilisateur pour les applications Winsock IPv6](user-interface-issues-2.md)
-   [Protocoles sous-jacents pour les applications Winsock IPv6](underlying-protocols-2.md)
-   [Sockets à double pile pour les applications Winsock IPv6](dual-stack-sockets.md)

Étant donné qu’il n’existe pas de séquence d’événements uniforme, les sections qui traitent des problèmes d’activation D’ipv6 ne sont pas organisées de façon séquentielle, de sorte que vous pouvez référencer n’importe quelle section à tout moment. Il est fortement recommandé d’examiner chaque section tout en ajoutant des fonctionnalités IPv6 à votre application. Il est également recommandé de lire l’utilitaire Checkv4.exe, car il contient des conseils sur l’ordre dans lequel résoudre les problèmes d’activation d’IPv6.

Pour examiner l’utilitaire de Checkv4.exe et pour examiner l’ordre dans lequel vous devez aborder le processus de Portage dans vos applications, consultez [utilisation de l’utilitaire de Checkv4.exe](using-the-checkv4-exe-utility-2.md). Cette section contient des informations sur un indicateur de compilation qui vérifie rigoureusement les éléments de programmation incompatibles avec IPv6.

Pour accéder directement à l’exemple d’application, consultez [annexe A : code source IPv4 uniquement](appendix-a-ipv4-only-source-code-2.md) et [annexe B : code source agnostique de la version IP](appendix-b-ip-version-agnostic-source-code-2.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Protocole Internet version 6 (IPv6)](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[Prise en charge D’ipv6](ipv6-support-2.md)
</dt> <dt>

[version préliminaire de la technologie IPv6 pour Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[Utilisation de l’utilitaire Checkv4.exe](using-the-checkv4-exe-utility-2.md)
</dt> <dt>

[Annexe A : code source uniquement IPv4](appendix-a-ipv4-only-source-code-2.md)
</dt> <dt>

[Annexe B : code source agnostique de la version IP](appendix-b-ip-version-agnostic-source-code-2.md)
</dt> </dl>

 

 



