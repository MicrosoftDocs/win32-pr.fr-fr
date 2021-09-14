---
description: 'Vous pouvez utiliser le handle vers un métafichier amélioré pour effectuer les tâches suivantes :'
ms.assetid: 8f887c38-6cfa-4918-aa44-dd5fb837b40b
title: Opérations de métafichier améliorées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ba9e2ac2f14c4436c039a66cc3211b471c0461
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120253"
---
# <a name="enhanced-metafile-operations"></a>Opérations de métafichier améliorées

Vous pouvez utiliser le handle vers un métafichier amélioré pour effectuer les tâches suivantes :

-   Affichez l’image stockée dans un métafichier amélioré.
-   Créer des copies d’un métafichier amélioré.
-   Modifiez un métafichier amélioré.
-   Récupère la description facultative stockée dans un métafichier amélioré.
-   Récupère une copie d’un en-tête de métafichier amélioré.
-   Récupérer une version binaire d’un métafichier amélioré.
-   Énumérer les couleurs dans la palette facultative.

Ces tâches sont décrites dans les sections du reste de cette rubrique.

## <a name="display-the-picture-stored-in-an-enhanced-metafile"></a>Afficher l’image stockée dans un métafichier amélioré

Vous pouvez afficher l’image stockée dans un métafichier amélioré à l’aide de la fonction [**PlayEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile) . Transmettez la fonction à un handle vers le métafichier amélioré, sans vous préoccuper du format des enregistrements de métafichiers améliorés. Toutefois, il est parfois souhaitable d’énumérer les enregistrements dans le métafichier amélioré pour rechercher une fonction GDI particulière et modifier les paramètres de la fonction d’une certaine manière. Pour ce faire, vous pouvez utiliser [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) et fournir une fonction de rappel, [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc), pour traiter les enregistrements de métafichiers améliorés. Pour modifier les paramètres d’un enregistrement de métafichier amélioré, vous devez connaître le format des paramètres dans l’enregistrement.

## <a name="create-copies-of-an-enhanced-metafile"></a>Créer des copies d’un métafichier amélioré

Certaines applications créent des copies de sauvegarde temporaire (ou en double) d’un fichier avant de permettre à l’utilisateur de modifier l’original. Une application peut créer une copie de sauvegarde d’un métafichier amélioré en appelant la fonction [**CopyEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-copyenhmetafilea) , en fournissant un handle qui identifie le métafichier amélioré et en fournissant un pointeur vers le nom du nouveau fichier.

Pour créer un métafichier de format amélioré basé sur la mémoire, appelez la fonction [**SetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-setenhmetafilebits) .

## <a name="edit-an-enhanced-metafile"></a>Modifier un métafichier amélioré

La plupart des applications de dessin, d’illustration et de conception assistée par ordinateur (CAD) requièrent un moyen de modifier une image stockée dans un métafichier amélioré. Bien que la modification d’un métafichier amélioré soit une tâche complexe, vous pouvez utiliser la fonction [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) conjointement avec d’autres fonctions pour fournir cette fonctionnalité dans votre application. La fonction **EnumEnhMetaFile** et sa fonction de rappel associée, [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc), permettent à l’application de traiter des enregistrements individuels dans un métafichier amélioré.

## <a name="retrieve-the-optional-description-stored-in-an-enhanced-metafile"></a>Récupérer la description facultative stockée dans un métafichier amélioré

Certaines applications affichent la description textuelle d’un métafichier amélioré avec le nom de fichier correspondant dans la boîte de dialogue **ouvrir** . Vous pouvez déterminer si cette chaîne existe dans un métafichier amélioré en extrayant l’en-tête du métafichier avec la fonction [**GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) et en examinant l’un de ses membres. Si la chaîne existe, l’application la récupère en appelant la fonction [**GetEnhMetaFileDescription**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafiledescriptiona) .

## <a name="retrieve-a-binary-version-of-an-enhanced-metafile"></a>Récupérer une version binaire d’un métafichier amélioré

Vous pouvez récupérer le contenu d’un métafichier en appelant la fonction [**GetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilebits) ; Toutefois, avant de récupérer le contenu, vous devez spécifier la taille du fichier. Pour connaître la taille, vous pouvez utiliser la fonction [**GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) et examiner le membre approprié.

## <a name="enumerate-the-colors-in-the-optional-palette"></a>Énumérer les couleurs dans la palette facultative

Pour obtenir des couleurs cohérentes quand une image est affichée sur différents périphériques de sortie, vous pouvez appeler la fonction [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette) et stocker une palette logique dans un métafichier amélioré. Une application qui affiche l’image stockée dans le métafichier amélioré récupère cette palette et appelle la fonction [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) avant d’afficher l’image. Pour déterminer si une palette est stockée dans un métafichier amélioré, récupérez l’en-tête du métafichier et examinez le membre approprié. Si une palette existe, vous pouvez appeler la fonction [**GetEnhMetaFilePaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilepaletteentries) pour récupérer la palette logique.

 

 
