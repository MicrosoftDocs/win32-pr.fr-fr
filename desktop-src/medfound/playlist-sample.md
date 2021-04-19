---
description: Exemple de sélection
ms.assetid: ffe663ce-3e9a-4dfc-8904-6f055332c119
title: Exemple de sélection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f83d05762385d0de43a5d7f2bcd73cda2c6e2d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544735"
---
# <a name="playlist-sample"></a>Exemple de sélection

Montre comment utiliser Microsoft Media Foundation pour lire une séquence de fichiers audio dans une sélection. L’exemple utilise la [source de Sequencer](sequencer-source.md) pour créer et gérer la sélection.

> [!Note]  
> Cet exemple n’est plus inclus dans le kit de développement logiciel (SDK).

 

## <a name="apis-demonstrated"></a>API illustrées

Cet exemple illustre les interfaces de Media Foundation suivantes :

-   [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
-   [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
-   [**IMFSequencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)

## <a name="usage"></a>Utilisation

L’exemple playlist génère une application Windows.

-   Pour créer une sélection, sélectionnez **Ajouter à la sélection** dans le menu **fichier** . Dans la boîte de dialogue **ouvrir un fichier** , sélectionnez un ou plusieurs fichiers audio. Les fichiers sont ajoutés à la sélection.
-   Pour lire la séquence, cliquez sur **lire**.
-   Pour suspendre le segment actuel, cliquez sur **suspendre**.
-   Pour arrêter le segment actuel, cliquez sur **arrêter**.
-   Pour passer à un fichier, double-cliquez sur l’élément dans la sélection.
-   Pour supprimer un fichier de la sélection, sélectionnez l’élément dans la sélection. Sélectionnez ensuite **supprimer de la sélection** dans le menu **fichier** .

## <a name="requirements"></a>Configuration requise



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible aux emplacements suivants.



| Emplacement                                                     | Chemin d’accès/URL                                                   |
|--------------------------------------------------------------|------------------------------------------------------------|
| [SDK Windows](https://www.microsoft.com/download/details.aspx?id=8279) | *Racine* \\ du SDK Exemples \\ de \\ playlist mediafoundation Multimedia \\ |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple BasicPlayback](/previous-versions//bb970475(v=vs.85))
</dt> <dt>

[Exemples du kit de développement logiciel Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Source de Sequencer](sequencer-source.md)
</dt> </dl>

 

 
