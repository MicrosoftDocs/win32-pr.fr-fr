---
description: L’infrastructure de Microsoft .NET vous donne la possibilité de déployer des applications à partir d’un serveur Web ou d’un serveur de fichiers.
ms.assetid: 7721cd92-241f-4409-a724-c8e8768a19a9
title: Aucun déploiement tactile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6567edf35dbd79256bed228de3941351bd5e7642
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106523744"
---
# <a name="no-touch-deployment"></a>Aucun déploiement tactile

L’infrastructure de Microsoft .NET vous donne la possibilité de déployer des applications à partir d’un serveur Web ou d’un serveur de fichiers. Cette technique, appelée « déploiement sans Touch », associe les performances et l’interactivité d’une application cliente intelligente à tous les avantages du déploiement d’une application Web. Pour déployer votre application sur le Web, cliquez avec le bouton droit sur le dossier qui contient votre fichier exécutable, puis sélectionnez **Propriétés**. Sous l’onglet **partage Web** , sélectionnez **partager ce dossier**. Entrez un alias pour le dossier. À présent, votre exécutable peut être exécuté sur le Web en utilisant cet alias comme répertoire sur votre serveur. Pour plus d’informations sur le déploiement sans toucher, consultez [clients intelligents .net](/archive/msdn-magazine/2002/july/net-zero-deployment-security-and-versioning-models-in-the-windows-forms-engine-help-you-create-and-deploy-smart-clients) et [déploiement sans toucher dans le .NET Framework](/documentation/?url=%2flibrary%2fdv_vstechart%2fhtml%2fvbtchno-touchdeploymentinnetframework.asp).

> [!Note]  
> Pour activer l’onglet **partage Web** dans la boîte de dialogue **Propriétés** , vous devez avoir installé Microsoft Internet Information Services (IIS) sur votre ordinateur.

 

Le déploiement sans toucher est appliqué aux applications prenant en charge l’écriture manuscrite de la même façon que n’importe quelle autre application Windows Forms. Les exemples fournis par le kit de développement logiciel (SDK) de Microsoft Windows XP Tablet PC Edition incluent une version de déploiement sans Touch de l’exemple de revendications automatiques, dans la section exemples Web manuscrits des exemples. Cet exemple prend l' [exemple de formulaire de déclaration automatique](auto-claims-form-sample.md) d’origine et fournit un programme d’installation qui place dans sur un partage Web. Lorsque Microsoft Internet Explorer accède à AutoClaims.exe dans le répertoire mappé au partage Web, l’application est lancée. Pour plus d’informations sur l’exemple [, consultez exemple Web de déploiement sans toucher](no-touch-deployment-web-sample.md) .

> [!Note]  
> Lorsque vous déployez une application .NET sur le Web, l’application peut être affectée par le modèle de sécurité .NET. La section [sécurité et confiance](security-and-trust.md) décrit le fonctionnement de la sécurité avec les applications Web compatibles avec l’écriture manuscrite.

 

 

 