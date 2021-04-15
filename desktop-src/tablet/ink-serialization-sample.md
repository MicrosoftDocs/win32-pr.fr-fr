---
description: Cet exemple montre comment sérialiser et désérialiser de l’encre dans différents formats.
ms.assetid: 468d9c2a-0b3c-4a44-a049-3f3b78e952ba
title: Ink Serialization, exemple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e898f91db17efcb7579c067e7db5c422da8213a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525288"
---
# <a name="ink-serialization-sample"></a><span data-ttu-id="cfb4b-103">Ink Serialization, exemple</span><span class="sxs-lookup"><span data-stu-id="cfb4b-103">Ink Serialization Sample</span></span>

<span data-ttu-id="cfb4b-104">Cet exemple montre comment sérialiser et désérialiser de l’encre dans différents formats.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-104">This sample demonstrates how to serialize and de-serialize ink in various formats.</span></span> <span data-ttu-id="cfb4b-105">L’application représente un formulaire avec des champs permettant de saisir le prénom, le nom et la signature.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-105">The application represents a form with fields for inputting first name, last name, and signature.</span></span> <span data-ttu-id="cfb4b-106">L’utilisateur peut enregistrer ces données en tant que format ISF (Ink Serialized Format), Extensible Markup Language (XML) à l’aide du format ISF encodé en base64, ou HTML, qui fait référence à l’encre dans une image GIF (Graphical Interchange Format) encodée en base64.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-106">The user may save this data as pure ink serialized format (ISF), Extensible Markup Language (XML) using base64 encoded ISF, or HTML, which references ink in a base64 encoded fortified Graphics Interchange Format (GIF) image.</span></span> <span data-ttu-id="cfb4b-107">L’application permet également à l’utilisateur d’ouvrir des fichiers enregistrés au format XML et ISF.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-107">The application also enables the user to open files that were saved as XML and ISF formats.</span></span> <span data-ttu-id="cfb4b-108">Le format ISF utilise des propriétés étendues pour stocker le prénom et le nom, tandis que les formats XML et HTML stockent ces informations dans des attributs personnalisés.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-108">The ISF format uses extended properties to store the first name and last name, whereas the XML and HTML formats store this information in custom attributes.</span></span>

<span data-ttu-id="cfb4b-109">Cet exemple ne prend pas en charge le chargement à partir du format HTML, car le code HTML n’est pas adapté au stockage de données structurées.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-109">This sample does not support loading from the HTML format, because HTML is not suitable for storing structured data.</span></span> <span data-ttu-id="cfb4b-110">Dans la mesure où les données sont séparées par un nom, une signature, etc., un format qui conserve cette séparation, par exemple XML ou un autre type de format de base de données, est requis.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-110">Because the data is separated into name, signature, and so on, a format that preserves this separation, such as XML or another kind of database format, is required.</span></span>

<span data-ttu-id="cfb4b-111">Le format HTML est très utile dans un environnement dans lequel la mise en forme est importante, par exemple dans un document de traitement de texte.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-111">HTML is very useful in an environment in which formatting is important, such as in a word processing document.</span></span> <span data-ttu-id="cfb4b-112">Le code HTML enregistré dans cet exemple utilise des fichiers GIF enrichis.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-112">The HTML that is saved by this sample uses fortified GIFs.</span></span> <span data-ttu-id="cfb4b-113">Ces gif comportent un ISF incorporé, ce qui préserve la fidélité totale de l’encre.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-113">These GIFs have ISF embedded within them, which preserves the full fidelity of the ink.</span></span> <span data-ttu-id="cfb4b-114">Une application de traitement de texte peut enregistrer un document contenant plusieurs types de données, tels que des images, des tableaux, du texte mis en forme et des entrées manuscrites conservées dans un format HTML.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-114">A word processing application can save a document containing multiple types of data, such as images, tables, formatted text, and ink persisted in an HTML format.</span></span> <span data-ttu-id="cfb4b-115">Ce code HTML s’affiche dans les navigateurs qui ne reconnaissent pas l’encre.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-115">This HTML would render in browsers that do not recognize ink.</span></span> <span data-ttu-id="cfb4b-116">Toutefois, lorsqu’elle est chargée dans une application activée pour l’écriture manuscrite, la fidélité totale de l’encre d’origine est disponible et peut être rendue, modifiée ou utilisée pour la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-116">However, when loaded into an application that is ink-enabled, the full fidelity of the original ink is available and can be rendered, edited, or used for recognition.</span></span>

<span data-ttu-id="cfb4b-117">Les fonctionnalités suivantes sont utilisées dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="cfb4b-117">The following features are used in this sample:</span></span>

