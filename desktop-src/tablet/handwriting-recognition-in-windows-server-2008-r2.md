---
description: Windows Server 2008 R2 ajoute la prise en charge de la reconnaissance de l’écriture manuscrite côté serveur à Windows. Cette rubrique explique comment reconnaître l’écriture manuscrite dans Windows Server 2008 R2.
ms.assetid: ec22391d-a6e8-49b0-8650-943a661cbcd3
title: Reconnaissance de l’écriture manuscrite dans Windows Server 2008 R2
ms.topic: article
ms.date: 06/02/2020
ms.openlocfilehash: e014a69919c6bdc87b149f761eece14bcc3d69a4
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "104032055"
---
# <a name="handwriting-recognition-in-windows-server-2008-r2"></a>Reconnaissance de l’écriture manuscrite dans Windows Server 2008 R2

Windows Server 2008 R2 prend en charge la reconnaissance de l’écriture manuscrite côté serveur. La reconnaissance côté serveur permet à un serveur de reconnaître du contenu à partir d’une entrée de stylet sur des pages Web. Cela s’avère particulièrement utile lorsque les utilisateurs d’un réseau spécifient des termes qui sont interprétés à l’aide d’un dictionnaire personnalisé. Par exemple, si vous avez une application médicale qui a interrogé une base de données de serveur pour connaître les noms des patients, ces noms peuvent être ajoutés à une autre base de données qui serait transmise à l’aide de recherches à partir d’un formulaire Silverlight manuscrit.

## <a name="set-up-your-server-for-server-side-recognition"></a>Configurer votre serveur pour la reconnaissance Server-Side

Les étapes suivantes doivent être suivies pour configurer la reconnaissance côté serveur.

- Installer Services de prise en charge de l’écriture manuscrite
- Installer la prise en charge du serveur Web (IIS) et du serveur d’applications
- Activer le rôle expérience utilisateur
- Démarrer le service d’entrée Tablet PC

### <a name="install-ink-and-handwriting-services"></a>Installer Services de prise en charge de l’écriture manuscrite

Pour installer les services d’encre et d’écriture manuscrite, ouvrez le gestionnaire de serveur en cliquant sur l’icône Gestionnaire de serveur à partir de la barre de lancement rapide. Dans le menu **fonctionnalités** , cliquez sur **Ajouter des fonctionnalités**. Veillez à activer la case à cocher **services de prise en charge de l’écriture manuscrite** . L’illustration suivante montre la boîte de dialogue **Sélectionner des fonctionnalités** avec **services de prise en charge de l’écriture manuscrite** sélectionné.

![Case à cocher de la boîte de dialogue Sélectionner les fonctionnalités avec les services d’encre et d’écriture activée](images/setup-server-1-ink-and-handwriting.png)<br/>
*Case à cocher de la boîte de dialogue Sélectionner les fonctionnalités avec les services d’encre et d’écriture activée*

### <a name="installation-support-for-web-server-iis-and-application-server"></a>Prise en charge de l’installation du serveur Web (IIS) et du serveur d’applications

Ouvrez le gestionnaire de serveur comme vous l’avez fait pour la première étape. Ensuite, vous devrez ajouter les rôles serveur Web (IIS) et serveur d’applications. Dans le menu **rôles** , cliquez sur **Ajouter des rôles**. L’Assistant Ajout de rôles s’affiche. Cliquez sur **Suivant**. Assurez-vous que **serveur d’applications** et **serveur Web (IIS)** sont sélectionnés. L’illustration suivante montre la boîte de dialogue **Sélectionner des rôles de serveurs** avec les rôles serveur **Web (IIS)** et **serveur d’applications** sélectionnés.

![Boîte de dialogue Sélectionner des rôles de serveurs avec les rôles serveur Web (IIS) et serveur d’applications sélectionnés](images/setup-server-2-select-server-roles.png)<br/>
*Boîte de dialogue Sélectionner des rôles de serveurs avec les rôles serveur Web (IIS) et serveur d’applications sélectionnés*

