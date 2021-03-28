---
description: Pour ajouter un élément au sous-menu programmes, procédez comme suit.
ms.assetid: F8793C33-2281-4E4A-9659-4189E1C8279A
title: Comment ajouter des raccourcis au menu Démarrer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77ee942e07c48ed7addf07160412008bfb5b9322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115514"
---
# <a name="how-to-add-shortcuts-to-the-start-menu"></a><span data-ttu-id="8056f-103">Comment ajouter des raccourcis au menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="8056f-103">How to Add Shortcuts to the Start Menu</span></span>

<span data-ttu-id="8056f-104">Pour ajouter un élément au sous-menu **programmes** , procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="8056f-104">To add an item to the **Programs** submenu, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="8056f-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="8056f-105">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="8056f-106">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="8056f-106">Step 1:</span></span>

<span data-ttu-id="8056f-107">Créez un [lien de Shell](./links.md) à l’aide de l’interface [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) .</span><span class="sxs-lookup"><span data-stu-id="8056f-107">Create a [shell link](./links.md) by using the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface.</span></span>

### <a name="step-2"></a><span data-ttu-id="8056f-108">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="8056f-108">Step 2:</span></span>

<span data-ttu-id="8056f-109">Obtenez l’emplacement du dossier programmes à l’aide de la fonction [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) , en passant les [**\_ programmes FOLDERID**](knownfolderid.md).</span><span class="sxs-lookup"><span data-stu-id="8056f-109">Obtain the location of the Programs folder by using the [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) function, passing [**FOLDERID\_Programs**](knownfolderid.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="8056f-110">Étape 3 :</span><span class="sxs-lookup"><span data-stu-id="8056f-110">Step 3:</span></span>

<span data-ttu-id="8056f-111">Ajoutez le lien de l’interpréteur de commandes au dossier programmes.</span><span class="sxs-lookup"><span data-stu-id="8056f-111">Add the Shell link to the Programs folder.</span></span> <span data-ttu-id="8056f-112">Vous pouvez également créer un dossier dans le dossier programmes et ajouter le lien vers ce dossier.</span><span class="sxs-lookup"><span data-stu-id="8056f-112">You can also create a folder in the Programs folder and add the link to that folder.</span></span>

 

 
