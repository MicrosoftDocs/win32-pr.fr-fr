---
description: Montre comment implémenter un verbe de Shell à l’aide de la méthode CreateProcess.
title: CreateProcess, exemple de verbe
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2939BC36-35C0-4549-9971-742CBDA02547
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c0af34d5ec9f687ec6c58bb73f337b38d512527c0ace4bd20eae12d49c87a62d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858339"
---
# <a name="createprocess-verb-sample"></a>CreateProcess, exemple de verbe

Montre comment implémenter un verbe de Shell à l’aide de la méthode CreateProcess.

Cette rubrique contient les sections suivantes.

-   [Description](#description)
-   [Requirements](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)

## <a name="description"></a>Description

Les verbes basés sur CreateProcess dépendent de l’exécution d’un exécutable et de sa transmission à un argument de ligne de commande. Cette méthode n’est pas aussi puissante que les méthodes DropTarget et ExecuteCommand, mais elle permet d’obtenir le comportement out-of-process souhaitable.

## <a name="requirements"></a>Configuration requise



| Produit                                | Version minimale du produit |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Kit de développement logiciel Windows | 7.0                     |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

| Emplacement      | URL du chemin                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemple CreateProcessVerb](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/CreateProcessVerb) |

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **CreateProcessVerb** .
2.  Entrez `msbuild CreateProcessVerb.sln`.

pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  ouvrez Windows Explorer et accédez au répertoire du projet **CreateProcessVerb** .
2.  Double-cliquez sur l’icône du fichier CreateProcessVerb. sln pour ouvrir le projet dans Visual Studio.
3.  Dans le menu **Générer**, sélectionnez **Générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de l’invite de commandes ou de l’explorateur de Windows.
2.  Sur la ligne de commande, entrez `CreateProcessVerb.exe` . vous pouvez également, à partir de Windows Explorer, double-cliquer sur l’icône de CreateProcessVerb.exe.
3.  Suivez les instructions de la boîte de dialogue qui s’affiche

 

 



