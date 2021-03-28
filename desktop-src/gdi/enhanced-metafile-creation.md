---
description: Vous créez un métafichier amélioré à l’aide de la fonction CreateEnhMetaFile, en fournissant les arguments appropriés.
ms.assetid: b012e50e-a7f5-4687-9833-38dacc113d77
title: Création de métafichiers améliorée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 080c350e41e895c5d4bf834a6f407cca5907743d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754413"
---
# <a name="enhanced-metafile-creation"></a>Création de métafichiers améliorée

Vous créez un métafichier amélioré à l’aide de la fonction [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) , en fournissant les arguments appropriés. Le système utilise ces arguments pour conserver les dimensions de l’image, déterminer si le métafichier doit être stocké sur un disque ou en mémoire, et ainsi de suite.

Pour conserver les dimensions d’image sur les périphériques de sortie, [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) requiert la résolution de l’appareil de référence. Ce *périphérique de référence* est l’appareil sur lequel l’image est apparue pour la première fois, et le *DC de référence* est le *contexte de périphérique* associé à l’appareil de référence. Lors de l’appel de la fonction **CreateEnhMetaFile** , vous devez fournir un handle qui identifie ce contrôleur de périphérique. Vous pouvez récupérer ce handle en appelant la fonction [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) ou [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) . Vous pouvez également spécifier **null** comme handle pour utiliser le périphérique d’affichage actuel pour l’appareil de référence.

La plupart des applications stockent des images de manière permanente et, par conséquent, créent un métafichier amélioré stocké sur un disque. Toutefois, il y a des cas où cela n’est pas nécessaire. Par exemple, une application de traitement de texte qui fournit des fonctionnalités de dessin de graphique peut stocker un graphique défini par l’utilisateur en mémoire en tant que métafichier amélioré, puis copier les bits de métafichier améliorés de la mémoire dans le fichier de document de l’utilisateur. Une application qui requiert un métafichier qui est stocké de manière permanente sur un disque doit fournir le nom de fichier lorsqu’il appelle [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea). Si vous ne fournissez pas de nom de fichier, le système traite automatiquement le métafichier comme un fichier temporaire et le stocke dans la mémoire.

Vous pouvez ajouter une description textuelle facultative à un métafichier contenant des informations sur l’image et l’auteur. Une application peut afficher ces chaînes dans la boîte de dialogue Ouvrir un fichier pour fournir à l’utilisateur des informations sur le contenu du métafichier qui vous aideront à sélectionner le fichier approprié. Si une application comprend la description textuelle, elle doit fournir un pointeur vers la chaîne lorsqu’elle appelle [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea).

Quand [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) parvient, il retourne un handle qui identifie un contexte de périphérique de métafichier spécial. Un contexte de périphérique de métafichier est unique en ce qu’il est associé à un fichier plutôt qu’à un périphérique de sortie. Lorsque le système traite une fonction GDI qui a reçu un handle vers un contexte de périphérique de métafichier, il convertit la fonction GDI en un enregistrement de métafichier amélioré et ajoute l’enregistrement à la fin du métafichier amélioré.

Une fois l’image terminée et le dernier enregistrement ajouté au métafichier amélioré, l’application peut fermer le fichier en appelant la fonction [**CloseEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-closeenhmetafile) . Cette fonction ferme et supprime le contexte de périphérique de métafichier spécial et retourne un handle identifiant le métafichier amélioré.

Pour supprimer un métafichier de format amélioré ou un handle de métafichier de format amélioré, appelez la fonction [**DeleteEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-deleteenhmetafile) .

 

 