Lorsque vous sélectionnez le **serveur d’applications**, vous êtes invité à installer l’infrastructure ASP.net. Cliquez sur le bouton **Ajouter les fonctionnalités requises** . Une fois que vous avez cliqué sur **suivant**, une boîte de dialogue d’aperçu s’affiche. Cliquez sur **suivant**. La boîte de dialogue **Sélectionner des services de rôle** doit maintenant être disponible. Vérifiez que **serveur Web (IIS)** est sélectionné. L’illustration suivante montre la boîte de dialogue **Sélectionner les services de rôle** avec le serveur Web (IIS) activé.

![Boîte de dialogue Sélectionner les services de rôle avec le serveur Web (IIS) activé](images/setup-server-3-select-role-services.png)<br/>
*Boîte de dialogue Sélectionner les services de rôle avec le serveur Web (IIS) activé*

Cliquez sur **Suivant**. Une boîte de dialogue vue d’ensemble s’affiche. Cliquez de nouveau sur **suivant** . Vous voyez maintenant une page proposant des options pour les rôles de serveur Web (IIS). Cliquez sur **Suivant**. Sur la page suivante, le bouton **installer** devient actif. Cliquez sur **installer** pour installer la prise en charge du serveur Web (IIS) et du serveur d’applications.

### <a name="enable-the-desktop-experience-role"></a>Activer le rôle expérience utilisateur

Pour activer la fonctionnalité expérience utilisateur, cliquez sur **Démarrer**, sur **Outils d’administration**, puis sur **Gestionnaire de serveur**. Sélectionnez **Ajouter des services** , puis sélectionnez le service **expérience utilisateur** . L’illustration suivante montre la boîte de dialogue **Sélectionner des fonctionnalités** avec l’option expérience utilisateur installée.

![Boîte de dialogue Sélectionner les fonctionnalités avec le service expérience utilisateur sélectionné](images/setup-server-4-desktop-experience.png)<br/>
*Boîte de dialogue Sélectionner les fonctionnalités avec le service expérience utilisateur sélectionné*

Cliquez sur **suivant** pour installer la fonctionnalité expérience utilisateur.

### <a name="start-the-tablet-service"></a>Démarrer le service tablette

Une fois que vous avez installé le service expérience utilisateur, le service d’entrée du Tablet PC s’affiche dans le menu **services** . Pour accéder au menu **services** , cliquez sur **Démarrer**, sur **Outils d’administration**, puis sur **services**. Pour démarrer le service, cliquez avec le bouton droit sur **service d’entrée du Tablet PC** , puis cliquez sur **Démarrer**. L’illustration suivante montre le menu **services** avec le service d’entrée Tablet PC démarré.

![Menu services avec le service d’entrée Tablet PC démarré](images/setup-server-5-tablet-pc-input-service.png)<br/>
*Menu services avec le service d’entrée Tablet PC démarré*

## <a name="performing-server-side-recognition-using-silverlight"></a>Exécution de la reconnaissance des Server-Side à l’aide de Silverlight

Cette section montre comment créer une application Web qui utilise Silverlight pour capturer une entrée d’écriture manuscrite. Pour programmer le module de reconnaissance dans Visual Studio 2008, procédez comme suit.

- Installez et mettez à jour Visual Studio 2008 pour ajouter la prise en charge de Silverlight.
- Créez un projet Silverlight dans Visual Studio 2008.
- Ajoutez les références de service nécessaires à votre projet.
- Créez un service WCF Silverlight pour la reconnaissance de l’encre.
- Ajoutez la référence de service à votre projet client.
- Ajoutez la classe InkCollector au projet InkRecognition.
- Supprimer les directives de transport sécurisées de la configuration du client

### <a name="install-and-update-visual-studio-2008-to-add-support-for-silverlight"></a>Installer et mettre à jour Visual Studio 2008 pour ajouter la prise en charge de Silverlight

