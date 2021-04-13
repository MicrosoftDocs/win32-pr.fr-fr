---
description: Pour utiliser le modèle de script WIA (Windows Image Acquisition), le fichier Wiascr.dll doit être installé et enregistré sur l’ordinateur.
ms.assetid: 94b08833-9fbd-46cf-b6a3-71713cc6ac30
title: Configuration de l’environnement de développement du modèle de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6b70d52e937e93f26f95926c5ec2319611b2e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201485"
---
# <a name="setting-up-the-scripting-model-development-environment"></a>Configuration de l’environnement de développement du modèle de script

Pour utiliser le modèle de script WIA (Windows Image Acquisition), le fichier Wiascr.dll doit être installé et enregistré sur l’ordinateur.

> [!Note]  
> Ce système de script a été remplacé par la couche d’automatisation de l’acquisition d’images Windows (WIA). Voir [couche d’automatisation de l’acquisition d’image Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

Copiez ce fichier à partir du kit de développement logiciel (SDK) WIA dans le répertoire *% windir%*/system32 (par exemple, c : \\ Windows \\ system32). Sur la ligne de commande, accédez à ce répertoire, puis tapez **regsvr32 Wiascr.dll**.

Cela a pour conséquence d’entrer les informations nécessaires dans le registre système.

Vous êtes maintenant prêt à utiliser le modèle de script WIA.

 

 
