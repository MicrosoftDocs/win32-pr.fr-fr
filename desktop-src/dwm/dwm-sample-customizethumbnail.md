---
title: Personnaliser une miniature d’icône et une image bitmap Live Preview
description: Montre comment personnaliser une miniature sous forme et une image bitmap en mode aperçu instantané (également appelée aperçu de lecture).
ms.assetid: 43fe71e7-4e5c-46fb-876b-e26996071665
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 8fceb94727257b51a2e6235cbfcc44b155635343
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/20/2021
ms.locfileid: "106538072"
---
# <a name="customize-an-iconic-thumbnail-and-a-live-preview-bitmap"></a>Personnaliser une miniature d’icône et une image bitmap Live Preview

## <a name="description"></a>Description

Vous pouvez personnaliser une image bitmap sous forme et une image de l' *aperçu instantané* (ou aperçu de l' *Aperçu*) en utilisant des fonctions et des messages introduits dans les API Windows 7 gestionnaire de fenêtrage (DWM).

Plus précisément, vous utilisez la fonction [**DwmSetIconicThumbnail**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) et le message [**WM \_ SENDICONICTHUMBNAILBITMAP**](wm-dwmsendiconicthumbnail.md) pour personnaliser une miniature de sous forme. Vous pouvez également utiliser la fonction [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) et le message [**WM \_ SENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md) pour définir une image bitmap de l’aperçu instantané de sous forme.

Pour obtenir un exemple d’application qui utilise la fonction **DwmSetIconicThumbnail** , consultez [exemple TabThumbnails](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails).

L’illustration suivante montre une miniature par défaut transformée en miniature personnalisée.

![illustration d’une image miniature d’origine et d’une image miniature modifiée avec une bitmap personnalisée](images/customthumbnail.jpg)

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|--------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows 7 ou Windows Vista avec Service Pack 2 (SP2) et mise à jour de la plateforme pour Windows Vista                          |
| Serveur minimal pris en charge | Windows Server 2008 R2 ou Windows Server 2008 avec Service Pack 2 (SP2) et mise à jour de plateforme pour Windows Server 2008 |
| SDK Windows minimal      | [Kit de développement logiciel (SDK) Windows pour Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx)             |

## <a name="building-the-tabthumbnails-sample"></a>Génération de l’exemple TabThumbnails

**Pour générer l’exemple à l’aide de Microsoft Visual Studio (méthode recommandée)**

1.  Ouvrez l’Explorateur Windows et accédez au dossier où se trouve le fichier TabThumbnails. sln.
2.  Double-cliquez sur le fichier solution (. sln) pour ouvrir le fichier dans Microsoft Visual Studio.
3.  Dans le menu **Générer**, cliquez sur **Générer la solution**. L’application est générée dans le \\ Répertoire de débogage ou de version par défaut \\ .

**Pour générer l’exemple à l’aide de l’invite de commandes**

1.  Ouvrez une fenêtre d’invite de commandes et accédez au répertoire de l’exemple.
2.  Entrez `msbuild TabThumbnails.sln`.

## <a name="related-topics"></a>Rubriques connexes

[Gestionnaire de fenêtres du Bureau](dwm-overview.md)

[Développement Windows](/windows/desktop/win32-and-com-development)
