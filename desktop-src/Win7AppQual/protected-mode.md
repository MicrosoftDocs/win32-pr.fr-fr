---
description: Mode protégé
ms.assetid: 88810916-A85E-4EC7-A6AE-1CA2A2205DBC
title: Mode protégé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc1b8b1e6931ed83ec59ccfe4c3c63d8e5b5eed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414547"
---
# <a name="protected-mode"></a>Mode protégé

la plupart des Windows fonctionnalités de sécurité d’internet explorer 8 sont disponibles dans internet explorer 8 pour le système d’exploitation Windows XP avec Service Pack 2 (SP2) et les versions ultérieures. le Mode protégé n’est disponible que pour Windows vista ou versions ultérieures, car il est basé sur les fonctionnalités de sécurité suivantes qui sont nouvelles dans Windows Vista :

-   [Le contrôle de compte d’utilisateur (UAC)](https://msdn.microsoft.com/library/aa511445.aspx) facilite l’exécution sans privilèges d’administrateur. Lorsque les utilisateurs exécutent des programmes avec des privilèges utilisateur limités, ils sont plus sûrs contre une attaque que lorsqu’ils s’exécutent avec des privilèges d’administrateur. le système d’exploitation Windows peut empêcher le code malveillant d’effectuer des actions nuisibles.
-   Un mécanisme d’intégrité restreint l’accès en écriture aux [objets sécurisables](../secauthz/securable-objects.md) par des processus de plus faible intégrité, de la même façon que l’appartenance aux groupes de comptes d’utilisateur restreint les droits des utilisateurs à accéder aux composants système sensibles.
-   L’isolation des privilèges de l' [interface utilisateur (UIPI)](/previous-versions/dotnet/articles/bb625963(v=msdn.10)) empêche les processus d’envoyer des messages de fenêtre sélectionnés et d’autres API utilisateur aux processus qui s’exécutent avec une intégrité plus élevée.

l’infrastructure de sécurité du mécanisme d’intégrité du Windows permet au Mode protégé de fournir Windows Internet Explorer avec les privilèges dont les utilisateurs ont besoin pour naviguer sur le web, tout en disposant des privilèges dont les utilisateurs ont besoin pour installer des programmes en mode silencieux ou pour modifier les données système sensibles.

Les utilisateurs peuvent désactiver cette fonctionnalité par le biais d’une case à cocher, et les administrateurs peuvent la désactiver à l’aide de stratégie de groupe.

> [!IMPORTANT]
> Vous ne devez désactiver la fonctionnalité qu’en tant que mesure temporaire pendant la résolution des problèmes pour comparer le comportement de l’application lorsque celle-ci est activée ou non. Nous vous recommandons de conserver cette fonctionnalité activée de manière permanente.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
