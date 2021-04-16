---
description: Cette rubrique présente les API d’analyse d’encre.
ms.assetid: a3126930-2802-43c7-9e98-3a73498ac3f5
title: Reconnaissance de base et analyse de l’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9858ceedba245a733d4dc0055dd0747507654f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393240"
---
# <a name="basic-recognition-and-ink-analysis"></a>Reconnaissance de base et analyse de l’encre

Cette rubrique présente les API d’analyse d’encre.

## <a name="simple-recognition"></a>Reconnaissance simple

La fonctionnalité de base exposée par l’API d’analyse d’encre est l’accès aux résultats de la reconnaissance pour une partie donnée de l’encre. Cette opération est simple et simple, comme illustré dans l’exemple de code suivant.


```C++
// Instantiate a new InkAnalyzer object, passing in an Ink object and
// the synchronizing object.
InkAnalyzer ia = new InkAnalyzer(myInkOverlay.Ink, this);

// Associate the Strokes to be recognized with the InkAnalyzer.
ia.AddStrokes(myInkOverlay.Ink.Strokes);

// Synchronously recognize the Strokes.
ia.Analyze();

// Access the results and display.
string myResults = ia.GetRecognizedString();
MessageBox.Show(myResults);
```



Les résultats de l’opération de reconnaissance sont simplement une valeur de chaîne représentant la valeur reconnue de l’encre manuscrite. L’API d’analyse d’encre expose une plus grande fonctionnalité de reconnaissance que la seule chaîne reconnue, mais c’est l’opération la plus courante.

## <a name="incremental-recognition"></a>Reconnaissance incrémentielle

Le processus de reconnaissance prend du temps, bloquant l’accès à l’application en bloquant le thread d’interface utilisateur de l’application. Il peut donc être coûteux et frustrant pour l’utilisateur final d’attendre des résultats de façon synchrone. De nombreuses applications Tablet PC nécessitent la reconnaissance de plus de quelques lignes d’encre, et une approche incrémentielle pour la reconnaissance des traits sur un thread d’arrière-plan est la stratégie optimale. L’avantage d’une approche incrémentielle au lieu d’une opération en bloc est qu’elle permet la reconnaissance des traits sur une période donnée, en étalant le travail sur le thread d’arrière-plan plutôt que de façon synchrone sur le thread de premier plan. Pour prendre en charge l’analyse incrémentielle, l’objet [**InkAnalyzer**](inkanalyzer.md) possède une méthode [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) , qui gère la création et la gestion d’un thread d’arrière-plan pour l’application. Le **InkAnalyzer** prend également automatiquement en charge la gestion de ce qui doit être reconnu et ce qui a déjà été reconnu.

Par conséquent, il existe deux mécanismes pour atteindre les résultats de la reconnaissance :

-   La méthode [**analyze**](iinkanalyzer-analyze.md) (analyse synchrone), qui fonctionne le mieux pour :

    -   Petites quantités d’encre.
    -   Lorsque les résultats sont nécessaires avant de passer à l’opération suivante dans l’application, par exemple lors de l’affichage d’une interface utilisateur de correction.

-   La méthode [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) (analyse asynchrone), qui fonctionne le mieux pour :

    -   Toute quantité d’encre.
    -   En cas d’utilisation avec un minuteur clignotant environ toutes les 600 millisecondes.

> [!Note]  
> la recommandation actuelle est de 600 millisecondes, mais ce minutage est susceptible de changer en attendant d’autres tests.

 

Pour utiliser l’opération [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) , l’objet [**InkCollector**](inkcollector-class.md) (ou des objets ou des contrôles similaires tels que [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md)ou [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) dans Windows Presentation Foundation) gère la collection et le rendu des traits d’encre. Si le formulaire **InkCollector** est associé aux API d’analyse d’encre, les applications peuvent conserver les résultats de la reconnaissance à jour en informant le [**InkAnalyzer**](inkanalyzer.md) sur chaque nouveau trait ajouté à l’application. Cela permet au **InkAnalyzer** de reconnaître les traits de manière incrémentielle et sur un thread d’arrière-plan.

