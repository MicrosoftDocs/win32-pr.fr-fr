---
title: Création d’un disque multisession
ms.assetid: 327304c4-fdb9-47c6-9b19-49100b933590
description: 'En savoir plus sur : création d’un disque multisession'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95147cbadedc76487ae64797c342eb256df0967bf99efecb9e9cda443b5d3010
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758575"
---
# <a name="creating-a-multisession-disc"></a>Création d’un disque multisession

L' [API de mastérisation d’image](about-imapi.md) (IMAPI) prend en charge l’ajout et la suppression de fichiers dans, ou à partir de, les types de disques multisessions suivants :

-   CD-R/CD-RW
-   Single-Layer DVD + R/DVD-R
-   DVD + R double couche
-   BD-R
-   dvd-rw/dvd + rw (**Windows 7 uniquement**)
-   DVD-RAM (**Windows 7 uniquement**)
-   BD-RE (**Windows 7 uniquement**)

La création d’un disque multisession à l’aide d’IMAPi se compose des étapes suivantes. chacune de ces étapes documentées contient la partie appropriée de l’exemple complet de script Visual Basic fourni dans la dernière section.

## <a name="initializing-the-disc-recorder"></a>Initialisation de l’enregistreur de disque

Avant l’initialisation de l’appareil, l’objet **MsftDiscMaster2** fournit une énumération des périphériques optiques sur le système. L’interface [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) fournit l’accès à cette énumération d’appareils pour faciliter l’emplacement de l’appareil d’enregistrement approprié. L’objet **MsftDiscMaster2** fournit également des notifications d’événements lors de l’ajout ou de la suppression d’appareils optiques sur un ordinateur.

Après avoir localisé un enregistreur optique et récupéré l’ID qui lui est affecté, créez un nouvel objet **MsftDiscMaster2** et initialisez l’enregistreur à l’aide de l’ID d’appareil spécifique.

L’interface [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) fournit un accès aux informations de base sur l’appareil, telles que l’ID de fournisseur, l’ID de produit, la révision de produit, ainsi que les méthodes permettant d’éjecter un support ou de fermer la barre d’État.

> [!Note]  
> Les constantes et dimensions supplémentaires déclarées dans l’exemple suivant sont utilisées ultérieurement dans l’exemple de script complet situé dans la dernière section de ce document. Ces éléments ne sont pas requis pour l’initialisation d’un enregistreur de disque.

 


```VB
' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)
```



## <a name="creating-a-data-writer"></a>Création d’un enregistreur de données

L’objet **MsftDiscFormat2Data** fournit la méthode d’écriture, ses propriétés, ainsi que les propriétés spécifiques au média. L’interface [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) fournit l’accès à cet objet.

L’enregistreur de disque est lié au writer de format à l’aide de la propriété [**IDiscFormat2Data ::p ut \_ Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) . Une fois que l’enregistreur est lié au writer de format, les requêtes de propriété de média et d’écriture peuvent être effectuées avant d’écrire l’image de résultat sur le disque à l’aide de la méthode [**IDiscFormat2Data :: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) .

> [!Note]  
> La chaîne de nom de client spécifiée dans l’exemple de code ci-dessous doit être ajustée en fonction de l’application spécifique.

 


```VB
    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"
```



## <a name="creating-the-file-system-object"></a>Création de l’objet de système de fichiers

Pour pouvoir enregistrer une nouvelle session, vous devez d’abord générer une image de gravure. Une image de gravure pour les formats **ISO9660**, **Joliet** et **UDF** est constituée de systèmes de fichiers de fichiers et de répertoires individuels. L’objet **MsftFileSystemImage** est l’objet de système de fichiers qui contient les fichiers et les répertoires à placer sur le support optique. L’interface [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) fournit l’accès à l’objet et aux paramètres du système de fichiers.


```VB
    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
```



## <a name="importing-a-file-system"></a>Importation d’un système de fichiers

Avant de continuer, assurez-vous que le disque n’est pas vide en vérifiant la propriété [**IDiscFormat2 :: obtenir \_ MediaHeuristicallyBlank**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2-get_mediaheuristicallyblank) .

Après la création de l’objet **MsftFileSystemImage** , la propriété [**IFileSystemImage ::p ut \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) doit être initialisée avant un appel à la méthode [**IFileSystemImage :: ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) ou [**IFileSystemImage :: ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) pour importer le système de fichiers à partir de la dernière session enregistrée. Ces méthodes remplissent automatiquement l’objet **MsftFileSystemImage** avec des informations décrivant les fichiers et répertoires précédemment enregistrés.

> [!Note]  
> La propriété [**IFileSystemImage ::p ut \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_multisessioninterfaces) est généralement initialisée avec les interfaces multisession fournies par l’enregistreur de données via la propriété [**IDiscFormat2Data :: obten \_ MultisessionInterfaces**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_multisessioninterfaces) .

 

Les tentatives de définition de la propriété **IFileSystemImage ::p ut \_ MultisessionInterfaces** ÉCHOUEnt si IMAPI ne prend pas en charge la multisession pour le support actuellement inséré ou si le support ne peut pas être ajouté pour une raison quelconque (par exemple, parce qu’il est fermé).

Si la session de gravure précédente contenait plusieurs types de système de fichiers, la méthode [**IFileSystemImage :: ImportFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importfilesystem) importera les informations du type de système de fichiers le plus avancé présent. Par exemple, dans l’exemple fourni dans cette rubrique, UDF est le système de fichiers importé. Toutefois, l’utilisation de la méthode [**IFileSystemImage :: ImportSpecificFileSystem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-importspecificfilesystem) permet la sélection spécifique du système de fichiers à importer.

