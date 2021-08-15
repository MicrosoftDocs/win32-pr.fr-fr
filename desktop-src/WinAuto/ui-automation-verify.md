---
title: Vérification d’UI Automation (UIA Verify)
description: Vérification d’UI Automation (UIA Verify) est une infrastructure de test pour les tests manuels et automatisés de l’implémentation d’un contrôle ou d’une application de Microsoft UI Automation.
ms.assetid: C66AF411-2746-4695-A893-1552B3ED1066
keywords:
- UI Automation Verify
- Vérification de UIA
- Implémentation d’UI Automation, test
- test de l’Automation d’interface utilisateur
- Outils de test de UIA
- Outils de test UI Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f8c97d6522e353445ededff47a9a7cf123998b94f1323f1df59b7a380ac1d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052387"
---
# <a name="accessibility-tools---ui-automation-verify-uia-verify"></a>Outils d’accessibilité-vérification de l’UI Automation (UIA Verify)

**Vérification d’UI Automation (UIA Verify)** est une infrastructure de test pour les tests manuels et automatisés de l’implémentation d’un contrôle ou d’une application de Microsoft UI Automation. La plupart des fonctionnalités de l’infrastructure de test proviennent d’une DLL appelée WUIATestLibrary.dll. Cette DLL contient le code permettant de tester des fonctionnalités d’automatisation d’interface utilisateur spécifiques et prend également en charge la journalisation des résultats des tests. Vous pouvez intégrer votre application dans le code de test et procéder à des tests réguliers, automatisés ou à des contrôles ponctuels de vos scénarios d’automatisation d’interface utilisateur.

**UIA Verify** est installé avec le kit de développement logiciel (SDK) Windows. Il se trouve dans le \\ dossier bin \\ < *version* > \\ < *Platform* > \\ UIAVerify du chemin d’installation du kit de développement logiciel (VisualUIAVerifyNative.exe).

**UIA Verify** se compose d’une API appelée bibliothèque de test UI Automation et d’une interface GUI appelée **vérification** de l’interface utilisateur de Visual UI. Celles-ci sont décrites dans les rubriques suivantes.

> [!NOTE]
> **UI Automation Verify** est un outil hérité. nous vous recommandons d’utiliser à la place l' [accessibilité Informations](https://accessibilityinsights.io/) .

## <a name="requirements"></a>Configuration requise

UI Automation doit être présent sur le système. Pour plus d’informations, consultez la section « Configuration requise » d' [UI Automation](entry-uiauto-win32.md).

**UIA Verify** est installé dans le cadre de l’ensemble d’outils de la SDK Windows, il n’est pas distribué en tant que téléchargement séparé. le SDK Windows comprend tous les outils liés à l’accessibilité documentés dans cette section. [obtient le SDK Windows.](https://developer.microsoft.com/) (Il existe également un kit de développement logiciel (SDK) à partir de cette page, si vous avez besoin d’une version précédente.)

Pour exécuter **UIA Verify** comme outil visuel, recherchez VisualUIAVerifyNative.exe dans le \\ dossier bin \\ < *Platform* > \\ UIAVerify et exécutez-le (vous n’êtes généralement pas obligé d’exécuter en tant qu’administrateur). Pour plus d’informations, voir [Visual UI Automation Verify](visual-ui-automation-verify.md). Pour utiliser les bibliothèques, consultez [UI Automation test Library](ui-automation-test-library.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accessible Event Watcher](accessible-event-watcher.md)
</dt> <dt>

[Inspecter](inspect-objects.md)
</dt> <dt>

[Outils de test](testing-tools.md)
</dt> <dt>

[Vérificateur d’accessibilité de l’interface utilisateur](ui-accessibility-checker.md)
</dt> </dl>

 

 




