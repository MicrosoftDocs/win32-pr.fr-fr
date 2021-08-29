---
description: Si une application doit être inscrite, créez le package d’installation comme décrit dans la section Ajout et suppression de clés de registre lors de l’installation ou de la suppression de composants.
ms.assetid: d2c6afde-cede-4ed1-ac1a-8ddb1bc73ec2
title: Ajout et suppression d’une application et absence de trace dans le registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa6d3884a91efefac9cab1409a36e1843941469aae9822154be5534313b05c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105459"
---
# <a name="adding-and-removing-an-application-and-leaving-no-trace-in-the-registry"></a>Ajout et suppression d’une application et absence de trace dans le registre

Si une application doit être inscrite, créez le package d’installation comme décrit dans la section [Ajout et suppression de clés de registre lors de l’installation ou de la suppression de composants](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md). L’inscription est utilisée par le programme d’installation pour la publication et par la fonctionnalité Ajout/suppression de programmes du panneau de configuration. Si une application n’est pas inscrite, elle ne peut pas être publiée et n’est pas répertoriée dans la fonctionnalité Ajout/suppression de programmes du panneau de configuration.

Vous pouvez omettre l’inscription d’une application en supprimant l’action [RegisterProduct](registerproduct-action.md), l’action [RegisterUser](registeruser-action.md), l’action [PublishProduct](publishproduct-action.md)et l' [action PublishFeatures](publishfeatures-action.md) de la table [InstallExecuteSequence](installexecutesequence-table.md) et de la [table AdvtExecuteSequence](advtexecutesequence-table.md). Toutes ces actions doivent être supprimées ou une trace de l’application peut rester dans le registre. La suppression de toutes ces actions empêche l’application d’être listée dans la fonctionnalité Ajout/suppression de programmes du panneau de configuration et empêche la publication de l’application. la suppression de toutes ces actions empêche également l’inscription de l’application avec les données de configuration de Windows Installer. cela signifie que vous ne pouvez pas supprimer, réparer ou réinstaller l’application à l’aide des [Options de ligne de commande](command-line-options.md)Windows Installer, ni de l’interface de programmation d’applications (API) Windows Installer.

pour masquer une application à partir de la fonctionnalité ajout/suppression de programmes du panneau de configuration tout en étant en mesure d’utiliser la Windows Installer pour gérer une application, laissez les actions d’inscription dans les tables de séquence et définissez la [**propriété ARPSYSTEMCOMPONENT**](arpsystemcomponent.md) dans la [Table de propriétés](property-table.md) sur 1 (un). l’application n’apparaît pas dans la fonctionnalité ajout/suppression de programmes, mais vous pouvez utiliser le Windows Installer pour installer à la demande, désinstaller, réparer et réinstaller l’application.

 

 



