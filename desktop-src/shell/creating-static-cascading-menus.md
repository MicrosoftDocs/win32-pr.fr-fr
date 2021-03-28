---
description: À compter de Windows 7, les menus en cascade sont créés par le biais de l’entrée de Registre subcommandes, de l’entrée de Registre ExtendedSubCommandsKey ou de l’interface IExplorerCommand.
title: Création de menus en cascade statiques
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E3A6F174-BE53-48EF-AE9B-A3F297E91B95
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d812b4d3d2fb0754002cb37d72718e4fe861ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104562463"
---
# <a name="creating-static-cascading-menus"></a><span data-ttu-id="8029a-103">Création de menus en cascade statiques</span><span class="sxs-lookup"><span data-stu-id="8029a-103">Creating Static Cascading Menus</span></span>

<span data-ttu-id="8029a-104">Dans Windows 7 et versions ultérieures, l’implémentation des menus en cascade est prise en charge via les paramètres du Registre.</span><span class="sxs-lookup"><span data-stu-id="8029a-104">In Windows 7 and later, cascading menu implementation is supported through registry settings.</span></span> <span data-ttu-id="8029a-105">Avant Windows 7, la création de menus en cascade était possible uniquement via l’implémentation de l’interface [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="8029a-105">Prior to Windows 7, the creation of cascading menus was possible only through the implementation of the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span> <span data-ttu-id="8029a-106">Dans Windows 7 et versions ultérieures, vous devez recourir à des solutions basées sur du code COM (Component Object Model) uniquement lorsque les méthodes statiques sont insuffisantes.</span><span class="sxs-lookup"><span data-stu-id="8029a-106">In Windows 7 and later, you should resort to Component Object Model (COM) code-based solutions only when the static methods are insufficient.</span></span>

<span data-ttu-id="8029a-107">La capture d’écran suivante fournit un exemple de menu en cascade.</span><span class="sxs-lookup"><span data-stu-id="8029a-107">The following screen shot provides an example of a cascading menu.</span></span>

![capture d’écran montrant un exemple de menu en cascade](images/file-assoc/filecascademenu2ndex.png)

<span data-ttu-id="8029a-109">Dans Windows 7 et versions ultérieures, il existe trois façons de créer des menus en cascade, qui sont décrits dans les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="8029a-109">In Windows 7 and later, there are three ways to create cascading menus, which are described in the following sections.</span></span>

-   [<span data-ttu-id="8029a-110">Comment créer des menus en cascade avec l’entrée de Registre subcommandes</span><span class="sxs-lookup"><span data-stu-id="8029a-110">How to Create Cascading Menus with the SubCommands Registry Entry</span></span>](how-to--create-cascading-menus-with-the-subcommands-registry-entry.md)
-   [<span data-ttu-id="8029a-111">Comment créer des menus en cascade avec l’entrée de Registre ExtendedSubCommandsKey</span><span class="sxs-lookup"><span data-stu-id="8029a-111">How to Create Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>](how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry.md)
-   [<span data-ttu-id="8029a-112">Comment créer des menus en cascade avec l’interface IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="8029a-112">How to Create Cascading Menus with the IExplorerCommand Interface</span></span>](how-to-create-cascading-menus-with-the-iexplorercommand-interface.md)

 

 
