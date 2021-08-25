---
description: Effectue toutes les opérations nécessaires sur la mémoire tampon des métadonnées et libère l’objet ISpatialAudioMetadataItems spécifié.
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
title: 'ISpatialAudioMetadataWriter :: Close, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISpatialAudioMetadataWriter.Close
api_type:
- COM
api_location:
- spatialaudiometadata.h
ms.openlocfilehash: 4b29efb38cf11ba718a631f676323eb3db93aab042c70691dfb89ce957266e86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875419"
---
# <a name="ispatialaudiometadatawriterclose-method"></a>ISpatialAudioMetadataWriter :: Close, méthode

Effectue toutes les opérations nécessaires sur la mémoire tampon des métadonnées et libère l’objet [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Close();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne la valeur \_ OK. En cas d’échec, les codes de retour possibles incluent, sans s’y limiter, les valeurs indiquées dans le tableau suivant.



| Code de retour                                                                                                                     | Description                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ aucun \_ élément \_ ouvert**</dt> </dl>            | Le [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) fourni n’a pas été ouvert avec un appel à [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open).<br/> |
| <dl> <dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ aucun \_ élément \_ écrit**</dt> </dl>         | Aucun élément de métadonnées n’a été écrit dans le [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)fourni.<br/>                                              |
| <dl> <dt>**l' \_ élément SPTLAUD MD \_ CLNT \_ E \_ \_ doit \_ avoir des \_ commandes**</dt> </dl> | Aucune commande de métadonnées n’a été écrite dans le [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)fourni.<br/>                                           |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISpatialAudioMetadataWriter**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadatawriter)
</dt> </dl>

 

 




