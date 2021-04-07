---
title: Création d’un fichier à partir de flux existants
description: Création d’un fichier à partir de flux existants
ms.assetid: 5149a766-7809-42b7-8e5c-b67b847b9218
keywords:
- AVISave fonction)
- AVISaveV fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc422d2170ccd49b8a9746666db7ebbcd7dff14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939885"
---
# <a name="creating-a-file-from-existing-streams"></a>Création d’un fichier à partir de flux existants

Une façon de créer un fichier contenant des flux de données consiste à combiner des flux existants dans un nouveau fichier. Les flux qui fournissent des données pour le nouveau fichier peuvent résider dans la mémoire ou dans un ou plusieurs fichiers.

Vous pouvez générer un fichier à partir de plusieurs flux à l’aide de la fonction [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) . Cette fonction crée un fichier et écrit les flux de données spécifiés dans sa séquence d’appel dans le fichier. La séquence d’appel pour **AVISave** utilise un nombre variable d’arguments qui incluent des interfaces pour les flux combinés dans le nouveau fichier.

Vous pouvez également combiner des flux de données dans un nouveau fichier à l’aide de la fonction [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) . Cette fonction fournit les mêmes fonctionnalités que **AVISave**, mais quand vous utilisez **AVISaveV**, votre application spécifie les flux de données sous forme de tableau, et non comme un nombre variable d’arguments.

Vous pouvez créer une boîte de dialogue dans laquelle l’utilisateur peut sélectionner des paramètres de compression pour le nouveau fichier à l’aide de la fonction [**AVISaveOptions**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions) . La boîte de dialogue affiche les paramètres de compression actuels et permet à l’utilisateur de les modifier. Les modifications des paramètres de compression sont stockées dans une structure [**AVICOMPRESSOPTIONS**](/windows/desktop/api/Vfw/ns-vfw-avicompressoptions) .

Vous pouvez également inclure une fonction de rappel avec [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) et [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) que votre application peut utiliser pour afficher la progression de l’écriture du fichier et, si nécessaire, permettre à l’utilisateur d’annuler l’opération d’enregistrement. Vous pouvez inclure l’adresse de la fonction de rappel dans la séquence d’appel de **AVISave** ou **AVISaveV**.

Vous pouvez laisser l’utilisateur sélectionner un nom de fichier pour le nouveau fichier à l’aide de la fonction [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) . Cette fonction affiche la boîte de dialogue Enregistrer sous dans laquelle l’utilisateur peut afficher un aperçu du premier flux (normalement le flux vidéo) d’un fichier AVI.

Vous pouvez créer un pointeur d’interface de fichier (et un fichier virtuel) pour un groupe de flux à l’aide de la fonction [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) . D’autres fonctions AVIFile peuvent utiliser le pointeur d’interface de fichier retourné par cette fonction pour accéder aux flux dans le fichier virtuel. Une fois que vous avez fini d’utiliser le fichier virtuel, supprimez le pointeur d’interface de fichier à l’aide de la fonction [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) .

> [!Note]  
> Pour réduire la dégradation des images et du son, évitez de compresser un fichier AVI plusieurs fois. Combinez des éléments vidéo non compressés dans votre système de montage, puis compressez le produit final. Pour plus d’informations sur les options de compression, consultez [Video Compression Manager](video-compression-manager.md).

 

 

 