> [!Note]  
> La méthode [**IFileSystemImage :: IdentifyFileSystemsOnDisc**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-identifyfilesystemsondisc) peut être utilisée pour déterminer les systèmes de fichiers disponibles sur le disque.

 


```VB
    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If
```



## <a name="adding-or-removing-files-to-the-file-system"></a>Ajout ou suppression de fichiers dans le système de fichiers

Après avoir créé l’objet de système de fichiers et importé le système de fichiers à partir de la session précédente, appelez les méthodes [**IFileSystemImage :: CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) et [**IFileSystemImage :: CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) pour créer respectivement des objets de fichier et de répertoire. Les objets de fichier et de répertoire fournissent des détails spécifiques sur les fichiers et les répertoires. Vous pouvez également utiliser la méthode [**IFsiDirectoryItem :: AddTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-addtree) d’un objet d’annuaire, représenté par le biais de l’interface [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) , pour ajouter des fichiers et des répertoires existants à partir d’un autre dispositif de stockage (par exemple, un disque dur).

La méthode de mise à jour du gestionnaire d’événements disponible pour [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) identifie le fichier en cours d’ajout à l’image du système de fichiers, le nombre de secteurs déjà copiés et le nombre total de secteurs à copier.

Pour supprimer des fichiers et des répertoires existants du système de fichiers, utilisez les méthodes [**IFsiDirectoryItem :: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) et [**IFsiDirectoryItem :: RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) des objets d’annuaire représentés par le biais de l’interface [**IFsiDirectoryItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifsidirectoryitem) . La propriété [**\_ racine IFileSystemImage :: obtenir**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-get_root) est utilisée pour obtenir un pointeur vers le répertoire racine du système de fichiers et l’interface **IFsiDirectoryItem** pour traverser l’arborescence de répertoires.

> [!Note]  
> Les fichiers et répertoires supprimés via les méthodes [**IFsiDirectoryItem :: Remove**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-remove) et [**IFsiDirectoryItem :: RemoveTree**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifsidirectoryitem-removetree) ne sont pas physiquement supprimés du disque, et les logiciels avancés peuvent facilement récupérer les informations supprimées.

 


```VB
    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false
```



## <a name="constructing-a-file-system-image"></a>Construction d’une image de système de fichiers

La dernière étape consiste à appeler [**IFileSystemImage :: CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) pour créer un flux de données pour l’image de gravure et lui fournir un accès via l’interface [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult) . Ce flux de données peut être fourni directement à la méthode [**IDiscFormat2Data :: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) ou être enregistré dans un fichier en vue d’une utilisation ultérieure.


```VB
    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
```



## <a name="example-summary"></a>Exemple de résumé

l’exemple de script Visual Basic suivant montre comment utiliser des objets imapi pour créer des disques multisession. L’exemple crée une nouvelle session et ajoute un répertoire au disque. Par souci de simplicité, le code n’effectue pas de vérification étendue des erreurs et suppose les points suivants :

-   Un périphérique de disque compatible est installé sur le système.
-   Le périphérique à disque est le premier lecteur sur le système.
-   Un disque compatible est inséré dans le périphérique du disque.
-   Les fichiers à ajouter au disque se trouvent dans « g : \\ burndir ».

Des fonctionnalités supplémentaires telles que la vérification étendue des erreurs, la compatibilité des appareils et des supports, la notification d’événements et le calcul de l’espace libre sur le disque peuvent être ajoutées au script.


```VB
' This script adds data files from a single directory tree to a
' disc (a new session is added, if the disc already contains data)

' Copyright (C) Microsoft. All rights reserved.

Option Explicit

' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to add
    Dim Stream               ' Data stream for burning device
    
    Index = 0                ' First drive on the system
    Path = "G:\BurnDir"      ' Files to add to the disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim DiscMaster
    Set DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder2 object for the specified burning device.
    Dim UniqueId
    set Recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    UniqueId = DiscMaster.Item(Index)
    Recorder.InitializeDiscRecorder(UniqueId)

    ' Create a DiscFormat2Data object and set the recorder
    Dim DataWriter
    Set DataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    DataWriter.Recorder = Recorder
    DataWriter.ClientName = "IMAPIv2 TEST"

    ' Create a new file system image object
    Dim FSI
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")

    ' Import the last session, if the disc is not empty, or initialize
    ' the file system, if the disc is empty
    If Not DataWriter.MediaHeuristicallyBlank _
    Then
        On Error Resume Next
        FSI.MultisessionInterfaces = DataWriter.MultisessionInterfaces
        If Err.Number <> 0 _
        Then
            WScript.Echo "Multisession is not supported for this disc"
            Main = 1
            Exit Function
        End If
        On Error Goto 0

        WScript.Echo "Importing data from the previous session..."
        FSI.ImportFileSystem()
    Else 
        FSI.ChooseImageDefaults(Recorder)
    End If

    ' Add the directory and its contents to the file system 
    WScript.Echo "Adding " & Path & " directory to the disc..."
    FSI.Root.AddTree Path, false

    ' Create an image from the file system image object
    Dim Result
    Set Result = FSI.CreateResultImage()
    Stream = Result.ImageStream
    
    ' Write stream to disc using the specified recorder
    WScript.Echo "Writing content to the disc..."
    DataWriter.Write(Stream)

    WScript.Echo "Finished writing content."
    Main = 0
End Function

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’IMAPi](using-imapi.md)
</dt> <dt>

[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> <dt>

[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> </dl>

 

 