Avant de commencer, vous devez effectuer les étapes suivantes sur votre serveur Windows Server 2008 R2.

- Installez Visual Studio 2008.
- Installez [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986).
- Installez le [Kit de développement logiciel (SDK) Microsoft Silverlight 5](https://www.microsoft.com/silverlight/).

Après avoir installé ces applications et mises à jour, vous êtes prêt à créer votre application Web de reconnaissance côté serveur.

### <a name="create-a-new-silverlight-web-project-in-visual-studio-2008"></a>Créer un projet Web Silverlight dans Visual Studio 2008

Dans le menu **Fichier**, cliquez sur **Nouveau projet**. Sélectionnez le modèle application Silverlight dans la \# liste projet Visual C. Nommez votre projet InkRecognition, puis cliquez sur **OK**. L’illustration suivante montre le \# projet Silverlight C sélectionné et nommé InkRecognition.

![\#projet Silverlight c sélectionné, avec le nom InkRecognition](images/project-1-new-project.png)<br/>
*\#projet Silverlight c sélectionné, avec le nom InkRecognition*

Une fois que vous avez cliqué sur **OK**, une boîte de dialogue vous invite à ajouter une application Silverlight à votre projet. Sélectionnez **Ajouter un nouveau projet Web ASP.net à la solution pour héberger Silverlight** , puis cliquez sur **OK**. L’illustration suivante montre comment configurer l’exemple de projet avant de cliquer sur **OK**.

![Boîte de dialogue avec invite pour ajouter une application Silverlight à un projet](images/project-2-add-a-new-aspnetproject.png)<br/>
*Boîte de dialogue avec invite pour ajouter une application Silverlight à un projet*

### <a name="add-the-necessary-service-references-to-your-project"></a>Ajouter les références de service nécessaires à votre projet

Vous avez maintenant votre projet client Silverlight générique (InkRecognition) avec un projet Web (InkRecognition. Web) configuré dans votre solution. Le projet s’ouvre avec page. xaml et default. aspx ouvert. Fermez ces fenêtres et ajoutez les références System. Runtime. Serialization et System. ServiceModel au projet InkRecognition en cliquant avec le bouton droit sur le dossier références dans le projet InkRecognition et en sélectionnant **Ajouter une référence**. L’illustration suivante montre la boîte de dialogue avec les références requises sélectionnées.

![Boîte de dialogue Ajouter des références avec System. Runtime. Serialization et System. ServiceModel sélectionné](images/project-3a-add-references-to-inkreco.png)<br/>
*Boîte de dialogue Ajouter des références avec System. Runtime. Serialization et System. ServiceModel sélectionné*

Ensuite, vous devez ajouter les références System. ServiceModel et Microsoft. Ink au projet InkRecognition. Web. La référence Microsoft. Ink n’apparaît pas dans les références .NET par défaut. par conséquent, recherchez Microsoft.Ink.dll dans votre dossier Windows. Une fois que vous avez localisé la DLL, ajoutez l’assembly aux références du projet : sélectionnez l’onglet **Parcourir** , accédez au dossier contenant Microsoft.Ink.dll, sélectionnez Microsoft.Ink.dll, puis cliquez sur **OK**. L’illustration suivante montre la solution du projet dans l’Explorateur Windows avec tous les assemblys de référence ajoutés.

![projet InkRecognition dans l’Explorateur Windows avec tous les assemblys de référence ajoutés](images/project-3b-with-reference-assemblies.png)<br/>
*projet InkRecognition dans l’Explorateur Windows avec tous les assemblys de référence ajoutés*

### <a name="create-a-silverlight-wcf-service-for-ink-recognition"></a>Créer un service WCF Silverlight pour la reconnaissance de l’encre

Ensuite, vous allez ajouter un service WCF pour la reconnaissance de l’encre au projet. Cliquez avec le bouton droit sur votre projet InkRecognition. Web, cliquez sur **Ajouter**, puis sur **nouvel élément**. Sélectionnez le modèle de service WCF Silverlight, remplacez le nom par InkRecogitionService, puis cliquez sur **Ajouter**. L’illustration suivante montre la boîte de dialogue **Ajouter un nouvel élément** avec le service WCF Silverlight sélectionné et nommé.

![Boîte de dialogue Ajouter un nouvel élément avec service WCF Silverlight sélectionné et nommé](images/project-4-add-wcf-service.png)<br/>
*Boîte de dialogue Ajouter un nouvel élément avec service WCF Silverlight sélectionné et nommé*

Une fois que vous avez ajouté le service WCF Silverlight, le code de service derrière, InkRecognitionService. cs, s’ouvre. Remplacez le code du service par le code suivant.

```CSharp
using System;
using System.Linq;
using System.Runtime.Serialization;
using System.ServiceModel;
using System.ServiceModel.Activation;
using System.Collections.Generic;
using System.Text;
using Microsoft.Ink;

namespace InkRecognition.Web
{
    [ServiceContract(Namespace = "")]
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class InkRecognitionService
    {
        [OperationContract]
        public string[] Recognize(int[][] packets)
        {
            // Deserialize ink.
            Ink ink = new Ink();
            Tablet tablet = new Tablets().DefaultTablet;
            TabletPropertyDescriptionCollection desc = new TabletPropertyDescriptionCollection();
            desc.Add(new TabletPropertyDescription(PacketProperty.X, tablet.GetPropertyMetrics(PacketProperty.X)));
            desc.Add(new TabletPropertyDescription(PacketProperty.Y, tablet.GetPropertyMetrics(PacketProperty.Y)));
            int numOfStrokes = packets.GetUpperBound(0) + 1;
            for (int i = 0; i < numOfStrokes; i++)
            {
                ink.CreateStroke(packets[i], desc);
            }

            // Recognize ink.
            RecognitionStatus recoStatus;
            RecognizerContext recoContext = new RecognizerContext();
            recoContext.RecognitionFlags = RecognitionModes.LineMode | RecognitionModes.TopInkBreaksOnly;
            recoContext.Strokes = ink.Strokes;
            RecognitionResult recoResult = recoContext.Recognize(out recoStatus);
            RecognitionAlternates alternates = recoResult.GetAlternatesFromSelection();
            string[] results = new string[alternates.Count];
            for (int i = 0; i < alternates.Count; i++)
            {
                results[i] = alternates[i].ToString();
            }

            // Send results to client.
            return results;
        }
    }
}
```

### <a name="add-the-service-reference-to-your-client-project"></a>Ajouter la référence de service à votre projet client

Maintenant que vous disposez de votre service WCF Silverlight pour InkRecognition, vous utiliserez le service à partir de votre application cliente. Cliquez avec le bouton droit sur le projet InkRecognition, puis sélectionnez **Ajouter une référence de service**. Dans la boîte de dialogue **Ajouter une référence de service** qui s’affiche, sélectionnez **découvrir** pour découvrir les services de la solution actuelle. InkRecognitionService s’affiche dans le volet services. Double-cliquez sur InkRecognitionService dans le volet services, remplacez l’espace de noms par InkRecognitionServiceReference, puis cliquez sur **OK**. L’illustration suivante montre la boîte de dialogue **Ajouter une référence de service** avec l’option InkRecognitionService sélectionnée et l’espace de noms modifié.

![Boîte de dialogue Ajouter une référence de service avec inkrecognitionservice sélectionné et espace de noms modifié](images/project-5-discover-service-reference.png)<br/>
*Boîte de dialogue Ajouter une référence de service avec inkrecognitionservice sélectionné et espace de noms modifié*

### <a name="add-the-inkcollector-class-to-the-inkrecognition-project"></a>Ajouter la classe InkCollector au projet InkRecognition

Cliquez avec le bouton droit sur le projet InkRecognition, cliquez sur **Ajouter**, puis sur **nouvel élément**. Dans le menu **Visual \# c** , sélectionnez **c \# classe**. Nommez la classe InkCollector. L’illustration suivante montre la boîte de dialogue avec la \# classe C sélectionnée et nommée.

![Boîte de dialogue Ajouter un nouvel élément avec la \# classe c sélectionnée et nommée](images/project-6-add-ink-collector.png)<br/>
*Boîte de dialogue Ajouter un nouvel élément avec la \# classe c sélectionnée et nommée*

Une fois que vous avez ajouté la classe InkCollector, la définition de classe s’ouvre. Remplacez le code dans le collecteur d’encre par le code suivant.

```CSharp
using System;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Documents;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;

namespace InkRecognition
{
    public class InkCollector : IDisposable
    {
        public InkCollector(InkPresenter presenter)
        {
            _presenter = presenter;
            _presenter.Cursor = Cursors.Stylus;
            _presenter.MouseLeftButtonDown += new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove += new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp += new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
        }

        void _presenter_MouseLeftButtonDown(object sender, MouseButtonEventArgs e)
        {
            _presenter.CaptureMouse();
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
                _stroke = new Stroke(e.StylusDevice.GetStylusPoints(_presenter));
                _stroke.DrawingAttributes = _drawingAttributes;
                _presenter.Strokes.Add(_stroke);
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
                _erasePoints = e.StylusDevice.GetStylusPoints(_presenter);
            }
        }

        void _presenter_MouseMove(object sender, MouseEventArgs e)
        {
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
            }
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            else if (_erasePoints != null)
            {
                _erasePoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
                StrokeCollection hitStrokes = _presenter.Strokes.HitTest(_erasePoints);
                if (hitStrokes.Count > 0)
                {
                    foreach (Stroke hitStroke in hitStrokes)
                    {
                        _presenter.Strokes.Remove(hitStroke);
                    }
                }
            }
        }

        void _presenter_MouseLeftButtonUp(object sender, MouseButtonEventArgs e)
        {
            _presenter.ReleaseMouseCapture();
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            _stroke = null;
            _erasePoints = null;
        }

        public DrawingAttributes DefaultDrawingAttributes
        {
            get { return _drawingAttributes; }
            set { _drawingAttributes = value; }
        }

        public void Dispose()
        {
            _presenter.MouseLeftButtonDown -= new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove -= new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp -= new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
            _presenter = null;
        }

        private InkPresenter _presenter = null;
        private Stroke _stroke = null;
        private StylusPointCollection _erasePoints = null;
        private DrawingAttributes _drawingAttributes = new DrawingAttributes();
    }
}
```

### <a name="update-the-xaml-for-the-default-page-and-add-a-code-behind-for-handwriting-recognition"></a>Mettre à jour le XAML pour la page par défaut et ajouter un code-behind pour la reconnaissance de l’écriture manuscrite

Maintenant que vous avez une classe qui collecte de l’encre, vous devez mettre à jour le XAML dans page. XAML avec le code XAML suivant. Le code suivant ajoute un dégradé jaune à la zone d’entrée, un contrôle InkCanvas et un bouton qui déclenche la reconnaissance.

```XML
<UserControl x:Class="InkRecognition.Page"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" 
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
    <Grid x:Name="LayoutRoot" Background="White">
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
        </Grid.RowDefinitions>
        <Border Margin="5" Grid.Row="0" BorderThickness="4" BorderBrush="Black" CornerRadius="5" Height="200">
            <Grid>
                <InkPresenter x:Name="inkCanvas">
                    <InkPresenter.Background>
                        <LinearGradientBrush StartPoint="0.5,0" EndPoint="0.5,1">
                            <GradientStop Offset="0" Color="Yellow"/>
                            <GradientStop Offset="1" Color="LightYellow"/>
                        </LinearGradientBrush>
                    </InkPresenter.Background>
                </InkPresenter>
                <Button Grid.Row="0" HorizontalAlignment="Right" VerticalAlignment="Bottom" Margin="10" Content="Recognize" Click="RecoButton_Click"/>
            </Grid>
        </Border>
        <Grid Grid.Row="1">
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="Auto"/>
                <ColumnDefinition Width="*"/>
            </Grid.ColumnDefinitions>
            <TextBlock Grid.Column="0" FontSize="28" Text="Result: "/>
            <ComboBox x:Name="results" Grid.Column="1" FontSize="28"/>
        </Grid>
    </Grid>
</UserControl>
```

Remplacez la page code-behind, page. Xaml. cs, par le code suivant, qui ajoute un gestionnaire d’événements pour le bouton **Recognize** .

```CSharp
using System;
using System.Collections.Generic;
using System.Collections.ObjectModel;
using System.Linq;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;
using InkRecognition.InkRecognitionServiceReference;

namespace InkRecognition
{
    public partial class Page : UserControl
    {
        public Page()
        {
            InitializeComponent();
            inkCol = new InkCollector(inkCanvas);
            recoClient = new InkRecognitionServiceClient();
            recoClient.RecognizeCompleted += new EventHandler<RecognizeCompletedEventArgs>(recoClient_RecognizeCompleted);
        }

        private void RecoButton_Click(object sender, RoutedEventArgs e)
        {
            // Serialize the ink into an array on ints.
            ObservableCollection<ObservableCollection<int>> packets = new ObservableCollection<ObservableCollection<int>>();
            double pixelToHimetricMultiplier = 2540d / 96d;

            foreach (Stroke stroke in inkCanvas.Strokes)
            {
                packets.Add(new ObservableCollection<int>());
                int index = inkCanvas.Strokes.IndexOf(stroke);
                for (int i = 0; i < stroke.StylusPoints.Count; i += 2)
                {
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].X * pixelToHimetricMultiplier));
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].Y * pixelToHimetricMultiplier));
                }
            }

            // Call the Web service.
            recoClient.RecognizeAsync(packets);
        }

        void recoClient_RecognizeCompleted(object sender, RecognizeCompletedEventArgs e)
        {
            // We have received results from the server, now display them.
            results.ItemsSource = e.Result;
            UpdateLayout();
            results.SelectedIndex = 0;
            inkCanvas.Strokes.Clear();
        }

        private InkRecognitionServiceClient recoClient = null;
        private InkCollector inkCol = null;
    }
}
```

### <a name="remove-secure-transport-directives-from-the-client-configuration"></a>Supprimer les directives de transport sécurisées de la configuration du client

Avant de pouvoir utiliser le service WCF, vous devez supprimer toutes les options de transport sécurisées de la configuration du service, car les transports sécurisés ne sont actuellement pas pris en charge dans les services WCF 2,0 de Silverlight. À partir du projet InkRecognition, mettez à jour les paramètres de sécurité dans ServiceReferences. ClientConfig. Modifier le code XML de sécurité

```XML
          <security mode="None">
            <transport>
              <extendedProtectionPolicy policyEnforcement="WhenSupported" />
            </transport>
          </security>
```

to

```XML
       <security mode="None"/>
```

À présent, votre application doit s’exécuter. L’illustration suivante montre comment l’application recherche dans awebpagewith une écriture manuscrite entrée dans la zone reconnaissance.

![Application dans awebpagewith une entrée manuscrite entrée dans la zone de reconnaissance](images/demo-1.png)<br/>
*Application dans awebpagewith une entrée manuscrite entrée dans la zone de reconnaissance*

L’illustration suivante montre le texte reconnu dans la liste déroulante de **résultats** .

![Application dans awebpagewith texte reconnu dans la liste déroulante des résultats](images/demo-2.png)<br/>
*Application dans awebpagewith texte reconnu dans la liste déroulante des résultats*

 

 



