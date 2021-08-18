---
title: Chargement d’un caractère
description: Chargement d’un caractère
ms.assetid: 973de75b-b530-40c6-896d-e2ab0755ae2c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78d796df5c1699b405e8cae1dbae0e7d7d8d37932aa50534fa7331a458dc54a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748402"
---
# <a name="loading-a-character"></a>Chargement d’un caractère

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Pour animer un caractère, vous devez d’abord charger le caractère. Utilisez la méthode [**Load**](load-method.md) pour charger les données du caractère. Microsoft agent prend en charge deux formats de données de caractères et d’animation : un seul fichier structuré et des fichiers distincts. En général, vous utilisez le format de fichier unique (. ACS) lorsque les données sont stockées localement. Le format de fichier multiple (. ACF,. CCN) fonctionne mieux lorsque vous souhaitez télécharger des animations individuellement, par exemple lors de l’accès à des animations à partir d’un serveur HTTP.

Une application cliente ne peut charger qu’une seule instance du même caractère. Toute tentative de chargement du même caractère plusieurs fois échoue. Toutefois, une application peut avoir plusieurs instances du même caractère chargées en fournissant des connexions distinctes à Microsoft Agent. Par exemple, une application peut charger le même caractère à partir de deux copies du contrôle Microsoft Agent.

Vous pouvez également définir vos propres caractères en vue de les utiliser avec Microsoft Agent. vous pouvez utiliser n’importe quel outil de rendu que vous préférez créer les images, à condition de vous retrouver avec Windows fichiers de format bitmap. Pour assembler et compiler les images d’un caractère dans des animations en vue de les utiliser avec Microsoft Agent, utilisez l’éditeur de caractères Microsoft Agent. Cet outil vous permet de définir les propriétés par défaut d’un caractère et de définir des animations pour ce caractère. L’éditeur de caractères Microsoft agent vous permet également de sélectionner le format de fichier approprié lorsque vous créez un caractère.

 

 




