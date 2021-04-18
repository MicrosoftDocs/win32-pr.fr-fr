---
description: Les Windows Installer peuvent annoncer la disponibilité d’une application aux utilisateurs ou à d’autres applications sans réellement installer l’application.
ms.assetid: 67170daa-448a-4a20-b38a-2dd36c95440f
title: Publication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bb31f14fb4cd6f589e94939afdd5575df52c43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519661"
---
# <a name="advertisement"></a>Publication

Les Windows Installer peuvent annoncer la disponibilité d’une application aux utilisateurs ou à d’autres applications sans réellement installer l’application. Si une application est publiée, seules les interfaces requises pour le chargement et le lancement de l’application sont présentées à l’utilisateur ou à d’autres applications. Si un utilisateur ou une application active une interface publiée, le programme d’installation continue à installer les composants nécessaires, comme décrit dans [installation à la demande](installation-on-demand.md).

Les deux types de publicité sont l’attribution et la publication. Une application est installée pour un utilisateur lorsque cette application est assignée à l’utilisateur. Le menu **Démarrer** contient les raccourcis appropriés, les icônes sont affichées, les fichiers sont associés à l’application, et les entrées de Registre reflètent l’installation de l’application. Lorsque l’utilisateur tente d’ouvrir une application affectée, il est installé à la demande.

Le programme d’installation prend en charge la publication d’applications et de fonctionnalités selon le système d’exploitation. Le programme d’installation inscrit les informations de classe COM pour les applications attribuées à partir de Windows XP. Cela permet au programme d’installation d’installer l’application lors de la création d’une instance d’une classe publiée. Pour plus d’informations, consultez [prise en charge des plateformes de la publication](platform-support-of-advertisement.md).

Vous pouvez publier une application à partir du serveur à partir de Windows Server 2003. L’application publiée est ensuite installée par le biais de son association de fichiers ou du type MIME (Multipurpose Internet Mail extension). La publication ne remplit pas l’interface utilisateur avec les icônes de l’application. Le système d’exploitation client peut installer une application publiée à partir de Windows XP.

 

 