Pour effectuer une analyse incrémentielle en arrière-plan, les applications doivent implémenter trois étapes (affichées pour le code managé) :

1. Ajoutez le trait à [**InkAnalyzer**](inkanalyzer.md) chaque fois que l’événement [**Stroke**](inkoverlay-stroke.md) de l’objet [**InkOverlay**](inkoverlay-class.md) est déclenché :


```C++
/// Event Handler from InkOverlay's Stroke event
/// This event is fired when a new stroke is drawn. 
/// In this case, it is necessary to update the ink analyzer's 
/// Strokes collection. The event is fired even when the eraser 
/// stroke is created.
/// The event handler must filter out the eraser strokes.
/// <param name="sender">The control that raised the event.</param>
/// <param name="e">The event arguments.</param>
private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e)
{
        // Add the new stroke to the InkAnalyzer's stroke collection
        theInkAnalyzer.AddStroke(e.Stroke);
        this.Refresh();
}
```



2. Appelle les opérations [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) à un intervalle défini.


```C++
//Setup a timer tick handler
private System.Windows.Forms.Timer analysisTimer;
analysisTimer = new Timer();
analysisTimer.Tick += new System.EventHandler(this.analysisTimer_Tick);

// The timer is enabled and set to tick every 600 milliseconds.
analysisTimer.Enabled = true;
analysisTimer.Interval = 600;
// ...
//The background analysis operation is invoked with every tick
private void analysisTimer_Tick(object sender, System.EventArgs e)
{
    theInkAnalyzer.BackgroundAnalyze();
}
```



> [!Note]  
> Remarque les applications ne doivent pas simplement appeler l’opération d’analyse en arrière-plan après chaque nouveau trait. Cela échoue (en retournant la valeur **false**) si une opération en arrière-plan est déjà en cours d’exécution. La raison de ce comportement est de limiter le nombre de threads d’arrière-plan et d’opérations de réconciliation requis.

 

3. Écoutez l’événement [ResultsUpdated](/previous-versions/ms567607(v=vs.100)) (code managé) ou les événements de [**résultats**](-ianalysisevents-results.md) (code C++) pour déterminer à quel moment le processus en arrière-plan est terminé :


```C++
// ...
theInkAnalyzer.Results += new ResultsEventHandler(ia_Results);
// ...

private void ia_Results(object sender, ResultsEventArgs e)
{
    String myResults = e.InkAnalyzer.GetRecognizedString();
    MessageBox.Show(myResults);
}
```



Maintenant que le traitement de l’encre est effectué sur un thread d’arrière-plan, l’application a la possibilité d’accepter les modifications apportées à l’encre pendant que l’opération en arrière-plan fonctionne. Si nous utilisons un thread synchrone, cela n’est pas possible. Le travail s’exécute sur le thread d’interface utilisateur, ce qui bloque la possibilité d’apporter des modifications. Les modifications incluent l’ajout d’une entrée manuscrite supplémentaire au document, la suppression de l’encre ou la transformation de l’emplacement ou de l’apparence de l’encre existante. Les modifications qui se produisent pendant l’opération d’arrière-plan peuvent en fait invalider les résultats. Par exemple, la suppression d’un trait d’un mot modifie la valeur de reconnaissance de ce mot. L’API [**InkAnalyzer**](inkanalyzer.md) a un processus de réconciliation intégré qui détermine automatiquement les parties de l’opération d’arrière-plan qui deviennent non valides en raison de la modification de l’encre lors de l’analyse.

Le processus de réconciliation automatique est effectué en raison de trois facteurs :

