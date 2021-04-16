---
title: Publication avec l’inscription Windows Sockets & résolution
description: Les services Windows Sockets peuvent utiliser les API d’inscription et de résolution (RnR) pour publier des services et Rechercher des services publiés avec RnR.
ms.assetid: 95c16d0b-abbc-4407-ac31-d7de0b25bd74
ms.tgt_platform: multiple
keywords:
- Inscription et résolution Windows Sockets Active Directory, publication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e722d83447bd97e3964a9a0cc85df45ffd27faba
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/04/2019
ms.locfileid: "104462631"
---
# <a name="publishing-with-windows-sockets-registration--resolution"></a>Publication avec l’inscription Windows Sockets & résolution

Les services Windows Sockets peuvent utiliser les API d’inscription et de résolution (RnR) pour publier des services et Rechercher des services publiés avec RnR. La publication RnR se produit en deux étapes. La première étape installe une classe de service qui associe un GUID à un nom pour le service. La classe de service peut contenir des données de configuration spécifiques au service. Les services peuvent ensuite se publier eux-mêmes en tant qu’instances de la classe de service. Une fois publiées, les clients peuvent interroger le service d’annuaire pour les instances d’une classe donnée à l’aide des API RnR et sélectionner une instance à lier. Quand une classe n’est plus nécessaire, elle peut être supprimée.

 

 




