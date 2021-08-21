---
description: Cet exemple montre comment sérialiser et désérialiser de l’encre dans différents formats.
ms.assetid: 468d9c2a-0b3c-4a44-a049-3f3b78e952ba
title: Ink Serialization, exemple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e71eed5c91bf4fa1524cc52af163516ced0c7362d0d20b8ecf52ac1a08ccd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032267"
---
# <a name="ink-serialization-sample"></a>Ink Serialization, exemple

Cet exemple montre comment sérialiser et désérialiser de l’encre dans différents formats. L’application représente un formulaire avec des champs permettant de saisir le prénom, le nom et la signature. L’utilisateur peut enregistrer ces données en tant que format ISF (Ink Serialized Format), Extensible Markup Language (XML) à l’aide du format ISF encodé en base64, ou HTML, qui fait référence à l’encre dans une image GIF (Graphical Interchange Format) encodée en base64. L’application permet également à l’utilisateur d’ouvrir des fichiers enregistrés au format XML et ISF. Le format ISF utilise des propriétés étendues pour stocker le prénom et le nom, tandis que les formats XML et HTML stockent ces informations dans des attributs personnalisés.

Cet exemple ne prend pas en charge le chargement à partir du format HTML, car le code HTML n’est pas adapté au stockage de données structurées. Dans la mesure où les données sont séparées par un nom, une signature, etc., un format qui conserve cette séparation, par exemple XML ou un autre type de format de base de données, est requis.

Le format HTML est très utile dans un environnement dans lequel la mise en forme est importante, par exemple dans un document de traitement de texte. Le code HTML enregistré dans cet exemple utilise des fichiers GIF enrichis. Ces gif comportent un ISF incorporé, ce qui préserve la fidélité totale de l’encre. Une application de traitement de texte peut enregistrer un document contenant plusieurs types de données, tels que des images, des tableaux, du texte mis en forme et des entrées manuscrites conservées dans un format HTML. Ce code HTML s’affiche dans les navigateurs qui ne reconnaissent pas l’encre. Toutefois, lorsqu’elle est chargée dans une application activée pour l’écriture manuscrite, la fidélité totale de l’encre d’origine est disponible et peut être rendue, modifiée ou utilisée pour la reconnaissance.

Les fonctionnalités suivantes sont utilisées dans cet exemple :

-   Méthode [Load](/previous-versions/ms569609(v=vs.100)) de l’objet [Ink](/previous-versions/aa515768(v=msdn.10))
-   Méthode [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) de l’objet [Ink](/previous-versions/aa515768(v=msdn.10))
-   Propriété [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) de l’objet [Ink](/previous-versions/aa515768(v=msdn.10))

## <a name="collecting-ink"></a>Collecte d'encre

tout d’abord, référencez l’API tablet pc qui est installée avec le kit de développement logiciel (SDK) Windows Vista et Windows XP Tablet pc Edition.


```C++
using Microsoft.Ink;
```



Le constructeur crée et active un [InkCollector](/previous-versions/ms836493(v=msdn.10)), `ic` , pour le formulaire.


```C++
ic = new InkCollector(Signature.Handle);
ic.Enabled = true;
```



## <a name="saving-a-file"></a>Enregistrement d’un fichier

La `SaveAsMenu_Click` méthode gère la boîte de dialogue Enregistrer sous, crée un flux de fichier dans lequel enregistrer les données d’encre et appelle la méthode Save qui correspond au choix de l’utilisateur.

## <a name="saving-to-an-isf-file"></a>Enregistrement dans un fichier ISF

Dans la `SaveISF` méthode, les premières et dernières valeurs de nom sont ajoutées à la propriété [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) de la propriété [Ink](/previous-versions/ms836505(v=msdn.10)) de l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) , avant que l’encre ne soit sérialisée et écrite dans le fichier. Une fois l’encre sérialisée, les valeurs du prénom et du nom sont supprimées de la propriété ExtendedProperties de l’objet [Ink](/previous-versions/aa515768(v=msdn.10)) .


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



## <a name="saving-to-an-xml-file"></a>Enregistrement dans un fichier XML

Dans la `SaveXML` méthode, un objet [XmlTextWriter](/dotnet/api/system.xml.xmltextwriter?view=netcore-3.1) est utilisé pour créer et écrire dans un document XML. À l’aide de la méthode [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) de l’objet [Ink](/previous-versions/aa515768(v=msdn.10)) , l’encre est tout d’abord convertie en un tableau d’octets au format sérialisé en écriture en code Base64, puis le tableau d’octets est converti en chaîne à écrire dans le fichier XML. Les données de texte du formulaire sont également écrites dans le fichier XML.


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



## <a name="saving-to-an-html-file"></a>Enregistrement dans un fichier HTML

La méthode SaveHTML utilise le cadre englobant de la collection [Strokes](/previous-versions/ms827799(v=msdn.10)) pour tester la présence d’une signature. Si la signature existe, elle est convertie au format GIF viné à l’aide de la méthode [Save](/previous-versions/dotnet/netframework-3.5/ms571335(v=vs.90)) de l’objet Ink et écrite dans un fichier. Le GIF est ensuite référencé dans le fichier HTML.


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



## <a name="loading-a-file"></a>Chargement d’un fichier

La `OpenMenu_Click` méthode gère la boîte de dialogue Ouvrir, ouvre le fichier et appelle la méthode de chargement qui correspond au choix de l’utilisateur.

## <a name="loading-an-isf-file"></a>Chargement d’un fichier ISF

La `LoadISF` méthode lit le fichier créé précédemment et convertit le tableau d’octets en entrée manuscrite avec la méthode [Load](/previous-versions/ms569609(v=vs.100)) de l’objet [Ink](/previous-versions/aa515768(v=msdn.10)) . Le collecteur d’encre est temporairement désactivé pour lui assigner l’objet Ink. La `LoadISF` méthode vérifie ensuite la propriété [ExtendedProperties](/previous-versions/ms582214(v=vs.100)) de l’objet Ink pour obtenir les premières et les dernières chaînes de nom.


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



## <a name="loading-an-xml-file"></a>Chargement d’un fichier XML

La `LoadXML` méthode charge un fichier XML créé précédemment, récupère les données du nœud Ink et convertit les données du nœud en encre à l’aide de la méthode [Load](/previous-versions/ms569609(v=vs.100)) de l’objet [Ink](/previous-versions/aa515768(v=msdn.10)) . Le [InkCollector](/previous-versions/ms836493(v=msdn.10)) est temporairement désactivé pour lui assigner l’objet Ink. La zone signature est invalidée et les informations sur le prénom et le nom sont extraites du document XML.


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



## <a name="closing-the-form"></a>Fermeture du formulaire

La méthode dispose du formulaire [supprime](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) l’objet [InkCollector](/previous-versions/ms836493(v=msdn.10)) .

 

 
