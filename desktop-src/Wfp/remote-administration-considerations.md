---
description: Certaines considérations sont spécifiques aux systèmes administrés à distance.
ms.assetid: bfdf121e-9b4e-4323-82ec-9bd32531caad
title: Considérations relatives à l’administration à distance WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b3106a02aa4098d2814a955e6582d6e8f1c79f7f161a6875891e13a0db71a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098589"
---
# <a name="wfp-remote-administration-considerations"></a>Considérations relatives à l’administration à distance WFP

Certaines considérations sont spécifiques aux systèmes administrés à distance. Tout d’abord, lorsque l’installation du logiciel est déployée à distance (à l’aide de SMS ou de MSI), des boîtes de dialogue d’erreur WFP s’affichent à l’écran d’un administrateur connecté localement (le cas échéant), et non au service d’installation. Deuxièmement, si un administrateur se connecte à un serveur Terminal Server à distance et installe une application qui remplace les fichiers système protégés, les boîtes de dialogue d’erreur WFP s’affichent uniquement dans la console principale, et non dans la fenêtre distante de l’administrateur.

Pour ces raisons, WFP supprime ses boîtes de dialogue d’erreur jusqu’à ce qu’un administrateur se connecte localement. Les administrateurs distants peuvent trouver des erreurs de remplacement de fichier dans le journal des événements système.

**Windows Vista et Windows Server 2008 :** L’administration à distance de WFP n’est pas prise en charge.

 

 



