---
description: L’exemple d’application de blog Ink montre comment créer une classe UserControl managée qui dispose de la fonctionnalité d’encrage et héberger ce contrôle dans Microsoft Internet Explorer.
ms.assetid: b6c3ad92-3ab1-4311-b318-13939e1a1a5a
title: Exemple de blog manuscrit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24f132d355a95c9cb8debebe074df3f976e3b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112319"
---
# <a name="ink-blog-web-sample"></a>Exemple de blog manuscrit

L’exemple d’application de blog Ink montre comment créer une classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) managée qui dispose de la fonctionnalité d’encrage et héberger ce contrôle dans Microsoft Internet Explorer. L’exemple illustre également une technique permettant d’envoyer des données d’encre sur un réseau à l’aide du protocole HTTP et de conserver l’encre sur un serveur.

> [!Note]  
> Pour exécuter cet exemple, vous devez disposer de Microsoft Internet Information Services (IIS) avec ASP.NET installé. Assurez-vous que votre ordinateur répond à la configuration requise pour que les applications ASP.NET s’exécutent sur votre ordinateur.

 

> [!Note]  
> Si vous exécutez cet exemple sur un ordinateur qui n’est pas un Tablet PC avec Microsoft Windows XP Tablet PC Edition Kit de développement 1,7 installé, la fonctionnalité de reconnaissance de texte pour le titre de l’encre ne fonctionnera pas. Cela est dû au fait qu’un ordinateur non Tablet PC avec le kit de développement logiciel (SDK) Tablet PC 1,7 installé ne contient pas de module de reconnaissance. Le reste de l’application fonctionne comme décrit.

 

## <a name="overview"></a>Vue d’ensemble

L’exemple de blog Ink crée un weblog avec écriture manuscrite. InkBlogWeb est une application ASP.NET. L’entrée manuscrite est effectuée au moyen d’un contrôle utilisateur référencé à partir d’une page ASP.NET.

Le contrôle utilisateur détecte si les composants de la plateforme Tablet PC sont installés sur l’ordinateur client. Si c’est le cas, le contrôle utilisateur présente à l’utilisateur deux zones compatibles avec l’écriture manuscrite sur la page Web : une pour l’entrée manuscrite d’un titre pour l’entrée de blog et une pour le corps de l’entrée. Si les composants de plateforme Tablet PC ne sont pas installés, l’utilisateur reçoit un contrôle de zone de texte standard pour le titre et le corps de l’entrée.

Lorsque l’utilisateur a terminé de créer l’entrée, il clique sur un bouton, ajouter un blog, et la publication est envoyée au serveur Web pour le stockage. Sur le serveur, l’application enregistre le texte du titre et la date de publication, ainsi qu’une référence à un fichier GIF (Graphics Interchange Format). Le fichier GIF, également enregistré sur le serveur, contient les données d’encre du corps d’un fichier GIF viné. Pour plus d’informations sur le format GIF viné, consultez [stockage de l’encre en HTML](storing-ink-in-html.md).

Il existe deux projets dans la solution InkBlog : le projet **InkBlogControls** et le projet **InkBlogWeb** .

## <a name="inkblogcontrols-project"></a>Projet InkBlogControls

Le projet **InkBlogControls** est un projet [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) qui contient le code pour le contrôle utilisateur qui active l’écriture manuscrite sur la page Web. Le code pour ce contrôle, le contrôle InkArea, se trouve dans le fichier InkArea. cs.

La `InkArea` classe hérite de la classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) . Le constructeur pour le `InkArea` contrôle appelle une méthode d’assistance, `CreateInkCollectionSurface` .


```C++
public InkArea()
{
    // Standard template code

    try
    {
        inputArea = CreateInkCollectionSurface();
    }
    catch (FileNotFoundException)
    { 
        inputArea = new TextBox();
        ((TextBox)inputArea).Multiline = true;
    }

    inputArea.Size = this.Size;

    // Add the control used for collecting blog input
    this.Controls.Add(inputArea);
}
```



La `CreateInkCollectionSurface` méthode détermine si les composants d’encrage du Tablet PC sont disponibles sur le client en tentant de créer une instance de la classe [InkCollector](/previous-versions/ms583683(v=vs.100)) . Si l’appel à la `CreateInkCollectionSurface` méthode s’effectue correctement, la méthode retourne un objet [panneau](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) comme contrôle.


