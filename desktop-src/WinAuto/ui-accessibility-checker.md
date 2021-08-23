---
title: Outils d’accessibilité-AccChecker (vérificateur d’accessibilité de l’interface utilisateur)
description: Décrit AccChecker (UI Accessibility Checker), un outil de test de l’implémentation UI Automation ou Microsoft Active Accessibility (MSAA) d’une application.
ms.assetid: 92155984-356A-4774-A99D-35B15A3BB704
keywords:
- Vérificateur d’accessibilité de l’interface utilisateur
- AccChecker
- Implémentation d’UI Automation, test
- Implémentation de UIA, test
- Implémentation de Microsoft Active Accessibility, test
- Implémentation MSAA, test
- test de l’Automation d’interface utilisateur
- test de UIA
- test de Microsoft Active Accessibility
- test de MSAA
- Outils de test de UIA
- Outils de test UI Automation
- Outils de test MSAA
- Outils de test Microsoft Active Accessibility
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 452ff74140b50f1f6ea6d5357187e42ecff2d83cc85076d11ff22e191da7f3ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052407"
---
# <a name="accessibility-tools---accchecker-ui-accessibility-checker"></a>Outils d’accessibilité-AccChecker (vérificateur d’accessibilité de l’interface utilisateur)

**AccChecker** (outil d’analyse d’accessibilité de l’interface utilisateur) vérifie que les exigences d’accessibilité de l’interface utilisateur clés sont respectées dans la conception et l’implémentation d’UI Automation (UIA) ou de Microsoft Active Accessibility (MSAA) indépendamment de l’infrastructure d’interface utilisateur sous-jacente. **AccChecker** comprend également un ensemble de vérifications de l’accessibilité du Web.

**AccChecker** fournit les niveaux de fonctionnalité suivants :

- Windows application GUI qui prend en charge les tests manuels, la journalisation des messages et la génération de suppressions.
- API à utiliser dans les infrastructures de tests automatisés.
- Application console qui prend en charge les automations de test non managées pour les scénarios où l’API managée **AccChecker** ne peut pas être utilisée.

Tous les niveaux de fonctionnalités **AccChecker** fournissent des routines pour vérifier l’accès par programme de Microsoft Active Accessibility, la génération d’événements par programme, la disposition des contrôles et la navigation au clavier. **AccChecker** fournit également un service de transcription de lecteur d’écran de base.

**AccChecker** est installé avec le kit de développement logiciel (SDK) Windows. Il se trouve dans le \\ dossier bin \\ < *version* > \\ < *Platform* > \\ AccChecker du chemin d’installation du kit de développement logiciel (SDK).

> [!NOTE]
> **AccChecker** est un outil hérité. nous vous recommandons d’utiliser à la place l' [accessibilité Informations](https://accessibilityinsights.io/) .

## <a name="requirements"></a>Configuration requise

requiert .NET Framework 2,0 ou une version ultérieure.

**AccChecker** peut être utilisé pour examiner les données d’accessibilité sur les systèmes qui n’ont pas Microsoft UI Automation, mais qui peuvent uniquement examiner les propriétés de Microsoft Active Accessibility. Pour examiner l’Automation d’interface utilisateur, UI Automation doit être présent sur le système. Pour plus d’informations, consultez la section « Configuration requise » d' [UI Automation](entry-uiauto-win32.md).

**AccChecker** est installé dans le cadre du jeu d’outils global dans le kit de développement logiciel (SDK) le, il n’est pas distribué en tant que téléchargement de fichier exécutable distinct. le SDK Windows comprend tous les outils liés à l’accessibilité documentés dans cette section. [obtient le SDK Windows.](https://developer.microsoft.com/) (Il existe également un kit de développement logiciel (SDK) à partir de cette page, si vous avez besoin d’une version précédente.)

## <a name="related-topics"></a>Rubriques connexes

- [Accessible Event Watcher](accessible-event-watcher.md)
- [Inspecter](inspect-objects.md)
- [Outils de test](testing-tools.md)
- [UI Automation Verify](ui-automation-verify.md)
