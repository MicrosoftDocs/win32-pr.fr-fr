---
title: publication avec la résolution de & d’inscription de Windows sockets
description: Windows Les services de sockets peuvent utiliser les API d’inscription et de résolution (RnR) pour publier des services et Rechercher des services publiés avec RnR.
ms.assetid: 95c16d0b-abbc-4407-ac31-d7de0b25bd74
ms.tgt_platform: multiple
keywords:
- Windows Inscription et résolution des sockets Active Directory, publication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a071a37d1d017e4c034f3eaab175889fdfcd1789d9f48aeac2c2943dfc8b4f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184923"
---
# <a name="publishing-with-windows-sockets-registration--resolution"></a>publication avec la résolution de & d’inscription de Windows sockets

Windows Les services de sockets peuvent utiliser les API d’inscription et de résolution (RnR) pour publier des services et Rechercher des services publiés avec RnR. La publication RnR se produit en deux étapes. La première étape installe une classe de service qui associe un GUID à un nom pour le service. La classe de service peut contenir des données de configuration spécifiques au service. Les services peuvent ensuite se publier eux-mêmes en tant qu’instances de la classe de service. Une fois publiées, les clients peuvent interroger le service d’annuaire pour les instances d’une classe donnée à l’aide des API RnR et sélectionner une instance à lier. Quand une classe n’est plus nécessaire, elle peut être supprimée.

 

 




