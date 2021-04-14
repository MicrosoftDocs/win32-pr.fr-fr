---
title: Bibliothèque de tests UI Automation
description: La bibliothèque de tests UI Automation (bibliothèque de tests UIA) est une API qui est appelée par l’application de pilote dans un scénario de test automatisé.
ms.assetid: A11341E5-71FC-442C-8F78-C40E717BF798
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64200673d45f800e1e18dee2afd5c4acd2b604f
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2021
ms.locfileid: "104561725"
---
# <a name="ui-automation-test-library"></a><span data-ttu-id="31f0f-103">Bibliothèque de tests UI Automation</span><span class="sxs-lookup"><span data-stu-id="31f0f-103">UI Automation Test Library</span></span>

<span data-ttu-id="31f0f-104">La bibliothèque de tests UI Automation (bibliothèque de tests UIA) est une API qui est appelée par l’application de *pilote* dans un scénario de test automatisé.</span><span class="sxs-lookup"><span data-stu-id="31f0f-104">The UI Automation Test Library (UIA Test Library) is an API that is called by the *driver* application in an automated testing scenario.</span></span> <span data-ttu-id="31f0f-105">Le pilote est l’application qui obtient un élément Automation (objet [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ) à partir d’un contrôle qui nécessite une vérification et le fournit à la bibliothèque de tests UI Automation.</span><span class="sxs-lookup"><span data-stu-id="31f0f-105">The driver is the application that obtains an automation element ([**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) object) from a control that requires verification, and provides it to the UI Automation Test Library.</span></span> <span data-ttu-id="31f0f-106">Ensuite, la bibliothèque de tests vérifie et valide l’implémentation d’UI Automation.</span><span class="sxs-lookup"><span data-stu-id="31f0f-106">Then, the test library checks and validates the UI Automation implementation.</span></span> <span data-ttu-id="31f0f-107">Pour en savoir plus sur l’Automation d’interface utilisateur et les éléments Automation, consultez [notions de base d’UI Automation](entry-uiautocore-overview.md).</span><span class="sxs-lookup"><span data-stu-id="31f0f-107">To learn more about UI Automation and automation elements, see [UI Automation Fundamentals](entry-uiautocore-overview.md).</span></span>

-   [<span data-ttu-id="31f0f-108">Flux de travail de la bibliothèque de tests UI Automation</span><span class="sxs-lookup"><span data-stu-id="31f0f-108">UI Automation Test Library Workflow</span></span>](#ui-automation-test-library-workflow)
-   [<span data-ttu-id="31f0f-109">Journalisation avec la bibliothèque de tests UI Automation</span><span class="sxs-lookup"><span data-stu-id="31f0f-109">Logging with the UI Automation Test Library</span></span>](#logging-with-the-ui-automation-test-library)
    -   [<span data-ttu-id="31f0f-110">Journalisation XML</span><span class="sxs-lookup"><span data-stu-id="31f0f-110">XML Logging</span></span>](#xml-logging)
    -   [<span data-ttu-id="31f0f-111">Journalisation de la console</span><span class="sxs-lookup"><span data-stu-id="31f0f-111">Console Logging</span></span>](#console-logging)
    -   [<span data-ttu-id="31f0f-112">Spécifications de code pour la journalisation</span><span class="sxs-lookup"><span data-stu-id="31f0f-112">Code Requirements for Logging</span></span>](#code-requirements-for-logging)
    -   [<span data-ttu-id="31f0f-113">Exemples de journalisation</span><span class="sxs-lookup"><span data-stu-id="31f0f-113">Logging Examples</span></span>](#logging-examples)

## <a name="ui-automation-test-library-workflow"></a><span data-ttu-id="31f0f-114">Flux de travail de la bibliothèque de tests UI Automation</span><span class="sxs-lookup"><span data-stu-id="31f0f-114">UI Automation Test Library Workflow</span></span>

<span data-ttu-id="31f0f-115">Le diagramme suivant montre un flux de travail de test qui incorpore la bibliothèque de tests UI Automation à l’aide d’une application console comme pilote.</span><span class="sxs-lookup"><span data-stu-id="31f0f-115">The following diagram shows a test workflow that incorporates the UI Automation Test Library by using a console application as the driver.</span></span> <span data-ttu-id="31f0f-116">Dans ce cas, le pilote démarre une instance de Notepad.exe et obtient un élément Automation (autrement dit, un objet [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ) à partir du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="31f0f-116">In this case, the driver starts an instance of Notepad.exe and obtains an automation element (that is, a [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) object) from the edit control.</span></span> <span data-ttu-id="31f0f-117">Ensuite, le pilote crée un objet de bibliothèque de tests UI Automation basé sur la plateforme d’interface utilisateur testée, puis passe dans l’élément Automation en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="31f0f-117">Next, the driver creates a UI Automation Test Library object based on the UI platform being tested, and then passes in the automation element as a parameter.</span></span> <span data-ttu-id="31f0f-118">La bibliothèque de tests UI Automation détermine que l’élément Automation est un type de contrôle de [document](uiauto-supportdocumentcontroltype.md) , puis exécute les tests de contrôle de document, les tests de modèle de contrôle de [défilement](uiauto-implementingscroll.md) et de [texte](uiauto-implementingtextandtextrange.md) , ainsi que les tests d’élément Automation génériques.</span><span class="sxs-lookup"><span data-stu-id="31f0f-118">The UI Automation Test Library determines that the automation element is a [Document](uiauto-supportdocumentcontroltype.md) control type, and then executes the Document control tests, the [Text](uiauto-implementingtextandtextrange.md) and [Scroll](uiauto-implementingscroll.md) control pattern tests, and generic automation element tests.</span></span>

![Diagramme illustrant le passage du pilote à l’application à UIATestLibrary à l’aide de flèches rouges.](images/uia-test-library-workflow.png)

## <a name="logging-with-the-ui-automation-test-library"></a><span data-ttu-id="31f0f-120">Journalisation avec la bibliothèque de tests UI Automation</span><span class="sxs-lookup"><span data-stu-id="31f0f-120">Logging with the UI Automation Test Library</span></span>

<span data-ttu-id="31f0f-121">La bibliothèque de tests UI Automation utilise des dll externes pour enregistrer les résultats à partir des séries de tests.</span><span class="sxs-lookup"><span data-stu-id="31f0f-121">The UI Automation Test Library uses external DLLs to log results from test runs.</span></span> <span data-ttu-id="31f0f-122">Il prend en charge la journalisation au format XML et la journalisation dans la console.</span><span class="sxs-lookup"><span data-stu-id="31f0f-122">It supports logging as XML and logging to the console.</span></span>

### <a name="xml-logging"></a><span data-ttu-id="31f0f-123">Journalisation XML</span><span class="sxs-lookup"><span data-stu-id="31f0f-123">XML Logging</span></span>

<span data-ttu-id="31f0f-124">La journalisation XML est généralement utilisée par la vérification de l’automatisation de l’interface utilisateur de Visual, mais elle peut également être incorporée dans un flux de travail de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="31f0f-124">XML logging is typically used by Visual UI Automation Verify, but it can also be incorporated into a command-line workflow.</span></span>

<span data-ttu-id="31f0f-125">Si la journalisation XML est spécifiée, l’application de pilote doit sérialiser la sortie en créant un objet **XmlWriter** et en le passant à la méthode **XmlLog. GetTestRunXml** .</span><span class="sxs-lookup"><span data-stu-id="31f0f-125">If XML logging is specified, the driver application must serialize the output by creating an **XmlWriter** object and passing it to the **XmlLog.GetTestRunXml** method.</span></span> <span data-ttu-id="31f0f-126">Le pilote peut ensuite utiliser le code XML sérialisé en interne ou l’écrire dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="31f0f-126">The driver can then use the serialized XML internally or write it to a file.</span></span>

<span data-ttu-id="31f0f-127">Les dll suivantes sont requises pour la journalisation XML.</span><span class="sxs-lookup"><span data-stu-id="31f0f-127">The following DLLs are required for XML logging.</span></span>

-   <span data-ttu-id="31f0f-128">WUIALogging.dll</span><span class="sxs-lookup"><span data-stu-id="31f0f-128">WUIALogging.dll</span></span>
-   <span data-ttu-id="31f0f-129">WUIALoggerXml.dll</span><span class="sxs-lookup"><span data-stu-id="31f0f-129">WUIALoggerXml.dll</span></span>

### <a name="console-logging"></a><span data-ttu-id="31f0f-130">Journalisation de la console</span><span class="sxs-lookup"><span data-stu-id="31f0f-130">Console Logging</span></span>

<span data-ttu-id="31f0f-131">Par défaut, la bibliothèque de tests UI Automation utilise la journalisation de la console, où toute la sortie de journalisation est dirigée en texte brut dans la fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="31f0f-131">By default, the UI Automation Test Library uses console logging, where all logging output is piped as plain text to the console window.</span></span> <span data-ttu-id="31f0f-132">WUIALogging.dll est requis pour la journalisation de la console.</span><span class="sxs-lookup"><span data-stu-id="31f0f-132">WUIALogging.dll is required for console logging.</span></span>

### <a name="code-requirements-for-logging"></a><span data-ttu-id="31f0f-133">Spécifications de code pour la journalisation</span><span class="sxs-lookup"><span data-stu-id="31f0f-133">Code Requirements for Logging</span></span>

<span data-ttu-id="31f0f-134">Une application de pilote doit inclure les extraits de code suivants pour utiliser la journalisation de la bibliothèque de tests UI Automation.</span><span class="sxs-lookup"><span data-stu-id="31f0f-134">A driver application must include the following code snippets to use UI Automation Test Library logging.</span></span>


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



### <a name="logging-examples"></a><span data-ttu-id="31f0f-135">Exemples de journalisation</span><span class="sxs-lookup"><span data-stu-id="31f0f-135">Logging Examples</span></span>

<span data-ttu-id="31f0f-136">Les exemples suivants illustrent la fonctionnalité de journalisation de base et montrent comment utiliser l’API de la bibliothèque de tests UI Automation dans une application de pilote Automation de test de base.</span><span class="sxs-lookup"><span data-stu-id="31f0f-136">The following examples demonstrate basic logging functionality and show how to use the UI Automation Test Library API in a basic test automation driver application.</span></span>


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



 

 




