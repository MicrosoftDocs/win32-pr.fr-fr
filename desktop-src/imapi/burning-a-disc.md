---
title: Gravure d’une image de disque
description: 'La maîtrise (gravure d’un disque) à l’aide d’IMAPi se compose des étapes suivantes : créer une image de système de fichiers qui contient les répertoires et les fichiers pour écrire le disque. Configurez un enregistreur de disque pour communiquer avec le périphérique optique. Créez un enregistreur de données et gravez l’image sur le disque.'
ms.assetid: f2eee14e-695d-4678-b3c1-b521ab4d4a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 237a4aa73b6820b75b4a9a1ed03baeeb87ac093bfc549cb9cc0ed947077515dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758909"
---
# <a name="burning-a-disc-image"></a>Gravure d’une image de disque

La maîtrise (gravure d’un disque) à l’aide d’IMAPi comprend les étapes suivantes :

1.  Construisez une image de système de fichiers qui contient les répertoires et les fichiers pour écrire le disque.
2.  [Configurez un enregistreur de disque](#set-up-a-disc-recorder) pour communiquer avec le périphérique optique.
3.  [Créez un enregistreur de données](#create-a-data-writer-and-write-the-burn-image) et gravez l’image sur le disque.

Pour obtenir un exemple qui grave une image disque, consultez l' [exemple VBScript](#vbscript-example).

## <a name="construct-a-burn-image"></a>Construire une image de gravure

Une image de gravure est un flux de données qui est prêt à être écrit sur un support optique. L’image de gravure pour les formats ISO9660, Joliet et UDF se compose d’un système de fichiers de fichiers et de répertoires individuels. L’objet **CFileSystemImage** est l’objet de système de fichiers qui contient les fichiers et les répertoires à placer sur le média optique. L’interface [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) fournit l’accès à l’objet et aux paramètres du système de fichiers.

Après avoir créé l’objet de système de fichiers, appelez les méthodes [**IFileSystemImage :: CreateFileItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createfileitem) et [**IFileSystemImage :: CreateDirectoryItem**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createdirectoryitem) pour créer respectivement les objets de fichier et de répertoire. Les objets de fichier et de répertoire peuvent être utilisés pour fournir des détails spécifiques sur le fichier et le répertoire. Les méthodes de gestionnaire d’événements disponibles pour [**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage) peuvent identifier le fichier en cours d’ajout à l’image du système de fichiers, le nombre de secteurs déjà copiés et le nombre total de secteurs à copier.

Si vous le souhaitez, une image de démarrage peut être attachée au système de fichiers à l’aide de la propriété [**IFileSystemImage ::p ut \_ BootImageOptions**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-put_bootimageoptions) . Pour obtenir un exemple, consultez [Ajout d’une image de démarrage](adding-a-boot-image.md).

Enfin, appelez [**IFileSystemImage :: CreateResultImage**](/windows/desktop/api/imapi2fs/nf-imapi2fs-ifilesystemimage-createresultimage) pour créer un flux de données et fournir l’accès via [**IFileSystemImageResult**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimageresult). Le nouveau flux de données peut ensuite être fourni directement à la méthode [**IDiscFormat2Data :: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) ou être enregistré dans un fichier pour une utilisation ultérieure.

## <a name="set-up-a-disc-recorder"></a>Configurer un enregistreur de disque

L’objet **MsftDiscMaster2** fournit une énumération des périphériques optiques sur le système. L’interface [**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2) fournit l’accès à l’énumération d’appareils résultante. Parcourez les énumérations pour localiser un appareil d’enregistrement approprié. L’objet **MsftDiscMaster2** fournit également des notifications d’événements lors de l’ajout ou de la suppression d’appareils optiques sur un ordinateur.

Après avoir trouvé un enregistreur optique et avoir récupéré son ID, créez un objet **MsftDiscRecorder2** et initialisez l’enregistreur à l’aide de l’ID de l’appareil. L’interface [**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2) fournit l’accès à l’objet enregistreur, ainsi que des informations de base sur l’appareil, telles que l’ID du fournisseur, l’ID du produit, la révision du produit et les méthodes permettant d’éjecter le support et de fermer la barre d’État.

## <a name="create-a-data-writer-and-write-the-burn-image"></a>Créer un writer de données et écrire l’image de gravure

L’objet **MsftDiscFormat2Data** fournit la méthode d’écriture, les propriétés relatives à la fonction d’écriture et aux propriétés spécifiques au média. L’interface [**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data) fournit l’accès à l’objet **MsftDiscFormat2Data** .

L’enregistreur de disque est lié au writer de format à l’aide de la propriété [**IDiscFormat2Data ::p ut \_ Recorder**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-put_recorder) . Une fois que l’enregistreur est lié au writer de format, vous pouvez exécuter des requêtes sur le média et mettre à jour les propriétés spécifiques à l’écriture avant d’écrire l’image de résultat sur le disque à l’aide de la méthode [**IDiscFormat2Data :: Write**](/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-write) .

D’autres interfaces d’écriture de format fournies par IMAPi fonctionnent de la même manière. les interfaces d’écriture de format supplémentaires sont les suivantes :

-   [**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase) efface les supports optiques réinscriptibles.
-   [**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd) écrit une image brute sur un support optique.
-   [**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce) écrit des pistes audio sur un support optique.

> [!Note]  
> Il est possible qu’une transition de l’état d’alimentation ait lieu pendant une opération de gravure (c’est-à-dire une fermeture de session de l’utilisateur ou une interruption du système), entraînant l’interruption du processus de gravure et une perte de données éventuelle. Pour plus d’informations sur la programmation, consultez [empêcher la déconnexion ou l’interruption pendant une gravure](preventing-logoff-or-suspend-during-a-burn.md).

 

## <a name="vbscript-example"></a>Exemple VBScript

Cet exemple de script montre comment utiliser les objets IMAPi pour graver un média optique. plus précisément, écrivez un répertoire sur un disque vierge. Le code ne contient pas de vérification des erreurs et suppose les points suivants :

-   Un périphérique de disque compatible est installé sur le système.
-   Le périphérique à disque est le deuxième lecteur du système.
-   Un disque compatible est inséré dans le périphérique du disque.
-   Le disque est vide.
-   Les fichiers à écrire sur le disque se trouvent dans « g : \\ burndir ».

Des fonctionnalités supplémentaires telles que la vérification des erreurs, la compatibilité des appareils et des supports, la notification d’événements et le calcul de l’espace libre sur le disque peuvent être ajoutées à ce script.


```VB
' This script burns data files to disc in a single session 
' using files from a single directory tree.
 
' Copyright (C) Microsoft Corp. 2006

Option Explicit

' *** CD/DVD disc file system types
Const FsiFileSystemISO9660 = 1
Const FsiFileSystemJoliet  = 2
Const FsiFileSystemUDF102  = 4

WScript.Quit(Main)

Function Main
    Dim Index                ' Index to recording drive.
    Dim Recorder             ' Recorder object
    Dim Path                 ' Directory of files to burn
    Dim Stream               ' Data stream for burning device
    
    Index = 1                ' Second drive on the system
    Path = "g:\BurnDir"      ' Files to transfer to disc

    ' Create a DiscMaster2 object to connect to optical drives.
    Dim g_DiscMaster
    Set g_DiscMaster = WScript.CreateObject("IMAPI2.MsftDiscMaster2")

    ' Create a DiscRecorder object for the specified burning device.
    Dim uniqueId
    set recorder = WScript.CreateObject("IMAPI2.MsftDiscRecorder2")
    uniqueId = g_DiscMaster.Item(index)
    recorder.InitializeDiscRecorder( uniqueId )

    ' Create an image stream for a specified directory.
    Dim FSI                  ' Disc file system
    Dim Dir                  ' Root directory of the disc file system
    Dim dataWriter    
        
    ' Create a new file system image and retrieve root directory
    Set FSI = CreateObject("IMAPI2FS.MsftFileSystemImage")
    Set Dir = FSI.Root

    'Create the new disc format and set the recorder
    Set dataWriter = CreateObject ("IMAPI2.MsftDiscFormat2Data")
    dataWriter.recorder = Recorder
    dataWriter.ClientName = "IMAPIv2 TEST"

    FSI.ChooseImageDefaults(recorder)
        
    ' Add the directory and its contents to the file system 
    Dir.AddTree Path, false
        
    ' Create an image from the file system
    Dim result
    Set result = FSI.CreateResultImage()
    Stream = result.ImageStream
    
    ' Write stream to disc using the specified recorder.
    WScript.Echo "Writing content to disc..."
    dataWriter.write(Stream)

    WScript.Echo "----- Finished writing content -----"
    Main = 0
End Function

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’IMAPi](using-imapi.md)
</dt> <dt>

[**IDiscFormat2Data**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data)
</dt> <dt>

[**IDiscFormat2Erase**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2erase)
</dt> <dt>

[**IDiscFormat2RawCD**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2rawcd)
</dt> <dt>

[**IDiscFormat2TrackAtOnce**](/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonce)
</dt> <dt>

[**IDiscMaster2**](/windows/desktop/api/imapi2/nn-imapi2-idiscmaster2)
</dt> <dt>

[**IDiscRecorder2**](/windows/desktop/api/imapi2/nn-imapi2-idiscrecorder2)
</dt> <dt>

[**IFileSystemImage**](/windows/desktop/api/imapi2fs/nn-imapi2fs-ifilesystemimage)
</dt> <dt>

[**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)
</dt> </dl>

 

 