---
description: Utilisation des types de médias MFT
ms.assetid: 16c270ee-f246-4222-97e9-d8d0fe009155
title: Utilisation des types de médias MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98bfc996704f6069ca1d16570b33f456ea1cc115
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104211226"
---
# <a name="working-with-mft-media-types"></a>Utilisation des types de médias MFT

Un type de média est un moyen de décrire le format d’un flux multimédia. Dans Media Foundation, les types de média sont représentés par l’interface **IMFMediaType** . Cette interface hérite de l’interface **IMFAttributes** . Les détails d’un type de média sont spécifiés en tant qu’attributs.

Pour créer un type de média, appelez la fonction **MFCreateMediaType** . Cette fonction retourne un pointeur vers l’interface **IMFMediaType** . Initialement, le type de média n’a pas d’attribut.

Le kit de développement logiciel (SDK) Media Foundation fournit plusieurs fonctions d’assistance pour l’initialisation des types de média à partir de structures de format. Par exemple, la fonction **MFInitMediaTypeFromVideoInfoHeader** Initialise un type de vidéo à partir d’une structure **VIDEOINFOHEADER** , et la fonction **MFInitMediaTypeFromWaveFormatEx** Initialise un type de vidéo à partir d’une structure **WAVEFORMATEX** ou **WAVEFORMATEXTENSIBLE** .

Les types de format utilisés par les codecs sont généralement limités à ceux décrits par les structures **VIDEOINFOHEADER** et **WAVEFORMATEX** .

Vous trouverez plus d’informations sur la création et l’accès aux Media Foundation types de média dans la documentation du kit de développement logiciel (SDK) Media Foundation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du codec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



