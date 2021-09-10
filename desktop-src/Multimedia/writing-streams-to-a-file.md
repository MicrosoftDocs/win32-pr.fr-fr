---
title: écriture d’Flux dans un fichier
description: écriture d’Flux dans un fichier
ms.assetid: a3766f8c-aaa6-4fc5-a306-54aee71018f1
keywords:
- AVIFileCreateStream fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 370df08534bbdde870f6d28c828d47935abd80db
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369311"
---
# <a name="writing-streams-to-a-file"></a>écriture d’Flux dans un fichier

Vous pouvez également créer un fichier contenant des flux de données en écrivant un nouveau flux de données dans un fichier.

Vous pouvez créer un flux dans un nouveau fichier ou un fichier existant à l’aide de la fonction [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) . Cette fonction définit un nouveau flux en fonction des caractéristiques décrites dans une structure [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) , crée une interface de flux pour le nouveau flux, incrémente le décompte de références du flux et retourne l’adresse du pointeur d’interface de flux.

Avant d’écrire le contenu du flux, vous devez spécifier le format de flux. Vous pouvez définir le format de flux à l’aide de la fonction [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) . Lorsque vous définissez le format d’un flux vidéo, vous devez fournir cette fonction avec une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenant les informations appropriées. Lorsque vous définissez le format d’un flux audio, vous devez fournir une structure [**WaveFormat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) ou [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) contenant les informations appropriées. Les informations que vous devez fournir à la fonction pour d’autres types de flux dépendent du type de flux et du gestionnaire de flux.

Vous pouvez écrire le contenu multimédia dans un flux à l’aide de la fonction [**AVIStreamWrite**](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite) . Cette fonction copie les données brutes à partir d’une mémoire tampon fournie par l’application dans le flux spécifié. Le gestionnaire de fichiers AVI par défaut ajoute des informations à la fin d’un flux. Le gestionnaire WAVE par défaut peut écrire des données Waveform-Audio dans un flux, ainsi qu’à la fin d’un flux.

Vous pouvez écrire des informations supplémentaires sur le fichier ou le flux qui n’est pas inclus dans la fonction [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) ou [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) à l’aide des fonctions [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) et [**AVIStreamWriteData**](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata) . Vous pouvez enregistrer les données qui s’appliquent à l’ensemble du fichier, telles que les informations de copyright et l’historique des modifications, à l’aide de **AVIFileWriteData**. Vous pouvez enregistrer des informations spécifiques au flux, telles que les paramètres de compression et de décompression, à l’aide de **AVIStreamWriteData**. Les informations supplémentaires sont stockées dans des blocs distincts au sein du fichier.

Vous pouvez fermer le flux une fois que vous avez fini d’écrire dans le nouveau flux à l’aide de la fonction [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) . Cette fonction efface les mémoires tampons utilisées pour enregistrer les données de flux, puis termine et ferme tous les blocs de données incomplets dans le fichier.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Opérations de flux](stream-operations.md)
</dt> </dl>

 

 