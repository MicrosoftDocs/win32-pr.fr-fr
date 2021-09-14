---
description: En interne, un métafichier est un tableau de structures de longueur variable appelées enregistrements de métafichier.
ms.assetid: 222f9b8b-d759-49f9-a3ea-ac59f85263b8
title: À propos des sous-fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdba8b3c0a13c6c5799563b05e189829a0734427
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126914359"
---
# <a name="about-metafiles"></a>À propos des sous-fichiers

En interne, un métafichier est un tableau de structures de longueur variable appelées *enregistrements de métafichier*. Les premiers enregistrements du métafichier spécifient des informations générales, telles que la résolution de l’appareil sur lequel l’image a été créée, les dimensions de l’image, etc. Les enregistrements restants, qui constituent le bloc de tout métafichier, correspondent aux fonctions GDI (Graphics Device Interface) requises pour dessiner l’image. Ces enregistrements sont stockés dans le métafichier après la création d’un contexte de périphérique de métafichier spécial. Ce contexte de périphérique de métafichier est ensuite utilisé pour toutes les opérations de dessin nécessaires à la création de l’image. Lorsque le système traite une fonction GDI associée à un contexte de périphérique de métafichier, il convertit la fonction en données appropriées et stocke ces données dans un enregistrement ajouté au métafichier.

Une fois qu’une image est terminée et que le dernier enregistrement est stocké dans le métafichier, vous pouvez transmettre le métafichier à une autre application en procédant comme suit :

-   Utilisation du presse-papiers
-   Incorporation dans un autre fichier
-   Stockage sur disque
-   Sa lecture à plusieurs reprises

Un métafichier est *lu* lorsque ses enregistrements sont convertis en commandes de périphérique et traités par l’appareil approprié.

Il existe deux types de fichiers :

-   [Fichiers de format amélioré](enhanced-format-metafiles.md)
-   [Windows-fichiers de format](windows-format-metafiles.md)

 

 



