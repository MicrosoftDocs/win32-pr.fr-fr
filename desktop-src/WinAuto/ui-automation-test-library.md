---
title: Bibliothèque de tests UI Automation
description: La bibliothèque de tests UI Automation (bibliothèque de tests UIA) est une API qui est appelée par l’application de pilote dans un scénario de test automatisé.
ms.assetid: A11341E5-71FC-442C-8F78-C40E717BF798
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac2c02433eaaa9f5d5658ca9f469803042b0a637bb20e6cdce72299bf7c4643f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133526"
---
# <a name="ui-automation-test-library"></a>Bibliothèque de tests UI Automation

La bibliothèque de tests UI Automation (bibliothèque de tests UIA) est une API qui est appelée par l’application de *pilote* dans un scénario de test automatisé. Le pilote est l’application qui obtient un élément Automation (objet [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ) à partir d’un contrôle qui nécessite une vérification et le fournit à la bibliothèque de tests UI Automation. Ensuite, la bibliothèque de tests vérifie et valide l’implémentation d’UI Automation. Pour en savoir plus sur l’Automation d’interface utilisateur et les éléments Automation, consultez [notions de base d’UI Automation](entry-uiautocore-overview.md).

-   [Flux de travail de la bibliothèque de tests UI Automation](#ui-automation-test-library-workflow)
-   [Journalisation avec la bibliothèque de tests UI Automation](#logging-with-the-ui-automation-test-library)
    -   [Journalisation XML](#xml-logging)
    -   [Journalisation de la console](#console-logging)
    -   [Spécifications de code pour la journalisation](#code-requirements-for-logging)
    -   [Exemples de journalisation](#logging-examples)

## <a name="ui-automation-test-library-workflow"></a>Flux de travail de la bibliothèque de tests UI Automation

Le diagramme suivant montre un flux de travail de test qui incorpore la bibliothèque de tests UI Automation à l’aide d’une application console comme pilote. Dans ce cas, le pilote démarre une instance de Notepad.exe et obtient un élément Automation (autrement dit, un objet [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ) à partir du contrôle d’édition. Ensuite, le pilote crée un objet de bibliothèque de tests UI Automation basé sur la plateforme d’interface utilisateur testée, puis passe dans l’élément Automation en tant que paramètre. La bibliothèque de tests UI Automation détermine que l’élément Automation est un type de contrôle de [document](uiauto-supportdocumentcontroltype.md) , puis exécute les tests de contrôle de document, les tests de modèle de contrôle de [défilement](uiauto-implementingscroll.md) et de [texte](uiauto-implementingtextandtextrange.md) , ainsi que les tests d’élément Automation génériques.

![Diagramme illustrant le passage du pilote à l’application à UIATestLibrary à l’aide de flèches rouges.](images/uia-test-library-workflow.png)

## <a name="logging-with-the-ui-automation-test-library"></a>Journalisation avec la bibliothèque de tests UI Automation

La bibliothèque de tests UI Automation utilise des dll externes pour enregistrer les résultats à partir des séries de tests. Il prend en charge la journalisation au format XML et la journalisation dans la console.

### <a name="xml-logging"></a>Journalisation XML

La journalisation XML est généralement utilisée par la vérification de l’automatisation de l’interface utilisateur de Visual, mais elle peut également être incorporée dans un flux de travail de ligne de commande.

Si la journalisation XML est spécifiée, l’application de pilote doit sérialiser la sortie en créant un objet **XmlWriter** et en le passant à la méthode **XmlLog. GetTestRunXml** . Le pilote peut ensuite utiliser le code XML sérialisé en interne ou l’écrire dans un fichier.

Les dll suivantes sont requises pour la journalisation XML.

-   WUIALogging.dll
-   WUIALoggerXml.dll

### <a name="console-logging"></a>Journalisation de la console

Par défaut, la bibliothèque de tests UI Automation utilise la journalisation de la console, où toute la sortie de journalisation est dirigée en texte brut dans la fenêtre de console. WUIALogging.dll est requis pour la journalisation de la console.

### <a name="code-requirements-for-logging"></a>Spécifications de code pour la journalisation

Une application de pilote doit inclure les extraits de code suivants pour utiliser la journalisation de la bibliothèque de tests UI Automation.


```CSharp
\\ Include logging functionality.
using Microsoft.Test.UIAutomation.Logging;

...

\\ Select a logger.
UIAVerifyLogger.SetLoggerType(LogTypes.DefaultLogger | 
                              LogTypes.ConsoleLogger | 
                              LogTypes.XmlLogger);

...

\\ Output comment to selected logger.
UIAVerifyLogger.LogComment("...");
```



### <a name="logging-examples"></a>Exemples de journalisation

Les exemples suivants illustrent la fonctionnalité de journalisation de base et montrent comment utiliser l’API de la bibliothèque de tests UI Automation dans une application de pilote Automation de test de base.


```CSharp
//---------------------------------------------------------------------------
//
// Description: Sample logger.
//
//---------------------------------------------------------------------------
using System;

namespace WUITest
{
    using Microsoft.Test.UIAutomation.Logging;

    public sealed class TestMain
    {
        private TestMain() { }

        /// -----------------------------------------------------------------
        /// <summary>
        /// Entry point
        /// </summary>
        /// -----------------------------------------------------------------
        [STAThread]
        static void Main(string[] args)
        {
            // Call SetLogger() if you don't want to use the default logger.
            // To set the logger type, call SetLogger(<string>).
            // <string> can be specified from the command line or from the 
            // the UI Automation Test Library enumeration:
            //  
            //     Logger.SetLogger(LogTypes.ConsoleLogger);
            //     Logger.SetLogger(LogTypes.DefaultLogger);

            Logger.SetLogger(LogTypes.DefaultLogger);

            Logger.StartTest("Test 1");
            Logger.LogComment("This is a comment");
            Logger.LogError(new Exception("My error"), false);
            Logger.EndTest();

            Logger.StartTest("Test 2");
            Logger.LogComment("This is a second comment");
            Logger.LogPass();
            Logger.EndTest();

            Logger.ReportResults();

        }
    }
}
```




```CSharp
//---------------------------------------------------------------------------
//
// Description: Sample test automation.
//
//---------------------------------------------------------------------------

using System;
using System.Windows;

namespace WUITest
{
    using System.Diagnostics;
    using System.Threading;
    using System.Windows.Automation;
    using Microsoft.Test.UIAutomation;
    using Microsoft.Test.UIAutomation.Core;
    using Microsoft.Test.UIAutomation.TestManager;
    using Microsoft.Test.UIAutomation.Tests.Controls;
    using Microsoft.Test.UIAutomation.Tests.Patterns;
    using Microsoft.Test.UIAutomation.Tests.Scenarios;
    using Microsoft.Test.UIAutomation.Logging;

    public sealed class TestMain
    {

        // Time in milliseconds to wait for the application to start.
        static int MAXTIME = 5000;
        // Time in milliseconds to wait before trying to find the application.
        static int TIMEWAIT = 100; 

        /// -------------------------------------------------------------------
        /// <summary>
        /// Start Notepad, obtain an AutomationElement object, and run tests.
        /// </summary>
        /// -------------------------------------------------------------------
        [STAThread]
        static void Main(string[] args)
        {
            // Dump the information to the console window.  
            // Use a different LogTypes value if you need to dump to another logger, 
            // or create your own logger that complies with the interface.
            UIAVerifyLogger.SetLoggerType(LogTypes.ConsoleLogger);

            // Get the automation element.
            AutomationElement element = StartApplication("NOTEPAD.EXE", null);

            // Call the UI Automation Test Library tests.
            TestRuns.RunAllTests(element, true, TestPriorities.Pri0, 
                    TestCaseType.Generic, false, true, null);

            // Clean up.
            ((WindowPattern)element.GetCurrentPattern(WindowPattern.Pattern)).Close();

            // Dump the summary of results.
            UIAVerifyLogger.ReportResults();
        }

        /// -------------------------------------------------------------------------
        /// <summary>
        /// Start the application and retrieve its AutomationElement. 
        /// </summary>
        /// -------------------------------------------------------------------------
        static public AutomationElement StartApplication(string appPath, 
                string arguments)
        {
            Process process;

            Library.ValidateArgumentNonNull(appPath, "appPath");

            ProcessStartInfo psi = new ProcessStartInfo();

            process = new Process();
            psi.FileName = appPath;

            if (arguments != null)
            {
                psi.Arguments = arguments;
            }

            UIAVerifyLogger.LogComment("Starting({0})", appPath);
            process.StartInfo = psi;

            process.Start();

            int runningTime = 0;
            while (process.MainWindowHandle.Equals(IntPtr.Zero))
            {
                if (runningTime > MAXTIME)
                    throw new Exception("Could not find " + appPath);

                Thread.Sleep(TIMEWAIT);
                runningTime += TIMEWAIT;

                process.Refresh();
            }

            UIAVerifyLogger.LogComment("{0} started", appPath);

            UIAVerifyLogger.LogComment("Obtained an AutomationElement for {0}", appPath);
            return AutomationElement.FromHandle(process.MainWindowHandle);

        }
    }
}
```



 

 




