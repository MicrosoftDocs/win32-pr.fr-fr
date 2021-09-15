---
title: Sélection des fonctionnalités de profil
description: Sélection des fonctionnalités de profil
ms.assetid: 5e09000d-1417-43aa-9e9c-0aff536d52b7
keywords:
- profils, sélection de fonctionnalités
- profils, sélection des fonctionnalités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769b10387bb4fb660c31678b406090cfc7e42743
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404195"
---
# <a name="selecting-profile-features"></a>Sélection des fonctionnalités de profil

Le tableau suivant répertorie les fonctionnalités de profil et décrit si vous ne souhaitez pas les utiliser.



| Fonctionnalité                            | Quand l’utiliser                                                                                                                                                                                                                                                                                                                | Quand ne pas utiliser                                                                                                                                                                                                                                                                    |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exclusion mutuelle par vitesse de transmission (MBR) | Le fichier sera diffusé en continu à une audience dont les vitesses de connexion varient d’un utilisateur à l’utilisateur (par exemple, des fichiers remis sur Internet).                                                                                                                                                                              | Le fichier ne sera pas diffusé sur un réseau. Le fichier sera diffusé sur un réseau avec une bande passante disponible de manière cohérente (par exemple, les fichiers livrés sur un réseau local d’entreprise).<br/>                                                              |
| Exclusion mutuelle par langue       | Le fichier contient des flux qui dupliquent les mêmes données dans différentes langues. (Par exemple, un film nommé en plusieurs langages aurait la piste audio encodée sous forme de flux s’excluant mutuellement.)                                                                                                                         | Le fichier contient uniquement des flux dans une seule langue. Si le fichier contient uniquement des flux qui doivent être modifiés pour des langues individuelles, il peut être plus simple de créer un fichier pour chaque langue (par exemple, pour un film d’apprentissage avec un grand nombre de texte dans le flux vidéo).<br/> |
| Exclusion mutuelle par présentation   | Vous souhaitez fournir une vidéo dans plusieurs proportions. Par exemple, un fichier peut contenir la même vidéo formatée pour la télévision et le format de grand écran de théâtre d’origine.                                                                                                                                     | Il n’existe qu’une seule version de chaque flux vidéo.                                                                                                                                                                                                                                    |
| Partage de bande passante                  | Le fichier est diffusé en continu et comporte au moins deux flux qui, lorsqu’ils sont combinés, utilisent moins de bande passante que les valeurs de vitesse de transmission des deux flux ajoutés ensemble. Étant donné que la vitesse de transmission d’un flux est essentiellement la bande passante maximale requise pour le flux, certains flux peuvent avoir des périodes de transfert de données inférieur. | Le fichier ne sera pas diffusé sur un réseau. Tous les flux ont des vitesses de transmission cohérentes.<br/>                                                                                                                                                                                     |
| Hiérarchisation des flux              | Le fichier est diffusé en continu et certains flux sont plus importants que d’autres.                                                                                                                                                                                                                                                 | Le fichier ne sera pas diffusé sur un réseau. Tous les flux sont d’une importance égale.<br/>                                                                                                                                                                                       |
| Extensions d’unité de données               | Il existe des informations importantes relatives aux exemples dans un flux de données qui doivent être conservées avec les exemples.                                                                                                                                                                                                                      | Le fichier est destiné à être remis via une bande passante limitée. Dans ce cas, les extensions d’unité de données peuvent utiliser une charge trop importante.                                                                                                                                                    |



 

Il est également important de prendre en compte les fonctionnalités du codec que vous souhaitez utiliser avec votre fichier lors de la création d’un profil. Pour plus d’informations, consultez [fonctionnalités du codec](codec-features.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Fonctionnalités des fichiers ASF**](asf-file-features.md)
</dt> <dt>

[**Conception de profils**](designing-profiles.md)
</dt> </dl>

 

 