1.  Propriété [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) .

    -   Chaque fois que l’application ajoute (méthode [**AddStroke**](iinkanalyzer-addstroke.md) ) ou supprime (méthode [**RemoveStroke**](iinkanalyzer-removestroke.md) ) un trait vers ou à partir du [**InkAnalyzer**](inkanalyzer.md), l’emplacement physique du trait est capturé et la prochaine fois qu’une opération d’analyse est appelée, le **InkAnalyzer** garantit que ce trait, ou la zone occupée par ce trait, est analysé.
    -   Chaque fois que l’application modifie l’encre existante, modifie l’emplacement ou modifie d’autres attributs de dessin de l’encre, l’emplacement de la modification (les limites de l’encre) peut être ajouté à la propriété [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) de [**InkAnalyzer**](inkanalyzer.md). Cela garantit que la prochaine fois que l’application démarre l’opération d’analyse, les résultats corrects sont vérifiés.
    -   Par conséquent, la propriété [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) effectue le suivi, entre les exécutions d’analyse, les zones du document et, à tour de rôle, les traits qui doivent être vérifiés pour obtenir des résultats corrects d’analyse de l’encre et de reconnaissance.

2.  Analyse limitée.

    -   Chaque fois que l’application appelle l’opération d’analyse, la propriété [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) identifie les traits qui doivent être analysés. Cela permet à l’opération d’analyse de limiter l’opération aux seules régions modifiées et d’ignorer toutes les autres régions, ce qui optimise la durée passée à analyser l’encre.
    -   Le [**InkAnalyzer**](inkanalyzer.md) n’ignore pas complètement toutes les autres régions de la page, mais peut à la place examiner les zones voisines pour déterminer si les modifications apportées à la région modifiée affectent ces régions voisines. Par exemple, l’analyseur classe « is », dans l’exemple d’encre suivant, en tant que type **InkWord** unique de la classe [**ContextNode**](icontextnode.md) :

![manuscrit « is »](images/b0e45d31-a0e5-4157-a345-a3a32de2566e.jpg)

La suppression de la « s » donne lieu à une région modifiée (marquée d’un cadre rouge).

![manuscrit « i »](images/272a25a7-c730-40e6-b7d8-214ccbb85569.jpg)

Après l’analyse, l’analyseur change la classification de « I » en type **InkDrawing** , même si elle est en dehors de la région modifiée, car sans le trait « s » de prise en charge, l’analyseur d’encre a une chance de 50/50 de l’encre classée comme un dessin ou un mot.

-   État mis en cache en interne.

    -   Lorsqu’une application appelle une opération d’analyse en arrière-plan, [**InkAnalyzer**](inkanalyzer.md) met en cache une capture instantanée des données élaguées. En effectuant un instantané, le **InkAnalyzer** peut soit travailler sur l’analyse des données indépendamment des données utilisées par l’application, soit utiliser l’instantané comme point de comparaison pour déterminer les modifications apportées par l’application lors de l’analyse en arrière-plan.
    -   La mise en cache de l’État et la comparaison des modifications sont préférables à la conservation d’une liste de toutes les modifications qui se sont produites pour une raison principale : proxy de données. Il s’agit d’un scénario avancé décrit plus loin dans ce document, mais il implique que l’application met à jour les [**InkAnalyzer**](inkanalyzer.md) avec uniquement les données d’encre et de non-encre actuelles avant l’opération d’analyse appelée et avant le traitement des résultats d’une opération d’analyse.

## <a name="simple-ink-analysis"></a>Analyse d’encre simple

Les deux scénarios précédents (reconnaissance simple et reconnaissance incrémentielle) décrivent comment accéder aux valeurs de reconnaissance, mais ne mentionnent pas comment accéder aux résultats de l’analyse ou de la classification de l’encre. La configuration par défaut de [**InkAnalyzer**](inkanalyzer.md)exécute à la fois les algorithmes d’analyse d’encre et les algorithmes de reconnaissance. Cette configuration produit les résultats les plus précis, car les deux technologies fonctionnent ensemble pour améliorer la précision. Autrement dit, les moteurs d’analyse d’encre permettent de séparer le dessin de l’écriture et de normaliser l’écriture en angle dans un plan horizontal, qui est le plan d’entrée optimal pour les moteurs de reconnaissance.