```C++
protected Control CreateInkCollectionSurface()
{
    try
    {
        Panel inkPanel = new Panel();
        inkPanel.BorderStyle = BorderStyle.Fixed3D;
        inkCollector = new InkCollector(inkPanel);
        ((InkCollector)inkCollector).Enabled = true;
        return inkPanel;
    }
    catch
    {
        throw;
    }
}
```



Si le constructeur échoue parce que les fichiers de plateforme d’écriture manuscrite sont introuvables, le `InputArea` contrôle est instancié en tant que contrôle [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) plutôt qu’en tant que contrôle [InkCollector](/previous-versions/ms583683(v=vs.100)) . Le constructeur dimensionne ensuite le contrôle à la taille du contrôle utilisateur parent et l’ajoute à la collection de contrôles du parent.

La classe de contrôle InkArea implémente trois propriétés publiques intéressantes : InkData, TextData et webactived.

La propriété InkData est en lecture seule et fournit l’accès aux données sérialisées de l’encre, si le client prend en charge l’écriture manuscrite. Si le client ne prend pas en charge l’entrée manuscrite, la propriété InkData obtient une chaîne vide. La propriété InkData appelle une méthode d’assistance, SerializeInkData, pour déterminer si le client prend en charge l’écriture manuscrite.


```C++
protected String SerializeInkData()
{
    Debug.Assert(InkEnabled, null, "Client must be ink-enabled");

    // Obtain the ink associated with this control
    Ink ink = ((InkCollector)inkCollector).Ink;

    // Serialize the ink
    if (ink.Strokes.Count > 0) 
    {
        byte[] inkDataBytes = ink.Save(PersistenceFormat.Gif);
        return Convert.ToBase64String(inkDataBytes);
    }

    // Default to returning the empty string.
    return String.Empty;
}
```



Dans la `SerializeInkData` méthode, le cast en [InkCollector](/previous-versions/ms583683(v=vs.100)) est nécessaire lors de l’obtention de l’objet [Ink](/previous-versions/ms583670(v=vs.100)) , car `inputArea` est déclaré en tant que [contrôle](/dotnet/api/system.windows.forms.control?view=netcore-3.1). Si l’objet Ink contient des traits, les données d’entrée manuscrite sont enregistrées dans le `inkDataBytes` tableau d’octets sous la forme d’un fichier GIF (spécifié à l’aide de la valeur d’énumération [PersistenceFormat](/previous-versions/ms552503(v=vs.100)) ). La méthode convertit ensuite le tableau d’octets en une chaîne encodée en base64 et retourne cette chaîne.

En supposant que le client puisse effectuer la reconnaissance, la `TextData` propriété retourne l’objet [RecognitionResult](/previous-versions/ms552537(v=vs.100)) à partir du passage des données de l’encre à un module de reconnaissance de l’écriture manuscrite. Si le client ne prend pas en charge l’écriture manuscrite, le contenu de la zone de texte est retourné, comme indiqué dans le code suivant.


```C++
public string TextData
{
    get
    {
        if (this.WebEnabled) 
        {
            return RecognizeInkData();
        }
        else
        {
            return ((TextBox)inputArea).Text;
        }
    }
}
```



La `TextData` propriété appelle une méthode d’assistance, `RecognizeInkData` , illustrée dans le code suivant, pour effectuer la reconnaissance. Lorsque les moteurs de reconnaissance sont présents sur le système, la `RecognizeInkData` méthode retourne une chaîne contenant la propriété de la [chaîne](/previous-versions/ms572009(v=vs.100)) de l’objet [RecognitionResult](/previous-versions/ms552537(v=vs.100)) . Sinon, la fonction retourne une chaîne vide.


```C++
protected String RecognizeInkData()
{
    // Obtain the ink associated with this control
    Ink ink = ((InkCollector)inkCollector).Ink;

    if (ink.Strokes.Count > 0) 
    {

        // Attempt to create a recognition context and use it to
        // retrieve the top alternate.
        try 
        {
            RecognizerContext recognizerContext = new RecognizerContext();
            RecognitionStatus recognitionStatus;
            recognizerContext.Strokes = ink.Strokes;
            RecognitionResult recognitionResult = recognizerContext.Recognize(out recognitionStatus);
            if (recognitionStatus == RecognitionStatus.NoError) && ( null != recognitionResult) )
            {
                return recognitionResult.TopString;
            }
        }
        catch (Exception)
        {
            // An exception will occur if the client does not have
            // any handwriting recognizers installed on their system.
            // In this case, we default to returning an empty string. 
        }
    }

    return String.Empty;
}
```



