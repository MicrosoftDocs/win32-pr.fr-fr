---
title: API AccChecker
description: L’API AccChecker prend en charge les tests automatisés. Après avoir suivi une application à l’aide de tests manuels avec l’interface graphique utilisateur AccChecker, vous pouvez écrire des tests automatisés qui incorporent les journaux de messages et de suppression créés avec l’outil GUI.
ms.assetid: 9AD9A259-130B-4968-B7FD-DAFA89320391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c098d25e282a8df8ff4125dfd2ce1f94d795b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839442"
---
# <a name="the-accchecker-api"></a>API AccChecker

L’API AccChecker prend en charge les tests automatisés. Après avoir suivi une application à l’aide de tests manuels avec l’interface graphique utilisateur AccChecker, vous pouvez écrire des tests automatisés qui incorporent les journaux de messages et de suppression créés avec l’outil GUI.

L’exemple de code suivant montre comment utiliser l’API AccChecker pour tester la fonctionnalité de tabulation dans l’application du panneau de configuration du pare-feu Windows.


```CSharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using AccCheck.Logging;
 
public class TestCases : TestBase
{
    public void AccessibilityTestCase()
    {
        //  get our user interface ready for AccChecker
        Setup();
 
        //  AccChecker's class representing verifications that you can run
        AccCheck.Verification.VerificationManager vm = new AccCheck.Verification.VerificationManager();
 
        //  create a console logger to get output in the console
        ConsoleLogger consoleLogger = new ConsoleLogger();
 
        //  add AccChecker's Console Logger
        vm.AddLogger(consoleLogger);
 
        //  disable all verifications
        vm.DisableVerifications(AccCheck.Verification.VerificationFilter.All);
 
        // enable the ones we want to run
        vm.EnableRoutine("CheckTabbing");
 
        //  run it against the firewall
        vm.ExecuteEnabled(_fireWallHwnd);
 
        //  check if the verification failed by looking at the logger
        if (consoleLogger.ErrorCount > 0)
        {
            Console.WriteLine("Test failed!");
 
            Console.WriteLine("Error count = " + consoleLogger.ErrorCount);
        }
 
        // cleanup our user interface
        Cleanup();
    }
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vérificateur d’accessibilité de l’interface utilisateur](ui-accessibility-checker.md)
</dt> </dl>

 

 




