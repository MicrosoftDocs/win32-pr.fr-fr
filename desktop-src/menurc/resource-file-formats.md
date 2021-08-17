---
title: Formats de fichiers de ressources
description: Cette section décrit le format du fichier de ressources binaires que le compilateur de ressources crée en fonction du contenu du fichier de définition de ressource.
ms.assetid: a0b17555-f50a-4d58-b2bc-760843dd67eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16bfc85190993992b7bf87001f3d807b777ed2fe27b4d66cba0b7f7c948d8cfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869790"
---
# <a name="resource-file-formats"></a>Formats de fichiers de ressources

Cette section décrit le format du fichier de ressources binaires que le compilateur de ressources crée en fonction du contenu du fichier de définition de ressource. Ce fichier a généralement une extension. res. L’éditeur de liens reformate le fichier. res en fichier d’objet de ressource, puis le lie au fichier exécutable d’une application.

Un fichier de ressources binaire se compose d’un certain nombre d’entrées de ressources concaténées. Chaque entrée se compose d’un en-tête de ressource et des données de cette ressource. Un en-tête de ressource est aligné sur **DWORD** dans le fichier et se compose des éléments suivants :

-   **Valeur DWORD** qui contient la taille de l’en-tête de ressource
-   **Valeur DWORD** qui contient la taille des données de ressource.
-   Type de ressource
-   Nom de la ressource
-   Informations supplémentaires sur les ressources

La structure [**RESOURCEHEADER**](resourceheader.md) décrit le format de cet en-tête. Les données de la ressource suivent l’en-tête de ressource et sont spécifiques à chaque type de ressource. Certaines ressources emploient également une structure d’en-tête de groupe spécifique aux ressources pour fournir des informations sur un groupe de ressources.

## <a name="accelerator-table-resources"></a>Ressources de la table d’accélérateurs

Une table d’accélérateurs est une entrée de ressource dans un fichier de ressources. Il n’a pas d’en-tête de groupe. Une structure [**ACCELTABLEENTRY**](acceltableentry.md) décrit chaque entrée de la table d’accélérateurs. Plusieurs tables d’accélérateurs sont autorisées.

## <a name="cursor-and-icon-resources"></a>Ressources curseur et icône

Le système gère chaque icône et chaque curseur sous la forme d’un fichier unique. Toutefois, ceux-ci sont stockés dans des fichiers. res et dans des fichiers exécutables sous la forme d’un groupe de ressources d’icône ou d’un groupe de ressources curseur. Les formats de fichier des ressources icône et curseur sont similaires. Dans le fichier. res, un en-tête de groupe de ressources suit tous les composants individuels des icônes ou des groupes de curseurs.

Le format de chaque composant d’icône ressemble de près au format du fichier. ico. Chaque image d’icône est stockée dans une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) suivie par les bits DIB (Device-Independent Bitmap) du masque **Xor** de l’icône. Les bits DIB monochrome de l’icône **et** du masque suivent les bits de couleur dib.

Le format de chaque composant de curseur est semblable au format du fichier. cur. Chaque image de curseur est stockée dans une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) suivie des bits DIB monochrome du masque **Xor** du curseur, puis par les bits DIB monochrome des curseurs **et** du masque. Notez qu’il existe une différence dans les bitmaps des deux ressources : contrairement aux icônes, les masques de curseur XOR n’ont pas de bits de couleur DIB. Bien que les bitmaps des masques de curseur soient monochromes et ne possèdent pas d’en-têtes ou de tables de couleurs DIB, les bits sont toujours au format DIB en ce qui concerne l’alignement et la direction. Une autre différence importante entre les curseurs et les icônes est que les curseurs ont une zone réactive et des icônes.

L’en-tête de groupe pour les ressources d’icône et de curseur se compose d’une structure [**NEWHEADER**](newheader.md) plus une ou plusieurs structures [**RESDIR**](resdir.md) . Il existe une structure **RESDIR** pour chaque icône ou curseur. L’en-tête de groupe contient les informations dont une application a besoin pour sélectionner l’icône ou le curseur correct à afficher. L’en-tête de groupe et les données qui se répètent pour chaque icône ou curseur du groupe ont une longueur fixe. Cela permet à l’application d’accéder de manière aléatoire aux informations.

## <a name="dialog-box-resources"></a>Ressources de boîte de dialogue

Une boîte de dialogue est également une entrée de ressource dans le fichier de ressources. Il se compose d’une structure d’en-tête de boîte de dialogue [**DLGTEMPLATE**](/windows/desktop/api/winuser/ns-winuser-dlgtemplate) plus une structure [**DLGITEMTEMPLATE**](/windows/desktop/api/winuser/ns-winuser-dlgitemtemplate) pour chaque contrôle dans la boîte de dialogue. Les structures [**DLGTEMPLATEEX**](/windows/desktop/dlgbox/dlgtemplateex) et [**DLGITEMTEMPLATEEX**](/windows/desktop/dlgbox/dlgitemtemplateex) décrivent le format des ressources de boîte de dialogue étendues.

## <a name="font-resources"></a>Ressources de police

Les polices sont stockées dans le fichier de ressources en tant que groupe de ressources. Les différentes polices composent un groupe de polices. Instruction de définition de ressource d' [instruction de police](./font-statement.md) dans le. Le fichier RC définit chaque police. Chaque police individuelle de la ressource se compose du contenu complet du fichier. FNT associé. Une structure [**FONTGROUPHDR**](fontgrouphdr.md) suit tous les composants de police individuels dans le fichier. res.

Les ressources de police ne sont pas ajoutées aux ressources d’une application spécifique. Au lieu de cela, ils sont généralement ajoutés aux fichiers exécutables qui ont une extension. fon. Ces fichiers sont généralement des dll de ressources uniquement plutôt que des applications.

## <a name="menu-resources"></a>Ressources de menu

Une *ressource de menu* se compose d’une structure [**MENUHEADER**](menuheader.md) suivie d’une ou de plusieurs structures [**NORMALMENUITEM**](normalmenuitem.md) ou [**POPUPMENUITEM**](popupmenuitem.md) , une pour chaque élément de menu dans le modèle de menu. L' [**\_ \_ en-tête de modèle menuex**](menuex-template-header.md) et les structures d' [**\_ \_ élément de modèle menuex**](menuex-template-item.md) décrivent le format des ressources de menu étendu.

## <a name="message-table-resources"></a>Ressources de la table de messages

Une *table de messages* est une ressource qui contient le texte mis en forme à afficher en tant que message d’erreur ou dans une boîte de message. La structure principale d’une ressource de table de messages est la structure de [**\_ \_ données de ressource de message**](/windows/desktop/api/Winnt/ns-winnt-message_resource_data) .

## <a name="version-resources"></a>Ressources de version

La structure principale d’une ressource de version est la structure [**vs \_ FIXEDFILEINFO**](/windows/win32/api/verrsrc/ns-verrsrc-vs_fixedfileinfo) . Les structures supplémentaires incluent la structure [**VarFileInfo**](varfileinfo.md) pour stocker les données d’informations de langue et [**StringFileInfo**](stringfileinfo.md) pour les informations de chaîne définies par l’utilisateur. Toutes les chaînes d’une ressource de version sont au format Unicode. Chaque bloc d’informations est aligné sur une limite **DWORD** .

 

 