La `InkEnabled` propriété est une valeur booléenne en lecture seule qui indique si l’entrée manuscrite est prise en charge sur l’ordinateur client.

Un autre membre public important de la `InkArea` classe de contrôle est la `DisposeResources` méthode. Cette méthode appelle en interne la `Dispose` méthode pour s’assurer que toutes les ressources exploitées par le contrôle utilisateur sont nettoyées. Toute application qui utilise le `InkArea` contrôle doit appeler la `DisposeResources` méthode lorsqu’elle a fini d’utiliser le contrôle.

## <a name="inkblogweb-project"></a>Projet InkBlogWeb

Le projet InkBlogWeb est un projet de déploiement d’installation Web qui référence le `InkArea` contrôle pour fournir la fonctionnalité de blog. Pour plus d’informations sur les projets de déploiement de l’installation Web, consultez [déploiement d’un projet d’installation Web](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).

Il existe deux fichiers. aspx qui implémentent l’exemple de blog : default. aspx et AddBlog. aspx. Default. aspx est la page par défaut de l’application InkBlogWeb. Le fichier code-behind de cette page est default. aspx. cs. Cette page fournit un lien vers la page contenant le nouveau formulaire de saisie de blog et affiche les entrées de blog existantes. Ce processus est décrit ultérieurement, après l’examen suivant de la page du nouveau formulaire de saisie de blog, AddBlog. aspx.

AddBlog. aspx et son fichier code-behind, AddBlog. aspx. cs, contiennent la logique et le code de l’interface utilisateur permettant de créer des entrées de blog. AddBlox. aspx fait référence à deux instances de la classe de contrôle InkArea créée dans le projet InkBlogControls à l’aide de l’élément objet HTML, comme indiqué dans l’exemple suivant. Une instance a un `id` attribut de inkBlogTitle et l’autre a un attribut d’ID de inkBlogBody.

`<OBJECT id="inkBlogTitle" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="48" VIEWASTEXT>``</OBJECT>``<br/>``<OBJECT id="inkBlogBody" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="296" VIEWASTEXT>``</OBJECT>`

L’assembly de InkBlogControls.dll doit être présent dans le même répertoire que la page. aspx qui y fait référence. Le projet de déploiement de l’installation Web garantit que c’est le cas, tel qu’il est prouvé par la présence de l’élément « sortie principale de InkBlogControls » dans le projet de déploiement.

Le contrôle titre est uniquement de 48 pixels de haut pour faciliter l’entrée d’une seule ligne d’encre pour le titre. Le contrôle du corps est de 296 pixels de haut pour faire de la place pour les entrées de blog plus grandes de plusieurs lignes ou des dessins.

Les contrôles InkArea sont connectés à une fonction de script côté client, AddBlog, au moyen du gestionnaire d’événements OnClick d’un élément BUTTON HTML standard.

`<button id="BUTTON1" type="button" onclick="AddBlog()">Add Blog</button>`

Il existe également un formulaire HTML sur la page qui contient trois éléments d’entrée masqués : BlogTitleText, BlogBodyText et BlogBodyInkData. Ce formulaire est utilisé pour replacer les données de l’entrée de blog sur le serveur. AddBlog. aspx est le gestionnaire de publication défini pour le formulaire.

La fonction AddBlog-écrite dans Microsoft JScript <entity type="reg"/> : extrait les données de blog à partir des contrôles InkArea et publie les résultats sur le serveur.


```C++
function AddBlog() 
{
    // Extract the blog's title data as ink and text
    form.BlogTitleText.value  = inkBlogTitle.TextData;
    
    // Extract the blog's body data as ink and text
    form.BlogBodyText.value = inkBlogBody.TextData;
    form.BlogBodyInkData.value = inkBlogBody.InkData;   

    form.submit();
}
```



Lorsque les données arrivent sur le serveur, le code dans AddBlog. aspx. cs vérifie le \_ Gestionnaire d’événements de chargement de page pour voir si la propriété Form de l’objet HttpRequest contient des données. Si c’est le cas, il crée un nom de fichier basé sur l’heure système actuelle, place les données du formulaire dans trois variables de chaîne et écrit les données dans un fichier HTML et un fichier GIF contenant les données d’encre, le cas échéant, comme indiqué dans le code suivant.


