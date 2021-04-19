---
title: Prise en charge d’images personnalisées pour les appareils
description: Prise en charge d’images personnalisées pour les appareils
ms.assetid: 0ccc327c-e953-4348-9802-705331b574ac
keywords:
- Lecteur Windows Media, prise en charge d’images personnalisées pour les appareils
- Lecteur Windows Media, prise en charge d’images pour les appareils
- prise en charge des images personnalisées par l’appareil
- prise en charge d’images personnalisées pour les appareils
- prise en charge des images pour les appareils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ffdf318df39935e844cc84919bb4d6e50cc259a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511699"
---
# <a name="custom-image-support-for-devices"></a>Prise en charge d’images personnalisées pour les appareils

> [!Note]  
> Cette section décrit une fonctionnalité du lecteur Windows Media 10 qui est disponible lors de l’utilisation du système d’exploitation Windows XP. Elle n’est peut-être pas disponible dans les versions ultérieures.

 

Les fabricants de périphériques peuvent fournir deux fichiers image spéciaux pour personnaliser la façon dont un appareil est représenté dans l’interface utilisateur du lecteur Windows Media 10. Ces deux fichiers sont les suivants :

-   DevIcon. fil. Fichier de format d’icône Windows qui représente le matériel de l’appareil. Cette image s’affiche dans le lecteur Windows Media 10 partout où une icône est utilisée pour représenter un appareil, comme la liste des appareils dans la fonctionnalité de **synchronisation** .
-   Dévlogo. fil. Fichier de format PNG qui représente le logo de l’entreprise du fabricant de l’appareil. Cette image s’affiche dans le lecteur Windows Media 10 Anywhere. la personnalisation de l’entreprise est utilisée, telle que la boîte de dialogue Configuration de l' **appareil** .

## <a name="general-guidelines-for-images"></a>Instructions générales pour les images

Les indications suivantes s’appliquent à la prise en charge d’images personnalisées en général :

-   Cette fonctionnalité est facultative. Les appareils qui ne fournissent pas d’images sont représentés par des images par défaut.
-   Cette fonctionnalité est prise en charge uniquement pour les appareils compatibles MTP.
-   Pour empêcher la modification des fichiers, il est recommandé de stocker les fichiers image dans un microprogramme ou un support de stockage protégé, et non avec des fichiers créés par l’utilisateur.
-   Les fichiers ne doivent pas être retournés aux clients Windows Media Gestionnaire de périphériques qui énumèrent le stockage racine de l’appareil. En outre, la suppression, le déplacement ou le changement de nom des fichiers doivent échouer.
-   Si l’appareil fournit plus d’un support de stockage, l’appareil doit retourner les fichiers image en réponse aux demandes d’ouverture de fichier à partir de n’importe quel support. Différentes icônes d’appareil peuvent être retournées à partir de chaque support de stockage.
-   Pour les clients Windows Media Gestionnaire de périphériques 1,2, ces images ont priorité sur les propriétés d’icône fournies par les mécanismes d’installation de Windows, tels que les propriétés de nœud d’appareil.
-   Les images ne doivent pas contenir d’informations nécessitant une localisation.
-   Pour les appareils multifonctions, seules les fonctionnalités de lecture musicale de Windows XP utilisent ces images.

## <a name="creating-the-device-icon-image"></a>Création de l’image de l’icône d’appareil

Le fichier image de l’icône de l’appareil, DevIcon. fil, doit contenir un fichier au format icône Windows. Les icônes de l’article MSDN [dans Win32](/previous-versions/ms997538(v=msdn.10)) décrivent comment créer un fichier de ce type. L’article MSDN [création d’icônes Windows XP](/previous-versions/ms997636(v=msdn.10)) fournit des règles de style pour les icônes Windows XP. Le fichier image icône d’appareil intègre douze images dans un fichier unique en fournissant quatre tailles différentes avec trois profondeurs de couleurs différentes.

Veillez à prêter une attention particulière aux recommandations suivantes :

-   Les tailles recommandées (en pixels) sont 16x16, 32x32, 48 et 256x256.
-   Les profondeurs de couleurs recommandés sont 24 bits avec un canal alpha 8 bits, 8 bits avec transparence de 1 bit et 4 bits avec transparence de 1 bit.
-   Utilisez l’angle de perspective et les recommandations d’ombre portée décrites dans les articles MSDN mentionnés précédemment.

Une fois que vous avez créé le fichier d’icône, il vous suffit de le renommer DevIcon. fil.

## <a name="creating-the-corporate-logo-image"></a>Création de l’image du logo de l’entreprise

Le fichier image du logo de l’entreprise, devlogo. fil, doit contenir un fichier au format PNG. Pour créer l’image, suivez les instructions ci-dessous :

-   Les dimensions maximales de l’image sont 150x32 pixels.
-   L’image doit prendre en charge la fusion alpha pour permettre une transition sans heurts entre l’interface utilisateur de Windows Media Player 10 et le logo.

Une fois que vous avez créé le fichier de logo de l’entreprise, il vous suffit de le renommer devlogo. fil.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecteur Windows Media**](windows-media-player.md)
</dt> </dl>

 

 