-   <span data-ttu-id="cfb4b-118">Méthode [Load](/previous-versions/ms569609(v=vs.100)) de l’objet [Ink](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="cfb4b-118">The [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Load](/previous-versions/ms569609(v=vs.100)) method</span></span>
-   <span data-ttu-id="cfb4b-119">Méthode [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) de l’objet [Ink](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="cfb4b-119">The [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method</span></span>
-   <span data-ttu-id="cfb4b-120">Propriété [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) de l’objet [Ink](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="cfb4b-120">The [Ink](/previous-versions/aa515768(v=msdn.10)) object's [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) property</span></span>

## <a name="collecting-ink"></a><span data-ttu-id="cfb4b-121">Collecte d'encre</span><span class="sxs-lookup"><span data-stu-id="cfb4b-121">Collecting Ink</span></span>

<span data-ttu-id="cfb4b-122">Tout d’abord, référencez l’API Tablet PC qui est installée avec le kit de développement logiciel (SDK) Windows Vista et Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-122">First, reference the Tablet PC API, which are installed with the Windows Vista and Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="cfb4b-123">Le constructeur crée et active un [InkCollector](/previous-versions/ms836493(v=msdn.10)), `ic` , pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-123">The constructor creates and enables an [InkCollector](/previous-versions/ms836493(v=msdn.10)), `ic`, for the form.</span></span>


```C++
ic = new InkCollector(Signature.Handle);
ic.Enabled = true;
```



## <a name="saving-a-file"></a><span data-ttu-id="cfb4b-124">Enregistrement d’un fichier</span><span class="sxs-lookup"><span data-stu-id="cfb4b-124">Saving a File</span></span>

<span data-ttu-id="cfb4b-125">La `SaveAsMenu_Click` méthode gère la boîte de dialogue Enregistrer sous, crée un flux de fichier dans lequel enregistrer les données d’encre et appelle la méthode Save qui correspond au choix de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-125">The `SaveAsMenu_Click` method handles the Save As dialog box, creates a file stream in which to save the ink data, and calls the save method that corresponds to the user's choice.</span></span>

## <a name="saving-to-an-isf-file"></a><span data-ttu-id="cfb4b-126">Enregistrement dans un fichier ISF</span><span class="sxs-lookup"><span data-stu-id="cfb4b-126">Saving to an ISF File</span></span>

<span data-ttu-id="cfb4b-127">Dans la `SaveISF` méthode, les premières et dernières valeurs de nom sont ajoutées à la propriété [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) de la propriété [Ink](/previous-versions/ms836505(v=msdn.10)) de l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) , avant que l’encre ne soit sérialisée et écrite dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-127">In the `SaveISF` method, the first and last name values are added to the [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) property of the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [Ink](/previous-versions/ms836505(v=msdn.10)) property, before the ink is serialized and written to the file.</span></span> <span data-ttu-id="cfb4b-128">Une fois l’encre sérialisée, les valeurs du prénom et du nom sont supprimées de la propriété ExtendedProperties de l’objet [Ink](/previous-versions/aa515768(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="cfb4b-128">After the ink has been serialized, the first and last name values are removed from the [Ink](/previous-versions/aa515768(v=msdn.10)) object's ExtendedProperties property.</span></span>


```C++
byte[] isf;

// This is the ink object which is serialized
ExtendedProperties inkProperties = ic.Ink.ExtendedProperties;

// Store the name fields in the ink object
// These fields roundtrip through the ISF format
// Ignore empty fields since strictly empty strings 
//       cannot be stored in ExtendedProperties.
if (FirstNameBox.Text.Length > 0)
{
    inkProperties.Add(FirstName, FirstNameBox.Text);
}
if (LastNameBox.Text.Length > 0)
{
    inkProperties.Add(LastName, LastNameBox.Text);
}

// Perform the serialization
isf = ic.Ink.Save(PersistenceFormat.InkSerializedFormat);

// If the first and last names were added as extended
// properties to the ink, remove them - these properties
// are only used for the save and there is no need to
// keep them around on the ink object.
if (inkProperties.DoesPropertyExist(FirstName))
{
    inkProperties.Remove(FirstName);
}
if (inkProperties.DoesPropertyExist(LastName))
{
    inkProperties.Remove(LastName);
}

// Write the ISF to the stream
s.Write(isf,0,isf.Length);
```



## <a name="saving-to-an-xml-file"></a><span data-ttu-id="cfb4b-129">Enregistrement dans un fichier XML</span><span class="sxs-lookup"><span data-stu-id="cfb4b-129">Saving to an XML File</span></span>

<span data-ttu-id="cfb4b-130">Dans la `SaveXML` méthode, un objet [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) est utilisé pour créer et écrire dans un document XML.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-130">In the `SaveXML` method, an [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) object is used to create and write to an XML document.</span></span> <span data-ttu-id="cfb4b-131">À l’aide de la méthode [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) de l’objet [Ink](/previous-versions/aa515768(v=msdn.10)) , l’encre est tout d’abord convertie en un tableau d’octets au format sérialisé en écriture en code Base64, puis le tableau d’octets est converti en chaîne à écrire dans le fichier XML.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-131">Using the [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method, the ink is first converted to a base64 encoded Ink Serialized Format byte array, and then the byte array is converted to a string to be written out to the XML file.</span></span> <span data-ttu-id="cfb4b-132">Les données de texte du formulaire sont également écrites dans le fichier XML.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-132">The text data from the form is also written out to the XML file.</span></span>


```C++
// Get the base64 encoded ISF
base64ISF_bytes = ic.Ink.Save(PersistenceFormat.Base64InkSerializedFormat);

// Convert it to a String
base64ISF_string = utf8.GetString(base64ISF_bytes);

// Write the ISF containing node to the XML
xwriter.WriteElementString("Ink", base64ISF_string);

// Write the text data from the form
// Note that the names are stored as XML fields, rather
// than custom properties, so that these properties can 
// be most easily accessible if the XML is saved in a database.
xwriter.WriteElementString("FirstName",FirstNameBox.Text);
xwriter.WriteElementString("LastName",LastNameBox.Text);
```



## <a name="saving-to-an-html-file"></a><span data-ttu-id="cfb4b-133">Enregistrement dans un fichier HTML</span><span class="sxs-lookup"><span data-stu-id="cfb4b-133">Saving to an HTML File</span></span>

<span data-ttu-id="cfb4b-134">La méthode SaveHTML utilise le cadre englobant de la collection [Strokes](/previous-versions/ms827799(v=msdn.10)) pour tester la présence d’une signature.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-134">The SaveHTML method uses the bounding box of the [Strokes](/previous-versions/ms827799(v=msdn.10)) collection to test for the presence of a signature.</span></span> <span data-ttu-id="cfb4b-135">Si la signature existe, elle est convertie au format GIF viné à l’aide de la méthode [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) de l’objet Ink et écrite dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-135">If the signature exists, it is converted to the fortified GIF format using the ink object's [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) method, and written to a file.</span></span> <span data-ttu-id="cfb4b-136">Le GIF est ensuite référencé dans le fichier HTML.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-136">The GIF is then referenced in the HTML file.</span></span>


```C++
if (ic.Ink.Strokes.GetBoundingBox().IsEmpty)
{
   MessageBox.Show("Unable to save empty ink in HTML persistence format.");
}
else
{
    FileStream gifFile;
    byte[] fortifiedGif = null;
    ...

    // Create a directory to store the fortified GIF which also contains ISF
    // and open the file for writing
    Directory.CreateDirectory(nameBase + "_files");
    using (FileStream gifFile = File.OpenWrite(nameBase + "_files\\signature.gif"))
    {

        // Generate the fortified GIF represenation of the ink
        fortifiedGif = ic.Ink.Save(PersistenceFormat.Gif);

        // Write and close the gif file
        gifFile.Write(fortifiedGif, 0, fortifiedGif.Length);
    }
```



## <a name="loading-a-file"></a><span data-ttu-id="cfb4b-137">Chargement d’un fichier</span><span class="sxs-lookup"><span data-stu-id="cfb4b-137">Loading a File</span></span>

<span data-ttu-id="cfb4b-138">La `OpenMenu_Click` méthode gère la boîte de dialogue Ouvrir, ouvre le fichier et appelle la méthode de chargement qui correspond au choix de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-138">The `OpenMenu_Click` method handles the Open dialog box, opens the file, and calls the loading method that corresponds to the user's choice.</span></span>

## <a name="loading-an-isf-file"></a><span data-ttu-id="cfb4b-139">Chargement d’un fichier ISF</span><span class="sxs-lookup"><span data-stu-id="cfb4b-139">Loading an ISF File</span></span>

<span data-ttu-id="cfb4b-140">La `LoadISF` méthode lit le fichier créé précédemment et convertit le tableau d’octets en entrée manuscrite avec la méthode [Load](/previous-versions/ms569609(v=vs.100)) de l’objet [Ink](/previous-versions/aa515768(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="cfb4b-140">The `LoadISF` method reads the previously created file and converts the Byte array to ink with the [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Load](/previous-versions/ms569609(v=vs.100)) method.</span></span> <span data-ttu-id="cfb4b-141">Le collecteur d’encre est temporairement désactivé pour lui assigner l’objet Ink.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-141">The ink collector is temporarily disabled to assign the Ink object to it.</span></span> <span data-ttu-id="cfb4b-142">La `LoadISF` méthode vérifie ensuite la propriété [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) de l’objet Ink pour obtenir les premières et les dernières chaînes de nom.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-142">The `LoadISF` method then checks the Ink object's [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) property for the first and last name strings.</span></span>


```C++
Ink loadedInk = new Ink();
byte[] isfBytes = new byte[s.Length];

// read in the ISF
s.Read(isfBytes, 0, (int) s.Length);

// load the ink into a new ink object
// After an ink object has been "dirtied" it can never load ink again
loadedInk.Load(isfBytes);

// temporarily disable the ink collector and swap ink objects
ic.Enabled = false;
ic.Ink = loadedInk;
ic.Enabled = true;

// Repaint the inkable region
Signature.Invalidate();

ExtendedProperties inkProperties = ic.Ink.ExtendedProperties;

// Get the raw data out of this stroke's extended
// properties list, using the previously defined 
// Guid as a key to the extended property.
// Since the save method stored the first and last
// name information as extended properties, this
// information can be remove now that the load is complete.
if (inkProperties.DoesPropertyExist(FirstName))
{
    FirstNameBox.Text = (String) inkProperties[FirstName].Data;
    inkProperties.Remove(FirstName);
}
else
{
    FirstNameBox.Text = String.Empty;
}

if (inkProperties.DoesPropertyExist(LastName))
{
    LastNameBox.Text = (String) inkProperties[LastName].Data;
    inkProperties.Remove(LastName);
}
else
{
    LastNameBox.Text = String.Empty;
}
```



## <a name="loading-an-xml-file"></a><span data-ttu-id="cfb4b-143">Chargement d’un fichier XML</span><span class="sxs-lookup"><span data-stu-id="cfb4b-143">Loading an XML File</span></span>

<span data-ttu-id="cfb4b-144">La `LoadXML` méthode charge un fichier XML créé précédemment, récupère les données du nœud Ink et convertit les données du nœud en encre à l’aide de la méthode [Load](/previous-versions/ms569609(v=vs.100)) de l’objet [Ink](/previous-versions/aa515768(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="cfb4b-144">The `LoadXML` method loads a previously created XML file, retrieves data from the Ink node, and converts the data in the node to ink using the [Ink](/previous-versions/aa515768(v=msdn.10)) object's [Load](/previous-versions/ms569609(v=vs.100)) method.</span></span> <span data-ttu-id="cfb4b-145">Le [InkCollector](/previous-versions/ms836493(v=msdn.10)) est temporairement désactivé pour lui assigner l’objet Ink.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-145">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) is temporarily disabled to assign the Ink object to it.</span></span> <span data-ttu-id="cfb4b-146">La zone signature est invalidée et les informations sur le prénom et le nom sont extraites du document XML.</span><span class="sxs-lookup"><span data-stu-id="cfb4b-146">The signature box is invalidated, and the first and last name information is retrieved from the XML document.</span></span>


```C++
// This object encodes our byte data to a UTF8 string
UTF8Encoding utf8 = new UTF8Encoding();

XmlDocument xd = new XmlDocument();
XmlNodeList nodes;
Ink loadedInk = new Ink();

// Load the XML data into a DOM
xd.Load(s);

// Get the data in the ink node
nodes = xd.GetElementsByTagName("Ink");

// load the ink into a new ink object
// After an ink object has been "dirtied" it can never load ink again
if (0 != nodes.Count)
    loadedInk.Load(utf8.GetBytes(nodes[0].InnerXml));

// temporarily disable the ink collector and swap ink objects
ic.Enabled = false;
ic.Ink = loadedInk;
ic.Enabled = true;

// Repaint the inkable region
Signature.Invalidate();

// Get the data in the FirstName node
nodes = xd.GetElementsByTagName("FirstName");
if (0 != nodes.Count)
{
    FirstNameBox.Text = nodes[0].InnerXml;
}
else
{
    FirstNameBox.Text = String.Empty;
}

// Get the data in the LastName node
nodes = xd.GetElementsByTagName("LastName");
if (0 != nodes.Count)
{
    LastNameBox.Text = nodes[0].InnerXml;
}
else
{
    LastNameBox.Text = String.Empty;
}
```



## <a name="closing-the-form"></a><span data-ttu-id="cfb4b-147">Fermeture du formulaire</span><span class="sxs-lookup"><span data-stu-id="cfb4b-147">Closing the Form</span></span>

<span data-ttu-id="cfb4b-148">La méthode dispose du formulaire [supprime](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="cfb4b-148">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object.</span></span>

 

 