Pour accéder aux résultats de l’analyse de l’encre, votre application utilise les méthodes [**analyze**](iinkanalyzer-analyze.md) ou [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) exactement comme décrit dans les deux scénarios de reconnaissance précédents. Rien n’est modifié, car les algorithmes d’analyse et de reconnaissance de l’encre sont déjà en cours d’exécution lorsque ces méthodes sont appelées. Toutefois, l’accès aux résultats est plus complexe que la lecture de la valeur d’une chaîne. À titre d’exemple, l’exemple de code suivant montre le regroupement et les emplacements de tous les segments **InkWord** et **InkDrawing** en affichant un rectangle autour du groupe de traits qui composent la classification.

Cet exemple utilise simplement l’événement **Paint** du formulaire pour restituer les rectangles de couleur autour des mots ou des dessins. La méthode [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) retourne une collection d’objets qui existe uniquement si l’opération d’analyse a été exécutée et les résultats contiennent des classifications avec le type [**ContextNode**](icontextnode.md) spécifié. S’il n’existe aucun **ContextNode** du type souhaité dans le document, les étapes de dessin des rectangles sont ignorées.

Chaque objet retourné par la méthode [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) aura des propriétés qui sont liées à ce type de classification. Par exemple, le **InkWordNode** fait référence à tous les traits qui composent un mot unique dans le document et référencent la chaîne reconnue pour ce mot. **InkDrawingNode** fait référence à tous les traits qui composent le dessin unique dans le document et référencent le nom de la forme pour ce dessin.

La méthode [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) est très similaire à la méthode [**DivisionResult :: ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) qui retournait des collections de [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) de types d’écriture ou de dessin.


```C++
private void Form1_Paint(object sender, PaintEventArgs e)
{
    //Setup the pen to draw
    using(Pen penBox = new Pen(Color.Red, 1))
    {
        // Find all the InkWord ContextNodes in the results
        ContextNodeCollection InkWordNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkWord);
        // For each InkWord node found, cast the ContextNode to a type specific
        // "InkWordNode" to easily access the rotated bounding box property.
        foreach (ContextNode InkWord in InkWordNodes)
        {
            //Draw the rotated bounding box.
            e.Graphics.DrawPolygon(penBox,
                    ((InkWordNode)InkWord).GetRotatedBoundingBox());
        }

        // Find all the InkDrawing ContextNodes in the results
        ContextNodeBaseCollection InkDrawingNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkDrawing);

        penBox.Color = Color.Green;

        // For each InkDrawing node found, access the node's location property to
        // draw a rectangle around the drawing.
        foreach (ContextNode InkDrawing in InkDrawingNodes)
        {
            e.Graphics.DrawRectangle(penBox, InkDrawing.Location.GetBounds());
        }
    }
}
```



Pour mettre l’exemple de code précédent en perspective, considérez l’exemple d’encre suivant :

![exemple d’encre « il s’agit d’une entrée manuscrite ». avec un cercle en dessous](images/f11cc578-d2eb-4246-af77-6bc768b0b91c.jpg)

Si vous appelez la méthode [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) et transmettez le champ static pour **InkWord**, l’analyseur retourne une collection de quatre objets **InkWordNode** :

![résultat de l’analyseur, « il s’agit d’une entrée manuscrite »](images/16ae768a-d97c-494e-9e3d-16bce1bcb432.jpg)

Si vous appelez la méthode [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) et transmettez le champ static pour **InkDrawing**, l’analyseur retourne une collection d’un objet **InkDrawingNode** :

![image représentant « Oval », le résultat de l’analyseur InkDrawing](images/624b6a53-b6b9-4ccf-9bb8-c4c5629b88cf.jpg)

Une fois l’événement **Paint** déclenché, l’exemple de code affiche des rectangles autour de chacun des objets :

![dessin original avec des rectangles rendus autour de l’objet et des mots](images/7fd9bcc3-8d7c-4cab-aa36-ba5ed78a25c0.jpg)

Cet exemple ne touche que la méthode [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) , mais comme les moteurs d’analyse d’encre peuvent détecter un ensemble plus riche de types d’encres, la méthode correspond également à tous les types de nœuds détectables par les moteurs d’analyse d’encre (tels que les lignes, les paragraphes et d’autres structures).

