---
description: Montre comment étendre le menu contextuel glisser-déplacer (parfois appelé menu contextuel).
title: NonDefaultDropMenuVerb, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: F19B7561-D280-41df-A829-15960FEB12F8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 9d326e012fb78b04fd542f88d49c370e8aeab613
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196448"
---
# <a name="nondefaultdropmenuverb-sample"></a>NonDefaultDropMenuVerb, exemple

Montre comment étendre le menu contextuel glisser-déplacer (parfois appelé menu contextuel).

Cette rubrique contient les sections suivantes.

-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)

## <a name="requirements"></a>Spécifications



| Produit                                | Version minimale du produit |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de développement logiciel Windows | 7.0                     |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

| Emplacement      | URL du chemin                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemple NonDefaultDropMenuVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NonDefaultDropMenuVerb) |

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **NonDefaultDropMenuVerb** .
2.  Entrez `msbuild NonDefaultDropMenuVerb.sln`.

pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  ouvrez Windows Explorer et accédez au répertoire du projet **NonDefaultDropMenuVerb** .
2.  Double-cliquez sur l’icône du fichier NonDefaultDropMenuVerb. sln pour ouvrir le projet dans Visual Studio.
3.  Dans le menu **Générer**, sélectionnez **Générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  accédez au répertoire qui contient le nouveau fichier DLL à l’aide de l’invite de commandes ou de l’explorateur de Windows.
2.  copiez NonDefaultDropMenuVerb.dll dans le répertoire système (par exemple, C : \\ Windows \\ System32).
3.  À l’invite de commandes, entrez `regedit NonDefaultDropMenuVerb.reg` .
4.  Utilisez le bouton droit de la souris pour faire glisser un fichier d’un dossier vers un autre. Des éléments de menu supplémentaires s’affichent pour l’opération de déplacement.

 

 



