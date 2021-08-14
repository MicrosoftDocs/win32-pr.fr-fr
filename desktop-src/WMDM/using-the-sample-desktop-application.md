---
title: Utilisation de l’exemple d’application de bureau
description: Utilisation de l’exemple d’application de bureau
ms.assetid: 5e3e5283-9e27-4f6a-93a9-84d84f2e875a
keywords:
- Windows Gestionnaire de périphériques de média, exemples
- Gestionnaire de périphériques, exemples
- applications de bureau, exemples
- Windows Media Gestionnaire de périphériques, exemple d’application de bureau
- Gestionnaire de périphériques, exemple d’application de bureau
- exemples, applications de bureau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b418458c9e6091b3e2002a30afb95abb77919d062667a9667a3aac9d4dad6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584165"
---
# <a name="using-the-sample-desktop-application"></a>Utilisation de l’exemple d’application de bureau

l’exemple d’application de bureau est une fenêtre de base à deux volets similaire à l’explorateur de Windows. Elle vous permet de parcourir le contenu d’un appareil à l’aide d’un affichage en arborescence des dossiers dans le volet gauche et des fichiers dans le volet droit. La racine de chaque arborescence de dossiers est considérée logiquement comme un appareil différent, bien que certains appareils puissent se représenter comme plusieurs objets (un pour chaque stockage racine). Pour lire les propriétés de base d’un dossier ou d’un fichier, cliquez avec le bouton droit sur l’objet et sélectionnez **Propriétés**.

Vous pouvez supprimer des fichiers sur l’appareil en sélectionnant un fichier dans le volet droit et en sélectionnant **supprimer** dans le menu **fichier** . Pour ajouter des fichiers multimédias à l’appareil, vous pouvez faire glisser des fichiers du bureau vers le volet droit du programme. Notez que les fichiers doivent être d’un format de média pris en charge par l’appareil. les fichiers de formats inacceptables (fichiers autres que des fichiers multimédias, tels que les fichiers .txt ou les formats de média non pris en charge par l’appareil) ne sont pas envoyés à l’appareil. (Notez que cette restriction est le programme ; Windows Le Gestionnaire de périphériques de média vous permet d’envoyer n’importe quel fichier à un appareil s’il est accepté par l’appareil.)

Pour capturer les événements de rappel envoyés à l’interface [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) , vous devez activer l’option « utiliser l’interface de l’opération » dans le menu **options** .

Le menu **options** vous permet également de choisir s’il faut utiliser plusieurs interfaces plus avancées avec les fonctionnalités prises en charge par les appareils avancés.

Le menu **conteneurs** contient des options pour vous permettre de créer une sélection ou un album. Pour créer une sélection, sélectionnez une ou plusieurs chansons sur l’appareil, puis cliquez sur **créer une sélection** dans le menu **conteneurs** . Cette fonctionnalité fonctionne uniquement sur les appareils MTP, car le code ne prend en charge que la création d’un fichier de sélection « virtuel ». (Une sélection virtuelle est une sélection spécifiée uniquement par des valeurs de métadonnées, plutôt que par un fichier physique, par exemple un fichier WPL.) L’appareil doit prendre en charge les sélections vides pour utiliser cette fonctionnalité.

Pour créer un album (une sélection avec une image associée), sélectionnez une ou plusieurs chansons sur l’appareil, puis cliquez sur **créer un album** dans le menu **conteneurs** . Une boîte de dialogue vous permet d’accéder à un fichier image sur votre ordinateur pour l’associer à l’album. De même que pour créer des sélections, l’application crée un fichier d’album « vide ». Si l’appareil ne prend pas en charge les albums vides, cette fonctionnalité ne fonctionnera pas.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Exemple d’application de bureau**](sample-desktop-application.md)
</dt> </dl>

 

 