## <a name="using-ink-analysis-with-point-erase"></a>Utilisation de l’analyse de l’encre avec l’effacement de point

Votre application doit effectuer des ajustements dans la façon dont elle met à jour les traits lors de l’effacement de point pour garantir de bonnes performances. Tout d’abord, au niveau de la couche d’application, remplacez le point du stylet du trait existant par le point du stylet du nouveau trait, puis appelez [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) sur ce trait et mettez à jour la région modifiée avec les limites du trait. Ainsi, le [**InkAnalyzer**](inkanalyzer.md) récupère les données de trait mises à jour lors du démarrage de l’analyse d’arrière-plan suivante. Cette technique est illustrée dans l’exemple suivant.


```C++
using System;
using System.Diagnostics;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;

class PointEraseAnalysisSample : Application
{
  InkAnalyzer _analyzer;
  InkCanvas _canvas;
  bool _isPointErasing = false;
  bool _strokesManipulated = false;

  protected override void OnStartup(StartupEventArgs e)
  {
      base.OnStartup(e);
      Window win = new Window();

      _canvas = new InkCanvas();
      _canvas.Background = new LinearGradientBrush(Colors.Yellow, Colors.LightYellow, 60d);
      _canvas.EditingModeInverted = InkCanvasEditingMode.EraseByPoint;
      _canvas.Strokes.StrokesChanged += new StrokeCollectionChangedEventHandler(Strokes_StrokesChanged);
      _canvas.AddHandler(InkCanvas.MouseUpEvent, new MouseButtonEventHandler(_canvas_MouseUp), true);

      _analyzer = new InkAnalyzer(this.Dispatcher);
      _analyzer.ResultsUpdated += new ResultsUpdatedEventHandler(_analyzer_ResultsUpdated);

      win.Content = _canvas;
      win.Show();
  }

  void _analyzer_ResultsUpdated(object sender, ResultsUpdatedEventArgs e)
  {
      if (!_analyzer.DirtyRegion.IsEmpty)
      {
          _analyzer.BackgroundAnalyze();
          return;
      }

      Console.WriteLine(_analyzer.GetRecognizedString());
  }

  void _canvas_MouseUp(object sender, MouseButtonEventArgs e)
  {
      if (_isPointErasing)
      {
          _isPointErasing = false;
          _analyzer.BackgroundAnalyze();
      }
  }

  void Strokes_StrokesChanged(object sender, StrokeCollectionChangedEventArgs e)
  {
      if (_strokesManipulated)
      {
          // ignore StrokesChanged if we changed them ourselves
          _strokesManipulated = false;
          return;
      }

      if (_canvas.ActiveEditingMode == InkCanvasEditingMode.EraseByPoint &&
          e.Added.Count == 1 && e.Removed.Count == 1)
      {
          // set flag so we call BackgroundAnalyze in MouseUp
          _isPointErasing = true;

          // set flag so we ignore the next StrokesChanged
          _strokesManipulated = true;

          // replace the stylus points on the removed stroke with the added stroke
          e.Removed[0].StylusPoints = e.Added[0].StylusPoints;
          
          // force IA to update the stroke data for the removed stroke
          _analyzer.ClearStrokeData(e.Removed[0]);

          // replace the added stroke with the updated removed stroke back into InkCanvas
          _canvas.Strokes.Replace(e.Added[0], new StrokeCollection(new Stroke[] {e.Removed[0]})); 
          
          return;
      }

      if (e.Added.Count > 0)
      {
          _analyzer.AddStrokes(e.Added);
      }

      if (e.Removed.Count > 0)
      {
          _analyzer.RemoveStrokes(e.Removed);
      }

      _analyzer.BackgroundAnalyze();
  }

  [STAThread]
  static void Main(string[] args)
  {
      new PointEraseAnalysisSample().Run();
  }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Présentation de l’analyse de l’encre](ink-analysis-overview.md)
</dt> <dt>

[Utilisation de l’API analyse de l’encre](ink-analysis-api-usage.md)
</dt> </dl>

 

 
