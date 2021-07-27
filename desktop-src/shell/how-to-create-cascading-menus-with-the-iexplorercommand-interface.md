---
description: 'Vous pouvez également ajouter des verbes à un menu en cascade à l’aide de IExplorerCommand :: EnumSubCommands.'
ms.assetid: 010157F3-B950-4A57-B0AA-248B4990DA34
title: Créer des menus en cascade avec l’interface IExplorerCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed12cf78dc4b5f6a77bbd00b06897b49474a401
ms.sourcegitcommit: 5a78723ad484955ac91a23cf282cf9c176c1eab6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/22/2021
ms.locfileid: "114436094"
---
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a>Comment créer des menus en cascade avec l’interface IExplorerCommand

Vous pouvez également ajouter des verbes à un menu en cascade à l’aide de [**IExplorerCommand :: EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands). Cette méthode permet aux sources de données qui fournissent leurs commandes de module de commande par le biais de l’interface [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) d’utiliser ces commandes comme verbes dans un menu contextuel. dans Windows 7 et versions ultérieures, vous pouvez fournir la même implémentation de verbe à l’aide de l’interface [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) , comme vous pouvez le faire avec l’interface [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .

## <a name="instructions"></a>Instructions


Les deux captures d’écran suivantes illustrent l’utilisation des menus en cascade dans le dossier **appareils** .

![Capture d’écran montrant un exemple de menu en cascade dans le dossier appareils.](images/file-assoc/FileCascadeMenu.png)

![capture d’écran montrant un exemple de menu en cascade dans le dossier appareils](images/file-assoc/cascadeDevices2.png)

## <a name="remarks"></a>Remarques

> [!Note]  
> Étant donné que [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) prend uniquement en charge l’activation in-process, il est recommandé d’utiliser des sources de données Shell qui doivent partager l’implémentation entre des commandes et des menus contextuels.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)
</dt> <dt>

[**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider)
</dt> <dt>

[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
</dt> </dl>

 

 
