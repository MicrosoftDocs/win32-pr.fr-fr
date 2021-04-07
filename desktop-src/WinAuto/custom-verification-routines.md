---
title: Routines de vérification personnalisées
description: Cette section décrit comment créer une routine de vérification personnalisée pour l’outil de vérification de l’accessibilité de l’interface utilisateur (AccChecker).
ms.assetid: 56F3EA1F-39C3-4DD9-8F2B-0C3608DD8737
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d66ad2fe0e27d16b55dd2d50d367250aadd15c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939746"
---
# <a name="custom-verification-routines"></a>Routines de vérification personnalisées

Cette section décrit comment créer une routine de vérification personnalisée pour l’outil de vérification de l’accessibilité de l’interface utilisateur (AccChecker).

-   [Création d’une vérification personnalisée](#creating-a-custom-verification)
    -   [Exemple de vérification personnalisée](#sample-custom-verification)
-   [Utilisation d’une vérification personnalisée](#using-a-custom-verification)
    -   [Interface utilisateur graphique (GUI) AccChecker](#the-accchecker-graphical-user-interface-gui)
    -   [AccChecker Automation](#accchecker-automation)
-   [Rubriques connexes](#related-topics)

L’outil de vérification de l’accessibilité de l’interface utilisateur (AccChecker) est un outil de test d’accessibilité conçu pour vérifier l’implémentation de Microsoft Active Accessibility (MSAA) dans une interface utilisateur de contrôle ou d’application. Les problèmes d’accessibilité ayant un impact élevé qui peuvent être exposés par l’implémentation MSAA sont testés avec un ensemble de routines de vérification automatisées intégrées. Ces routines de vérification natives peuvent être complétées par des routines personnalisées à l’aide de la plateforme AccChecker extensible.

## <a name="creating-a-custom-verification"></a>Création d’une vérification personnalisée

Une vérification personnalisée est créée sous la forme d’une bibliothèque de classes (DLL) qui implémente une interface unique ( `IVerificationRoutine` ) contenant un membre ( `Execute` ) :


```CSharp
void Execute(
    System.IntPtr hwnd, 
    AccCheck.Logging.ILogger logger, 
    bool AllowUI, 
    AccCheck.GraphicsHelper graphics
);
```



**Paramètres**

*HWND*

Type : **System. IntPtr**

HWND de l’élément en cours de vérification.

*suivi*

Tapez : **AccCheck. Logging. ILogger**

Méthode de journalisation sélectionnée. Parmi les types possibles, citons **AccumulatingLogger** (utilisé par AccChecker pour mettre en cache toutes les entrées de journal jusqu’à ce que les vérifications soient terminées), **ConsoleLogger**, **TextFileLogger** et **XMLSerializingLogger**.

*AllowUI*

Type : **bool**

Indique si la routine de vérification affiche l’interface utilisateur testée. Généralement défini sur false dans les scénarios de test automatisé.

*graphismes*

Tapez : **AccCheck. GraphicsHelper**

Utilisé pour les captures d’écran et autres visualisations dans AccChecker.

### <a name="sample-custom-verification"></a>Exemple de vérification personnalisée

L’exemple suivant est une vérification personnalisée C# qui effectue une vérification de la profondeur d’une arborescence d’éléments simple. Une erreur est consignée si l’arborescence d’éléments est supérieure à 50 niveaux, un avertissement est consigné si l’arborescence des éléments est comprise entre 20 et 50 niveaux et un message d’information est enregistré dans le cas contraire.


```CSharp
using System;
using System.Collections.Generic;
using System.Text;
using AccCheck;
using AccCheck.Logging;
using AccCheck.Verification;

namespace VerificationRoutines
{
    \\ Verification routine attributes.
    \\ If these values are not specified, the verification will not be displayed in the 
    \\ AccChecker UI. However, it is still loaded and will be included in all subsequent 
    \\ verification runs since it cannot be unchecked and excluded.
    [Verification(
        // Title - the title of the verification routine.
        "Sample Check Tree Depth",
        // Description - this attribute is not currently displayed.
        "Checks that the accessibility tree isn't excessively deep.",
        // Group Title - the verification group to add the routine. This can be a new or 
        //  existing group.
        Group = "TreeDepthCheck"
        )]

    public class CheckTreeDepth : IVerificationRoutine
    {
        private const int S_OK = 0;
        private const int ERROR_TREE_DEPTH = 50;
        private const int WARNING_TREE_DEPTH = 20;
        private int _depth = 0;

        private void TraverseTree(Accessible parent, int level)
        {
            if (level > _depth)
            {
                _depth = level;
            }

            // never go deeper than ERROR_TREE_DEPTH, that's a sign of a loop
            if (_depth > ERROR_TREE_DEPTH)
            {
                return;
            }

            Accessible[] children;
            if (parent.Children(out children) == S_OK)
            {
                foreach (Accessible child in children)
                {
                    TraverseTree(child, level + 1);
                }
            }
        }

        public void Execute(IntPtr hwnd, ILogger logger, bool AllowUI, 
                GraphicsHelper graphics)
        {
            Accessible root;
            if (Accessible.FromWindow(hwnd, out root) == S_OK)
            {
                TraverseTree(root, 0);
            }
            else
            {
                return;
            }

            if (_depth >= ERROR_TREE_DEPTH)
            {
                logger.Log(new LogEvent(EventLevel.Error, "DepthCheck", String.Format(
                    "The tree is too deep; the tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
            else if (_depth >= WARNING_TREE_DEPTH)
            {
                logger.Log(new LogEvent(EventLevel.Warning, "DepthCheck", String.Format(
                    "The tree might be too deep; the tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
            else
            {
                logger.Log(new LogEvent(EventLevel.Information, "DepthCheck", String.Format(
                    "The tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
        }
    }
}
```



> [!Note]  
> Une solution Microsoft Visual Studio qui contient un exemple de code de vérification est incluse dans la documentation d’aide. Les fichiers se trouvent dans le chemin d’installation de AccChecker.

 

## <a name="using-a-custom-verification"></a>Utilisation d’une vérification personnalisée

Cette section décrit comment incorporer une vérification personnalisée dans les scénarios de test AccChecker.

### <a name="the-accchecker-graphical-user-interface-gui"></a>Interface utilisateur graphique (GUI) AccChecker

Pour inclure une routine de vérification personnalisée dans l’application AccChecker, cliquez simplement sur Ouvrir la DLL dans le menu fichier et recherchez la DLL de la routine. La routine personnalisée sera ajoutée au bas de la liste des vérifications dans le volet Sélectionner les routines de vérification.

La capture d’écran suivante montre l’exemple de vérification personnalisée de profondeur d’arborescence de vérification ajoutée à AccChecker.

![exemple de la routine de vérification personnalisée de la profondeur de l’arborescence de vérification ajoutée à l’interface utilisateur accchecker](images/accchecker-sample-custom-verification.png)

> [!Note]  
> Si les valeurs d’attribut de vérification ne sont pas spécifiées dans la routine de vérification personnalisée, la vérification est toujours chargée dans AccChecker même si elle n’apparaît pas dans l’interface utilisateur. Étant donné qu’elle n’est pas affichée dans l’interface utilisateur, elle ne peut pas être désactivée et exclue des exécutions de vérification suivantes.

 

### <a name="accchecker-automation"></a>AccChecker Automation

L’incorporation d’une routine de vérification personnalisée dans une infrastructure AccChecker automatisée est aussi simple que l’ajout de la DLL de vérification et l’activation des routines de vérification souhaitées.

L’extrait de code suivant montre comment utiliser l’API AccChecker pour tester la fonctionnalité de tabulation dans l’application du panneau de configuration du pare-feu Windows.


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
        //  Get our user interface ready for AccChecker.
        Setup();

        //  AccChecker's class representing verifications that you can run.
        AccCheck.Verification.VerificationManager vm = new AccCheck.Verification.VerificationManager();

        //  Create a console logger to get output in the console.
        ConsoleLogger consoleLogger = new ConsoleLogger();

        //  Add the AccChecker Console Logger.
        vm.AddLogger(consoleLogger);

        //  Disable all verifications; all verifications are enabled by default.
        vm.DisableVerifications(AccCheck.Verification.VerificationFilter.All);

        // Add a custom verification DLL.
        vm.AddVerificationDll("CheckTreeDepthVerification.dll");
        
        // Enable the routine we want to run.
        vm.EnableRoutine("Sample Check Tree Depth");

        //  Run the verification routine against the firewall.
        vm.ExecuteEnabled(_fireWallHwnd);

        //  Check the logger to see if the verification failed.
        if (consoleLogger.ErrorCount > 0)
        {
            Console.WriteLine("Test failed!");
            Console.WriteLine("Error count = " + consoleLogger.ErrorCount);
        }

        // Clean up the user interface.
        Cleanup();
    }
}
```



> [!Note]  
> Une solution Microsoft Visual Studio 2008 qui contient un exemple de code de vérification est incluse dans la documentation d’aide. Les fichiers se trouvent dans le chemin d’installation de AccChecker.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vérificateur d’accessibilité de l’interface utilisateur](ui-accessibility-checker.md)
</dt> </dl>

 

 