```C++
if ( (String.Empty != inkBody) )
{           
    // Use helper method to create a GIF image file from ink data 
    CreateGif(imagePath, fileName, inkBody);
    
    // Create an HTML fragment to reference the image file
    content = "<img src=\"Blogs/Images/" + fileName + ".gif\"></img>";
}                
else 
{
    // If no ink data is available create an HTML fragment that contains
    // the blog's text directly.
    content = "<P>" + textBody + "</P>";
}

// Use helper method to create the blog web page on the server
CreateHtm(blogPath, fileName, blogTitle, content);
```



Pour plus d’informations sur les méthodes d’assistance, reportez-vous à l’exemple de code source.

## <a name="running-the-sample"></a>Exécution de l'exemple

Le kit de développement logiciel (SDK) Tablet PC 1,7 installe l’exemple Web de blog Ink par défaut. Pour exécuter l’exemple, dans Internet Explorer, accédez à https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx . Si vous exécutez Windows Server 2003, remplacez « localhost » par le nom de votre ordinateur.

> [!Note]  
> Les exemples Web compilés ne sont pas installés par l’option d’installation par défaut pour le kit de développement logiciel (SDK). Vous devez effectuer une installation personnalisée et sélectionner la sous-option « exemples Web précompilés » pour les installer.

 

Vous pouvez également exécuter l’exemple en ouvrant et en générant le projet dans Microsoft Visual Studio <entity type="reg"/> .net, puis en le déployant sur un ordinateur distinct qui exécute IIS.

## <a name="troubleshooting-the-sample"></a>Résolution des problèmes liés à l'exemple

Trois zones qui peuvent engendrer des difficultés lors de l’exécution ou de l’hébergement de l’exemple sont les autorisations et la reconnaissance.

### <a name="permissions"></a>Autorisations

L’exemple requiert des autorisations d’écriture dans le dossier racine virtuel pour le compte qui tente de créer une entrée de blog. Par défaut, la version compilée de l’exemple fourni dans le kit de développement logiciel (SDK) Tablet PC 1,7 dispose des autorisations appropriées pour répondre à cette exigence.

Si vous générez et déployez l’exemple à l’aide du projet de déploiement de l’installation Web fourni, vous devez accorder au groupe% MACHINENAME% \\ Users l’accès en écriture au dossier du système de fichiers désigné par la racine virtuelle InkBlogWeb (par exemple, C : \\ Inetpub \\ wwwroot \\ InkBlogWeb). Le groupe utilisateurs comprend le compte anonyme utilisé par IIS, ce qui permet à l’application ASP.NET d’écrire les nouvelles entrées de blog dans le système de fichiers. Une alternative consiste à supprimer l’accès anonyme à la racine virtuelle et à forcer l’authentification.

### <a name="recognition"></a>Reconnaissance

Les détecteurs d’écriture manuscrite doivent être installés afin de reconnaître l’encre dans le titre du blog. Si vous accédez à l’application InkBlog à partir d’un ordinateur équipé d’un système d’exploitation autre que Windows XP Édition Tablet PC, mais avec le kit de développement logiciel (SDK) Tablet PC 1,7 installé, vous pouvez écrire dans les contrôles InkArea, mais les moteurs de reconnaissance ne sont pas présents et aucun titre ne s’affiche pour vos entrées de blog. Toutefois, le contenu de l’encre dans le corps apparaît toujours.

### <a name="machine-configuration"></a>Configuration de l’ordinateur

Si vous avez installé ASP.NET et le .NET Framework sur un ordinateur et que vous désinstallez puis réinstallez IIS, les mappages de script échouent et ASP.NET ne fonctionnera pas. Dans ce cas, vous pouvez réparer les mappages de script ASP.NET à l’aide de l’outil d’inscription ASP.NET IIS (ASPNET \_regiis.exe-i).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Collecte](/previous-versions/ms583683(v=vs.100))
</dt> <dt>

[Entrée manuscrite sur le Web](ink-on-the-web.md)
</dt> <dt>

[Formats de données manuscrites](ink-data-formats.md)
</dt> <dt>

[System. Windows. Forms. UserControl (classe)](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)
</dt> </dl>

 

 
