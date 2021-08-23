---
title: Interaction avec IMAPi
description: Les étapes suivantes décrivent une interaction classique entre une application et IMAPi.
ms.assetid: e57a86c4-7e27-40cf-a9c1-081b3f20d9d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab97d1a9d76d1e82dab64fb777ef5207d3d47560b2a889981c698ab78e3622b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726989"
---
# <a name="interacting-with-imapi"></a>Interaction avec IMAPi

Les étapes suivantes décrivent une interaction classique entre une application et IMAPi.

1.  Créez une instance de **MSDiscMasterObj** (à l’aide de **CoCreateInstance**, de pointeurs intelligents d’une importation, etc.) et demandez l’interface [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) .
2.  Pour obtenir l’accès à IMAPi, appelez [**IDiscMaster :: Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open). Si cet appel a échoué, l’application dispose d’un accès complet à toutes les interfaces et méthodes implémentées dans **MSDiscMasterObj**.
3.  Récupérez l’énumérateur de format de disque maître à l’aide de [**EnumDiscMasterFormats**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscmasterformats). Énumérez l’ensemble de formats pris en charge par l’objet maître Disc, puis sélectionnez le format actif. Les formats retournés à partir de l’énumérateur sont les IID des interfaces pour [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) et [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster).
4.  Récupérez l’énumérateur de l’enregistreur de disque à l’aide de [**EnumDiscRecorders**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscrecorders). Énumérez la liste des enregistreurs de disques pris en charge (spécifiques au format actif), puis sélectionnez l’enregistreur actif. L’interface [**IDiscRecorder**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) représente un appareil physique.
5.  Utilisez [**IDiscMaster ::P rogressadvise**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-progressadvise) pour vous inscrire pour les rappels de progression.
6.  Utilisez l’interface pour le format sélectionné pour générer le contenu. Les builds de contenu sont incrémentielles, de sorte que les pistes ou le contenu du dossier peuvent être ajoutés à un disque par morceau. La création de ce contenu est appelée *intermédiaire d’une image*. Le contenu de l’image intermédiaire ne peut pas être supprimé de façon incrémentielle (vous ne pouvez pas supprimer une piste qui a été ajoutée), mais il est possible de supprimer le contenu d’une image intermédiaire pour que la mise en lots puisse recommencer. Utilisez [**IDiscMaster :: ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) pour redémarrer la mise en lots.

* * Pour l’audio : * *

1.  Utilisez [**IRedbookDiscMaster :: CreateAudioTrack**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-createaudiotrack) pour indiquer qu’une nouvelle piste audio est démarrée sur le disque.
2.  Utilisez [**IRedbookDiscMaster :: AddAudioTrackBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-addaudiotrackblocks) pour ajouter des données audio brutes à une piste. L’application peut utiliser [**GetAvailableAudioTrackBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getavailableaudiotrackblocks), [**GetTotalAudioBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-gettotalaudioblocks)et [**GetUsedAudioBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getusedaudioblocks) pour récupérer des informations statistiques.
3.  Utilisez [**IRedbookDiscMaster :: CloseAudioTrack**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-closeaudiotrack) pour fermer une piste audio.
4.  Répétez les étapes 1-3 jusqu’à ce que l’espace soit insuffisant ou que toutes les pistes audio aient été écrites.

* * Pour les données : * *

1.  Utilisez [**IJolietDiscMaster :: AddData**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-adddata) pour ajouter le contenu d’un dossier à l’image. Les éléments d’un dossier sont placés à la racine du fichier image. Utilisez [**GetTotalDataBlocks**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-gettotaldatablocks) et [**GetUsedDataBlocks**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-getuseddatablocks) pour récupérer des informations statistiques.
2.  Répétez l’étape ci-dessus jusqu’à ce que l’espace soit insuffisant ou que toutes les données aient été ajoutées.

* * Pour tous les disques : * *

1.  Utilisez [**IDiscMaster :: RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) pour enregistrer le disque.
2.  Fermez la session IMAPi à l’aide de [**IDiscMaster :: Close**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-close). La fermeture de la session efface le contenu de la dissimulation de disque.

 

 




