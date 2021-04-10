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
# <a name="ink-blog-web-sample"></a><span data-ttu-id="7f290-103">Exemple de blog manuscrit</span><span class="sxs-lookup"><span data-stu-id="7f290-103">Ink Blog Web Sample</span></span>

<span data-ttu-id="7f290-104">L’exemple d’application de blog Ink montre comment créer une classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) managée qui dispose de la fonctionnalité d’encrage et héberger ce contrôle dans Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="7f290-104">The Ink Blog sample application demonstrates how to create a managed [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class that has inking capability and host that control in Microsoft Internet Explorer.</span></span> <span data-ttu-id="7f290-105">L’exemple illustre également une technique permettant d’envoyer des données d’encre sur un réseau à l’aide du protocole HTTP et de conserver l’encre sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="7f290-105">The sample also demonstrates one technique for sending ink data across a network by using HTTP and for persisting ink on a server.</span></span>

> [!Note]  
> <span data-ttu-id="7f290-106">Pour exécuter cet exemple, vous devez disposer de Microsoft Internet Information Services (IIS) avec ASP.NET installé.</span><span class="sxs-lookup"><span data-stu-id="7f290-106">You must have Microsoft Internet Information Services (IIS) with ASP.NET installed to run this sample.</span></span> <span data-ttu-id="7f290-107">Assurez-vous que votre ordinateur répond à la configuration requise pour que les applications ASP.NET s’exécutent sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7f290-107">Make sure that your computer meets the requirements necessary for ASP.NET applications to run on your computer.</span></span>

 

> [!Note]  
> <span data-ttu-id="7f290-108">Si vous exécutez cet exemple sur un ordinateur qui n’est pas un Tablet PC avec Microsoft Windows XP Tablet PC Edition Kit de développement 1,7 installé, la fonctionnalité de reconnaissance de texte pour le titre de l’encre ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="7f290-108">If you run this sample on a non-Tablet PC computer with the Microsoft Windows XP Tablet PC Edition Development Kit 1.7 installed the text recognition feature for the ink title will not function.</span></span> <span data-ttu-id="7f290-109">Cela est dû au fait qu’un ordinateur non Tablet PC avec le kit de développement logiciel (SDK) Tablet PC 1,7 installé ne contient pas de module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="7f290-109">This occurs because a non-Tablet PC computer with the Tablet PC SDK 1.7 installed lacks recognizers.</span></span> <span data-ttu-id="7f290-110">Le reste de l’application fonctionne comme décrit.</span><span class="sxs-lookup"><span data-stu-id="7f290-110">The rest of the application performs as described.</span></span>

 

## <a name="overview"></a><span data-ttu-id="7f290-111">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="7f290-111">Overview</span></span>

<span data-ttu-id="7f290-112">L’exemple de blog Ink crée un weblog avec écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="7f290-112">The Ink Blog sample creates an ink-enabled Weblog.</span></span> <span data-ttu-id="7f290-113">InkBlogWeb est une application ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="7f290-113">InkBlogWeb is an ASP.NET application.</span></span> <span data-ttu-id="7f290-114">L’entrée manuscrite est effectuée au moyen d’un contrôle utilisateur référencé à partir d’une page ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="7f290-114">Ink entry is accomplished by means of a user control that is referenced from an ASP.NET page.</span></span>

<span data-ttu-id="7f290-115">Le contrôle utilisateur détecte si les composants de la plateforme Tablet PC sont installés sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="7f290-115">The user control detects whether the Tablet PC platform components are installed on the client computer.</span></span> <span data-ttu-id="7f290-116">Si c’est le cas, le contrôle utilisateur présente à l’utilisateur deux zones compatibles avec l’écriture manuscrite sur la page Web : une pour l’entrée manuscrite d’un titre pour l’entrée de blog et une pour le corps de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="7f290-116">If so, the user control presents the user with two ink-enabled areas on the Web page: one for inking a title for the blog entry and one for the body of the entry.</span></span> <span data-ttu-id="7f290-117">Si les composants de plateforme Tablet PC ne sont pas installés, l’utilisateur reçoit un contrôle de zone de texte standard pour le titre et le corps de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="7f290-117">If the Tablet PC Platform components are not installed, then the user is given a standard text box control for the title and body of the entry.</span></span>

<span data-ttu-id="7f290-118">Lorsque l’utilisateur a terminé de créer l’entrée, il clique sur un bouton, ajouter un blog, et la publication est envoyée au serveur Web pour le stockage.</span><span class="sxs-lookup"><span data-stu-id="7f290-118">When the user finishes creating the entry, she clicks a button, Add Blog, and the post is sent to the Web server for storage.</span></span> <span data-ttu-id="7f290-119">Sur le serveur, l’application enregistre le texte du titre et la date de publication, ainsi qu’une référence à un fichier GIF (Graphics Interchange Format).</span><span class="sxs-lookup"><span data-stu-id="7f290-119">On the server, the application saves the title text and posting date, as well as a reference to a Graphics Interchange Format (GIF) file.</span></span> <span data-ttu-id="7f290-120">Le fichier GIF, également enregistré sur le serveur, contient les données d’encre du corps d’un fichier GIF viné.</span><span class="sxs-lookup"><span data-stu-id="7f290-120">The GIF file, also saved to the server, contains the ink data from the body in a fortified GIF file.</span></span> <span data-ttu-id="7f290-121">Pour plus d’informations sur le format GIF viné, consultez [stockage de l’encre en HTML](storing-ink-in-html.md).</span><span class="sxs-lookup"><span data-stu-id="7f290-121">For more information about the fortified GIF format, see [Storing Ink in HTML](storing-ink-in-html.md).</span></span>

<span data-ttu-id="7f290-122">Il existe deux projets dans la solution InkBlog : le projet **InkBlogControls** et le projet **InkBlogWeb** .</span><span class="sxs-lookup"><span data-stu-id="7f290-122">There are two projects in the InkBlog solution: the **InkBlogControls** project and the **InkBlogWeb** project.</span></span>

## <a name="inkblogcontrols-project"></a><span data-ttu-id="7f290-123">Projet InkBlogControls</span><span class="sxs-lookup"><span data-stu-id="7f290-123">InkBlogControls Project</span></span>

<span data-ttu-id="7f290-124">Le projet **InkBlogControls** est un projet [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) qui contient le code pour le contrôle utilisateur qui active l’écriture manuscrite sur la page Web.</span><span class="sxs-lookup"><span data-stu-id="7f290-124">The **InkBlogControls** project is a [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) project that contains the code for the user control that enables inking on the Web page.</span></span> <span data-ttu-id="7f290-125">Le code pour ce contrôle, le contrôle InkArea, se trouve dans le fichier InkArea. cs.</span><span class="sxs-lookup"><span data-stu-id="7f290-125">The code for this control, the InkArea control, is in the InkArea.cs file.</span></span>

<span data-ttu-id="7f290-126">La `InkArea` classe hérite de la classe [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="7f290-126">The `InkArea` Class inherits from the [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class.</span></span> <span data-ttu-id="7f290-127">Le constructeur pour le `InkArea` contrôle appelle une méthode d’assistance, `CreateInkCollectionSurface` .</span><span class="sxs-lookup"><span data-stu-id="7f290-127">The constructor for the `InkArea` control calls a helper method, `CreateInkCollectionSurface`.</span></span>


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



<span data-ttu-id="7f290-128">La `CreateInkCollectionSurface` méthode détermine si les composants d’encrage du Tablet PC sont disponibles sur le client en tentant de créer une instance de la classe [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="7f290-128">The `CreateInkCollectionSurface` method determines whether the Tablet PC inking components are available on the client by attempting to create an instance of the [InkCollector](/previous-versions/ms583683(v=vs.100)) class.</span></span> <span data-ttu-id="7f290-129">Si l’appel à la `CreateInkCollectionSurface` méthode s’effectue correctement, la méthode retourne un objet [panneau](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) comme contrôle.</span><span class="sxs-lookup"><span data-stu-id="7f290-129">If the call to the `CreateInkCollectionSurface` method succeeds, the method returns a [Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) object as the control.</span></span>


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



<span data-ttu-id="7f290-130">Si le constructeur échoue parce que les fichiers de plateforme d’écriture manuscrite sont introuvables, le `InputArea` contrôle est instancié en tant que contrôle [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) plutôt qu’en tant que contrôle [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="7f290-130">If the constructor fails because the inking platform files are not found, then the `InputArea` control is instantiated as a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) control rather than a [InkCollector](/previous-versions/ms583683(v=vs.100)) control.</span></span> <span data-ttu-id="7f290-131">Le constructeur dimensionne ensuite le contrôle à la taille du contrôle utilisateur parent et l’ajoute à la collection de contrôles du parent.</span><span class="sxs-lookup"><span data-stu-id="7f290-131">The constructor then sizes the control to the size of the parent user control and adds it to the parent's Controls collection.</span></span>

<span data-ttu-id="7f290-132">La classe de contrôle InkArea implémente trois propriétés publiques intéressantes : InkData, TextData et webactived.</span><span class="sxs-lookup"><span data-stu-id="7f290-132">The InkArea control class implements three interesting public properties: InkData, TextData, and WebEnabled.</span></span>

<span data-ttu-id="7f290-133">La propriété InkData est en lecture seule et fournit l’accès aux données sérialisées de l’encre, si le client prend en charge l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="7f290-133">The InkData property is read-only and provides access to the serialized ink data, if the client supports inking.</span></span> <span data-ttu-id="7f290-134">Si le client ne prend pas en charge l’entrée manuscrite, la propriété InkData obtient une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="7f290-134">If the client does not support inking, the InkData property gets an empty string.</span></span> <span data-ttu-id="7f290-135">La propriété InkData appelle une méthode d’assistance, SerializeInkData, pour déterminer si le client prend en charge l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="7f290-135">The InkData property calls a helper method, SerializeInkData, to determine if the client supports inking.</span></span>


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



<span data-ttu-id="7f290-136">Dans la `SerializeInkData` méthode, le cast en [InkCollector](/previous-versions/ms583683(v=vs.100)) est nécessaire lors de l’obtention de l’objet [Ink](/previous-versions/ms583670(v=vs.100)) , car `inputArea` est déclaré en tant que [contrôle](/dotnet/api/system.windows.forms.control?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="7f290-136">In the `SerializeInkData` method, the cast to [InkCollector](/previous-versions/ms583683(v=vs.100)) is necessary when obtaining the [Ink](/previous-versions/ms583670(v=vs.100)) object, because `inputArea` is declared as a [Control](/dotnet/api/system.windows.forms.control?view=netcore-3.1).</span></span> <span data-ttu-id="7f290-137">Si l’objet Ink contient des traits, les données d’entrée manuscrite sont enregistrées dans le `inkDataBytes` tableau d’octets sous la forme d’un fichier GIF (spécifié à l’aide de la valeur d’énumération [PersistenceFormat](/previous-versions/ms552503(v=vs.100)) ).</span><span class="sxs-lookup"><span data-stu-id="7f290-137">If the Ink object contains any strokes, the ink data is saved into the `inkDataBytes` byte array as a GIF (specified by using the [PersistenceFormat](/previous-versions/ms552503(v=vs.100)) enumeration value).</span></span> <span data-ttu-id="7f290-138">La méthode convertit ensuite le tableau d’octets en une chaîne encodée en base64 et retourne cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="7f290-138">The method then converts the byte array to a Base64-encoded string and returns this string.</span></span>

<span data-ttu-id="7f290-139">En supposant que le client puisse effectuer la reconnaissance, la `TextData` propriété retourne l’objet [RecognitionResult](/previous-versions/ms552537(v=vs.100)) à partir du passage des données de l’encre à un module de reconnaissance de l’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="7f290-139">Assuming that the client can perform recognition, the `TextData` property returns the [RecognitionResult](/previous-versions/ms552537(v=vs.100)) object from passing the ink data to a handwriting recognizer.</span></span> <span data-ttu-id="7f290-140">Si le client ne prend pas en charge l’écriture manuscrite, le contenu de la zone de texte est retourné, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="7f290-140">If the client is not ink-aware, the text box contents are returned, as shown in the following code.</span></span>


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



<span data-ttu-id="7f290-141">La `TextData` propriété appelle une méthode d’assistance, `RecognizeInkData` , illustrée dans le code suivant, pour effectuer la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="7f290-141">The `TextData` property calls a helper method, `RecognizeInkData`, shown in the following code, to carry out the recognition.</span></span> <span data-ttu-id="7f290-142">Lorsque les moteurs de reconnaissance sont présents sur le système, la `RecognizeInkData` méthode retourne une chaîne contenant la propriété de la [chaîne](/previous-versions/ms572009(v=vs.100)) de l’objet [RecognitionResult](/previous-versions/ms552537(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="7f290-142">When recognition engines are present on the system, the `RecognizeInkData` method returns a string containing the [RecognitionResult](/previous-versions/ms552537(v=vs.100)) object's [TopString](/previous-versions/ms572009(v=vs.100)) property.</span></span> <span data-ttu-id="7f290-143">Sinon, la fonction retourne une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="7f290-143">Otherwise, it returns an empty string.</span></span>


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



<span data-ttu-id="7f290-144">La `InkEnabled` propriété est une valeur booléenne en lecture seule qui indique si l’entrée manuscrite est prise en charge sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="7f290-144">The `InkEnabled` property is a read-only Boolean value that indicates whether inking is supported on the client machine.</span></span>

<span data-ttu-id="7f290-145">Un autre membre public important de la `InkArea` classe de contrôle est la `DisposeResources` méthode.</span><span class="sxs-lookup"><span data-stu-id="7f290-145">Another important public member of the `InkArea` control class is the `DisposeResources` method.</span></span> <span data-ttu-id="7f290-146">Cette méthode appelle en interne la `Dispose` méthode pour s’assurer que toutes les ressources exploitées par le contrôle utilisateur sont nettoyées.</span><span class="sxs-lookup"><span data-stu-id="7f290-146">This method internally calls the `Dispose` method to ensure that all resources leveraged by the user control are cleaned up.</span></span> <span data-ttu-id="7f290-147">Toute application qui utilise le `InkArea` contrôle doit appeler la `DisposeResources` méthode lorsqu’elle a fini d’utiliser le contrôle.</span><span class="sxs-lookup"><span data-stu-id="7f290-147">Any application that uses the `InkArea` control must call the `DisposeResources` method when it is finished using the control.</span></span>

## <a name="inkblogweb-project"></a><span data-ttu-id="7f290-148">Projet InkBlogWeb</span><span class="sxs-lookup"><span data-stu-id="7f290-148">InkBlogWeb Project</span></span>

<span data-ttu-id="7f290-149">Le projet InkBlogWeb est un projet de déploiement d’installation Web qui référence le `InkArea` contrôle pour fournir la fonctionnalité de blog.</span><span class="sxs-lookup"><span data-stu-id="7f290-149">The InkBlogWeb project is a Web Setup deployment project that references the `InkArea` control to provide the blogging functionality.</span></span> <span data-ttu-id="7f290-150">Pour plus d’informations sur les projets de déploiement de l’installation Web, consultez [déploiement d’un projet d’installation Web](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="7f290-150">For more information about Web Setup deployment projects, see [Deployment of a Web Setup Project](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).</span></span>

<span data-ttu-id="7f290-151">Il existe deux fichiers. aspx qui implémentent l’exemple de blog : default. aspx et AddBlog. aspx.</span><span class="sxs-lookup"><span data-stu-id="7f290-151">There are two .aspx files that implement the blogging sample: Default.aspx and AddBlog.aspx.</span></span> <span data-ttu-id="7f290-152">Default. aspx est la page par défaut de l’application InkBlogWeb.</span><span class="sxs-lookup"><span data-stu-id="7f290-152">Default.aspx is the default page for the InkBlogWeb application.</span></span> <span data-ttu-id="7f290-153">Le fichier code-behind de cette page est default. aspx. cs.</span><span class="sxs-lookup"><span data-stu-id="7f290-153">The code behind file for this page is Default.aspx.cs.</span></span> <span data-ttu-id="7f290-154">Cette page fournit un lien vers la page contenant le nouveau formulaire de saisie de blog et affiche les entrées de blog existantes.</span><span class="sxs-lookup"><span data-stu-id="7f290-154">This page provides a link to the page containing the new blog entry form and displays any existing blog entries.</span></span> <span data-ttu-id="7f290-155">Ce processus est décrit ultérieurement, après l’examen suivant de la page du nouveau formulaire de saisie de blog, AddBlog. aspx.</span><span class="sxs-lookup"><span data-stu-id="7f290-155">This process is described later, after the following examination of the new blog entry form page, AddBlog.aspx.</span></span>

<span data-ttu-id="7f290-156">AddBlog. aspx et son fichier code-behind, AddBlog. aspx. cs, contiennent la logique et le code de l’interface utilisateur permettant de créer des entrées de blog.</span><span class="sxs-lookup"><span data-stu-id="7f290-156">AddBlog.aspx and its code-behind file, AddBlog.aspx.cs, contain the logic and user interface code for creating new blog entries.</span></span> <span data-ttu-id="7f290-157">AddBlox. aspx fait référence à deux instances de la classe de contrôle InkArea créée dans le projet InkBlogControls à l’aide de l’élément objet HTML, comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="7f290-157">AddBlox.aspx references two instances of the InkArea control class created in the InkBlogControls project by using the HTML OBJECT element as shown in the following example.</span></span> <span data-ttu-id="7f290-158">Une instance a un `id` attribut de inkBlogTitle et l’autre a un attribut d’ID de inkBlogBody.</span><span class="sxs-lookup"><span data-stu-id="7f290-158">One instance has an `id` attribute of inkBlogTitle and the other has an id attribute of inkBlogBody.</span></span>

`<OBJECT id="inkBlogTitle" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="48" VIEWASTEXT>``</OBJECT>``<br/>``<OBJECT id="inkBlogBody" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="296" VIEWASTEXT>``</OBJECT>`

<span data-ttu-id="7f290-159">L’assembly de InkBlogControls.dll doit être présent dans le même répertoire que la page. aspx qui y fait référence.</span><span class="sxs-lookup"><span data-stu-id="7f290-159">The InkBlogControls.dll assembly must be present in the same directory as the .aspx page that is referencing it.</span></span> <span data-ttu-id="7f290-160">Le projet de déploiement de l’installation Web garantit que c’est le cas, tel qu’il est prouvé par la présence de l’élément « sortie principale de InkBlogControls » dans le projet de déploiement.</span><span class="sxs-lookup"><span data-stu-id="7f290-160">The Web Setup deployment project ensures that this is the case, as evidenced by the presence of the "Primary output from InkBlogControls" item in the Deployment Project.</span></span>

<span data-ttu-id="7f290-161">Le contrôle titre est uniquement de 48 pixels de haut pour faciliter l’entrée d’une seule ligne d’encre pour le titre.</span><span class="sxs-lookup"><span data-stu-id="7f290-161">The title control is only 48 pixels high to facilitate the entry of a single line of ink for the title.</span></span> <span data-ttu-id="7f290-162">Le contrôle du corps est de 296 pixels de haut pour faire de la place pour les entrées de blog plus grandes de plusieurs lignes ou des dessins.</span><span class="sxs-lookup"><span data-stu-id="7f290-162">The body control is 296 pixels high to make room for larger blog entries of multiple lines or perhaps drawings.</span></span>

<span data-ttu-id="7f290-163">Les contrôles InkArea sont connectés à une fonction de script côté client, AddBlog, au moyen du gestionnaire d’événements OnClick d’un élément BUTTON HTML standard.</span><span class="sxs-lookup"><span data-stu-id="7f290-163">The InkArea controls are connected to a client-side script function, AddBlog, by means of a standard HTML BUTTON element's onclick event handler.</span></span>

`<button id="BUTTON1" type="button" onclick="AddBlog()">Add Blog</button>`

<span data-ttu-id="7f290-164">Il existe également un formulaire HTML sur la page qui contient trois éléments d’entrée masqués : BlogTitleText, BlogBodyText et BlogBodyInkData.</span><span class="sxs-lookup"><span data-stu-id="7f290-164">There is also an HTML form on the page that contains three hidden INPUT elements: BlogTitleText, BlogBodyText, and BlogBodyInkData.</span></span> <span data-ttu-id="7f290-165">Ce formulaire est utilisé pour replacer les données de l’entrée de blog sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7f290-165">This form is used to post the blog entry data back to the server.</span></span> <span data-ttu-id="7f290-166">AddBlog. aspx est le gestionnaire de publication défini pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="7f290-166">AddBlog.aspx is the post-back handler defined for the form.</span></span>

<span data-ttu-id="7f290-167">La fonction AddBlog-écrite dans Microsoft JScript <entity type="reg"/> : extrait les données de blog à partir des contrôles InkArea et publie les résultats sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7f290-167">The AddBlog function-written in Microsoft JScript<entity type="reg"/>-extracts the blog data from the InkArea controls and posts the results to the server.</span></span>


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



<span data-ttu-id="7f290-168">Lorsque les données arrivent sur le serveur, le code dans AddBlog. aspx. cs vérifie le \_ Gestionnaire d’événements de chargement de page pour voir si la propriété Form de l’objet HttpRequest contient des données.</span><span class="sxs-lookup"><span data-stu-id="7f290-168">When the data arrives at the server, the code in AddBlog.aspx.cs checks the Page\_Load event handler to see if the HttpRequest object's Form property contains any data.</span></span> <span data-ttu-id="7f290-169">Si c’est le cas, il crée un nom de fichier basé sur l’heure système actuelle, place les données du formulaire dans trois variables de chaîne et écrit les données dans un fichier HTML et un fichier GIF contenant les données d’encre, le cas échéant, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="7f290-169">If so, it creates a file name based on the current system time, puts the form data into three string variables and writes the data out to an HTML file and a GIF file containing the ink data, if present, as shown in the following code.</span></span>


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



<span data-ttu-id="7f290-170">Pour plus d’informations sur les méthodes d’assistance, reportez-vous à l’exemple de code source.</span><span class="sxs-lookup"><span data-stu-id="7f290-170">For more details about the helper methods, refer to the sample source code.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="7f290-171">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="7f290-171">Running the Sample</span></span>

<span data-ttu-id="7f290-172">Le kit de développement logiciel (SDK) Tablet PC 1,7 installe l’exemple Web de blog Ink par défaut.</span><span class="sxs-lookup"><span data-stu-id="7f290-172">The Tablet PC SDK 1.7 installs the Ink Blog Web sample by default.</span></span> <span data-ttu-id="7f290-173">Pour exécuter l’exemple, dans Internet Explorer, accédez à https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx .</span><span class="sxs-lookup"><span data-stu-id="7f290-173">To run the sample, in Internet Explorer, navigate to https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx.</span></span> <span data-ttu-id="7f290-174">Si vous exécutez Windows Server 2003, remplacez « localhost » par le nom de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="7f290-174">If you are running Windows Server 2003, substitute your computer name for "localhost".</span></span>

> [!Note]  
> <span data-ttu-id="7f290-175">Les exemples Web compilés ne sont pas installés par l’option d’installation par défaut pour le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="7f290-175">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="7f290-176">Vous devez effectuer une installation personnalisée et sélectionner la sous-option « exemples Web précompilés » pour les installer.</span><span class="sxs-lookup"><span data-stu-id="7f290-176">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

<span data-ttu-id="7f290-177">Vous pouvez également exécuter l’exemple en ouvrant et en générant le projet dans Microsoft Visual Studio <entity type="reg"/> .net, puis en le déployant sur un ordinateur distinct qui exécute IIS.</span><span class="sxs-lookup"><span data-stu-id="7f290-177">You can also run the sample by opening and building the project in Microsoft Visual Studio<entity type="reg"/> .NET and then deploying it to a separate computer running IIS.</span></span>

## <a name="troubleshooting-the-sample"></a><span data-ttu-id="7f290-178">Résolution des problèmes liés à l'exemple</span><span class="sxs-lookup"><span data-stu-id="7f290-178">Troubleshooting the Sample</span></span>

<span data-ttu-id="7f290-179">Trois zones qui peuvent engendrer des difficultés lors de l’exécution ou de l’hébergement de l’exemple sont les autorisations et la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="7f290-179">Three areas that may cause difficulty when running or hosting the sample are permissions and recognition.</span></span>

### <a name="permissions"></a><span data-ttu-id="7f290-180">Autorisations</span><span class="sxs-lookup"><span data-stu-id="7f290-180">Permissions</span></span>

<span data-ttu-id="7f290-181">L’exemple requiert des autorisations d’écriture dans le dossier racine virtuel pour le compte qui tente de créer une entrée de blog.</span><span class="sxs-lookup"><span data-stu-id="7f290-181">The sample requires write permissions within the virtual root folder for the account that is attempting to create a new blog entry.</span></span> <span data-ttu-id="7f290-182">Par défaut, la version compilée de l’exemple fourni dans le kit de développement logiciel (SDK) Tablet PC 1,7 dispose des autorisations appropriées pour répondre à cette exigence.</span><span class="sxs-lookup"><span data-stu-id="7f290-182">By default, the compiled version of the sample provided in the Tablet PC SDK 1.7 has the correct permissions set to meet this requirement.</span></span>

<span data-ttu-id="7f290-183">Si vous générez et déployez l’exemple à l’aide du projet de déploiement de l’installation Web fourni, vous devez accorder au groupe% MACHINENAME% \\ Users l’accès en écriture au dossier du système de fichiers désigné par la racine virtuelle InkBlogWeb (par exemple, C : \\ Inetpub \\ wwwroot \\ InkBlogWeb).</span><span class="sxs-lookup"><span data-stu-id="7f290-183">If you build and deploy the sample by using the provided Web Setup deployment project, you must give the %MACHINENAME%\\Users group write-access to the file system folder pointed to by the InkBlogWeb virtual root (for example, C:\\InetPub\\WWWRoot\\InkBlogWeb).</span></span> <span data-ttu-id="7f290-184">Le groupe utilisateurs comprend le compte anonyme utilisé par IIS, ce qui permet à l’application ASP.NET d’écrire les nouvelles entrées de blog dans le système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="7f290-184">The Users group includes the Anonymous account used by IIS, thus allowing the ASP.NET application to write the new blog entries to the file system.</span></span> <span data-ttu-id="7f290-185">Une alternative consiste à supprimer l’accès anonyme à la racine virtuelle et à forcer l’authentification.</span><span class="sxs-lookup"><span data-stu-id="7f290-185">An alternative is to remove anonymous access to the virtual root and force authentication.</span></span>

### <a name="recognition"></a><span data-ttu-id="7f290-186">Reconnaissance</span><span class="sxs-lookup"><span data-stu-id="7f290-186">Recognition</span></span>

<span data-ttu-id="7f290-187">Les détecteurs d’écriture manuscrite doivent être installés afin de reconnaître l’encre dans le titre du blog.</span><span class="sxs-lookup"><span data-stu-id="7f290-187">The handwriting recognizers must be installed in order to recognize the ink in the title of the blog.</span></span> <span data-ttu-id="7f290-188">Si vous accédez à l’application InkBlog à partir d’un ordinateur équipé d’un système d’exploitation autre que Windows XP Édition Tablet PC, mais avec le kit de développement logiciel (SDK) Tablet PC 1,7 installé, vous pouvez écrire dans les contrôles InkArea, mais les moteurs de reconnaissance ne sont pas présents et aucun titre ne s’affiche pour vos entrées de blog.</span><span class="sxs-lookup"><span data-stu-id="7f290-188">If you access the InkBlog application from a computer with an operating system other than Windows XP Tablet PC Edition but with the Tablet PC SDK 1.7 installed, you can write in ink in the InkArea controls, but the recognition engines will not be present and no titles will appear for your blog entries.</span></span> <span data-ttu-id="7f290-189">Toutefois, le contenu de l’encre dans le corps apparaît toujours.</span><span class="sxs-lookup"><span data-stu-id="7f290-189">The ink content in the body still appears, though.</span></span>

### <a name="machine-configuration"></a><span data-ttu-id="7f290-190">Configuration de l’ordinateur</span><span class="sxs-lookup"><span data-stu-id="7f290-190">Machine Configuration</span></span>

<span data-ttu-id="7f290-191">Si vous avez installé ASP.NET et le .NET Framework sur un ordinateur et que vous désinstallez puis réinstallez IIS, les mappages de script échouent et ASP.NET ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="7f290-191">If you have installed ASP.NET and the .NET Framework on a computer and you then uninstall and reinstall IIS, the script maps will break and ASP.NET will not work.</span></span> <span data-ttu-id="7f290-192">Dans ce cas, vous pouvez réparer les mappages de script ASP.NET à l’aide de l’outil d’inscription ASP.NET IIS (ASPNET \_regiis.exe-i).</span><span class="sxs-lookup"><span data-stu-id="7f290-192">If this happens, you can repair the ASP.NET script maps with the ASP.NET IIS Registration tool (Aspnet\_regiis.exe -i).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f290-193">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7f290-193">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7f290-194">[Collecte](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="7f290-194">[InkCollector](/previous-versions/ms583683(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="7f290-195">Entrée manuscrite sur le Web</span><span class="sxs-lookup"><span data-stu-id="7f290-195">Ink on the Web</span></span>](ink-on-the-web.md)
</dt> <dt>

[<span data-ttu-id="7f290-196">Formats de données manuscrites</span><span class="sxs-lookup"><span data-stu-id="7f290-196">Ink Data Formats</span></span>](ink-data-formats.md)
</dt> <dt>

[<span data-ttu-id="7f290-197">System. Windows. Forms. UserControl (classe)</span><span class="sxs-lookup"><span data-stu-id="7f290-197">System.Windows.Forms.UserControl Class</span></span>](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)
</dt> </dl>

 

 
