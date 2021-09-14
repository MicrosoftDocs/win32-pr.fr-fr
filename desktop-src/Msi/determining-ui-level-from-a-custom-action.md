---
description: Une action personnalisée dans une table de séquence d’interface utilisateur ou un fichier exécutable externe peut nécessiter le niveau d’interface utilisateur actuel de l’installation.
ms.assetid: d1ddadd5-b4ec-4c7c-aee4-b2d688a57eb4
title: Détermination du niveau d’interface utilisateur à partir d’une action personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2586cd03bfda2b22e721c0ae9c3393d4bbc525a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091605"
---
# <a name="determining-ui-level-from-a-custom-action"></a>Détermination du niveau d’interface utilisateur à partir d’une action personnalisée

Une action personnalisée dans une table de séquence d’interface utilisateur ou un fichier exécutable externe peut nécessiter le niveau d’interface utilisateur actuel de l’installation. Par exemple, une action personnalisée qui a une boîte de dialogue ne doit afficher la boîte de dialogue que lorsque le niveau de l’interface utilisateur est une interface utilisateur complète ou une interface utilisateur réduite, mais ne doit pas afficher la boîte de dialogue si le niveau d’interface utilisateur est interface utilisateur de base ou aucun. Vous devez utiliser la propriété [**UILevel**](uilevel.md) pour déterminer le niveau actuel de l’interface utilisateur. Vous ne pouvez pas appeler [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) à partir d’une action personnalisée et il n’est pas possible de modifier la propriété de niveau interface utilisateur à partir d’une action personnalisée.

Il est recommandé que les actions personnalisées n’utilisent pas le niveau d’interface utilisateur comme condition pour envoyer des messages d’erreur au programme d’installation, car cela peut interférer avec la journalisation et les messages externes.

 

 



