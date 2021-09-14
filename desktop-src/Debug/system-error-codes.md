---
description: Fournit des liens vers les codes d’erreur système définis dans le fichier d’en-tête WinError. h et est destiné aux développeurs.
ms.assetid: 4a3a8feb-a05f-4614-8f04-1f507da7e5b7
title: Codes d’erreur système
ms.topic: article
ms.date: 10/31/2019
ms.openlocfilehash: 072e1eb4a43c787055bc2793b3f58d69cdf6dd12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114517"
---
# <a name="system-error-codes"></a>Codes d’erreur système

Cette section s’adresse aux développeurs qui déboguent des erreurs système. Si vous avez atteint cette page lors de la recherche d’autres erreurs, voici quelques liens qui peuvent vous aider :

* [erreurs de Windows Update](https://support.microsoft.com/help/10164/fix-windows-update-errors) : pour résoudre les problèmes liés à Windows Update.
* [Windows des erreurs d’activation](https://support.microsoft.com/help/10738/windows-10-get-help-with-activation-errors) : pour vous aider à vérifier votre copie de Windows.
* [Résolution des erreurs d’écran bleu](https://support.microsoft.com/help/14238/windows-10-troubleshoot-blue-screen-errors) -pour vous aider à découvrir ce qui a provoqué une erreur d’arrêt.
* [Support Microsoft](https://support.microsoft.com) -pour la prise en charge d’un produit Microsoft.

## <a name="more-ways-to-find-an-error-code"></a>Autres méthodes pour rechercher un code d’erreur

Nous avons listé les codes d’erreur système de cette section, organisés par nombre. Si vous avez besoin de plus d’aide pour le suivi d’une erreur spécifique, voici quelques recommandations :

* Utilisez l' [outil de recherche d’erreurs Microsoft](system-error-code-lookup-tool.md).
*  installez les outils de débogage pour Windows, chargez un fichier de vidage de la mémoire, puis exécutez la commande **\! err \<code>** .
* Recherchez du texte brut ou un code d’erreur dans le site des protocoles Microsoft. pour plus d’informations, consultez [[MS-ERREF] : Windows Codes d’erreur](/openspecs/windows_protocols/ms-erref/1bc92ddf-b79e-413c-bbaa-99a5281a6c90).

## <a name="third-party-error-codes"></a>Codes d’erreur tiers

D’autres codes d’erreur peuvent être générés par des services ou des applications tierces (par exemple, le **code d’erreur :-118** peut être affiché par le [service de jeu de vapeur](https://support.steampowered.com/kb_cat.php?id=59)) et, dans ces cas, vous devez contacter la ligne de support du tiers.

## <a name="system-error-codes"></a>Codes d’erreur système

Les codes d’erreur système sont très larges : chacun d’eux peut se produire dans l’une des centaines d’emplacements du système. Par conséquent, les descriptions de ces codes ne peuvent pas être très spécifiques. L’utilisation de ces codes requiert un certain nombre d’investigations et d’analyses. Vous devez noter à la fois le contexte de programmation et le contexte d’exécution dans lesquels ces erreurs se produisent. 

Étant donné que ces codes sont définis dans WinError. h pour quiconque puisse les utiliser, les codes sont parfois retournés par des logiciels non-système. Et parfois, le code est retourné par une fonction profonde dans la pile et supprimé du code qui gère l’erreur.

Les rubriques suivantes fournissent des listes de codes d’erreur système. Ces valeurs sont définies dans le fichier d’en-tête WinError. h.

-   [Codes d’erreur système (0-499) (0x0-0x1f3)](system-error-codes--0-499-.md)
-   [Codes d’erreur système (500-999) (0x1F4-0x3e7)](system-error-codes--500-999-.md)
-   [Codes d’erreur système (1000-1299) (0x3e8-0x513)](system-error-codes--1000-1299-.md)
-   [Codes d’erreur système (1300-1699) (0x514-0x6a3)](system-error-codes--1300-1699-.md)
-   [Codes d’erreur système (1700-3999) (0x6a4-0xf9f)](system-error-codes--1700-3999-.md)
-   [Codes d’erreur système (4000-5999) (0xfa0-0x176f)](system-error-codes--4000-5999-.md)
-   [Codes d’erreur système (6000-8199) (0x1770-0x2007)](system-error-codes--6000-8199-.md)
-   [Codes d’erreur système (8200-8999) (0x2008-0x2327)](system-error-codes--8200-8999-.md)
-   [Codes d’erreur système (9000-11999) (0x2328-0x2edf)](system-error-codes--9000-11999-.md)
-   [Codes d’erreur système (12000-15999) (0x2ee0-0x3e7f)](system-error-codes--12000-15999-.md)
