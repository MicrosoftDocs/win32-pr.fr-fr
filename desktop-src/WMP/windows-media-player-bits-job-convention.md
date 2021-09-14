---
title: Lecteur Windows Media Convention de travail BITS
description: Lecteur Windows Media pouvez télécharger et ajouter automatiquement des éléments multimédias numériques à la bibliothèque si vous utilisez Service de transfert intelligent en arrière-plan (BITS).
ms.assetid: 643faba7-9af2-4292-8d92-e321d7690a5b
keywords:
- Lecteur Windows Media des magasins en ligne, Service de transfert intelligent en arrière-plan (BITS)
- magasins en ligne, Service de transfert intelligent en arrière-plan (BITS)
- type 2 magasins en ligne, Service de transfert intelligent en arrière-plan (BITS)
- Service de transfert intelligent en arrière-plan (BITS)
- BITS (Service de transfert intelligent en arrière-plan)
- Lecteur Windows Media les magasins en ligne, convention de travail BITS
- magasins en ligne, Convention de travail BITS
- type 2 magasins en ligne, Convention de travail BITS
- Convention de travail BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85278593ce151f46370ca491ccac8e1645f9bb70
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013182"
---
# <a name="windows-media-player-bits-job-convention"></a>Lecteur Windows Media Convention de travail BITS

Lecteur Windows Media pouvez télécharger et ajouter automatiquement des éléments multimédias numériques à la bibliothèque si vous utilisez [Service de transfert intelligent en arrière-plan (BITS)](/windows/desktop/Bits/background-intelligent-transfer-service-portal). Pour tirer parti de cette fonctionnalité, vous devez ajouter votre travail à la file d’attente de transfert BITS et appeler **méthode ibackgroundcopyjob :: SetDescription**, en fournissant une chaîne de description qui utilise le format correct.

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

## <a name="syntax"></a>Syntaxe

``` syntax
::WMP_JOB:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="serviceId"></span><span id="serviceid"></span><span id="SERVICEID"></span>*serviceId*
</dt> <dd>

valeur 32 bits générée de manière aléatoire que Lecteur Windows Media utilise pour identifier le service.

</dd> <dt>

<span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>*Moteur*
</dt> <dd>

Nom du fournisseur. Cette valeur doit correspondre à un nom de clé de magasin en ligne valide.

</dd> <dt>

<span id="AlbumArtist"></span><span id="albumartist"></span><span id="ALBUMARTIST"></span>*AlbumArtist*
</dt> <dd>

Nom de l’artiste principal de l’album.

</dd> <dt>

<span id="AlbumTitle"></span><span id="albumtitle"></span><span id="ALBUMTITLE"></span>*AlbumTitle*
</dt> <dd>

Titre de l’album.

</dd> <dt>

<span id="TrackNumber"></span><span id="tracknumber"></span><span id="TRACKNUMBER"></span>*TrackNumber*
</dt> <dd>

Numéro de piste du CD.

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>*Bonhomme*
</dt> <dd>

Titre du contenu.

</dd> <dt>

<span id="Duration"></span><span id="duration"></span><span id="DURATION"></span>*Macauley*
</dt> <dd>

Durée du contenu.

</dd> <dt>

<span id="Rating"></span><span id="rating"></span><span id="RATING"></span>*Audience*
</dt> <dd>

Évaluation du contenu.

</dd> </dl>

## <a name="remarks"></a>Remarques

lorsque Lecteur Windows Media 10 ou une version ultérieure utilise le service BITS pour télécharger du contenu, il énumère les travaux dans la file d’attente de transfert et inspecte la chaîne de description de chaque travail. si la chaîne de description correspond à la convention attendue, Lecteur Windows Media télécharge le contenu.

Vous devez ajouter un seul fichier multimédia numérique à télécharger pour chaque travail BITS.

une fois que vous avez démarré une tâche BITS à l’aide de cette convention, vous devez laisser Lecteur Windows Media terminer la tâche. Lecteur Windows Media supprime également la tâche de la file d’attente BITS, déplace le fichier téléchargé vers l’emplacement où l’extraction de musique est enregistrée et ajoute le fichier téléchargé à la bibliothèque.

Le paramètre *ServiceId* doit contenir une valeur différente de zéro 32 bits. Nous vous recommandons d’utiliser la fonction [**CryptGenRandom**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom) pour créer cette valeur.

Le nom de fichier que vous spécifiez à l’aide du paramètre *LocalName* de **méthode ibackgroundcopyjob :: AddFile** doit avoir une extension de nom de fichier. WMA,. wmv, .mp3 ou. ASF.

Les paramètres restants sont conçus pour contenir des valeurs de métadonnées relatives au contenu. Vous pouvez récupérer ces valeurs à partir de votre page Web de boutique en ligne à l’aide de **DownloadItem. getItemInfo**. Vous pouvez récupérer la collection de téléchargements appropriée en appelant **downloadmanager. getDownloadCollection** et  en fournissant ServiceId *comme paramètre de* l’ensemble.

Lecteur Windows Media inspecte la file d’attente BITS régulièrement pendant que le lecteur est en cours d’exécution. pour vous assurer que Lecteur Windows Media vérifie la file d’attente BITS pour les travaux de téléchargement, vous devez créer une valeur dans la sous-clé de registre suivante :

**HKEY \_ Current \_ User \\ Software \\ Microsoft \\ MediaPlayer \\ services**

La valeur doit être créée comme suit.



| Name                | Type      | Description                                                                                                                                                                                                          |
|---------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **RefreshDownload** | **DWORD** | spécifie si Lecteur Windows Media doit inspecter la file d’attente BITS pour les travaux de téléchargement. Si la valeur est égale à zéro, le lecteur n’inspecte pas la file d’attente BITS. Le joueur doit inspecter la file d’attente si la valeur est différente de zéro. |



 

vous pouvez utiliser la syntaxe alternative suivante pour ajouter des tâches BITS qui Lecteur Windows Media ne se termine pas, mais pour lesquelles il affiche simplement des informations d’état :

``` syntax
::WMP_STATUS:1:serviceId:Provider:AlbumArtist:AlbumTitle:TrackNumber:Title:Duration:Rating
```

Lorsque vous utilisez la syntaxe précédente, vous devez écrire du code pour terminer le téléchargement BITS, organiser le contenu sur l’ordinateur de l’utilisateur et ajouter le contenu à la bibliothèque, si vous le souhaitez.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[CryptGenRandom](/windows/desktop/api/wincrypt/nf-wincrypt-cryptgenrandom)
</dt> <dt>

[**DownloadItem. getItemInfo**](downloaditem-getiteminfo.md)
</dt> <dt>

[**DownloadManager.getDownloadCollection**](downloadmanager-getdownloadcollection.md)
</dt> <dt>

[**Référence pour les magasins en ligne de type 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 