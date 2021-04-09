---
description: .
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Mode protégé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ace82e27bbec3bb97a9ffbd3b64c9c6cee9e11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865966"
---
# <a name="protected-mode"></a>Mode protégé

La plupart des fonctionnalités de sécurité de Windows Internet Explorer 8 sont disponibles dans Internet Explorer 8 pour le système d’exploitation Windows XP avec Service Pack 2 (SP2) et les versions ultérieures. Le mode protégé est disponible uniquement pour Windows Vista ou versions ultérieures, car il est basé sur les fonctionnalités de sécurité suivantes qui sont nouvelles dans Windows Vista :

-   [Le contrôle de compte d’utilisateur (UAC)](https://msdn.microsoft.com/library/aa511445.aspx) facilite l’exécution sans privilèges d’administrateur. Lorsque les utilisateurs exécutent des programmes avec des privilèges utilisateur limités, ils sont plus sûrs contre une attaque que lorsqu’ils s’exécutent avec des privilèges d’administrateur. Le système d’exploitation Windows peut empêcher le code malveillant d’effectuer des actions nuisibles.
-   Un mécanisme d’intégrité restreint l’accès en écriture aux [objets sécurisables](../secauthz/securable-objects.md) par des processus de plus faible intégrité, de la même façon que l’appartenance aux groupes de comptes d’utilisateur restreint les droits des utilisateurs à accéder aux composants système sensibles.
-   L’isolation des privilèges de l' [interface utilisateur (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) empêche les processus d’envoyer des messages de fenêtre sélectionnés et d’autres API utilisateur aux processus qui s’exécutent avec une intégrité plus élevée.

L’infrastructure de sécurité du mécanisme d’intégrité Windows permet au mode protégé de fournir à Windows Internet Explorer les privilèges dont les utilisateurs ont besoin pour naviguer sur le Web, tout en disposant des privilèges dont les utilisateurs ont besoin pour installer des programmes en mode silencieux ou pour modifier les données système sensibles.

Les utilisateurs peuvent désactiver cette fonctionnalité par le biais d’une case à cocher, et les administrateurs peuvent la désactiver à l’aide de stratégie de groupe.

> [!IMPORTANT]
> Vous ne devez désactiver la fonctionnalité qu’en tant que mesure temporaire pendant la résolution des problèmes pour comparer le comportement de l’application lorsque celle-ci est activée ou non. Nous vous recommandons de conserver cette fonctionnalité activée de manière permanente.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
